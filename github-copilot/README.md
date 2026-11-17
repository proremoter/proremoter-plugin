# ProRemoter for GitHub Copilot

ProRemoter turns code into plain-language flowcharts. This GitHub Copilot and VS Code agent plugin connects your agent to the hosted ProRemoter MCP server (`https://proremoter.com/mcp`) and adds three skills: `proremoter-explore` (orient in a codebase), `proremoter-review-change` (review what a change does to the logic) and `proremoter-describe-code` (write plain-language function descriptions). The plugin has no logic of its own; all agent behaviour comes from your client, and sign-in uses the normal OAuth flow.

Privacy and terms: <https://proremoter.com/terms>. Website: <https://proremoter.com>

## Install

- VS Code: add the marketplace `proremoter/proremoter-plugin` (setting `chat.plugins.marketplaces`, or the deep link `vscode://chat-plugin/add-marketplace?ref=proremoter%2Fproremoter-plugin`), then install `ProRemoter` from Agent Customizations, Plugins.
- GitHub Copilot CLI: `copilot plugin install proremoter/proremoter-plugin:github-copilot`, or `copilot plugin marketplace add proremoter/proremoter-plugin` followed by `copilot plugin install ProRemoter@proremoter-plugin`.

This folder is self-contained. The Claude plugin lives in `../claude`.
