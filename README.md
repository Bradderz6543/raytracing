# 💎 Glass Ray Tracer

A fully interactive, browser-based path tracer specializing in realistic glass rendering. Built as a single HTML file with no dependencies.

![Glass Ray Tracer](https://img.shields.io/badge/Renderer-Path%20Tracing-blue) ![Single File](https://img.shields.io/badge/Single-HTML%20File-green) ![No Dependencies](https://img.shields.io/badge/Dependencies-None-orange)

## Features

### 🎨 Interactive Scene Editor
- Add and remove glass objects (spheres and cubes) via a sidebar UI
- Adjust position (X, Y, Z), size, and material properties per object
- Select objects to edit their properties in real-time

### 🔬 Physically-Based Glass Rendering
- **Snell's Law** refraction with configurable Index of Refraction (1.0 – 2.5)
- **Fresnel effect** via Schlick's approximation for realistic reflection/refraction balance
- **Beer's Law** absorption for colored glass tinting
- **Total internal reflection** when light cannot escape dense media
- **Frosted glass** support via surface roughness perturbation

### 🌟 Path Tracing Engine
- Up to 6 ray bounces for realistic caustics and inter-reflections
- Progressive rendering — watch the image refine in real-time
- Soft shadows from area-like lighting
- Depth of field with thin lens camera model
- Gamma-correct tone mapping

### 🖥️ Clean UI
- Dark-themed sidebar with object list and property editors
- Multiple resolution presets (400×300 to 1024×768)
- Configurable sample counts (64 to 4096)
- Start/Stop render controls with live sample counter

## Usage

1. Open `index.html` in any modern browser
2. Add glass objects using the **🔮 Sphere** or **🧊 Cube** buttons
3. Select objects to adjust position, size, IOR, color tint, and roughness
4. Choose resolution and sample count in Render Settings
5. Click **🚀 Render** and watch the image progressively improve

## Technical Details

- Pure JavaScript — no WebGL, no libraries, no build step
- All rendering runs on the CPU via the HTML5 Canvas 2D API
- Each sample traces one path per pixel with Russian-roulette-style bouncing
- Accumulation buffer averages samples for noise reduction over time

## Default Scene

The app starts with three glass objects pre-placed:
- A large clear glass sphere (IOR 1.52)
- A pink-tinted frosted glass cube (IOR 1.45)
- A small green-tinted diamond-like sphere (IOR 2.0)

## License

MIT
