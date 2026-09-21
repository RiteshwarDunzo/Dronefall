# 🛸 DRONEFALL

### A 3D aerial combat shooter built in Unreal Engine 5.8

> Pilot your combat drone through a cyberpunk industrial arena. Engage waves of enemy drones, dodge incoming fire, and face off against a powerful boss drone in intense aerial dogfights.

---

## 🎮 Gameplay

You control a fully maneuverable **combat drone pawn** in a neon-lit cyberpunk environment. Enemy drones spawn in waves, each armed with energy blasters. Survive the onslaught, collect health pickups, and take down the **Boss Drone** to win.

### 📹 Gameplay Demo

<!-- VIDEO 1: Replace the link below with your gameplay video URL -->
<!-- Example: https://github.com/user-attachments/assets/your-video-id -->

https://github.com/user-attachments/assets/VIDEO_1_PLACEHOLDER

---

### ⚔️ Combat & Boss Fight

<!-- VIDEO 2: Replace the link below with your boss fight / combat video URL -->
<!-- Example: https://github.com/user-attachments/assets/your-video-id -->

https://github.com/user-attachments/assets/VIDEO_2_PLACEHOLDER

---

## ✨ Features

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

## 🏗️ Project Architecture

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

## 🎯 Controls

| Action | Input |
|--------|-------|
| **Move** | `WASD` / Left Stick |
| **Look** | Mouse / Right Stick |
| **Fire** | Left Mouse Button / Right Trigger |

> Built with Unreal Engine's **Enhanced Input System** — fully rebindable via `IMC_Drone` input mapping context.

---

## 🔧 Tech Stack

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

## 🚀 Getting Started

### Prerequisites

- [Unreal Engine 5.8](https://www.unrealengine.com/) installed via the Epic Games Launcher

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/Dronefall.git
   ```

2. **Open the project**
   - Launch Unreal Engine 5.8
   - Open `Dronefall.uproject`

3. **Play**
   - Open `Content/Maps/Botlevel` 
   - Hit **Play** (Alt+P)

---

## 📁 Key Blueprints

| Blueprint | Role |
|-----------|------|
| `BP_DronePawn` | The player. Handles movement, camera, firing, health, and input. |
| `BP_Drone` | Enemy drone. AI-driven with energy rifle attacks. |
| `BP_DroneBoss` | Boss encounter. Larger mesh, boss beam, tougher to kill. |
| `BP_DroneSpawner` | Places waves of enemy drones into the arena. |
| `BP_DronefallGameMode` | Sets the default pawn, HUD, and game rules. |
| `BI_Damageable` | Interface that standardizes damage messaging across actors. |

---

## 🎵 Soundtrack

| Track | Vibe |
|-------|------|
| `leberch-cyberpunk` | Ambient cyberpunk groove |
| `monume-cyberpunk-music` | Atmospheric level BGM |
| `prettyjohn1-suspense-cyberpunk` | Tension & suspense |
| `kulakovka-hard-cyberpunk` | Hard-hitting boss fight music |

---

## 📜 License

This project is for educational and portfolio purposes.  
Third-party assets (CyberpunkIndustries, NW_MuzzleFX, SimpleDamageText, CrosshairFreePack) are subject to their respective licenses.

---

<p align="center">
  Built with 💜 in Unreal Engine 5.8
</p>
