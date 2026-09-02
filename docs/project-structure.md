# Project Structure

Room Zero separates engine scenes, scripts, and 3D assets so it stays understandable as the experiment grows.

```text
room-zero/
├── assets/
│   ├── materials/
│   └── models/
├── docs/
│   ├── README.md
│   ├── learning-path.md
│   ├── project-structure.md
│   └── stack-decisions.md
├── scenes/
│   └── main.tscn
├── scripts/
├── .gitignore
├── project.godot
└── README.md
```

## `assets/models/`

Imported/exported 3D assets used by Godot belong here. For example:

```text
assets/models/desk.glb
assets/models/lamp.glb
```

Editable Blender source files can later be organized separately if the project begins accumulating many source assets. The important idea is to distinguish editable source art from engine-ready exports.

## `assets/materials/`

Godot-specific materials and related reusable visual resources belong here.

## `scenes/`

Godot scene files (`.tscn`) belong here.

`main.tscn` is the initial runnable environment. Later the player, room, or interactive props can become separate reusable scenes instead of allowing one scene to become enormous.

## `scripts/`

GDScript files belong here. If Room Zero later uses C#, the structure can be adjusted rather than creating complexity before it is needed.

## `docs/`

This is the project's learning notebook. It records architecture decisions, workflow explanations, and milestones so the repository shows not only what was built, but why.

## `project.godot`

This is Godot's project configuration and entry point. Godot recognizes the repository as a project through this file.

## `.gitignore`

Generated Godot caches, editor metadata, Blender backups, and exported builds are excluded from Git. Source files and intentional project assets stay versioned.

## Asset Flow

A typical prop should move through the project like this:

```text
idea
 ↓
Blender model
 ↓
.blend source
 ↓ export
.glb asset
 ↓
assets/models/
 ↓
Godot scene
 ↓
collision / material / interaction
```

Keeping that flow visible is one of the main educational goals of Room Zero.