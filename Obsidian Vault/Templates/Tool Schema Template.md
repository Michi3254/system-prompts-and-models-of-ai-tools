---
title: Tool Schema Template
tags: [template, tools, schema, reusable]
---

# Tool Schema Template

> [!summary]
> Gold-Standard-Gerüst aus [[Tool Schema Design]]. Format: Anthropic-Tool-Use (`input_schema`). Für OpenAI-Function-Calling analog unter `parameters`.

```json
{
  "name": "verb_noun",
  "description": "ONE-LINER: was das Tool tut.\n\nWhen to use:\n- {{Fall A}}\n- {{Fall B}}\n\nWhen NOT to use:\n- {{Gegenfall}} → use {{ANDERES_TOOL}} instead.\n\nExample: {{kurzes konkretes Beispiel}}",
  "input_schema": {
    "type": "object",
    "properties": {
      "primary_param": {
        "type": "string",
        "description": "REQUIRED. Was es tut + Constraints. Reuse the user's exact wording unless there's a clear reason not to."
      },
      "mode": {
        "type": "string",
        "enum": ["option_a", "option_b"],
        "description": "OPTIONAL. option_a = …, option_b = …",
        "default": "option_a"
      },
      "limit": {
        "type": "integer",
        "description": "OPTIONAL. Keep as small as possible to avoid excessive output/memory.",
        "default": 50
      },
      "safe_to_auto_run": {
        "type": "boolean",
        "description": "Set true ONLY if extremely confident it is safe. If unsure, set false EVEN if the user asks.",
        "default": false
      },
      "summary": {
        "type": "string",
        "description": "First arg. 2-5 word UI summary, e.g. 'searching the web', 'editing file'."
      }
    },
    "required": ["primary_param"],
    "additionalProperties": false
  }
}
```

## Checkliste für ein gutes Tool
- [ ] Verb-first, snake_case, im Namespace (`file_*`, `browser_*`)
- [ ] Beschreibung hat **When to use** UND **When NOT to use**
- [ ] Verweist bei Abgrenzung auf das richtige Nachbar-Tool
- [ ] `required` minimal; Optionales hat `default`
- [ ] Enums statt Freitext, wo möglich
- [ ] Parameter-Beschreibungen mit Constraints/Beispielen
- [ ] Safety-Gate bei destruktiven Ops (`safe_to_auto_run`/`blocking`)
- [ ] Output-Limits angekündigt (Truncation)

## Verwandt
- [[Tool Schema Design]] · [[Common Tools Reference]] · [[System Prompt Template]] · [[00 - Index (MOC)]]
