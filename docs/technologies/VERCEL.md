# Vercel

## Overview

**Website:** [https://vercel.com](https://vercel.com)  
**Category:** Deployment Platform

Vercel is a cloud platform for static sites and serverless functions.

---

## Why Vercel?

### Benefits

| Benefit              | Description                                   |
| -------------------- | --------------------------------------------- |
| **Static Hosting**   | Perfect for static HTML/CSS/JS sites          |
| **Global CDN**       | Fast content delivery worldwide               |
| **Auto Deploy**      | Deploys on every push                         |
| **Preview URLs**     | Every PR gets a preview                       |
| **Free Tier**        | Generous free tier for small projects         |

---

## Configuration

### vercel.json

```json
{
  "rewrites": [{ "source": "/(.*)", "destination": "/" }],
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        { "key": "X-Content-Type-Options", "value": "nosniff" },
        { "key": "X-Frame-Options", "value": "DENY" },
        { "key": "X-XSS-Protection", "value": "1; mode=block" }
      ]
    }
  ]
}
```

---

## Deployment

### Automatic Deployment

1. Connect GitHub repository to Vercel
2. Push to `main` branch
3. Vercel automatically builds and deploys

### Manual Deployment

```bash
# Install Vercel CLI
npm i -g vercel

# Login
vercel login

# Deploy preview
vercel

# Deploy production
vercel --prod
```

---

## Environment

| Branch     | Environment | URL                           |
| ---------- | ----------- | ----------------------------- |
| `main`     | Production  | support.3asoftwares.com       |
| `develop`  | Preview     | develop-support.vercel.app    |
| PR branches| Preview     | pr-xxx-support.vercel.app     |

---

## Production URL

| Type       | URL                                |
| ---------- | ---------------------------------- |
| Production | https://support.3asoftwares.com    |
| API        | https://api.3asoftwares.com/graphql|

---

## Related Documentation

- [JavaScript](JAVASCRIPT.md) - Application code
- [Bootstrap](BOOTSTRAP.md) - UI framework
