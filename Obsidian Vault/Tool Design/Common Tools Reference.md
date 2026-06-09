---
title: Common Tools Reference
tags: [tools, reference, read, edit, search, terminal, todo]
---

# Common Tools Reference

> [!summary]
> Dieselben ~6 Tools tauchen in fast jedem Produkt auf — aber mit lehrreichen Designunterschieden. Referenz für eigene Tool-Suites.

## 📖 Read File
| Tool | Ansatz |
|---|---|
| Anthropic | simpel: `file_path` + optional `offset`/`limit` (default 2000 Zeilen) |
| Cursor | **query-getrieben**: `query` „what you're looking for" → AI liefert relevante Chunks |
| Same.dev | präzise Zeilen: `start_line_one_indexed` … (default erste 500) |

→ Bei großen Dateien gewinnt **query-getrieben / Zeilenbereich** gegen Volltext.

## ✏️ Edit File — drei Schulen
- **A) String-Replace (diff):** `old_str`/`new_str` — *Manus*; mehrere Chunks pro Call — *Windsurf `ReplacementChunks`*
- **B) Full-File-Overwrite:** ganze Datei <1000 LOC neu — *Same.dev*
- **C) Chunked structured:** `TargetContent`/`ReplacementContent`/`AllowMultiple` — *Trae*

> „Do NOT try to replace the entire existing content with the new content, this is very expensive." — *Windsurf*

→ Default sollte **diff-basiert** sein (siehe [[Code-Editing Workflow]]).

## 🔎 Search / Grep
- **Output-Modi:** `content` | `files_with_matches` | `count` — *Anthropic*
- **Kontextfenster:** `context_lines_before/after` — *Windsurf*
- **Multiline:** „use `multiline: true`" für zeilenübergreifende Pattern — *Lovable*
- Best practice: **erst semantische Suche, dann grep** für Exaktheit

## 💻 Terminal / Shell
- Session-Modell: `id`, `exec_dir` (absoluter Pfad), `command` — *Manus*
- **Safety-Gate:** `SafeToAutoRun` (nie true bei Zweifel) — *Trae*
- **Blocking-Steuerung:** `Blocking`/`is_background` für lange Prozesse — *Trae/Windsurf*

## ✅ Todo / Planning
- `status`-Enum: `pending` | `in_progress` | `completed` — *Anthropic, Lovable*
- **Wann nutzen:** ≥3 Schritte, komplex, mehrere Tasks
- **Wann NICHT:** Single-Step, trivial, rein konversationell — *Replit*
- Milestone-Tasks, nicht Mikroschritte; „NO vague tasks" (kein „Polish/Test/Finalize") — *Lovable*

## 🤖 Sub-Agent / Task
- `Task` mit `subagent_type` startet spezialisierte Agenten — *Anthropic*
- Delegation von Risiko-Domänen (DB/Auth) → siehe [[Clever Patterns Worth Stealing]]

## Verwandt
- [[Tool Schema Design]]
- [[Code-Editing Workflow]]
- [[Agent Loop & Planning]]
- [[00 - Index (MOC)]]
