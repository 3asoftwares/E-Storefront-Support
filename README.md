# E-Storefront Support

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.0-purple?logo=bootstrap)](https://getbootstrap.com/)
[![SCSS](https://img.shields.io/badge/SCSS-CSS_Preprocessor-pink?logo=sass)](https://sass-lang.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Customer support and help center website for E-Storefront platform, built with **vanilla JavaScript**, **Bootstrap 5**, and **SCSS**.

## 📑 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Development](#-development)
- [Deployment](#-deployment)
- [Documentation](#-documentation)
- [Contributing](#-contributing)
- [License](#-license)

## ✨ Features

| Feature              | Description                 |
| -------------------- | --------------------------- |
| 📖 **Help Center**   | FAQ and knowledge base      |
| 📝 **Contact Form**  | Customer inquiry submission |
| 🎫 **Ticket System** | Support ticket tracking     |
| 📱 **Responsive**    | Mobile-first design         |
| 🎨 **Modern UI**     | Clean Bootstrap 5 design    |

## 🛠️ Tech Stack

| Category      | Technology     | Version | Purpose          |
| ------------- | -------------- | ------- | ---------------- |
| **Markup**    | HTML5          | -       | Page structure   |
| **Styling**   | CSS3           | -       | Base styling     |
| **Styling**   | SCSS           | 1.69    | CSS preprocessor |
| **Framework** | Bootstrap      | 5.0     | UI framework     |
| **Scripting** | JavaScript     | ES6+    | Interactivity    |
| **Icons**     | Material Icons | -       | Icon library     |
| **API**       | Fetch API      | -       | HTTP requests    |
| **API**       | GraphQL        | -       | Backend API      |
| **Server**    | live-server    | 1.2     | Dev server       |
| **Hosting**   | Vercel         | -       | Deployment       |

## 🎨 Technology Architecture

```
┌─────────────────────────────────────────────────────────────────────────────┐
<<<<<<< HEAD
│                  E-Storefront Support Technology Stack                       │
=======
│                   E-Storefront Support Technology Stack                      │
>>>>>>> 195f8e0876b63d63253d616bb9a40c254f057cbb
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                           UI LAYER                                     │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
<<<<<<< HEAD
│  │   ┌──────────────────┐  ┌──────────────────┐  ┌──────────────────┐   │ │
│  │   │   Bootstrap 5    │  │  Bootstrap Icons │  │  Material Icons  │   │ │
│  │   │   Components     │  │    Icon Set      │  │   Google Fonts   │   │ │
│  │   └──────────────────┘  └──────────────────┘  └──────────────────┘   │ │
=======
│  │   ┌─────────────────────────────────────────────────────────────────┐ │ │
│  │   │                      Bootstrap 5.0                              │ │ │
│  │   │    Grid System │ Components │ Utilities │ Responsive Design    │ │ │
│  │   └─────────────────────────────────────────────────────────────────┘ │ │
│  │                                                                        │ │
│  │   ┌─────────────────────┐  ┌─────────────────────────────────────┐   │ │
│  │   │    SCSS (Sass)      │  │       Material Icons                │   │ │
│  │   │  Variables, Mixins  │  │     Icon Library                    │   │ │
│  │   │  Nesting, Functions │  │                                     │   │ │
│  │   └─────────────────────┘  └─────────────────────────────────────┘   │ │
>>>>>>> 195f8e0876b63d63253d616bb9a40c254f057cbb
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
<<<<<<< HEAD
│  │                        APPLICATION LAYER                               │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌──────────────────────────────────────────────────────────────────┐│ │
│  │   │                    Vanilla JavaScript (ES6+)                     ││ │
│  │   │     MVC Pattern │ Singleton Pattern │ Fetch API │ Debouncing    ││ │
│  │   └──────────────────────────────────────────────────────────────────┘│ │
=======
│  │                       MARKUP LAYER                                     │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌─────────────────────────────────────────────────────────────────┐ │ │
│  │   │                         HTML5                                   │ │ │
│  │   │        Semantic Elements │ Accessibility │ SEO Friendly        │ │ │
│  │   └─────────────────────────────────────────────────────────────────┘ │ │
>>>>>>> 195f8e0876b63d63253d616bb9a40c254f057cbb
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
<<<<<<< HEAD
│  │                         STYLING LAYER                                  │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌──────────────────────────┐  ┌──────────────────────────────────┐  │ │
│  │   │         SCSS            │  │         CSS3 Output              │  │ │
│  │   │    Preprocessor         │  │    Compiled Stylesheet           │  │ │
│  │   └──────────────────────────┘  └──────────────────────────────────┘  │ │
=======
│  │                      SCRIPTING LAYER                                   │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌─────────────────────────────────────────────────────────────────┐ │ │
│  │   │                   Vanilla JavaScript (ES6+)                     │ │ │
│  │   │   Modules │ Async/Await │ Fetch API │ DOM Manipulation         │ │ │
│  │   └─────────────────────────────────────────────────────────────────┘ │ │
>>>>>>> 195f8e0876b63d63253d616bb9a40c254f057cbb
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│                                      ▼                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                           API LAYER                                    │ │
<<<<<<< HEAD
│  │                    GraphQL Gateway (Backend)                           │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                      DEVELOPMENT TOOLS                                 │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │          Sass (dart-sass) │ live-server │ concurrently                │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                         DEPLOYMENT                                     │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                           Vercel                                       │ │
=======
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │              Fetch API → GraphQL Gateway (Ticket Service)             │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                      BUILD & DEPLOYMENT                                │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │     SCSS Compiler (sass) │ Live Server (Dev) │ Vercel (Production)    │ │
>>>>>>> 195f8e0876b63d63253d616bb9a40c254f057cbb
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

<<<<<<< HEAD
## 📦 Prerequisites

- **Node.js** >= 18.x
- **yarn** or **npm**

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/3asoftwares/E-Storefront-Support.git
cd E-Storefront-Support
```

### 2. Install Dependencies

```bash
yarn install
# or
npm install
```

### 3. Start Development Server

```bash
yarn dev
# or
npm run dev
```

This will:

- Start the SCSS compiler in watch mode
- Start the live-server on port 3003

Visit [http://localhost:3003](http://localhost:3003) to view the application.

=======
For detailed technology documentation, see [docs/technologies/](docs/technologies/).

## 🚀 Getting Started

### Prerequisites

- **Node.js** 18+
- **npm** 8+

### Installation

```bash
# Clone repository
git clone https://github.com/3asoftwares/E-Storefront-Support.git
cd E-Storefront-Support

# Install dependencies
npm install

# Start development server
npm start
```

### Quick Start

```bash
# One-liner setup
git clone https://github.com/3asoftwares/E-Storefront-Support.git && cd E-Storefront-Support && npm install && npm start
```

>>>>>>> 195f8e0876b63d63253d616bb9a40c254f057cbb
## 📁 Project Structure

```
E-Storefront-Support/
<<<<<<< HEAD
├── index.html              # Main HTML entry point
├── css/
│   └── main.css            # Compiled CSS output
├── scss/
│   └── main.scss           # SCSS source files
├── js/
│   └── app.js              # Main JavaScript application (ES6+)
├── images/                 # Image assets
├── docs/                   # Documentation
│   └── technologies/       # Technology guides
├── package.json            # Dependencies & scripts
└── vercel.json             # Vercel deployment config
```

## 📜 Available Scripts

| Command          | Description                           |
| ---------------- | ------------------------------------- |
| `yarn dev`       | Start dev server with SCSS watch mode |
| `yarn start`     | Start live-server on port 3003        |
| `yarn sass`      | Watch SCSS and compile to CSS         |
| `yarn build`     | Build CSS for production (compressed) |
| `yarn build:css` | Compile SCSS to compressed CSS        |

## 🌐 Deployment

### Vercel

The project is configured for Vercel deployment with `vercel.json`:

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy to Vercel
vercel
```

### Manual Deployment

1. Build CSS for production:

    ```bash
    yarn build
    ```

2. Deploy the following files to your static hosting:
    - `index.html`
    - `css/main.css`
    - `js/app.js`
    - `images/` folder

## � Documentation
=======
├── index.html              # Main HTML page
├── package.json            # Dependencies
├── vercel.json            # Vercel config
├── css/
│   └── main.css           # Compiled CSS
├── scss/
│   └── main.scss          # SCSS source
├── js/
│   └── app.js             # JavaScript
├── images/                # Image assets
└── docs/                  # Documentation
    ├── ARCHITECTURE.md
    ├── DEPLOYMENT.md
    ├── ENVIRONMENT.md
    └── technologies/
```

## 💻 Development

### Available Scripts

| Command              | Description          |
| -------------------- | -------------------- |
| `npm start`          | Start live server    |
| `npm run build`      | Build for production |
| `npm run sass`       | Compile SCSS to CSS  |
| `npm run sass:watch` | Watch SCSS changes   |
| `npm run dev`        | SCSS watch + server  |

### SCSS Development

```bash
# Watch SCSS changes + start server
npm run dev

# Or run separately:
# Terminal 1: Watch SCSS
npm run sass:watch

# Terminal 2: Start server
npm start
```

### Pre-PR Checklist

1. Compile SCSS: `npm run sass`
2. Check for JS errors in browser console
3. Test responsiveness on multiple screen sizes
4. Validate HTML (W3C validator)
5. Test all interactive features

## 🚀 Deployment

### Vercel Deployment

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel
```

### Configuration

```json
// vercel.json
{
    "rewrites": [{ "source": "/(.*)", "destination": "/index.html" }]
}
```

### Manual Deployment

```bash
# Build CSS
npm run sass

# Upload files to hosting:
# - index.html
# - css/main.css
# - js/app.js
# - images/
```

## 📚 Documentation
>>>>>>> 195f8e0876b63d63253d616bb9a40c254f057cbb

All documentation is located in the [`docs/`](docs/) folder:

### Core Documentation

<<<<<<< HEAD
| Document                                | Description                             |
| --------------------------------------- | --------------------------------------- |
| [README.md](docs/README.md)             | Documentation index                     |
| [ARCHITECTURE.md](docs/ARCHITECTURE.md) | System architecture and design patterns |
| [API.md](docs/API.md)                   | GraphQL API reference and integration   |
| [GETTING-STARTED.md](docs/GETTING-STARTED.md) | Quick start guide                 |
| [DEPLOYMENT.md](docs/DEPLOYMENT.md)     | Vercel deployment guide                 |
| [ENVIRONMENT.md](docs/ENVIRONMENT.md)   | Environment configuration               |
| [SECURITY.md](docs/SECURITY.md)         | Security policies and best practices    |
| [CONTRIBUTING.md](docs/CONTRIBUTING.md) | Contribution guidelines                 |
| [CHANGELOG.md](docs/CHANGELOG.md)       | Version history                         |

### Technology Guides

| Document                                             | Description              |
| ---------------------------------------------------- | ------------------------ |
| [Technologies Overview](docs/technologies/)          | Full tech stack docs     |
| [JavaScript](docs/technologies/JAVASCRIPT.md)        | JavaScript ES6+ patterns |
| [HTML5](docs/technologies/HTML5.md)                  | HTML5 markup             |
| [CSS3](docs/technologies/CSS3.md)                    | CSS3 styling             |
| [Bootstrap](docs/technologies/BOOTSTRAP.md)          | Bootstrap 5 framework    |
| [SCSS](docs/technologies/SCSS.md)                    | SCSS preprocessor        |
| [Sass](docs/technologies/SASS.md)                    | Sass compiler            |
| [Bootstrap Icons](docs/technologies/BOOTSTRAP_ICONS.md) | Icon library          |
| [Live Server](docs/technologies/LIVE_SERVER.md)      | Development server       |
| [Vercel](docs/technologies/VERCEL.md)                | Vercel deployment        |

## �🔗 Related Projects

- [E-Storefront](https://github.com/3asoftwares/E-Storefront) - Backend services & admin apps
- [E-Storefront-Web](https://github.com/3asoftwares/E-Storefront-Web) - Customer web storefront
- [E-Storefront-Mobile](https://github.com/3asoftwares/E-Storefront-Mobile) - Mobile app
=======
| Document                                | Description          |
| --------------------------------------- | -------------------- |
| [ARCHITECTURE.md](docs/ARCHITECTURE.md) | Project architecture |
| [DEPLOYMENT.md](docs/DEPLOYMENT.md)     | Deployment guide     |
| [ENVIRONMENT.md](docs/ENVIRONMENT.md)   | Environment config   |

### Technology Guides

| Document                                         | Description     |
| ------------------------------------------------ | --------------- |
| [BOOTSTRAP.md](docs/technologies/BOOTSTRAP.md)   | Bootstrap 5     |
| [SCSS.md](docs/technologies/SCSS.md)             | SCSS/Sass       |
| [JAVASCRIPT.md](docs/technologies/JAVASCRIPT.md) | JavaScript ES6+ |

### Additional Documentation

| Document                                | Description             |
| --------------------------------------- | ----------------------- |
| [CONTRIBUTING.md](docs/CONTRIBUTING.md) | Contribution guidelines |
| [CHANGELOG.md](docs/CHANGELOG.md)       | Version history         |

## 🤝 Contributing

Please read [CONTRIBUTING.md](docs/CONTRIBUTING.md) for contribution guidelines.
>>>>>>> 195f8e0876b63d63253d616bb9a40c254f057cbb

## 📄 License

This project is licensed under the MIT License.

---

<p align="center">
  Made with ❤️ by <a href="https://3asoftwares.com">3A Softwares</a>
</p>
