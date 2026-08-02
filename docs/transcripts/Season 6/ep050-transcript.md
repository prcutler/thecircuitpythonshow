---
date:
  created: 2025-11-10
title: "Episode 50 - John Romkey"
---

## Show Notes

[Show notes available here.](../../episodes/Season 6/ep050.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. This episode, I welcome John Romkey.

John is a computer scientist, software architect, and longtime internet engineer, who's been building and breaking network since the early days of TCPIP. John demonstrated one of the earliest Internet of Things devices, the Internet Toaster, controlled via SNMP in 1993, along with Simon Hackett. John currently works with microcontrollers, sensors, home automation, and full-stack systems, with occasional detours into PCB design and development.

John currently works with microcontrollers, sensors, home automation, and full-stack systems with occasional detours into PCB design and development. He enjoys programming in CircuitPython, Python, Ruby, C, and C++, and working with Docker and similar technologies for backend work. John, welcome to the show.

John Romkey

Hi, thank you very much. I'm very happy to be here. Thanks for inviting me.

Paul

How did you first get started with computers and electronics?

John Romkey

When I was a teenager, I got bitten by a radioactive chip. No, I was a really bored teenager in rural Maine in the late 70s, and the kind of thing that you would do at that point, some of us, the nerds, would hang out at Radio Shack. And Radio Shack in those days when it existed, that was like the golden age of Radio Shack.

And it was like electronics. It was almost like you walked into a, a 70s version of Adafruit in a store in a mall. I had a lot of exposure to electronics there in components and early personal computers. We were not a well-off family, but somehow my father managed to afford a TRSAD for me. And that pretty much changed my life. And so between that and the access to electronics at Radio Shack, that kind of got me into that.

at the time we didn't have if you wanted to program write programs on a TRSady you were programs in assembler which was or basic I'm sorry basic which was not a lot better than assembler really and it was very very low resource machine like your your baseline TRS80 would have 4K of memory so you know going from there to like decades later and writing software for Arduinos P32s, it really takes me back there, although we have such better tools for working in software these days, you know, and CircuitPython's a great example of that. You couldn't even have imagined something like CircuitPython back then. But that was how I initially started working with this stuff. I was super bored, and I hung out at Radio Shack. How did you discover CircuitPython. Through, I mean, through Adafruit, I was doing, I got involved in doing work with ESP 32s, or the ESP 8266 at first, and looking for resources and looking for more hardware to work with Adafruit was right there. And Adafruit does such an amazing job at fostering community and also doing open source hardware and software, which is very important to me. I was very wrong to Adafruit. Anyway, if you spend any time poking around Adafruit and looking at, you know, what Adafruit offers, Adafruits put so much resources into CircuitPython. And I've done a lot of work writing C software.

And I love C. C is better than programming an assembler, but it's like right next to it, really. And it's so easy to shoot yourself in the foot in C. You know, you just like misjudge the of your array and suddenly you've written over your stack and what happens when you return, who knows? And your program just explodes in new and exciting ways, which are really difficult to debug because you're not on a full-fledged computer, you're on some tiny microcontroller.

And CircuitPython just protects you from all of that and lets you write code in a civilized way. For all the power that C gives you, when you start just manipulative, strings, you're in a world of hurt. And especially on these kinds of microcontrollers.

And, you know, if you're doing anything like, say, you're doing a web server, which you can totally do in C, in Arduino, you know, on an ESB 32. Or anyway, if you're doing that, you're doing a lot of string manipulation. And this is just not something that C is very inviting to or supportive of C++ better.

but CircuitPython's just got your back. CircuitPython just makes it really easy, especially since CircuitPython started supporting F strings in Python, where you can just interpolate values in it. It's so much more relaxing to program in CircuitPython than it is in C. I know that some people get uptight about the overhead of CircuitPython.

You know, CircuitPython has less memory available. A CircuitPython is interpretive. it's much slower doing some operations than C is.

It's actually shockingly fast for some things. But I think they lose track of the fact that your average program just doesn't need that level of performance. Yeah, if you're writing something on an ESP 32, I keep coming back to that because that's the chip that I use the most.

But if you're writing something on an ESP 32 that's very graphics intensive, like maybe you're writing some game or something that really pushes what you can do on an ESP, 32, then sure, you're probably not going to write that in CircuitPython. But most people just write code that's like a simple loop and it's just reading some sensors or, you know, controlling some servos or something like that, you know, serving a web page. And it's actually not even touching the getting close to the limits of the ESP 32.

And CircuitPython is great for that. There's plenty of capacity, plenty of resources. Anyway, it's a great tool for a lot of applications.

Paul

Speaking of tools, you've written a tool for CircuitPython called CircRemote. Tell me more about it and how it works.

John Romkey

CircRemote basically will send a chunk of code to CircuitPython either over a serial port over USB, or if you have a device, which I believe only ESP 32s do this currently, a device that supports the web workflow so that you could connect to it over why. Wi-Fi or Ethernet, if you have that kind of device, then it can do it over the network. So it doesn't have to be directly connected to your computer.

So I do a lot of work with sensors, and I've been building some of my own PCBs with sensors. Ada fruits are fine, but sometimes I just want something a little different. Also, it's fun, honestly.

It's just fun, and it's a nice stretch. There's a lot of stuff that I end up running frequently, like I to C scanner, because most of the sensors that I connect are over I to C. I'm using Stemak UT for the hardware connection, which is awesome. It makes prototyping so quick and easy.

But I am so tired of finding the I to C scanner code for CircuitPython and copying and pasting it in. And so I figured I'll write a utility that will just keep track of this for me and then send it to the device, whether it's over Wi-Fi or whether it's over USB. And once I started doing that, having drivers for the different kinds of chips that I use was the next step to do.

And so I decided to, of course, make it way more complicated and add way more functionality to it and just came up with this general concept. of a command, which is the code that you send over and let it organize the commands and keep track of them, added the ability to have multiple paths to search for the commands. So it comes with, I think there's over 100 things built in currently.

And they're not all things for sensors. There are a lot of sensors that supports like temperature sensors, light sensors, things like that. But also there are some utilities like list the files that are on the flash drive.

One of the utilities that I added enables web workflow. And so it takes the credentials for your Wi-Fi and the other information that you need to set up web workflow and then just creates the Settings.comal file on the device. Another one just resets it.

You know, I got tired of typing import microcontroller, microcontroller reset. Another one puts it in UF2 bootloader mode. Another one can just display the contents of an arbitrary file on it.

Oh, this is one that I really enjoyed, and it's a little OCD. I use a Mac, and I love Apple mostly until they release major operating system updates and break everything. But one of the things they do when a Mac is writing to a flash drive with a DOS file system on it, like CircuitPython, very reasonably uses.

It's the right choice. One of the things they do is they just put all this trash on the drive, all these like random little files. And these are keeping track of Mac-specific metadata or indexing for Spotlight, which is the Max search system.

And it turns out Apple's not the only one. Windows does something similar. I use an editor that I would never recommend that anybody use called Emacs, which is ancient.

I've used it for decades. It's basically built into my fingers at this point. and it's very hard for me to switch to a different editor.

Emacs leaves trash all over the place. It leaves copies of files and checkpoints of files and things. And so this doesn't really take up all that much space because most of these files are tiny.

But there's just all those crap on your drive, on your CircuitPython drive. There's a utility to remove the crap. It decraps it.

I think it's actually called Clean, not DeCrap. Although that might have been a better choice for the name. So anyway, the point is a bunch of utilities there too.

And at this point, I'm using it on an almost daily basis. There's stuff that I'm doing all the time. I've actually have, in my office, I have a LED matrix sign that I've built using AdaFruits matrix portal, S3.

That's another project. And someday I'll try to get to a point where it's actually really releasable so that other people could use it. But one of the things with it is it's quite bright. And at night, I would like to turn it off. And I haven't actually added an off function to it yet. So what I do right now is I have a thing that runs every night on my Mac, which just uses Cirque remote in an automated way to poke the sign and just I edit a stop command. And all that does is it's just a loop.

That's like, while true pass. And then in the morning, I have a another one that does a reset to it. And so the sign goes off at night and it comes back on in the morning and I'm happy and I didn't actually have to fix the code and the sign to do the right thing.

So it's been really helpful to me and I hope it's something that may be helpful to other folks too.

Paul

You'll be happy to know that you're not the only Emacs user. Todbot is a big Emacs user as well.

John Romkey

Yes. I'm not the final Emacs user in the world. Sometimes people ask me, like, what editor do you use?

I want to use the editor you use? And I'm like, no, no, you don't. You do not want to use the editor that I use. You should use something modern.

You should probably use VS code or something like that. Don't do that to yourself.

Paul

Circremote supports dozens of sensors. I plugged in a DPS310 barometric and temperature sensor, ran Circ Remote slash dev slash TTIWI, DPS310, and it installed the dependencies and then I ran it again, and it spit out the temperature, pressure, and altitude settings without me having to write any code. How are you able to support so many sensors in Cirque Remote?

John Romkey

I cheated. So it's not really a cheat, but some people think it is. I actually had an AI write most of CircRemote.

And I have no illusions about this. I've been writing software since the late 70s. I've been pretty dubious about LLM's writing code. They've come a long way since just a year ago, even six months ago.

I have to say that the rate of improvement and progress in LLMs is just stunning compared to other things that I've seen over the course of my life. So I could write most of SIRC remote myself. I kind of didn't feel like it.

And I was curious to do an experiment. The one part that I would have had some trouble with would have been the web workflow. Talking to the device over serial over USB, not a big deal.

The web workflow uses web sockets. And I know how web sockets work, and I've worked with them a bunch. But I've never programmed them in Python.

And so just to be clear, for folks, CircRemote itself is a C-Python program. It's a Python program that runs on a Mac, on Linux, on Windows, CircRemote itself doesn't run on the device and isn't CircuitPython. What it does, though, is have a library of commands written in CircuitPython, which it then sends to the device.

So we've kind of got these two dialects of Python going on there, but CircRemote doesn't execute the CircuitPython itself. So I decided, why not take a shot at this? Let's see what happens if I try to have an LLM write this for me.

And at that time, I have a good friend, Elena Hardy, who has been doing a lot of work using Cursor. And Cursor is a front-end written that works with VS code. And it turns out there's a juicy Emacs compatibility mode for VS code.

And it actually is really good. And so that worked really nicely for me. Thank you.

Whoever wrote that, I am so grateful to you, or your AI, or whatever wrote that for you. you. And so Cursor can work with a variety of back-end LLMs, and I've been having it use Claude. I think it was on Claude 4, Claude Sonnet 4 when I did this.

And you'll get different results depending on which LLM, which model, language model you're using. So I basically gave it a set of instructions, and I tried to be really clear, and I tried to not give it too much up And I don't think this counts as vibe coding because I wasn't really just like throwing stuff at it and like, hey, how about if we do this? How about if we do that? It was more like, I want this, I want this file location. I want it organized like this. It was a spec that I gave it. And it worked. It was shockingly good. It wrote the code to send the code to it. One of the things that makes this work, It CircuitPython supports this thing called raw ripple mode.

And so this is something where it does no interpretation of what you're sending it as you send it. And then you send a Terminator, and that's when it goes and it actually processes the code. And this makes it so much easier to automate sending code to it to execute.

And CircRemote is not the only program that does this. There are other programs that use it this way as well. I think Thani does and probably Mu and a few other.

things. So that was great. So then I tossed in having it work with the web workflow. And I had to intervene in a couple of places there. It didn't get the correct URL for the device. I had to look that up. And I couldn't get it to work, though. And it was having a bunch of issues with it.

And I got frustrated. And so I have done WebSocket programming in Ruby. And so I basically just went and said, okay, just rewrite it in Ruby for me. And it rewrote it in Ruby in one shot. It just, it did it. And the WebSocket code in Ruby worked. And so that was amazing. And so I lived with that for a few days. And then I thought, how much is the CircuitPython community going to love me? If I give them a utility that's written in Ruby. And I figured not at all. And so then I decided, Let's just take another leap and have it translate this Ruby program that now worked back to Python.

And it did it in one shot, and it worked the first time I tried it, which just blew me away. That was really, really wild. So that's been really positive.

The negative to it has been that when things go wrong, they can go really wrong. and because I didn't write the code, I'm not familiar with it in the way that I would be, and it can be really tough to debug. And the LLM, the LLN is more than happy to go deep, deep down a rabbit hole trying to debug something.

But it's not very good at declaring defeat and realizing that you need to back up and take a new approach. I have to do that. And so one of the things I learned really, quickly was not only did I have to recognize when we were totally going in the wrong direction, which is fine, but also it can be tough to unravel what it's done in going in that direction.

So I just get like 99% of the rest of the world. And you definitely need to have really good get hygiene with this. It's easier to just throw away the work that's been being done and go back to where you started, when you started to debug this, than it is to get the LLM to reliably go back to a checkpoint.

Now, it's quite possible that cursor is pretty good at this, and it's not something I know how to do in it. Cursor's got a ton of stuff that it does, that I'm not an expert cursor user by any means. So there may be expert cursor users, like my friend Elena, who will listen to this and roll her eyes and be like, I told you how to do this, and she probably did.

that's some experience with that. So I also, you know, I wanted to support lots and lots of sensors and other devices. So I told Cursor to look at AetaFruits store and see what Adafruits sells and write commands for those.

And that was partly really successful. It was great at scanning what AtaFruid had available and it was great at organizing that. And the thing with Python versus CircuitPython is there's a lot of Python code on the Internet, and there's a lot less CircuitPython code.

And they look really similar because they are really similar. And so the training, the base of code in CircuitPython for the language models to be trained on is much smaller. And so it doesn't do as good of a job with generating CircuitPython code.

And sometimes it gets confused. and especially things for accessing the file system is different in CircuitPython versus Python, which is totally reasonable, not a complaint at all. It's actually just totally impressive everything that CircuitPython does.

But so I found that the LLM would frequently get confused about that, and it would still hallucinate things that are not there. Mostly it did a really good job at figuring out the Adafruit libraries to use for the devices, occasionally, I think once or twice, it hallucinated a library name that didn't exist. But mostly it did a good job with that.

I had to manually intervene and fix things much more often with the CircuitPython code than with the Python code. I also, at one point, it had a sort of systematic error that had done across most of the commands. And so I actually was able to tell it how to fix that and then have it apply to.

that to all the commands, which was a huge time saver. I figured out the fix. It did the work.

And that was pretty good. I liked that.

Paul

Yeah. That's pretty neat. You do a lot of work with sensors, both for yourself and for your community. How are you using sensors in your community?

John Romkey

I am trying to do some projects to do sort of, I guess one phrase for it is citizen science so that people can have sensor networks or communities can have sensor networks in them to track things like air quality or noise pollution or light pollution or things like that. Air quality is such a big, difficult question because we tend to focus on one or two things for air quality. We have the AQI calculation, which is really a synthetic number.

And it tends to focus on particulate pollution, which is a big deal. But also there's a ton of other things, respiratory irritants gases like formaldehyde. I live in Portland in North Portland, and there was an incident with a factory on that sort of not real residential part of North Portland, but which has been fined multiple times for releasing formaldehyde. And so I'd love for folks who are interested in doing this to be able to have cheap devices that they can put on a public sensor network that could monitor for stuff like this. And so that's kind of a passion of mine. I work with a local hacker space, PDX hacker space, and folks there help with this, and some of us are working on projects like that. Also like CO2 monitoring, CO2 monitoring.

Like CO2 can build up in a closed environment, like an office space or home, but also it got used as a proxy for airflow during the pandemic. A lot of people were getting CO2 monitors with the idea that if CO2 levels went up, then the possibility of COVID, the virus in the air went up as well, because that's a sign that air exchange isn't happening. And so they were less concerned about the CO2 than they were just about fresh air, which is fair.

And so a bunch of folks at the HackerSpace were very interested in that. One friend, Darcy Neal, is building personal CO2 monitors. And so we've collaborated on some hardware there.

There's a commercial device called Purple Air, which does something similar. It's an air quality monitoring device, very focused on particulate matter, and they have air quality maps that they generate from their data. I'd like to generalize that.

I'm fine with commercial products. There's a lot to be said for just buying it, having it be supported. That's great.

But I also like lower cost things available to hobbyists or DIY people, makerspaces, things like that. And so the hardware that I've been designing and the software that I've built is all open source. I got kind of waylaid by the tariff situation.

There's a board that I was doing a lot of work on and got to find a iteration of it spring before the tariffs hit, but they really jacked up the cost on doing everything. And I'm happy to, like, I'd love to build things in the U.S. But there's no options to do that.

The businesses just simply don't exist at this time. There's a really great place in China called JLCPCB, and a lot of folks use them. And they have, it's just like it's so easy to work with them.

You upload your designs through their web interface, you walk through it, and you get the order set right there. It takes minutes. And there's just nothing comparable to that in the U.S.

And also what I found trying to price things, it's the factories in the U.S. that do circuit board assembly, they want to do hundreds of thousands of boards, which is fair. You know, I don't begrudge them that.

I don't blame them. I would much prefer to deal with large commercial orders than individual hobbyists as well. But, you know, it's just like they don't want to talk to you if you want to do 10 boards.

And that's fine. That's totally fair. So there's simply no alternative available at this time.

And I know a lot of hobbyists and makers got really, had a really hard time with this. So I'm getting, you know, now the things have stabilized, even though it costs a lot more. It's still orders of magnitude cheaper to do it through China.

And so I'm trying to get back to that now and just, you know, hopefully don't get hit with, $1,000 tariff or broker fee or something like that for $100 worth of PCBs. But we'll see how it goes. That's pretty neat.

Paul

Last question I ask each guest. You're going to start a new project or prototype. Which board do you reach for?

John Romkey

That's a great question. And it would really depend a lot on the project. So like I have these LED matrix signs that are using Adafruit's Matrix Portal S3.

And if I were doing an LAMD matrix, that is absolutely the board I would go for. That's just really well thought out, well designed, and actually impressively chief for what it does board. If I were going for just a more general purpose, so almost everything I do is ESP 32-based because I always want connectivity.

But if I were going for just a more general purpose board with connectivity, Aida Fruit's Feathers are great. The board that I'm designing, it's just called sensor, which is, you know, but it's got connectors on it to hook up some more specific things like a particle sensor, which needs a weird little within cable connector. AidaFruit sells a version of that, but I like having it directly on the board because almost all the instances of this that I'm going to put together are going to need that.

So, you know, it's not very satisfying, but I might go for my own board. But Adafruit in general, like the feather boards are great. For just general purpose boards, Unexpected Maker makes some really, really nice hardware.

A lot of emphasis on low power, low overhead in the power if you want to use a battery with it. So I often look at his boards too. So those are both really great choices, yeah.

Paul

Yeah, those are great choices. John, thanks so much for coming on the show.

John Romkey

Thanks very much for having me. This is a lot of fun.

Paul

Thank you for listening to the CircuitPython Show. For show notes and transcripts, visit www.com. And if you're enjoying the show, do me a favor and share a review on your favorite podcast app.

It really helps. Until next time, stay positive.
