# ProRemoter for Claude

ProRemoter turns code into plain-language flowcharts. This Claude Code / Claude desktop plugin connects your agent to the hosted ProRemoter MCP server (`https://proremoter.com/mcp`) and adds three skills: `proremoter-explore` (orient in a codebase), `proremoter-review-change` (review what a change does to the logic) and `proremoter-describe-code` (write plain-language function descriptions). The plugin has no logic of its own; all agent behaviour comes from your client, and sign-in uses the normal OAuth flow.

Privacy and terms: <https://proremoter.com/terms>. Website: <https://proremoter.com>

## Install

- Claude Code: `/plugin marketplace add proremoter/proremoter-plugin`, then `/plugin install proremoter@proremoter-plugin`.
- Claude desktop (sideload): upload `proremoter-claude-plugin.zip` from the repository releases, or zip the contents of this folder so that `.claude-plugin/plugin.json` is at the top level of the archive.

This folder is self-contained. The GitHub Copilot / VS Code plugin lives in the repository root and shares nothing with it except the content of the skills, which are kept identical.
