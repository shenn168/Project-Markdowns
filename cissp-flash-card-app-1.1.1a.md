# CodeLens: cissp-flash-card-app-1.1.1a

> Auto-generated codebase documentation optimized for LLM context.
> Paste into an AI chat to enable codebase-aware assistance.

## 1. PROJECT OVERVIEW

- **Project:** cissp-flash-card-app-1.1.1a
- **Files Analyzed:** 21
- **Total Lines:** 7,325
- **JS Files:** 13
- **HTML Files:** 3
- **CSS Files:** 1
- **Browser Extension:** Yes (Manifest V3)
- **Entry Points:** popup.html

## 2. FILE STRUCTURE

```
css\styles.css (1330 lines)
data\cissp-advanced-deck.json (643 lines)
data\cissp-beginner-8-domains-part-1.json (632 lines)
data\cissp-starter-deck.json (410 lines)
generate-icons.html (89 lines)
js\app.js (309 lines)
js\dashboard.js (448 lines)
js\db.js (310 lines)
js\deckmanager.js (94 lines)
js\exporter.js (245 lines)
js\importer.js (203 lines)
js\parsers.js (484 lines)
js\popup.js (241 lines)
js\scenario.js (287 lines)
js\settings.js (180 lines)
js\sm2.js (80 lines)
js\studymode.js (452 lines)
js\utils.js (260 lines)
manifest.json (26 lines)
newtab.html (284 lines)
popup.html (318 lines)
```

## 4. BROWSER EXTENSION MANIFEST

### `manifest.json`

- **Manifest Version:** 3
- **Name:** CISSP StudyDeck
- **Version:** 1.1.1
- **Description:** Offline CISSP flash card study tool with spaced repetition, scenario cards, and collaborative deck merging.
- **Permissions:** `storage`
- **Popup:** `popup.html`
- **Icons:** `{'16': 'assets/icon16.png', '48': 'assets/icon48.png', '128': 'assets/icon128.png'}`
- **All Referenced Files:**
  - `assets/icon128.png`
  - `assets/icon16.png`
  - `assets/icon48.png`
  - `popup.html`

## 5. HTML FILES

### `generate-icons.html`

- **Lines:** 89
- **Title:** Generate CISSP StudyDeck Icons
- **Scripts (1):**
  - Inline: `function drawIcon(canvasId) {
      const canvas = document.getElementById(canvasId);
      const ctx = canvas.getContex...`
- **Inline `<style>` blocks:** 1
- **IDs (3):** `canvas#c16, canvas#c48, canvas#c128`
- **CSS Classes (1):** `row`

### `newtab.html`

- **Lines:** 284
- **Title:** CISSP StudyDeck
- **Stylesheets:** `css/styles.css`
- **Scripts (12):**
  - `js/utils.js`
  - `js/db.js`
  - `js/parsers.js`
  - `js/sm2.js`
  - `js/importer.js`
  - `js/studymode.js`
  - `js/scenario.js`
  - `js/dashboard.js`
  - `js/exporter.js`
  - `js/deckmanager.js`
  - `js/settings.js`
  - `js/app.js`
- **Semantic Tags:** <header> x1, <nav> x1, <main> x1, <section> x8
- **IDs (63):** `button#themeToggle, section#view-home, div#homeStats, span#statTotalCards, span#statDueToday, span#statMastered, span#statStreak, div#homeDomains, section#view-import, div#importZone, div#importDropzone, input#importFileInput, input#mergeOnImport, div#mergePreview, div#mergeStats, div#mergeList, button#confirmImport, button#cancelImport, div#importErrors, ul#importErrorList`
- **CSS Classes (83):** `topnav, topnav-brand, brand-icon, brand-text, brand-accent, topnav-links, nav-btn, active, theme-toggle, theme-icon-dark, theme-icon-light, main-content, view, home-hero, home-subtitle, home-stats, stat-card, stat-number, stat-label, home-actions, btn, btn-primary, btn-lg, btn-secondary, home-domains, view-container, view-desc, import-zone, import-dropzone, drop-icon`

### `popup.html`

- **Lines:** 318
- **Title:** CISSP StudyDeck
- **Scripts (1):**
  - `js/popup.js`
- **Inline `<style>` blocks:** 1
- **IDs (3):** `button#popupThemeToggle, div#popupBody, div#popupLoading`
- **CSS Classes (11):** `popup-header, popup-brand, popup-brand-icon, popup-brand-accent, theme-btn, theme-dark, theme-light, popup-body, loading, loading-spinner, popup-footer`

## 6. CSS FILES

### `css\styles.css`

- **Lines:** 1330
- **Total Rules:** 197
- **CSS Variables (35):** `--bg-primary, --bg-secondary, --bg-card, --bg-card-hover, --bg-input, --bg-tooltip, --text-primary, --text-secondary, --text-muted, --text-inverse, --accent-primary, --accent-secondary, --accent-glow, --accent-green, --accent-green-glow, --accent-yellow, --accent-yellow-glow, --accent-red, --accent-red-glow, --accent-purple`
- **Animations:** `fadeIn, toastIn, toastOut`
- **Media Queries (1):**
  - `(max-width: 768px)` (11 selectors)
- **Selectors (197):**
  - `:root` (35 props: --bg-primary, --bg-secondary, --bg-card, --bg-card-hover, --bg-input)
  - `[data-theme="light"]` (25 props: --bg-primary, --bg-secondary, --bg-card, --bg-card-hover, --bg-input)
  - `*, *::before, *::after` (3 props: margin, padding, box-sizing)
  - `html` (2 props: font-size, scroll-behavior)
  - `body` (6 props: font-family, background, color, line-height, min-height)
  - `[data-theme="dark"] body::before` (7 props: content, position, inset, background-image, background-size)
  - `h1, h2, h3, h4` (2 props: font-weight, line-height)
  - `h1` (1 props: font-size)
  - `h2` (1 props: font-size)
  - `h3` (1 props: font-size)
  - `h4` (5 props: font-size, color, text-transform, letter-spacing, margin-bottom)
  - `a` (3 props: color, text-decoration, transition)
  - `a:hover` (1 props: color)
  - `.brand-accent` (1 props: color)
  - `.topnav` (11 props: position, top, z-index, display, align-items)
  - `.topnav-brand` (6 props: display, align-items, gap, font-size, font-weight)
  - `.brand-icon` (1 props: font-size)
  - `.topnav-links` (5 props: display, gap, flex-wrap, flex, justify-content)
  - `.nav-btn` (10 props: background, border, color, padding, border-radius)
  - `.nav-btn:hover` (3 props: color, background, border-color)
  - `.nav-btn.active` (3 props: color, background, border-color)
  - `.theme-toggle` (8 props: background, border, border-radius, padding, cursor)
  - `.theme-toggle:hover` (2 props: border-color, box-shadow)
  - `[data-theme="dark"] .theme-icon-light` (1 props: display)
  - `[data-theme="dark"] .theme-icon-dark` (1 props: display)
  - `[data-theme="light"] .theme-icon-dark` (1 props: display)
  - `[data-theme="light"] .theme-icon-light` (1 props: display)
  - `.main-content` (5 props: position, z-index, max-width, margin, padding)
  - `.view` (1 props: display)
  - `.view.active` (2 props: display, animation)
  - `to` (2 props: opacity, transform)
  - `}

.view-container` (2 props: max-width, margin)
  - `.view-desc` (2 props: color, margin-bottom)
  - `.btn` (12 props: display, align-items, gap, padding, border)
  - `.btn-primary` (3 props: background, color, border-color)
  - `.btn-primary:hover` (2 props: background, box-shadow)
  - `.btn-secondary` (3 props: background, color, border-color)
  - `.btn-secondary:hover` (1 props: background)
  - `.btn-ghost` (3 props: background, color, border-color)
  - `.btn-ghost:hover` (2 props: color, border-color)
  - ... and 157 more

## 7. JAVASCRIPT FILES

### `js\app.js`

- **Lines:** 309
- **Functions (8):**
  - `navigateTo(viewName)` (line 43)
  - `async initHome()` (line 84)
  - `initImportView()` (line 126)
  - `async handleFile(file)` (line 171)
  - `showImportPreview(result)` (line 200)
  - `async confirmImport()` (line 262)
  - `cancelImport()` (line 280)
  - `getInitialView()` (line 287)
- **Event Listeners:** `click, change, dragover, dragleave, drop, hashchange`
- **DOM Queries:** `themeToggle, statTotalCards, statDueToday, statMastered, statStreak, homeDomains, view-home, importDropzone, importFileInput, mergePreview, importErrors, importSuccess, confirmImport, cancelImport, mergeOnImport, importErrorList, mergeStats, mergeList, importSuccessMsg, [data-view], .view`

### `js\dashboard.js`

- **Lines:** 448
- **Functions (10):**
  - `async init()` (line 7)
  - `calculateStats(cards, sessions, streakData)` (line 67)
  - `buildOverviewCard(stats)` (line 144)
  - `buildStreakCard(stats)` (line 165)
  - `buildMasteryCard(stats)` (line 204)
  - `buildDomainChart(stats)` (line 244)
  - `buildDomainAccuracyChart(stats)` (line 298)
  - `buildWeakAreasCard(stats)` (line 356)
  - `buildRecentSessionsCard(sessions)` (line 409)
  - `Dashboard(() =>` (line 189)
- **Event Listeners:** `click`
- **DOM Queries:** `dashboardContent`

### `js\db.js`

- **Lines:** 310
- **Functions (31):**
  - `open()` (line 11)
  - `getStore(storeName, mode = 'readonly')` (line 77)
  - `put(storeName, record)` (line 82)
  - `putBatch(storeName, records)` (line 91)
  - `get(storeName, key)` (line 101)
  - `getAll(storeName)` (line 110)
  - `getAllByIndex(storeName, indexName, value)` (line 119)
  - `remove(storeName, key)` (line 129)
  - `removeBatch(storeName, keys)` (line 138)
  - `count(storeName)` (line 148)
  - `clear(storeName)` (line 157)
  - `async getAllCards()` (line 169)
  - `async getCardById(id)` (line 170)
  - `async saveCard(card)` (line 176)
  - `async saveCards(cards)` (line 181)
  - `prepareCardForStorage(card)` (line 186)
  - `async deleteCard(id)` (line 197)
  - `async getCardsByDomain(domain)` (line 198)
  - `async getCardCount()` (line 199)
  - `async getCardsDueByDate(dateStr)` (line 204)
  - `async getAllDecks()` (line 232)
  - `async saveDeck(deck)` (line 233)
  - `async deleteDeck(id)` (line 234)
  - `async getAllSessions()` (line 239)
  - `async saveSession(session)` (line 240)
  - `async getSetting(key)` (line 245)
  - `async setSetting(key, value)` (line 250)
  - `async buildTermIndex()` (line 257)
  - `async resolveRelatedCard(termStr, termIndex)` (line 268)
  - `async migrateCards()` (line 278)
  - `DB(() =>` (line 181)
- **Constants:** `DB, DB_NAME, DB_VERSION`

### `js\deckmanager.js`

- **Lines:** 94
- **Functions (2):**
  - `async init()` (line 7)
  - `DeckManager(() =>` (line 177)
- **Event Listeners:** `click`
- **DOM Queries:** `deckManagerContent, clearAllData`

### `js\exporter.js`

- **Lines:** 245
- **Functions (10):**
  - `async init()` (line 7)
  - `async updateExportInfo()` (line 57)
  - `async getFilteredCards()` (line 62)
  - `async doExport()` (line 76)
  - `exportJSON(cards, includeProgress)` (line 111)
  - `exportCSV(cards, includeProgress)` (line 139)
  - `exportPlainText(cards, includeProgress)` (line 179)
  - `csvEscape(val)` (line 222)
  - `downloadFile(content, filename, mimeType)` (line 231)
  - `Exporter(() =>` (line 175)
- **Event Listeners:** `click, change`
- **DOM Queries:** `exportContent, exportBtn, exportInfo, exportFlaggedOnly, exportIncludeProgress, input[name=`

### `js\importer.js`

- **Lines:** 203
- **Functions (7):**
  - `async processFile(content, fileName, mergeMode = true)` (line 9)
  - `async confirmImport()` (line 102)
  - `cancelImport()` (line 162)
  - `getPending()` (line 166)
  - `updateDuplicateAction(index, action)` (line 170)
  - `extractContributor(newCards, duplicates)` (line 176)
  - `Importer(() =>` (line 198)

### `js\parsers.js`

- **Lines:** 484
- **Functions (8):**
  - `parse(content, fileName)` (line 7)
  - `parseJSON(content, fileName)` (line 30)
  - `normalizeJSONItem(item, fileName)` (line 94)
  - `parseCSV(content, fileName)` (line 197)
  - `parsePlainText(content, fileName)` (line 290)
  - `matchFieldLabel(line)` (line 395)
  - `parseCSVLines(text)` (line 422)
  - `Parsers(() =>` (line 194)

### `js\popup.js`

- **Lines:** 241
- **Functions (6):**
  - `openDB()` (line 38)
  - `getAllFromStore(db, storeName)` (line 68)
  - `getSettingFromStore(db, key)` (line 78)
  - `todayStr()` (line 88)
  - `getMasteryTier(card)` (line 92)
  - `isDueToday(card)` (line 105)
- **Constants:** `DB_NAME, DB_VERSION, DOMAINS`
- **Event Listeners:** `click`
- **DOM Queries:** `popupThemeToggle, popupBody, openNewTab, openStudy, openDashboard, openNewTabFallback`

### `js\scenario.js`

- **Lines:** 287
- **Functions (9):**
  - `async init()` (line 12)
  - `async startSession()` (line 129)
  - `showCard()` (line 166)
  - `toggleFlip()` (line 220)
  - `async assessCard(quality)` (line 227)
  - `updateProgress()` (line 249)
  - `async completeSession()` (line 255)
  - `async endSession()` (line 276)
  - `ScenarioMode(() =>` (line 186)
- **Event Listeners:** `click`
- **DOM Queries:** `scenarioContent, scenarioDomainFilter, startScenarioSession, scenarioFlipContainer, endScenarioSession, newScenarioSession, scenarioComplete, scenarioSessionArea, scenarioFlipCard, scnDomainBadge, scnDomainBadgeBack, scnTerm, scnScenarioText, scnAnswer, scnExamTipSection, scnExamTip, scnRelatedSection, scnRelated, scnAttribution, scenarioProgressBar, scenarioProgressText, scenarioSummary, #scenarioContent .study-toolbar, #scenarioFlipCard .flip-card-front, #scenarioFlipCard .flip-card-back, #scenarioAssessButtons .assess-btn`

### `js\settings.js`

- **Lines:** 180
- **Functions (4):**
  - `async init()` (line 7)
  - `async loadSettings()` (line 136)
  - `async updateStorageInfo()` (line 158)
  - `Settings(() =>` (line 176)
- **Event Listeners:** `change`
- **DOM Queries:** `settingsContent, settingDarkTheme, settingCardsPerSession, settingShuffle, settingAutoFlip, settingEaseFactor, settingStorageInfo`

### `js\sm2.js`

- **Lines:** 80
- **Functions (4):**
  - `calculate(card, quality)` (line 7)
  - `createReviewEvent(quality)` (line 54)
  - `reviewCard(card, quality)` (line 62)
  - `SM2(() =>` (line 179)
- **Constants:** `SM2`

### `js\studymode.js`

- **Lines:** 452
- **Functions (12):**
  - `async init()` (line 12)
  - `async startSession()` (line 59)
  - `showCard()` (line 153)
  - `toggleFlip()` (line 255)
  - `async assessCard(quality)` (line 266)
  - `updateProgress()` (line 293)
  - `async completeSession()` (line 302)
  - `async updateStreak()` (line 353)
  - `async endSession()` (line 387)
  - `async jumpToRelatedCard(termStr)` (line 397)
  - `handleKeyboard(e)` (line 416)
  - `StudyMode(() =>` (line 189)
- **Event Listeners:** `click, keydown`
- **DOM Queries:** `studyDomainFilter, noCardsMsg, startStudySession, flipCardContainer, endSession, newSession, sessionComplete, studySession, studyTypeFilter, studyQueueFilter, flipCard, cardDomainBadge, cardTypeBadge, cardTerm, cardTags, cardScenarioText, cardDomainBadgeBack, cardAnswer, cardAlsoSeeSection, cardAlsoSee, cardExamTipSection, cardExamTip, cardRelatedSection, cardRelated, cardAttribution, studyProgressBar, studyProgressText, sessionSummary, .study-toolbar, .flip-card-front, .flip-card-back, .assess-btn`

### `js\utils.js`

- **Lines:** 260
- **Functions (15):**
  - `generateUUID()` (line 20)
  - `todayStr()` (line 34)
  - `nowISO()` (line 42)
  - `dateDiffDays(dateStrA, dateStrB)` (line 51)
  - `normalizeTerm(term)` (line 63)
  - `validateDomain(input)` (line 71)
  - `validateType(input)` (line 94)
  - `createCard(data)` (line 101)
  - `toast(message, type = 'info')` (line 173)
  - `formatDate(dateStr)` (line 184)
  - `escapeHTML(str)` (line 193)
  - `getMasteryTier(card)` (line 206)
  - `isDueToday(card)` (line 225)
  - `shuffle(arr)` (line 232)
  - `Utils(() =>` (line 174)
- **Constants:** `DOMAINS, DOMAIN_NAMES`
- **DOM Queries:** `toastContainer`

## 8. OTHER CONFIG FILES

### `data\cissp-advanced-deck.json`

- **Type:** json
- **Lines:** 643

### `data\cissp-beginner-8-domains-part-1.json`

- **Type:** json
- **Lines:** 632

### `data\cissp-starter-deck.json`

- **Type:** json
- **Lines:** 410

## 9. DETECTED PATTERNS & CONVENTIONS

- **Entry Points:** popup.html
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
