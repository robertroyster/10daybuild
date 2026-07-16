# tracker/ — idea & pitch tracker (replaces Google Sheets)

This folder holds `pitches.md`, a single Markdown table of every idea being
tracked. It is the "spreadsheet" — but for lists of things with statuses, which
is what spreadsheets actually get used for most of the time.

## The table

`pitches.md` has one table with these columns:

| Column   | Meaning                                                        |
|----------|----------------------------------------------------------------|
| Title    | Short name of the idea/pitch                                   |
| Status   | One of: `idea`, `pitched`, `drafting`, `submitted`, `published`, `dropped` |
| Added    | Date the row was created (`YYYY-MM-DD`)                        |
| Notes    | Anything useful — links, blockers, editor, deadline            |

## Rules

- Add new rows at the **top** of the table (newest first) unless asked otherwise.
- Set `Added` to the real current date when creating a row.
- When the user says something moved forward ("X is drafting now"), update the
  **Status** cell in place — do not create a duplicate row.
- Keep `Status` values to the list above. If the user wants a new status, add it
  here first, then use it.
- Never delete a row to mark it finished — set status to `published` or
  `dropped` so history is preserved.
- Keep the Markdown table aligned and valid (header + separator row intact).
