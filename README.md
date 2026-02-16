# 💎 Glass Ray Tracer

A fully interactive, browser-based path tracer specializing in realistic glass rendering. Built as a single HTML file with no dependencies.

![Glass Ray Tracer](https://img.shields.io/badge/Renderer-Path%20Tracing-blue) ![Single File](https://img.shields.io/badge/Single-HTML%20File-green) ![No Dependencies](https://img.shields.io/badge/Dependencies-None-orange)

## Features

### 🎨 Professional Dark UI
- Blender/Three.js-inspired dark theme with gradient toolbar and panels
- Left sidebar with scene object list and render settings
- Right properties panel with transform and material controls
- Status bar with real-time feedback

### 🖥️ Real-Time 3D Preview
- Canvas 2D perspective projection with interactive viewport
- **Solid mode**: Flat-shaded objects with specular highlights and depth-sorted faces
- **Wireframe mode**: Transparent wireframe with ellipse rings on spheres
- Ground grid with colored X/Z axes
- 3D axes indicator gizmo with arrow tips

### 🎥 Camera Controls
- **Orbit**: Left mouse drag to rotate around target
- **Zoom**: Mouse scroll wheel to dolly in/out
- **Pan**: Right mouse drag or Shift+Left drag to pan
- Camera state carries directly to the path-traced render

### 📋 Scene Management
- Add spheres and cubes from toolbar or sidebar buttons
- Object list with color dots, IOR display, and position info
- Click to select, inline delete buttons
- Clear scene and reset camera controls

### 🔬 Physically-Based Glass Rendering
- **Snell's Law** refraction with configurable Index of Refraction (1.0 – 2.5)
- **Fresnel effect** via Schlick's approximation for realistic reflection/refraction balance
- **Beer's Law** absorption for colored glass tinting
- **Total internal reflection** when light cannot escape dense media
- **Frosted glass** support via surface roughness perturbation

### 🌟 Path Tracing Engine
- Configurable ray bounces (3–10) for realistic caustics and inter-reflections
- Progressive rendering — watch the image refine in real-time
- Soft shadows from area-like lighting
- Depth of field with thin lens camera model
- Gamma-correct tone mapping
- Render overlay with elapsed time and ETA display

### ⚙️ Render Settings
- Multiple resolution presets (320×240 to 1024×768)
- Configurable sample counts (32 to 4096)
- Adjustable bounce depth
- Preview mode toggle (Solid/Wireframe)

## Usage

1. Open `index.html` in any modern browser
2. Use the 3D preview to frame your scene — orbit, zoom, and pan the camera
3. Add glass objects using the toolbar or sidebar **+ Sphere / + Cube** buttons
4. Select objects to adjust position, size, IOR, color tint, and roughness
5. Configure resolution, samples, and bounces in Render Settings
6. Click **▶ Render** and watch the image progressively improve
7. Use **■ Stop** to halt early or **← Edit** to return to the preview

## Technical Details

- Pure JavaScript — no WebGL, no libraries, no build step
- All rendering runs on the CPU via the HTML5 Canvas 2D API
- Each sample traces one path per pixel with physically-based bouncing
- Accumulation buffer averages samples for noise reduction over time
- Depth-sorted solid preview with per-face lighting

## Default Scene

The app starts with three glass objects pre-placed:
- A large clear glass sphere (IOR 1.52)
- A pink-tinted frosted glass cube (IOR 1.45)
- A small green-tinted diamond-like sphere (IOR 2.0)

## License

MIT
