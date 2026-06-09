---
title: Constraints & Guardrails
tags: [prompt-engineering, constraints, guardrails, rules]
---

# Constraints & Guardrails

> [!summary]
> Die wertvollste Erkenntnis: **Verbote sind mächtiger als Erlaubnisse.** Die besten Prompts bestehen zu großen Teilen aus expliziten `NEVER`/`ALWAYS`-Regeln, die genau die häufigsten Fehlermodi abfangen.

## Wiederkehrende NEVER-Regeln

- **Nie Code an den User ausgeben**, statt das Edit-Tool zu nutzen *(Devin, Windsurf, Trae, Orchids)*
- **Nie annehmen, dass eine Library verfügbar ist** — erst `package.json` prüfen *(Devin, Trae)*
- **Nie `grep`/`find` in der Shell** — dedizierte Such-Tools nutzen *(Devin, VSCode Agent)*
- **Nie Dateien ändern, ohne sie vorher zu lesen** *(Orchids, Replit, Trae)*
- **Nie um Erlaubnis fragen für sichere Operationen** — aus Kontext schließen *(Windsurf)*
- **Nie Secrets committen / API-Keys hardcoden** *(Devin, Trae)*
- **Nie Tests/Linting überspringen**, außer der User will es *(Cursor, Devin)*
- **Nie das Scope überschreiten** — „Never modify a user's content unless explicitly asked" *(Notion AI)*

## Wiederkehrende ALWAYS-Regeln

- **Immer alle Imports/Dependencies** ergänzen, bevor Code läuft *(Windsurf, Cursor, Replit)*
- **Immer dem Tool-Schema exakt folgen**, alle Pflichtparameter liefern *(alle)*
- **Immer Backticks** für Dateinamen, Funktionen, Verzeichnisse *(Cursor, Trae, Orchids, Lovable)*
- **Immer Kontext-Dateien zuerst prüfen** — „NEVER read files already in context" *(Lovable)*
- **Immer unabhängige Reads/Searches parallelisieren** *(Cursor, Windsurf, Orchids)*
- **Immer das Todo aktualisieren**, bevor man Arbeit als erledigt meldet *(Cursor)*

## Technik: Negativ-Beispiele als Guardrail

Statt nur zu sagen *was* zu tun ist, geben starke Prompts ein Anti-Beispiel:

> „When user asks you to think, brainstorm, talk through, analyze, or review, DO NOT edit pages or databases directly. Respond in chat only unless user explicitly asked to apply, add, or insert content." — *Notion AI*

> [!tip] Übertragbares Prinzip
> Für jeden bekannten Fehlerfall deines Agenten → **eine explizite NEVER-Regel + ein Anti-Beispiel**. Das ist effektiver als generische Qualitätsappelle.

## Verwandt
- [[Prompt Structure & Skeleton]]
- [[Code-Editing Workflow]]
- [[Safety, Refusals & Prompt Injection]]
- [[00 - Index (MOC)]]
