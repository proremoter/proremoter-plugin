---
name: proremoter-explore
description: Understand, visualize and explore code as plain-language flowcharts with ProRemoter (MCP). Use when the user asks how a project or function works, where logic starts, what calls what, for an architecture or system overview, or to show, draw, visualize or diagram code as a flowchart or call graph.
---

# Explore a codebase with ProRemoter

Use the ProRemoter MCP tools. They work from a deterministic model of the code; you provide the interpretation.

1. `project_list` to find the project id. If the code is not imported, use `project_create` then `project_import_files` (read the files yourself and send them).
2. `project_health` first. Report the share of steps modeled and anything skipped before drawing conclusions, because a chart that looks complete may not be.
3. `system_map` to find entry points (web routes, jobs, messages, command-line starts). Entry points are guesses; say so.
4. `graph_project_tree` and `graph_search` to find functions. Ids appear in [brackets].
5. `graph_show_function` (by name) or `graph_show_function_by_id` to show a flowchart to the user. Use these whenever the user asks to see, draw or visualise code.
6. `graph_explain_function` for a plain-language summary; `graph_impact` for callers and callees; `graph_call_paths` for how one function reaches another.

Rules:
- Never claim the picture is complete. Mention calls that could not be followed (libraries, dynamic calls) when the tool lists them.
- Do not invent behaviour the tools did not return; read the source when a step is opaque.
