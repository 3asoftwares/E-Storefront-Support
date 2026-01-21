# JavaScript (ES6+)

## Overview

**Version:** ES6+ (ECMAScript 2015+)  
**Category:** Programming Language

Vanilla JavaScript is used for all application logic in E-Storefront Support, leveraging modern ES6+ features.

---

## Why Vanilla JavaScript?

### Benefits

| Benefit              | Description                                   |
| -------------------- | --------------------------------------------- |
| **No Dependencies**  | No framework overhead                         |
| **Performance**      | Fast execution, small bundle size             |
| **Simplicity**       | Easy to understand and maintain               |
| **Browser Support**  | Native browser support                        |
| **Learning**         | Core JavaScript skills                        |

---

## ES6+ Features Used

### Modules

```javascript
// app.js - Main entry point
import { TicketService } from './services/ticketService.js';
import { AuthService } from './services/authService.js';
import { UI } from './ui/ui.js';

// Initialize app
const app = {
  ticketService: new TicketService(),
  authService: new AuthService(),
  ui: new UI(),

  init() {
    this.authService.checkAuth();
    this.ui.init();
    this.loadTickets();
  },

  async loadTickets() {
    const tickets = await this.ticketService.getAll();
    this.ui.renderTickets(tickets);
  },
};

document.addEventListener('DOMContentLoaded', () => app.init());
```

### Classes

```javascript
// services/ticketService.js
export class TicketService {
  constructor() {
    this.baseUrl = 'https://api.3asoftwares.com/graphql';
  }

  async getAll() {
    const response = await this.query(GET_TICKETS);
    return response.tickets;
  }

  async getById(id) {
    const response = await this.query(GET_TICKET, { id });
    return response.ticket;
  }

  async create(input) {
    const response = await this.mutation(CREATE_TICKET, { input });
    return response.createTicket;
  }

  async query(query, variables = {}) {
    const response = await fetch(this.baseUrl, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        Authorization: `Bearer ${localStorage.getItem('token')}`,
      },
      body: JSON.stringify({ query, variables }),
    });
    const { data, errors } = await response.json();
    if (errors) throw new Error(errors[0].message);
    return data;
  }
}
```

### Arrow Functions

```javascript
// Callbacks
const tickets = data.map((ticket) => ({
  id: ticket.id,
  title: ticket.title,
  status: ticket.status,
}));

// Event handlers
searchInput.addEventListener('input', (e) => {
  this.handleSearch(e.target.value);
});

// Array methods
const openTickets = tickets.filter((t) => t.status === 'open');
const totalPriority = tickets.reduce((sum, t) => sum + t.priority, 0);
```

### Template Literals

```javascript
// HTML templates
function renderTicketCard(ticket) {
  return `
    <div class="card ticket-card" data-id="${ticket.id}">
      <div class="card-body">
        <h5 class="card-title">${ticket.title}</h5>
        <p class="card-text">${ticket.description}</p>
        <span class="badge bg-${getStatusColor(ticket.status)}">
          ${ticket.status}
        </span>
      </div>
    </div>
  `;
}
```

### Destructuring

```javascript
// Object destructuring
const { id, title, status, priority } = ticket;

// Array destructuring
const [first, ...rest] = tickets;

// Function parameters
function updateTicket({ id, status, assignee }) {
  // ...
}
```

### Async/Await

```javascript
async function loadTickets() {
  try {
    showLoader();
    const tickets = await ticketService.getAll();
    renderTickets(tickets);
  } catch (error) {
    showError(error.message);
  } finally {
    hideLoader();
  }
}
```

### Spread Operator

```javascript
// Merge objects
const updatedTicket = { ...ticket, status: 'resolved' };

// Copy arrays
const ticketsCopy = [...tickets];

// Function arguments
const maxPriority = Math.max(...tickets.map((t) => t.priority));
```

---

## Design Patterns

### Singleton Pattern

```javascript
// services/authService.js
class AuthService {
  static instance = null;

  constructor() {
    if (AuthService.instance) {
      return AuthService.instance;
    }
    AuthService.instance = this;
    this.user = null;
  }

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
// utils/helpers.js
export const helpers = {
  formatDate(date) {
    return new Date(date).toLocaleDateString();
  },

  debounce(func, wait) {
    let timeout;
    return function executedFunction(...args) {
      clearTimeout(timeout);
      timeout = setTimeout(() => func.apply(this, args), wait);
    };
  },

  capitalize(str) {
    return str.charAt(0).toUpperCase() + str.slice(1);
  },
};
```

---

## DOM Manipulation

```javascript
// Query elements
const container = document.getElementById('ticket-container');
const cards = document.querySelectorAll('.ticket-card');

// Create elements
const card = document.createElement('div');
card.className = 'card';
card.innerHTML = renderTicketCard(ticket);

// Append elements
container.appendChild(card);

// Event delegation
container.addEventListener('click', (e) => {
  const card = e.target.closest('.ticket-card');
  if (card) {
    const ticketId = card.dataset.id;
    showTicketDetail(ticketId);
  }
});
```

---

## Related Documentation

- [HTML5](HTML5.md) - Markup structure
- [CSS3](CSS3.md) - Styling
- [Bootstrap](BOOTSTRAP.md) - UI framework
