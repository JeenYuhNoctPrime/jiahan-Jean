# Claude Code — AI in the Terminal

Claude Code runs in your terminal. It can read files, run commands, and make edits — useful for scripts and automation.

## When to use it

- "Rename all `.jpg` files in this folder with today's date"
- "Write a Python script that converts my journal markdown to HTML"
- "Debug why `git push` failed"

For visual web design, **Cursor is usually easier**. Claude Code shines for **files, scripts, and git**.

## Setup

1. Install [Claude Code](https://docs.anthropic.com/en/docs/claude-code) (follow official docs)
2. Authenticate in terminal
3. `cd` into your project folder before starting

## Basic usage

```bash
cd family-ai-summer-2026
claude
```

Then talk naturally:

```
List all markdown files in sites/my-name/journal/ and show me the
newest one.
```

```
Create a script scripts/new-journal-entry.sh that creates a dated
markdown file with a title prompt. Keep it simple.
```

## Safety rules

Claude Code can run shell commands. Before approving:

- Read what command it wants to run
- Say **no** to `rm -rf`, force pushes, or anything you don't understand
- Keep work inside this project folder

## Compare the three tools

| Task | Best tool |
|------|-----------|
| "Make my site pretty" | Cursor |
| "Complete this function while I type" | Copilot |
| "Organize 200 files" | Claude Code |
| "Explain git error" | Any — try all three in Week 6 |

## Practice exercise (optional)

If Claude Code is installed:

```
Count how many lines are in my index.html and journal entries combined.
```

If not installed yet, skip to Week 6 in the curriculum.
