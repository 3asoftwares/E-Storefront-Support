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
