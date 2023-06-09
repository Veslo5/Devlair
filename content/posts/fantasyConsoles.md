---
title: "Why I love fantasy game consoles (and you should too)"
date: 2023-06-08T17:53:00Z
tags: [post]
draft: false
type: "posts"
layout: "simple-comment"
---
Fantasy game consoles are "virtual computers" that lets you create and play retro-style software on your PC. But how does it work? Well, it is very simple, users have to download binaries (or use a web version) of the desired console and launch them. The console then welcomes the users with a booting screen and with old school console-like interface which the user uses for "navigating" through all the tools.

But why should one love them? Here are some reasons:

- They are nostalgic. Ever wanted to create a retro game that your dad played when he was young?

- Limitations = fun. You have to work with limited memory, limited resolution, and the size of your code is limited too. Sounds scary, but actually it is not. Just use your creativity and plan your project with mentioned limits in mind.

- They are tiny and portable. You can take them almost everywhere with you. Use your phone, laptop or handheld console and enjoy developing or playing on vacation.

- Fully integrated tools for sprite editing, music/sfx editing, code writing and game browsing.

- Simple programming languages. Most used scripting language for fantasy consoles is Lua, which is perfect for both beginners and experts.

- No resolution handling.

We have many interesting [consoles](https://github.com/paladin-t/fantasy) to choose from and while many of them are very promising and interesting, I would recommend using the most used ones, which are PICO-8 and TIC-80.

## PICO-8

{{< rawhtml >}}
    <img src="/logos/pico8_logo.png" class="rounded mx-auto d-block"></img>
    <br/>
{{< /rawhtml >}}

Created by [Lexaloffle Games](https://www.lexaloffle.com/), PICO-8 is easily recognizable and there is a big chance that you have already seen a game created in it. Games are limited to 128x128 pixels and can use a maximum of 16 colors. Audio output has 4 channels and 8 wave-forms. There is also the controversial 8192 tokens limitation which enforces smaller game complexity and size. 

For example, this tiny lua code uses 5 tokens:

```lua
fooX =  5 - 5 -- this line is gonna cost us 5 tokens
```

### Distribution

 Projects are distributed via cartriges which are literally .png images.

{{< rawhtml >}}
<div class="text-center">
    <img src="/fantasyConsoles/xenith.png" class="rounded mx-auto d-block" ></img>
    <a href="https://www.lexaloffle.com/bbs/?pid=130692#p">PICO-8 game "Xenith" by Godmil</a>
</div>
<br/>
{{< /rawhtml >}}

You can browse PICO-8 projects [here](https://www.lexaloffle.com/bbs/?cat=7).

### Price

PICO-8 costs 14.99$ and runs on Windows, Mac, Linux and Raspberry Pi. [Version](https://www.lexaloffle.com/pico-8.php?page=schools) for educators and school also exists.


## TIC-80
{{< rawhtml >}}
    <img src="/logos/tic80_logo.png" class="rounded mx-auto d-block"></img>
    <br/>
{{< /rawhtml >}}

TIC-80 is open source fantasy console created by [Vadim Grigoruk](https://github.com/nesbox) also known as nesbox. Users have 240x136 display resolution, 16 color palette which colors are customizable. Sound has 4 channels and also customizable wave-forms. TIC-80 does not enforce any token limits, but the cartrige needs to fit 64Kb. Users can develop in Lua, MoonScript, JavaScript, Ruby, Wren, Fennel, Squirrel and Janet.

### Distribution

Games are distributed in .tic format, or similar to PICO-8, in the .png format.

{{< rawhtml >}}
<div class="text-center">
    <img src="/fantasyConsoles/balmung.png" class="rounded mx-auto d-block" ></img>
    <a href="https://tic80.com/play?cart=636">TIC-80 game "Balmung" by petet</a>
</div>
    <br/>
{{< /rawhtml >}}

You can browse TIC-80 projects [here](https://tic80.com/play).


### Price

TIC-80 is free, but you can support the project by purchasing PRO version for $5 which includes saving/loading cartridges in the text format.

