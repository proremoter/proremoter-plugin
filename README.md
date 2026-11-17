# ProRemoter plugins

ProRemoter turns code into plain-language flowcharts for agentic coders. These packages connect your agent to the hosted MCP server (`https://proremoter.com/mcp`) and add three skills: explore a codebase, review a change, describe functions. They have no logic of their own; all agent behaviour comes from your client. Website: <https://proremoter.com>

## Layout

One self-contained folder per client, each in that client's own plugin format.

| Folder | Client | Format |
|---|---|---|
| `github-copilot/` | VS Code, GitHub Copilot CLI | `plugin.json`, `.mcp.json`, `skills/` |
| `claude/` | Claude Code, Claude desktop / Cowork | `.claude-plugin/plugin.json`, `.mcp.json`, `skills/` |
| `goose/` | Goose | recipe, `skills/`, README (Goose has no plugin format) |

At the repository root, `.github/plugin/marketplace.json` lists the Copilot plugin and `.claude-plugin/marketplace.json` lists the Claude plugin, so the repository can be added as a marketplace in either client. The `skills/` folders are copies; keep them identical.

## Install

- **VS Code:** add `https://github.com/proremoter/proremoter-plugin.git` as a plugin marketplace (setting `chat.plugins.marketplaces`, or `vscode://chat-plugin/add-marketplace?ref=https%3A%2F%2Fgithub.com%2Fproremoter%2Fproremoter-plugin.git`), then install `ProRemoter`.
- **GitHub Copilot CLI:** `copilot plugin marketplace add https://github.com/proremoter/proremoter-plugin.git`, then `copilot plugin install ProRemoter@proremoter-plugin`
- **Claude Code:** `/plugin marketplace add https://github.com/proremoter/proremoter-plugin.git`, then `/plugin install ProRemoter@proremoter-plugin`
- **Claude desktop:** zip the contents of `claude/` (so `.claude-plugin/plugin.json` is at the top of the archive) and upload it under Customize, Plugins.
- **Goose:** see [goose/README.md](goose/README.md).

On Windows, if Goose reports "Auth required" after signing in, set `GOOSE_DISABLE_KEYRING=1`.

## Status

The Claude plugin passes `claude plugin validate` and installs in Claude Code. The Copilot and Goose packages follow the documented formats but were not installed from this repository. Not every client shows plugin icons.

## License

MIT, see [LICENSE](LICENSE).
