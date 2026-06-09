---
title: Agent Loop & Planning
tags: [agents, agent-loop, planning, todo, parallelization]
---

# Agent Loop & Planning

> [!summary]
> Agenten laufen in einer Schleife: **analysieren → Tool wählen → beobachten → iterieren → abschließen**. Fortschritt wird über Todo-Listen und kurze Statusupdates sichtbar gemacht. Unabhängige Tool-Calls laufen **parallel**.

## Die Schleife (Manus, kanonisch)

1. **Analyze Events** — User-Bedarf + aktuellen Zustand verstehen
2. **Select Tools** — nächsten Tool-Call wählen
3. **Wait for Execution** — Ergebnis abwarten
4. **Iterate** — nur **ein** Tool-Call pro Iteration, wiederholen
5. **Submit Results** — Ergebnis + Deliverables liefern
6. **Enter Standby** — in Leerlauf gehen, wenn fertig

## Todo-Lifecycle (Cursor, Lovable, Replit)

- Atomare Tasks **vorab** anlegen (verb-geführt, kurz)
- Status sofort aktualisieren; **nur ein** `in_progress` zugleich
- Mit `merge=true` updaten statt ersetzen
- Mit **Abschluss-Summary** schließen

> „Before starting any new file or code edit, reconcile the todo list: mark newly completed items as completed and set the next task to in_progress." — *Cursor*

**Wann KEIN Todo:** Single-Step-/triviale/rein konversationelle Anfragen → siehe [[Tool Schema Design]] (TodoManager „When NOT to use").

## Statusupdates (UX)

> „Let me search for where the load balancer is configured." → „I found the load balancer configuration. Now I'll update the number of replicas to 3." → „My edit introduced a linter error. Let me fix that." — *Cursor*

- 1–3 Sätze pro Tool-Batch; Vergangenheit für Erledigtes, Präsens für Laufendes
- Triviales nicht erzählen; Blocker/Risiken nennen

## Parallelisierung (großer Hebel)

> „For maximum efficiency, whenever you perform multiple operations, invoke all relevant tools concurrently rather than sequentially. … DEFAULT TO PARALLEL unless operations MUST be sequential." — *Windsurf / Cursor*

- Unabhängige Reads/Searches/Writes **batchen**
- ~3–5 Tools pro Batch (Timeout-Schutz)

> [!tip] Übertragbares Prinzip
> Schleife + Todo + knappe Statusupdates + Default-Parallel. Das ist das Rückgrat jedes produktiven Agenten (auch im Claude Agent SDK).

## Verwandt
- [[Code-Editing Workflow]]
- [[Tool Schema Design]]
- [[Clever Patterns Worth Stealing]]
- [[00 - Index (MOC)]]
