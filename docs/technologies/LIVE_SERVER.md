# Live Server

## Overview

**Version:** 1.2.2  
**Website:** [https://www.npmjs.com/package/live-server](https://www.npmjs.com/package/live-server)  
**Category:** Development Server

Live Server is a development server with live reload capability for static files.

---

## Why Live Server?

### Benefits

| Benefit          | Description                                   |
| ---------------- | --------------------------------------------- |
| **Live Reload**  | Auto-refresh browser on file changes          |
| **Zero Config**  | Works out of the box                          |
| **Static Files** | Perfect for HTML/CSS/JS projects              |
| **Fast**         | Lightweight and fast                          |

---

## Usage

### package.json Scripts

```json
{
  "scripts": {
    "start": "live-server",
    "dev": "concurrently \"npm run sass:watch\" \"npm run start\""
  }
}
```

### Commands

```bash
# Start server (default port 8080)
npm start

# Start with SCSS watching
npm run dev
```

---

## Configuration

### Command Line Options

```bash
# Custom port
live-server --port=3000

# Custom entry point
live-server --entry-file=index.html

# Open specific browser
live-server --browser=chrome

# Ignore files
live-server --ignore=scss,node_modules
```

---

## With Concurrently

Run SCSS compilation and live server together:

```json
{
  "scripts": {
    "sass:watch": "sass --watch scss/main.scss css/main.css",
    "start": "live-server",
    "dev": "concurrently \"npm run sass:watch\" \"npm run start\""
  }
}
```

---

## Related Documentation

- [SCSS](SCSS.md) - CSS compilation
- [JavaScript](JAVASCRIPT.md) - Application code
