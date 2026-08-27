# Quarto Website Setup

Turn markdown journal files into a real website.

---

## Install Quarto

1. Download: [quarto.org/docs/download](https://quarto.org/docs/download/)
2. Install (Windows: run the `.msi`)
3. Verify in terminal:

```bash
quarto --version
```

Optional: install **Quarto** extension in Cursor/VS Code for syntax highlighting.

## Add Python code

Quarto runs Python code through Jupyter. Install Jupyter once from PowerShell:

```powershell
python -m pip install jupyter
```

The `jupyter: python3` setting in `sites/your-name/_quarto.yml` selects Python for
the site. Put executable Python in a QMD code cell:

````markdown
```{python}
numbers = [1, 2, 3]
sum(numbers)
```
````

Then render or preview as usual. The result appears in the generated webpage.

---

## Your site folder

Each person works in `sites/your-name/`:

```
sites/your-name/
├── _quarto.yml          # Site config (title, nav, theme)
├── index.qmd            # Home page
├── about.qmd            # About page
├── styles.css           # Optional custom styles
└── journal/
    ├── index.qmd        # Journal listing page
    └── 2026-08-19-first-entry.qmd
```

---

## Daily workflow

```bash
cd sites/your-name
quarto preview          # Live preview in browser — leave running while editing
```

Edit `.qmd` files → save → browser refreshes.

When happy:

```bash
quarto render           # Builds static site to _site/
```

---

## Publish to GitHub Pages

### Option 1 — Quarto publish (easiest)

From your site folder, with GitHub authenticated:

```bash
quarto publish gh-pages
```

Quarto creates/updates a `gh-pages` branch. Enable Pages in repo Settings → Pages → branch `gh-pages`.

### Option 2 — GitHub Action (family repo)

For multiple sites in one repo, a parent can set up Actions later. Ask AI: *"Create a GitHub Action that runs quarto render on sites/jiahe-yu/ and sites/jiahan-yu/ and deploys to Pages."*

### Option 3 — Personal repo (Model B/C)

Kid owns `username.github.io`. Same `quarto publish gh-pages` from their repo root.

---

## Customize with AI

Good prompts:

```
Read _quarto.yml in sites/my-name/. Change the theme to darkly and
add a footer with my name and the current year.
```

```
Create a new journal entry qmd for today using our standard template
in docs/markdown-basics.md
```

```
My quarto preview shows a broken image in journal/2026-08-19-first-entry.qmd.
Fix the path — explain what was wrong.
```

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| `quarto: command not found` | Reopen terminal after install; check PATH |
| Preview won't start | Run from folder containing `_quarto.yml` |
| Journal page empty | Add `.qmd` files under `journal/` with YAML title |
| Theme looks wrong | Edit `format: html: theme:` in `_quarto.yml` |

Built output goes to `_site/` — don't edit files there; always edit `.qmd` sources.

---

## Themes to try

In `_quarto.yml` under `format: html: theme:`:

- `cosmo` — clean default
- `darkly` — dark mode
- `flatly` — flat bright
- `journal` — blog-like
- `minty` — soft green

List: [quarto.org/docs/output-formats/html-themes](https://quarto.org/docs/output-formats/html-themes.html)
