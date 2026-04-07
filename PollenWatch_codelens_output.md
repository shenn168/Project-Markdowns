# CodeLens: PollenWatch

> Auto-generated codebase documentation optimized for LLM context.
> Paste into an AI chat to enable codebase-aware assistance.

## 1. PROJECT OVERVIEW

- **Project:** PollenWatch
- **Files Analyzed:** 9
- **Total Lines:** 1,531
- **JS Files:** 4
- **HTML Files:** 2
- **CSS Files:** 2
- **Browser Extension:** Yes (Manifest V3)
- **Entry Points:** background.js, popup.js, sidebar.js, popup.html

## 2. FILE STRUCTURE

```
background.js (164 lines)
manifest.json (35 lines)
popup.css (165 lines)
popup.html (69 lines)
popup.js (317 lines)
sidebar.css (95 lines)
sidebar.html (36 lines)
sidebar.js (140 lines)
utils.js (510 lines)
```

## 4. BROWSER EXTENSION MANIFEST

### `manifest.json`

- **Manifest Version:** 3
- **Name:** PollenWatch
- **Version:** 1.0.0
- **Description:** Free pollen, mold & allergen counts and forecasts by zip code.
- **Permissions:** `storage, alarms`
- **Host Permissions:** `https://api.open-meteo.com/*, https://api.zippopotam.us/*, https://www.pollen.com/*, https://api.ambeedata.com/*`
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

- **Lines:** 69
- **Title:** PollenWatch
- **Stylesheets:** `popup.css`
- **Scripts (2):**
  - `utils.js`
  - `popup.js`
- **Semantic Tags:** <header> x1
- **IDs (24):** `div#app, header#header, button#btn-settings, div#location-bar, select#location-select, button#btn-refresh, div#loading, div#error, p#error-msg, div#current, div#overall-banner, div#cards-grid, div#triggers-section, div#triggers-list, div#weather-info, button#btn-forecast, div#settings, div#zip-list, input#input-zip, button#btn-add-zip`
- **CSS Classes (10):** `header-left, logo, hidden, spinner, section-title, btn-primary, add-zip-row, btn-small, btn-secondary, first-run-icon`

### `sidebar.html`

- **Lines:** 36
- **Title:** PollenWatch - Forecast
- **Stylesheets:** `sidebar.css`
- **Scripts (2):**
  - `utils.js`
  - `sidebar.js`
- **Semantic Tags:** <header> x1
- **IDs (6):** `div#sidebar-app, div#sidebar-location, div#sidebar-loading, div#sidebar-error, div#forecast-container, div#legend`
- **CSS Classes (5):** `logo, hidden, spinner, legend-title, legend-items`

## 6. CSS FILES

### `popup.css`

- **Lines:** 165
- **Total Rules:** 68
- **Animations:** `spin`
- **Selectors (68):**
  - `*` (3 props: margin, padding, box-sizing)
  - `body` (8 props: width, min-height, max-height, overflow-y, font-family)
  - `body::-webkit-scrollbar` (1 props: width)
  - `body::-webkit-scrollbar-track` (1 props: background)
  - `body::-webkit-scrollbar-thumb` (2 props: background, border-radius)
  - `#app` (1 props: padding)
  - `#header` (4 props: display, align-items, justify-content, margin-bottom)
  - `.header-left` (3 props: display, align-items, gap)
  - `.logo` (1 props: font-size)
  - `#header h1` (3 props: font-size, font-weight, color)
  - `#btn-settings` (7 props: background, border, font-size, cursor, padding)
  - `#btn-settings:hover` (1 props: background)
  - `#location-bar` (3 props: display, gap, margin-bottom)
  - `#location-select` (9 props: flex, padding, border-radius, border, background)
  - `#location-select:focus` (1 props: border-color)
  - `#btn-refresh` (7 props: background, border, border-radius, padding, cursor)
  - `#btn-refresh:hover` (1 props: background)
  - `.section-title` (7 props: font-size, font-weight, text-transform, letter-spacing, color)
  - `#overall-banner` (4 props: border-radius, padding, margin-bottom, text-align)
  - `.banner-index` (2 props: font-size, font-weight)
  - `.banner-label` (3 props: font-size, font-weight, margin-top)
  - `.banner-scale` (3 props: font-size, color, margin-top)
  - `#cards-grid` (4 props: display, grid-template-columns, gap, margin-bottom)
  - `.pollen-card` (5 props: background, border-radius, padding, border-left, transition)
  - `.pollen-card:hover` (1 props: transform)
  - `.card-header` (4 props: display, justify-content, align-items, margin-bottom)
  - `.card-type` (5 props: font-size, font-weight, text-transform, letter-spacing, color)
  - `.card-emoji` (1 props: font-size)
  - `.card-value` (3 props: font-size, font-weight, margin-bottom)
  - `.card-label` (2 props: font-size, color)
  - `.card-bar` (5 props: height, border-radius, background, margin-top, overflow)
  - `.card-bar-fill` (3 props: height, border-radius, transition)
  - `#triggers-list` (4 props: display, flex-wrap, gap, margin-bottom)
  - `.trigger-tag` (7 props: display, padding, border-radius, font-size, font-weight)
  - `.trigger-tag.tree` (2 props: border-color, color)
  - `.trigger-tag.grass` (2 props: border-color, color)
  - `.trigger-tag.weed` (2 props: border-color, color)
  - `.trigger-tag.mold` (2 props: border-color, color)
  - `#weather-info` (10 props: background, border-radius, padding, margin-bottom, font-size)
  - `.weather-item` (1 props: text-align)
  - ... and 28 more

### `sidebar.css`

- **Lines:** 95
- **Total Rules:** 36
- **Animations:** `spin`
- **Selectors (36):**
  - `*` (3 props: margin, padding, box-sizing)
  - `body` (7 props: font-family, background, color, font-size, padding)
  - `body::-webkit-scrollbar` (1 props: width)
  - `body::-webkit-scrollbar-track` (1 props: background)
  - `body::-webkit-scrollbar-thumb` (2 props: background, border-radius)
  - `header` (4 props: display, align-items, gap, margin-bottom)
  - `.logo` (1 props: font-size)
  - `header h1` (3 props: font-size, font-weight, color)
  - `#sidebar-location` (3 props: font-size, color, margin-bottom)
  - `.forecast-day` (4 props: background, border-radius, padding, margin-bottom)
  - `.forecast-day.today` (1 props: border)
  - `.day-header` (4 props: display, justify-content, align-items, margin-bottom)
  - `.day-date` (2 props: font-weight, font-size)
  - `.day-date .today-badge` (9 props: display, background, color, font-size, font-weight)
  - `.day-overall-score` (2 props: font-size, font-weight)
  - `.day-allergens` (4 props: display, grid-template-columns, gap, margin-bottom)
  - `.allergen-chip` (7 props: display, flex-direction, align-items, background, border-radius)
  - `.chip-icon` (2 props: font-size, margin-bottom)
  - `.chip-label` (5 props: font-size, color, text-transform, letter-spacing, margin-bottom)
  - `.chip-value` (2 props: font-size, font-weight)
  - `.chip-severity` (2 props: font-size, margin-top)
  - `.chip-bar` (6 props: width, height, background, border-radius, margin-top)
  - `.chip-bar-fill` (2 props: height, border-radius)
  - `.day-triggers` (4 props: display, flex-wrap, gap, margin-bottom)
  - `.trigger-tag` (7 props: display, padding, border-radius, font-size, font-weight)
  - `.trigger-tag.tree` (2 props: border-color, color)
  - `.trigger-tag.grass` (2 props: border-color, color)
  - `.trigger-tag.weed` (2 props: border-color, color)
  - `.trigger-tag.mold` (2 props: border-color, color)
  - `.day-weather` (3 props: font-size, color, margin-top)
  - `#legend` (4 props: margin-top, padding, background, border-radius)
  - `.legend-title` (6 props: font-size, font-weight, text-transform, letter-spacing, color)
  - `.legend-items` (4 props: display, flex-wrap, gap, font-size)
  - `.spinner` (7 props: width, height, border, border-top-color, border-radius)
  - `}
#sidebar-loading p` (2 props: text-align, color)
  - `.hidden` (1 props: display)

## 7. JAVASCRIPT FILES

### `background.js`

- **Lines:** 164
- **Entry Point:** Yes ⭐
- **Functions (5):**
  - `async refreshData()` (line 17)
  - `estimatePollenFromWeatherBg(daily)` (line 71)
  - `estimateBgIndex(type, temp, rain, wind, humidity, uv)` (line 120)
  - `estimateBgMold(temp, rain, humidity)` (line 145)
  - `getCategoryNameBg(index)` (line 157)
- **Event Listeners:** `chrome.runtime.onInstalled`

### `popup.js`

- **Lines:** 317
- **Entry Point:** Yes ⭐
- **Functions (17):**
  - `async init()` (line 17)
  - `showView(view)` (line 47)
  - `populateSelect()` (line 57)
  - `onLocationChange()` (line 70)
  - `async addZipFirst()` (line 76)
  - `async addZipFromSettings()` (line 80)
  - `async addZip(inputEl)` (line 86)
  - `showError(msg)` (line 115)
  - `async loadData()` (line 124)
  - `renderCurrentView(pollenData)` (line 153)
  - `updateBadge(today)` (line 245)
  - `openSettings()` (line 256)
  - `closeSettings()` (line 258)
  - `renderZipList()` (line 263)
  - `async handleDelete(e)` (line 285)
  - `async openSidebar()` (line 299)
  - `openFallback()` (line 312)
- **Event Listeners:** `DOMContentLoaded, click, change, keydown`
- **DOM Queries:** `btn-settings, btn-back, btn-refresh, btn-add-zip, btn-add-first, btn-forecast, location-select, input-zip-first, input-zip, location-bar, error-msg, overall-banner, cards-grid, triggers-section, triggers-list, weather-info, zip-list`

### `sidebar.js`

- **Lines:** 140
- **Entry Point:** Yes ⭐
- **Functions (1):**
  - `async loadForecast()` (line 14)
- **Event Listeners:** `DOMContentLoaded`
- **DOM Queries:** `sidebar-loading, forecast-container, sidebar-location, sidebar-error`

### `utils.js`

- **Lines:** 510
- **Functions (18):**
  - `getSeverityFromIndex(value)` (line 15)
  - `zipToCoords(zip)` (line 26)
  - `fetchPollenComCurrent(zip)` (line 55)
  - `fetchPollenComForecast(zip)` (line 60)
  - `fetchPollenComEndpoint(url)` (line 65)
  - `fetchTomorrowPollen(lat, lon)` (line 88)
  - `fetchAmbeePollen(lat, lon)` (line 110)
  - `fetchAllPollenData(zip, lat, lon)` (line 132)
  - `parsePollenComData(currentResp, forecastResp)` (line 157)
  - `getCategoryName(index)` (line 223)
  - `fetchWeatherBasedEstimate(lat, lon)` (line 238)
  - `estimatePollenFromWeather(daily)` (line 262)
  - `estimateCategoryIndex(type, temp, rain, wind, humidity, uv)` (line 326)
  - `estimateMoldIndex(temp, rain, humidity)` (line 408)
  - `buildWeatherTriggers(treeIdx, grassIdx, weedIdx, moldIdx, temp)` (line 442)
  - `getEmptyResult()` (line 475)
  - `formatDate(dateStr)` (line 483)
  - `isToday(dateStr)` (line 501)

## 9. DETECTED PATTERNS & CONVENTIONS

- **Entry Points:** background.js, popup.js, sidebar.js, popup.html
- **Other Patterns:**
  - Browser Extension (Manifest V3)
  - Background service worker: background.js
  - Permissions: storage, alarms

## 10. HOW TO USE THIS DOCUMENT WITH AN LLM

1. This document describes the **complete structure** of the codebase.
2. To modify a file, ask the LLM and reference the file path from this doc.
3. The LLM can see all classes, functions, DOM queries, and event listeners.
4. For browser extensions, the manifest section shows the full extension wiring.
5. For deeper context, paste the actual source code of the specific file you want to change.
6. The dependency/import map shows how files connect to each other.

**Tip:** Start your prompt with:
> "Given the codebase documented above, help me [your task]."
