# Room Zero Documentation

This folder records the reasoning and learning path behind Room Zero.

Room Zero is deliberately small: the purpose is to understand a complete beginner 3D workflow before attempting a larger game.

## Documents

- [Stack Decisions](stack-decisions.md) — why Blender, Godot, glTF/GLB, and GDScript/C# are used.
- [Learning Path](learning-path.md) — the order in which the experiment should grow.
- [Project Structure](project-structure.md) — what each folder is for and how assets move through the project.

## Core Pipeline

```text
Blender
  ↓
model / material / simple animation
  ↓
glTF / GLB
  ↓
Godot
  ↓
scene + collision + lighting + camera
  ↓
GDScript / C#
  ↓
movement + interaction + game behavior
```

The goal is not to hide this pipeline behind tools. The goal is to learn what each stage contributes.