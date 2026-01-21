# CSS3

## Overview

**Version:** CSS3  
**Category:** Styling Language

CSS3 is the latest evolution of Cascading Style Sheets, used to style HTML documents.

---

## Modern CSS Features

### Flexbox

```css
.flex-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  gap: 1rem;
}

.flex-item {
  flex: 1;
}
```

### Grid

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

/* Responsive grid */
.ticket-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1rem;
}
```

### CSS Variables

```css
:root {
  --primary-color: #0d6efd;
  --secondary-color: #6c757d;
  --success-color: #198754;
  --danger-color: #dc3545;
  --border-radius: 0.5rem;
  --shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.card {
  border-radius: var(--border-radius);
  box-shadow: var(--shadow);
}

.btn-primary {
  background-color: var(--primary-color);
}
```

### Transitions

```css
.card {
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
}

.btn {
  transition: background-color 0.15s ease-in-out;
}
```

### Animations

```css
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.ticket-card {
  animation: fadeIn 0.3s ease-out;
}

@keyframes spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

.loading-spinner {
  animation: spin 1s linear infinite;
}
```

---

## Responsive Design

### Media Queries

```css
/* Mobile first */
.container {
  padding: 1rem;
}

/* Tablet and up */
@media (min-width: 768px) {
  .container {
    padding: 2rem;
  }
}

/* Desktop */
@media (min-width: 992px) {
  .container {
    max-width: 960px;
    margin: 0 auto;
  }
}
```

### Container Queries

```css
.card-container {
  container-type: inline-size;
}

@container (min-width: 400px) {
  .card {
    display: flex;
    flex-direction: row;
  }
}
```

---

## Utility Classes

```css
/* Spacing */
.m-1 { margin: 0.25rem; }
.m-2 { margin: 0.5rem; }
.p-1 { padding: 0.25rem; }
.p-2 { padding: 0.5rem; }

/* Display */
.d-none { display: none; }
.d-flex { display: flex; }
.d-grid { display: grid; }

/* Text */
.text-center { text-align: center; }
.text-muted { color: #6c757d; }
.fw-bold { font-weight: 700; }

/* Visibility */
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
```

---

## Related Documentation

- [SCSS](SCSS.md) - CSS preprocessor
- [Bootstrap](BOOTSTRAP.md) - CSS framework
- [HTML5](HTML5.md) - Markup
