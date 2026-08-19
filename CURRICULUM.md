# 8-Week Summer Curriculum

Flexible plan — ~3–5 hours per week. Adjust pace to your schedule.

---

## Week 1 — Markdown & setup

**Goals:** GitHub/Cursor ready, understand markdown, first journal entry.

| Day | Activity |
|-----|----------|
| 1 | Install Cursor + clone repo. Read [docs/markdown-basics.md](docs/markdown-basics.md) cheat sheet. |
| 2 | Complete **Exercise 1** (hello journal) in a new `.qmd` file under `sites/your-name/journal/`. |
| 3 | Install [Quarto](https://quarto.org/docs/download/). Run `quarto preview` in your site folder. |
| 4 | Read [docs/ai-tools/cursor.md](docs/ai-tools/cursor.md). Ask: *"Review my markdown for mistakes."* |
| 5 | **Exercise 2–3** (links, table). First git commit. |

**Deliverable:** One journal `.qmd` file + preview running locally.

**Parent checkpoint:** Can they write `# heading`, `**bold**`, and a bullet list from memory?

---

## Week 2 — Quarto site & journal habit

**Goals:** Customize site config, write 3 journal entries, understand front matter.

| Day | Activity |
|-----|----------|
| 1 | Edit `_quarto.yml` — change title and try a new `theme:`. |
| 2 | Personalize `index.qmd` and `about.qmd`. |
| 3 | Write 2 more journal entries using the template in markdown-basics. |
| 4 | Add an image to one entry (local file in `images/` or royalty-free URL). |
| 5 | Ask Cursor: *"Explain what _quarto.yml controls vs what my .qmd files control."* |

**Deliverable:** 3 journal entries visible on the Journal page.

**Prompt practice:** [prompts/starter-prompts.md](prompts/starter-prompts.md)

---

## Week 3 — Make it yours

**Goals:** Custom styling, optional CSS, peer review.

| Day | Activity |
|-----|----------|
| 1 | Try 3 Quarto themes — pick one and explain why in a journal entry. |
| 2 | Edit `styles.css` with AI help (small change — font size, link color). |
| 3 | Add a "Projects" or "Hobbies" section to `index.qmd`. |
| 4 | Optional: peek at [docs/optional-html-starter/](docs/optional-html-starter/) — compare HTML vs your rendered `_site/`. |
| 5 | Peer review: swap laptops, suggest one improvement each. |

**Deliverable:** Site that reflects their personality + journal entry comparing markdown vs HTML.

---

## Week 4 — Git collaboration

**Goals:** Branches, pull requests, not stepping on each other's work.

| Day | Activity |
|-----|----------|
| 1 | Read [docs/git-basics.md](docs/git-basics.md). |
| 2 | Each person works on their own branch: `git checkout -b sites/yourname-week4` |
| 3 | Make changes, push, open a Pull Request on GitHub. |
| 4 | Review sibling's PR — leave one constructive comment. |
| 5 | Merge PRs together. Fix any conflicts with AI help. |

**Deliverable:** At least one merged pull request per person.

**Parent checkpoint:** Can they explain branch vs. main?

---

## Week 5 — Feature sprint

**Goals:** Pick one feature from [PROJECT-IDEAS.md](PROJECT-IDEAS.md) and ship it.

Suggestions by person:

- **Jiahan (14):** flashcard generator, text adventure chapter, photo gallery
- **Jiahe (16):** hobby dashboard, portfolio section, automation script — or start the **Hugo** optional track

| Day | Activity |
|-----|----------|
| 1–2 | Plan the feature (bullet list, sketch on paper). |
| 3–4 | Build with AI pair programming. |
| 5 | Write a short `FEATURE.md` explaining what you built and one thing AI got wrong. |

**Deliverable:** One new feature + honest retrospective.

---

## Week 6 — Second AI tool

**Goals:** Compare tools fairly. Same small task, three approaches.

**The experiment:** Add a "footer with social links" to your site using:

1. Cursor Agent (chat)
2. GitHub Copilot (inline)
3. Claude Code (terminal) — if installed

| Day | Activity |
|-----|----------|
| 1 | Copilot setup + [docs/ai-tools/github-copilot.md](docs/ai-tools/github-copilot.md) |
| 2 | Complete task #2 with Copilot |
| 3 | Claude Code setup (optional) + task #3 |
| 4 | Write a comparison table: speed, quality, ease |
| 5 | Pick your default tool and explain why |

**Deliverable:** `docs/my-ai-tool-review.md` (create it — your opinions matter).

---

## Week 7 — Go live

**Goals:** Deploy to GitHub Pages. Custom domain optional.

| Day | Activity |
|-----|----------|
| 1 | Read [docs/quarto-setup.md](docs/quarto-setup.md) |
| 2 | Run `quarto publish gh-pages` or set up GitHub Action with AI help |
| 3 | Fix anything broken in production (paths, images) |
| 4 | Share the URL with one person outside the family |
| 5 | Add a `robots.txt` and think about privacy (what not to publish) |

**Deliverable:** Public URL that loads on a phone.

---

## Week 8 — Demo day 🎉

**Goals:** Present, reflect, plan what's next.

| Day | Activity |
|-----|----------|
| 1–2 | Prepare 5-minute demo (site walkthrough + one AI story) |
| 3 | **Demo day** — present to family |
| 4 | Write final journal entry: "What I learned about AI this summer" |
| 5 | Archive or tag repo `summer-2026-complete`. Brainstorm fall projects. |

**Deliverable:** Demo + written reflection.

---

## Assessment rubric (informal)

| Skill | Emerging | Solid | Strong |
|-------|----------|-------|--------|
| Prompting | Vague requests | Clear context + constraints | Iterates, verifies output |
| Git | Can commit | Branch + PR | Resolves merge conflicts |
| Web basics | Edits text | Adds pages + CSS | Responsive, deployed |
| AI literacy | Uses AI for everything | Knows when to verify | Critiques AI mistakes |
| Ownership | Copies blindly | Explains their code | Ships original ideas |

---

## If you fall behind

- **Minimum viable summer:** personal site + 3 journal entries + deployed + one AI tool mastered.
- **Skip weeks 5–6** if needed; don't skip week 7 (going live is the best motivator).
