## DRONEFALL

### A 3D aerial combat shooter prototype built in Unreal Engine 5.8

> Pilot your combat drone through a cyberpunk industrial arena. Engage waves of enemy drones, dodge incoming fire, and face off against a powerful boss drone in intense aerial dogfights.

---

##  Gameplay

You control a fully maneuverable **combat drone pawn** in a neon-lit cyberpunk environment. Enemy drones spawn in waves, each armed with energy blasters. Survive the onslaught, collect health pickups, and take down the **Boss Drone** to win.
Options to play both in Third Person or First Person are available. 

###  Gameplay Demo

First Person
https://github.com/user-attachments/assets/ca165d20-02a5-407b-8232-d06a5ff6e3f7





Third Person
https://github.com/user-attachments/assets/3292c8e7-0f80-4efe-942f-109f647907d5



---

###  Combat & Boss Fight

https://github.com/user-attachments/assets/0c19db46-fb87-4033-bb74-be08614a279a

---

##  Features

| Feature | Description |
|---------|-------------|
| **Aerial Drone Combat** | Full 6DOF-style drone movement with look, move, and fire input actions |
| **Wave Spawner System** | `BP_DroneSpawner` and `BP_SphereSpawner` manage enemy wave generation |
| **Boss Battle** | A dedicated `BP_DroneBoss` with unique mesh and boss blaster beam |
| **Energy Blaster Weapons** | Player, enemy, and boss each have distinct blaster beam variants with custom materials |
| **Damage System** | Blueprint Interface (`BI_Damageable`) for a unified damage pipeline across all actors |
| **Floating Damage Text** | On-hit damage numbers via the SimpleDamageText system |
| **HUD & Health UI** | Overlay HUD with health bar widget (`WBP_Health`, `WBP_OverlayHUD`) |
| **Dynamic Crosshair** | Modular crosshair system with separate top/bottom/left/right/center elements |
| **Muzzle Flash FX** | Niagara-powered muzzle flash and beam burst particle effects |
| **Cyberpunk BGM** | Multiple cyberpunk music tracks with level ↔ boss music crossfade transitions |
| **Cyberpunk Environment** | Industrial cyberpunk arena built with the CyberpunkIndustries asset pack |

---

##  Project Architecture

```
Content/
├── Assets/
│   ├── BlasterBeam/        # Beam mesh & materials (player, enemy, boss variants)
│   ├── Drone/              # Drone & DroneBoss meshes, materials, textures
│   ├── DronePawn/          # Player-controlled drone pawn blueprint
│   ├── FX/                 # Niagara beam burst effects
│   ├── Input/              # Enhanced Input — IMC_Drone, IA_Move, IA_Look, IA_Fire
│   ├── LevelSphere/        # Level sphere collectible mesh & materials
│   ├── SmallSphere/        # Small sphere pickup mesh & materials
│   ├── Sounds/
│   │   ├── BGM/            # Background music tracks (cyberpunk)
│   │   └── Drone/          # Drone energy rifle SFX
│   ├── Textures/           # Crosshair textures
│   └── UI/                 # HUD class, health bar & overlay widgets
│
├── BlueprintInterfaces/
│   └── BI_Damageable       # Damage interface implemented by all destructible actors
│
├── Blueprints/
│   ├── BP_DronePawn         # Player pawn — drone with full aerial movement
│   ├── BP_Drone             # Enemy drone AI
│   ├── BP_DroneBoss         # Boss drone with enhanced attacks
│   ├── BP_DroneSpawner      # Wave-based drone spawning system
│   ├── BP_SphereSpawner     # Sphere pickup spawner
│   ├── BP_BlasterBeam       # Base blaster beam projectile
│   ├── BP_PlayerBlasterBeam_Child   # Player beam variant
│   ├── BP_EnemyBlasterBeam_Child    # Enemy beam variant
│   ├── BP_BossBlasterBeam   # Boss beam variant
│   ├── BP_SmallSphere       # Collectible sphere pickup
│   └── BP_DronefallGameMode # Game mode configuration
│
├── CyberpunkIndustries/     # Environment art — meshes, materials, textures
├── Maps/
│   ├── Botlevel.umap        # Main gameplay level
│   └── TestingMap.umap      # Development testing level
└── ...
```

---

##  Controls

| Action | Input |
|--------|-------|
| **Move** | `WASD` / Left Stick |
| **Look** | Mouse / Right Stick |
| **Fire** | Left Mouse Button / Right Trigger |
| **StrafeUp** | Spacebar / Right Bumper |

> Built with Unreal Engine's **Enhanced Input System** — fully rebindable via `IMC_Drone` input mapping context.

---

##  Tech Stack

| | |
|---|---|
| **Engine** | Unreal Engine 5.8 |
| **Language** | Blueprints (100%) |
| **Input** | Enhanced Input System |
| **VFX** | Niagara Particle System |
| **Audio** | AudioComponent with fade-based music transitions |
| **UI** | UMG Widgets |
| **Platform** | Windows (Win64) |

---

##  Soundtrack

All sound effects used in this project were sourced from Pixabay and are free to use under the Pixabay Content License. No ownership of the original audio assets is claimed.

# Tracks-

| `leberch-cyberpunk` | Ambient cyberpunk groove |

| `monume-cyberpunk-music` | Atmospheric level BGM |

| `prettyjohn1-suspense-cyberpunk` | Tension & suspense |

| `kulakovka-hard-cyberpunk` | Hard-hitting boss fight music |


---

## Under Development

This project is actively being improved as a learning-focused game development project.

Planned and ongoing improvements include:-

Improved HUD with additional gameplay information and features.

Start Screen & Settings UI with improved navigation and presentation.

Improved Enemy Behaviour with more responsive and engaging AI.

Continued improvements to gameplay mechanics, systems, and overall polish.

Most of the future development on this project will be focused on learning and experimentation rather than preparing it for commercial publishing. The project will continue to evolve mechanically as I learn and implement new game-development concepts.

This is an improvised learning project inspired by Stephen Ulibarri's tutorials, with additional systems, modifications, and experimentation implemented along the way to deepen my understanding of Unreal Engine and game development.


##  License

This project is for educational and portfolio purposes.  
Third-party assets were sourced from fab (CyberpunkIndustries, NW_MuzzleFX, SimpleDamageText, CrosshairFreePack) are subject to their respective licenses.

---

