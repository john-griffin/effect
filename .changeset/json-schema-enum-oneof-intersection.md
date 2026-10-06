---
"effect": patch
---

Fix `SchemaRepresentation.fromJsonSchemaDocument` rejecting objects whose `oneOf` / `anyOf` branches narrow an `enum` property declared next to them (for example a `kind` enum narrowed to one `const` per branch). Each branch now receives the intersected property instead of failing with an unsupported intersection error.
