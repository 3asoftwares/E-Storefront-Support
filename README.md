# E-Storefront Support

[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.2-purple?logo=bootstrap)](https://getbootstrap.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![SCSS](https://img.shields.io/badge/SCSS-1.69.0-pink?logo=sass)](https://sass-lang.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Customer Support Admin Portal for 3A Softwares - A ticketing system for managing customer support requests.

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Available Scripts](#-available-scripts)
- [Deployment](#-deployment)
- [License](#-license)

## ✨ Features

| Feature                  | Description                                       |
| ------------------------ | ------------------------------------------------- |
| 🎫 **Ticket Management** | Create, view, update, and resolve support tickets |
| 🔍 **Search & Filter**   | Search tickets with debounced input               |
| 📊 **Dashboard**         | Overview of ticket statistics                     |
| 👤 **User Management**   | Admin authentication and session management       |
| 📱 **Responsive Design** | Mobile-first responsive interface                 |
| 🔄 **Real-time Updates** | Live ticket status updates                        |

## 🛠 Tech Stack

| Category            | Technologies                        |
| ------------------- | ----------------------------------- |
| **Languages**       | JavaScript (ES6+), HTML5, CSS3      |
| **Styling**         | SCSS 1.69.0, Bootstrap 5.3.2        |
| **UI Components**   | Bootstrap 5, Bootstrap Icons 1.11.1 |
| **Icons**           | Bootstrap Icons, Material Icons     |
| **Build Tools**     | Sass (dart-sass)                    |
| **Dev Server**      | live-server 1.2.2                   |
| **Task Runner**     | concurrently 8.2.0                  |
| **API Integration** | Fetch API (REST)                    |
| **Deployment**      | Vercel                              |

## 🎨 Technology Architecture

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                  E-Storefront Support Technology Stack                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                           UI LAYER                                     │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌──────────────────┐  ┌──────────────────┐  ┌──────────────────┐   │ │
│  │   │   Bootstrap 5    │  │  Bootstrap Icons │  │  Material Icons  │   │ │
│  │   │   Components     │  │    Icon Set      │  │   Google Fonts   │   │ │
│  │   └──────────────────┘  └──────────────────┘  └──────────────────┘   │ │
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                        APPLICATION LAYER                               │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌──────────────────────────────────────────────────────────────────┐│ │
│  │   │                    Vanilla JavaScript (ES6+)                     ││ │
│  │   │     MVC Pattern │ Singleton Pattern │ Fetch API │ Debouncing    ││ │
│  │   └──────────────────────────────────────────────────────────────────┘│ │
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                         STYLING LAYER                                  │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌──────────────────────────┐  ┌──────────────────────────────────┐  │ │
│  │   │         SCSS            │  │         CSS3 Output              │  │ │
│  │   │    Preprocessor         │  │    Compiled Stylesheet           │  │ │
│  │   └──────────────────────────┘  └──────────────────────────────────┘  │ │
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│                                      ▼                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                           API LAYER                                    │ │
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
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

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

## 📁 Project Structure

```
E-Storefront-Support/
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

All documentation is located in the [`docs/`](docs/) folder:

### Core Documentation

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

## 📄 License

This project is licensed under the MIT License.

---

<p align="center">
  Made with ❤️ by <a href="https://3asoftwares.com">3A Softwares</a>
</p>
