---
name: meeting-notes
description: Generate a fresh meeting-notes Markdown file with the standard sections (attendees, agenda, discussion, decisions, action items). Use when the user says "meeting notes", "/meeting-notes", "take notes for the <name> meeting", or wants to capture a meeting.
---

# meeting-notes

Create a new, ready-to-fill meeting-notes file so the user never has to hunt for
a template.

## Steps

1. Work out the meeting title and date.
   - Title: from what the user said ("standup", "design review"). If none given,
     use `Meeting`.
   - Date: the real current date, `YYYY-MM-DD`.
2. Create the file at `claude/notes/meeting-YYYY-MM-DD-<kebab-title>.md`.
   If a file with that name already exists, append `-2`, `-3`, etc.
3. Write the template below, filling in the title and date. Leave the body
   sections empty (just the headings and a placeholder bullet) unless the user
   already dictated content — in which case slot it into the right section.
4. Tell the user the path you created and offer to fill it in as the meeting
   goes.

## Template

```
# <Title> — YYYY-MM-DD

> captured YYYY-MM-DD

## Attendees
-

## Agenda
-

## Discussion
-

## Decisions
-

## Action items
- [ ] <owner> — <task>
```

## Notes

- Action items should be checkboxes with an owner so they can later be copied
  into `claude/tasks/tasks.md` if asked.
- Keep it Markdown; this lives alongside the other notes so search works.
