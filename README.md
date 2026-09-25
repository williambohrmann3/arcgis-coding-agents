# Esri Developer Skills

Technology-specific [Agent Plugins 1.0](https://agent-plugins.org/specification/) packages containing Esri Developer documentation guidance and the **MCP for Esri Developers** server.

## Plugins

Each plugin is named after its ArcGIS SDK, API, or mapping library and contains three skills, where `x` is the plugin name:

- `search-x-docs`: technology-specific documentation guidance.
- `follow-x-best-practices`: placeholder for best-practice guidance.
- `build-a-starter-x-mapping-app`: placeholder for starter mapping app guidance.

The two placeholder skills do not yet provide implementation guidance. Install the plugins relevant to your project:

- [arcgis-pro-sdk-dotnet](plugins/arcgis-pro-sdk-dotnet): ArcGIS Pro SDK for .NET
- [arcgis-api-for-python](plugins/arcgis-api-for-python): ArcGIS API for Python
- [calcite-design-system](plugins/calcite-design-system): Calcite Design System
- [cesiumjs](plugins/cesiumjs): CesiumJS with ArcGIS services
- [dotnet-maps-sdk](plugins/dotnet-maps-sdk): ArcGIS Maps SDK for .NET
- [esri-leaflet](plugins/esri-leaflet): Esri Leaflet
- [flutter-maps-sdk](plugins/flutter-maps-sdk): ArcGIS Maps SDK for Flutter
- [javascript-maps-sdk](plugins/javascript-maps-sdk): ArcGIS Maps SDK for JavaScript
- [kotlin-maps-sdk](plugins/kotlin-maps-sdk): ArcGIS Maps SDK for Kotlin
- [maplibre-arcgis](plugins/maplibre-arcgis): MapLibre GL JS with ArcGIS services
- [openlayers](plugins/openlayers): OpenLayers with ArcGIS services
- [qt-maps-sdk](plugins/qt-maps-sdk): ArcGIS Maps SDK for Qt
- [swift-maps-sdk](plugins/swift-maps-sdk): ArcGIS Maps SDK for Swift
- [unity-maps-sdk](plugins/unity-maps-sdk): ArcGIS Maps SDK for Unity
- [unreal-maps-sdk](plugins/unreal-maps-sdk): ArcGIS Maps SDK for Unreal Engine

## Package Layout

Use the selected `plugins/<plugin-name>` directory as the plugin root:

```text
plugins/<plugin-name>/
  plugin.json
  skills/
    search-<plugin-name>-docs/SKILL.md
    follow-<plugin-name>-best-practices/SKILL.md
    build-a-starter-<plugin-name>-mapping-app/SKILL.md
  mcp.json
```

Each package follows the standard fixed component locations:

- `plugin.json` declares the Agent Plugins 1.0 manifest schema.
- `skills/` contains the documentation search skill and the two placeholder skills, each in a folder matching its skill name.
- `mcp.json` configures **MCP for Esri Developers** over Streamable HTTP at `https://developers-mcpdevext.arcgis.com/mcp`.

The packages include only portable skills and MCP configuration. No GitHub Copilot prompt or custom agent extension is included.

## Installation documentation

Use the client’s official documentation for the installation flow. Select or package the desired `plugins/<plugin-name>` directory as the plugin source where the client supports Agent Plugins 1.0. The repository catalogs list all 15 plugins individually.

- [GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/plugins-finding-installing)
- [VS Code](https://code.visualstudio.com/docs/agent-customization/agent-plugins#_install-a-plugin-from-source)
- [Claude Code](https://code.claude.com/docs/en/discover-plugins#add-from-github)
- [Cursor](https://cursor.com/docs/plugins#installing-plugins)
- [Xcode](https://developer.apple.com/documentation/xcode/extending-and-customizing-agents#Install-agentic-coding-plug-ins)
- [Kiro](https://kiro.dev/docs/powers/installation/#from-public-github-url)

These references describe each client’s official installation or extension workflow. The recommended approach is to install directly from this repository.

## Validation

Validate package manifests against the official [Agent Plugins 1.0 plugin schema](https://agent-plugins.org/schemas/1.0.0/plugin.schema.json) and [MCP schema](https://agent-plugins.org/schemas/1.0.0/mcp.schema.json). After installation, verify that:

- each installed plugin's three skills are discoverable; and
- **MCP for Esri Developers** is connected.
