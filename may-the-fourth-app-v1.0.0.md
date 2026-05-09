# CodeLens: may-the-fourth-quiz

> Auto-generated codebase documentation optimized for LLM context.
> Paste into an AI chat to enable codebase-aware assistance.

## 1. PROJECT OVERVIEW

- **Project:** may-the-fourth-quiz
- **Files Analyzed:** 4
- **Total Lines:** 645
- **JS Files:** 1
- **HTML Files:** 1
- **CSS Files:** 1
- **Browser Extension:** Yes (Manifest V3)
- **Entry Points:** popup.js, popup.html

## 2. FILE STRUCTURE

```
manifest.json (20 lines)
popup.css (265 lines)
popup.html (45 lines)
popup.js (315 lines)
```

## 4. BROWSER EXTENSION MANIFEST

### `manifest.json`

- **Manifest Version:** 3
- **Name:** Which Side Are You?
- **Version:** 1.0.0
- **Description:** May the Fourth personality quiz — discover your galactic archetype!
- **Permissions:** `storage`
- **Popup:** `popup.html`
- **Icons:** `{'16': 'icons/icon-default-16.png', '48': 'icons/icon-default-48.png', '128': 'icons/icon-default-128.png'}`
- **All Referenced Files:**
  - `icons/icon-default-128.png`
  - `icons/icon-default-16.png`
  - `icons/icon-default-48.png`
  - `popup.html`

## 5. HTML FILES

### `popup.html`

- **Lines:** 45
- **Title:** Which Side Are You?
- **Stylesheets:** `popup.css`
- **Scripts (1):**
  - `popup.js`
- **IDs (16):** `canvas#starfield, div#screen-intro, button#btn-start, div#screen-quiz, div#progress-fill, p#question-counter, h2#question-text, div#answers-container, div#screen-result, div#result-emoji, h2#result-title, p#result-description, div#result-breakdown, button#btn-copy, button#btn-retake, p#copy-confirmation`
- **CSS Classes (18):** `screen, active, crawl-title, subtitle, description, btn-primary, progress-bar, progress-fill, question-counter, question-text, answers-container, result-emoji, result-title, result-description, result-breakdown, result-actions, btn-secondary, copy-confirmation`

## 6. CSS FILES

### `popup.css`

- **Lines:** 265
- **Total Rules:** 36
- **Selectors (36):**
  - `*` (3 props: margin, padding, box-sizing)
  - `body` (7 props: width, height, font-family, background, color)
  - `#starfield` (6 props: position, top, left, width, height)
  - `.screen` (14 props: position, top, left, width, height)
  - `.screen.active` (2 props: opacity, visibility)
  - `.crawl-title` (7 props: font-size, font-weight, text-align, letter-spacing, line-height)
  - `.subtitle` (5 props: font-size, color, letter-spacing, text-transform, margin-bottom)
  - `.description` (5 props: font-size, color, text-align, margin-bottom, line-height)
  - `.btn-primary` (10 props: background, color, border, padding, font-size)
  - `.btn-primary:hover` (2 props: transform, box-shadow)
  - `.btn-secondary` (9 props: background, color, border, padding, font-size)
  - `.btn-secondary:hover` (1 props: background)
  - `.progress-bar` (6 props: width, height, background, border-radius, margin-bottom)
  - `.progress-fill` (5 props: height, width, background, border-radius, transition)
  - `.question-counter` (5 props: font-size, color, letter-spacing, text-transform, margin-bottom)
  - `.question-text` (7 props: font-size, color, text-align, line-height, margin-bottom)
  - `.answers-container` (4 props: width, display, flex-direction, gap)
  - `.answer-btn` (10 props: width, background, border, color, padding)
  - `.answer-btn:hover` (3 props: background, border-color, transform)
  - `#screen-result` (2 props: justify-content, padding-top)
  - `.result-emoji` (2 props: font-size, margin-bottom)
  - `.result-title` (4 props: font-size, font-weight, text-shadow, margin-bottom)
  - `.result-description` (6 props: font-size, color, text-align, line-height, margin-bottom)
  - `.result-breakdown` (2 props: width, margin-bottom)
  - `.breakdown-row` (4 props: display, align-items, margin-bottom, font-size)
  - `.breakdown-label` (5 props: width, color, text-align, padding-right, flex-shrink)
  - `.breakdown-bar-bg` (6 props: flex, height, background, border-radius, overflow)
  - `.breakdown-bar` (3 props: height, border-radius, transition)
  - `.breakdown-pct` (3 props: width, color, font-size)
  - `.result-actions` (3 props: display, gap, margin-top)
  - `.copy-confirmation` (4 props: font-size, color, margin-top, height)
  - `.color-jedi` (1 props: background)
  - `.color-sith` (1 props: background)
  - `.color-smuggler` (1 props: background)
  - `.color-droid` (1 props: background)
  - `.color-bountyhunter` (1 props: background)

## 7. JAVASCRIPT FILES

### `popup.js`

- **Lines:** 315
- **Functions (12):**
  - `initStarfield()` (line 124)
  - `resize()` (line 130)
  - `createStars()` (line 135)
  - `draw()` (line 148)
  - `showScreen(screen)` (line 171)
  - `renderQuestion()` (line 177)
  - `selectAnswer(answer)` (line 194)
  - `showResult()` (line 211)
  - `updateBadgeIcon(arch)` (line 251)
  - `copyResult()` (line 277)
  - `resetQuiz()` (line 288)
  - `init()` (line 297)
- **Constants:** `ARCHETYPES, QUESTIONS, STAR_COUNT`
- **Event Listeners:** `resize, click`
- **DOM Queries:** `screen-intro, screen-quiz, screen-result, btn-start, btn-copy, btn-retake, question-counter, question-text, answers-container, progress-fill, result-emoji, result-title, result-description, result-breakdown, copy-confirmation, starfield`

## 9. DETECTED PATTERNS & CONVENTIONS

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
