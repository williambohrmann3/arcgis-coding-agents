# Esri Developer Skills

An [Agent Plugins 1.0](https://agent-plugins.org/specification/) package containing Esri Developer skills, the **MCP for Esri Developers** server, and a Copilot custom agent.

## Package

Use [plugins/esri-developer-skills](plugins/esri-developer-skills) as the plugin root:

```text
plugins/esri-developer-skills/
  plugin.json
  skills/
    <skill-name>/SKILL.md
  mcp.json
  com.github.copilot/
    agents/
      Esri_Developer.agent.md
```

The package follows the standard fixed component locations:

- `plugin.json` declares the Agent Plugins 1.0 manifest schema.
- `skills/` contains the ArcGIS technology-specific skills.
- `mcp.json` configures **MCP for Esri Developers** over Streamable HTTP at `https://developers-mcpdevext.arcgis.com/mcp`.
- `com.github.copilot/` contains the VS Code and GitHub Copilot-specific custom agent extension.

The portable standard defines skills and MCP. Client-specific extensions, including the custom agent, are interpreted by the owning client.

## Installation documentation

Use the client’s official documentation for the installation flow. Select or package the `plugins/esri-developer-skills` directory as the plugin source where the client supports Agent Plugins 1.0.

- [VS Code agent plugins](https://code.visualstudio.com/docs/agent-customization/agent-plugins)
- [Claude Code plugins](https://code.claude.com/docs/en/plugins)
- [GitHub Copilot for Xcode](https://github.com/github/CopilotForXcode)
- [GitHub Copilot in JetBrains IDEs, including Android Studio](https://docs.github.com/en/copilot/how-tos/use-copilot-in-the-ide/getting-code-suggestions-in-your-ide)
- [GitHub Copilot for Visual Studio](https://learn.microsoft.com/en-us/visualstudio/ide/visual-studio-github-copilot-install-and-states)

These references describe each client’s official installation or extension workflow.

## Validation

The package manifests are validated against the official [Agent Plugins 1.0 plugin schema](https://agent-plugins.org/schemas/1.0.0/plugin.schema.json) and [MCP schema](https://agent-plugins.org/schemas/1.0.0/mcp.schema.json). After installation, verify that:

- the ArcGIS skills are discoverable;
- **MCP for Esri Developers** is connected; and
- the Copilot custom agent is available (if applicable).
