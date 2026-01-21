# Deployment

## Overview

E-Storefront Support is deployed to Vercel for hosting.

---

## Vercel Deployment

### Automatic Deployment

1. Connect GitHub repository to Vercel
2. Push to `main` branch triggers production deploy
3. Pull requests get preview deployments

### Manual Deployment

```bash
# Install Vercel CLI
npm i -g vercel

# Login to Vercel
vercel login

# Deploy preview
vercel

# Deploy production
vercel --prod
```

---

## Build Configuration

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

## Pre-Deployment Checklist

- [ ] Build CSS: `npm run build`
- [ ] Test locally: `npm run start`
- [ ] Check all links work
- [ ] Verify API connectivity
- [ ] Update environment variables

---

## Environments

| Branch    | Environment | URL                          |
| --------- | ----------- | ---------------------------- |
| main      | Production  | support.3asoftwares.com      |
| develop   | Staging     | staging-support.vercel.app   |
| feature/* | Preview     | preview-*.vercel.app         |

---

## Rollback

```bash
# List deployments
vercel ls

# Promote previous deployment
vercel promote <deployment-url>
```

---

## Related Documentation

- [Vercel](technologies/VERCEL.md) - Vercel platform
- [Environment](ENVIRONMENT.md) - Environment configuration
