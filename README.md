# 10daybuild

A local, file-based productivity workspace driven by **Claude Code** — set up to
cover the everyday jobs people usually reach for Google Workspace to do, without
leaving a folder of plain-text and Markdown files.

The idea (borrowed from [this XDA write-up](https://www.xda-developers.com/)) is
simple: Claude Code is mostly *file access*. Point it at a folder and it can
read, write, and reorganize whatever lives there. The coding part is just one
use case. This repo is the non-coding use case — notes, planning, tracking, and
tasks — all as files you own.

## Layout

```
claude/                 # the workspace parent directory
├── CLAUDE.md           # workspace-wide rules every session reads first
├── tracker/            # Google Sheets replacement
│   ├── CLAUDE.md
│   └── pitches.md      # Markdown table of ideas + status
├── planner/            # Google Calendar (daily view) replacement
│   ├── CLAUDE.md
│   ├── today.md        # must-dos / would-likes / notes for the day
│   └── archive/        # yesterday's plans roll in here
├── tasks/              # Google Tasks replacement
│   ├── CLAUDE.md
│   └── tasks.md        # active + done sections
└── notes/              # Google Keep / Docs replacement
    ├── CLAUDE.md
    └── ...             # one Markdown file per note

.claude/
└── skills/
    └── meeting-notes/  # a saved workflow you trigger by name
        └── SKILL.md
```

Each folder carries its own `CLAUDE.md` describing what lives there and how it
should be handled, so a Claude Code session already knows the rules before you
say anything.

## How to use it

1. Open this folder in Claude Code (desktop app or CLI).
2. Talk to it: *"add a pitch", "what did I plan last Tuesday?", "add a task for
   every pitch marked drafting", "/meeting-notes for the standup".*
3. Claude edits the files. You keep plain text you fully control and can grep,
   sync, or version however you like.

It is not a background daemon — nothing watches the folders while you sleep — but
starting a session is fast enough that in practice it behaves like one.

## Why files

- **Portable** — plain Markdown, readable in any editor, Obsidian, or `cat`.
- **Yours** — no lock-in, no subscription, trivially backed up with git.
- **Searchable** — Claude reads across every file in seconds.
- **Composable** — a session can pull from `tracker/` to populate `tasks/`.
