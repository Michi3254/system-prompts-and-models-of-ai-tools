---
title: Formatting & Output Rules
tags: [prompt-engineering, formatting, markdown, output]
---

# Formatting & Output Rules

> [!summary]
> Format wird *präzise* vorgeschrieben — bis hin zu „kein einzelner Listenpunkt" und „Level-2-Header statt Level-1". Diese Mikro-Regeln machen Output gleichmäßig und skimmbar.

## Markdown-Struktur

- **Header-Hierarchie:** „Use Level 2 headers (`##`) for sections. If necessary, use bolded text (`**`) for subsections." — *Perplexity*  (nie `#` / H1 — auch *Cursor*)
- **Nicht mit Header starten:** „NEVER start the answer with a header." — *Perplexity*
- **Backticks** für `Dateinamen`, `Funktionen`, `Verzeichnisse` — *Cursor, Trae, Orchids, Lovable*
- **Nicht die ganze Nachricht** in einen Code-Block wickeln — *Cursor*

## Listen-Regeln

- „Avoid nesting lists, instead create a markdown **table**." — *Perplexity*
- „Prefer unordered lists. Only use ordered lists when presenting **ranks**." — *Perplexity*
- „**NEVER** have a list with only one single solitary bullet." — *Perplexity*

## Länge

Siehe [[Communication Style Rules]] — harte Zeilen-/Wortgrenzen statt „be concise".

## Mathematik

> „All math must be rendered using LaTeX: `$…$` for in-line and `$$…$$` for multi-line. … Never use unicode to render math expressions, ALWAYS use LaTeX." — *Perplexity*

## Query-Typ-spezifisches Format (clever)

Perplexity definiert >10 Query-Typen mit je eigenen Format-Regeln, z. B.:

> „Academic Research: provide long and detailed answers … formatted as a scientific write-up, with paragraphs and sections, using markdown and headings." — *Perplexity*

> [!tip] Übertragbares Prinzip
> Format-Regeln so **konkret** wie möglich (Header-Level, Tabelle statt Nest-Liste, keine 1-Item-Liste). Optional: Output-Format an den **Query-Typ** koppeln.

## Verwandt
- [[Communication Style Rules]]
- [[Citation & Factuality]]
- [[00 - Index (MOC)]]
