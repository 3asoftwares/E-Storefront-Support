# Contributing to E-Storefront Support

Thank you for your interest in contributing! This document provides guidelines for contributing to the E-Storefront Support website.

## 📑 Table of Contents

- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Pre-PR Checklist](#pre-pr-checklist)
- [Coding Standards](#coding-standards)

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- npm 8+

### Setup

```bash
# 1. Fork and clone
git clone https://github.com/YOUR_USERNAME/E-Storefront-Support.git
cd E-Storefront-Support

# 2. Install dependencies
npm install

# 3. Start development server
npm start
```

## 🔄 Development Workflow

### 1. Create Feature Branch

```bash
git checkout -b feature/your-feature-name
```

### 2. Make Changes

- Edit HTML, CSS/SCSS, JavaScript files
- Test locally with `npm start`
- Compile SCSS: `npm run sass`

### 3. Test Your Changes

- Open in multiple browsers
- Test responsive design
- Verify all interactive features

### 4. Push and Create PR

```bash
git push origin feature/your-feature-name
```

## ✅ Pre-PR Checklist

```bash
# 1. Compile SCSS to CSS
npm run sass

# 2. Validate HTML (use W3C validator)
# https://validator.w3.org/

# 3. Test in browsers
# - Chrome, Firefox, Safari, Edge

# 4. Test responsive design
# - Mobile, Tablet, Desktop

# 5. Check console for errors
# - No JavaScript errors
```

### Checklist

- [ ] SCSS compiled to CSS
- [ ] HTML validates
- [ ] No console errors
- [ ] Responsive design works
- [ ] Cross-browser tested
- [ ] Forms functional

## 📝 Coding Standards

### HTML

```html
<!-- Use semantic HTML5 -->
<header>
    <nav>...</nav>
</header>
<main>
    <section>...</section>
</main>
<footer>...</footer>

<!-- Use descriptive class names (BEM) -->
<div class="card">
    <h2 class="card__title">Title</h2>
    <p class="card__description">Description</p>
</div>
```

### CSS/SCSS

```scss
// Use BEM naming
.block {
    &__element {
        // styles
    }

    &--modifier {
        // styles
    }
}

// Use variables for colors
$primary-color: #2563eb;
$secondary-color: #7c3aed;
```

### JavaScript

```javascript
// Use ES6+ features
const fetchData = async (url) => {
    const response = await fetch(url);
    return response.json();
};

// Use descriptive function names
function handleFormSubmit(event) {
    event.preventDefault();
    // ...
}

// Comment complex logic
/**
 * Validates contact form fields
 * @param {Object} formData - Form field values
 * @returns {boolean} - True if valid
 */
function validateForm(formData) {
    // ...
}
```

## 📋 Commit Guidelines

### Format

```
<type>: <description>
```

### Types

| Type       | Description         |
| ---------- | ------------------- |
| `feat`     | New feature         |
| `fix`      | Bug fix             |
| `docs`     | Documentation       |
| `style`    | CSS/styling changes |
| `refactor` | Code refactoring    |

### Examples

```bash
git commit -m "feat: add FAQ accordion section"
git commit -m "fix: contact form validation"
git commit -m "style: update button hover states"
```

---

Thank you for contributing! 🎉
