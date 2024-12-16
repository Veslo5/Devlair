---
title: "Viewport letterboxing in Raylib"
date: 2023-09-03T12:02:00Z
description: "How to create viewport letterboxing in Raylib"
tags: ["post", "gamedev"]
draft: false
type: "posts"
layout: "simple-comment"
---
About week ago I started little 2D old school like project in latest .NET 7 just to test some new things I allways wanted to try. For graphic representation I've used small library called [Raylib](https://www.raylib.com/). For those who don't know Raylib is high level OpenGL "wrapper" written in pure C and inspired by XNA - so it works more or less like Monogame or Love2D.

I wanted to develop whole project in one native resolution which is small (in my case 480x320) for that desired old school look and feel. Technically it's pretty simple, we just create render texture (aka offscreen target, render target or canvas) and basically draw everything into it instead of default framework canvas. Then we take our render texture and draw it how we want. That means we can use some trivial math to calculate positon and size when user resize window.

*[Godot](https://docs.godotengine.org/en/stable/tutorials/rendering/multiple_resolutions.html) community described viewport resolution handling very well with some awesome examples.*

First step is load our render target, that's pretty easy in Raylib
```
_renderTexture = Raylib.LoadRenderTexture(width, height);
```

Then we calculate ScreenPosition of our renderTexture. This is part of my code which is called everytime when window is resized
```csharp
	public void WindowResized()
	{
		var windowWidth = Game.WindowWidth;
		var windowHeight = Game.WindowHeight;

		// ViewPortType.Expand just stretch render texture to window
		// ViewPortType.Aspect stretch texture to window in way to retain aspect ratio
		if (_viewPortType == ViewPortType.Expand)
		{
			ScreenPosition = new Rectangle(0, 0, windowWidth, windowHeight);
			LetterBoxSpacing = Vector2.Zero;
		}
		else if (_viewPortType == ViewPortType.Aspect)
		{
			// NativeSize is Vector2 with original render texture size
			// Due to how OpenGL coordinates internally works on render textures, we must negate NativeSize.height
			float ratio = Math.Min(windowWidth / NativeSize.width, windowHeight / -NativeSize.height);

			int width = (int)(480 * ratio);
			int height = (int)(320 * ratio);

			var centerX = windowWidth / 2 - width / 2;
			var centerY = windowHeight / 2 - height / 2;

			// Calculation of letter box spacing
			LetterBoxSpacing = new Vector2((windowWidth - width) / 2, (windowHeight - height) / 2);

			//final position and size
			ScreenPosition = new Rectangle(centerX, centerY, width, height);

		}
		
		ScreenCenter = new Vector2(ScreenPosition.x + ScreenPosition.width / 2, ScreenPosition.y + ScreenPosition.height / 2);
	}
```

So we can now begin drawing into render texture

```csharp
		Raylib.BeginTextureMode(_renderTexture);
		Raylib.ClearBackground(ClearColor);
		//Draw something here...
		Raylib.EndTextureMode();
```

Then we draw render texture
```csharp
		Raylib.DrawTexturePro(Viewport.GetRenderTexture(), Viewport.NativeSize, Viewport.ScreenPosition, Vector2.Zero, 0, Color.WHITE);
```

And... that's all! Seems pretty simple doesn't it? 
