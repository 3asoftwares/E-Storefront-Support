# HTML5

## Overview

**Version:** HTML5  
**Category:** Markup Language

HTML5 is the standard markup language for creating web pages and web applications.

---

## Document Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>E-Storefront Support</title>
  
  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
  
  <!-- Bootstrap Icons -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.1/font/bootstrap-icons.css" rel="stylesheet">
  
  <!-- Custom CSS -->
  <link href="css/main.css" rel="stylesheet">
</head>
<body>
  <!-- Header -->
  <header>
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
      <!-- Navigation content -->
    </nav>
  </header>

  <!-- Main Content -->
  <main class="container py-4">
    <!-- Page content -->
  </main>

  <!-- Footer -->
  <footer class="bg-light py-3">
    <!-- Footer content -->
  </footer>

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
  
  <!-- App JS -->
  <script type="module" src="js/app.js"></script>
</body>
</html>
```

---

## Semantic Elements

```html
<header>
  <!-- Site header, navigation -->
</header>

<nav>
  <!-- Navigation links -->
</nav>

<main>
  <!-- Main content -->
</main>

<section>
  <!-- Themed grouping of content -->
</section>

<article>
  <!-- Self-contained content (ticket card) -->
</article>

<aside>
  <!-- Sidebar content -->
</aside>

<footer>
  <!-- Page footer -->
</footer>
```

---

## Forms

```html
<form id="ticketForm">
  <div class="mb-3">
    <label for="title" class="form-label">Title</label>
    <input 
      type="text" 
      class="form-control" 
      id="title" 
      name="title"
      required
      minlength="3"
      maxlength="100"
    >
  </div>

  <div class="mb-3">
    <label for="email" class="form-label">Email</label>
    <input 
      type="email" 
      class="form-control" 
      id="email"
      required
    >
  </div>

  <div class="mb-3">
    <label for="priority" class="form-label">Priority</label>
    <select class="form-select" id="priority" required>
      <option value="">Select priority</option>
      <option value="low">Low</option>
      <option value="medium">Medium</option>
      <option value="high">High</option>
    </select>
  </div>

  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

---

## Data Attributes

```html
<!-- Store data on elements -->
<div class="ticket-card" 
     data-id="123" 
     data-status="pending"
     data-priority="high">
  <!-- Content -->
</div>

<!-- Access in JavaScript -->
<script>
  const card = document.querySelector('.ticket-card');
  const ticketId = card.dataset.id;        // "123"
  const status = card.dataset.status;      // "pending"
  const priority = card.dataset.priority;  // "high"
</script>
```

---

## Accessibility

```html
<!-- ARIA labels -->
<button aria-label="Close modal" class="btn-close"></button>

<!-- Screen reader only text -->
<span class="visually-hidden">Loading...</span>

<!-- Form accessibility -->
<label for="search">Search tickets</label>
<input type="search" id="search" aria-describedby="searchHelp">
<div id="searchHelp" class="form-text">Enter ticket ID or title</div>

<!-- Role attributes -->
<div role="alert" class="alert alert-success">
  Ticket created successfully!
</div>
```

---

## Related Documentation

- [CSS3](CSS3.md) - Styling
- [JavaScript](JAVASCRIPT.md) - Interactivity
- [Bootstrap](BOOTSTRAP.md) - UI components
