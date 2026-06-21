# Workspace rules

This `claude/` directory is a personal productivity workspace. It is **not** a
software project — there is no code to build or test. Treat every file here as
notes, plans, trackers, and tasks that belong to the user.

## General behaviour

- Files are the source of truth. When the user asks you to record, change, or
  reorganize something, **edit the relevant file** rather than only replying in
  chat.
- Default to **Markdown**: headings, bullet lists, and tables where they fit.
  Give messy pasted text real structure.
- Keep prose tight. These are working documents, not essays.
- Never invent facts to fill a table cell. If something is unknown, leave it
  blank or write `—`.
- Dates use `YYYY-MM-DD`. Use the real current date, not a guess.
- When a request spans folders, you may read from one to act on another (for
  example: pull pitches from `tracker/` to create entries in `tasks/`).

## What each folder is for

| Folder      | Replaces             | Holds                                   |
|-------------|----------------------|-----------------------------------------|
| `tracker/`  | Google Sheets        | `pitches.md` — a status table of ideas  |
| `planner/`  | Google Calendar      | `today.md` — the day's plan; `archive/` |
| `tasks/`    | Google Tasks         | `tasks.md` — active + done lists        |
| `notes/`    | Google Keep / Docs   | one Markdown file per note              |

Each folder has its own `CLAUDE.md` with the specifics. Read it before acting on
files in that folder.

## Skills

Saved workflows live in `.claude/skills/`. Trigger them by name (e.g.
`meeting-notes`) instead of re-describing the workflow each time.
