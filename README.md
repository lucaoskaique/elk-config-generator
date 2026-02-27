# ELK Config Generator & Tester

A web-based tool for testing and generating [ELK (Eclipse Layout Kernel)](https://www.eclipse.org/elk/) layout configurations. Visually adjust layout parameters, test with your own graph data, and export configurations for use in any project.

## Features

- **Import Graph JSON**: Paste your graph structure (nodes and edges) to visualize and test layouts
- **Interactive Controls**: Adjust spacing, edge routing, node placement, and more with real-time preview
- **Visual Customization**: Control edge opacity, width, and color
- **Export Configurations**: Copy layout settings in JSON, JavaScript, or TypeScript format
- **Dark Theme**: Beautiful dark UI optimized for extended use

## Usage

### 1. Load Your Graph

Click **"⬆ Load Graph JSON"** and paste your graph data. The tool supports the standard ELK JSON format:

```json
{
  "id": "root",
  "layoutOptions": { ... },
  "children": [
    { "id": "node1", "type": "..." },
    { "id": "node2", "type": "..." }
  ],
  "edges": [
    { "id": "e1", "sources": ["node1"], "targets": ["node2"] }
  ]
}
```

### 2. Adjust Layout Options

Use the sidebar controls to tune:
- **Algorithm**: Edge routing, node placement, crossing minimization
- **Spacing**: Layer spacing, node spacing, edge spacing
- **Visual**: Edge appearance and colors

### 3. Apply & Test

Click **"▶ Apply Layout"** to see your changes in real-time.

### 4. Export Configuration

Click **"↓ Export Config"** to copy your layout settings in:
- Pure JSON
- JavaScript object
- TypeScript with types

## Supported Graph Format

The tool accepts graphs with:
- `children` array containing node objects
- `edges` array with `sources` and `targets` arrays (ELK extended edge format)
- Optional `layoutOptions` that will be merged with UI controls
- Custom node data structures (displayed as pills/badges)

## Local Development

Simply open `index.html` in a modern web browser. No build step required.

## Technologies

- [ELK.js](https://github.com/kieler/elkjs) - Graph layout engine
- Vanilla JavaScript - No framework dependencies
- SVG - High-quality vector rendering

## License

MIT
