# CodeLens: zen-quotes-extension

> Auto-generated codebase documentation optimized for LLM context.
> Paste into an AI chat to enable codebase-aware assistance.

## 1. PROJECT OVERVIEW

- **Project:** zen-quotes-extension
- **Files Analyzed:** 4
- **Total Lines:** 342
- **JS Files:** 1
- **HTML Files:** 1
- **CSS Files:** 1
- **Browser Extension:** Yes (Manifest V3)
- **Entry Points:** popup.js, popup.html

## 2. FILE STRUCTURE

```
manifest.json (24 lines)
popup.css (173 lines)
popup.html (39 lines)
popup.js (106 lines)
```

## 4. BROWSER EXTENSION MANIFEST

### `manifest.json`

- **Manifest Version:** 3
- **Name:** Zen Quotes
- **Version:** 1.0.0
- **Description:** Get inspired with random zen quotes every time you click!
- **Host Permissions:** `https://zenquotes.io/*`
- **Popup:** `popup.html`
- **Icons:** `{'16': 'icons/icon16.png', '48': 'icons/icon48.png', '128': 'icons/icon128.png'}`
- **All Referenced Files:**
  - `icons/icon128.png`
  - `icons/icon16.png`
  - `icons/icon48.png`
  - `popup.html`

## 5. HTML FILES

### `popup.html`

- **Lines:** 39
- **Title:** Zen Quotes
- **Stylesheets:** `popup.css`
- **Scripts (1):**
  - `popup.js`
- **IDs (5):** `p#quote-text, p#quote-author, button#new-quote-btn, div#loading, div#error`
- **CSS Classes (13):** `container, header, lotus, quote-container, quote-mark, quote-text, quote-author, quote-btn, btn-icon, loading, hidden, spinner, error`

## 6. CSS FILES

### `popup.css`

- **Lines:** 173
- **Total Rules:** 22
- **Animations:** `float, shimmer, spin, fadeIn`
- **Selectors (22):**
  - `*` (3 props: margin, padding, box-sizing)
  - `body` (5 props: font-family, width, min-height, background, color)
  - `.container` (4 props: padding, display, flex-direction, align-items)
  - `.header` (4 props: display, align-items, gap, margin-bottom)
  - `.lotus` (2 props: font-size, animation)
  - `50%` (1 props: transform)
  - `}

h1` (9 props: font-size, font-weight, letter-spacing, background, background-size)
  - `}

.quote-container` (11 props: background, border-radius, padding, margin-bottom, position)
  - `.quote-mark` (7 props: position, top, left, font-size, color)
  - `.quote-text` (7 props: font-size, line-height, color, font-style, text-align)
  - `.quote-author` (4 props: font-size, color, text-align, font-weight)
  - `.quote-author::before` (1 props: content)
  - `.quote-btn` (13 props: background, border, padding, border-radius, color)
  - `.quote-btn:hover` (2 props: transform, box-shadow)
  - `.quote-btn:active` (1 props: transform)
  - `.btn-icon` (1 props: font-size)
  - `.loading` (6 props: display, flex-direction, align-items, gap, color)
  - `.spinner` (6 props: width, height, border, border-top-color, border-radius)
  - `}

.error` (7 props: color, font-size, text-align, padding, background)
  - `.hidden` (1 props: display)
  - `.fade-in` (1 props: animation)
  - `to` (2 props: opacity, transform)

## 7. JAVASCRIPT FILES

### `popup.js`

- **Lines:** 106
- **Entry Point:** Yes ⭐
- **Functions (6):**
  - `async fetchQuote()` (line 15)
  - `displayQuote(quote, author)` (line 50)
  - `showLoading(show)` (line 64)
  - `showError()` (line 76)
  - `hideError()` (line 80)
  - `getLocalQuote()` (line 85)
- **Event Listeners:** `DOMContentLoaded, click`
- **DOM Queries:** `quote-text, quote-author, new-quote-btn, loading, error, .quote-container`

## 9. DETECTED PATTERNS & CONVENTIONS

- **Entry Points:** popup.js, popup.html
- **Other Patterns:**
  - Browser Extension (Manifest V3)

## 10. HOW TO USE THIS DOCUMENT WITH AN LLM

1. This document describes the **complete structure** of the codebase.
2. To modify a file, ask the LLM and reference the file path from this doc.
3. The LLM can see all classes, functions, DOM queries, and event listeners.
4. For browser extensions, the manifest section shows the full extension wiring.
5. For deeper context, paste the actual source code of the specific file you want to change.
6. The dependency/import map shows how files connect to each other.

**Tip:** Start your prompt with:
> "Given the codebase documented above, help me [your task]."
