# Environment Configuration

## Overview

Environment configuration for E-Storefront Support application.

---

## Configuration File

### js/config.js

```javascript
const config = {
  // API Configuration
  apiUrl: process.env.API_URL || 'https://api.3asoftwares.com/graphql',
  authUrl: process.env.AUTH_URL || 'https://auth.3asoftwares.com',
  
  // Feature Flags
  enableDebug: process.env.NODE_ENV !== 'production',
  
  // Pagination
  defaultPageSize: 20,
  
  // Timeouts
  requestTimeout: 30000,
};

export default config;
```

---

## Environment Variables

### Production

| Variable  | Value                                 |
| --------- | ------------------------------------- |
| API_URL   | https://api.3asoftwares.com/graphql   |
| AUTH_URL  | https://auth.3asoftwares.com          |

### Development

| Variable  | Value                        |
| --------- | ---------------------------- |
| API_URL   | http://localhost:4000/graphql|
| AUTH_URL  | http://localhost:3001        |

---

## Vercel Environment

Set in Vercel Dashboard → Settings → Environment Variables:

| Variable | Environment | Value                               |
| -------- | ----------- | ----------------------------------- |
| API_URL  | Production  | https://api.3asoftwares.com/graphql |
| API_URL  | Preview     | https://staging-api.3asoftwares.com/graphql |

---

## Related Documentation

- [Deployment](DEPLOYMENT.md) - Deployment configuration
- [API](API.md) - API endpoints
