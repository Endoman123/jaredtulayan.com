---
title: "Wii Modding Escapades: Prologue"
tags: [wii, electronics]
---
Recently I got around to modding Wii's, particularly because my friend suddenly wanted his modded.

Honestly I forgot just how versatile these consoles were, and being older and more experienced had me more
confident in being able to fix my bricked Wii.

For context, about 4 years ago I modded my own Wii, but in a manner that was quite unwise. Basically,
I installed a bad system theme twice. The first time that I saw my Wii fail to boot, I used Priiloader to load
into BootMii to reset the NAND to before Priiloader and BootMii. I reinstalled the bad theme, 
and ended up with a Wii unable to boot at all, with no anti-brick measures to access. At the time, there were no methods to recover from a brick like this, at least not without a modchip. At this point, I gave up, and left my
Wii in storage for a bit of time.

For those of you interested in actually modding your wii, you can avoid what I've done with these tips:
- **INSTALL ANTI-BRICK TOOLS!!** More importantly, don't do any actions that would involve wiping your NAND to a state without said tools. Try not to panic and revert your NAND back using BootMii like I did. 
- Don't theme your system menu. If you're like me, you're probably going to use an USB loader. Just theme that.
- If you do want a themed system menu, do it on emulated NAND. It's essentially your flash NAND memory emulated on your external drive. This means that it won't affect the operability of your actual Wii.
- If you seriously want to theme your real NAND system menu, and the theme ends up stopping your Wii from booting up, just revert to the regular system menu by reinstalling the default system menu WAD for the version you were using before. You can download the WAD from the NUS Downloader, and you can load into MyThemeify Mod through Priiloader.

Fast forward to today (or more specifically, 3 weeks ago as of writing this), and I've gotten more comfortable with soldering on PCBs, and I have a disposable income to buy parts. Because of this, more techniques are on the
table to get this Wii up and running again.

On first research on this topic, Bluebomb had been what I was hoping to use. Simply put, it transmits a payload through the Wii's bluetooth module that allows it to launch homebrew. At first glance I thought it would work
for my console, but it wasn't working when I tried using it on my Wii. It would simply get stuck on `Awaiting response from stage0`.

So from there, my only option was to autoboot a game from the recovery menu and run an exploit on the autobooted game. This would require a GameCube Controller for a function called _SaveMiiFrii_, a modchip, and by extension,
a D2A/D2B disc drive for my Wii.

That's the game plan. I'll go over each stage in different posts.
