# Environment Configuration - E-Storefront Support

## 📑 Table of Contents

- [Overview](#overview)
- [Development](#development)
- [Production](#production)
- [Vercel Configuration](#vercel-configuration)

## 🌐 Overview

E-Storefront Support is a static website that connects to the backend API for ticket submission.

## 💻 Development

### Configuration

Update API endpoints in `js/app.js`:

```javascript
// js/app.js
const CONFIG = {
    API_URL: 'http://localhost:4000/graphql', // Local GraphQL gateway
    TICKET_API: 'http://localhost:4006/api/tickets', // Local ticket service
};
```

### Running Locally

```bash
# Install dependencies
npm install

# Start live server
npm start

# Access at http://localhost:8080
```

## 🚀 Production

### Configuration

```javascript
// js/app.js (production)
const CONFIG = {
    API_URL: 'https://api.3asoftwares.com/graphql',
    TICKET_API: 'https://api.3asoftwares.com/tickets',
};
```

### Build for Production

```bash
# Compile SCSS to CSS
npm run sass

# Files ready for deployment:
# - index.html
# - css/main.css
# - js/app.js
# - images/
```

## ☁️ Vercel Configuration

### vercel.json

```json
{
    "rewrites": [{ "source": "/(.*)", "destination": "/index.html" }],
    "headers": [
        {
            "source": "/(.*)",
            "headers": [
                { "key": "X-Frame-Options", "value": "DENY" },
                { "key": "X-Content-Type-Options", "value": "nosniff" },
                { "key": "X-XSS-Protection", "value": "1; mode=block" }
            ]
        }
    ]
}
```

### Environment Variables (Vercel Dashboard)

| Variable  | Value                         | Description |
| --------- | ----------------------------- | ----------- |
| `API_URL` | `https://api.3asoftwares.com` | Backend API |

---

See also:

- [DEPLOYMENT](./DEPLOYMENT.md) - Deployment guide
- [ARCHITECTURE](./ARCHITECTURE.md) - Project structure
