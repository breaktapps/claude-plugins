# BreaktApps Claude Plugins

A curated marketplace of MCP plugins for Claude Code, maintained by [BreaktApps](https://github.com/breaktapps).

## What is this

This repository indexes plugins built to extend Claude Code via the Model Context Protocol (MCP). Each plugin is maintained in its own repository and listed here for discovery and installation.

## Available Plugins

| Plugin | Description | Repository |
|--------|-------------|------------|
| Claude Token Saver | Semantic code search that reduces token consumption by 70–90% during code exploration. Replaces grep/cat cascading with vector search returning only relevant chunks. | [breaktapps/claude-token-saver](https://github.com/breaktapps/claude-token-saver) |

## How to Install

### Claude Token Saver

Add the plugin to your Claude Code MCP configuration:

```json
{
  "mcpServers": {
    "claude-token-saver": {
      "command": "uvx",
      "args": ["--from", "git+https://github.com/breaktapps/claude-token-saver", "claude-token-saver"]
    }
  }
}
```

Requirements: Python 3.11+, uv 0.4.0+

Refer to the plugin repository for full setup instructions and configuration options.

## How to Contribute

To submit a new plugin:

1. Ensure your plugin is published in a public GitHub repository with a `README.md` and `pyproject.toml` (or equivalent manifest).
2. Open a pull request adding a `plugin-metadata.json` entry under `plugins/<your-plugin-id>/`.
3. Follow the metadata schema used by existing plugins in this repository.
4. A maintainer will review and merge if the plugin meets quality standards.

## License

MIT
