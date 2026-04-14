---
title: Shape Builder
description: A Meshery extension for interactively creating custom polygon shapes for Meshery components and Kanvas designs.
display_title: false
categories:
- shape-builder
---

## Overview

[Shape Builder](https://shapes.meshery.io) is a Meshery extension that provides an interactive, browser-based tool for designing custom polygon shapes. Once created, shapes are exported in the coordinate format that [Kanvas](/extensions/kanvas/) uses to render custom component visuals inside Meshery designs.

- **GitHub:** [meshery-extensions/shape-builder](https://github.com/meshery-extensions/shape-builder)
- **Live tool:** [shapes.meshery.io](https://shapes.meshery.io)

## How It Works

Shape Builder renders a grid canvas. Click on the grid to place polygon vertices one by one. When your shape is complete, the tool outputs the polygon coordinates in a matrix notation (ranging from `-1` to `+1`) that Meshery and Kanvas expect for a custom `polygon` shape type.

### Controls

| Key / Action | Effect |
|---|---|
| Click on grid | Add a vertex point |
| `Enter` or `Esc` | Close and complete the shape |
| `Ctrl` | Snap vertex to nearest grid line |
| `Ctrl` + `Z` | Undo last vertex |
| Clear button | Reset the canvas |

## Usage

1. Open [shapes.meshery.io](https://shapes.meshery.io) in your browser.
2. Click on the grid to place the vertices of your polygon.
3. Press `Enter` or `Esc` to close the shape.
4. Copy the generated **Polygon Coordinates (SVG format)** string from the output panel.
5. Paste the coordinate string into the `polygon` shape field of your Meshery Component definition.

### Example: Plus Icon

The following coordinate string defines a plus (`+`) icon shape: 
```
-0.33 -1 0.33 -1 0.33 -0.33 1 -0.33 1 0.33 0.33 0.33 0.33 1 -0.33 1 -0.33 0.33 -1 0.33 -1 -0.33 -0.33 -0.33
```


## Relationship to Built-in Shapes

Meshery ships with predefined geometric shapes available to all components. Shape Builder extends this by enabling fully custom polygons. For the full list of built-in shapes see:

➡ [Identifying Meshery Components](/guides/configuration-management/identifying-components/)

## Discussion Forum

Not finding what you're looking for? Ask on the [Discussion Forum](https://meshery.io/community#discussion-forums).
