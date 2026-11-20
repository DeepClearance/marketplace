# Deep Clearance marketplace

One Claude Code install adds the skill and the remote MCP server.

In a Claude Code session:

```
/plugin marketplace add DeepClearance/marketplace
/plugin install deep-clearance@deepclearance
```

Set `DEEP_CLEARANCE_KEY` to the paid key before Claude Code starts. The plugin sends it as `Authorization: Bearer`. Claude Code can send a remote header that names a credential variable as an empty value. If `claude mcp list` shows a 401, add the server directly.

```
claude mcp add --transport http deep-clearance https://mcp.deepclearance.com/mcp --header "Authorization: Bearer $DEEP_CLEARANCE_KEY"
```

The endpoint is `https://mcp.deepclearance.com/mcp`. Install steps for other clients are at `https://deepclearance.com/skills/`.
