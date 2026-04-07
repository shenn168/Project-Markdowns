# CodeLens: tara-feasibility-tracker-2

> Auto-generated codebase documentation optimized for LLM context.
> Paste into an AI chat to enable codebase-aware assistance.

## 1. PROJECT OVERVIEW

- **Project:** tara-feasibility-tracker-2
- **Files Analyzed:** 8
- **Total Lines:** 1,928
- **JS Files:** 3
- **HTML Files:** 1
- **CSS Files:** 1
- **Browser Extension:** Yes (Manifest V3)
- **Entry Points:** background.js, popup.js, popup.html

## 2. FILE STRUCTURE

```
background.js (58 lines)
data\historical_tara_baseline.json (1 lines)
data\living_tara_updates.json (9 lines)
lib\threat-matcher.js (251 lines)
manifest.json (33 lines)
popup.css (601 lines)
popup.html (239 lines)
popup.js (736 lines)
```

## 4. BROWSER EXTENSION MANIFEST

### `manifest.json`

- **Manifest Version:** 3
- **Name:** TARA Feasibility Tracker
- **Version:** 1.0.0
- **Description:** UNR155 TARA Attack Feasibility monitoring and recalibration tool
- **Permissions:** `storage, alarms, notifications`
- **Host Permissions:** `https://services.nvd.nist.gov/*, https://cve.circl.lu/*, https://api.github.com/*, https://otx.alienvault.com/*`
- **Service Worker:** `background.js`
- **Popup:** `popup.html`
- **Icons:** `{'16': 'icons/icon16.png', '48': 'icons/icon48.png', '128': 'icons/icon128.png'}`
- **All Referenced Files:**
  - `background.js`
  - `icons/icon128.png`
  - `icons/icon16.png`
  - `icons/icon48.png`
  - `popup.html`

## 5. HTML FILES

### `popup.html`

- **Lines:** 239
- **Title:** TARA Feasibility Tracker
- **Stylesheets:** `popup.css`
- **Scripts (2):**
  - `lib/threat-matcher.js`
  - `popup.js`
- **Semantic Tags:** <header> x1, <nav> x1, <section> x4, <footer> x1
- **IDs (41):** `div#statusBar, section#dashboard, span#criticalCount, span#mediumCount, span#lowCount, span#totalCount, p#lastScanTime, p#pendingUpdates, button#quickScanBtn, section#scan, input#srcNvd, input#srcGithub, input#srcOtx, input#srcAutoIsac, input#srcAcademic, div#keywordTags, input#newKeyword, button#addKeywordBtn, button#runScanBtn, div#scanProgress`
- **CSS Classes (51):** `container, header, logo, logo-icon, version, status-bar, status-indicator, online, status-text, tabs, tab-btn, active, tab-content, stats-grid, stat-card, critical, stat-value, stat-label, medium, low, total, info-card, btn, btn-primary, btn-full, source-selector, checkbox-item, checkmark, source-info, keyword-section`

## 6. CSS FILES

### `popup.css`

- **Lines:** 601
- **Total Rules:** 95
- **CSS Variables (16):** `--primary, --primary-dark, --danger, --warning, --success, --critical, --high, --medium, --low, --very-low, --bg-dark, --bg-card, --bg-hover, --text-primary, --text-secondary, --border`
- **Animations:** `pulse`
- **Selectors (95):**
  - `:root` (16 props: --primary, --primary-dark, --danger, --warning, --success)
  - `*` (3 props: margin, padding, box-sizing)
  - `body` (7 props: width, min-height, max-height, overflow-y, font-family)
  - `.container` (1 props: padding)
  - `.header` (6 props: display, justify-content, align-items, margin-bottom, padding-bottom)
  - `.logo` (3 props: display, align-items, gap)
  - `.logo-icon` (1 props: font-size)
  - `.logo h1` (2 props: font-size, font-weight)
  - `.version` (5 props: font-size, color, background, padding, border-radius)
  - `.status-bar` (8 props: display, align-items, gap, padding, background)
  - `.status-indicator` (4 props: width, height, border-radius, background)
  - `.status-indicator.online` (1 props: background)
  - `.status-indicator.scanning` (2 props: background, animation)
  - `50%` (1 props: opacity)
  - `}


.tabs` (6 props: display, gap, margin-bottom, background, padding)
  - `.tab-btn` (10 props: flex, padding, border, background, color)
  - `.tab-btn:hover` (2 props: background, color)
  - `.tab-btn.active` (2 props: background, color)
  - `.tab-content` (1 props: display)
  - `.tab-content.active` (1 props: display)
  - `.stats-grid` (4 props: display, grid-template-columns, gap, margin-bottom)
  - `.stat-card` (5 props: background, padding, border-radius, text-align, border-left)
  - `.stat-card.critical` (1 props: border-left-color)
  - `.stat-card.medium` (1 props: border-left-color)
  - `.stat-card.low` (1 props: border-left-color)
  - `.stat-card.total` (1 props: border-left-color)
  - `.stat-value` (3 props: display, font-size, font-weight)
  - `.stat-label` (4 props: font-size, color, text-transform, letter-spacing)
  - `.info-card` (4 props: background, padding, border-radius, margin-bottom)
  - `.info-card h3` (2 props: font-size, margin-bottom)
  - `.info-card p` (2 props: font-size, color)
  - `.btn` (7 props: padding, border, border-radius, font-size, font-weight)
  - `.btn-primary` (2 props: background, color)
  - `.btn-primary:hover` (1 props: background)
  - `.btn-secondary` (3 props: background, color, border)
  - `.btn-secondary:hover` (1 props: background)
  - `.btn-danger` (2 props: background, color)
  - `.btn-small` (2 props: padding, font-size)
  - `.btn-full` (2 props: width, margin-top)
  - `.source-selector` (1 props: margin-bottom)
  - ... and 55 more

## 7. JAVASCRIPT FILES

### `background.js`

- **Lines:** 58
- **Entry Point:** Yes ⭐
- **Functions (1):**
  - `async fetchNvdData(keywords)` (line 43)
- **Event Listeners:** `chrome.runtime.onMessage, chrome.runtime.onInstalled`

### `lib\threat-matcher.js`

- **Lines:** 251
- **Exports (1):**
  - `module.exports = ThreatMatcher;`
- **Functions (1):**
  - `matchThreatsToTara(threats, taraData)` (line 191)

### `popup.js`

- **Lines:** 736
- **Entry Point:** Yes ⭐
- **Functions (28):**
  - `async initializeApp()` (line 23)
  - `async loadSavedState()` (line 43)
  - `async saveState()` (line 69)
  - `attachEventListeners()` (line 85)
  - `switchTab(tabId)` (line 125)
  - `updateDashboardStats()` (line 137)
  - `getMergedTaraData()` (line 160)
  - `renderKeywordTags()` (line 179)
  - `addKeyword()` (line 193)
  - `removeKeyword(keyword)` (line 209)
  - `async runQuickScan()` (line 218)
  - `async runFullScan()` (line 245)
  - `async fetchNvdThreats()` (line 337)
  - `async fetchGithubThreats()` (line 376)
  - `async fetchOtxThreats()` (line 406)
  - `generateAutoIsacAlerts()` (line 434)
  - `generateAcademicThreats()` (line 462)
  - `generateMockThreats(count)` (line 488)
  - `renderRecommendations()` (line 522)
  - `filterUpdates()` (line 569)
  - `applySelectedUpdates()` (line 598)
  - `exportUpdates()` (line 647)
  - `clearLivingUpdates()` (line 660)
  - `handleImport(event)` (line 672)
  - `showJsonViewer(title, data)` (line 701)
  - `downloadJson(filename, data)` (line 710)
  - `setStatus(state, text)` (line 723)
  - `simulateDelay(ms)` (line 734)
- **Constants:** `HISTORICAL_TARA_DATA`
- **Event Listeners:** `DOMContentLoaded, click, keypress, change`
- **DOM Queries:** `lastScanTime, pendingUpdates, quickScanBtn, runScanBtn, addKeywordBtn, newKeyword, severityFilter, systemFilter, exportUpdatesBtn, applyUpdatesBtn, viewBaselineBtn, exportBaselineBtn, viewLivingBtn, exportLivingBtn, clearLivingBtn, importBtn, importFile, closeViewerBtn, jsonViewer, criticalCount, mediumCount, lowCount, totalCount, livingDataInfo, keywordTags, srcNvd, srcGithub, srcOtx, srcAutoIsac, srcAcademic, scanProgress, progressFill, progressText, updatesList, jsonViewerTitle, jsonContent, .status-indicator, .status-text, .tab-btn, .tab-content, .update-item, .update-checkbox:checked`

## 8. OTHER CONFIG FILES

### `data\historical_tara_baseline.json`

- **Type:** json
- **Lines:** 1
- **Keys:** `tara`

### `data\living_tara_updates.json`

- **Type:** json
- **Lines:** 9
- **Keys:** `schemaVersion, createdDate, updates, metadata`

## 9. DETECTED PATTERNS & CONVENTIONS

- **Architecture:** Standard src/lib layout
- **Naming:** kebab-case
- **Entry Points:** background.js, popup.js, popup.html
- **Other Patterns:**
  - Browser Extension (Manifest V3)
  - Background service worker: background.js
  - Permissions: storage, alarms, notifications

## 10. HOW TO USE THIS DOCUMENT WITH AN LLM

1. This document describes the **complete structure** of the codebase.
2. To modify a file, ask the LLM and reference the file path from this doc.
3. The LLM can see all classes, functions, DOM queries, and event listeners.
4. For browser extensions, the manifest section shows the full extension wiring.
5. For deeper context, paste the actual source code of the specific file you want to change.
6. The dependency/import map shows how files connect to each other.

**Tip:** Start your prompt with:
> "Given the codebase documented above, help me [your task]."
