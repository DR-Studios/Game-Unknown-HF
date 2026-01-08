---
title: Game-Unknown
emoji: 🎮
colorFrom: green
colorTo: blue
sdk: gradio
sdk_version: "3.50.2"
app_file: app.py
pinned: false
---



🎮 Game‑Unknown
Is A 3D sandbox where you pick a model or Load your own model(Encouraged), pick a Preset world enviroment, and enjoy.

🧠 Concept:
(see Note from Dave below)


🔧 How It Works

User loads token → Authenticates 

Upload your Custom .gld, .obj, or ghlt model (or if got none: Selects a one of the preset Default Model)

Chose  A World Enviroment From a dropdown menu

Click on the "Enter" button the screen and enjoy 

🗂️ File Highlights
app.py — backend logic

3dmain.py — sandbox engine

index.html / new index.html — frontend entry points

GameConfig — defines world, player, enemy setup

*.glb — 3D assets (Greek city, male.glb, Dragon1.glb, etc.)

🌍 Preset Worlds
Greek city

Abandoned warehouse

Dragon’s lair

Unknown ruins (coming soon)

🧙‍♂️ Player Models
male.glb

Custom GLB uploads supported

🧪 Try It Out


# Note from Dave:
   what my end result/ hope to Accomplish is: A HF Space that consist of a GUI that lets you choose from a preset of 3d world environments, then user uploads  There own: glb, obj, .ghlt  3d Model (or chose one of preset models from drop down menu), then choose from a couple of creator(me) defined world environments, and then hits "Enter" button on screen to jump on in a game world environment and tryout, experiment, kill some monsters or just !@$!@ around and Explore (with there model in a 3d environment, try it out, or show it off, etc..) a 3d game environment (choose from various preset environments [currently only 1 uploaded greek city.glb plan on more]) and do some stuff (not fully defined yet[ ideas i got though small open world can walk, talk, shoot simple npcs, fly, box others would be cool otherwise npc , explore shit like that]) and if i would be lucky and make a stretch a small lobby so multiple users could possibly interact with each other and of course they for any of this probably would have to enter in there own hf-tolken. { in summary this is the mission plan on this "Game-Unknown" project }