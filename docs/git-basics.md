# Git Basics for This Project

You only need a handful of commands to start.

## Core commands

```bash
git status              # What changed?
git add .               # Stage all changes
git commit -m "message" # Save a snapshot
git push                # Upload to GitHub
git pull                # Download latest from GitHub
```

## Branch workflow (one person per branch)

```bash
git checkout main
git pull
git checkout -b my-feature
# ... make changes ...
git add .
git commit -m "Add photo gallery to my site"
git push -u origin my-feature
```

Then open a **Pull Request** on GitHub → sibling or parent reviews → **Merge**.

## Commit messages — keep them short

Good:

- `Add first journal entry`
- `Fix mobile nav layout`
- `Dark mode toggle`

Bad:

- `stuff`
- `asdfasdf`
- `fixed it`

## If something goes wrong

Ask Cursor or Copilot — but learn these magic words:

```bash
git status                    # always start here
git diff                      # see what changed
git checkout -- filename      # undo changes to ONE file (careful!)
```

**Never** run `git push --force` on `main` unless a parent says so.

## Visual guide

```
main ─────●─────●─────●─────  (stable, shared)
               \
                ●───●  your-branch  (your experiments)
```

Merge your branch when the feature works.

## Practice

1. Edit one word on your homepage
2. `git add . && git commit -m "Update homepage tagline"`
3. `git push`
4. Check GitHub — your commit should appear
