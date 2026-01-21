# Support Website Deployment Guide

## 📑 Overview

E-Storefront Support is a static website deployed to **Vercel**.

## 🚀 Deployment Methods

### Vercel (Recommended)

#### Automatic Deployment

Connect GitHub repository to Vercel for automatic deployments on push.

#### Manual Deployment

```bash
# Install Vercel CLI
npm install -g vercel

# Login
vercel login

# Deploy
vercel

# Deploy to production
vercel --prod
```

### Configuration

```json
// vercel.json
{
    "rewrites": [{ "source": "/(.*)", "destination": "/index.html" }]
}
```

## 🔧 Build Process

### Pre-Deployment Steps

```bash
# 1. Compile SCSS to CSS
npm run sass

# 2. Verify output
ls -la css/main.css

# 3. Test locally
npm start
```

### Production Checklist

- [ ] SCSS compiled to CSS
- [ ] All images optimized
- [ ] JavaScript minified (if applicable)
- [ ] Environment variables configured
- [ ] Forms tested
- [ ] Mobile responsiveness verified

## 🌐 Environment Variables

Set in Vercel dashboard:

| Variable      | Description      |
| ------------- | ---------------- |
| `API_URL`     | Backend API URL  |
| `GRAPHQL_URL` | GraphQL endpoint |

## 📊 Monitoring

### Vercel Analytics

Enable in Vercel dashboard for:

- Page views
- Performance metrics
- Error tracking

---

See also:

- [ARCHITECTURE.md](./ARCHITECTURE.md) - Project architecture
