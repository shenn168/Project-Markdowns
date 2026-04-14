# CodeLens: remedy-safety-journal

> Auto-generated codebase documentation optimized for LLM context.
> Paste into an AI chat to enable codebase-aware assistance.

## 1. PROJECT OVERVIEW

- **Project:** remedy-safety-journal
- **Files Analyzed:** 10
- **Total Lines:** 1,608
- **JS Files:** 4
- **HTML Files:** 2
- **CSS Files:** 1
- **Browser Extension:** Yes (Manifest V3)
- **Frameworks:** Express.js
- **Entry Points:** extension\background.js

## 2. FILE STRUCTURE

```
extension\background.js (3 lines)
extension\manifest.json (14 lines)
extension\popup.html (41 lines)
extension\popup.js (87 lines)
package-lock.json (854 lines)
package.json (13 lines)
public\app.js (168 lines)
public\index.html (53 lines)
public\styles.css (103 lines)
server.js (272 lines)
```

## 3. DEPENDENCIES

- **name:** remedy-safety-journal-v0-1-0
- **version:** 0.1.0
- **description:** Prototype for Remedy Safety Journal
- **main:** server.js
- **Dependencies (2):**
  - `cors@^2.8.5`
  - `express@^4.19.2`
- **Scripts:**
  - `start`: `node server.js`

## 4. BROWSER EXTENSION MANIFEST

### `extension\manifest.json`

- **Manifest Version:** 3
- **Name:** Remedy Safety Journal
- **Version:** 0.1.0
- **Description:** Save remedy posts and videos and compare against your meds.
- **Permissions:** `activeTab, storage, scripting`
- **Host Permissions:** `http://localhost:3000/*, https://x.com/*, https://www.youtube.com/*`
- **Service Worker:** `background.js`
- **Popup:** `popup.html`
- **All Referenced Files:**
  - `background.js`
  - `popup.html`

## 5. HTML FILES

### `extension\popup.html`

- **Lines:** 41
- **Title:** Save Remedy
- **Scripts (1):**
  - `popup.js`
- **Inline `<style>` blocks:** 1
- **IDs (6):** `input#title, input#creator, textarea#snippet, textarea#note, button#saveBtn, div#message`
- **CSS Classes (1):** `message`

### `public\index.html`

- **Lines:** 53
- **Title:** Remedy Safety Journal
- **Stylesheets:** `/styles.css`
- **Scripts (1):**
  - `/app.js`
- **Semantic Tags:** <section> x2
- **IDs (6):** `textarea#prescriptions, textarea#otc, textarea#supplements, button#saveProfile, div#profileMessage, div#remedies`
- **CSS Classes (6):** `container, sub, card, grid, flag, message`

## 6. CSS FILES

### `public\styles.css`

- **Lines:** 103
- **Total Rules:** 19
- **Selectors (19):**
  - `body` (5 props: font-family, background, color, margin, padding)
  - `.container` (3 props: max-width, margin, padding)
  - `h1, h2, h3` (1 props: margin-top)
  - `.sub` (1 props: color)
  - `.card` (5 props: background, border-radius, padding, margin-bottom, box-shadow)
  - `.grid` (3 props: display, grid-template-columns, gap)
  - `textarea, input, select` (6 props: width, box-sizing, padding, margin-top, border)
  - `label` (2 props: display, margin-bottom)
  - `button` (8 props: background, color, border, border-radius, padding)
  - `button.secondary` (1 props: background)
  - `.message` (2 props: margin-top, color)
  - `.remedy` (4 props: border, border-radius, padding, margin-bottom)
  - `.tags` (4 props: display, flex-wrap, gap, margin)
  - `.tag` (5 props: background, color, border-radius, padding, font-size)
  - `.risk-red` (1 props: color)
  - `.risk-yellow` (1 props: color)
  - `.risk-gray` (1 props: color)
  - `.risk-green` (1 props: color)
  - `.row` (4 props: display, gap, flex-wrap, margin-top)

## 7. JAVASCRIPT FILES

### `extension\background.js`

- **Lines:** 3
- **Entry Point:** Yes ⭐
- **Event Listeners:** `chrome.runtime.onInstalled`

### `extension\popup.js`

- **Lines:** 87
- **Functions (5):**
  - `async getCurrentTab()` (line 1)
  - `detectPlatform(url)` (line 6)
  - `async saveOfflineQueue(payload)` (line 13)
  - `async flushOfflineQueue()` (line 20)
  - `async init()` (line 44)
- **Event Listeners:** `click`
- **DOM Queries:** `title, saveBtn, creator, snippet, note, message`

### `public\app.js`

- **Lines:** 168
- **Functions (11):**
  - `parseLines(text)` (line 1)
  - `async loadProfile()` (line 12)
  - `async saveProfile()` (line 33)
  - `renderRisk(result)` (line 49)
  - `renderObservationForm(remedy)` (line 58)
  - `renderTrialForm(remedy)` (line 72)
  - `renderStatusButtons(remedy)` (line 85)
  - `async loadRemedies()` (line 92)
  - `async updateStatus(id, status)` (line 128)
  - `async saveTrial(id)` (line 137)
  - `async saveObservation(id)` (line 152)
- **Event Listeners:** `click`
- **DOM Queries:** `prescriptions, otc, supplements, profileMessage, remedies, saveProfile, .flag, .flag:checked`

### `server.js`

- **Lines:** 272
- **Imports (3):**
  - `const express = require("express");`
  - `const cors = require("cors");`
  - `const path = require("path");`
- **Functions (4):**
  - `normalizeText(value)` (line 35)
  - `parseRemedies(text)` (line 39)
  - `getAllProfileItems()` (line 44)
  - `checkRisks(remedyNames)` (line 52)
- **Constants:** `PORT, KNOWN_REMEDIES`

## 8. OTHER CONFIG FILES

### `package-lock.json`

- **Type:** json
- **Lines:** 854
- **Keys:** `name, version, lockfileVersion, requires, packages`

## 9. DETECTED PATTERNS & CONVENTIONS

- **Frameworks:** Express.js
- **Entry Points:** extension\background.js
- **Other Patterns:**
  - Browser Extension (Manifest V3)
  - Background service worker: background.js
  - Permissions: activeTab, storage, scripting

## 10. HOW TO USE THIS DOCUMENT WITH AN LLM

1. This document describes the **complete structure** of the codebase.
2. To modify a file, ask the LLM and reference the file path from this doc.
3. The LLM can see all classes, functions, DOM queries, and event listeners.
4. For browser extensions, the manifest section shows the full extension wiring.
5. For deeper context, paste the actual source code of the specific file you want to change.
6. The dependency/import map shows how files connect to each other.

**Tip:** Start your prompt with:
> "Given the codebase documented above, help me [your task]."
