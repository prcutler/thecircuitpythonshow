---
date:
  created: 2023-04-24
title: "Episode 26 - Seth Kerr"
---

## Show Notes

[Show notes available here.](../../episodes/Season 3/ep026.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Seth Kerr.

Seth is an embedded software engineer and open source hardware developer. Seth has designed the icy blue feather and FBGA development board for mobile and power conscious applications. Seth, welcome to the show.

Seth Kerr

Hey, it's good to be here. I'm really excited to come on.

Paul

I'm glad you're here, too. how did you first get started with computers and electronics?

Seth Kerr

My origin story with electronics is a lot like everybody else's, you know, parents had a computer. You're really excited about it. You know, growing up in the 90s and then early 2000s when the Internet was, you know, coming full force, I mostly got started with doing IRC chat bots back in the IRC days.

And I sort of put it down for a little bit, but then a couple years ago I was like, I got to really do something with my life. So I decided to go back to school for computer engineering and took my electronics class. And I started building transistor adders and stuff on breadboards.

And one thing led to another. And I'm here designing custom circuit boards and trying to make things a lot easier for people who started not too different of a place that I did.

Paul

Speaking of custom circuit boards, you have a crowd supply campaign running for the icy blue. FPGA feather. Let's start at the beginning. For listeners like me, what is an FPGA?

Seth Kerr

An FPGA is a field programmable gate array. So the easiest way I tend to think of it as if you put transistors in a circuit board, it's like that, but you're doing it with words. So FPGAs, they use a language model called hardware definition languages. And so what those do is you can describe functionality.

So if I want to add two numbers together, I can describe that process of adding it together. And these tools that we use for programming at PGAs, they will synthesize. So take what you have described and turn it into an actual circuit that's programmed onto these chips to do exactly, or in most cases, exactly what you described to do.

Paul

What are the advantages to using an FPGA over a typical microcontroller?

Seth Kerr

So an FPGA is sort of like a blank slate compared to a microcontroller. So a microcontroller, you kind of expect to have everything that you need to make your project go. You just need to code it.

Whereas an FPGA, it gives you the ability to customize your approach. If you want to do something specific and really fast, an FPGA would be a perfect tool to allow you to do that. It doesn't have to worry about, you know, am I waiting on other things to finish up to be able to do what I need to do?

It can just do it compared to a microcontroller. It's not as like general purpose. It's very, very specific.

Paul

What is your process to designing a board? Do you use KiCad or Eagle CAD?

Seth Kerr

For the longest time, I've used EagleCAD, and that's where I cut my teeth in school, because I got a free student license, and I figured out everything that I needed to with that. But I'm slowly working on transitioning to KiCad because, you know, takes cost money for Fusion and Eagle, and Eagle is not being regularly updated because they're trying to push everybody to Fusion 360 electronics designer. But, you know, KiCad offers just like a great open source and very, you know, progressively improved platform.

In that process, you know, I usually think about what I want to build. So like if I'm, for instance, if I wanted to make a, yeah, I've got a board here actually that I can share. So if I wanted to make like this Bluetooth board, for instance, I think about, okay, well, what chip I'm using?

what are some constraints that I have and what are features or things that I want to include. And with that, you know, what number of layer of PCB layers do I need to, in order to make that design function properly. And so from there, I go through and I pick parts that are going to fit those needs.

And then I start by just going through the data sheets and laying out the connections for those individual parts. then, you know, going back to the main microcontroller or whatever chip is going to be the host on the board, and I get those things all connected up, and then go into the PCB design. I figure out the design I want, so like, in case it's like a feather.

So, like, I have a feather, a pre-design layout for feather footprint, so I don't ever have to worry about the measurements or anything or where headers or USB are going to go. And then I can just weigh my parts out, how they're best going to route. And then I route them up, figure out power scheme, and then I'm done.

Send it off to Fab.

Paul

So now that we know a little about what an FPGA is, tell me more about the icy blue FPGA feather.

Seth Kerr

So the icy blue FPGA feather is my attempt to bring a very prolific and very easy to use format to the FPGA world. And it was kind of already done. There's an orange crab.

FPGA feather. It's a fantastic feather, but the various use it can be maybe a little bit intimidating, thinking about having to program it or like, oh, you've got DDR3 memory on that. It's a really cool board, but it's not quite at that beginner novice level that someone would hope to get into. And so I decided that it's going to go to a traditional approach, use a, an FT 2302.

to USB bridge, which is from FTDI, and that allows us to, you know, have only one mode to program. So there's some spy flash on there that you can load your bitstream onto through this USB chip. And it sort of removes the guesswork of, oh, well, am I programming the FPG directly?

Am I programming flash? And so that, you know, it leaves out a whole chunk of things that might be difficult to understand when getting into FVG. So, you know, the first thing is removing some of these barriers and make it confusing.

And then the second idea was using this feather format, we can make it part of an ecosystem. So if people are very familiar with Adafruit, they know that there's maybe 10 dozen feather wings out there that can be used with like I-squared C or spy interfaces or just regular digital GPIO. So what that does, it just creates a structure.

sort of like reward where it's like if you figure out what you're doing and you and you process you know work through the examples that you would have you know learning uh and how to use an FPGA you're like okay well I can I know how to set up a nice square C interface now I want to I want to use this feather wing that you know has a display on it I want to I want to figure out how to drive a display really fast with an FPGA so you know there's there's a door open for you for a project or in the 1Bit squared Discord, somebody had mentioned they had made a keyboard with an FPGA, which is really novel. You wouldn't think to like, oh, well, I'll just use a microcontroller, but microcontrollers don't inherently have matrix scanning as something that they're good at. But in FPGA, it's all real-time I-O. It's very fast, so you can do matrix scanning faster more accurately than you could on a microcontroller.

So they made an FPGA powered keyboard and I was like, oh wow, that's really cool. So, you know, thinking about what are the things that I can do, this feather opens it up because of the ecosystem that's part of. And so that's like these driving motivations as I've been working on it and refining it is all these cool projects that people are going to be able to do simply because of the format that it's in.

And the process for programming it is so much simpler. there's no gets work. There's only one way to do it. You know, that's sort of what it is, what the motivation is behind it, right? It also has, you know, some features on it that are, you know, like what you kind of expect for something that's geared towards people trying to make something or use something for the first time. It's got some LEDs on it and it's got the traditional RGB LED because everybody loves RGB, right? I've got tons of examples already ready for people to use on GitHub that are set up.

They've already been tested. And then as well, a bunch of project boards as well that will have all the code. I say code, but it's kind of just like the HDL files.

They'll all be ready for people to look at, to dissect, and hopefully inspire people to dig deeper and start digging into the feather ecosystem.

Paul

You kind of touched on it, but within the feather ecosystem, how could you use the Icy Blue Feather with another board running Circuit Python, for example.

Seth Kerr

So the example that I like to give for this is, so the FPGA that's on the Icy Blue Feather, it has what are called DSP blocks, so digital signal processing blocks. And essentially what they are is they're these multiplier box that can multiply incredibly fast. And they've also got these accumulators, which essentially you multiply and accumulate. You can run some very fast in a based digital signal processing.

And so one thing that most microcontrollers are not good at is digital signal processing, unless they have specific, you know, hardware for that, like, hardware floating point units. It may be a little bit slower to do it on a micropotroller. So one thing that people could do, interfacing, you know, the icy blue feather and another feather.

So, like, say the feather, rp2040 for instance. And this is a really good example because the, the, RP2040 has two 8-bit PIO registers on it. And those can send data single clock cycle and receive data single clock cycle, which is essentially like, it's almost like having an FPGA on a microcontroller.

But essentially what this allows you to do is you could take eight pins on your feather, set eight pins on the icy blue, and send data back and forth incredibly fast. Do your DSP. So, like, if you're, you know, trying to run a very, like a FFT, fast-for-year-transformer, you don't have to worry about doing that on your RAP2040.

You can continue collecting your data, sending it on, and not have to worry about losing clock cycles, you know, doing your FFT. You can offload that to your FPGA. And that's, you know, that's a huge advantage that you would have with using the Icy blue within the feather ecosystem, is the ability to do these tasks very quickly off-chip without having to worry about O-M-I, am I squeezing the most resources out of my microcontroller?

Paul

You touched on HDL earlier. For those used to programming with CircuitPython, how different is it to program the icy blue feather?

Seth Kerr

It can't be a little bit of a learning curve, just because you're going from a mindset of telling hardware that's already preconfigured how you want it to run, right? So it's already converted into instructions that you don't have to worry about. With HDLs, you're, you know, like I said, you're telling it how exactly it's going to run, what you're doing with the data that comes in and now, what you're doing with the data that's interlinked and shared between described modules.

But in terms of, like, the environments that you use and whatnot, you can use DS code to write your HDL or your varrolog. code. The examples that I have set up in the GitHub repository, they are all Barlog, which I tend to like Barlog a little bit more because it's not really a good comparison, but it's considered closer to C than VHDL is, but I tend to find it a little bit easier to work with.

It tends to give you this feeling that it's a little bit more understandable. It's not as, like, the language is a little bit easier, the words of these to describe what you do. But with that in mind, like you can code it with the VS code, and then there's make files that are very easy to understand what's going on.

If you want to set up a new project, you essentially just copy the make file from another project, and then you just make sure that your file name and the module name in your top-level file match inside the MCFile, And then you just do make build and then make program flash. Some of them have a slightly different make command just because I have like maybe have multiple examples in the directory. But for the most part, it's what happens inside those commands is, you know, like there's not really anything, not much that needs to change.

You're really trying to make sure that the barriers to starting out are as low as possible.

Paul

Well, we're almost out of time. But before we go, I like the. ask each guest one last question. You're about to start a new project. Which board do you reach for?

Seth Kerr

I'm kind of biased towards my own stuff, but one of my favorite boards to use is the Red 2040, which is a USBC RP 2040 board that I made that is like slightly smaller than a feather, has a neopixel and everything on it. It's a cute little board. It's very breadboard friendly. And it just works for a lot of stuff. stuff that I'm doing.

Paul

If people want to learn more about you or the icy blue feather, where should they go?

Seth Kerr

So the icy blue feather currently isn't pre-launch on CrowdSupply. So if you go to CrowdSupply and go to the pre-launch page, you'll see the icy blue there. I also have a website where I'm trying to get back into more blogging and whatnot around the company. So that's oakdev.com.

Paul

I'll make sure to link to that in the show notes as well. Seth, thanks so much for being on the show.

Seth Kerr

Thanks for having me. Appreciate it.

Paul

Thank you for listening to The CircuitPython Show. For show notes and transcripts, visit CircuitPythonShow.com. Until next time, stay positive.
