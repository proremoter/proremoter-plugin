# ProRemoter for GitHub Copilot

ProRemoter turns code into plain-language flowcharts. This GitHub Copilot and VS Code agent plugin connects your agent to the hosted ProRemoter MCP server (`https://proremoter.com/mcp`) and adds three skills: `proremoter-explore` (orient in a codebase), `proremoter-review-change` (review what a change does to the logic) and `proremoter-describe-code` (write plain-language function descriptions). The plugin has no logic of its own; all agent behaviour comes from your client, and sign-in uses the normal OAuth flow.

Privacy and terms: <https://proremoter.com/terms>. Website: <https://proremoter.com>

## Install

- VS Code: add the marketplace `https://github.com/proremoter/proremoter-plugin.git` (setting `chat.plugins.marketplaces`, or the deep link `vscode://chat-plugin/add-marketplace?ref=https%3A%2F%2Fgithub.com%2Fproremoter%2Fproremoter-plugin.git`), then install `ProRemoter` from Agent Customizations, Plugins.
- GitHub Copilot CLI: `copilot plugin marketplace add https://github.com/proremoter/proremoter-plugin.git` followed by `copilot plugin install ProRemoter@proremoter-plugin`.

This folder is self-contained. The Claude plugin lives in `../claude`.
