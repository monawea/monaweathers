# Thoughts for Today — Update Skill

description: Update the "Thoughts for Today" section on mona-shelly-site.html with a new thought from Mona.

## When to use

Trigger when the user says any of:
- `/thoughts`
- "update my thought"
- "new thought for today"
- "change the thoughts for today"
- "post a new thought"

## What this updates

File: `/home/claude/repo/mona-shelly-site.html`

Section: the `<section class="tft" id="thoughts">` block.

Three things change every time:
1. **Main thought** — the `<p class="tft-lead">` text (required)
2. **Follow-up note** — the `<p class="tft-note">` text (optional — delete the line if Mona only wants one paragraph)
3. **Date** — both the `datetime="YYYY-MM-DD"` attribute and the visible date text inside `<time>` (e.g. `20 Aug`)

## Instructions

1. Ask Mona for the new thought if she hasn't provided it. She may give:
   - Just the main thought (one paragraph)
   - A main thought + a follow-up note (two paragraphs)
2. Use today's date from the session context for the `<time>` tag.
3. Make the three edits above using the Edit tool.
4. Commit with message: `Update Thoughts for Today — [date]`
5. Push to GitHub using the token push command from CLAUDE.md.
6. Confirm it's live.

## Commit push command

Use the token push format from CLAUDE.md — the token is stored in the session, not here.
