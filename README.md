# WarBound

A turn-based, grid-based dungeon RPG built on a **custom C++ game engine** by team *Struct Squad* for the GAM200/GAM250 modules at DigiPen Institute of Technology Singapore (SIT-DigiPen).

Lead a party of heroes (Warrior, Mage, Berserker) through procedurally generated levels. Each turn you spend movement points on the grid, fight enemies in turn-based combat and use skills to reach and defeat each level's boss.

<!-- Screenshots / gameplay GIF go here -->

## Features

- **Custom engine** written from scratch in C++ with an Entity Component System (ECS)
- **OpenGL renderer** with batched meshes, shaders, sprite animation, particles and text rendering
- **Procedural map generation** and **A\* pathfinding** for enemy AI
- **Turn-based combat** with a skill system and skill-select between levels
- **Lua scripting** for gameplay logic (bosses, UI, level control)
- **In-engine level and prefab editor** built with Dear ImGui
- Game state manager, event/messaging system, serialization (JSON), FMOD audio

## My role: Graphics programmer

I was mainly responsible for the rendering and windowing side of the engine:

- **Mesh system and MeshFactory**: creating and managing the meshes used by everything that's drawn
- **Window system**: GLFW window creation, resizing and context setup
- **Shaders and resource manager**: loading and caching shaders and other rendering resources
- **Animation system**: sprite-sheet animation for characters and enemies
- **Particle system and particle manager**: runtime particle effects
- Contributed to the core graphics system alongside our graphics/audio teammate

Relevant code: [`src/Graphics/`](src/Graphics), [`src/Windows/`](src/Windows), [`engine/Graphics/`](engine/Graphics)

## Tech stack

C++ · OpenGL (GLEW) · GLFW · GLM · Dear ImGui · Lua · nlohmann/json · FreeType · stb · FMOD · CMake

## Building (Windows)

Requirements: Visual Studio 2022 with **Desktop development with C++** and **C++ CMake tools for Windows**, plus Git (CMake fetches some dependencies).

```bat
run.bat               :: build and run the game (Debug)
run.bat release       :: Release build
run.bat editor        :: build with the level editor
run.bat clean         :: delete build folders
```

The executable is written to `bat-build\vs2022-game-x64-<Config>\<Config>\StructSquad.exe`. See [`ProjectGuide.txt`](ProjectGuide.txt) for more detail.

## Controls

| Key | Action |
| --- | --- |
| W A S D | Move one tile (uses a movement point) |
| 1 – 4 | Select skill (Tab cycles targets) |
| P | End turn |
| Esc | Pause menu / settings |
| Q | Quit |

## Team

Ivan Ng (Product Manager), Ethan Ng (Tech Lead), Sim Kah Yan (Graphics + Audio), **Tan Wei Leong (Graphics Programmer)**, Josh Ong (Map), Ge Yong Qi (Debug), Zhou Jiahao (Collision + Physics), Carl Jameson Z. Padilla (Programmer), Gerard Lou (Design Lead).

---

Made as a student project at DigiPen Institute of Technology Singapore. All content © DigiPen Institute of Technology Singapore.
