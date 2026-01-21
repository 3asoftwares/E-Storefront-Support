# Bootstrap

## Overview

**Version:** 5.3.2  
**Website:** [https://getbootstrap.com](https://getbootstrap.com)  
**Category:** CSS Framework

Bootstrap is the world's most popular front-end open source toolkit for building responsive, mobile-first sites.

---

## Why Bootstrap?

### Benefits

| Benefit              | Description                                   |
| -------------------- | --------------------------------------------- |
| **Responsive**       | Mobile-first responsive grid                  |
| **Components**       | Pre-built UI components                       |
| **Customizable**     | Easy to customize with SCSS                   |
| **Documentation**    | Excellent documentation                       |
| **Browser Support**  | Cross-browser compatibility                   |

---

## Grid System

### Container

```html
<div class="container">
  <!-- Fixed-width container -->
</div>

<div class="container-fluid">
  <!-- Full-width container -->
</div>
```

### Rows and Columns

```html
<div class="container">
  <div class="row">
    <div class="col-12 col-md-6 col-lg-4">
      <!-- Full on mobile, half on tablet, third on desktop -->
    </div>
    <div class="col-12 col-md-6 col-lg-4">
      <!-- Content -->
    </div>
    <div class="col-12 col-md-12 col-lg-4">
      <!-- Content -->
    </div>
  </div>
</div>
```

### Responsive Breakpoints

| Breakpoint | Class Infix | Dimensions |
| ---------- | ----------- | ---------- |
| X-Small    | (none)      | <576px     |
| Small      | `sm`        | ≥576px     |
| Medium     | `md`        | ≥768px     |
| Large      | `lg`        | ≥992px     |
| X-Large    | `xl`        | ≥1200px    |
| XX-Large   | `xxl`       | ≥1400px    |

---

## Components Used

### Cards

```html
<div class="card">
  <div class="card-header">
    <h5 class="card-title">Ticket #123</h5>
  </div>
  <div class="card-body">
    <p class="card-text">Ticket description goes here.</p>
    <span class="badge bg-warning">Pending</span>
  </div>
  <div class="card-footer">
    <button class="btn btn-primary">View Details</button>
  </div>
</div>
```

### Modals

```html
<div class="modal fade" id="ticketModal" tabindex="-1">
  <div class="modal-dialog modal-lg">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">Ticket Details</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
      </div>
      <div class="modal-body">
        <!-- Ticket content -->
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save Changes</button>
      </div>
    </div>
  </div>
</div>
```

### Forms

```html
<form>
  <div class="mb-3">
    <label for="title" class="form-label">Title</label>
    <input type="text" class="form-control" id="title" required>
  </div>
  <div class="mb-3">
    <label for="description" class="form-label">Description</label>
    <textarea class="form-control" id="description" rows="3"></textarea>
  </div>
  <div class="mb-3">
    <label for="priority" class="form-label">Priority</label>
    <select class="form-select" id="priority">
      <option value="low">Low</option>
      <option value="medium">Medium</option>
      <option value="high">High</option>
    </select>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

### Badges

```html
<span class="badge bg-primary">New</span>
<span class="badge bg-success">Resolved</span>
<span class="badge bg-warning text-dark">Pending</span>
<span class="badge bg-danger">Urgent</span>
<span class="badge bg-info">In Progress</span>
```

### Buttons

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-danger">Delete</button>
<button class="btn btn-outline-primary">Outline</button>
<button class="btn btn-sm">Small</button>
<button class="btn btn-lg">Large</button>
```

### Tables

```html
<table class="table table-striped table-hover">
  <thead>
    <tr>
      <th>ID</th>
      <th>Title</th>
      <th>Status</th>
      <th>Actions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>#123</td>
      <td>Login issue</td>
      <td><span class="badge bg-warning">Pending</span></td>
      <td>
        <button class="btn btn-sm btn-primary">View</button>
      </td>
    </tr>
  </tbody>
</table>
```

---

## Utility Classes

### Spacing

```html
<!-- Margin -->
<div class="m-3">Margin all sides</div>
<div class="mt-3">Margin top</div>
<div class="mx-auto">Center horizontally</div>

<!-- Padding -->
<div class="p-3">Padding all sides</div>
<div class="py-3">Padding vertical</div>
<div class="px-4">Padding horizontal</div>
```

### Display

```html
<div class="d-none d-md-block">Hidden on mobile</div>
<div class="d-block d-md-none">Visible only on mobile</div>
<div class="d-flex justify-content-between">Flexbox</div>
```

### Text

```html
<p class="text-center">Centered text</p>
<p class="text-muted">Muted text</p>
<p class="fw-bold">Bold text</p>
<p class="fs-4">Large text</p>
```

---

## Related Documentation

- [SCSS](SCSS.md) - SCSS customization
- [Bootstrap Icons](BOOTSTRAP_ICONS.md) - Icons
- [JavaScript](JAVASCRIPT.md) - Interactivity
