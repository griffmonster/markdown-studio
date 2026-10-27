# 🥾 Griffmonster Walks — Pipeline Markdown Studio

An authoring environment designed specifically for writing, validating, and preparing walk route content for the **[Griffmonster Walks](https://griffmonster-walks.blogspot.com/)** ecosystem and publishing pipeline.

This single-file web application provides a real-time side-by-side Markdown editor, schema validation engine, and local draft recovery to streamline route documentation before it is pushed through the automated Saxon XSLT build pipeline.

---

## 🚀 Key Features

* **Strict Schema Validation:** Pre-flight checks (`Run XSLT Pre-Check`) enforce allowable top-level section headers (`#`) and prevent duplicate header IDs to guarantee clean XML transformations downstream.
* **Auto-Save & Local Recovery:** Automatically backs up active work to browser storage on every keystroke, preventing data loss during session disconnects or accidental browser closes.
* **Built-in Walk Template & Snippets:** Includes the standard walk route schema as a default template, along with quick-insert dropdown snippets for standard sections (Directions, Pubs, Features, Validation, etc.).
* **Independent Pane Scrolling:** The editor and preview panes feature separate physical scrolling for maximum visual precision when working with large image embeds and long walk descriptions.
* **Toolbar Helpers:** Instant formatting buttons for bold, italic, inline quotes, blockquotes, lists, links, images, and section snippets.

---

## 📋 Standard Walk Schema Rules

To ensure compatibility with the blog processing scripts and eBook/PDF build pipelines, all walk documents must strictly adhere to the following top-level section whitelist:

| Section Header | Purpose & Sub-structure |
| :--- | :--- |
| `# Description` | Summary of the route, key highlights, and overview text. |
| `# Directions` | Step-by-step turn guidance (usually numbered lists). |
| `# Notes` | Background info, access notes, or `## References`. |
| `# Pubs` | Details on food/drink stops (`## Pub Name, Place name`, address, website). |
| `# Features` | Points of interest along the route (`## Feature Name`). |
| `# Updates` | Revision history and path updates. |
| `# Images` | High-resolution photo embeds and map screenshots. |
| `# Validation` | Verification logs (`## YYYY-MM-DD`, weather, walk duration, validator notes). |

> **Note:** Top-level headings (`#`) outside this whitelist will trigger a validation error during pre-flight checks.

---

## 💻 Authoring Workflow

1. **Start a Draft:**
   - Click **`New`** to begin a blank walk draft.
   - Click **`Load Template`** to populate the editor with the standardized Griffmonster Walks route template.
   - Click **`Open Existing...`** to import a previously saved `.md` file from your computer.

2. **Compose Content:**
   - Use the formatting toolbar or shortcut keys to add inline formatting, blockquotes, and lists.
   - Use the **`+ Insert Template Section...`** dropdown to append pre-formatted sections.

3. **Validate:**
   - Click **`Run
