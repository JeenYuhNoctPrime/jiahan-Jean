# Choosing a Site Builder — Quarto vs Hugo vs Others

You write **markdown**. A **static site generator** turns your files into a website. You don't hand-write HTML for every page.

This doc helps pick the right tool for **Jiahan (14)** and **Jiahe (16)**.

---

## Recommendation

| Person | Suggested tool | Why |
|--------|----------------|-----|
| **Both kids (start here)** | **Quarto** | Markdown-native, one config file, great preview, gentle learning curve |
| **Jiahe (16) — optional "blog engineering"** | **Hugo** (after Quarto) | Industry standard, huge themes, portfolio-ready |
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
    ├── jiahe-yu/     ← Jiahe (16)
    └── jiahan-yu/    ← Jiahan (14)
```

- Everyone collaborates in one repo
- Each person only edits their folder
- Deploy: separate GitHub Pages site per subfolder (or one combined index linking to both)

### Model B — Fork → rename to `*-site` (you are here)

1. Parent keeps `family-ai-summer-2026` as curriculum
2. Each kid forks, renames to `jiahe-site` / `jiahan-site`
3. Keep only their Quarto folder (optionally move it to repo root)
4. Deploy with GitHub Actions → `https://USERNAME.github.io/jiahe-site/`

**Full steps:** [own-your-site.md](own-your-site.md)

### Model C — Personal site repo (most "real world")

Each kid creates `username.github.io` — standard pattern for portfolios.

Quarto or Hugo lives at repo root. Best for **Jiahe (16)** when ready to show colleges/employers.

**Suggestion:** Family repo for shared lessons; Model B for each kid’s live site.

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
