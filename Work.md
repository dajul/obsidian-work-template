---
type: index
area: work
TQ_short_mode: true
TQ_show_backlink: true
TQ_show_task_count: true
---

# Work

- Daily folder: [[Daily]]
- Tracking base: [[Bases/Work days.base]]
- Daily template: [[Templates/Daily Note]]
- Inbox dashboard: [[Inbox]]
- Inbox folder: [[Inbox]]
- Inbox base: [[Bases/Inbox.base]]
- Inbox template: [[Templates/Inbox Note]]
- Notes dashboard: [[Notes]]
- Notes folder: [[Notes]]
- Notes base: [[Bases/Notes.base]]
- Notes template: [[Templates/Note]]
- Archive dashboard: [[Archive]]
- Archive folder: [[Archive]]
- Archive base: [[Bases/Archive.base]]
- Meetings folder: [[Meetings]]
- Meetings dashboard: [[Meetings]]
- Meetings base: [[Bases/Meetings.base]]

## Daily use

1. Run `Open today's daily note`
2. Add tasks under `Today's tasks`
3. Update `status` and `follow_up` at the end of the day

## Where things go

- `Daily/`: today-specific work, notes, and tasks
- `Inbox/`: quick capture, rough notes, and temporary material
- `Notes/`: cleaned-up reference notes you expect to revisit
- `Archive/`: inactive notes you want to keep but not actively browse

## Meeting note naming

- Use `YYYY-MM-DD Team Sync`
- Examples: `2026-03-20 Team Sync`, `2026-03-20 1:1 Manager`, `2026-03-20 Sprint Retro`

## Inbox capture

1. Create a new note in `Inbox/`
2. Use `Templates/Inbox Note`
3. Name it `YYYY-MM-DD HHmm - topic`
4. Keep only the current note open and find the rest through `[[Bases/Inbox.base]]`

## Persistent notes

1. Create a new note in `Notes/`
2. Use `Templates/Note`
3. Keep cleaned-up, durable information there
4. Review and organize notes through `[[Bases/Notes.base]]`

## Inbox to Notes workflow

1. Capture rough ideas, links, and temporary tasks in `Inbox/`
2. Review the note once the information is worth keeping
3. Move the useful parts into a note in `Notes/`
4. Keep only the durable version in `Notes/` and archive or delete the inbox note

## Notes to Archive workflow

1. Keep active reference notes in `Notes/`
2. When a note is no longer active but still worth keeping, change `status` to `archived`
3. Move the file into `Archive/`
4. Review archived notes through `[[Archive]]` and `[[Bases/Archive.base]]`

## Active inbox tasks

```tasks
not done
path includes Inbox
sort by scheduled
sort by due
sort by priority
```

## Open tasks

```tasks
not done
path includes Daily
sort by scheduled
sort by due
sort by priority
```

## Meeting actions

```tasks
not done
path includes Meetings
sort by scheduled
sort by due
sort by priority
```

## Days with follow-up

```tasks
not done
path includes Daily
group by filename
sort by path
```
