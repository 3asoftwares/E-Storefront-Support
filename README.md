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
│                   E-Storefront Support Technology Stack                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                           UI LAYER                                     │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
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
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                       MARKUP LAYER                                     │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌─────────────────────────────────────────────────────────────────┐ │ │
│  │   │                         HTML5                                   │ │ │
│  │   │        Semantic Elements │ Accessibility │ SEO Friendly        │ │ │
│  │   └─────────────────────────────────────────────────────────────────┘ │ │
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                      SCRIPTING LAYER                                   │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌─────────────────────────────────────────────────────────────────┐ │ │
│  │   │                   Vanilla JavaScript (ES6+)                     │ │ │
│  │   │   Modules │ Async/Await │ Fetch API │ DOM Manipulation         │ │ │
│  │   └─────────────────────────────────────────────────────────────────┘ │ │
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│                                      ▼                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                           API LAYER                                    │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │              Fetch API → GraphQL Gateway (Ticket Service)             │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                      BUILD & DEPLOYMENT                                │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │     SCSS Compiler (sass) │ Live Server (Dev) │ Vercel (Production)    │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

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

## 📁 Project Structure

```
E-Storefront-Support/
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

All documentation is located in the [`docs/`](docs/) folder:

### Core Documentation

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

## 📄 License

This project is licensed under the MIT License.

---

<p align="center">
  Made with ❤️ by <a href="https://3asoftwares.com">3A Softwares</a>
</p>
