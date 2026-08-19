# Personal Sites

Each person has a **Quarto website** folder:

| Folder | Person |
|--------|--------|
| `jiahe-yu/` | Jiahe Yu |
| `jiahan-yu/` | Jiahan Yu |

**Rule:** Only edit your own folder.

## Structure

```
sites/jiahe-yu/   (or jiahan-yu/)
├── _quarto.yml       # Site config — title, nav, theme
├── index.qmd         # Home page (markdown!)
├── about.qmd
├── styles.css        # Optional custom CSS
└── journal/
    ├── index.qmd     # Auto-lists your entries
    └── YYYY-MM-DD-title.qmd
```

## Quick start

```bash
# Install Quarto first: https://quarto.org/docs/download/
cd sites/jiahe-yu    # or sites/jiahan-yu
quarto preview
```

Edit any `.qmd` file → save → browser updates.

## Learn markdown first

[docs/markdown-basics.md](../docs/markdown-basics.md)

## Deploy

[docs/quarto-setup.md](../docs/quarto-setup.md)

## Optional: raw HTML track

[docs/optional-html-starter/](../docs/optional-html-starter/)
