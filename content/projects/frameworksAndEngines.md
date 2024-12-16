---
title: "Frameworks & Engines"
date: 2023-06-03T19:53:00Z
description: "Information I gathered over the years about game tools and engines"
tags: ["project", "gamedev"]
draft: false
type: "projects"
layout: "simple-comment"
---
We live in such a wonderful age to be software developers. A few decades back, game development was a pretty challenging task even for intermediate programmers. Nowadays it is very easy to get directly into game development. Modern hardware is powerful, and in fact, a moderately powerful laptop is enough for development. Also, indie devs nowadays have access to a rich library of tools. Just choose the right one... yes? 

Well, the more alternatives, the better, sure thing, but it comes with one drawback, how do I choose the right tool for my dream project when we have so many options? 

That's the reason why I started my first blog. I wanted to write articles about my "hunt for the best tool". In past years I've tried almost every at least little known framework/engine and now I want to tell you about my experiences in the form of an informational table with a short product description.

I've tried to be as objective as I could. If you have any suggestions, just put a comment below :)

# Frameworks/Engines

Explanation: 

- **Name:** name of the product and link to its official web page.
- **Language:** primary programming language. Excludes bindings or any other programming languages used as extensions.
- **Target platforms:** platforms on which exported software can run. Includes only official supported ones. **Will add consoles and other misc platforms later.*
- **Editor:** support for official editor
- **Crossed out:** no longer supported or archived

{{<table "table table-dark table-bordered">}}
| Name | Language | Target platforms | Open source | Editor |
| :---------------------------------------------: | :------------------: | :--------------------------------: |:--: |:--:|
| [Amulet](http://www.amulet.xyz/)                | Lua                  | win, linux, mac, ios, android, web | ✔️  | ❌ |
| [Bevy](https://bevyengine.org/)                 | Rust                 | win, linux, mac ios, web           | ✔️  | ❌ |
| [Cocos2D](https://www.cocos.com/en)             | Lua/JS/C++           | win, linux, mac, ios, android, web | ✔️  | ✔️ |
| [Defold](https://defold.com/)                   | Lua                  | win, linux, mac, ios, android, web | ✔️* | ✔️ |
| [Duality](https://adamslair.github.io/duality/) | C#                   | win, linux, mac                    | ✔️  | ✔️ |
| [Ebiten](https://ebitengine.org/)               | Go                   | win, linux, mac, ios, android, web | ✔️  | ❌ |
| [FNA](https://fna-xna.github.io/)               | C#                   | win, linux, mac ios,               | ✔️  | ❌ |
| [Flax Engine](https://flaxengine.com/)          | C++/C#               | win, linux, mac ios, android       | ✔️  | ✔️ |
| [HaxeFlixel](https://haxeflixel.com/)           | Haxe                 | win, linux, mac ios, android, web  | ✔️  | ❌ |
| [Heaps IO](https://heaps.io/)                   | Haxe                 | win, linux, mac, ios, android, web | ✔️  | ✔️ |
| [Löve2D](https://love2d.org/)                   | Lua                  | win, linux, mac, ios, android      | ✔️  | ❌ |
| [Monogame](https://www.monogame.net/)           | C#                   | win, linux, mac, ios, android      | ✔️  | ❌ |
| [O3DE](https://www.o3de.org/)                   | C++/Lua              | win, linux, android                | ✔️  | ✔️ |
| [Orx](https://orx-project.org/)                 | C++                  | win, linux, mac, ios, android      | ✔️  | ❌ |
| [Oxygine](https://oxygine.org/)                 | C++                  | win, linux, mac, ios, android, web | ✔️  | ✔️ |
| [Phaser](https://phaser.io/)                    | JS/TS                | web                                | ✔️  | ❌ |
| [PyGame](https://www.pygame.org/)               | Python               | win, linux, mac, web               | ✔️  | ❌ |
| [Raylib](https://www.raylib.com/)               | C                    | win, linux, mac, ios, android, web | ✔️  | ❌ |
| [SDL2](https://www.libsdl.org/)                 | C/C++                | win, linux, mac, ios, android, web | ✔️  | ❌ |
| [SFML](https://www.sfml-dev.org/)               | C++                  | win, linux, mac, ios, android      | ✔️  | ❌ |
| [Stride](https://www.stride3d.net/)             | C#                   | win, linux, ios, android           | ✔️  | ✔️ |
| [libGDX](https://libgdx.com/)                   | Java                 | win, linux, mac, ios, android, web | ✔️  | ❌ |
| ~~[Amethyst](https://amethyst.rs/)~~            | ~~Rust~~             | ~~win, linux, mac~~                | ~~✔️~~  | ~~❌~~|
{{</table>}}

**Defold is actually [shared source](https://defold.com/license/)*

# Mainstream engines

Widely used and well-known engines. 

{{<table "table table-dark table-bordered">}}
| Name | Language | Target platforms | Open source | Editor |
| :---------------------------------------------: | :------------------: | :--------------------------------: |:--: |:--:|
| [Cryengine](https://www.cryengine.com/)         | C++/Lua/C#      | win, linux, mac                    | ❌  | ✔️ |
| [GameMaker](https://www.yoyogames.com/gamemaker)| GML             | win, linux, mac, ios, android, web | ❌  | ✔️ |
| [Godot](https://godotengine.org/)               | GodotScript/C#  | win, linux, mac, ios, android, web | ✔️  | ✔️ |
| [Unity](https://unity.com/)                     | C#              | win, linux, mac, ios, android, web | ❌  | ✔️ |
| [Unreal](https://www.unrealengine.com/en-US/)   | C++             | win, linux, mac, ios, android, web | ✔️  | ✔️ |
{{</table>}}

# Visual programming

{{<table "table table-dark table-bordered">}}
| Name |
| :----------------------------------------: | 
| [RPG Maker](http://www.rpgmakerweb.com/)   |
| [Construct](https://www.construct.net/en)  |
| [Buildbox](https://www.buildbox.com/)      |
| [GameSalad](https://gamesalad.com/)        |
| [GDevelop](https://gdevelop.io/)        |

{{</table>}}

# Fantasy consoles

{{<table "table table-dark table-bordered">}}
| Name |
| :----------------------------------------: | 
| [TIC-80](https://tic80.com/)   |
| [PICO-8](https://www.lexaloffle.com/pico-8.php)  |
| [Liko-12](https://liko-12.github.io/)      |
| [Voxatron](https://www.lexaloffle.com/voxatron.php)      |
| [Pixel Vision 8](https://pixelvision8.github.io/Website/)      |
| [Pyxel](https://github.com/kitao/pyxel)      |
{{</table>}}

*last update: 09.06.2023*