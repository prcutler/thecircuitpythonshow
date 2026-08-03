---
date:
  created: 2022-07-25
title: "Episode 14 - Kevin Matocha"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep014.md)

## Transcript

Paul

Welcome to The CircuitPython show. I'm your host, Paul Cutler. This episode, I'm joined by Kevin Matocha. Kevin is a longtime CircuitPython community member and currently works as a vintage stereo repair technician in Austin, Texas. Kevin, welcome to the show.

Kevin Matocha

Hey, thanks for having me. Thanks for an invitation. I hope I've got something useful I can share.

Paul

How did you first get into computers and electronics?

Kevin Matocha

Probably like me and 12 million other families. I had a Commodore 64 as a kid. And my brother was actually the better programmer and, you know, studying how to do the programming, but a little bit rubbed off on me as a kid playing games and typing in code from magazines with the family as we traded off typing.

And eventually did some, you know, courses in high school learning Pascal, which was kind of the educational language of choice then, and thought I wanted to go into computers. I started in a double E program, electrical engineering program, with computer emphasis, thinking I want to do computer stuff, but then got distracted with more of the semiconductor design processing aspects of things. So kind of, you know, took some more programming classes in college, but feared towards more of the, you know, how the chips are made and designed and fabricated in commercial environments. So, so I kind of strayed from computing, you know, pure computing, but always retained that sort of software coding capability. And, in a particular how do you analyze big groups of data, how do you visualize it? And that got me into MATLAB and eventually into Python after that. So that's how I sort of had always an interest in computing, maybe strayed from that, but I'll always use sort of coding to sort of help me in my day-to-day work.

Paul

How did you discover CircuitPython? I think I got here through Arduino. My daughter had

Kevin Matocha

Arduino Uno, I think, one of the basic boards stuck down to her bed for a long time that she got as a gift. I pulled it out and realized, wow, the tools that are available now, which was Arduino at that time, are so much more than what I had when I was in, you know, first looking at microcontrollers in undergrad. I remember starting with Motorola HC-11 programming and assembly, using Buffalo to talk to some arcane in a way of analyzing what the ship was doing. And that was actually on a project, sort of assistance technology project with a professor who was trying to make it where you could push a button and it, you know, say something or highlight a picture or something like that.

But it was near impossible to get anywhere with so low-level coding. So fast forward 20 years later and see Arduino and all these libraries and, you know, the support for things that basically any ship you wanted to talk to or use, you could find somebody who had done that to help you along. So that was eye-opening.

And after that, doing some basic projects, you know, even some graphics projects with Arduino, then heard about Circa Python. I thought, wow, this is even, you know, the next level. If I thought Arduino was a, you know, a huge leap forward, then the CircuitPython thing is even further.

So just got involved with that. First, a user and then then help them contribute on especially some graphics things. And I've just been enjoying it.

With CircuitPython, I guess there's awareness that basically the chips are getting so powerful that there's basically an oversupply of capability, right? Like how fast the processes do you need to flash LEDs, right? It's probably not that much.

But you can use that processing power to make it so you can flash LEDs in two minutes instead of taking 20 minutes to figure out how to do that. So I think that's what I like about it, that you get something working in a few minutes rather than maybe an hour or something like that with other things. So that's why I was just kind of stuck with it and trying to move things along in little ways that I can.

Paul

Well, that's a great segue to one of your next projects that does involve graphics that probably takes a little more than a couple of minutes. But you've been working on something you call the hackpad. Tell me about that.

Kevin Matocha

I've always been interested in displays, and sort of a big jump for me was when the Adafruit PyPortal came out. You know, it was a chip and the display all connected.

So basically it's easy to prototype. You don't have to have a bunch of wires, you know, hanging out there to connect the display, which always seems to be as the wires are always a stumbling block or a place to break. So with that, it made it clear, hey, you know, you have a ship and CircuitPython and display capability, but it's pretty small.

So having any kind of user interface is pretty limited just based on how big fingers are. So I've been looking for how to get a big display working in CircuitPython. And in particular, the problem with big displays is they're more expensive.

Process there is a small cost, but now the display is sort of overwhelming costs. So from just a prototyping standpoint, I was able to find some displays that were basically these conference room scheduling units that I guess they're supposed to be mounted on the wall in a conference room. And so you can see, oh, is this room available or how much time?

I've actually never used them, but I think that's the purpose. So they're fairly big, and they have a capacitive touchscreen on them. So that's really what I was looking for.

And even better, I could find them on eBay for 20 bucks apiece. So probably even cheaper than I could buy a raw display from overseas to get it. So, you know, sort of hit all the right targets or, you know, criteria for what I was looking for.

cheap and big display and capacitive touch. And as I said, one of the challenges with making a, I guess, a product with a display is the display cost. Part of that display cost is usually the processor that goes between your microcontroller and the display itself.

And actually this display that I found is actually one of the simplest displays, so-called like an RGB display or sometimes called dot clock display, where you've got to give it a lot of signals, basically for, you've got to send it signals to redraw every time. you want to draw frame, as opposed to other displays have some controller in between that has memory, and you just send it like maybe what parts you want to update. So it has some displays have some intelligence built in. These so-called RGB displays are cheaper because they don't have that controller in it. But it takes more work to be able to run them. And at the same time, that was fortuitous, a new chip came out from expressive called the ESP 32S3, which actually inside the main processor has the capability to drive this kind of simple RGB display.

So in essence, for one price in the microprocessor, you don't need another chip in between to actually run the display. So in essence, it's kind of a combination of realizing this S3 chip now has the capability of driving these simple displays and finding a suitable display to hack around on. So that's how the hack tab that came about.

So most of the work of getting to work in CircuitPython has been how to to understand this new LCD driver built into this S3 chip. And it's still new things coming every day from the expressive team to try and how to better use that. So my final goal is to make something that you can, you know, kind of make iPad-like demos on.

It's probably never going to be as fast as, you know, what Apple can do with its, you know, amazing ships and stuff like that. But at least you could toy around with some touch interaction and a reasonable size of a display that you can. and modify and react to.

Paul

Right. I don't think I've seen anything bigger than a PyPortal Titano that has touch on it. So that would be great to see. Are these about a 7-inch tablet, like the old Google Nexus-sized?

Kevin Matocha

Yeah, it's 7-inch. So the one I've got. Of course, if you have that capability for the running an RGB display, then you can pick whatever size you want.

So another benefit of this new chip is that it's got, or at least the demo boards that I've been able to get is they've got quite a bit RAM and also storage space on them. So you can have plenty of space for large memory space for frame buffers for these displays too. So sort of combination of all the features of these new chips are making it easier to drive these big displays.

Paul

How hard was it to connect the SB 32 S3 chip to it? Was it just a matter of simple soldering or was it a lot of reverse engineering involved?

Kevin Matocha

Well, as you could hear from my previous comment about wiring beyond sometimes the difficult a most difficult problem. My first attempt used a bunch of adapters. You know, you've got, first you've got the chip or the demo board with headers, and you've got to convert that to some maybe 40-pin cable connector. So the, you know, connecting 40, or I don't know, maybe it's not quite 40, but, you know, 30 pins between a demo board and a cable adapter. That's usually where the problem is.

Plus, you've got to drive the backlight. And so there's just a bunch of wires. So, it's a real pain. Eventually, it's my first demo of a circuit board. So I made a circuit board adapter, which made my life a heck of a lot easier where I could solder it and it's just wires. It's nothing more complicated than that. So if you think about that, it just saves you from having to pull wires out of your breadboard on a daily basis. So the circuit board, even though it's a, you know, kind of takes a while to get it made and delivered, it's made my life so much easier to make some progress on the project.

Paul

Did you submit the hackpad to the latest, Hackaday contest that they're running?

Kevin Matocha

Yep, sure did on the one that just finished up. Basically, how do you reuse or recycle? I can't remember the name of it.

But yeah, submitted to that. And I noticed that a similar project got selected for the next one, Deshipu's PewPew, which is kind of a game pad, but also reusing displays. So I've been watching his project for a while and actually learned a lot from what he's done.

So it's good to see what he's going to come up with next.

Paul

I've been watching his projects as well, he'll be a guest on an upcoming episode. I'm looking forward to having him on.

Kevin Matocha

Oh, cool.

Paul

One of your other projects is Tiny Logic Friend. What is that project?

Kevin Matocha

This was a project that was posed by, and it's actually started by Scott Shawcroft, tannewt, that works on the CircuitPython project. He had this concept of how to use low-cost microcontroller boards like Adafruit and many other cell, but to use the capability to do logic analysis a form of logic analyzer. And what that is is basically when you have two chips talking to each other, they have a certain language of ones and zeros and timing so that they can communicate.

But if something goes wrong, you can't see what's going wrong with a communication, right? You may just get nothing back or garbage or what when you're just talking with from your processor to how, say, a sensor is talking back. Often you'll need some way to debug, you know, what is it actually talking?

what is the microprocessor sending to the sensor, and what is the sensor sending back? First, you might think you need a psiloscope, which basically is a time measurement of signals, which that might work, but a psiloscope basically measures, like I said, a voltage level over time, but it's usually used for repeating signals, so that it's the same waveform, usually analog signals, not necessarily, but usually some kind of repeating measurements that are the same thing over and over. But in contrast, the chips talking back and forth, you know, it's a one and zero of, you know, different timing between each one. And so usually you'll need to string like a long amount of ones and zeros to see, you know, one transaction, you know, with the chip sending one request for data and then a long thing of all the data back from the sensors say.

So in essence, what you really just need is, okay, how long was the zero for? How long was the next one for? You know, so in essence, you just want to know the ones and zeros and the duration of them.

So that's what a logic analyzer does. It basically tells you, okay, you know, how long that those ones and zeros are for. So you can then decode that into something that makes sense to you.

So this project was actually conceived as an add-on to an existing piece of software called Sigrock. So signal meaning, you know, Sigrach is a combination of signal analysis, which the logic analyzer is. And Groch, which is a word, I think, developed in the 50s or 60s that was used to to say like, hey, understanding something.

And I think coders use that a lot. So anyway, a combination of signal understanding is this software. And in essence, what that does is takes, you know, even just a raw file, basically has to take that data of ones and zeros over time.

But then convert that into something you can understand, like whether it be visually of seeing the timing, which there's a tool inside of that tool suite to do that called PulseView. Or build on top of that, like knowing that when the chip sends a hexade, code 32, that means I'm asking for data or, you know, or converting even 8-bit to numbers or, you know, or letters, you know, hex codes or something else. So it has capability to build on top of that, not just what ones and zeros and how long, but what does that mean in multiple different levels?

So, so basically it helps you even further analyze how these two chips are talking back and forth. So long story, but in essence, it's how do, how to, instead of buying a, you know, several hundred dollar, you know, logic analyzer that's, you know, custom made for that. Can we take these $15 boards and also use them? Because they can measure fast. You know, they're spitting out signals at the same rates. Why can't they read them and report them back? So in essence, it's how to connect, you know, simple microcontrollers to Sigrock. So you can use the existing tool set, but these fairly low-cost boards. And this tiny logic front is one of the several others that are trying to do the same kind of thing.

Paul

So was there a way to contribute that back into upstream into the Sigrok project?

Kevin Matocha

Yeah, there is a way. But since we're talking at CircuitPython, you know, one thing that's, you know, promoted about CircuitPython is that there's a big community wrapped around it, right? There's forums where there's people crawling around there that are willing to, you know, contribute their time to do that. When I worked on this tiny logic friend, it felt a little more like a little more lonely of a project, I would say, that basically I'm contributing. It's not a huge community. And the best way to communicate us through an email server to get some help. But it's kind of hard, difficult to elicit feedback from that, I guess, because people are doing their own things. And most of that, the project actually, the Sigrock is focused on commercial or, you know, analyzers that people are using that. So, so, but I have seen as sort of a group of different projects that are kind of heading in the same direction. So I'm hopeful that maybe those can converge around, maybe make it easier that the, the concept is the Sigrock software can have a generic capability to be able to accept data from a lot of different microcontroller boards, maybe a standard way of talking to it. So you don't really need to be changing Sigrock a lot. You just need to, you can take any kind of board as long as you fit or you behave a certain way. Can you get the Sigrock to understand that? So I see a few projects, you know, kind of heading in that direction. So question is can we all sort of come together and figure out how to make that work. So basically can anybody take any kind of small board that they want and still have hooked that into the Sigrog project, which has a great capability to be able to analyze and understand these signals. So that's the ultimate goal. I can't say have achieved that yet, but I think that's what the concept of this is.

Paul

Last question for you. You're about to start a new project or prototype. Which microcontroller are you reaching for?

Kevin Matocha

Yeah, for me, it's no question. I mean, that PyPortal, it's got a special place on my desk. I even made a bracket, so it sits right on top of my monitor, and it just stays there staring at me with a blinka right there and a Ripple. So, yeah, no question, that's my first one to go to.

You know, it's good to have a display connected, so, you know, you can get different outputs if you want to debug what's going on. So, yeah, that cortex import chip, and it's got a fair amount of RAM, It's got touch response on the display. So that's definitely got to be my go-toe.

Paul

I'm right there with you. I've talked about on the show before, how I have a PyPortal Titano on my desk, and it's one of my favorite CircuitPython devices.

Kevin Matocha

Yeah, exactly. Yep.

Paul

Kevin, thanks so much for being on the show.

Kevin Matocha

Yeah, thanks a lot. Thanks for having me.

Paul

Thank you for listening to The CircuitPython Show. For show notes, transcripts, and to support the show, visit CircuitPythonShow.com. Until next episode, stay positive.
