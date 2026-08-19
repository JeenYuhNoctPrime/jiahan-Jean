# Deploy Your Site with GitHub Pages

Turn your folder into a real website anyone can visit.

## Option A — Simple (recommended to start)

Each personal site can be published from a subfolder using a branch or GitHub Actions. For the **easiest first deploy**:

### Steps

1. Push your site to GitHub (already done if you're reading this online)
2. On GitHub: **Settings → Pages**
3. Under **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: `main` → folder `/ (root)` *or* `/docs` if you move sites later
4. Save. Wait 1–2 minutes.
5. Your site appears at `https://[username].github.io/family-ai-summer-2026/`

### Fix paths for subfolders

If your site lives in `sites/your-name/`, links must be relative:

```html
<!-- Good -->
<link rel="stylesheet" href="css/style.css">
<a href="journal/2026-08-19-first-entry.html">First entry</a>

<!-- Bad (breaks on GitHub Pages) -->
<link rel="stylesheet" href="/css/style.css">
```

Ask Cursor: *"Check all my links work when hosted at /family-ai-summer-2026/sites/my-name/"*

## Option B — One site per kid (later)

When ready, each person can:

1. Create branch `gh-pages-yourname`, or
2. Use a GitHub Action (ask AI to help set this up), or
3. Split into separate repos — `yourname.github.io` pattern

## Custom domain (optional)

Buy a domain → GitHub Pages settings → add CNAME → follow DNS instructions.

## Privacy checklist before going public

- [ ] No full name + school + address together
- [ ] No phone number or email unless intentional
- [ ] Photos of others only with permission
- [ ] Journal entries you're okay with grandparents reading

## Troubleshooting

| Problem | Fix |
|---------|-----|
| 404 page | Check Settings → Pages is enabled; wait 5 min |
| CSS missing | Use relative paths, not `/css/...` |
| Images broken | Check filename case (Linux is case-sensitive) |

## Celebrate

Screenshot your live URL and paste it in your journal. You shipped. 🎉
