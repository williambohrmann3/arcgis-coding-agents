# Esri Developer Skills

[Agent Plugins](https://agent-plugins.org/specification/) for Esri Developer skills and the **MCP for Esri Developers** server.

## Plugins

Choose a plugin for the ArcGIS product, SDK, API, or mapping library you use. Each includes technology-specific development guidance and a connection to **MCP for Esri Developers**.

Plugins contain the following skills:

- **Documentation search:** find relevant Esri Developer documentation.
- **Best practices:** apply technology-specific recommendations to your project.
- **Starter projects:** build an app, Python script, or ArcGIS Pro extension.

The ArcGIS Location Platform and ArcGIS Enterprise plugins include documentation search only.

### Available Plugins

- [arcgis-location-platform](plugins/arcgis-location-platform): ArcGIS Location Platform
- [arcgis-enterprise](plugins/arcgis-enterprise): ArcGIS Enterprise
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

## Installation documentation

Use the client’s official documentation for the installation flow to install the desired plugin(s).

- [GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/plugins-finding-installing)
- [VS Code](https://code.visualstudio.com/docs/agent-customization/agent-plugins#_install-a-plugin-from-source)
- [Claude Code](https://code.claude.com/docs/en/discover-plugins#add-from-github)
- [Cursor](https://cursor.com/docs/plugins#installing-plugins)
- [Xcode](https://developer.apple.com/documentation/xcode/extending-and-customizing-agents#Install-agentic-coding-plug-ins)
- [Kiro](https://kiro.dev/docs/powers/installation/#from-public-github-url)

These references describe each client’s official installation or extension workflow. The recommended approach is to install directly from this repository.

## Validation

Validate package manifests against the official [Agent Plugins 1.0 plugin schema](https://agent-plugins.org/schemas/1.0.0/plugin.schema.json) and [MCP schema](https://agent-plugins.org/schemas/1.0.0/mcp.schema.json). After installation, verify that:

- each installed plugin's included skills are discoverable; and
- **MCP for Esri Developers** is connected.
