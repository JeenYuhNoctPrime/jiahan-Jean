# Personal Sites (Quarto)

Each person gets a **Quarto website** folder here. Rename `teen-one` and `teen-two` to your names.

## Structure

```
sites/your-name/
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
cd sites/your-name
quarto preview
```

Edit any `.qmd` file → save → browser updates.

## Learn markdown first

Before customizing the site, complete [docs/markdown-basics.md](../docs/markdown-basics.md).

## Deploy

See [docs/quarto-setup.md](../docs/quarto-setup.md).

## Optional: raw HTML track

Hand-written HTML/CSS starter (for curiosity, not the main path):

[docs/optional-html-starter/](../docs/optional-html-starter/)

## Choosing Quarto vs Hugo

See [docs/choosing-a-site-builder.md](../docs/choosing-a-site-builder.md).
