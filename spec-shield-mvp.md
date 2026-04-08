# CodeLens: SpecShield-MVP

> Auto-generated codebase documentation optimized for LLM context.
> Paste into an AI chat to enable codebase-aware assistance.

## 1. PROJECT OVERVIEW

- **Project:** SpecShield-MVP
- **Files Analyzed:** 4
- **Total Lines:** 275
- **JS Files:** 2
- **HTML Files:** 1
- **CSS Files:** 0
- **Browser Extension:** Yes (Manifest V3)
- **Entry Points:** content.js, popup.js, popup.html

## 2. FILE STRUCTURE

```
content.js (6 lines)
manifest.json (13 lines)
popup.html (31 lines)
popup.js (225 lines)
```

## 4. BROWSER EXTENSION MANIFEST

### `manifest.json`

- **Manifest Version:** 3
- **Name:** SpecShield 24MM Assessor
- **Version:** 1.0
- **Description:** Analyzes webpages for threats and checks 24MM mitigation status.
- **Permissions:** `activeTab, scripting`
- **Popup:** `popup.html`
- **All Referenced Files:**
  - `popup.html`

## 5. HTML FILES

### `popup.html`

- **Lines:** 31
- **Title:** SpecShield 24MM
- **Scripts (2):**
  - `https://cdn.tailwindcss.com`
  - `popup.js`
- **Inline `<style>` blocks:** 1
- **IDs (3):** `button#scanBtn, div#results, div#assessmentContent`
- **CSS Classes (34):** `bg-gray-50, text-gray-800, p-4, flex, items-center, mb-4, w-8, h-8, bg-red-600, text-white, rounded, justify-center, font-bold, text-xl, mr-2, text-lg, text-gray-900, text-sm, text-gray-600, w-full, hover:bg-red-700, font-semibold, py-2, px-4, shadow, transition, duration-200, mt-4, hidden, text-md`

## 7. JAVASCRIPT FILES

### `content.js`

- **Lines:** 6
- **Functions (1):**
  - `getPageText()` (line 2)

### `popup.js`

- **Lines:** 225
- **Functions (1):**
  - `analyzeTextFast(text)` (line 182)
- **Event Listeners:** `click`
- **DOM Queries:** `scanBtn, results, assessmentContent`

## 9. DETECTED PATTERNS & CONVENTIONS

- **Entry Points:** content.js, popup.js, popup.html
- **Other Patterns:**
  - Browser Extension (Manifest V3)
  - Permissions: activeTab, scripting

## 10. HOW TO USE THIS DOCUMENT WITH AN LLM

1. This document describes the **complete structure** of the codebase.
2. To modify a file, ask the LLM and reference the file path from this doc.
3. The LLM can see all classes, functions, DOM queries, and event listeners.
4. For browser extensions, the manifest section shows the full extension wiring.
5. For deeper context, paste the actual source code of the specific file you want to change.
6. The dependency/import map shows how files connect to each other.

**Tip:** Start your prompt with:
> "Given the codebase documented above, help me [your task]."
