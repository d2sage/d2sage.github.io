---
layout:    post
title:     "Running Steam games from the command line under Linux"
tags:      ["steam", "linux"]
category:  "dota 2"
---

## Passing launch options to Steam games run through flatpak

When you run Steam through flatpak, you normally use something like the following:

	flatpak run com.valvesoftware.Steam

What if you want to run a Steam game directly from the command line? You can specify the
`-applaunch` option to steam. The option must be set to the game's ID; for example, Dota 2
has ID 570. We then get the line:

	flatpak run com.valvesoftware.Steam -applaunch 570

When run this way, Steam lets us set launch options. You can add them directly after the
command:

	flatpak run com.valvesoftware.Steam -applaunch 570 +fps_max 138 -console 

Or even put your options in a file:

	flatpak run com.valvesoftware.Steam -applaunch 570 $(cat /home/user/dota2_launch_options.txt) $@

This is useful because Steam otherwise limits the length of your launch options.

