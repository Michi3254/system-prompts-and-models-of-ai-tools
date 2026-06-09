---
title: Citation & Factuality
tags: [prompt-engineering, citation, factuality, search, hallucination]
---

# Citation & Factuality

> [!summary]
> Such-/Antwort-Assistenten erzwingen Quellen mit **mechanisch präzisen** Regeln (Klammer-Index, kein Leerzeichen davor) und steuern Halluzination über Unsicherheits- und Frische-Regeln.

## Zitier-Mechanik

> „You MUST cite search results used directly after each sentence it is used in … Enclose the index of the relevant search result in brackets at the end of the corresponding sentence." — *Perplexity*

- „Do not leave a space between the last word and the citation." — *Perplexity*
- „Cite up to three relevant sources per sentence." — *Perplexity*
- „Each index should be enclosed in its own brackets and never include multiple indices in a single bracket group." — *Perplexity*

## Anti-Halluzination

- „ALWAYS acknowledge uncertainty when present." — *Cluely*
- „Never answer from memory if internal info could change the answer; do a quick default search first." — *Notion AI*
- „…do not produce copyrighted material verbatim." — *Perplexity*

## Such-Strategie (effizient)

- **Sofort suchen, nicht fragen:** „Immediately call a tool if the request can be resolved with a tool call. Do not ask permission to use tools." — *Notion AI*
- **2-Suchen-Limit:** „Avoid conducting more than two back-to-back searches for the same information … the third attempt is unlikely to find anything useful." — *Notion AI*
- **Großzügig suchen:** „Use searches liberally. It's cheap, safe, and fast." — *Notion AI*

## Frische / Datum

> „Remember that the current date is: Tuesday, May 13, 2025…" — *Perplexity*  → siehe [[Context & Memory Handling]]

> [!tip] Übertragbares Prinzip
> Zitierregeln **mechanisch** machen (genaues Format). Halluzination per „erst suchen, dann antworten" + „Unsicherheit benennen" reduzieren. Such-Budget deckeln (z. B. max 2 Wiederholungen).

## Verwandt
- [[Safety, Refusals & Prompt Injection]]
- [[Context & Memory Handling]]
- [[00 - Index (MOC)]]
