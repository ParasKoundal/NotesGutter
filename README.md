# 📓 NotesGutter

> **Don't pollute your code. Annotate it.**

**NotesGutter** is the ultimate "out-of-band" annotation tool for VS Code. Attach **rich Markdown notes** and **infinite-canvas drawings** to any line of code—without turning your source files into a comment graveyard.

![NotesGutter Preview](https://github.com/ParasKoundal/NotesGutter/raw/main/Preview.png)

---

### 📦 Install Now

| Platform | Link |
| :--- | :--- |
| **VS Code Marketplace** | [![VS Code Marketplace](https://img.shields.io/visual-studio-marketplace/v/ParasKoundal.notesgutter?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=ParasKoundal.notesgutter) |
| **Open VSX** | [![Open VSX](https://img.shields.io/open-vsx/v/ParasKoundal/notesgutter?style=for-the-badge&logo=eclipse-ide)](https://open-vsx.org/extension/ParasKoundal/notesgutter) |

---

## 🤔 The Problem

You've been there. You need to explain a complex regex or a weird hack, so you write a comment:

```javascript
// TODO: Refactor this mess.
// We are manually filtering this array because the legacy API
// returns duplicates on Tuesdays. Also, see issue #420.
// Do not touch this unless you have coffee.
// ... (20 more lines of context) ...
const users = rawData.filter(u => u.isActive && !u.isDeleted);
```

Now your file is cluttered with comments instead of code. 😩

## 💡 The Solution

With **NotesGutter**, your code stays clean:

```javascript
// @ng note api-hack-explanation
const users = rawData.filter(u => u.isActive);

// @ng draw architecture-diagram
class UserManager { ... }
```

Click the button which will appear above the comment, and a beautiful **Markdown Editor** slides open. Or click a button and draw a full architecture diagram right there. All your notes live safely in a separate folder, synced with your repo.

---

## ✨ Features

### 🗂️ Activity Bar Table of Contents (Notes Explorer)
Access all your notes, drawings, and attachments in one centralized sidebar:
- **Activity Bar Button**: Dedicated icon on the sidebar for browsing all anchors across your project or directory.
- **Directory / Project Scope Switcher**: Switch between the entire workspace, current file's directory, or any custom folder.
- **Flexible Grouping Modes**: View notes grouped by file, directory hierarchy, or as a flat list.
- **One-Click Item Actions**:
  - **Go to Code** (`$(go-to-file)`): Jump directly to the exact line in code.
  - **Open Note / Drawing** (`$(book)`): Open sidecar editor or canvas in one click.
  - **Rename Anchor** (`$(edit)`): Rename anchors with automatic link syncing.
  - **Delete Anchor** (`$(trash)`): Remove notes and clean up comments.
- **Checklist Badges & Snippet Previews**: Track task progress (e.g. `✓ 2/5`) and hover over notes for rich content previews.

### 📝 Rich Markdown Notes
Write full documentation, TODOs, or rants using a Notion-style editor. Headers, lists, code blocks—it's all there.

### ✏️ Infinite Canvas Drawings
Need to draw a flowchart? A database schema? A stick figure of your boss? Do it with specific lines of code using embedded **Excalidraw**.

### 🔗 Cross-File Magic
Link notes across your entire project. It's like a wiki for your code.

```typescript
// See the user model in another file:
// @ng note ../models/User.ts:schema-diagram
// Or use slash syntax:
// @ng note ../models/User.ts/schema-diagram
```

### ⚓ Deep Linking
Jump straight to a specific header inside any note (local or remote) using `#`.

```javascript
// Link to the "Performance" section of any note:
// @ng note architecture-doc#Performance
```

### 🎯 Multiple Notes in One Line
Want to attach a note AND a drawing to the same line? No problem.

```javascript
// @ng note logic-details @ng draw flow-diagram
function criticalProcess() { ... }
```

### 🔗 Global Attachments (`@ng attach`)
Attach any external URL or local file path to a line of code. Clicking it opens the target instantly, keeping your editor clean.

```javascript
// Link to online docs:
// @ng attach https://github.com/ParasKoundal/NotesGutter

// Link to a local file:
// @ng attach ../assets/architecture.pdf
```

### ✅ Inline To-Do Checklists
Get an instant progress summary for any note containing a checklist (`- [ ]`, `* [x]`) directly in the CodeLens.
```typescript
// [📝 refactoring-plan] (2/5)
// @ng note refactoring-plan
```

### ⚡ Zero Config
It just works. Install, click, type.

---

## 🚀 How to Use

1.  **Open Table of Contents**:
    -   Click the **NotesGutter** icon in the Activity Bar on the left side of VS Code.
    -   Use the top toolbar buttons to switch directories/projects, switch grouping, or refresh notes.
    -   Click any note to open its sidecar editor, or click the **Go to Code** button to jump directly to the code location.

2.  **Add a Note**:
    -   Place your cursor on a tricky line.
    -   Run `NotesGutter: Insert Note Anchor` (or `Cmd+Shift+M`) or manually type the comment.
    -   Start typing! ✍️

3.  **Add a Drawing**:
    -   Run `NotesGutter: Insert Draw Anchor` (or `Cmd+Shift+D`) or manually type.
    -   Unleash your inner artist! 🎨

---

## ⌨️ Commands & Shortcuts

| Command | Shortcut (macOS) | Shortcut (Windows/Linux) | Description |
| :--- | :--- | :--- | :--- |
| `NotesGutter: Insert Note Anchor` | `Cmd+Shift+M` | `Ctrl+Shift+M` | Insert a new Markdown note anchor at current line |
| `NotesGutter: Insert Draw Anchor` | `Cmd+Shift+D` | `Ctrl+Shift+D` | Insert a new infinite-canvas drawing anchor |
| `NotesGutter: Insert Attach Anchor` | `Cmd+Shift+A` | `Ctrl+Shift+A` | Attach a URL or local file to current line |
| `NotesGutter: Switch Directory or Project Scope` | — | — | Switch TOC scope (Workspace, Current Folder, Custom) |
| `NotesGutter: Change Grouping Mode` | — | — | Toggle TOC grouping (By File, By Directory, Flat) |
| `NotesGutter: Refresh Notes` | — | — | Force re-scan of all notes in the active scope |
| `NotesGutter: Rename Anchor` | — | — | Rename anchor and update linked storage |
| `NotesGutter: Prune Orphaned Notes` | — | — | Clean up unused note files in `.notesgutter/` |

---

## 🔒 Privacy & Storage

We believe **your data is yours**.
-   Notes are stored in a `.notesgutter` folder in your project.
-   It works **100% offline**.
-   Commits to Git just like any other file.

## ❤️ Contribute

Found a bug? Have a wild idea? [Open an issue](https://github.com/ParasKoundal/NotesGutter/issues)!

---

*Made with ☕ by [Paras Koundal](https://github.com/ParasKoundal)*
