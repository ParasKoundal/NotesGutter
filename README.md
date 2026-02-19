# 📓 NotesGutter

> **Don't pollute your code. Annotate it.**

**NotesGutter** is the ultimate "out-of-band" annotation tool for VS Code. Attach **rich Markdown notes** and **infinite-canvas drawings** to any line of code—without turning your source files into a comment graveyard.

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

Now your file is cluttered with comments instead of code. 😫

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

### ⚡ Zero Config
It just works. Install, click, type.

---

## 🚀 How to Use

1.  **Add a Note**:
    -   Place your cursor on a tricky line.
    -   Run `NotesGutter: Insert Note Anchor` (or `Cmd+Shift+M`) or manually type the command.
    -   Start typing! ✍️

2.  **Add a Drawing**:
    -   Run `NotesGutter: Insert Draw Anchor` or manually type.
    -   Unleash your inner artist! 🎨

## 🔒 Privacy & Storage

We believe **your data is yours**.
-   Notes are stored in a `.notesgutter` folder in your project.
-   It works **100% offline**.
-   Commits to Git just like any other file.

## ❤️ Contribute

Found a bug? Have a wild idea? [Open an issue](https://github.com/ParasKoundal/NotesGutter/issues)!

---

*Made with ☕ by [Paras Koundal](https://github.com/ParasKoundal)*

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow.svg)](https://buymeacoffee.com/paraskoundal)
