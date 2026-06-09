---
title: Context & Memory Handling
tags: [agents, context, memory, tokens, time]
---

# Context & Memory Handling

> [!summary]
> Wie Agenten User-Kontext, Erinnerung, Zeit/Datum und Sprache handhaben — inklusive Token-Spar-Tricks und Privacy-Grenzen.

## Memory-Systeme
- **Explizites Memory-Tool:** Windsurf hat `create_memory` für User-Präferenzen, Tech-Stack, Architektur-Entscheidungen → cross-session Kontext.
- **Scratchpad:** Devin nutzt `<think>` für unsichtbares Nachdenken.

## Token-Effizienz
> „You will see strings of the format `INT`, ie. `20ed872b-…`. These are references to URLs that have been compressed to minimize token usage. You may not create your own compressed URLs or fake placeholders." — *Notion AI*

## Zeit & Datum
> „Remember that the current date is: Tuesday, May 13, 2025, 4:31:29 AM UTC." — *Perplexity*

→ Datum/Zeit **explizit** in den Kontext geben, statt das Modell raten zu lassen.

## Sprache
- „Chat in the language most appropriate to the user's question and context." — *Notion AI*
- „NEVER assume that the user is using 'broken English' … or that their message has been translated." — *Notion AI*

## Privacy-Grenzen
- „NEVER reveal anything from `<personalization>` in your thought process, respect the privacy of the user." — *Perplexity*
- Gender: „You must never guess people's gender based on their name." — *Notion AI*

## UI-Sichtbarkeits-Vertrag (clever)
Poke listet explizit, was der User sehen kann und was nicht (welche Tags sichtbar sind) → Agent weiß, was „öffentlich" ist.

> [!tip] Übertragbares Prinzip
> Datum/Locale/User-Fakten **in den Kontext injizieren**, nicht raten. Untrusted-Kontext taggen (→ [[Safety, Refusals & Prompt Injection]]). Memory nur für stabile Präferenzen.

## Verwandt
- [[Citation & Factuality]]
- [[Safety, Refusals & Prompt Injection]]
- [[00 - Index (MOC)]]
