---
date:
  created: 2022-09-05
title: "Episode 17 - Radomir Dopieralski"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep017.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Radomir Dopieralski. Radomir is a Python programmer by day, a walking robot builder, game developer, and wiki enthusiasts by night. Radomir, welcome to the show.

Radomir Dopieralski

Thank you for having me.

Paul

Glad you're here. How did you first get into computing and electronics?

Radomir Dopieralski

Well, I was raised behind the iron curtain, so we didn't really have home electronics much. in the space there were other priorities but what we had was arcade games they came pretty quickly of course smuggled so the first computer I actually saw was an arcade cabinet on some shady you know shady wagon somewhere next to a train station at that moment I was hooked I never actually played those games but I could spend like hours standing there watching other people play as soon as I got access to a computer I tried to write those games were not those games that somehow were similar to what I saw at the arcade. Fortunately, when my parents bought a computer, because they both a very old one, and most of the games you could buy at the time didn't work on it anymore. So I had to spend a lot of time getting them to work. I didn't have a hard disk drive, so I had to pack them all their files on as many discets as were. necessary and you know there was a lot of try and error in there i learned much more than if i spent that time just playing games and one thing came to another i went to IT at the university and so on so i'm a programmer now

Paul

H did you discover MicroPython and CircuitPython well i discovered

Radomir Dopieralski

MicroPython from the MicroPython kickstarter back when it just started i thought it was a great idea At the time I was mostly using Python, both for work and for my hobbies. So it was a great idea to have it on a device like that. And of course, the most immediate idea what you could use it for was to have a handheld gaming device with it.

Problem was that it was a bit expensive at the time. You couldn't, you know, design a handheld device. That would cost so much that nobody would build it except for you.

So that didn't work for me. What really got me started into MicroPython and got me contributing to it was the second Kickstarter with the ESPA-266 version, because a $3 board that was still relatively powerful 80-Mahhertz CPU, so you could do a lot with that. That got me on my way to making a handheld device that you could program with MicroPython.

Paul

So you've been working with a number of handhelds over the years that you call the Pew-Pew family. Tell me about that.

Radomir Dopieralski

Right. So apart from my quest to actually recreate the arcade games or like the handheld games from Game Boy or from Switch. I also got involved in the Python community into doing workshops. I was very annoyed that the first half, an hour, an hour often at the workshop you spent helping people to install everything, helping people to install Python, helping people, people to install Pi game if you are doing a game making workshop.

So I wanted a solution that would let me just tell people, okay, take this device, connect it to your computer, and we are starting with the game making. So I needed the minimal viable gaming console I could use to teach programming. And that's why I came with PiuPu.

And since it's for workshops, so you are likely to have to buy like 20 of the people. I had to make it as cheap as possible, as affordable as possible. It's just an 8x8 LED matrix and the smallest chip that can run CircuitPython possible.

But since it's a CircuitPython, you really, it's super simple to style, you just connect it. It comes as a USB drive and you just write your code. So that's it.

Well, if you want to see the error message, that's a bit more advanced, but most of the time people manage time.

Paul

So they get a Pew-Pew device in a workshop. What do you teach them? What do they learn?

Radomir Dopieralski

So the library I use for displaying things on this display, and for handling buttons, it's very minimal. Because I really wanted to get down to the main game loop. People have suggested to me, okay, make those callback functions, update on button press, like in the microbeet, right?

Where you can, it's much easier for kids to then write code like that because they just have to fill the gaps and everything else is there already for them. I really didn't want that. I wanted to let people own the device and really struggle with every single problem, like starting off, of rating an interactive application.

So I don't even do the bouncing on the bottom. You have to do the balancing yourself if you want to have like a turn-based game where one key press is really one key press, not multiple key presses. You have to do the bouncing yourself.

You basically only have simple functions for writing a pixel to the display and some functions for copying images in the memory. And that's it. Since the games are very simple, I get away with that.

But I think that you can really teach things that are very much transferable into other, like. programming problems. Suddenly you have to program a robot. And that's also an interactive program.

You have to react to sensors, you have to move the robot in real time. So you get the same kind of problems as you learned by writing games. So it's not just about the games. Actually, it's really not. If you learn to write a game for a PiuPiu, you won't be able to next day to write Quake. At least you get this idea about how interactive applications work inside.

Paul

How does CircuitPython make it easy to program games?

Radomir Dopieralski

Well, as I said, you're connected to the computer. It comes up as a disk drive, and every time you save, it restarts and runs your game from the scratch, so you can see what's changed. That's basically it.

Otherwise, well, I tried to write the library in a way that makes it easy. the reason to really match you can do it's code, it's code. With the more complicated game consoles where you have actual graphics, it's also super easy with the disk because you can then copy the files onto the console or the assets or the sounds.

You already have the audio audio module so you don't have to figure out how to make sound. You just make wave files and copy them. A lot of ready modules, there is a key pad module.

that does the bouncing for you and handling of the buttons. There is the whole display I.O. that lets you do more advanced graphics than you can do with my libraries.

So there is a lot of stuff already done for you. But of course, if you want to do something really strange or new, you will have to do it yourself.

Paul

What are some of the challenges programming games in CircuitPython?

Radomir Dopieralski

Those are microcontrollers, so they have very little memory, it's like programming on those 8-bit micropo computers at home. If you have like 240 pixels by 240 on your display, and that's 16-bit color because the display only super 16-bit colors, that's 2 bytes per pixel. That's really a lot, that's like kilobytes of memory suddenly.

So you can't even store all of that in microcontroller's memory. You have to do tricks. So you have sprites and ties by repeating the same image multiple times that you cheat them.

You only store this one small image. It gets repeated, so it uses much less memory. With sprites, you can move things around your screen without having to, you know, yourself clean the previous position and redraw the whole thing in a new position.

So you don't have to keep the background in your frame buffer. There are also things like on-disc bitmap in CircuitPython that let you draw bitmaps directly from the flash, from the USB drive, without having to load it into the memory. So that helps as well.

But generally, depending on the device, of course, if you have an ESP 32 S2 or S3 with 4 megabytes of PS RAM, then you can do a lot more than you can do on a SAMD 21 with 16 kilobytes of

Paul

if I code a game using a certain display, are all users going to be locked into using that specific display?

Radomir Dopieralski

Well, it depends how you do it. The display A.O. lets you check the size of the display, for instance, inside your game.

So you could scale your game depending on what size the display is. And if you do it in a naive way just for this one display, then probably it's going to be difficult to scale. Since there is no game framework right now for CircuitPython, I think there should be at some point.

Right now you are left to figure out those things yourself. So you have to think ahead and write your code in an elastic way to be able to target multiple devices. Yeah, it's something that you learn after your second or third game, that you have to think a bit about how the elements of the interface are going to move if the display changes.

Paul

One of your many projects is building out robots. Can you tell me about the fluff bug?

Radomir Dopieralski

Actually that's what got me into electronics initially. I decided, oh, one day, I, you know, I looked at all those Arduino projects and I said, okay, I want to make a walking robot, a four-legged spider-legged walking robot. How hard can it be?

I got like a servo controller, not even one that you could program, but one where you could record server positions. A battery and a bunch of servos and I connected it all together and turns out that Walking is a little bit more complicated than just recorded positions. Then I switched to a Raspberry Pi on it and a bigger battery.

Then I switched to stronger servers. Then I switched once MicroPython was out, I switched to... Oh, before MicroPython was out, actually I switched to ESPA-266.

That was communicating with a computer where normal Python was grinding, and sending the command to the robot over Wi-Fi. Then my MicroPython came out and that made things much easier for me. But still, at some point, I was...

Because I wanted it to also be super cheap so that other people can build it and use it as a starting point for their projects. Like, you know, make it look like some robot from a game or movie they like. So there is this Toad, T-O-T-E project where I'm still using Arduino because it was the cheapest board you could use where I have like step-by-step instructions for building the robot and it's controlled with a TV remote.

So super easy. And now I'm working on an even cheaper, even more versatile and even easier to program robot with CircuitPython. Since the main cost of the robots, of the mechanics are the servers themselves, the original robot had 12 of them.

That comes up to like $25, just for the servers if you want to buy them. So the current one has only eight and I have compromised a little bit on turning. I can no longer turn in place, I have to turn like a tank that because of that, because I can't move the next sideways anymore.

But you know, it shapes off like one-third of the price from the robot. so I think it's worth it. It doesn't really have a function.

It's a desktop robot for walking, for programming it yourself. You can make it dance or you can make it... No. You can put sensors on it.

It takes shields that actually are attached like face masks. Because most of the sensors you want to be facing forward, like a distance sensor or issue sensor. So it's like a face mask.

And I also made one that... display so you can show a face on it or an eye to make it look super creepy.

Paul

I'll have to get a picture of that from you and put that in the show notes.

Radomir Dopieralski

Yeah, so that's the robots. The challenge for them is the code. Like the mechanics I have pretty much figured out.

It's the same for several iterations now. The problem is with the code because, as I said, it's an interactive application. Right now I'm struggling with the async, Async I. I think in general, I want to rewrite all the content I have that currently does only one thing on the robot.

So either you have a walking robot or you have a robot with the eye or you have a robot with the sensor. I want to combine it all into one code.

Paul

So if you're using asyncio, you can asynchronously program so the eye is moving while it's walking, for example.

Radomir Dopieralski

Exactly.

Paul

That's a really neat project. I'll make sure I link to those in the show notes. We're almost out of time, but the final question I have for you is you're about to start a new project. Which microcontroller are you going to reach for?

Radomir Dopieralski

The practical answer right now is SAMD21, and that's because when the chip shortage started, I bought the last 50 ones from Mouser. So I have them in my drawer right now, and they are super easy to use because you literally only need two capacitors for them. And not even like, if you are running from a battery, you don't even need voltage regulator.

You can connect the battery directly to them to capacitors that that's it. So I have a lot of simple products that use that chip just because I already have it and I know it and it's convenient. What I should be doing is using the RP 2040 because that's the only chip you can buy right now.

basically, or the expressive ones. I'm still a bit intimidated by the fact that you need the crystal, you need the external flash memory trip. You need all those stuff around the chip.

You have to design the PCB for it properly. So I hope to get over that hump and start using it.

Paul

But those are great choices. Radomir, thanks so much for being on the show.

Radomir Dopieralski

Thank you.

Paul

Thank you to Radomir for being on the show. and I apologize for any mispronunciation. For show notes, transcripts, and to support the show, visit CircuitPythonshow.com. Until next episode, stay positive.
