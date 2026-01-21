# Getting Started

## Prerequisites

- Node.js 18+
- npm or yarn
- Modern web browser (Chrome, Firefox, Safari, Edge)

---

## Quick Start

### 1. Clone Repository

```bash
git clone https://github.com/3asoftwares/e-storefront-support.git
cd e-storefront-support
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Start Development Server

```bash
npm run dev
```

This starts both SCSS compilation and live server.

### 4. Open Browser

Navigate to `http://localhost:8080`

---

## Available Scripts

| Command            | Description                         |
| ------------------ | ----------------------------------- |
| `npm run dev`      | Start dev server with SCSS watching |
| `npm run start`    | Start live server only              |
| `npm run sass`     | Compile SCSS once                   |
| `npm run sass:watch`| Watch SCSS for changes             |
| `npm run build`    | Build CSS for production            |

---

## Project Structure

```
E-Storefront-Support/
├── index.html           # Main page
├── css/
│   └── main.css         # Compiled CSS (generated)
├── scss/
│   └── main.scss        # SCSS source
├── js/
│   └── app.js           # Application JavaScript
├── images/              # Static assets
└── docs/                # Documentation
```

---

## Environment Configuration

Create environment configuration in `js/config.js`:

```javascript
const config = {
  apiUrl: 'https://api.3asoftwares.com/graphql',
  authUrl: 'https://auth.3asoftwares.com',
};

export default config;
```

---

## Next Steps

1. Read the [Architecture](ARCHITECTURE.md) documentation
2. Explore the [API](API.md) integration guide
3. Review [Technologies](technologies/) used
