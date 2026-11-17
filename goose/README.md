# ProRemoter for Goose

Goose has no plugin package format. It uses extensions (MCP servers), recipes and skills, so this folder holds the three pieces that together do what the Claude and Copilot plugins do. ProRemoter turns code into plain-language flowcharts; the hosted MCP server is `https://proremoter.com/mcp`, and all agent behaviour comes from Goose.

| File | Purpose |
|---|---|
| `proremoter-review.yaml` | Recipe that includes the ProRemoter extension and the review workflow |
| `skills/` | Three skills (`proremoter-explore`, `proremoter-review-change`, `proremoter-describe-code`) |

## Use

1. Extension only: Extensions, Add custom extension, type **Streamable HTTP**, URL `https://proremoter.com/mcp`, name `ProRemoter`.
2. Recipe: `goose run --recipe proremoter-review.yaml --params task="review the latest change in project Orders"`.
3. Skills: copy the folders in `skills/` to `~/.config/goose/skills` (Windows: `%USERPROFILE%\.config\goose\skills`).

On Windows, if Goose reports "Auth required" after signing in, set `GOOSE_DISABLE_KEYRING=1`.

Privacy and terms: <https://proremoter.com/terms>
