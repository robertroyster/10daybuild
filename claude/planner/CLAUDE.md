# planner/ — daily planner (replaces Google Calendar's daily view)

This folder holds `today.md`, the plan for the current day. It is not a calendar
and has no notifications — its job is to answer "what am I doing today?" and
"what did I plan on <date>?" in seconds.

## Daily roll-over (do this at the start of a session)

1. Read the date written at the top of `today.md`.
2. If that date is **before** the real current date:
   - Move the current `today.md` into `archive/` renamed to `YYYY-MM-DD.md`
     (using the date that was inside the file).
   - Create a fresh `today.md` for the current date using the template below.
   - Optionally carry over any unfinished must-dos into the new file's
     "Must-dos" section, and mention what you carried over.
3. If the date already matches the current date, leave it and just work in it.

Never overwrite a file already in `archive/`; if a name collision happens,
append ` (2)` etc.

## today.md template

```
# YYYY-MM-DD

## Must-dos
- [ ] ...

## Would-likes
- [ ] ...

## Notes
- ...
```

## Rules

- Use `- [ ]` / `- [x]` checkboxes for must-dos and would-likes.
- Keep "Must-dos" short — these are the things that actually have to happen.
- The archive is the record. To answer "what did I plan last Tuesday?", read the
  matching `archive/YYYY-MM-DD.md`.
