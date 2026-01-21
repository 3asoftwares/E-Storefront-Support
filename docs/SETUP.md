# Setup Guide

Development environment setup for E-Storefront Support.

---

## 📑 Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Development](#development)
- [Configuration](#configuration)
- [Common Tasks](#common-tasks)

---

## 📋 Prerequisites

### Required Software

| Software | Version | Purpose            |
| -------- | ------- | ------------------ |
| Node.js  | 18+     | JavaScript runtime |
| npm/yarn | Latest  | Package manager    |
| Git      | Latest  | Version control    |

### Recommended Extensions (VS Code)

- **Live Server** - Local development server
- **SCSS IntelliSense** - SCSS autocomplete
- **Prettier** - Code formatting
- **ESLint** - JavaScript linting

---

## 🚀 Installation

### 1. Clone Repository

```bash
git clone https://github.com/3asoftwares/E-Storefront-Support.git
cd E-Storefront-Support
```

### 2. Install Dependencies

```bash
# Using npm
npm install

# Using yarn
yarn install
```

### 3. Start Development Server

```bash
# Start both SCSS watcher and live server
yarn dev

# Or run separately:
yarn sass   # Watch and compile SCSS
yarn start  # Start live-server on port 3003
```

### 4. Open in Browser

Navigate to: `http://localhost:3003`

---

## 📁 Project Structure

```
E-Storefront-Support/
├── index.html           # Main entry point
├── package.json         # Dependencies and scripts
├── vercel.json          # Vercel deployment config
├── css/
│   └── main.css         # Compiled CSS (generated)
├── scss/
│   ├── main.scss        # Main SCSS file
│   ├── _variables.scss  # SCSS variables
│   ├── _mixins.scss     # SCSS mixins
│   └── _components.scss # Component styles
├── js/
│   └── app.js           # Main JavaScript file
├── images/
│   └── ...              # Static images
└── docs/
    ├── README.md        # Documentation index
    ├── SETUP.md         # This file
    ├── ARCHITECTURE.md  # System architecture
    ├── ENVIRONMENT.md   # Environment config
    ├── CONTRIBUTING.md  # Contribution guide
    ├── DEPLOYMENT.md    # Deployment guide
    └── CHANGELOG.md     # Version history
```

---

## 🛠️ Development

### Available Scripts

| Command          | Description                      |
| ---------------- | -------------------------------- |
| `yarn dev`       | Start SCSS watcher + live server |
| `yarn start`     | Start live-server only           |
| `yarn sass`      | Watch SCSS and compile to CSS    |
| `yarn build`     | Build CSS for production         |
| `yarn build:css` | Compile and minify SCSS          |

### SCSS Development

Edit files in `scss/` folder. Changes auto-compile to `css/main.css`:

```bash
# Watch mode (auto-compile on save)
yarn sass

# One-time build
yarn build:css
```

### JavaScript Development

Edit `js/app.js`. Live-server auto-reloads on changes.

---

## ⚙️ Configuration

### API Configuration

Update the GraphQL API endpoint in `js/app.js`:

```javascript
const API_CONFIG = {
    graphqlUrl: 'https://api.example.com/graphql',
    timeout: 10000,
};
```

### Environment Variables

Create environment-specific configs in `js/config.js`:

```javascript
const ENV = {
    development: {
        apiUrl: 'http://localhost:3000/graphql',
        debug: true,
    },
    production: {
        apiUrl: 'https://api.3asoftwares.com/graphql',
        debug: false,
    },
};

const config = ENV[window.location.hostname === 'localhost' ? 'development' : 'production'];
```

### Bootstrap Customization

Customize Bootstrap in `scss/_variables.scss`:

```scss
// Override Bootstrap defaults
$primary: #4f46e5;
$secondary: #6b7280;
$border-radius: 0.5rem;

// Then import Bootstrap
@import 'bootstrap/scss/bootstrap';
```

---

## 🔧 Common Tasks

### Add New Page

1. Create HTML file in root:

    ```html
    <!-- new-page.html -->
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <link rel="stylesheet" href="css/main.css" />
        </head>
        <body>
            <!-- Content -->
            <script src="js/app.js"></script>
        </body>
    </html>
    ```

2. Add styles in `scss/`:

    ```scss
    // scss/_new-page.scss
    .new-page {
        // styles
    }
    ```

3. Import in `main.scss`:
    ```scss
    @import 'new-page';
    ```

### Add New Component

1. Create component styles:

    ```scss
    // scss/_components/_card.scss
    .support-card {
        background: white;
        border-radius: 0.5rem;
        padding: 1rem;
    }
    ```

2. Add HTML:
    ```html
    <div class="support-card">
        <h3>Card Title</h3>
        <p>Card content</p>
    </div>
    ```

### Make API Call

```javascript
// js/app.js
async function submitTicket(data) {
    const response = await fetch(API_CONFIG.graphqlUrl, {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json',
        },
        body: JSON.stringify({
            query: `
        mutation CreateTicket($input: TicketInput!) {
          createTicket(input: $input) {
            id
            status
          }
        }
      `,
            variables: { input: data },
        }),
    });

    return response.json();
}
```

---

## 🐛 Troubleshooting

### Common Issues

| Issue                   | Solution                           |
| ----------------------- | ---------------------------------- |
| SCSS not compiling      | Run `yarn sass` manually           |
| Port 3003 in use        | Change port in `package.json`      |
| CSS not updating        | Clear browser cache (Ctrl+Shift+R) |
| Live reload not working | Check live-server is running       |

### Reset Development Environment

```bash
# Remove node_modules and reinstall
rm -rf node_modules
yarn install

# Rebuild CSS
yarn build:css

# Restart dev server
yarn dev
```

---

## 📚 Next Steps

1. Read [ARCHITECTURE.md](ARCHITECTURE.md) to understand the system
2. Review [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines
3. Check [DEPLOYMENT.md](DEPLOYMENT.md) for deployment instructions

---

## Related Documentation

- [ARCHITECTURE.md](ARCHITECTURE.md) - System architecture
- [ENVIRONMENT.md](ENVIRONMENT.md) - Environment configuration
- [DEPLOYMENT.md](DEPLOYMENT.md) - Deployment guide
