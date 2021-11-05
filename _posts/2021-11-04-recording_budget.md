---
title: "Recording on a Budget"
tags: ["music"]
---
This guide will serve to break down various considerations on audio recording for those that
lack the resources, space, or time to create a proper audio recording setting. As the topic
of recording as a whole is very large, the aim of this guide will be to set up an isolation
booth for single-person recording. This will be good for most applications, such as vocals,
simple instruments, and foley (SFX recordings).

## TABLE OF CONTENTS
1. [BUDGET](#budget)
2. [HARDWARE](#hardware)
3. [ACOUSTICS](#acoustics)
4. [INTERFERENCE](#interference)
5. [EXAMPLE](#example)
6. [CONCLUSION](#conclusion)

## BUDGET
One of the most important things to consider when designing anything is the budget you are willing to spend on it. 
This does not just mean how much money you are willing to spend on this project, 
but also _how much you want to spend on each aspect of it_. 
A good breakdown of a budget is as follows:

- Actual recording hardware (Interface, Mic)
- Acoustic material (acoustic foam pads, reflectors, etc.)
- DIY materials (hardware + tools you would use for mounting or building DIY acoustic solutions)

Depending on what you already have on you, what your space is like, among many other things, will change how you break 
down your budget between these three aspects. For this budget, a good start is 75-20-5. 
The following sections will provide more explanation on how this breakdown was derived.

# HARDWARE
You can’t polish a turd. As such, your audio recordings will only be as clear and high-resolution as the hardware you use to record that stuff. 
However, that doesn’t necessarily mean that you need to spend millions of dollars to get decent sounding audio. 
Many times it just requires doing good research on the hardware that you need to get so you get the best bang-for-buck. 

{% include md/figure.html src="https://yourfreesounds.com/wp-content/uploads/2020/08/cardioid_pattern_graphics_wMic.png" figcaption="Cardiod Pickup Pattern <br><i>source: yourfreesounds.com</i>" width="20%" height="20%" mods="left" %}

For this project, we only need an audio interface and a microphone. Most understand that a good microphone will pick up sound better, 
but there are so many other considerations such as pickup patterns, diaphragm types, etc. For an iso booth, we will get a good XLR cardioid microphone. 
XLR is just a 3-prong connector that most interfaces use, and cardioid describes the pickup pattern, 
i.e.: where around the microphone will it pick up sound. A cardioid pattern picks up only around the front, and somewhat around the sides. This will be good to eliminate the cost for acoustic padding.

<br>
<br>
<br>
<br>
<br>
<br>
<br>

{% include md/figure.html src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fmedia.sweetwater.com%2Fimages%2Fitems%2F750%2FUM2usb-large.jpg" figcaption="Behringer UM2 Audio Interface <br><i>source: Sweetwater</i>" width="20%" height="50%" mods="right" %}

Audio interfaces connect your audio devices to your computer. They also provide an audio-digital converter that is separate from your computer, which eliminates alot of electrical noise.
Audio interfaces at a low price point are all about the same, so just aim for a reputable company that makes good audio equipment. 
For instance, a Behringer UM2 is a good interface at just $30. 

<br>
<br>
<br>
<br>
<br>
<br>

Gear is far and plenty to come by, but consider these things when buying your recording hardware:
- Buy used; there are many people out there reselling the gear you may be looking for for well under its original price.
- Look at reviews; look more at the negative reviews and see if you see any common reviews about the hardware or the (re)seller. 
  Does it fail after a couple of months? Is the seller unreliable? Repeating reviews will tend to hold true.
- Weigh your options; most gear will have pros and cons at any price point. It is up to you to decide what you can compromise on and what you can't sway on.

## ACOUSTICS
Listen to these two sounds and compare them.
<audio src="/assets/2021-11-04/test1.wav" controls preload></audio>
<audio src="/assets/2021-11-04/test2.wav" controls preload></audio>

<br>

If you notice, one has a noticeable "flutter" or "shimmer" in the background when I clap.
The other, less background noise in general.

This effect is known as **reverb**, and it is the main enemy of an isolation room. 
Reverb is the reflection of sound from the walls of the room. With recording, 
especially loud noises and high gain, you may pick up the reverb from your sounds.
To eliminate reverb, you effectively need to redirect reflections, diffuse them, or absorb the
sound waves altogether.

Before we look at what we need to do to fix our reverb, we need to take a couple of considerations.
First you need to consider the room you are using; any furniture that is going to be in there will help 
reduce the severity of the reverb. Even hard furniture such as dressers and shelves can redirect the 
soundwaves in a way that your microphone won't pick up. Second, you should consider the pickup pattern 
that your microphone has. Since we have gone with a cardioid pickup pattern, _we can completely ignore 
any reflections behind the microphone_, as it will not be picked up by the mic. 
Instead, we can focus on the reflections happening in front of the microphone and to the sides of the microphone.

With those considerations, we now need to think about how to rid of any relevant reflections in the room.
With enough money, space, and freedom, we could just pad the entire surface area of the room. However, you most likely do not
have that luxury. Instead, here are a couple of options that you can consider:

- Fill your room with fabrics; most soft fabrics will dampen sound, so carpets, towels, etc. will all help
  reduce sound reflections. One particular item that is super effective and very accessible is drapery, especially
  large, pleated and layered curtains. These can diffuse sound very effectively.
- Reposition your recording devices; If you can, move your recording and audio devices as far away from other sound
  sources or hard walls as you can. Positioning your audio things off-axis from walls (i.e.: not parallel) can also
  help reduce direct reflections.
- Angle your furniture; something that you may not consider is how your furniture plays into reflections. Angling your
  furniture in a way that can send reflections to the sides or to the back of the recording area can help reduce reverbs
  that are picked up.
- Build DIY acoustic panels; you can do this using leftover rockwool, sheep wool, or some other type of insulation.
  A good place to start is [this video](https://www.youtube.com/watch?v=dmHFbygUtO4) by Kobi McCoull II. You
  can modify this idea to fit your needs, but generally the DIY route will require some research to make efficient acoustic panels.

## INTERFERENCE
Any active sound source can act as interference: People, other speakers, etc. can all act as interference to the sound
that is picked up. However, did you know that even electrical devices can act as interference? Microphones can actually
pick up certain frequencies as low hum, depending on the size and distance of the electrical device. For instance, 
most fluorescent light fixtures create a low 60hz hum that microphones will easily pick up. Similarly, even
small components in computers and other circuits can create noises that your microphone or even your audio interface
can pick up.

This is why a standalone audio interface is a good buy for this project; your computer has an onboard interface, but since
it is inside your computer, it can also take in the sounds brought by electrical interference.

There are many other things you can do to minimize interference (at least the interference _you_ can control):
- Use low-traffic areas; places such as far closets and attic spaces make great recording rooms since not many people move around
  there. If you can manage to use a similar room for recording, it may be a good idea to do so.
- Move electronic devices away from your recording equipment; this should minimize electrical interference. Even having solid walls
  between your devices and your electronic equipment can help.
- Use LED lights instead of fluorescent fixtures; if you can simply get a floor lamp and use a LED lightbulb, that will eliminate
  hum that comes from flouorescent lights.

## EXAMPLE
For a real-life example of what this information would look like applied, take my apartment room and gear for example.

{% include md/figure.html src="/assets/2021-11-04/room.jpg" figcaption="Corners of my room" width="25%" height="50%" mods="right" %}

My recording hardware is a Marantz MPM-1000 cardiod microphone, paired with a Behringer UM2 audio interface.
My apartment room is a small room, with a full-size bed and a band shirt on the wall. 
It's hardwood flooring, with some type of softwood walls, and other furniture and things that fill up the space.
Here are some examples of both vocal and instrumental recordings in this room:

<audio src="/assets/2021-11-04/voice.mp3" controls preload></audio>
<audio src="/assets/2021-11-04/inst.mp3" controls preload></audio>

<br>

Without much addition to my room, the quality of the recordings are already very nice. However, as you can tell there is still
some reverb that gets through the mic, particularly where I clap and snap. There are many ways to solve this issue. Personally,
I would consider putting some type of acoustic panel above my bed to dampen the reflections that come from there. My ceiling is hard
to pad, but a way of doing it could be to hang something on some stands above my head.

## CONCLUSION

I hope that this guide provides some information on how to go about spending your money and setting up your room
for recording audio. There are plenty of other sources online if you want more information on anything in specific
that was covered in this guide. Be sure to also visit forums if you need other opinions on choices regarding audio
considerations or recording hardware.
