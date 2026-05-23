# CodeLens: would-you-ship-this

> Auto-generated codebase documentation optimized for LLM context.
> Paste into an AI chat to enable codebase-aware assistance.

## 1. PROJECT OVERVIEW

- **Project:** would-you-ship-this
- **Files Analyzed:** 8
- **Total Lines:** 1,031
- **JS Files:** 5
- **HTML Files:** 1
- **CSS Files:** 1
- **Browser Extension:** Yes (Manifest V3)
- **Entry Points:** popup.js, popup.html

## 2. FILE STRUCTURE

```
data\scenarios.js (434 lines)
lib\quiz.js (11 lines)
lib\storage.js (35 lines)
lib\utils.js (36 lines)
manifest.json (19 lines)
popup.css (181 lines)
popup.html (115 lines)
popup.js (200 lines)
```

## 4. BROWSER EXTENSION MANIFEST

### `manifest.json`

- **Manifest Version:** 3
- **Name:** Would You Ship This?
- **Version:** 1.0.0
- **Description:** A lightweight quiz extension for learning product cybersecurity, automotive security, cloud security, embedded security, and AI risk decisions.
- **Permissions:** `storage`
- **Popup:** `popup.html`
- **Icons:** `{'16': 'icons/icon16.png', '32': 'icons/icon32.png', '48': 'icons/icon48.png', '128': 'icons/icon128.png'}`
- **All Referenced Files:**
  - `icons/icon128.png`
  - `icons/icon16.png`
  - `icons/icon32.png`
  - `icons/icon48.png`
  - `popup.html`

## 5. HTML FILES

### `popup.html`

- **Lines:** 115
- **Title:** Would You Ship This?
- **Stylesheets:** `popup.css`
- **Scripts (5):**
  - `data/scenarios.js`
  - `lib/utils.js`
  - `lib/storage.js`
  - `lib/quiz.js`
  - `popup.js`
- **Semantic Tags:** <header> x1, <main> x1, <section> x5
- **IDs (26):** `section#home-screen, button#quick-round-btn, button#practice-btn, div#progress-summary, section#category-screen, button#back-home-btn, section#quiz-screen, span#question-counter, span#question-category, h2#scenario-title, p#scenario-text, div#answer-buttons, section#result-screen, h2#result-title, p#result-correct-answer, p#result-explanation, ul#risk-list, p#principle-text, p#learn-more-text, button#next-btn`
- **CSS Classes (22):** `app, header, subtitle, screen, active, card, button-group, primary-btn, secondary-btn, stats, vertical, category-btn, text-btn, quiz-top, tag, scenario-text, answer-btn, danger, result-answer, result-block, learn-more, final-verdict`

## 6. CSS FILES

### `popup.css`

- **Lines:** 181
- **Total Rules:** 30
- **CSS Variables (10):** `--bg, --panel, --panel-2, --text, --muted, --accent, --accent-2, --danger, --border, --shadow`
- **Media Queries (1):**
  - `(prefers-reduced-motion: reduce)` (1 selectors)
- **Selectors (30):**
  - `:root` (10 props: --bg, --panel, --panel-2, --text, --muted)
  - `*` (1 props: box-sizing)
  - `body` (6 props: margin, width, min-height, font-family, background)
  - `.app` (1 props: padding)
  - `.header` (1 props: margin-bottom)
  - `.header h1` (2 props: margin, font-size)
  - `.subtitle` (3 props: margin, color, font-size)
  - `.screen` (1 props: display)
  - `.screen.active` (1 props: display)
  - `.card` (6 props: background, border, border-radius, padding, margin-bottom)
  - `.card h2` (2 props: margin-top, font-size)
  - `.button-group` (4 props: display, gap, flex-wrap, margin-top)
  - `.button-group.vertical` (1 props: flex-direction)
  - `button` (6 props: border, border-radius, padding, font-size, cursor)
  - `button:hover` (1 props: opacity)
  - `button:active` (1 props: transform)
  - `button:focus-visible` (2 props: outline, outline-offset)
  - `.primary-btn` (3 props: background, color, font-weight)
  - `.secondary-btn,
.category-btn,
.answer-btn` (3 props: background, color, border-color)
  - `.answer-btn.danger` (1 props: border-color)
  - `.text-btn` (3 props: background, color, padding-left)
  - `.quiz-top` (5 props: display, justify-content, align-items, gap, margin-bottom)
  - `.tag` (5 props: padding, border-radius, background, color, font-size)
  - `.scenario-text` (2 props: color, line-height)
  - `.result-answer,
.final-verdict` (2 props: color, font-weight)
  - `.result-block h3` (2 props: margin-bottom, font-size)
  - `.result-block ul` (2 props: margin, padding-left)
  - `.stats` (2 props: color, line-height)
  - `details` (2 props: margin-top, color)
  - `summary` (2 props: cursor, color)

## 7. JAVASCRIPT FILES

### `data\scenarios.js`

- **Lines:** 434

### `lib\quiz.js`

- **Lines:** 11

### `lib\storage.js`

- **Lines:** 35

### `lib\utils.js`

- **Lines:** 36

### `popup.js`

- **Lines:** 200
- **Functions (8):**
  - `showScreen(screenName)` (line 34)
  - `resetRound(questions)` (line 39)
  - `renderQuestion()` (line 47)
  - `renderResult(selectedAnswer)` (line 59)
  - `renderFinal()` (line 88)
  - `buildTakeaways()` (line 110)
  - `formatAnswerLabel(answer)` (line 132)
  - `async loadProgressSummary()` (line 141)
- **Event Listeners:** `click`
- **DOM Queries:** `home-screen, category-screen, quiz-screen, result-screen, final-screen, progress-summary, question-counter, question-category, scenario-title, scenario-text, result-title, result-correct-answer, result-explanation, risk-list, principle-text, learn-more-text, final-score, final-verdict, takeaway-list, quick-round-btn, practice-btn, back-home-btn, next-btn, play-again-btn, home-btn, .category-btn, .answer-btn`

## 9. DETECTED PATTERNS & CONVENTIONS

- **Architecture:** Standard src/lib layout
- **Entry Points:** popup.js, popup.html
- **Other Patterns:**
  - Browser Extension (Manifest V3)
  - Permissions: storage

## 10. HOW TO USE THIS DOCUMENT WITH AN LLM

1. This document describes the **complete structure** of the codebase.
2. To modify a file, ask the LLM and reference the file path from this doc.
3. The LLM can see all classes, functions, DOM queries, and event listeners.
4. For browser extensions, the manifest section shows the full extension wiring.
5. For deeper context, paste the actual source code of the specific file you want to change.
6. The dependency/import map shows how files connect to each other.

**Tip:** Start your prompt with:
> "Given the codebase documented above, help me [your task]."
