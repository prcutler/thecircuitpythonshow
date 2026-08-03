---
date:
  created: 2025-02-24
title: "Episode 40 - Building CircuitPython with Dan Halbert"
---

## Show Notes

[Show notes available here.](../../episodes/Season 5/ep040.md)

## Transcript

Paul

Welcome to the CircuitPython show. I'm your host, Paul Cutler. This episode, I'm joined by CircuitPython core developer Dan Halbert. Dan first visited the show back in episode 28, which I've linked to in the show notes. Dan, welcome back to the show.

Dan Halbert

Thank you very much, Paul. It was great to be on last time, and I'm really looking forward to this session as well.

Paul

In the last episode, I chatted with Bradan Lane about designing a PCB. That's a time when someone might want to build CircuitPython for this. their new board. When else would someone want to build CircuitPython from source?

Dan Halbert

There are a bunch of different reasons why somebody might want to build CircuitPython. I mean, one is just to see how it's done. But usually somebody has some motivation.

One thing that happens often is that they want to turn a feature on or off, or they need to make room, they want to turn on a feature, and we say, oh, that feature doesn't fit. But if you turn off this other thing, you can turn on this thing. And so that's a common reason to do that. Another common reason is that they've got some new board that they want to support, and so they want to try to make a build for it and test it and then maybe submit it as a poll request if they think that other people would be interested as well. Another reason is because they want to add some frozen modules, because they want to build that comes with some libraries already built in. For instance, they want to distribute a build to some other, to like users of their software, for instance, something like that.

And yet another reason is that there's a problem and they want to debug it. So it could just be that they want to run a debugger or put in some logging printouts. We might suggest that if they're having trouble.

Or they might want to do what's called a Git bisect where you take two versions and you take some versions. You don't have a version that, You know, it works, and let's say the latest version doesn't work. And then you want to find out, well, where was the change that broke it?

So what Git BISC does is that it divides things up. It'll go to the middle of that range of commits. And then you say, it did work or it didn't work.

You build it and say it did work or it didn't work. And then it keeps dividing. It does a divide and conquer thing until you get down to the commit.

Paul

So let's dive in. What is the process for building CircuitPython? What are the prerequisites? What should someone think about before they start?

Dan Halbert

Sure. Well, first of all, I would say before you start building it, you have to look at the building CircuitPython guide, which you can find on the unlearn.adototot.com. And we try to keep that guide up to date. Just before this podcast, I was reviewing it and I found a bunch of things that I wanted to update. So if you find something that's broken, tell us. We do development of CircuitPython on Linux. I use Ubuntu version 2404.

Jeff uses Debian, but it's very close to that version because Ubuntu is a Debian-based distribution. Scott uses Arch, which is kind of more up-to-date, but he also knows how it differs from kind of more vanilla distributions. So in all cases, it's easiest if you start with a Linux distribution.

And that's what I'd recommend if you're at all familiar with command line stuff, even if you're already familiar with command line stuff, say, on MacOS, you can build on MacOS, but there are always things that change. So I'd say start with Linux, and there's some descriptions about how to do that. Then just go through that build guide.

There's a bunch of pages under the introduction page about how to set up your system to build. You have to install a bunch of packages, both system packages and also Python packages. There's a page about setting up for Linux.

There's a page for setting up under MacOS, which details some idiosyncrasies. There's a page about setting up under Windows subsystem for Linux, WSL, which is basically Linux running inside Windows, and it really is pretty much just like using Linux. So it's kind of a substitute for setting up Linux instead of using a virtual machine.

In many ways, it's somewhat easier. So there's a page for that. And then there's some stuff about, well, if you had some more idiosyncratic Linux distribution, how do you use that?

And I'll also say that there's something that, which I haven't tried, but there's a technique for using GitHub code spaces, which lets you use kind of a prepackaged Linux environment. And there's a link to that. User Bablock B has described how to do that.

There are a whole bunch of steps of getting things set up. And then it's best if you fork CircuitPython. you could use the ATAF root.

You could clone the AtaFood thing. But if you're thinking of making any poll requests or anything like that, it's probably easier if you fork it. Make a branch right away and then just start building.

And follow the instructions. If you're building on Espressive, there's a special page for that as well.

Paul

So what are some of the different things that someone might want to know between the different ports, between a Broadcom build and an Espressif build? Are there any big gotchas that come to mind?

Dan Halbert

Sure. So many of the ports are straightforward. We use Git submodules a lot, which pull in various pieces of third-party software.

So for each port, in most cases, there's some port-specific sub-modules that you need to add. There's a description in the build guide of how to fetch sub-modules. You can fetch all the sub-modules for all the ports.

That takes a long time. And if you're on a slow network connection, you might not want to do that. You can also fetch the submodules for just a specific port.

And that's explained in the guide. So once you have the submodules, then you can just pick a board in that port and type make capital board equals in the name of the board. And it will start building that.

If you typed make in a ports directory without a board name, but actually will list you all the board names. which, let's say, the expressive port there can be, there's more than 100, or hundreds even. That's an easy way if you don't remember the board name, or you could look in the board's directory and find the directory name.

That's the board name.

Paul

For example, on the Espressif builds, it actually pulls in its own Python virtual environment and builds within that so the user doesn't have to do that. Is that correct?

Dan Halbert

You have to run some scripts to set up what it needs for Python. I'll back up a little bit to say that we use Python a lot in the build process. It used to be, say, in Ubuntu 2204, that we just install various Python modules and libraries right into your own user space, okay, and you share that with all your other uses of Python.

Beginning in Ubuntu 2404, you can't do that. You have to create what's called a virtual environment or a VN. there are directions for how to do that in the build guide.

So you're right, expressive sets up its own VN. And if you have one already set up, you can't set up a VN inside a VN. So the expressive build tools will complain and say, you can't do that.

And so I describe in the Expressive Builds page how to get out of your VNV and get into their VN that they create. For the Broadcom ports, those are very unusual. Those are these, they run on bare metal.

Raspberry Pi, you know, 3, 4, 5, say, and Pi 0. We're not talking about Pi Pico, okay? There are a lot of things named Raspberry Pi, but we're talking about the boards that can run Linux.

And in that case, you need a separate version of the GCC compiler and its associated tools that's specialized for that Broadcom chip. Or it's called a Cortex A chip. it's a kind of arm chip.

Most of the other boards are CortexM arm chips, not all of them, but many, many of them are. So to back up a little bit, one of the things you have to do to do is setup is install the GCC tool chain that's maintained by arm in most cases. The expressive build tools do that for you, but in most cases you have to do it by hand.

And we describe how to do that and which version to use, because if you use the wrong version of the compiler too old or too new, then you're going to get compiler errors. You're going to get compilation errors when you do a build. So pay attention to that in the build guide.

Paul

That's definitely something that people need to pay attention to. It's very easy to get the wrong version of GCC.

Dan Halbert

Yeah, exactly. And I also would say that this is a detailed, very complicated process, and you're probably going to get stuck at some point. And feel free to ask for help in Discord in the CircuitPython Dev channel, which is where the developers hang out, and we can help you along and get you over whatever stumbling block that you're encountering.

Paul

That's good advice as well. So we've gone through the guide, and we've got CircuitPython building from source, and we've got our PCB that we designed in our last episode as well. What needs to happen next to add that board to CircuitPython?

Dan Halbert

So what you want to do is find a board that's kind of like your board. You made a simple SAMD21 board, say. And I think Braden Lane's board, I'm not sure which chip it is.

I think it's one of the SAMD chips. I believe so. Yeah.

So find a board that's like your board. Look in the board's directory in the port for your chip and or chip family. And just find one that's pretty similar.

And in that words directory, you'll find a bunch of files. there's MP config board.h, MPconfigboard.mk, mpconfigboard.mk, pins.c, and board.c. And those all need to be customized for your particular board.

In some cases, you can use the boilerplate version of those and change just a few things. But the easiest thing to do is create a directory for your new board, give it a name, put the manufacturer name at the front of the name, and then the name of the board. and separate them with underscores, and then copy some board files from the most similar board, and then start editing them.

It's always better to start by changing an existing thing than starting from scratch. There's also, for expressive boards, there's yet another file called SDK config that you also need to copy and change. So MPConfigboard.h and.m.k.m.cforg.m.

like the name of the board and its USB identifiers and some other things like how much flash there is, which flash chips you're using. Pins.C gives the name of the pins and also other things that are in board like board.i2c or board dot stem I2c if you have a stemming connector. And board.c has optionally routines that set up the board. Like you have an, if you have an, if you have on board display, then you want to write some code that runs as soon as the board starts that sets up the display.

So you can see the REPL output on the display. On many boards that don't have display, board.c is just empty. It uses some default routines.

So all those things happen, and then you can do a build, and then try to copy the UF2 or the dot bin onto your board and see what happens. Usually you can just do run make over and over again. If you make certain kinds of changes, like you add new strings or new error messages or a new MPQster, which is a special kind of string name, then do a make clean first because otherwise you'll get weird errors.

And that's also true in expressive. If you make some changes to the ESP IDF settings, then you'll need to do a make clean because otherwise it will. won't rebuild the ESP IDF part of the base software.

Rebuild that.

Paul

When you're updating the pins.c file with the pin information, this is the file where you want to match the silk screen to what you put into the pins file. Is that correct?

Dan Halbert

Yes. There's a guide called How to Add a New Board to CircuitPython. And that describes in detail about changing these, copying these files and changing them.

It's not in the main building CircuitPython guide. but it's in the sidebar of that guide. So that describes how to change all these, and it describes also kind of the naming conventions for the pins.

Like you do want to make them match up with the silk. If they're just numbers, they can't be that. So it says, like, put a D or a GP or an I.O. in front, depending on the board family.

Look at an existing board, and in that board family, there's, like, a sort of a typical nomenclature. They're kind of sort of, they're often canonical. names for things. So try to copy those names if you can. The best reason for copying names is that it means that any particular piece of software can run on more than one board without changes or with easy changes.

Paul

Oh, that makes sense. I hadn't thought about that. One of the things you mentioned in passing earlier was that you need to have a vendor ID and a product ID for the USB device.

When and how does someone get a VID and a PID to add to their device? Yeah.

Dan Halbert

That can be a sticking point. So USB vendor IDs and product IDs are both 16-bit numbers. So a vendor ID comes from the USB organization.

I can't remember. Maybe it's a foundation, I can't remember. But it's at usb.org.

And in order to get an official one, you have to pay thousands of dollars. All right. So Aida-Fruit got one a long time ago.

And most manufacturers of some size got them. But that's a lot of money if you're just building a hobby board or something like that. So how do you get around that problem?

Well, you could just invent or reuse USB VID and PID, but we're not going to add that board to the list of CircuitPython boards if you invent one or just make one up because it's unofficial and it's sort of like not, It's easy to get in trouble, that way, kind of. Sure. It's true that many manufacturers, you know, small manufacturers steal the IDs and PEDs or just make them up, but don't do that.

So there are a few USB vendor IDs that are retired. And some people have taken over those vendor IDs and have been issuing product IDs under those vendor IDs. There's a website called PID.

codes, which you can go to and get one for free. It involves submitting a poll request to a GitHub repo. And Scott is one of the people who can assign vendor IDs through that repo.

If you're making an espresso board or a Raspberry Pi RP2 something board, then you can apply to those manufacturers for, a product ID and they will assign you one. Usually only takes a week or two. There's a mechanism for both of those to do that.

You use their vendor ID and they are allowed to give away product IDs under that vendor ID. So both of those things will work.

Paul

So that's almost something you want to be doing in parallel while you're building CircuitPython for the first time since it takes a week or two to get one.

Dan Halbert

If you are interested in submitting a board, yes. If you just want to build CircuitPython, you don't have to do this at all. Or if you just want to experiment and build your own board, nobody cares what the product ID. You're not distributing it, so it doesn't matter.

Paul

So for those who are distributing it, we've got CircuitPython running on our new board with a VID and PID. You want to add it to CircuitPython.org so it gets built every time when a new version of CircuitPython is released. How does that process work?

Dan Halbert

Okay, so it gets built whether or not it's on CircuitPython. dot org? Circuitpithon.org doesn't determine what's built.

What determines what's built is what's in the CircuitPython source tree. But for it to show up as something that you can download, when you submit a pull request to CircuitPython data board, we ask that you submit a parallel pull request to CircuitPython.org. And that's also explained in how to add a new board to CircuitPython.

So there's sort of a standard format of how you describe the board. There's a fixed set of features that you can say it does or doesn't have. And we want you to take pictures of it, clear pictures, and supply three different pictures in different resolutions.

And that's all explained in the how to add a new board to CircuitPython. When this happens, you know, when you start submitting a poll request, like it's going to go through, go ahead and submit a poll request to circunpython. or we'll remind you because we're not going to finalize the whole thing until both of those things are ready.

That makes sense.

Paul

Thinking back through this process, are there any things that come to mind where people get stuck or challenges that they seem to run into more often than not?

Dan Halbert

I would say, make sure that you install the correct version of GCC. A lot of people just say, oh, I'm just going to install the one that comes from Ubuntu. The compiler that we use for the arm chips is called arm-dash-none-dash.

EABI-GCC. But if you just install the version that comes in the Ubuntu or Debian distribution, it's the wrong one. So don't do that.

Another thing is we haven't mentioned, but is that we use pre-commit, which is the thing that reviews your changes before you make a commit, and it checks formatting and other things like that in advance. And so it's explained in the build guide about how to set a pre-commit. That will save you a lot of round-trip time because otherwise you'll be making simple, say, formatting mistakes.

And when you submit the pull request, you'll have to wait for the bill to complete. Then it will take a long time. So pre-commit will check for that stuff in advance because we run pre-commit when you submit a poll request also.

So you've got to pass that one way or the other. That makes sense. Yeah.

Getting the expressive build right is a lot of trouble. So we sometimes have to guide people through that. And dealing with the Python virtual environments is tricky because a lot of people haven't used that in the past.

And also, when in doubt, do a clean build in case you're getting odd build errors, because you may obtain something that needs, in which you need to do to start from a clean build. And if you're building on Mac OS, getting the right Python version is very difficult. you know there's an XKCD cartoon about how much trouble it is to set up Python properly.

And how many different versions of Python there can be available on MacOS. So that's a problem.

Paul

I'm on a Mac running HomeBrew and I run into that all the time. So that is definitely something that people should be looking out for.

Dan Halbert

Yeah, yeah. And there's so many versions of MacOS and things change abruptly. You know, they keep the same Python version for a while.

and then they jump up several versions. And it's just really confusing. And there's just a lot to learn here.

If you haven't used Git before, you've got to learn Git and GitHub. There's just a lot going on here. And so, you know, we try to make a recipe, but it's important that you try to spend some time and do some studying about things that you don't know about so that when something goes wrong, which invariably will, that you can have some understanding of like, well, what is really going on here?

You know, why is this error happening? You know, you know. But we're happy to help you along.

Paul

That's definitely good advice. And if people get stuck, again, come to the CircuitPython dev channel on the Adifer Discord, and you and the other core developers can sometimes help them out. Yeah, yeah, very much.

Well, this was all good advice. Dan, thanks so much for being on the show.

Dan Halbert

You're very welcome.

Paul

Thank you to Dan for sharing his knowledge of building CircuitPython. For show notes and transcripts, visit www.circuitpythonshow.com.

Until next time, stay positive.
