+++
draft = false
title = 'Studycase: Hack and Slash prototype with Unreal Engine'
tags = ['Test', 'Pinned', 'Unreal Engine 4.4', 'Hack ans Slash', '3D', 'Combo Development', 'AI']
categories = ['Test']
description = "A studycase project as an entry test for a company. Showcasing a comboed actions between a Player and an AI"
+++

> if any image is not shown, please open it in a new tab

## PROJECT LINK

[{{<icon "github">}} Project link](https://github.com/hiiamtrv/unreal-hacknslash)

[{{<icon "book">}} Release note](https://github.com/hiiamtrv/unreal-hacknslash/releases/tag/Prototype)

## DEMO VIDEO
{{< gdrive 1o8dxixOkT3hxt2ii9trOSi-G7g1eg5vJ >}}

## TECH STACK
|                   |                                                                                          | 
|:------------------|:-----------------------------------------------------------------------------------------|
| **Platforms**     | Windows                                                                                  | 
| **Game Frontend** | Unreal Engine 4.4                                                                        | 
| **Showcasing**    | Combo Chain Subsystem, AI Behaviour Tree, Animation Mixing, Blueprints, C++, Data Assets | 

## ⚙️ TECHNICAL INFORMATION

- **Engine**: Unreal Engine 5.4.4
- **Source**: Blueprint & C++
- **Demo video**: [Here](https://drive.google.com/file/d/1o8dxixOkT3hxt2ii9trOSi-G7g1eg5vJ/view?usp=drive_link) or in
  the download panel below.

![image](https://github.com/user-attachments/assets/02a3aada-d38b-49b7-9f8e-ff7c626f899f)

## 🎮 HOW TO PLAY

| Action       | Input         |
|--------------|---------------|
| Move         | `WASD`        |
| Jump         | `Space`       |
| Light Attack | `Left Click`  |
| Heavy Attack | `Right Click` |
| Dodge Left   | `Q`           |
| Dodge Right  | `E`           |

> 💡 Try mixing light and heavy attacks with directional dodges to explore different combos and behavior reactions.

---

## ⚙️ FEATURE DECISIONS

## 🔗 COMBO SYSTEM

While not the core focus of the current test, the combo system is **critical** to gameplay. It defines how both *
*players and AIs perform actions**, and it decides the flexibility allows for dynamic, scalable design.

### ✅ Design Goals

- Scalable and designer-friendly
- Clear separation between combo animation and logic tree
- Lower dependencies between design combo flows and present combo action

After extensive iteration, the final structure includes the following components:

### 🧩 Components

#### `ComboInput`

- Represents basic input actions (Light Attack, Heavy Attack, Counter, Dodge, etc.)
- Used to traverse the combo tree

#### `ComboTree`

- A **Trie-like data structure** for navigating input sequences
- Starts from a root (default state) and moves through valid input chains

#### `ComboSubsystem`

- Central system for managing combo trees
- Builds and manages combo trees for all relevant actors

#### `ComboRunner`

- Manages player interaction with combo trees
- Fetches tree from `ComboSubsystem`, progresses based on input
- Validates input at each stage to determine the next combo node

#### `ComboAnimationPlayer`

- Executes animations based on current combo state
- Communicates with the `ComboRunner` to play appropriate animations
- Uses Animation Montages with **Combo Window Notify States** to control combo timing windows
- (WIP) use "Combo Fastfoward State" to increase combo speed and smooth

#### 📊 Diagrams

![Combo TreeNode](https://github.com/user-attachments/assets/7c9cd28c-afaf-48bb-ab9e-8dd16c266da5)

![Combo Tree Architecture](https://github.com/user-attachments/assets/c7a63f77-80c9-4ddc-8441-bf136c910f54)

#### 🗃️ Data Asset views

![Combo Data Node Info](https://github.com/user-attachments/assets/189be8d5-7f67-4919-92ee-a00cd1aff36b)

![Combo Animation Info](https://github.com/user-attachments/assets/e03fab40-b620-4706-bf93-aa6e87d3809c)
---

## 🤖 AI BEHAVIOR

Thanks to Unreal Engine’s native support for:

- **Behavior Trees**
- **Blackboards**
- **BT Tasks** and **BT Conditions**

AI logic is cleanly implemented and **developer-efficient**.

### AI Perception

AI can detect the player through:

- Sight
- Sound
- Custom scripted triggers

---

### 🧭 AI Modes

> ⚔️ AI can execute combos, such as Player do because they send the same input flow as player's.

> ⚔️ To briefly demonstrate fighting impacts, hit actions now PUSH targets away instead of causing damages.

#### 🟡 Wander Mode

- AI walks between 4 predefined waypoints
- Pauses at each waypoint for ~8 seconds
- Randomly plays idle/fun animations
- When disengaging from combat, AI returns to the **nearest** waypoint

#### 🔴 Engage Mode

- AI approaches the player when in range
- Stops at appropriate combat distance
- Behavior includes:
    - **Evading** player attacks
    - **Counter-attacking** upon successful evade
    - **Flanking** if behind the player

#### 🌲 Behaviour Tree

![image](https://github.com/user-attachments/assets/3e8d2709-b528-4659-9b6b-5fea1fc9dea2)

---

## 🕺 PLAYER ANIMATION

- Base animations reused from **Unreal Engine Mannequin**
- Customizations added for immersion and responsiveness

### Enhancements:

- Randomized idle animations to add realism
- **Player** automatically draws sword when:
    - Enemy is near
    - Enemy is visible via the camera system
- **AI** automatically draws sword when see or hear Player (via AI Senses).

---