# Neon Portal (Portal Escape Game)

Portal Escape, also referred to as Phase Lock, is a first-person 3D puzzle-platform shooter built using OpenGL. The game combines precision shooting, spatial puzzle-solving, and timing-based challenges within enclosed, neon-styled environments. Players navigate tiled rooms, create paired portals on walls, interact with environmental elements, avoid dynamic hazards, and reach the exit to complete each level.

## Overview

Phase Lock emphasizes:

- First-person camera and physics-driven movement
- Portal-based teleportation with color pairing
- Dynamic laser hazards and moving obstacles
- Button-activated doors and environmental logic
- Shooting mechanics tied to scoring and progression
- Neon-inspired visual styling and HUD feedback

The gameplay blends accuracy, timing, and spatial reasoning to create an immersive 3D experience.

## Gameplay Mechanics

### Player Control

- First-person perspective
- Keyboard-based movement for forward, backward, and strafing
- Yaw and pitch controlled via keys
- Mouse click to capture input, aim, and fire portal bullets

### Physics

- Gravity and falling mechanics are applied
- Collision detection prevents passing through walls and obstacles
- Player movement is confined to the playable room
- On death, the player respawns at the starting location

### Health System

- Player has a limited number of lives
- Contact with lasers, moving obstacles, or locked doors reduces lives
- Losing all lives triggers a game-over state with a reset option

## Portal System

- Two distinct portal colors
- Portals can only be placed on valid wall surfaces
- Portals are paired by color and allow teleportation between surfaces
- Teleportation includes a cooldown to prevent immediate re-entry
- Using portals contributes to the player’s score
- Each wall tile can host only one portal; placing a new portal replaces the existing one and updates pairing

## Environmental Interaction

### Buttons

- Floor buttons activate doors or disable hazards
- Activation requires proximity and unobstructed line-of-sight
- Visual feedback indicates activation state

### Doors

- Doors visually indicate locked or unlocked states
- Doors unlock when required environmental conditions are met

### Laser Fields

- Static vertical laser barriers and oscillating horizontal laser bars
- Contact with lasers causes damage or death
- Lasers are rendered using layered geometry for a strong neon barrier effect

### Moving Platforms and Obstacles

- Level-specific moving hazards with predefined horizontal or vertical paths
- Colliding with obstacles reduces lives or kills the player
- Safe zones are maintained near spawn points and interactive elements

## Cheat Mode

- Toggle on or off by pressing C
- Allows the player to pass through lasers without losing lives
- HUD displays “Cheat: ON” when active
- Does not bypass locked doors or level-completion walls

## Combat and Shooting

### Gun Mechanics

- Neon-styled first-person gun model
- Gun is visible only in first-person mode
- Used for aiming and firing portal bullets

### Bullets

- Bullets travel forward with a limited lifetime
- Bullets collide with environment geometry
- Successful hits place portals on valid wall surfaces
- Portal placement updates wall appearance and awards points

### Accuracy and Stats

- Tracks shots fired, successful hits, and accuracy percentage
- Accuracy and hit count contribute to scoring and completion bonuses

## Scoring and HUD

### Scoring

- Points awarded for placing portals, teleportation usage, and button activation
- Level completion grants bonuses based on speed and shooting accuracy

### HUD Display

- Displays lives, elapsed time, portals used, accuracy, score, and current level
- Pause and status overlays provide instructions and feedback
- Circular cyan crosshair centered on screen for aiming

## Levels and Objectives

### Early Levels

- Introduce buttons, basic laser fields, and static hazards
- Objective is to activate the button, avoid hazards, and reach the exit

### Advanced Levels

- Introduce moving obstacles and oscillating horizontal lasers
- Increased timing and spatial complexity
- Objective is to use portals and movement to traverse hazards and reach the exit

### Level Completion

- Completion screen summarizes score, time, and bonuses
- Players may proceed to the next level or restart

## Game Loop

1. Player spawns at the center of the room
2. Input is captured to begin gameplay
3. Navigate hazards using movement and portal mechanics
4. Activate buttons to unlock doors or alter hazards
5. Avoid lasers and moving obstacles
6. Use paired portals to solve spatial puzzles
7. Reach the exit to complete the level
8. Earn bonuses or trigger game over if all lives are lost

## Visual and Rendering Features

- Tiled floor grid and solid ceiling defining the play area
- Outlined wall tiles designed for portal placement
- Colored circular portal visuals
- 2D HUD rendered using orthographic projection
- Neon-styled gun composed of primitive geometry
- Layered laser geometry for strong visual barriers
- Circular crosshair centered on screen

## Technical Notes

- Rooms are built from tiled wall surfaces optimized for portal placement
- Portal pairing and replacement logic ensures one portal per wall surface
- Bullets use simple forward motion, lifetime tracking, and collision detection
- Moving obstacles and oscillating lasers scale with level difficulty
- Timers and stat trackers record playtime, portal usage, accuracy, and score
