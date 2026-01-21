# Contributing

## Getting Started

1. Fork the repository
2. Clone your fork
3. Create a feature branch
4. Make your changes
5. Submit a pull request

---

## Development Setup

```bash
# Clone repository
git clone https://github.com/YOUR_USERNAME/e-storefront-support.git
cd e-storefront-support

# Install dependencies
npm install

# Start development
npm run dev
```

---

## Branch Naming

| Type     | Format                | Example                 |
| -------- | --------------------- | ----------------------- |
| Feature  | `feature/description` | `feature/ticket-search` |
| Bugfix   | `fix/description`     | `fix/login-error`       |
| Hotfix   | `hotfix/description`  | `hotfix/security-patch` |

---

## Commit Messages

Use conventional commits:

```
type(scope): description

feat(tickets): add search functionality
fix(auth): resolve login timeout issue
docs(readme): update installation steps
style(scss): fix button alignment
```

---

## Code Standards

### JavaScript

- Use ES6+ features
- Follow consistent naming conventions
- Add JSDoc comments for functions
- Use `const` and `let`, never `var`

### SCSS

- Follow BEM naming convention
- Use variables for colors and spacing
- Keep selectors shallow (max 3 levels)

### HTML

- Use semantic elements
- Include accessibility attributes
- Keep markup clean and organized

---

## Pull Request Process

1. Update documentation if needed
2. Ensure SCSS compiles without errors
3. Test in multiple browsers
4. Request review from maintainers

---

## Related Documentation

- [Getting Started](GETTING-STARTED.md) - Setup guide
- [Architecture](ARCHITECTURE.md) - Code structure
