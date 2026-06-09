---
title: Prompt Structure & Skeleton
tags: [prompt-engineering, structure, template]
---

# Prompt Structure & Skeleton

> [!summary]
> Quer durch alle untersuchten Coding-Agenten (Cursor, Windsurf, Devin, v0, Lovable, Orchids …) ist derselbe Bauplan erkennbar. Reihenfolge ist kein Zufall — sie spiegelt Priorität: zuerst *wer bin ich*, dann *was darf ich nicht*, dann *womit arbeite ich*.

## Das Standard-Skelett

1. **Identität / Rolle** — „You are X, an AI coding assistant…"
2. **Kernprinzipien** — Kommunikations- & Verhaltensregeln (oben, weil global)
3. **Capabilities-Scope** — was der Agent kann/**nicht** kann (Sprachen, Frameworks, Tools)
4. **Tool-Guidelines** — wann/wie Tools aufrufen (Parallelisierung, Schema-Treue)
5. **Code-Modification-Rules** — read-before-edit, testen, große Dateien, nichts kaputt machen
6. **Communication-Style** — Kürze, Markdown, Backticks für Code-Referenzen
7. **Task-Completion-Patterns** — Todo-Listen, Statusupdates, Abschluss-Summary
8. **Examples** — gute vs. schlechte Vorgehensweisen (Few-Shot)

## Warum diese Reihenfolge?

- **Globales zuerst:** Kommunikations- und Sicherheitsregeln stehen weit oben, damit sie alles Spätere überschreiben.
- **Negativ-Scope früh:** Was der Agent *nicht* tun soll, kommt vor den Tools — verhindert Fehlgriffe.
- **Beispiele zuletzt:** Few-Shot-Beispiele verankern den Stil, nachdem die Regeln gesetzt sind.

## Belegende Beobachtung

> „If the user wants you to implement a feature and they have not specified the files to edit, first break down the user's request into smaller concepts." — *Cursor, Agent Prompt 2025-09-03*

## Verwandt
- [[Constraints & Guardrails]]
- [[Communication Style Rules]]
- [[System Prompt Template]]
- [[00 - Index (MOC)]]
