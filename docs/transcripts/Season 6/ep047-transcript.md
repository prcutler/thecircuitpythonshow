---
date:
  created: 2025-09-29
title: "Episode 47 - John Fletcher"
---

## Show Notes

[Show notes available here.](../../episodes/Season 6/ep047.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I welcome John Fletcher to the show.

John is a self-taught programmer who holds a master of fine arts and writing from the University of Alaska, Fairbanks. John, welcome to the show.

John Fletcher

Hi, Paul. Thanks so much for having me.

Paul

How did you first get started with computers and electronics?

John Fletcher

Well, I'm sure a lot of commonalities with other folks that you've had on. the show before. My father, who worked in the insurance industry and his office at home, had a Commodore 64 that my brother and I were allowed to use. So on that machine, I really learned to be frustrated with the command flame. Otherwise, the influence came from kind of stereotypical dad's stuff or guy stuff from the 80s. My father had home stereo, home theater type equipment. He had dual VCRs. He was big in. to re-recording and editing home videos, especially things for my brother and I to watch. And he was the one that got the Nintendo and brought it into the house. I grew up a gadget guy. Firmly in the generation of thought that opening scene and back to the future, fiddling with the amplifier, one of the coolest things ever, as well, the interior of the Batcave from Tim Burton's 89 Batman, of all of the monitors set up. That's a drool-worthy setup. I think John Park is doing his best to sort of recreate it in his workshop.

But the rest of it, you can blame Pokemon for. And I love the fact that we sort of have this shared lineage, where it was video games that got us into programming. With you, it was EverQuest with me, it was Pokemon.

But the first generations of Pokemon required a connection connection cables and things for doing the trading, but they also had hacking. And so trying to catch them all really was what provided my first exposure to trying to understand and work with any sort of a code base.

Paul

How did you discover CircuitPython?

John Fletcher

I discovered Adafruit before I discovered CircuitPython. What I mean by this is I'm an avid DIYer. I've got fundamental skills for pretty much all areas of home improvement, a pretty skilled amateur woodworker as well.

So I found Adafruit a little more than five years ago while I was looking for some simple practical electronics and things that I could integrate into some of my home projects. So we're not even talking at the microcontroller level here. We're talking about motors, actuators, et cetera, for really basic mechanisms.

But again, it was Pokemon that brought me back and back to stay. So, kind of a long story short, and if you know, you know, I was looking for a way to recombine power and data from Power Over Ethernet, Splitter. And because I remembered Adafruit, I went back to the website, ordered a couple of things to try to do that.

But I also added a couple of extras into my cart, because such as the nature of AdaFruit, things are priced so reasonably that it's, well, while I'm making the order, I might as well. So I picked up a QTPI, Sam D-21, a time-of-flight sensor to play around with. Long story short, I never got the power and the data to recombine, but the time-of-flight sensor, I integrated into a nighttime stairway illumination project.

that's now in its maybe second kind of version. And really writing the code for that time of flight sensor was definitely an aha moment for me. So I knew that working with CircuitPython was something that I wanted to do.

Paul

Very cool. One of the fun questions I sometimes like to ask is about your Discord nickname. It's spelled J-O-H-N-H-J, John and then John backwards. Set the record straight. What is the correct pronunciation?

John Fletcher

Yeah, to me, this is no end of comedy for me with this. When I wrote the name, I didn't have any pronunciation in mind. I mentioned to Tim Foamy Guy on one of his live streams that it should perhaps be pronounced like, you know.

And so as a result of that, he's got this kind of Northern European Scandy influenced. take on it that I like. John Park always goes much more British sounding with John Nodge, which I think is maybe more appropriate for considering my own names heritage.

I tend to think of it as John O. Yeah.

Paul

CircuitPython has the online code editor at code.cuitpython.org. You forked that repository and created a port of CircuitPython that runs in the browser using WebAssembly. First, what is WebAssembly or Wasam? And what led you to create a web assembly part of CircuitPython?

John Fletcher

Yeah, so I won't claim to be completely familiar with WebAssembly myself. So anybody who is expert in this will probably find this a little painful, and please reach out and correct me if I'm wrong. But in essence, the same way that CircuitPython is compiled in order to run on microcontrollers, the C code can be compiled to run wherever JavaScript runs.

So that compilation process sort of breaks down the higher order C language into something friendlier for machines, or much less friendly for people. For CircuitPython, the target is the assembly language or the instruction set for a given chip, your RP2040s, your same D21s and so forth, so that your code can work intended with the hardware. And as its name suggests, web assembly or WASM, wasam, wasm, however you want to pronounce it, It runs on virtual machines in the JavaScript runtime environment.

Since CircuitPython is C code, by using a different compiler, we can break down the circuit Python code to work in those JavaScript virtual machines instead of the physical hardware. CircuitPython is normally compiled using C-Make, but for WebAssembly, we use Inscriptin or EMSDK, which I think uses LLVM or Clang under the hood.

Paul

So what led you to create a web assembly port of CircuitPython?

John Fletcher

Yeah, so creating the web assembly port really grew out of a larger, a long-term project working on an extension for VS code, and really thought that it would be beneficial to use web assembly within that extension. One of the not necessarily issues, but potential sticking points of working with CircuitPython and Python in general, is the need to create virtual environments. And I thought having something more portable, since VS code is a web browser basis based on a chromium browser, why not be able to have a portable Python interpreter that wouldn't need the creation of a virtual environment because it's already pre-compiled.

It's more or less a closed system. I think you could sidestep some of the issues. inherent there.

So the biggest advantage to the web assembly port that gives folks access to CircuitPython interpreter in the browser without needing a physical board. In that case, the browser, in some sense, is the board. And why I wanted to create a port of CircuitPython specifically, Micropython, for example, has its own WebAssembly port Pyscript as a well-known as a variant of the micropython web assembly port.

The issue with that is, even though it's based on micropython, there are certain things in CircuitPython that we'd like to have specifically. And for the Pyscript, Pyscript has a very specific goal in mind, which is to provide a Python interpreter in the browser and very little more. And that causes a problem for anyone who is interested in integrating more of the hardware awareness.

And so the CircuitPython port was able to add back in some sense of board, pin, one of these sorts of protocols.

Paul

So how does CircuitPython work in the browser? Does it drop you right into a REPL?

John Fletcher

Yes, it should. After you spool it up, very quickly should drop you right into a ripple. Of course, in the web page, that needs the intermediary program of having a pseudo-terminal to work just as a UI.

Paul

So when you ported it over, you used the Windows subsystem for Linux, WSL, and branched off of CircuitPython from there. Any challenges working with the Windows subsystem for Linux? I know folks have sometimes run into problems compiling CircuitPython itself in WSL. USL, but how was your experience in using it?

John Fletcher

I didn't really run into any issues in using the subsystem for Linux. I had used it before. I tried building the Unix port of CircuitPython, and of course, I used the subsystem for Linux in that regard as well.

And so I found it to be very straightforward to use. The biggest problem I found was interoperating between the Windows subsystem for Linux and Windows itself in order to keep my files straight. And I suppose that's more of a workflow issue on my part than anything else.

Paul

How did using Claude code help in parting this over to WebAssembly?

John Fletcher

At base, the WebAssembly port would not exist without Claude Code. I simply don't have the skills. certainly wouldn't have happened within the month or so that it took, maybe two or more years. But it really was essential to getting this off the ground.

Paul

Any challenges with the prompts? I know there's not a lot of CircuitPython code out in the world for the LLMs to learn from. How did you work with the prompts to get it to do what you wanted it to do?

John Fletcher

That was a large learning curve. And I think that's true for anyone who first comes to using anything like Claude code. And it's figuring out some of the quirks, I tend to think that Claude works very well to work on a code base, as opposed to working with a code base.

In this case, because it was C code and not CircuitPython, it was a little bit more, I guess, straightforward on Claude's behalf. but nevertheless it still wanted to default to always be adding something to the code base rather than working within the confines of what was already there. That quickly became a source of annoyance.

There are workarounds you can leverage agents. Things to kind of keep clawed on track and give it a little bit more of a direction and the other issue was the context window management. While I was working on it, Anthropic kind of kept bumping up the context window.

But certainly there were sessions in working with Claude where we'd come to the end of the context window. We'd need to compact the conversation. And I should have just called it a day at that point because it really, was sort of like working in Groundhog Day, where we're starting all over again.

Nobody has any knowledge of what came before. So also a source of frustrations.

Paul

How can folks test out running CircuitPython in the browser?

John Fletcher

So if they are able to navigate to the repository, the repository has instructions for being able to spin up a local server. They can self-host the web page. They can get in, select the virtual workflow, and that will drop them right into CircuitPython Ripple, not an emulation of it or sort of under the hood, kind of clever text-based thing, but the Ripple itself.

Paul

I'll make sure I link to your repository on GitHub in the show notes. John, if anyone wants to learn more about you and your work, where should they go?

John Fletcher

Yeah, I've got a couple of other CircuitPython-related repositories through my GitHub, so people can feel free to poke around there as well. If folks really want to learn more about my work, I'm looking to make a career change. So if you or anyone you know and love is looking for someone, I'd love to do that.

Paul

Good to know. Last question I ask each guest. You're going to start a new CircuitPython or microcontroller project. Which board do you reach for to prototype or build with?

John Fletcher

Probably a Qtpy or Trinkie with an RP 2040. I mostly work on a surface tablet convertible, so something small and light that I can plug in that doesn't weigh down the side. I do wish the Trinkie had some exposed ports or pins.

So kind of in a pinch, I've resorted to using Waveshares variant. Sorry, Adafruit. I do hope that we can see some of the RP 2350 versions in those form factors soon once the new stepping becomes available.

But of course, if I'm just looking to play around with the CircuitPython interpreter itself, there's a handy Wazim port that I can use.

Paul

There absolutely is. John, thanks so much for coming on the show.

John Fletcher

Thank you so much, Paul. I hope I can do something else cool soon and come back.

Paul

I look forward to it. Thank you for listening to The CircuitPython Show. For show notes and transcripts, visit www.circuitpythonshow.com.

To follow the show on Mastodon or Blue Sky, check out the links in the show notes. And if you're enjoying the show, I'd be grateful if you could leave a review. Until next time, stay positive.
