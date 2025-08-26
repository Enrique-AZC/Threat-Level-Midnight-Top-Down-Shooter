# Threat Level Midnight — Top-Down Shooter

## Overview  
**Threat Level Midnight — Top-Down** is a browser-based, canvas-rendered 2D shooter inspired by retro arcade gameplay and modern bullet-hell mechanics.  
Developed using **vanilla JavaScript**, **HTML5 Canvas**, and **Web Audio API**, the game explores technical aspects of **real-time rendering**, **state management**, **procedural combat mechanics**, and **UI integration** in a single-page application context.

The project demonstrates the application of object-oriented patterns in JavaScript to structure core gameplay entities (**Player, Enemy, Boss, Bullet**) alongside rendering and physics systems. The design emphasizes **performance**, **accessibility**, and **minimal dependencies**, relying solely on the web platform.

---

## Features  

-  **Top-Down Shooter Mechanics**  
  - WASD movement  
  - Mouse aiming & shooting  
  - Dash with invincibility frames  

-  **Dynamic Enemies**  
  - Procedural patrol/chase AI  
  - Collision handling with map solids  
  - Projectile-based combat  

-  **Boss System**  
  - Multi-phase boss (**TOBY**) with distinct attack patterns:  
    - Directed shots  
    - Cross burst  
    - Bullet rain  

-  **Adaptive Difficulty**  
  - Time-based scaling system  
  - Procedural spawning with parameter adjustments (HP, speed, spawn interval)  

-  **HUD & UI Overlay**  
  - Health bar with dynamic states  
  - Combo multiplier with decay  
  - Score and difficulty scaling indicators  
  - Overlay panels for **Pause, Game Over, Victory**  

-  **Synthesized Audio**  
  - Procedural sound effects via Web Audio API  
  - No external audio assets required  

-  **Visual FX**  
  - Camera shake on impact  
  - Blood particle effects  
  - Screen vignette post-processing  
  - Tile-based map with overlayed textures  

---

## Controls  

| Key / Action   | Function   |
|----------------|------------|
| **WASD**       | Movement   |
| **Mouse**      | Aim        |
| **Left Click** | Shoot      |
| **Spacebar**   | Dash (with cooldown) |
| **R**          | Restart    |
| **Esc**        | Pause / Resume |

---

## Technical Architecture  

- **Core Classes**  
  - `Player`: Movement, shooting, dash mechanics, health management  
  - `Enemy`: Patrol, chase AI, burst shooting  
  - `Boss`: Multi-phase attack cycles and adaptive AI  
  - `Bullet`: Projectile logic with collision and lifespan management  

- **World State**  
  - Central `world` object manages entities, timers, difficulty progression, and UI updates  

- **Rendering Pipeline**  
  - **Background**: Pre-rendered map image  
  - **Entities**: Iterative draw calls (player, enemies, bullets)  
  - **Effects**: Particle systems (blood, hit sparks)  
  - **PostFX**: Radial vignette and CRT-style scanlines  

- **Audio System**  
  - Pure JavaScript synthesis using oscillators and gain nodes  
  - Dynamic parameters (frequency, waveform, duration)  

---

## Installation & Execution  

### Prerequisites  
- Modern web browser with **HTML5 Canvas** and **Web Audio API** support (Chrome, Firefox, Edge, Safari).  
- No external dependencies or build tools required.  

### Run Locally  
1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/threat-level-midnight-topdown.git
   cd threat-level-midnight-topdown
2. Open `index.html` in a browser.  
3. Play.  

---

## Academic Relevance  

This project is a practical study of:  
- **Real-time interactive systems** within browser environments  
- **Lightweight game engine design** using JavaScript without frameworks  
- **Procedural difficulty scaling** and adaptive AI  
- **Human–Computer Interaction (HCI)** principles applied to responsive HUD and user feedback  
- **Audio synthesis for games**, avoiding reliance on external media assets  

---

## Future Work  

- Map randomization & procedural generation  
- Extended boss roster with unique mechanics  
- Power-ups and weapon variety  
- Persistent scoring / leaderboard system  
- Mobile/touch support  
