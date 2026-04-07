# CodeLens: japanese-learner-extension-dashboard-toyota-v1.1.11

> Auto-generated codebase documentation optimized for LLM context.
> Paste into an AI chat to enable codebase-aware assistance.

## 1. PROJECT OVERVIEW

- **Project:** japanese-learner-extension-dashboard-toyota-v1.1.11
- **Files Analyzed:** 12
- **Total Lines:** 5,401
- **JS Files:** 6
- **HTML Files:** 2
- **CSS Files:** 2
- **Browser Extension:** Yes (Manifest V3)
- **Entry Points:** background.js

## 2. FILE STRUCTURE

```
background.js (54 lines)
dashboard\dashboard.css (1240 lines)
dashboard\dashboard.html (358 lines)
dashboard\dashboard.js (1360 lines)
data\lessons.json (317 lines)
manifest.json (29 lines)
popup\popup.css (771 lines)
popup\popup.html (166 lines)
popup\popup.js (728 lines)
utils\storage.js (91 lines)
utils\theme.js (41 lines)
utils\tts.js (246 lines)
```

## 4. BROWSER EXTENSION MANIFEST

### `manifest.json`

- **Manifest Version:** 3
- **Name:** 日本語 Learner — Japanese for English Speakers
- **Version:** 1.1.11
- **Description:** A lightweight, offline-capable Japanese language learning extension with flashcards, quizzes, and pronunciation.
- **Permissions:** `storage, tts`
- **Service Worker:** `background.js`
- **Popup:** `popup/popup.html`
- **Icons:** `{'16': 'icons/icon16.png', '48': 'icons/icon48.png', '128': 'icons/icon128.png'}`
- **All Referenced Files:**
  - `background.js`
  - `icons/icon128.png`
  - `icons/icon16.png`
  - `icons/icon48.png`
  - `popup/popup.html`

## 5. HTML FILES

### `dashboard\dashboard.html`

- **Lines:** 358
- **Title:** 日本語 Learner — Dashboard
- **Stylesheets:** `dashboard.css`
- **Scripts (4):**
  - `../utils/storage.js`
  - `../utils/tts.js`
  - `../utils/theme.js`
  - `dashboard.js`
- **Semantic Tags:** <header> x1, <nav> x1, <main> x5, <section> x2, <aside> x1
- **IDs (80):** `aside#sidebar, span#sidebar-xp, span#sidebar-streak, span#sidebar-online-dot, span#sidebar-online-label, button#btn-sidebar-toggle, h2#topbar-title, button#btn-dash-theme, span#dash-theme-icon, main#dash-view-home, h2#hero-greeting-text, span#home-total-xp, span#home-streak, span#home-completed, span#home-total-cards, div#home-module-list, button#qa-random-card, button#qa-check-updates, button#qa-all-quiz, button#qa-reset`
- **CSS Classes (102):** `sidebar, sidebar-header, sidebar-logo, sidebar-title, sidebar-nav, nav-item, active, nav-icon, nav-label, sidebar-footer, sidebar-stat, stat-emoji, online-dot, offline, main-wrapper, topbar, topbar-menu-btn, topbar-title, topbar-actions, topbar-icon-btn, dash-view, home-hero, hero-greeting, hero-subtitle, hero-stats-row, hero-stat-card, hero-stat-number, hero-stat-label, home-section, section-title`

### `popup\popup.html`

- **Lines:** 166
- **Title:** 日本語 Learner
- **Stylesheets:** `popup.css`
- **Scripts (4):**
  - `../utils/storage.js`
  - `../utils/tts.js`
  - `../utils/theme.js`
  - `popup.js`
- **Semantic Tags:** <header> x1, <main> x5
- **IDs (44):** `button#btn-theme-toggle, span#theme-icon, button#btn-settings, span#xp-display, span#streak-display, span#online-indicator, span#online-label, main#view-modules, div#module-list, button#btn-check-updates, button#btn-open-dashboard, main#view-flashcard, button#btn-back-to-modules, span#card-counter, div#card-progress-bar, div#flashcard, span#card-japanese, span#card-romaji, button#btn-speak, span#card-english`
- **CSS Classes (55):** `header, header-left, logo-icon, app-title, header-right, icon-btn, stats-bar, stat, stat-icon, stat-value, online-dot, offline, view, active, module-list, footer-actions, btn, btn-secondary, btn-primary, flashcard-header, btn-back, card-counter, progress-bar-container, progress-bar, flashcard, flashcard-inner, flashcard-front, card-japanese, card-romaji, btn-speak`

## 6. CSS FILES

### `dashboard\dashboard.css`

- **Lines:** 1240
- **Total Rules:** 171
- **CSS Variables (22):** `--bg-primary, --bg-secondary, --bg-card, --text-primary, --text-secondary, --accent, --accent-hover, --accent-light, --border, --success, --warning, --danger, --shadow-sm, --shadow-md, --shadow-lg, --radius-sm, --radius-md, --radius-lg, --radius-xl, --font-jp-size`
- **Animations:** `fadeInDash, bounceInDash`
- **Media Queries (2):**
  - `(max-width: 900px)` (3 selectors)
  - `(max-width: 600px)` (4 selectors)
- **Selectors (171):**
  - `:root` (22 props: --bg-primary, --bg-secondary, --bg-card, --text-primary, --text-secondary)
  - `[data-theme="dark"]` (12 props: --bg-primary, --bg-secondary, --bg-card, --text-primary, --text-secondary)
  - `[data-fontsize="small"]` (1 props: --font-jp-size)
  - `[data-fontsize="medium"]` (1 props: --font-jp-size)
  - `[data-fontsize="large"]` (1 props: --font-jp-size)
  - `*, *::before, *::after` (3 props: margin, padding, box-sizing)
  - `html, body` (2 props: height, overflow)
  - `body` (5 props: font-family, background-color, color, display, transition)
  - `.sidebar` (9 props: width, min-width, height, background, border-right)
  - `.sidebar.collapsed` (4 props: transform, width, min-width, overflow)
  - `.sidebar-header` (5 props: display, align-items, gap, padding, border-bottom)
  - `.sidebar-logo` (1 props: font-size)
  - `.sidebar-title` (3 props: font-size, font-weight, letter-spacing)
  - `.sidebar-nav` (5 props: flex, display, flex-direction, padding, gap)
  - `.nav-item` (14 props: display, align-items, gap, padding, border)
  - `.nav-item:hover` (2 props: background, color)
  - `.nav-item.active` (2 props: background, color)
  - `.nav-icon` (3 props: font-size, width, text-align)
  - `.sidebar-footer` (5 props: padding, border-top, display, flex-direction, gap)
  - `.sidebar-stat` (6 props: display, align-items, gap, font-size, font-weight)
  - `.stat-emoji` (1 props: font-size)
  - `.online-dot` (4 props: width, height, border-radius, display)
  - `.online-dot.online` (2 props: background, box-shadow)
  - `.online-dot.offline` (1 props: background)
  - `.main-wrapper` (5 props: flex, display, flex-direction, height, overflow)
  - `.topbar` (7 props: display, align-items, gap, padding, background)
  - `.topbar-menu-btn` (6 props: background, border, font-size, cursor, color)
  - `.topbar-title` (3 props: flex, font-size, font-weight)
  - `.topbar-actions` (2 props: display, gap)
  - `.topbar-icon-btn` (7 props: background, border, font-size, cursor, padding)
  - `.topbar-icon-btn:hover` (1 props: background)
  - `.dash-view` (5 props: display, padding, overflow-y, flex, animation)
  - `.dash-view.active` (1 props: display)
  - `to` (2 props: opacity, transform)
  - `}



.home-hero` (1 props: margin-bottom)
  - `.hero-greeting h2` (3 props: font-size, font-weight, margin-bottom)
  - `.hero-subtitle` (3 props: font-size, color, margin-bottom)
  - `.hero-stats-row` (3 props: display, grid-template-columns, gap)
  - `.hero-stat-card` (9 props: background, border, border-radius, padding, text-align)
  - `.hero-stat-card:hover` (1 props: box-shadow)
  - ... and 131 more

### `popup\popup.css`

- **Lines:** 771
- **Total Rules:** 108
- **CSS Variables (20):** `--bg-primary, --bg-secondary, --bg-card, --text-primary, --text-secondary, --accent, --accent-hover, --accent-light, --border, --success, --warning, --danger, --shadow-sm, --shadow-md, --shadow-lg, --radius-sm, --radius-md, --radius-lg, --font-jp-size, --transition`
- **Animations:** `fadeIn, bounceIn`
- **Selectors (108):**
  - `:root` (20 props: --bg-primary, --bg-secondary, --bg-card, --text-primary, --text-secondary)
  - `[data-theme="dark"]` (12 props: --bg-primary, --bg-secondary, --bg-card, --text-primary, --text-secondary)
  - `[data-fontsize="small"]` (1 props: --font-jp-size)
  - `[data-fontsize="medium"]` (1 props: --font-jp-size)
  - `[data-fontsize="large"]` (1 props: --font-jp-size)
  - `*, *::before, *::after` (3 props: margin, padding, box-sizing)
  - `body` (8 props: width, min-height, max-height, overflow-y, font-family)
  - `body::-webkit-scrollbar` (1 props: width)
  - `body::-webkit-scrollbar-track` (1 props: background)
  - `body::-webkit-scrollbar-thumb` (2 props: background, border-radius)
  - `.header` (9 props: display, align-items, justify-content, padding, background)
  - `.header-left` (3 props: display, align-items, gap)
  - `.logo-icon` (1 props: font-size)
  - `.app-title` (3 props: font-size, font-weight, letter-spacing)
  - `.header-right` (3 props: display, align-items, gap)
  - `.icon-btn` (7 props: background, border, font-size, cursor, padding)
  - `.icon-btn:hover` (1 props: background)
  - `.stats-bar` (5 props: display, justify-content, padding, background, border-bottom)
  - `.stat` (5 props: display, align-items, gap, font-size, font-weight)
  - `.stat-icon` (1 props: font-size)
  - `.online-dot` (4 props: width, height, border-radius, display)
  - `.online-dot.online` (2 props: background, box-shadow)
  - `.online-dot.offline` (1 props: background)
  - `.view` (3 props: display, padding, animation)
  - `.view.active` (1 props: display)
  - `to` (2 props: opacity, transform)
  - `}



.module-list` (4 props: display, flex-direction, gap, margin-bottom)
  - `.module-card` (8 props: background, border, border-radius, padding, cursor)
  - `.module-card:hover` (2 props: box-shadow, transform)
  - `.module-card-header` (4 props: display, align-items, gap, margin-bottom)
  - `.module-icon` (8 props: font-size, width, height, display, align-items)
  - `.module-info h3` (3 props: font-size, font-weight, margin-bottom)
  - `.module-info p` (3 props: font-size, color, line-height)
  - `.module-meta` (4 props: display, align-items, justify-content, margin-top)
  - `.module-card-count` (2 props: font-size, color)
  - `.module-status` (4 props: font-size, font-weight, padding, border-radius)
  - `.module-status.completed` (2 props: background, color)
  - `.module-status.in-progress` (2 props: background, color)
  - `.module-status.not-started` (2 props: background, color)
  - `.module-progress-bar` (5 props: height, background, border-radius, margin-top, overflow)
  - ... and 68 more

## 7. JAVASCRIPT FILES

### `background.js`

- **Lines:** 54
- **Entry Point:** Yes ⭐
- **Functions (1):**
  - `async fetchLessonUpdates()` (line 40)
- **Constants:** `MOCK_UPDATE_URL`
- **Event Listeners:** `chrome.runtime.onMessage, chrome.runtime.onInstalled`

### `dashboard\dashboard.js`

- **Lines:** 1360
- **Functions (29):**
  - `qsa(sel)` (line 33)
  - `async init()` (line 41)
  - `applySettings()` (line 71)
  - `updateDashThemeIcon()` (line 92)
  - `checkTTSStatus()` (line 100)
  - `async loadLessons()` (line 123)
  - `detectOnlineStatus()` (line 148)
  - `update()` (line 149)
  - `async updateSidebarStats()` (line 169)
  - `showDashView(viewName)` (line 188)
  - `async renderHome()` (line 226)
  - `renderModuleGrid(containerId, progress, onClickFn)` (line 294)
  - `openStudyModule(moduleId)` (line 361)
  - `renderStudyCard()` (line 398)
  - `closeStudySession()` (line 464)
  - `async renderStudyModuleList()` (line 479)
  - `async renderQuizHub()` (line 490)
  - `findModuleById(moduleId)` (line 497)
  - `startModuleQuiz(moduleId)` (line 509)
  - `startMixedQuiz()` (line 546)
  - `renderDashQuizQuestion()` (line 604)
  - `handleDashAnswer(btnElement, selected, correct, question)` (line 660)
  - `async showDashQuizResults()` (line 712)
  - `resetQuizHub()` (line 777)
  - `async renderProgressView()` (line 805)
  - `showRandomCard()` (line 882)
  - `closeModal()` (line 943)
  - `showDashToast(message)` (line 954)
  - `bindEvents()` (line 972)
- **Event Listeners:** `online, offline, click, change, keydown`

### `popup\popup.js`

- **Lines:** 728
- **Functions (19):**
  - `qsa(sel)` (line 25)
  - `async init()` (line 33)
  - `applySettings()` (line 63)
  - `updateThemeIcon()` (line 84)
  - `async loadLessons()` (line 96)
  - `async renderModules()` (line 121)
  - `async updateStatsBar()` (line 194)
  - `detectOnlineStatus()` (line 209)
  - `update()` (line 210)
  - `showView(viewName)` (line 233)
  - `openModule(moduleId)` (line 249)
  - `renderCard()` (line 267)
  - `updateRomajiVisibility()` (line 335)
  - `startQuiz()` (line 350)
  - `renderQuizQuestion()` (line 362)
  - `handleAnswer(btnElement, selected, correct)` (line 413)
  - `async showResults()` (line 447)
  - `showToast(message)` (line 478)
  - `bindEvents()` (line 498)
- **Event Listeners:** `click, online, offline, change, keydown`

### `utils\storage.js`

- **Lines:** 91

### `utils\theme.js`

- **Lines:** 41
- **Event Listeners:** `change`

### `utils\tts.js`

- **Lines:** 246
- **Event Listeners:** `click`
- **DOM Queries:** `.tts-warning-toast`

## 8. OTHER CONFIG FILES

### `data\lessons.json`

- **Type:** json
- **Lines:** 317
- **Keys:** `version, lastModified, modules`

## 9. DETECTED PATTERNS & CONVENTIONS

- **Entry Points:** background.js
- **Other Patterns:**
  - Browser Extension (Manifest V3)
  - Background service worker: background.js
  - Permissions: storage, tts

## 10. HOW TO USE THIS DOCUMENT WITH AN LLM

1. This document describes the **complete structure** of the codebase.
2. To modify a file, ask the LLM and reference the file path from this doc.
3. The LLM can see all classes, functions, DOM queries, and event listeners.
4. For browser extensions, the manifest section shows the full extension wiring.
5. For deeper context, paste the actual source code of the specific file you want to change.
6. The dependency/import map shows how files connect to each other.

**Tip:** Start your prompt with:
> "Given the codebase documented above, help me [your task]."
