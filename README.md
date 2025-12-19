# Optimization Toolkit for Unity

![Animation](https://github.com/user-attachments/assets/aea0f312-416b-4da8-ab6f-2a2b7f12a037)

Optimization Toolkit is a modular Unity Editor toolkit that groups more than 20
custom editor tools into a single, centralized hub.

It was created to speed up optimization, cleanup, and content preparation tasks
commonly encountered in mid-to-large Unity projects, where manual workflows
become slow, error-prone, and difficult to scale.

This toolkit focuses on editor productivity and explicit, repeatable actions,
without introducing hidden automation or runtime dependencies.

---

## Key Features

### Centralized Tool Hub
All tools are accessed from a single custom Editor window, organized by category:

- Info  
- Modeling  
- Animation  
- Image  
- Scene  
- Utilities  

This avoids scattered menu items and keeps workflows consistent across projects.

---

## Tool Overview

### Modeling & Mesh Tools
- Split multi-material meshes into individual meshes
- Detect extremely small or problematic triangles
- Adjust and visualize mesh bounds directly in the Scene view
- Generate secondary UVs (UV2) for lightmapping
- Adjust UVs into grid or tile layouts
- Create hollow or clipped mesh shells
- Display vertex IDs directly in the Scene view

---

### Animation Tools
- Clean animation clips (remove unused keys, rename bindings, add prefixes)
- Combine multiple animation clips while preserving hierarchy paths
- Bake skinned mesh poses into static meshes
- Transfer bone weights between meshes
- Generate UI animation clips from sprite sequences

---

### Image & Video Tools
- Convert texture assets to image files and back
- Merge image channels (R/G/B/A) into a single texture
- Split image channels into separate files
- Extract frames from video files using FFmpeg

> Note: FFmpeg is **not included** in this repository.  
> Some video-related tools will not function unless the FFmpeg plugin is installed manually.

---

### Scene & Validation Tools
- Find objects using multiple materials
- List objects with lightmaps assigned
- Inspect scene content for common optimization issues

---

### Utilities
- Batch rename scene objects and project assets
- Flexible renaming rules (prefix, suffix, replace, numbering, case conversion)

---

## Architecture & Design

- Built entirely as Unity Editor tooling (C#)
- Modular and extensible design
- Each tool is self-contained and does not interfere with others
- Tool data and configuration are built around ScriptableObjects
- Optional Scene view overlays and helpers for visual feedback

---

## FFmpeg Integration (Optional)

Some media-related tools in this toolkit rely on FFmpeg for video processing.
FFmpeg is **not bundled** with this package.

### Setup
1. Obtain an FFmpeg build compatible with your platform.
2. Copy the FFmpeg folder into your Unity project under: Assets/Optimization_Toolkit/Plugins
3. Restart the Unity Editor.

Once installed, the toolkit will automatically detect the FFmpeg plugin.
If FFmpeg is not present, related tools will be disabled or unavailable.

---

## Requirements
- Unity 2021.3 or newer
- Editor-only tools (no runtime impact)
- Windows / macOS / Linux
- Optional: FFmpeg plugin for video-related tools

---

## Intended Users
- Technical artists
- Environment artists
- Animators
- Unity developers working on optimization passes
- Teams needing fast, repeatable editor-side utilities

---

## Philosophy
- One hub, many focused tools
- Explicit actions with predictable results
- No hidden automation
- Editor productivity over runtime abstraction
- FFmpeg tools behave exactly as defined by their parameters

---

## License
MIT License  
Free to use, modify, and integrate in both commercial and non-commercial projects.

