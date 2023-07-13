---
title: "Defold"
date: 2023-07-12T16:02:00Z
tags: ["post", "gamedev"]
draft: false
type: "posts"
layout: "simple-comment"
---


{{< rawhtml >}}
    <img src="/logos/defold_logo.png" class="mx-auto d-block"></img>
    <br/>
    <br/>
{{< /rawhtml >}}

Defold je svým způsobem jedinečný nástroj, který je určen pro tvorbu středně velkých a menších her. Již při prvním pohledu na oficiální stránky si potenciální uživatel lehce všimne, že Defold spíše cílí na mobilní zařízení a web, ale rozhodně to není nutnost protože podporuje výstup pro veškeré mainstreamové platformy a [nedávno byla dokonce přidána podpora pro PS4](https://forum.defold.com/t/defold-adds-support-for-sony-playstation-4/73490) s potvrzením, že podpora pro PS5 bude následovat.

Jako největší výhody oproti konkurenci bych zmínil tyto body:
- malý runtime exportovaného projektu - např. cca 3.4MB pro prázdný "release" projekt exportovaný na platformu Android 32+64 bit
- stabilní API a zpětná kompatibilita
- hot reload a integrovaný emulátor včetně detailního profileru
- možnost rozšiřovat engine nativním jazykem pro určenou platformu (android - java, web - js, pc - c++ atd.)
- oficiální podpora pro SDK rozšíření typu admob, facebook SDK, Steamworks atd.
- zdarma bez poplatků

Zajímavý je i celý koncept. Nejedná se totiž uplně o high level engine a některé "fičury" které najdeme třeba v Unity si potom člověk musí napsat sám, případně využije knihovnu třetí strany. To není nutně špatná věc, ale dokážu si představit, že pro vývojáře kteří chtějí čas věnovat hlavně hratelnosti to bude spíše přítěž. To samé platí např. pro UI část. Defold poskytuje základ a počítá se s tím, že si ho každý vývojář rozšíří podle svého.

Ohledně nástrojů, Defold obsahuje kompletní balík, včetně [editoru projektů](https://defold.com/manuals/editor/), editoru kodu, našeptávače, debuggeru, editoru scény, editoru GUI atd. Editor bohužel zatím nelze tak jednoduše rozšiřovat jako jsme zvyklí třeba z Unity.

Největší výhodou je potom poměrně hladký vývoj na mobilní platformy. Vývojář má možnost používat vzdálené debugování na fyzickém zařízení, ale zároveň si aplikaci může debugnout v klasickém "okně". Musím vyzdvihnout i velice jednoduchý export finálního produktu. Každý kdo kdy řešil release svojí aplikace nebo hry ví, jak lehce se z tohoto relativně nevinného procesu může stát noční můra. V Defoldu je to otázka pár kliknutí. Suprová je i zpětná kompatibilita projektů, protože vývojáři se snaží měnit API jádra co nejméně. Ohledně rychlosti a výkonu, veškerý heavy lifting obstarává jádro Defoldu napsané v **c++** a herní logika se píše v jazyku Lua, s tím že podporované platformy běží na verzi **LuaJIT** s fallbackem na vanillu 5.1.4. Pokud by Lua vývojáři z nějakého důvodu nestačila, má možnost vytvořit vlastní rozšíření enginu tzv. "**native extension**" v nativním jazyce (c++, js, java) pro rychlé výpočty či komunikaci s nativním HW/SW platformy. Pro renderovací backend je potom využit **Vulkan** s fallbackem na **OpenGL(WebGL)** a v případě Apple zařízení, **Metal**. Integrace SDK knihoven typu **Admob** či **Google services** je také jednoduchá, jelikož vývojáři je většinou oficiálně podporují a updatují. 

Komunita včetně vývojářů je přátelská a aktivní na oficiálním [forum](https://forum.defold.com/) nebo na [discordu](https://defold.com/discord/).

Alternativou k Defoldu je [Solar2D](https://solar2d.com/) (původně Corona), který funguje na dost podobném principu. Využívá programovací jazyk Lua, nativní rozšíření a "emulátor" platforem. Z velkých hráčů potom Unity, případně Godot. Pokud by někdo hledal alternativu v podobě frameworku, tak dobrým kandidátem je [Love2D](https://love2d.org/).
