# SCSS

## Overview

**Version:** 1.69.0 (dart-sass)  
**Website:** [https://sass-lang.com](https://sass-lang.com)  
**Category:** CSS Preprocessor

SCSS is a CSS preprocessor that adds features like variables, nesting, and mixins to CSS.

---

## Why SCSS?

### Benefits

| Benefit           | Description                                   |
| ----------------- | --------------------------------------------- |
| **Variables**     | Define reusable values                        |
| **Nesting**       | Nested selectors for cleaner code             |
| **Mixins**        | Reusable style blocks                         |
| **Partials**      | Split styles into organized files             |
| **Inheritance**   | Extend existing styles                        |

---

## Project Structure

```
scss/
├── main.scss           # Main entry file
├── _variables.scss     # Variables and colors
├── _mixins.scss        # Reusable mixins
├── _base.scss          # Base styles
├── _components.scss    # Component styles
├── _utilities.scss     # Utility classes
└── _layout.scss        # Layout styles
```

---

## Variables

```scss
// _variables.scss

// Colors
$primary: #0d6efd;
$secondary: #6c757d;
$success: #198754;
$danger: #dc3545;
$warning: #ffc107;
$info: #0dcaf0;

// Custom colors
$brand-primary: #3b82f6;
$brand-secondary: #6366f1;

// Spacing
$spacer: 1rem;
$spacers: (
  0: 0,
  1: $spacer * 0.25,
  2: $spacer * 0.5,
  3: $spacer,
  4: $spacer * 1.5,
  5: $spacer * 3,
);

// Typography
$font-family-base: 'Inter', sans-serif;
$font-size-base: 1rem;

// Breakpoints
$breakpoints: (
  sm: 576px,
  md: 768px,
  lg: 992px,
  xl: 1200px,
);
```

---

## Nesting

```scss
// _components.scss

.ticket-card {
  background: white;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s ease;

  &:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
  }

  .card-header {
    padding: 1rem;
    border-bottom: 1px solid #e5e7eb;

    .ticket-id {
      font-size: 0.875rem;
      color: #6b7280;
    }
  }

  .card-body {
    padding: 1rem;

    .ticket-title {
      font-weight: 600;
      margin-bottom: 0.5rem;
    }

    .ticket-description {
      color: #4b5563;
      line-height: 1.5;
    }
  }

  .card-footer {
    padding: 0.75rem 1rem;
    background: #f9fafb;
    border-top: 1px solid #e5e7eb;
  }
}
```

---

## Mixins

```scss
// _mixins.scss

// Responsive breakpoint
@mixin respond-to($breakpoint) {
  @if map-has-key($breakpoints, $breakpoint) {
    @media (min-width: map-get($breakpoints, $breakpoint)) {
      @content;
    }
  }
}

// Flexbox center
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

// Card shadow
@mixin card-shadow {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);

  &:hover {
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
  }
}

// Truncate text
@mixin truncate($lines: 1) {
  @if $lines == 1 {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  } @else {
    display: -webkit-box;
    -webkit-line-clamp: $lines;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }
}

// Usage
.ticket-title {
  @include truncate(2);
}

.modal-content {
  @include respond-to(md) {
    max-width: 600px;
  }
}
```

---

## Functions

```scss
// Darken/lighten colors
.btn-primary {
  background: $brand-primary;

  &:hover {
    background: darken($brand-primary, 10%);
  }

  &:active {
    background: darken($brand-primary, 15%);
  }
}

// Calculate values
.container {
  padding: calc($spacer * 2);
}
```

---

## Compilation

### package.json Scripts

```json
{
  "scripts": {
    "sass": "sass scss/main.scss css/main.css",
    "sass:watch": "sass --watch scss/main.scss css/main.css",
    "build": "sass scss/main.scss css/main.css --style=compressed"
  }
}
```

### Commands

```bash
# Compile once
npm run sass

# Watch for changes
npm run sass:watch

# Build for production (minified)
npm run build
```

---

## Related Documentation

- [Bootstrap](BOOTSTRAP.md) - Bootstrap customization
- [CSS3](CSS3.md) - CSS basics
