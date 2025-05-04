+++
draft = false
title = 'Studycase: Multiplayer test with Netcode for GameObjects'
tags = ['Test', 'Pinned', 'Unity', 'Netcode']
categories = ['Test']
description = "A studycase project as an entry test for a company. Showcasing realtime players interacting via a shared room."
+++

## PROJECT LINK

[{{<icon "github">}} Project link](https://github.com/hiiamtrv/unity-netcode-curly-test)

[{{<icon "book">}} Release note](https://github.com/hiiamtrv/unity-netcode-curly-test/releases/tag/curly-test)

## TECH STACK

|                   |                                    | 
|:------------------|:-----------------------------------|
| **Platforms**     | Windows                            | 
| **Game Frontend** | Unity, Netcode for GameObjects     | 
| **Backend**       | Unity, Netcode for GameObjects Gin | 

## UNITY NETCODE CURLY TEST

![Game Overview](https://github.com/user-attachments/assets/1f95a5a4-1f2f-4ba7-8f70-bdf2f3890dba)

### Overview

- Create room and enter room by known IP and Port.
- Brief walk, jump with decent synchronization.
- Charge Forward feature.

### Create room

1. Look at the UI group in the top-left corner. If it is about join room UI, press ">>Create Room" to back to required
   UI group.
2. Enter your favourite port, as long as it does not overlap with other services.
3. Press "Create Room", then your room is created with your player fell from the sky.
4. The text below will be updated with your IP and port. Tell no one but your fellows to crowd the room.
5. (Optional) Press "Close Room" to close your room and kick all your friends out.

### Join room

1. Look at the UI group in the top-left corner. If it is about create room UI, press ">>Join Room" to back to required
   UI group.
2. Enter your friend's IP and port to join with them.
3. Press "Join Room", then your man will fall from the sky (again ?).
4. (Optional) Press "Leave Room" to leave your friend and back to real world.

### Controls

- WASD or Arrows: Move the character in the third-person-perspective.
- Mouse: Look around
- Space: Jump
- Left Click (hold and release): Perform a Charge forward.
- Right Click: Cancel the Charge (or WIP Skill)