# E-Storefront Support Documentation

Comprehensive documentation for the E-Storefront Support application.

---

## 📑 Table of Contents

### Getting Started

| Document                              | Description                   |
| ------------------------------------- | ----------------------------- |
| [Getting Started](GETTING-STARTED.md) | Quick start guide             |
| [Environment](ENVIRONMENT.md)         | Environment configuration     |

### Architecture & API

| Document                        | Description                             |
| ------------------------------- | --------------------------------------- |
| [Architecture](ARCHITECTURE.md) | System architecture and design patterns |
| [API](API.md)                   | API integration guide                   |

### Development

| Document                        | Description             |
| ------------------------------- | ----------------------- |
| [Contributing](CONTRIBUTING.md) | Contribution guidelines |

### Operations

| Document                    | Description          |
| --------------------------- | -------------------- |
| [Deployment](DEPLOYMENT.md) | Vercel deployment    |
| [Security](SECURITY.md)     | Security policies    |

### Reference

| Document                      | Description           |
| ----------------------------- | --------------------- |
| [Changelog](CHANGELOG.md)     | Version history       |
| [Technologies](technologies/) | Technology stack docs |

---

## 🔗 Production URLs

| Environment | URL                                  | Description      |
| ----------- | ------------------------------------ | ---------------- |
| Production  | https://support.3asoftwares.com      | Support portal   |
| API         | https://api.3asoftwares.com/graphql  | GraphQL endpoint |
| Auth        | https://auth.3asoftwares.com         | Auth service     |

---

## 📁 Documentation Structure

```
docs/
├── README.md              # This file
├── GETTING-STARTED.md     # Quick start
├── ARCHITECTURE.md        # App architecture
├── API.md                 # API integration
├── CONTRIBUTING.md        # Contribution guide
├── DEPLOYMENT.md          # Deployment guide
├── ENVIRONMENT.md         # Environment config
├── SECURITY.md            # Security policies
├── CHANGELOG.md           # Version history
└── technologies/          # Technology documentation
    ├── README.md          # Tech stack overview
    ├── JAVASCRIPT.md      # JavaScript ES6+
    ├── HTML5.md           # HTML5 markup
    ├── CSS3.md            # CSS3 styling
    ├── BOOTSTRAP.md       # Bootstrap framework
    ├── SCSS.md            # SCSS preprocessor
    ├── BOOTSTRAP_ICONS.md # Icons
    ├── LIVE_SERVER.md     # Dev server
    ├── SASS.md            # Sass compiler
    └── VERCEL.md          # Deployment
```

---

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build CSS
npm run sass

# Watch CSS changes
npm run sass:watch
```
