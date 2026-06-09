---
title: Tool Schema Design
tags: [tools, schema, function-calling, design]
---

# Tool Schema Design

> [!summary]
> Die Qualität eines Agenten steckt zu großen Teilen in seinen **Tool-Definitionen**. Gute Schemas folgen klaren Mustern bei Naming, Beschreibung und Parametern — besonders wichtig: **wann NICHT** aufrufen.

## Naming
- **Verb-first, snake_case:** `file_read`, `file_write`, `file_str_replace`, `grep_search`, `shell_exec` — *Anthropic, Manus, Windsurf*
- **Namespace per Präfix:** alle Datei-Ops `file_*`, Browser `browser_*`, Shell `shell_*` — *Manus*
- 2–5 Wörter, beschreibend, eindeutig

## Beschreibung — die „Rule of Three"
Jede starke Beschreibung hat:
1. **One-Liner**: was das Tool tut
2. **When to use**: wann es passend ist
3. **When NOT to use**: was es verhindert (der wichtigste Teil!)

> „When NOT to use the Agent tool: If you want to read a specific file path, use Read or Glob instead. If you are searching for a specific class definition, use Glob instead…" — *Anthropic Claude Code (Task-Tool)*

**Eingebettete Beispiele & Vergleich zu Nachbar-Tools:**
> „This performs best when the search query is more precise … Results will be poor if asking a very broad question, such as asking about the general 'framework' …" — *Windsurf (codebase search)*

## Parameter-Design
- **Required minimal halten**, optionales mit `default`
- **Enums** gegen ungültige Calls: `output_mode: ["content","files_with_matches","count"]` — *Anthropic*
- **Pro-Parameter-Guidance** mit Constraints & Beispielen:
> „query: The search query to find relevant code. You should reuse the user's exact query/most recent message with their wording unless there is a clear reason not to." — *Cursor*
- **Constraint-Doku für Performance/Safety:**
> „OutputCharacterCount: … Make this as small as possible to avoid excessive memory usage." — *Windsurf*

## Clevere Schema-Tricks
- **Erzwungene Erklärung:** Bash-Tool verlangt `description` (5–10 Wörter) pro Befehl — *Anthropic*
- **Safety-Gate als Param:** `SafeToAutoRun` / `Blocking` — *Trae* (siehe [[Safety, Refusals & Prompt Injection]])
- **UI-Hinweis als Param:** `toolSummary` zuerst — *Windsurf*
- **Parallel-Hint:** „View up to 3 files simultaneously in batch mode." — *Lovable*
- **Output-Truncation angekündigt:** „If the output exceeds 30000 characters, output will be truncated." — *Anthropic*

> [!example] Gold-Standard-Gerüst
> Siehe [[Tool Schema Template]] für eine kopierfertige Vorlage.

## Verwandt
- [[Common Tools Reference]]
- [[Tool Schema Template]]
- [[Safety, Refusals & Prompt Injection]]
- [[00 - Index (MOC)]]
