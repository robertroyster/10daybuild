# tasks/ — task list (replaces Google Tasks)

This folder holds `tasks.md`, a persistent (not daily) list with an **Active**
section and a **Done** section.

## Rules

- New tasks go at the bottom of **Active** unless a priority is given.
- Use `- [ ]` for active items and `- [x]` for done items.
- When a task is completed, move the whole line from **Active** to the top of
  **Done** and check it. Append ` — done YYYY-MM-DD` with the real date.
- Trim **Done**: keep only the most recent ~15 entries. Older ones can be
  dropped — this is a working list, not an audit log.
- Tasks may reference other folders. This folder is allowed to **read from
  `tracker/`** so requests like *"add a task for every pitch marked drafting"*
  work: scan `../tracker/pitches.md`, find matching rows, and add one task each
  (skip pitches that already have a task).

## tasks.md shape

```
# Tasks

## Active
- [ ] ...

## Done
- [x] ... — done YYYY-MM-DD
```
