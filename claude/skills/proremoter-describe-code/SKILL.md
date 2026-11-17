---
name: proremoter-describe-code
description: Write plain-language descriptions of functions into ProRemoter so flowcharts are readable by non-programmers. Use when the user asks to document, describe or annotate a project, or when project_health reports functions without a description or with stale descriptions.
---

# Describe functions for ProRemoter

ProRemoter has no model of its own; the descriptions shown to people are the ones you write.

1. `descriptions_list_missing` returns functions without a description, most-used first, with callers, callees and a derived hint.
2. Read each function's code yourself. Write one or two plain sentences about what it is for in business terms. Do not restate the code or list its steps.
3. Send batches with `descriptions_save` (file and qualified name exactly as listed, plus the hash when given). Descriptions are bound to the function hash and show as stale when the function changes.
4. Repeat until the list is short, then run `project_health` to confirm missing and stale counts dropped.

Keep descriptions factual. If you cannot tell what a function is for, skip it rather than guess.
