# Agentic engineering

This repository provides an Agent Plugins 1.0 package for Esri coding skills, the Esri Developer custom agent, and the Esri Developer documentation MCP server.

```mermaid
flowchart TD
	subgraph IDE["IDE"]
		direction TB
		Skills["/skills "]

		subgraph CodingAgent["Coding agent"]
			direction TB
			AgentDoc@{ shape: doc, label: "Esri Developer agent.md" }
		end
	end

	MCP@{ shape: cloud, label: "MCP for Esri dev docs" }

	subgraph SkillsMarketplace["Coding skills marketplace"]
		direction LR
		Kotlin["/kotlin"]
		Flutter["/flutter"]
	end

	CodingAgent <--> MCP
	CodingAgent <--> Skills
	Skills <--> SkillsMarketplace
```

## Package layout

The portable package is [plugins/esri-developer-skills](plugins/esri-developer-skills):

```text
plugins/esri-developer-skills/
	plugin.json
	skills/
		<skill-name>/SKILL.md
	mcp.json
	com.github.copilot/agents/
		Esri_Developer.agent.md
```

`plugin.json` and `mcp.json` use the Agent Plugins 1.0 schemas. Skills remain in the fixed `skills/` directory. The MCP server is configured as a streamable HTTP server at `https://mcp.esri.com/`.

## Install

Install the `plugins/esri-developer-skills` directory as an Agent Plugins 1.0 package in clients that support the standard. The exact install command is client-specific; use the client’s plugin or extension installation flow and select this directory or a packaged copy of it.

The retained [Esri Developer agent](agents/Esri%20Developer.agent.md) remains available at the repository root for clients that do not load the bundled `com.github.copilot/agents/` directory.

### Legacy GitHub Copilot CLI

From a local checkout:

```powershell
copilot plugin marketplace add .
copilot plugin install esri-developer-skills@arcgis-coding-skills
```

From GitHub:

```powershell
copilot plugin marketplace add https://github.com/williambohrmann3/arcgis-coding-agents
copilot plugin install esri-developer-skills@arcgis-coding-skills
```

These commands use the repository’s legacy marketplace manifest. Use them when the client does not yet install Agent Plugins 1.0 packages directly.

### Legacy Claude Code

From a local checkout:

```powershell
claude plugin marketplace add .
claude plugin install esri-developer-skills@arcgis-coding-skills
```

From GitHub:

```powershell
claude plugin marketplace add https://github.com/williambohrmann3/arcgis-coding-agents
claude plugin install esri-developer-skills@arcgis-coding-skills
```

### Codex

The repository exposes a Codex-compatible marketplace manifest at `.agents/plugins/marketplace.json`.

Verify a legacy installation with `copilot plugin list` or `claude plugin list`, then inspect available skills with `/skills list`. For an Agent Plugins 1.0 installation, verify that the skills are listed and that the `esri-developer` MCP server is connected.

## Client validation

This repository validates the package manifests against the official Agent Plugins 1.0 schemas. Installation testing requires each client and is tracked here as follows:

| Client | Agent Plugins 1.0 package | Current result | Fallback |
| --- | --- | --- | --- |
| VS Code | Intended supported client | Package installation test pending | Install skills and MCP separately |
| Cursor | Intended supported client | Package installation test pending; use `${CURSOR_PLUGIN_ROOT}` if a path is required | Install skills and MCP separately |
| Kiro | Intended supported client | Power / Agent Plugins installation test pending | Install skills and MCP separately |
| Claude Code | Requires client-specific verification | Agent Plugins installation test pending | Use `.claude-plugin` marketplace package |
| Xcode | Requires client-specific verification | Copilot plugin installation test pending | Configure MCP separately and use skills supported by the client |
| Android Studio | Requires client-specific verification | Copilot JetBrains plugin installation test pending | Configure MCP separately and use skills supported by the client |
| Visual Studio 2026 | Requires client-specific verification | Copilot plugin installation test pending | Configure MCP separately and use skills supported by the client |

The repository must not treat standalone MCP configuration or standalone skills discovery as proof of plugin installation. Update this table with the client version, package source, and observed skills/MCP result after each manual installation test.
