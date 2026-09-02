# Learning Path

Room Zero should grow by proving one 3D concept at a time.

## Stage 0 — Engine boots

Open the Godot project and run the starter scene.

Learn:

- What a Godot project is
- What a scene is
- What nodes are
- How the 3D viewport relates to the running game

Success: a basic floor, light, and camera render without errors.

## Stage 1 — Make one object

Create one simple object in Blender. A desk, table, stool, crate, or lamp is better than starting with a character.

Learn:

- Object mode vs edit mode
- Basic transforms
- Simple mesh editing
- Scale and dimensions
- Saving a `.blend` source file

Success: the object exists as an original Blender model.

## Stage 2 — Asset pipeline

Export the object as GLB and import it into Godot.

Learn:

- Source assets vs exported assets
- Coordinate systems and scale
- What survives an export/import boundary
- How Godot represents an imported model

Success: the Blender object appears in the Room Zero scene at the expected size and orientation.

## Stage 3 — Build the room

Add walls and a few props while keeping the environment tiny.

Learn:

- Scene composition
- Reusable nodes/scenes
- Materials
- Basic lighting
- Transform hierarchy

Success: Room Zero looks recognizably like a small room.

## Stage 4 — Add a player

Start with a simple placeholder character before investing time in character modeling.

Learn:

- CharacterBody3D
- Input actions
- Velocity and movement
- Delta time
- Gravity

Success: WASD or equivalent controls move the player through the room.

## Stage 5 — Collision

Make the floor, walls, props, and character obey physical boundaries.

Learn:

- Collision shapes
- Static vs moving bodies
- Why rendered geometry and collision geometry are separate concepts

Success: the player cannot walk through the floor, walls, or chosen solid props.

## Stage 6 — Camera

Create a simple third-person camera.

Learn:

- Camera positioning
- Parent/child relationships
- Following a target
- Basic camera feel

Success: the camera follows the player through the room comfortably.

## Stage 7 — One interaction

Add exactly one interaction before adding more features.

Examples:

- Turn on a desk lamp
- Open a door
- Pick up an object
- Trigger a small animation

Learn:

- Input events
- Detection areas or ray casts
- Node communication
- State changes

Success: walking through the room leads to one visible interactive moment.

## Stage 8 — Original character

Only after the scene pipeline works, explore creating a simple original character in Blender.

Learn progressively:

- Low-poly character modeling
- Armatures / rigging
- Weight painting
- Idle and walk animation
- Animation import into Godot

This stage is deliberately later because character creation combines several 3D disciplines at once.

## Stretch Experiments

After the core sequence works, possible experiments include sound, better materials, animation blending, mobile controls, Android export, performance profiling, or a second tiny room.

These are not requirements for the first Room Zero milestone.