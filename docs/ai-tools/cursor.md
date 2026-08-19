# Cursor — Your AI Coding Partner

Cursor is VS Code with AI built in. You'll use it most for this project.

## Three ways to ask for help

| Mode | When to use | How |
|------|-------------|-----|
| **Chat** | Questions, planning, multi-file changes | `Ctrl+L` (Windows) |
| **Inline edit** | Change selected code | Select code → `Ctrl+K` |
| **Agent** | "Build this feature for me" | Chat → Agent mode |

## Your first prompts (copy and adapt)

```
I'm 14 and learning web development. Explain what index.html does in
simple terms. Use short paragraphs.
```

```
Look at sites/[my-name]/index.html. Add a navigation bar with links to
Home, About, and Journal. Match the existing color scheme.
```

```
I changed the CSS but my page looks broken on mobile. Help me fix it
step by step and explain each change.
```

## Good prompt habits

1. **Say who you are** — "I'm learning" gets better explanations.
2. **Point to files** — `@index.html` or drag files into chat.
3. **One task at a time** — "Add nav" then "Style nav" not both at once.
4. **Ask why** — "Explain what this CSS rule does before applying it."
5. **Verify** — Open the browser after every change.

## Agent mode rules

Agent can edit many files automatically. Before accepting:

- Read the diff (what changed?)
- Run the site locally
- Reject changes you don't understand — ask for an explanation first

## What Cursor is bad at

- Knowing your private passwords (never paste them)
- Guaranteeing facts (dates, statistics, API docs — verify)
- Reading your mind — be specific

## Practice exercise (15 min)

1. Open your site folder in Cursor.
2. Ask: *"What are three easy improvements to my homepage?"*
3. Pick one improvement and implement it with Agent.
4. Commit: `git commit -m "Improve homepage layout"`

## Resources

- [Cursor docs](https://docs.cursor.com)
- Keyboard shortcuts: `Ctrl+Shift+P` → "Keyboard Shortcuts"
