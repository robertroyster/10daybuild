# notes/ — notes (replaces Google Keep / Docs)

Every note is its own Markdown file in this folder. This covers both quick
captures (the Keep slot) and longer structured notes (the Docs slot).

## Rules

- One note per file. Name files `kebab-case-from-the-topic.md` — pick a sensible
  name from the content; don't make the user supply one.
- When the user pastes messy text and asks you to "organize" or "clean up" a
  note, give it real structure: a top-level `# Heading`, sub-headings, and
  bullet lists where they fit. Don't change the meaning.
- For quick captures, don't over-format — a heading and the text is enough.
- Add a `> captured YYYY-MM-DD` line under the title so notes are sortable by
  when they were taken.
- Searching: to answer "what did I write about X?", read across the files here
  and return the relevant note (or a short summary), not a list of filenames.
- Never delete a note unless explicitly asked.
