# Obsidian Work Template

This vault is a lightweight work dashboard for Obsidian. It is set up to help you manage daily work notes, meeting notes, follow-up items, and open tasks from a single place.

## What is in this vault

- `Work.md` - the main work homepage
- `Meetings.md` - the meetings homepage
- `Daily/` - where daily notes are created
- `Inbox/` - where temporary notes are captured
- `Notes/` - where durable notes are stored
- `Archive/` - where archived notes are kept but not actively worked
- `Meetings/` - where individual meeting notes are created
- `Templates/` - note templates used by Obsidian
- `Bases/` - Obsidian Bases definitions for structured views over your notes
- `.obsidian/` - plugin and vault configuration

## How it works

This vault combines four Obsidian features:

1. Daily Notes
2. Templates
3. Bases
4. Workspaces
5. The community `Tasks` plugin

The workflow is:

- create a daily note for the current day
- capture quick notes in `Inbox/` for temporary information
- move durable information into `Notes/` when it should be kept
- move inactive but useful notes into `Archive/`
- capture tasks and notes in that note
- create separate meeting notes when needed
- track unfinished work through Tasks queries
- review notes through Bases views that use frontmatter properties such as `type`, `status`, and `follow_up`

## Main pages

### `Work.md`

Use `Work.md` as the main entry point for your workday.

It includes:

- links to the daily notes area and templates
- links to the inbox dashboard, folder, template, and base
- links to the notes and archive areas
- links to the meetings area
- an open tasks query for notes inside `Daily/`
- a meeting actions query for notes inside `Meetings/`
- a grouped follow-up view for daily notes

Suggested daily routine:

1. Run Obsidian's command to open today's daily note.
2. Add work items under `Today's tasks`.
3. Add notes during the day.
4. At the end of the day, update `status` and `follow_up`.

Quick folder guide:

- use `Daily/` for day-specific work logs and tasks
- use `Inbox/` for quick capture and temporary notes
- use `Notes/` for cleaned-up reference notes you expect to revisit
- use `Archive/` for inactive notes you still want to keep

### `Inbox.md`

Use `Inbox.md` as the temporary-notes dashboard.

It includes:

- the expected location for inbox notes
- the inbox template reference
- a task query for open checkbox items inside `Inbox/`
- a link to `Bases/Inbox.base` for reviewing active and archived inbox notes

Suggested inbox routine:

1. Create a new note in `Inbox/`.
2. Apply `Templates/Inbox Note`.
3. Name it with a timestamp first, for example `2026-03-21 1430 - server issue`.
4. Keep only the note you are actively editing open.
5. Review old inbox notes through the base instead of tabs.
6. Delete the note or change `status` when you no longer need it.

### `Notes.md`

Use `Notes.md` as the durable-notes dashboard.

It includes:

- the expected location for long-lived notes
- the note template reference
- a task query for open checkbox items inside `Notes/`
- a link to `Bases/Notes.base` for reviewing active and archived notes

Suggested notes routine:

1. Create a new note in `Notes/`.
2. Apply `Templates/Note`.
3. Move cleaned-up information there from `Inbox/`, `Daily/`, or `Meetings/`.
4. Keep reusable decisions, references, and write-ups there.

### `Archive.md`

Use `Archive.md` as the archive dashboard.

It includes:

- the expected location for archived durable notes
- a review query for notes inside `Archive/`
- a link to `Bases/Archive.base` for browsing archived notes

Suggested archive routine:

1. Keep active notes in `Notes/`.
2. When a note is no longer active, change `status` to `archived`.
3. Move it into `Archive/`.
4. Review older notes there only when you need them.

### `Meetings.md`

Use `Meetings.md` as the meeting dashboard.

It includes:

- the expected location for meeting notes
- the meeting template reference
- a task query for open meeting action items
- a grouped task view by meeting note

## Templates

### `Templates/Daily Note.md`

This template creates daily notes with frontmatter like:

- `type: daily`
- `date`
- `status: open`
- `follow_up: false`

It also gives you sections for:

- open tasks
- today's tasks
- notes
- end of day review

At the end of the day:

- set `status` to `closed` when the day is complete
- set `follow_up: true` if there is unfinished work to revisit

### `Templates/Meeting Note.md`

This template creates one note per meeting and includes frontmatter like:

- `type: meeting`
- `date`
- `status: open`
- `follow_up: false`
- `people`
- `project`
- `team`
- `topic`
- `next_step`

It also includes sections for:

- context
- agenda
- notes
- decisions
- action items
- follow-up

Recommended naming format:

- `YYYY-MM-DD Team Sync`
- examples: `2026-03-20 Team Sync`, `2026-03-20 1:1 Manager`, `2026-03-20 Sprint Retro`

### `Templates/Inbox Note.md`

This template creates temporary notes with frontmatter like:

- `type: inbox`
- `created`
- `status: active`
- `topic`
- `promote_to`

It also gives you sections for:

- context
- notes
- actions
- promote to notes
- decision on whether to keep, archive, or delete the note

## Bases

The files in `Bases/` create structured table views over your notes.

### `Bases/Work days.base`

This Base includes notes that:

- are Markdown files
- are inside `Daily/`
- have `type: daily`

It provides views such as:

- Recent
- Last 7 days
- Last 30 days
- With follow-up
- Follow-up + Open
- Open
- Closed
- This year

### `Bases/Meetings.base`

This Base includes notes that:

- are Markdown files
- are inside `Meetings/`
- have `type: meeting`

It provides views such as:

- Recent
- Follow-up
- Open
- Last 30 days
- This year
- By project
- By team

### `Templates/Note.md`

This template creates durable notes with frontmatter like:

- `type: note`
- `created`
- `status: active`
- `area`
- `source`

It also gives you sections for:

- context
- key points
- details
- decisions
- related information
- next review
- archive trigger

### `Bases/Inbox.base`

This Base includes notes that:

- are Markdown files
- are inside `Inbox/`
- have `type: inbox`

It provides views such as:

- Recent
- Active
- Archived
- Created today

### `Bases/Notes.base`

This Base includes notes that:

- are Markdown files
- are inside `Notes/`
- have `type: note`
- do not have `status: archived`

It provides views such as:

- Recent
- Active
- By area

### `Bases/Archive.base`

This Base includes notes that:

- are Markdown files
- are inside `Archive/`
- have `status: archived`

It provides views such as:

- Recent
- By type
- By area

## Tasks plugin usage

This vault uses the community plugin `obsidian-tasks-plugin` to collect checkbox items across notes.

That means any checkbox like this can show up in dashboard queries:

```md
- [ ] Prepare status update
```

The plugin is configured with basic statuses including:

- todo: `[ ]`
- in progress: `[/]`
- done: `[x]`
- cancelled: `[-]`

The dashboards in `Work.md`, `Meetings.md`, and the templates use Tasks queries to show unfinished items automatically.

## Required setup in Obsidian

This vault is already configured to use:

- core plugin: Daily Notes
- core plugin: Templates
- core plugin: Bases
- core plugin: Workspaces
- community plugin: Tasks

Daily Notes is configured to:

- create notes in `Daily/`
- use the format `YYYY-MM-DD`
- apply `Templates/Daily Note`

Templates is configured to use:

- `Templates/`

## How to use the vault

### Daily workflow

1. Open `Work.md`.
2. Run `Open today's daily note` in Obsidian.
3. Add tasks under `Today's tasks`.
4. Keep notes in the same daily note as the day progresses.
5. Close or update tasks as work changes.
6. At the end of the day, review `status` and `follow_up`.

### Meeting workflow

1. Open `Meetings.md`.
2. Create a new note in `Meetings/` using `Templates/Meeting Note`.
3. Name it with the date-first convention.
4. Fill in properties like `project`, `team`, or `topic`.
5. Record decisions and action items in the same note.
6. Set `follow_up: true` if more work is needed later.

### Inbox workflow

1. Open `Inbox.md`.
2. Create a new note in `Inbox/`.
3. Apply `Templates/Inbox Note`.
4. Name it `YYYY-MM-DD HHmm - topic`.
5. Keep only the current inbox note open.
6. Review or clean up old inbox notes through `Bases/Inbox.base`.

### Notes workflow

1. Open `Notes.md`.
2. Create a new note in `Notes/`.
3. Apply `Templates/Note`.
4. Move durable information there after it is worth keeping.
5. Review long-lived notes through `Bases/Notes.base`.

### Archive workflow

1. Open `Archive.md` when you want to review archived notes.
2. Change a note to `status: archived` when it is no longer active.
3. Move the note into `Archive/`.
4. Keep the archive for retrieval, not active work.

## Tips

- Keep daily work in `Daily/` and meeting notes in `Meetings/` so Bases and task queries stay accurate.
- Keep temporary information in `Inbox/` so you do not need to keep many tabs open.
- Keep durable information in `Notes/` once it is worth preserving.
- Keep inactive but useful notes in `Archive/` so active areas stay lighter.
- Do not remove the `type` property from notes created from templates; Bases rely on it.
- Use `follow_up` to mark notes that still need attention.
- Use `status` consistently, especially `open` and `closed`, so filtered views remain useful.

## Getting started

If you open this vault on a new Obsidian install:

1. Enable community plugins if they are disabled.
2. Confirm the `Tasks` plugin is installed and enabled.
3. Open `Work.md` to start from the main dashboard.
4. Create your first daily note.
5. Create inbox notes as needed in `Inbox/`.
6. Create persistent notes as needed in `Notes/`.
7. Move inactive notes into `Archive/` when they are still worth keeping.
8. Create meeting notes as needed in `Meetings/`.

Once you start adding notes, the Tasks queries and Bases views will begin filling in automatically.
