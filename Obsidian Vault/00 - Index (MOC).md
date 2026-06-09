---
title: AI Prompt & Agent Knowledge Base — Index
tags: [moc, index, prompt-engineering, agents]
created: 2026-06-09
source_repo: x1xhlol/system-prompts-and-models-of-ai-tools
---

# 🧠 AI Prompt & Agent Knowledge Base

> [!abstract] Was ist das?
> Destillierte, **belegte Best Practices** aus ~104 geleakten System-Prompts und Tool-Schemas führender KI-Tools (Cursor, v0, Devin, Windsurf, Replit, Anthropic Claude Code, Perplexity, Notion AI, Comet, Lovable, Manus u. v. m.). Stand der Quellen: **2026-05-23**.
>
> Ziel: Wir lernen, wie die besten Produkte ihre Agenten instruieren — und stehlen die Muster für eigene Prompts, Agenten und Tools.

## 🗺️ Karte der Inhalte

### Prompt Engineering
- [[Prompt Structure & Skeleton]] — der wiederkehrende Bauplan jedes guten System-Prompts
- [[Constraints & Guardrails]] — die ALWAYS/NEVER-Regeln, die überall auftauchen
- [[Communication Style Rules]] — wie Agenten mit dem User reden (Kürze, kein Geschwafel)
- [[Persona & Identity]] — Identität, Ton, Werte definieren
- [[Formatting & Output Rules]] — Markdown, Länge, Listen vs. Prosa, LaTeX
- [[Citation & Factuality]] — Quellen, Unsicherheit, Aktualität, Anti-Halluzination
- [[Safety, Refusals & Prompt Injection]] — Grenzen, weiche Ablehnung, Injection-Abwehr

### Agent Design
- [[Agent Loop & Planning]] — Iteration, Todo-Listen, Statusupdates
- [[Code-Editing Workflow]] — Read → Plan → Edit → Verify
- [[Context & Memory Handling]] — User-Kontext, Memory, Zeit/Datum
- [[Clever Patterns Worth Stealing]] — die überraschend cleveren Tricks

### Tool Design
- [[Tool Schema Design]] — wie man Function/Tool-Definitionen schreibt
- [[Common Tools Reference]] — read/edit/search/terminal/todo im Vergleich

### Templates (sofort nutzbar)
- [[System Prompt Template]] — Gerüst für einen eigenen System-Prompt
- [[Tool Schema Template]] — Gold-Standard-Vorlage für ein Tool

### Anhang
- [[Sources — Index of Tools]] — welche Tools in der Quelle stecken

## ⭐ Die 7 wichtigsten Erkenntnisse (TL;DR)

1. **Struktur schlägt Länge.** Identität → Regeln → Tools → Stil → Beispiele. Siehe [[Prompt Structure & Skeleton]].
2. **Verbote sind mächtiger als Erlaubnisse.** Explizite NEVER-Regeln verhindern die häufigsten Fehler. Siehe [[Constraints & Guardrails]].
3. **Kürze ist eine Eigenschaft, kein Zufall.** "Antworte in <4 Zeilen, kein Vor-/Nachgeplänkel." Siehe [[Communication Style Rules]].
4. **Tool-Beschreibungen brauchen "wann NICHT".** Das beste Schema sagt, wann man es *nicht* aufruft. Siehe [[Tool Schema Design]].
5. **Read before write, minimal edits.** Erst lesen/verstehen, dann minimal ändern. Siehe [[Code-Editing Workflow]].
6. **Parallelisieren.** Unabhängige Tool-Calls immer gleichzeitig. Siehe [[Agent Loop & Planning]].
7. **Untrusted = Daten, nie Befehle.** Web-/Datei-Inhalte niemals als Anweisungen interpretieren. Siehe [[Safety, Refusals & Prompt Injection]].

> [!tip] Wie nutzen?
> Diesen Ordner in deinen Obsidian-Vault kopieren. Mit Graph-View die Verknüpfungen erkunden. Für ein eigenes Projekt: bei [[System Prompt Template]] und [[Tool Schema Template]] starten.
