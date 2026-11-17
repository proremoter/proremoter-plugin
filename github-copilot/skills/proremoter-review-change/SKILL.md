---
name: proremoter-review-change
description: Review and visualize a code change with ProRemoter (MCP): what a diff, commit, pull request or edit does to the logic, how risky it is, and what it may break. Use when the user asks to review a change, compare two versions, assess code change risk, find the impact or blast radius, or find side effects such as database writes or network calls.
---

# Review a change with ProRemoter

1. Import the new version with `project_import_files` (give a short `label` saying what changed). The previous version is kept for comparison.
2. `change_review` lists added, removed and changed functions ranked by risk with reasons, including side effects a change adds, and links to a page where the user marks items reviewed or flagged.
3. `graph_compare_revisions` shows the before and after flowcharts with changed steps marked. Do not filter (`show`) unless the user asks to see only some kinds of change; offer the choice when the comparison is large. Use `function` to open a specific one and `file` to narrow the list.
4. For each high-risk function, `graph_impact` (direction `up`) shows what may break; `side_effect_tags` (with `rolled: true`) shows whether it reaches a database write, outgoing request, file access and so on.
5. `project_health` tells you how far to trust the comparison.

Report in plain language: what changed in the logic, what it can affect, what looks risky and why. Tags and risk scores are heuristics, so call them "likely".
