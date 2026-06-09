---
title: Communication Style Rules
tags: [prompt-engineering, communication, tone, conciseness]
---

# Communication Style Rules

> [!summary]
> Kürze ist kein Zufall, sondern eine **hart kodierte Eigenschaft**. Fast jeder Top-Prompt schreibt eine konkrete Längenobergrenze vor und verbietet Vor-/Nachgeplänkel.

## Konkrete Längen-Regeln (zum Klauen)

- **Anthropic Claude Code:** „You MUST answer concisely with **fewer than 4 lines** (not including tool use or code generation), unless user asks for detail."
- **Lovable:** „You MUST answer concisely with **fewer than 2 lines** of text … unless user asks for detail."
- **Orchids:** „State what you're doing in **1-2 sentences max**, then do it."
- **Emergent:** Crisp summaries **<100 words**.

## Kein Vor-/Nachgeplänkel

> „You MUST avoid text before/after your response, such as 'The answer is <answer>.', 'Here is the content of the file…' or 'Based on the information provided, the answer is…'" — *Anthropic Claude Code*

> „NEVER start the answer with a header. NEVER start by explaining to the user what you are doing." — *Perplexity*

## Kein Dauer-Entschuldigen

> „Refrain from apologizing all the time when results are unexpected. Instead, just try your best to proceed or explain the circumstances … without apologizing." — *Lovable / Orchids / Trae*

## Keine Meta-Phrasen

> „NEVER use meta-phrases (e.g., 'let me help you', 'I can see that')." — *Cluely*

## Ton & Wärme (für Assistenten)

> „When speaking, be witty and warm, though never overdo it … sound like a friend … never be sycophantic." — *Poke*

## Markdown nur wo sinnvoll

> „Avoid wrapping the entire message in a single code block. Use Markdown **only where semantically correct** (e.g. `inline code`, code fences, lists, tables)." — *Cursor*

> [!tip] Übertragbares Prinzip
> Gib eine **harte Zahl** (Zeilen/Wörter) statt „be concise". Verbiete explizit Preamble/Postamble und Entschuldigungs-Floskeln.

## Verwandt
- [[Formatting & Output Rules]]
- [[Persona & Identity]]
- [[00 - Index (MOC)]]
