# Own Your Site — Fork → Separate Path → Deploy

The family curriculum repo is **public**:
[Zhenglei-BCS/family-ai-summer-2026](https://github.com/Zhenglei-BCS/family-ai-summer-2026)

That means you can make **your fork public**, rename it, and publish a website anyone can visit.

| Person | Likely GitHub | Suggested repo name | Site folder today |
|--------|---------------|---------------------|-------------------|
| Jiahe (16) | `jheyyx` | `jiahe-site` | `sites/jiahe-yu/` |
| Jiahan (14) | `JeenYuhNoctPrime` | `jiahan-site` | `sites/jiahan-yu/` |

Confirm usernames on your profile, then follow the **recommended path** below.

---

## Recommended path (do this)

Because the family repo is public, use this sequence:

```
1. Make YOUR fork public
2. Rename fork → jiahe-site / jiahan-site
3. Keep only YOUR site (move to repo root)
4. Preview with quarto
5. Deploy — pick Option A (Actions) or Option B (quarto publish)
6. Open your live URL on a phone
```

### Why this path?

| Choice | Why |
|--------|-----|
| **Public fork** | Free GitHub Pages needs a public repo. Parent repo is already public, so your fork can be public too. |
| **Rename to `*-site`** | Clear that this is *your* website, not the shared curriculum. |
| **Site at repo root** | Simplest Pages + Quarto setup. |
| **Deploy Option A (Actions)** | Recommended — every push to `main` updates the live site. |
| **Deploy Option B (`quarto publish`)** | Faster first publish — you run a command; no workflow file yet. |

**Remember:** Public repo + public Pages means **anyone with the URL can see the site and the source**. Write only what you are okay sharing (no phone numbers, school address, private photos of others without permission).

---

## Big picture

```
Family repo (public curriculum)
        │
        │  you forked
        ▼
Your fork  ──make public──►  rename ──►  jiahe-site / jiahan-site
        │
        │  keep only YOUR folder at root
        ▼
GitHub Pages  ──►  https://YOU.github.io/jiahe-site/
```

You and your sibling **do not share a deploy**. Each person pushes to their own repo.
The family repo stays the shared lesson book.

---

## Step 1 — Make your fork public

On GitHub, open **your** fork (not the family repo):

1. **Settings → General → Danger Zone → Change repository visibility**
2. Choose **Public**
3. Confirm

If the fork is still private, Pages on a free account usually will not stay published.

---

## Step 2 — Rename the fork

Still on **your** repo:

1. **Settings → General → Repository name**
2. Rename to `jiahe-site` or `jiahan-site`
3. Save

Clone URL becomes:

```text
https://github.com/YOUR-USERNAME/jiahe-site.git
```

---

## Step 3 — Clone (or update) on your computer

**If you have not cloned yet:**

```bash
git clone https://github.com/YOUR-USERNAME/jiahe-site.git
cd jiahe-site
```

**If you already cloned the old name:**

```bash
cd family-ai-summer-2026
git remote set-url origin https://github.com/YOUR-USERNAME/jiahe-site.git
git remote -v
```

---

## Step 4 — Keep only your site at the repo root (recommended)

Your Quarto site becomes the whole repo. Cleaner URLs and simpler deploys.

```powershell
# From the repo root — use YOUR folder
cd sites/jiahe-yu   # or sites/jiahan-yu

# Copy site files up to the repo root
Copy-Item -Recurse -Force * ..\..\
cd ..\..\
```

Then, in **your** repo only, remove what you do not need:

- the sibling's folder under `sites/`
- optionally most of `docs/` (keep if you still want curriculum locally)

Keep at least:

```text
_quarto.yml
index.qmd
about.qmd
styles.css
journal/
.github/workflows/   (after Step 6)
README.md            (short personal README)
```

Update `_quarto.yml` — your live URL and GitHub link:

```yaml
website:
  title: "Jiahe Yu"   # or Jiahan Yu
  site-url: https://YOUR-USERNAME.github.io/jiahe-site/
  navbar:
    right:
      - icon: github
        href: https://github.com/YOUR-USERNAME/jiahe-site
```

Commit and push:

```bash
git add -A
git commit -m "Make this repo my personal Quarto site"
git push -u origin main
```

### Alternative — keep the family folder layout

Stay in `sites/jiahe-yu/` (or `jiahan-yu/`). Delete only the sibling folder.
Deploy needs `working-directory` in the Action. Prefer the root layout unless you
want curriculum docs in the same repo.

---

## Step 5 — Preview locally

```bash
# Site at root (recommended)
quarto preview

# Folder layout alternative
cd sites/jiahe-yu
quarto preview
```

---

## Step 6 — Deploy (choose one)

You need a **public** `*-site` repo and a working `quarto preview` first.
Then pick **one** deploy method:

| | Option A — GitHub Actions | Option B — `quarto publish gh-pages` |
|---|---------------------------|--------------------------------------|
| **Best for** | Ongoing work (recommended) | First live site in 5 minutes |
| **How it updates** | Push to `main` → site rebuilds | You run `quarto publish` again |
| **Pages setting** | Source = **GitHub Actions** | Branch = **`gh-pages`** / root |
| **Where to look** | Steps below + [workflow template](templates/deploy-quarto-pages.yml) | Steps below + [quarto-setup.md — Publish](quarto-setup.md#publish-to-github-pages) |

You can start with **B**, then switch to **A** later. Do not enable both at once
(pick one Pages source).

Live URLs (either option):

```text
https://YOUR-USERNAME.github.io/jiahe-site/
https://YOUR-USERNAME.github.io/jiahan-site/
```

---

### Option A — GitHub Actions (recommended)

GitHub runs Quarto for you in the cloud. No need to remember a publish command.

1. In **your** `*-site` repo, create the folder `.github/workflows/`
2. Copy the family template into it:

   - **Copy from:** [`docs/templates/deploy-quarto-pages.yml`](templates/deploy-quarto-pages.yml)
   - **Save as:** `.github/workflows/deploy-quarto-pages.yml`

3. Edit the file if needed:

   - Site at **repo root** (recommended) → leave `working-directory: .` and `path: _site`
   - Site still under `sites/jiahe-yu/` → set `working-directory` and artifact `path` as the comments in that file explain

4. On GitHub: **Settings → Pages → Source: GitHub Actions**
5. Commit, push to `main`, open the **Actions** tab — wait for a green check
6. Visit your `*.github.io/…` URL

**What the Action does:** checkout → install Quarto → `quarto render` → upload `_site` → deploy Pages.

Ask Cursor if stuck: *"Help me add the deploy-quarto-pages workflow from the family repo template."*

---

### Option B — `quarto publish gh-pages` (fast first publish)

You build and push from your laptop. Good for a first demo day.

1. Open a terminal in the folder that contains `_quarto.yml`
2. Run:

```bash
quarto publish gh-pages
```

3. On GitHub: **Settings → Pages → Deploy from a branch → `gh-pages` / root**
4. Wait 1–2 minutes, then open your live URL

More detail: [quarto-setup.md — Publish to GitHub Pages](quarto-setup.md#publish-to-github-pages)

**Later:** copy the Action from Option A and switch Pages source to **GitHub Actions**
so every `git push` updates the site without running `quarto publish` again.

---

### Other Pages notes

Older HTML-only notes: [deploying-github-pages.md](deploying-github-pages.md)
(useful background; Quarto deploys follow Option A or B above).

---

## Step 7 — Separate from sibling (and optional curriculum sync)

| Do | Don't |
|----|-------|
| Edit only your site files | Edit the sibling's site folder |
| Push to **your** `jiahe-site` / `jiahan-site` | Expect the family repo to update your live site |
| Optionally pull tips from the family repo | Force-push or rewrite family history |

Optional — read curriculum updates without changing your live site:

```bash
git remote add upstream https://github.com/Zhenglei-BCS/family-ai-summer-2026.git
git fetch upstream
# Copy a useful doc by hand, or ask Cursor to help merge one file
```

You are **not** required to sync. Separate paths means your site evolves on its own.

---

## Jiahe (16) — Hugo later

When Quarto feels easy:

1. Keep this Quarto site as `jiahe-site`, **or**
2. Create a second repo `jiahe-hugo` and follow Hugo's getting started
3. Same idea: build → GitHub Pages

Finish one live Quarto site before switching builders.

---

## Checklist

- [ ] Fork is **public** (family repo is already public)
- [ ] Fork renamed to `jiahe-site` / `jiahan-site`
- [ ] Only my content left (sibling folder removed from **my** repo)
- [ ] `site-url` and GitHub link updated in `_quarto.yml`
- [ ] `quarto preview` works locally
- [ ] Deploy chosen: **Option A** (Actions) or **Option B** (`quarto publish`)
- [ ] Pages source matches that choice (Actions **or** `gh-pages` branch — not both)
- [ ] Live URL opens on phone
- [ ] Content is okay for the public internet
- [ ] First journal entry after going solo

---

## Visibility reminder

| Repo | Visibility | Effect |
|------|------------|--------|
| Family curriculum | **Public** | Anyone can read the lessons |
| Your `*-site` fork | **Public** (recommended) | Pages works on free GitHub; site is shareable |
| Your live website | Always public if Pages is on | Anyone with the URL can visit |

Private forks of a public parent are possible, but then free Pages usually will not publish. Stay public for this project.

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| Cannot make fork public | Family repo must be public (it is). Refresh Settings → Visibility. |
| 404 on GitHub Pages | Wait 2–5 min; check Actions **or** `gh-pages` branch; confirm Pages source matches Option A or B; repo must be public |
| Confused which deploy to use | See [Step 6](#step-6--deploy-choose-one) — A = Actions, B = `quarto publish` |
| CSS / links broken | Set `website: site-url:`; use relative links in `.qmd` |
| Action fails on Quarto | Open [workflow template](templates/deploy-quarto-pages.yml); read the red log in the Actions tab |
| `quarto publish` fails | Check you are logged in to GitHub (`gh auth status`); see [quarto-setup.md](quarto-setup.md#publish-to-github-pages) |
| Pushed to family repo by mistake | `git remote -v` — `origin` must be **your** username |
| Fork still named `family-ai-summer-2026` | Step 2 — rename first |

---

## Parent note

[Zhenglei-BCS/family-ai-summer-2026](https://github.com/Zhenglei-BCS/family-ai-summer-2026)
is the **public** shared curriculum. Kids own day-to-day commits and deploy on their
public `*-site` repos. Review live URLs on demo day — not every push to the family repo.
