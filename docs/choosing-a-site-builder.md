# Choosing a Site Builder — Quarto vs Hugo vs Others

You write **markdown**. A **static site generator** turns your files into a website. You don't hand-write HTML for every page.

This doc helps pick the right tool for ages 14 and 16.

---

## Recommendation

| Person | Suggested tool | Why |
|--------|----------------|-----|
| **Both kids (start here)** | **Quarto** | Markdown-native, one config file, great preview, gentle learning curve |
| **16yo who wants "real blog engineering"** | **Hugo** (after Quarto) | Industry standard, huge themes, faster at scale |
| **Parent / optional deep dive** | Raw HTML starter in `docs/optional-html-starter/` | See how the web works under the hood |

**Our repo uses Quarto as the default path.**

---

## Quarto — recommended default

**What it is:** Open-source tool from Posit. You write `.qmd` files (markdown + optional YAML). Run `quarto render` → website.

**Pros**
- Markdown-first — matches how we teach writing
- Built-in website project type (`project: type: website`)
- Nice themes out of the box (cosmo, darkly, etc.)
- `quarto preview` live reload while editing
- Same tool works for school reports later (PDF, slides)
- AI assistants know Quarto well

**Cons**
- Requires installing [Quarto CLI](https://quarto.org/docs/get-started/)
- Custom layouts beyond themes need a bit of CSS

**Best for:** Personal site + journal, school projects, mixed writing/code

---

## Hugo — great second step

**What it is:** Go-based static site generator. Content in `content/**/*.md`, config in `hugo.toml`.

**Pros**
- Extremely fast builds
- Thousands of community themes
- Powers many professional blogs
- Single binary, no Node/Ruby

**Cons**
- Theme customization uses Go templates — steep for beginners
- More "magic" folders (`layouts/`, `archetypes/`)
- Debugging a theme issue can frustrate new learners

**Best for:** Teen who finished Quarto and wants a polished blog with an existing theme

**When to introduce:** Week 5+ or second summer project, not day one.

---

## Other options (quick compare)

| Tool | Difficulty | GitHub Pages | Notes |
|------|------------|--------------|-------|
| **Quarto** | ★★☆☆☆ | ✅ | **Start here** |
| **Hugo** | ★★★☆☆ | ✅ | Strong blog, harder customize |
| **MkDocs + Material** | ★★☆☆☆ | ✅ | Docs-style sites, Python install |
| **Jekyll** | ★★★☆☆ | ✅ native | Ruby; GitHub's original default |
| **Eleventy** | ★★★★☆ | ✅ | Flexible JS, less hand-holding |
| **Astro** | ★★★★☆ | ✅ | Modern, more web-dev concepts |
| **Hand-coded HTML** | ★★☆☆☆ | ✅ | Good for learning HTML/CSS once |

---

## Per-account setup (each kid has their own GitHub)

Three workable models:

### Model A — One family repo (simplest)

```
family-ai-summer-2026/
└── sites/
    ├── alex/     ← Alex's Quarto site
    └── sam/      ← Sam's Quarto site
```

- Everyone collaborates in one repo
- Each person only edits their folder
- Deploy: separate GitHub Pages site per subfolder (or one combined index linking to both)

### Model B — Fork the template (good independence)

1. Parent maintains `family-ai-summer-2026` as template
2. Each kid: **Use this template** → creates `alex-site`, `sam-site` on their account
3. They own their repo, learn full git workflow
4. Deploy to `alex.github.io` via GitHub Pages

### Model C — Personal site repo (most "real world")

Each kid creates `username.github.io` — standard pattern for portfolios.

Quarto or Hugo lives at repo root. Best for 16yo ready to show colleges/employers.

**Suggestion:** Start with **Model A** for weeks 1–4, migrate to **Model B or C** when comfortable.

---

## Decision flowchart

```
Start
  │
  ▼
Can you write a markdown journal entry?
  │ no → docs/markdown-basics.md
  │ yes
  ▼
Want to focus on WRITING or ENGINEERING?
  │
  ├─ Writing → Quarto
  │
  └─ Engineering / themes → Hugo (after 2–3 weeks on Quarto)
```

---

## What we dropped from v1

The original repo had hand-written HTML/CSS sites. Those moved to `docs/optional-html-starter/` — still useful to peek at how `<nav>` and CSS work, but **not** the main path anymore.

---

## Parent FAQ

**Q: Do they need to learn HTML?**  
Eventually a little — bold understanding of links, images, and "inspect element" helps. Not week one.

**Q: Quarto vs Notion/Obsidian?**  
Notion/Obsidian are great for private notes. Quarto + GitHub teaches version control and public publishing.

**Q: Can AI set up Hugo/Quarto for them?**  
Yes — but they should run the commands and read the config so it's not magic.
