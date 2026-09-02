# Stack Decisions

Room Zero uses a deliberately small 3D stack. Each tool has one clear job so the project teaches the underlying workflow instead of hiding it behind a large framework.

## Blender — creating the 3D assets

Blender is used to create the room, furniture, props, and eventually an original character.

Why Blender:

- It is free and open source.
- It covers modeling, materials, UVs, rigging, and animation in one application.
- Skills learned in Blender transfer beyond Godot to other engines, rendering, animation, and 3D design.
- It lets Room Zero contain assets made from scratch instead of relying entirely on downloaded asset packs.

Blender is not the game engine. Its job is to create the objects that the engine will use.

## Godot — assembling and running the world

Godot is the game engine. It takes the models and turns them into an interactive scene.

Why Godot:

- It is free and open source.
- Its scene/node system makes the parts of a small 3D world visible and understandable.
- Collision, cameras, lighting, physics, input, and scripting are built into the engine.
- It is lightweight enough for a learning experiment without requiring a large production pipeline.
- The same project can later explore desktop and mobile builds.

Godot answers questions Blender does not: Can the player walk here? What happens when the player presses a key? Does this object block movement? What does the camera follow?

## glTF / GLB — moving assets between tools

Room Zero uses the glTF ecosystem, particularly `.glb`, as the main asset exchange format between Blender and Godot.

Why GLB:

- It is designed for modern 3D asset interchange.
- A single GLB can package geometry and related asset data conveniently.
- Blender exports it directly and Godot imports it directly.
- It creates a clean boundary between asset creation and game-engine work.

Conceptually:

```text
Blender source (.blend)
        ↓ export
Portable asset (.glb)
        ↓ import
Godot scene
```

The `.blend` file is the editable source. The `.glb` file is the version handed to the engine.

## GDScript / C# — behavior

Models by themselves do nothing. Scripts give the scene behavior: movement, interactions, doors, lights, triggers, camera logic, and other rules.

### Why start with GDScript

GDScript is a strong first choice for Room Zero because it is tightly integrated with Godot and keeps small gameplay experiments concise. Its syntax is approachable for someone already familiar with Python-style code.

### Why keep C# as an option

C# is also relevant because it is already part of the developer's existing software background. Later experiments can compare the same Godot concepts in GDScript and C#.

The important learning target is not the scripting language itself. It is understanding how code communicates with scene nodes and game-engine systems.

## Why not Unity or Unreal first?

Both are capable engines. They are intentionally not the starting point because Room Zero is a small learning laboratory, not a production game. Adding a larger engine would increase the number of concepts competing for attention before the basic 3D pipeline is understood.

Once the fundamentals are clear, comparing engines becomes much more meaningful.

## Why no backend, database, or cloud services?

The first experiment does not need them.

Room Zero currently has no accounts, multiplayer state, remote saves, commerce, analytics pipeline, or server-side gameplay. A backend would solve problems the project does not yet have.

That is an architectural lesson too: do not add infrastructure merely because it is available.

## Current Stack Boundary

```text
Asset creation       → Blender
Asset interchange    → GLB / glTF
World / engine       → Godot
Behavior             → GDScript (C# optional later)
Version control      → Git + GitHub
```

Every new technology should have to justify its place in this diagram.