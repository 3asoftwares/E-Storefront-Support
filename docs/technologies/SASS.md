# Sass (dart-sass)

## Overview

**Version:** 1.69.0  
**Website:** [https://sass-lang.com](https://sass-lang.com)  
**Category:** CSS Preprocessor Compiler

Dart Sass is the primary implementation of Sass, compiling SCSS to CSS.

---

## Installation

```bash
npm install sass --save-dev
```

---

## Usage

### Command Line

```bash
# Compile once
sass scss/main.scss css/main.css

# Watch for changes
sass --watch scss/main.scss css/main.css

# Compile minified
sass scss/main.scss css/main.css --style=compressed

# Source maps
sass scss/main.scss css/main.css --source-map
```

### package.json Scripts

```json
{
  "scripts": {
    "sass": "sass scss/main.scss css/main.css",
    "sass:watch": "sass --watch scss/main.scss css/main.css",
    "sass:build": "sass scss/main.scss css/main.css --style=compressed --no-source-map"
  }
}
```

---

## Output Styles

| Style        | Description                    |
| ------------ | ------------------------------ |
| `expanded`   | Default, readable output       |
| `compressed` | Minified, production-ready     |

---

## Related Documentation

- [SCSS](SCSS.md) - SCSS syntax and features
- [CSS3](CSS3.md) - CSS output
