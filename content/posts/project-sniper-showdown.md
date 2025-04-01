+++
draft = false
title = 'WIP Project: Sniper Showdown'
tags = ['Demo', 'Pinned', 'WIP', 'Unity', 'Fishnet', 'Golang', 'Docker']
categories = ['Demo']
description = "Showcase of my WIP multiplayer game: Sniper Showdown"
weight = 1
+++

## TECH STACK

|                          |                                    | 
|:-------------------------|:-----------------------------------|
| **Platforms**            | WebGL, Windows                     | 
| **Game Frontend**        | Unity, Fishnet-Network, Websocket  | 
| **Backend**              | Unity, Fishnet-Network, Golang Gin | 
| **Programing Languages** | C#, Golang                         | 
| **Support Tech**         | Docker, Nginx, Google Cloud, Bash  | 

## OVERVIEW

**Game Name**: Sniper Showdown

**Genre**: Action, Shooter

**Tags**: Shooter, Multiplayer, Tactical, Top-down, PvP

> *"SNIPER SHOWDOWN is a top-down competitive game simulating gunfights in darkness, where every move or shot has a
significant impact."*

## DEMO

{{< gdrive 1VeJdzLrudndnJBQ5KRZlLBdAKekC-xvU >}}

## ARCHITECTURE

{{< gdrive 1CtWAWpDF2y4x6ObDB3-Iy7cm0UBCR69I >}}

## CONTROLS

- **WASD** – Move

- **Mouse** – Look around

- **Left Click** – Shoot (Sniper Rifle & Shotgun) / Throw (Smoke)

- **Right Click** – Aim (Sniper Rifle)

- **1** – Equip Sniper Rifle

- **2** – Equip Shotgun

- **4** – Equip Smoke

- **Left Ctrl** – Toggle mouse locking

## FEATURES

### Lobby

When the game starts, the player enters the lobby screen.

Click **ENTER LOBBY** to connect. The player will be queued until they are assigned to an upcoming game, leave the
lobby, or disconnect (by closing the game or clicking **DISCONNECT**).

While waiting, an indicator displays the number of players currently in the lobby.

### Main Game

In the current version, players are matched with a bot opponent. PvP mode will be enabled once action stability is
ensured.

You can control your character (the blue sphere) using the controls above.

Note that bullet traces and smoke effects are visible to all players—use them strategically.

After the game ends, players will return to the Lobby screen.

## FUTURE PLANS

- [ ] Add more in-game items and environment objects.
- [ ] Login via Google Accounts (guests is still enabled but with limitations).
- [ ] Weekly/Monthly records & rankings & leaderboard.