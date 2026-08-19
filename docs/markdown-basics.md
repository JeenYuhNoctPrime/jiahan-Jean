# Markdown Basics

Markdown is plain text with simple symbols for formatting. You write it everywhere in this project — journals, README files, GitHub comments, and (with Quarto) entire websites.

**Rule of thumb:** If you can write a text message, you can write markdown.

---

## Why learn markdown first?

1. **Works everywhere** — GitHub, Notion, Discord, AI chat, Quarto, Hugo
2. **AI understands it** — paste markdown into Cursor and ask for edits
3. **You focus on words** — not HTML tags or layout engines
4. **Git-friendly** — easy to see what changed line by line

---

## Cheat sheet

```markdown
# Heading 1 (biggest)
## Heading 2
### Heading 3

Regular paragraph. Blank line = new paragraph.

**bold text**
*italic text*
~~strikethrough~~

- bullet item
- another item

1. numbered
2. list

[link text](https://example.com)
![image alt text](photos/summer.jpg)

> Blockquote — good for pull quotes or notes

`inline code`

```text
code block (use three backticks)
```

| Column A | Column B |
|----------|----------|
| cell     | cell     |

---   ← horizontal line
```

---

## YAML front matter (for Quarto / Hugo)

At the top of a `.qmd` or blog post file:

```yaml
---
title: "My first journal entry"
date: 2026-08-19
description: "What I learned about AI today"
---
```

The `---` lines matter. Everything below is normal markdown.

---

## Practice exercises

Do these in `sites/your-name/journal/` as `.qmd` files.

### Exercise 1 — Hello journal (10 min)

Create `journal/2026-08-20-hello.qmd`:

```markdown
---
title: Hello journal
date: 2026-08-20
---

# Hello journal

Today I learned that **markdown** is easier than HTML for writing.

## Three things I like
- Music
- Games
- Building things

> My goal this summer: ship something I'm proud of.
```

### Exercise 2 — Link and image (10 min)

Add a link to your favorite band or game wiki. Add an image (use a royalty-free URL or a local file in `images/`).

Ask Cursor: *"Check my markdown links and fix anything broken."*

### Exercise 3 — Table (15 min)

Make a table comparing three AI tools (Cursor, Copilot, Claude Code) with columns: Tool, Best for, Rating 1–5.

### Exercise 4 — Fix AI mistakes (15 min)

Paste this broken markdown into a file and fix it without AI first, then verify with AI:

```markdown
#My broken entry
**Today was fun*
- learned markdown
1. first
1. second

[my github] (https://github.com)
```

---

## Preview markdown in Cursor

1. Install extension: **Markdown Preview Enhanced** or use built-in preview (`Ctrl+Shift+V`)
2. Open any `.md` or `.qmd` file
3. Split view: edit left, preview right

For Quarto files, run `quarto preview` in your site folder (see [quarto-setup.md](quarto-setup.md)).

---

## Good journal entry template

Copy for each new entry:

```markdown
---
title: "Short descriptive title"
date: YYYY-MM-DD
---

# Title repeats here (or skip if title is enough)

## What I did

## What I learned

## What surprised me

## Tomorrow
```

---

## Markdown + AI workflow

| Step | You | AI |
|------|-----|-----|
| Draft | Write rough notes in markdown | — |
| Polish | Read every suggestion | Fix grammar, suggest headings |
| Format | Approve changes | Add tables, links, callouts |
| Verify | Check facts and tone | — |

**Never** let AI invent journal events. You write what happened; AI helps with clarity.

---

## Common mistakes

| Mistake | Fix |
|---------|-----|
| `#Heading` no space | `# Heading` |
| Forgetting blank line before list | Add empty line above `- item` |
| Broken link | Check `(url)` has no spaces |
| Smart quotes from Word | Re-type `"` and `'` in Cursor |

---

## Next step

Once you're comfortable with markdown, build your site with [quarto-setup.md](quarto-setup.md).
