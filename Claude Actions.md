---
type: Reference
---
#claude-session
## Claude Actions

Open action points across every Claude project in this vault, grouped by project folder. Each project keeps an `<Project> Actions` note at the top of its own folder: [[Finance Actions]], [[Divorce Actions]], [[Personal Actions]], [[Hosting Actions]], [[Mandy Actions]], [[Dylan Actions]] (in `061_Children/Dylan`), and [[Westgate Actions]] (which collects Westgate's to-dos from its topic notes). Tick items here or in the project note: both are the same checkbox. Sessions load their project's list at start and update it at `/close`. Items tagged `#claude-action` stay out of the daily note; Westgate's stay in it. See [[Claude Activity]] for what has been done.

### Urgent: High Priority or due within a Week

```tasks
not done
(tags include #claude-action) OR (path includes 010_Westgate)
(priority is above medium) OR (due before in 7 days)
group by root
sort by due
sort by priority
short mode
```

### All Open, by Project

```tasks
not done
(tags include #claude-action) OR (path includes 010_Westgate)
group by root
group by filename
sort by priority
sort by due
short mode
```

### Done in the Last Two Weeks

```tasks
done
(tags include #claude-action) OR (path includes 010_Westgate)
done after 14 days ago
group by root
sort by done reverse
short mode
```
