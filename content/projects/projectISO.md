---
title: "Project ISO"
date: 2023-06-11T16:03:00Z
tags: ["project", "gamedev"]
draft: false
type: "projects"
layout: "simple-comment"
---
Isometric projection is one of my favorite game stylization, and Project ISO was my first attempt to challenge myself and create a custom isometeric "engine". At the time I only worked with C#, so the obvious choice was to build the whole concept on top of the [Monogame](https://www.monogame.net/) framework and it served me well.

{{< rawhtml >}}
<div class="text-center">
    <img src="/projects/projectiso2.jpg" class="rounded mx-auto d-block img-fluid" alt="projectiso2"></img>
    <i>First project ISO prototype</i>
</div>
<br/>
{{< /rawhtml >}}

I didn't really know what challenges awaited me, so I set up the project and started to build the structure. After I created the basic structure of the project, my next task was to write my own system that parses the map metadata from [Tiled](https://www.mapeditor.org/) editor and then render it.
Then I figured out how to write a custom abstraction of the map view (camera), how to create an asynchronous resource loading system and how to handle scenes. I spent most of my time testing the rendering itself. In the beginning I was rendering 1000x1000 tiles at 30fps max. Then I ended up using canvas to render the map only if there was a change. This method itself brings many fps, but unfortunately also many limitations. In the end I chose a system where I only render tiles that are seen in the FOV of the camera. Kind of like "occlusion culling" only much simplified.

{{< rawhtml >}}
<div class="text-center">
    <img src="/projects/projectiso1.jpg" class="rounded mx-auto d-block img-fluid" alt="projectiso1"></img>
    <i>Final version with <a href="https://opengameart.org/content/isometric-walls">Ocylixs</a> isometric tileset</i>
</div>
<br/>
{{< /rawhtml >}}

 When I was happy with the result, I started to figure out how to further improve the project. I implemented an interesting [Moonsharp](https://www.moonsharp.org/) library to integrate the Lua interpreted language and I planned to implement all the game entity logic in it. I also implemented an open source [library](https://github.com/playerthree-ltd/MonoGame-Pixi-Particles) for fx particles, which I had to modify slightly. Finally, I invited a friend to start working on the GUI.

{{< rawhtml >}}
<a href="https://github.com/Veslo5/ProjectISO"><i data-feather="github"></i> Project ISO</a> was also my first game project which I tested on Linux :) 
<br/>
<br/>
{{< /rawhtml >}}