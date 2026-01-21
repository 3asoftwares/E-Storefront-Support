# API Integration

## Overview

E-Storefront Support connects to the GraphQL Gateway for ticket management operations.

---

## Endpoints

| Environment | URL                                  |
| ----------- | ------------------------------------ |
| Production  | https://api.3asoftwares.com/graphql  |
| Development | http://localhost:4000/graphql        |

---

## Authentication

### Login

```graphql
mutation Login($email: String!, $password: String!) {
  login(email: $email, password: $password) {
    token
    user {
      id
      email
      name
      role
    }
  }
}
```

### Token Storage

```javascript
// Store token after login
localStorage.setItem('token', token);

// Retrieve token for API calls
const token = localStorage.getItem('token');

// Include in requests
fetch(API_URL, {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': `Bearer ${token}`
  },
  body: JSON.stringify({ query, variables })
});
```

---

## Tickets

### Get All Tickets

```graphql
query GetTickets($status: String, $priority: String, $page: Int, $limit: Int) {
  tickets(status: $status, priority: $priority, page: $page, limit: $limit) {
    tickets {
      id
      ticketNumber
      title
      description
      status
      priority
      category
      customer {
        id
        name
        email
      }
      assignee {
        id
        name
      }
      createdAt
      updatedAt
    }
    total
    page
    totalPages
  }
}
```

### Get Ticket by ID

```graphql
query GetTicket($id: ID!) {
  ticket(id: $id) {
    id
    ticketNumber
    title
    description
    status
    priority
    category
    customer {
      id
      name
      email
    }
    assignee {
      id
      name
    }
    messages {
      id
      content
      sender {
        id
        name
        role
      }
      createdAt
    }
    createdAt
    updatedAt
  }
}
```

### Create Ticket

```graphql
mutation CreateTicket($input: CreateTicketInput!) {
  createTicket(input: $input) {
    id
    ticketNumber
    title
    status
  }
}
```

### Update Ticket Status

```graphql
mutation UpdateTicketStatus($id: ID!, $status: TicketStatus!) {
  updateTicketStatus(id: $id, status: $status) {
    id
    status
    updatedAt
  }
}
```

### Assign Ticket

```graphql
mutation AssignTicket($id: ID!, $assigneeId: ID!) {
  assignTicket(id: $id, assigneeId: $assigneeId) {
    id
    assignee {
      id
      name
    }
  }
}
```

### Add Message

```graphql
mutation AddTicketMessage($ticketId: ID!, $content: String!) {
  addTicketMessage(ticketId: $ticketId, content: $content) {
    id
    content
    sender {
      id
      name
    }
    createdAt
  }
}
```

### Close Ticket

```graphql
mutation CloseTicket($id: ID!, $resolution: String!) {
  closeTicket(id: $id, resolution: $resolution) {
    id
    status
    resolution
    closedAt
  }
}
```

---

## Ticket Status

| Status       | Description                    |
| ------------ | ------------------------------ |
| `open`       | New ticket, awaiting response  |
| `pending`    | Awaiting customer response     |
| `in_progress`| Being worked on                |
| `resolved`   | Issue resolved                 |
| `closed`     | Ticket closed                  |

## Ticket Priority

| Priority | Description                    |
| -------- | ------------------------------ |
| `low`    | Non-urgent issue               |
| `medium` | Standard priority              |
| `high`   | Urgent, needs quick response   |
| `urgent` | Critical, immediate attention  |

---

## JavaScript Implementation

```javascript
// services/ticketService.js
class TicketService {
  constructor() {
    this.baseUrl = 'https://api.3asoftwares.com/graphql';
  }

  async query(query, variables = {}) {
    const token = localStorage.getItem('token');
    
    const response = await fetch(this.baseUrl, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        ...(token && { Authorization: `Bearer ${token}` }),
      },
      body: JSON.stringify({ query, variables }),
    });

    const { data, errors } = await response.json();

    if (errors) {
      throw new Error(errors[0].message);
    }

    return data;
  }

  async getTickets(filters = {}) {
    const data = await this.query(GET_TICKETS, filters);
    return data.tickets;
  }

  async getTicket(id) {
    const data = await this.query(GET_TICKET, { id });
    return data.ticket;
  }

  async createTicket(input) {
    const data = await this.query(CREATE_TICKET, { input });
    return data.createTicket;
  }

  async updateStatus(id, status) {
    const data = await this.query(UPDATE_TICKET_STATUS, { id, status });
    return data.updateTicketStatus;
  }
}

export const ticketService = new TicketService();
```

---

## Error Handling

```javascript
async function handleApiCall(apiCall) {
  try {
    return await apiCall();
  } catch (error) {
    if (error.message.includes('UNAUTHENTICATED')) {
      // Redirect to login
      localStorage.removeItem('token');
      window.location.href = '/login.html';
      return;
    }
    
    // Show error to user
    showAlert(error.message, 'danger');
    throw error;
  }
}
```

---

## Related Documentation

- [Architecture](ARCHITECTURE.md) - System architecture
- [JavaScript](technologies/JAVASCRIPT.md) - JavaScript patterns
