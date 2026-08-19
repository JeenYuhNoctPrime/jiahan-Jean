# GitHub Copilot — AI While You Type

Copilot suggests code **as you type** in VS Code or GitHub.com. It's like autocomplete on steroids.

## Setup

1. Install [VS Code](https://code.visualstudio.com/) (or use Copilot inside GitHub.dev)
2. Install the **GitHub Copilot** extension
3. Sign in with your GitHub account (free tier available for students)

## How it works

- Gray ghost text appears → press `Tab` to accept
- `Alt+]` / `Alt+[` to cycle suggestions
- Highlight a comment, Copilot often suggests the code below it

## Example workflow

Type a comment first — Copilot reads comments as instructions:

```html
<!-- Navigation with Home, About, Journal links -->
```

Wait for the suggestion. Tab to accept. Edit if needed.

```css
/* Center the nav links horizontally with flexbox and gap 1rem */
```

## Copilot vs. Cursor

| | Copilot | Cursor |
|---|---------|--------|
| Best for | Small completions, boilerplate | Big refactors, questions, agents |
| Interaction | Inline while typing | Chat + agent |
| Learning | You drive, it assists | Can drive more of the task |

**Use both:** Cursor for "build my journal page"; Copilot for "finish this CSS rule."

## Good habits

- **Don't accept blindly** — read every suggestion
- **Comments are prompts** — write clear comments above empty functions
- **It repeats patterns** — if your code is messy, suggestions get messy

## Practice exercise (15 min)

1. Open `sites/your-name/css/style.css`
2. Add a comment: `/* Style journal entry titles with larger font and bottom border */`
3. Accept Copilot's suggestion or tweak it
4. Compare with asking Cursor the same thing — which did you prefer?

## Student benefit

GitHub offers **Copilot free for verified students**. Check: [GitHub Education](https://education.github.com/)
