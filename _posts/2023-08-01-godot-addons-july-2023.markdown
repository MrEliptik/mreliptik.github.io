---
title: "10 awesome addons for Godot 4"
layout: post
date: 2023-08-01 08:00
image: /assets/images/godot_addons_july_2023/godot_addons_july_2023_cover.png
headerImage: true
tag:
- gamedev
- godot
- godot 4
- addons
category: blog
author: mreliptik
hidden: false # don't count this post in blog pagination
description: I'm presenting you 10 awesome addons compatible with Godot 4
---

I've done [multiple videos](https://youtube.com/playlist?list=PLHepjQmYsQujq8kC98gcZwYlTEcbzDnt5) about awesome addons for Godot, but never specifically for Godot 4! I finally decided to do it, and you can watch the video below 👇

<iframe width="560" height="310" src="https://www.youtube.com/embed/IN6Z3C7V_Uk" frameborder="0" allowfullscreen></iframe>

I thought making the list available in text form would also be a great idea, and that's why I'm making this post, so let's start!

### 1 - Constraint Solving

![Constraint solving][constraint_solving]

Let’s start with [Constraint Solving](https://github.com/AlexeyBond/godot-constraint-solving) by **AlexeyBond**, an addon to calculate wave function collapse and generic constraint solving. 

Procedural generation is very popular and for a good reason: it’s super cool. While there are a lot of tutorials on the subject, it can be a bit daunting to get your hands dirty with such algorithms. 

That’ where this addon comes into play. It supports both **Tilemap** and flat **Gridmap**, backtracking, multithreading and a generic implementation of a constraint solving algorithm! It’s even capable of learning from an example of a valid map, that’s pretty cool.

![Map example][map_example]

### 2 - Deformable Mesh

![Deformable mesh][deformable_mesh]

[Deformable Mesh](https://github.com/cloudofoz/godot-deformablemesh) by **cloudofoz** is an amazing 3D addon allowing you to bend and deform meshes using a sphere.

You customize your deformer, add a `DeformableMeshInstance` and you’re ready to deform any mesh. From the examples, you can see how useful it can be to animate limbs, or other objects as if something was going through it. I love seeing more cool 3D addons like that for Godot.

### 3 - Wiggle bone

![Wiggle bone][wiggle_bone]

Continuing with cool 3D stuff, [Wigglebone](https://github.com/detomon/wigglebone) by **detomon**, allows you to create cool wiggly movement to any bones of a `Skeleton3D`. It reacts to animated and global motion. Movement looks very natural as its reacting to acceleration. You have a bunch of properties to setup the movement to what you like, so don’t wait and make your bones wiggle!

### 4 - WigglyAppendage2D

![Wiggly appendage 2D][wiggly_appendage_2D]

[Wiggly Appendage 2D](https://github.com/Tameno-01/GodotWigglyAppendage2D) by **Tameno-01** is similar to the previous addon we’ve seen but for 2D this time. It has more ways of controlling the wigglyness though and can also be used for longer things like tails, ropes, etc…

It can handle lots of different movement types, be scaled and even flipped, pretty cool stuff!

### 5 - Third person camera

![Third person camera][tpc]

Let’s go back to 3D with [Third Person Camera](https://github.com/JeanKouss/godot-third-person-camera) by **JeanKouss**. Let’s be real, a good camera is essential for a good game, but it can be extremely painful to implement, especially a third person one. Thankfully, this addon gives you a quick start with a camera you can rotate, put closer or further away, with angle limits, etc...

### 6 - Auto Layout

![Auto layout][auto_layout]

I know most of you don’t like UI, but thanks to [Auto Layout](https://github.com/don-tnowe/godot-auto-layout) by **don-tnowe**, arranging your node into container has never been easier. If you’re familiar with Figma’s auto layout feature, you’ll be glad to see it arrive in Godot. It’s super easy to use, select the nodes you want and hit shift+A, it automatically put your nodes into a container and by keeping pressing A you switch between multiple layout types. There’s even a small popup showing you the layout type you’re using. Super simple, yet very effective.

### 7 - Panku Console

![Panku console][panku]

Talking about things we don’t like, debugging is up there. Thanks to [PankuConsole](https://github.com/Ark2000/PankuConsole) by **Ark2000**, this will not be the case anymore! 

Panku is a real time debugging toolkit for Godot with which you can interact with your scripts and objects at runtime. One of the coolest feature is the multi window UI you can use, allowing you to make use of this 4 screens setup you were struggling to justify. Other that that, you can create a developer console, a logging window, a data controller that automatically put all your export var into a neat window, an expression monitor and much more! Because it's modular, you can even add or remove features as you see fit.

### 8 - Mirror

![Mirror][mirror]

Mirrors are pretty cool and that’s why we look at [Mirror](https://github.com/Norodix/GodotMirror) by **Norodix**. To be honest, they’re not that hard to create, but it’s always good to have a simple addon making things faster for you. This one is just a mirror you can drop into your game, with the ability to set the tint, size, visual layers and distortion.

### 9 - RL agents

![RL agents][rl_agents]

[RL agents](https://github.com/edbeeching/godot_rl_agents_plugin) by **edbeeching** is an addon to bridge the gap between your game and machine learning algorithms made in Python. It supports 3 reinforcement learning frameworks, 2D and 3D gamers and diverse AI sensors to use with your agent. This can be especially interesting for researchers, students or developers wanting to create ML based agents. There’s even a [paper](https://arxiv.org/abs/2112.03636) to read more about this project.

### 10 - Inventory system

![Inventory system][inventory_system]

And the last addon of this list is [Inventory System](https://github.com/expressobits/inventory-system) by **expressobits**. Making a great inventory system can be a pain, but thanks to this addon, you’ll be able to have a clean one in seconds. You have an inventory with slots, a craft system, a hotbar, separate UI inventory logic and much more.

This feels like a very complete tool to get you started making awesome games.


### Thank you for reading!

And with that, we finished this list of 10 awesome addons for Godot 4. Share with me other addons you like and other topics you’d like to me to cover.

If you want to help me continue making these, you can support me on Patreon! It starts at 1$ per month and you can get early access, behind the scenes, exclusive contents and much more 🙂 

Join now at [patreon.com/mreliptik](https://patreon.com/mreliptik)!

[![Patreon image][patreon]](https://patreon.com/mreliptik)

Byyye👋



[patreon]: /assets/images/become_patreon.png
[constraint_solving]: /assets/images/godot_addons_july_2023/constraint_solving.png
[map_example]: /assets/images/godot_addons_july_2023/map_example.png
[deformable_mesh]: /assets/images/godot_addons_july_2023/deformable_mesh.gif
[wiggle_bone]: /assets/images/godot_addons_july_2023/wiggle_bone.gif
[wiggly_appendage_2D]: /assets/images/godot_addons_july_2023/wiggly_appendage_2D.png
[tpc]: /assets/images/godot_addons_july_2023/third_person_camera.png
[auto_layout]: /assets/images/godot_addons_july_2023/auto_layout.gif
[panku]: /assets/images/godot_addons_july_2023/panku.png
[mirror]: /assets/images/godot_addons_july_2023/mirror.png
[rl_agents]: /assets/images/godot_addons_july_2023/rl_agents.png
[inventory_system]: /assets/images/godot_addons_july_2023/inventory_system.gif
