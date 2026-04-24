# Copilot Instructions

This is an **Obsidian vault** for an ATE (Automated Test Equipment) engineer at Analog Devices, Inc. It contains two vaults:

- `Seng-Work/` — work notes (ATE devices, test patterns, projects, daily logs)
- `Seng/` — personal notes (courses, data science)

## Vault Structure (`Seng-Work/`)

| Folder | Purpose |
|---|---|
| `DAILY/YYYY/Month/` | Daily notes, named `YYYY-MM-DD.md` |
| `DEVICES/<device>/` | Per-device notes (Atlanta, Goldengate, Omnibus) |
| `LEARNINGS/` | Study notes (SystemVerilog, etc.) |
| `PROGRAMMING/` | Reference notes for Python, Git, SVN, Linux |
| `PROJECTS/<name>/` | Project docs: `About.md`, `ChangeLogs.md`, `Plans and To-do.md`, `Scrap Notes.md` |
| `TESTERS/` | Tester-specific notes (SPEA DOT400s) |
| `TESTS/` | Test pattern and protocol references |
| `WORK HOW TOs/` | Step-by-step how-to guides |
| `zzzzz.templates/` | Core Obsidian templates using `{{date:YYYY-MM-DD}}` syntax |
| `zzzzz.templaters/` | Templater plugin templates using `<% tp.date.now("YYYY-MM-DD") %>` syntax |

The `zzzzz.*` prefix sorts these utility folders to the bottom of the file tree.

## Plugins

- **obsidian-git** — automatic Git sync of vault
- **templater-obsidian** — advanced templates; folder template for `zzzzz.templaters/` auto-applies `insert-date-debug-status.md` on file creation
- **code-emitter** — execute code blocks inline

## Note Conventions

### Bullet/Checkbox Types (Things theme)
Notes use semantic checkbox markers from the Things theme:

| Marker | Meaning |
|---|---|
| `- [ ]` | To-do |
| `- [x]` | Done |
| `- [/]` | In progress / incomplete |
| `- [-]` | Cancelled |
| `- [>]` | Forwarded |
| `- [?]` | Question |
| `- [!]` | Important |
| `- [i]` | Information / note |
| `- [I]` | Idea |
| `- [p]` / `- [c]` | Pros / Cons |

### Tags
Tags use `/`-separated hierarchies:
- `#device/omnibus`, `#device/goldengate`, `#device/atlanta`
- `#link/work`, `#link/work/goldengate/confluence`
- `#mail/work`
- `#ssh`

### Daily Notes
Stored at `DAILY/YYYY/Month/YYYY-MM-DD.md`. Entries are bullet lists grouped by device or topic.

### Changelog Entries
Use the Templater template `insert-date-changelog.md` which formats entries as:
```
1. v1.0.0 (2026-01-01):
```

### Debug Status Entries
Use the Templater template `insert-date-debug-status.md` which embeds a hidden inline data span:
```html
<span style="display: none">(status::{"date":"2026-01-01", "result": "PASS"})</span>
```

### Inline Links
Internal links use `[[WikiLink]]` syntax. External links (Confluence, HLM, ADMAP, etc.) are labeled with their system name followed by a `#link/...` tag.

## `.gitignore`
The repo ignores `workspace*.json`, `.obsidian/cache`, and `.DS_Store` — Obsidian config files that track window state are intentionally excluded.
