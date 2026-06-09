---
title: Clever Patterns Worth Stealing
tags: [agents, patterns, tricks, ideas]
---

# Clever Patterns Worth Stealing

> [!summary]
> Die überraschend cleveren Muster — Dinge, die man nicht erwartet, aber sofort übernehmen will.

## 1. `toolSummary` für UI-Sichtbarkeit
Jeder Tool-Call trägt eine 2–5-Wort-Zusammenfassung („analyzing directory", „editing file"), die live in der UI erscheint. Muss als **erstes** Argument kommen. — *Windsurf, v0*

## 2. Discussion-First-Modus
Default = planen/besprechen; **nur** bei expliziten Aktionswörtern („implement", „create", „add") wird gebaut. Verhindert Scope-Creep. — *Lovable, Orchids*

## 3. „Know when to stop"
> „The moment the user's request is correctly and completely fulfilled, stop." — *Orchids*
Keine ungefragten Optimierungen/Refactors/Politur.

## 4. Sub-Agent-Delegation für Risiko-Domänen
Kern-Agent fasst `src/db/schema.ts` oder Auth nie direkt an → delegiert an `use_database_agent` / `use_auth_agent`. Weniger Fehler. — *Orchids*

## 5. Explanation-after-the-fact
Tool aufrufen, **ohne** den Code vorher im Chat zu zeigen — das Tool wendet die Änderung an und zeigt sie. Spart Tokens. — *Orchids*

## 6. Absichtliche Stille
> „At the end of a conversation, you can react or output an empty string to say nothing when natural." — *Poke*

## 7. Konfidenz-Schwellen für mehrdeutige Eingaben
> „If you're 50%+ confident someone is asking something at the end, treat it as a question and answer it." — *Cluely* (für fehlerhafte Live-Transkripte)

## 8. Aufgaben-Prioritätshierarchie
Cluely Enterprise: Frage beantworten > Begriff definieren > Gespräch voranbringen > Einwand behandeln > Bildschirmproblem > Passiv-Modus.

## 9. Erzwungene Befehls-Erklärung
Das Bash-Tool verlangt eine 5–10-Wort-Beschreibung **pro Befehl** als Parameter → bessere Nachvollziehbarkeit. — *Anthropic Claude Code* (siehe [[Tool Schema Design]])

## 10. Ästhetik als harte Anforderung
> „The USER should be wowed at first glance … Failure to do this is UNACCEPTABLE." — *Google Antigravity*
Emotionale, absolute Sprache, um Qualitätslatte zu setzen.

> [!tip] Übertragbares Prinzip
> Viele dieser Tricks kosten 1–2 Sätze im Prompt, heben aber UX/Qualität/Effizienz spürbar. Kandidaten für jedes eigene Agenten-Design.

## Verwandt
- [[Agent Loop & Planning]]
- [[Tool Schema Design]]
- [[00 - Index (MOC)]]
