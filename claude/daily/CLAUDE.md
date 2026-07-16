# daily/ — the daily log (source of truth + permanent record)

This is the front door of the whole workspace. **Everything the user does, thinks,
or captures during a day goes into that day's file first.** From there, important
items get *routed* out to the action lists — but they are **never removed** from
the daily file. The daily log is the permanent, timestamped historical record of
what was said and when.

## The file

- One file per day: `claude/daily/YYYY-MM-DD.md`.
- Create it on the **first capture of the day** using the template below. Do not
  pre-create empty files for future days.
- These files are **append-only and never deleted, trimmed, or archived**. They
  accumulate as the record. If asked "when did I first mention X?", the answer
  lives here.

## Capturing (the default action)

When the user says anything that is a thought, task, idea, plan, or note — and
hasn't asked to do something else — **append it to today's file** as a timestamped
bullet under `## Log`:

```
- HH:MM — <verbatim-ish capture>
```

- Use the real current local time for `HH:MM`.
- Always **append at the bottom** of `## Log`. Never reorder, rewrite, or delete
  existing lines — that would corrupt the timeline.
- Keep the user's wording. Light cleanup is fine; don't change meaning.
- If the type is obvious, prefix a tag so processing is easier later:
  `[task]`, `[pitch]`, `[plan]`, `[note]`. If unsure, leave it untagged.

## Processing (on "process today" / "process the log" / end of day)

1. Read today's file (or the named day's file).
2. For each meaningful item, route it to the right destination:
   - action item → `../tasks/tasks.md`
   - article/idea → `../tracker/pitches.md`
   - something to do on a specific day → `../planner/`
   - reference info worth keeping → a note in `../notes/`
3. **Do not delete the line from the daily file.** Instead, annotate the original
   line with where it went, e.g.:
   ```
   - 09:14 — [task] email the editor back  → tasks.md
   ```
   Use ` → <destination>` (or ` → ✓` for "handled, nothing to file"). This keeps
   the record intact while showing what's already been processed, so the same
   item is never routed twice.
4. Leave purely-historical thoughts in place untouched; not everything needs to
   leave the log.

## Things that don't fit cleanly

Do **not** force an item into a list where it doesn't belong, and do **not**
invent a new category silently. Collect anything ambiguous and **ask the user**.
If a genuinely new bucket emerges (e.g. "contacts", "reading list"), propose
creating a new file/folder, get agreement, add its rule, *then* route to it.

## today template

```
# YYYY-MM-DD

## Log
- HH:MM — ...
```
