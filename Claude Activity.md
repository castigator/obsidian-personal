---
type: Reference
---
#claude-session
## Claude Activity

Which Claude project and session wrote what in this vault. Notes Claude creates or edits carry `claude_project` (the project folder that created them) and `claude_sessions` (links to the session notes in `Claude/Sessions/`). Each session note says what the session did, how to resume it, and lists the notes it touched. Everything below updates itself (Dataview).

### Recent Work

The ten most recently active sessions and what each one did (the "What this session did" list in each session note).

```dataview
TABLE WITHOUT ID
  file.link AS "Session",
  regexreplace(claude_project, "^.*/", "") AS "Project",
  last_active AS "Last active",
  filter(file.lists, (l) => contains(lower(meta(l.section).subpath), "what this session did")).text AS "What was done"
FROM "Claude/Sessions"
SORT last_active DESC, file.name DESC
LIMIT 10
```

### Projects, Most Recently Active First

```dataview
TABLE WITHOUT ID
  claude_project AS "Project",
  max(rows.last_active) AS "Last active",
  length(rows) AS "Sessions"
FROM "Claude/Sessions"
GROUP BY claude_project
SORT max(rows.last_active) DESC
```

### Sessions, Most Recent First

```dataview
TABLE WITHOUT ID
  file.link AS "Session",
  claude_project AS "Project",
  started AS "Started",
  last_active AS "Last active",
  resume AS "Resume"
FROM "Claude/Sessions"
SORT last_active DESC, file.name DESC
```

### Notes Written by Claude, Most Recently Changed First

```dataview
TABLE WITHOUT ID
  file.link AS "Note",
  claude_sessions AS "Sessions",
  file.mtime AS "Changed"
FROM ""
WHERE claude_project AND type != "Claude Session"
SORT file.mtime DESC
LIMIT 100
```
