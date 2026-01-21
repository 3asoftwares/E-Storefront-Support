# Support Website Architecture

## 📑 Overview

E-Storefront Support is a static website built with vanilla JavaScript and Bootstrap 5.

## 🏗️ Project Structure

```
E-Storefront-Support/
├── index.html              # Main entry point
├── css/
│   └── main.css           # Compiled CSS from SCSS
├── scss/
│   └── main.scss          # SCSS source files
├── js/
│   └── app.js             # Application JavaScript
└── images/                # Static images
```

## 🎨 Styling Architecture

### SCSS Structure

```scss
// scss/main.scss

// Bootstrap customization
$primary: #2563eb;
$secondary: #7c3aed;

// Import Bootstrap
@import 'bootstrap/scss/bootstrap';

// Custom styles
.hero-section {
    background: linear-gradient(135deg, $primary, $secondary);
}
```

### Bootstrap 5 Components Used

| Component | Usage            |
| --------- | ---------------- |
| Navbar    | Navigation       |
| Cards     | Content sections |
| Forms     | Contact form     |
| Modal     | Dialogs          |
| Accordion | FAQ section      |

## 📜 JavaScript Architecture

### Module Structure

```javascript
// js/app.js

// Initialize application
document.addEventListener('DOMContentLoaded', () => {
    initContactForm();
    initFAQ();
    initNavigation();
});

// Contact form handler
function initContactForm() {
    const form = document.getElementById('contact-form');
    form?.addEventListener('submit', handleFormSubmit);
}

// API communication
async function submitTicket(data) {
    const response = await fetch('/api/tickets', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(data),
    });
    return response.json();
}
```

## 🔗 API Integration

### GraphQL Communication

```javascript
// GraphQL query example
const SUBMIT_TICKET = `
  mutation SubmitTicket($input: TicketInput!) {
    createTicket(input: $input) {
      id
      status
    }
  }
`;

async function createTicket(ticketData) {
    const response = await fetch(GRAPHQL_URL, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
            query: SUBMIT_TICKET,
            variables: { input: ticketData },
        }),
    });
    return response.json();
}
```

---

See also:

- [DEPLOYMENT.md](./DEPLOYMENT.md) - Deployment guide

# Architecture

## Overview

E-Storefront Support is a customer support ticketing portal built with vanilla JavaScript and Bootstrap.

---

## Architecture Diagram

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                          E-Storefront Support                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                        PRESENTATION LAYER                              │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌──────────────┐  ┌──────────────┐  ┌──────────────┐               │ │
│  │   │   index.html │  │  ticket.html │  │  login.html  │               │ │
│  │   │  Dashboard   │  │ Ticket Detail│  │ Login Form   │               │ │
│  │   └──────────────┘  └──────────────┘  └──────────────┘               │ │
│  │                                                                        │ │
│  │   Bootstrap 5 Components │ Bootstrap Icons │ Custom SCSS              │ │
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                       APPLICATION LAYER                                │ │
│  ├────────────────────────────────────────────────────────────────────────┤ │
│  │                                                                        │ │
│  │   ┌──────────────────────────────────────────────────────────────────┐│ │
│  │   │                      app.js (Entry Point)                        ││ │
│  │   │  Initializes services, binds event handlers, manages state       ││ │
│  │   └──────────────────────────────────────────────────────────────────┘│ │
│  │                                                                        │ │
│  │   ┌──────────────┐  ┌──────────────┐  ┌──────────────┐               │ │
│  │   │ TicketService│  │  AuthService │  │   UIService  │               │ │
│  │   │ API calls    │  │ Login/Logout │  │ DOM Updates  │               │ │
│  │   └──────────────┘  └──────────────┘  └──────────────┘               │ │
│  │                                                                        │ │
│  │   ┌──────────────────────────────────────────────────────────────────┐│ │
│  │   │                     Utility Functions                            ││ │
│  │   │  Debounce │ Date Formatting │ Validation │ LocalStorage          ││ │
│  │   └──────────────────────────────────────────────────────────────────┘│ │
│  │                                                                        │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                      │                                       │
│                                      │ HTTPS (GraphQL)                       │
│                                      ▼                                       │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │                           API LAYER                                    │ │
│  │                    GraphQL Gateway (Backend)                           │ │
│  │                 https://api.3asoftwares.com/graphql                    │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Project Structure

```
E-Storefront-Support/
├── index.html           # Main dashboard page
├── package.json         # Dependencies
├── vercel.json          # Deployment config
├── css/
│   └── main.css         # Compiled CSS
├── scss/
│   ├── main.scss        # Main SCSS file
│   ├── _variables.scss  # Variables
│   ├── _mixins.scss     # Mixins
│   └── _components.scss # Component styles
├── js/
│   └── app.js           # Application JavaScript
├── images/              # Static images
└── docs/                # Documentation
```

---

## Design Patterns

### MVC Pattern

```
┌─────────────────────────────────────────────────────────────────┐
│                       MVC Architecture                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│   ┌──────────────┐     ┌──────────────┐     ┌──────────────┐   │
│   │    MODEL     │◄────│  CONTROLLER  │────►│     VIEW     │   │
│   │              │     │              │     │              │   │
│   │ TicketService│     │   app.js     │     │ DOM/HTML     │   │
│   │ AuthService  │     │              │     │ Templates    │   │
│   │ (API Data)   │     │ Event Handlers    │ UI Updates   │   │
│   └──────────────┘     └──────────────┘     └──────────────┘   │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Singleton Pattern

```javascript
// Services are singletons
class AuthService {
  static instance = null;

  static getInstance() {
    if (!AuthService.instance) {
      AuthService.instance = new AuthService();
    }
    return AuthService.instance;
  }
}
```

### Module Pattern

```javascript
// ES6 Modules for encapsulation
export class TicketService {
  // Private state within module
  // Public API via exports
}
```

---

## Data Flow

```
User Action
    │
    ▼
Event Handler (app.js)
    │
    ▼
Service Method (ticketService.js)
    │
    ▼
GraphQL API Call
    │
    ▼
API Response
    │
    ▼
UI Update (DOM manipulation)
    │
    ▼
User Sees Result
```

---

## Security

| Layer         | Protection                           |
| ------------- | ------------------------------------ |
| Transport     | HTTPS only                           |
| Authentication| JWT tokens                           |
| Storage       | LocalStorage (non-sensitive only)    |
| API           | Authorization header                 |
| XSS           | Content sanitization                 |
| CSRF          | SameSite cookies                     |

---

## Related Documentation

- [API](API.md) - API integration
- [JavaScript](technologies/JAVASCRIPT.md) - JavaScript patterns
- [Bootstrap](technologies/BOOTSTRAP.md) - UI components
