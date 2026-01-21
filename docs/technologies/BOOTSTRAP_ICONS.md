# Bootstrap Icons

## Overview

**Version:** 1.11.1  
**Website:** [https://icons.getbootstrap.com](https://icons.getbootstrap.com)  
**Category:** Icon Library

Bootstrap Icons is a free, high-quality, open source icon library with over 1,900 icons.

---

## Why Bootstrap Icons?

### Benefits

| Benefit              | Description                                   |
| -------------------- | --------------------------------------------- |
| **Free**             | Open source and free to use                   |
| **SVG-based**        | Crisp at any size                             |
| **Bootstrap Match**  | Designed to work with Bootstrap               |
| **Easy to Use**      | Simple class-based usage                      |

---

## Installation

### CDN

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.1/font/bootstrap-icons.css">
```

### npm

```bash
npm install bootstrap-icons
```

---

## Usage

### Icon Font

```html
<i class="bi bi-ticket"></i>
<i class="bi bi-person"></i>
<i class="bi bi-search"></i>
<i class="bi bi-bell"></i>
<i class="bi bi-check-circle"></i>
```

### With Text

```html
<button class="btn btn-primary">
  <i class="bi bi-plus-lg me-1"></i>
  New Ticket
</button>

<span class="badge bg-warning">
  <i class="bi bi-clock me-1"></i>
  Pending
</span>
```

### Sizing

```html
<!-- Using font-size -->
<i class="bi bi-ticket" style="font-size: 2rem;"></i>

<!-- Using Bootstrap classes -->
<i class="bi bi-ticket fs-1"></i>
<i class="bi bi-ticket fs-3"></i>
<i class="bi bi-ticket fs-5"></i>
```

### Colors

```html
<i class="bi bi-check-circle text-success"></i>
<i class="bi bi-exclamation-circle text-warning"></i>
<i class="bi bi-x-circle text-danger"></i>
<i class="bi bi-info-circle text-info"></i>
```

---

## Common Icons

| Icon Class              | Usage                |
| ----------------------- | -------------------- |
| `bi-ticket`             | Ticket               |
| `bi-person`             | User/Profile         |
| `bi-search`             | Search               |
| `bi-plus-lg`            | Add/Create           |
| `bi-pencil`             | Edit                 |
| `bi-trash`              | Delete               |
| `bi-check-circle`       | Success/Complete     |
| `bi-x-circle`           | Error/Close          |
| `bi-exclamation-circle` | Warning              |
| `bi-clock`              | Pending/Time         |
| `bi-chat-dots`          | Comments             |
| `bi-arrow-left`         | Back                 |
| `bi-three-dots-vertical`| More options         |
| `bi-filter`             | Filter               |
| `bi-sort-down`          | Sort                 |

---

## Icon Examples

### Status Icons

```html
<span class="badge bg-success">
  <i class="bi bi-check-circle me-1"></i> Resolved
</span>

<span class="badge bg-warning text-dark">
  <i class="bi bi-clock me-1"></i> Pending
</span>

<span class="badge bg-danger">
  <i class="bi bi-exclamation-triangle me-1"></i> Urgent
</span>

<span class="badge bg-info">
  <i class="bi bi-arrow-repeat me-1"></i> In Progress
</span>
```

### Action Buttons

```html
<div class="btn-group">
  <button class="btn btn-outline-primary btn-sm">
    <i class="bi bi-eye"></i>
  </button>
  <button class="btn btn-outline-secondary btn-sm">
    <i class="bi bi-pencil"></i>
  </button>
  <button class="btn btn-outline-danger btn-sm">
    <i class="bi bi-trash"></i>
  </button>
</div>
```

### Navigation

```html
<nav class="navbar">
  <ul class="navbar-nav">
    <li class="nav-item">
      <a class="nav-link" href="#">
        <i class="bi bi-house me-1"></i> Dashboard
      </a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">
        <i class="bi bi-ticket me-1"></i> Tickets
      </a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">
        <i class="bi bi-people me-1"></i> Users
      </a>
    </li>
  </ul>
</nav>
```

---

## Related Documentation

- [Bootstrap](BOOTSTRAP.md) - Bootstrap framework
- [CSS3](CSS3.md) - Styling icons
