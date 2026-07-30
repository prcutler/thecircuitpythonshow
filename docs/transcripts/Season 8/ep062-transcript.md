---
date:
  created: 2026-08-10
title: "Episode 62 - Tod Kurt Part 3"
---

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. This episode I welcome back Tod Kurt.

This is Tod's third visit to the show, and you may also know him from our other podcast we host together, The Bootloader. Tod is co-founder of Thingm, a ubiquitous computing device studio based in Pasadena and San Francisco. He is the creator of the popular Blink1 USB notification light and BlinkM, the smart LED prototyping device for Arduino.

Tod is a contributor to Make Magazine, author of the hacking Roomba, an active member in the Arduino and CircuitPython communities, and co-founder of the Los Angeles Hacker Space Crash Space. His past professions include Systems Architect for go-to.com, the first pay-per-click search engine, and an ML researcher at Yahoo Research Labs. Before that, Tod was a hardware and firmware engineer working on robotic camera systems for probes that went to Mars.

Tod, welcome back to the CircuitPython show.

Tod

Hey, thanks for having me.

Paul

I had Dan Halbert on earlier this year, and we chatted about building CircuitPython. It's recommended to do this on Linux, but not everyone has Linux or the knowledge to get up and running with Linux. You've come up with another solution for building CircuitPython using GitHub actions. Tell me more about it.

Tod

Well, so this all started because if you ever submit a pull request to the CircuitPython repo, it will automatically rebuild all the firmwares for all the boards and see if they all still work, like work in the sense of, do they fit in the available flash space for the board.

And are there any compile problems? Because if you're only testing your little change on one board, and it's something that can be used on other boards, on different architectures, there might be problems. And this has happened to me a lot.

So it's really great that one of the gates that a pull request has to go through to be accepted into CircuitPython is that it has to pass through. Does it build for all the boards? And there's like, what, 700, 800 boards now?

So like, this is a pretty big list. I think they've changed it recently. So if it detects that your change is only for a certain class of boards, it'll only build that class.

So that's really handy because they're using the same build process for these PRs. They use to build the official firmware for CircuitPython, which means you can get a pretty accurate test of what your firmware will look like for reels. Whereas like, you know, if you're building on your computer, you can set up the CircuitPython build environment to work on Windows or Mac, which is what I usually do, or on Linux, which is the preferred way.

But even if you're on Linux, you might have a different version of the, say, ARM-GCC compiler because that's installed globally. That's not installed just in the CircuitPython directory. And so there's been a lot of weird changes over the last 10 years of CircuitPython, where a small change in the compiler version will actually change a big amount of how the code gets compiled.

So having something that produced CircuitPython firmware via a GitHub action that is fully like the way that CircuitPython is really built was my initial goal. And I'm like, can I make a service so that anybody can go and just say, I want a version of CircuitPython for the Resbrae Pi Pico that doesn't have ePaper support, but also includes a bunch of frozen built-in libraries. Because you can do that with CircuitPython.

And that's a pretty big ask. That's a, you can do that on the command line, you know, if you know what to do. But it's hard.

And so I started on this pathway, it's just starting this path. And it turned out that like, oh, doing it for everybody is hard because I am now sort of using up my GitHub actions credits for anybody. If you are a GitHub, if you have a GitHub account, you can make a little GitHub token and then run the action really easily on your own account.

So there's this project that I created three months ago now called, what is even it called? CircuitPython Custom. And it started out as first, as I said, of tools I used on the CircuitPython checkout to sort of see what boards there were available in terms of the board IDs are.

Give me a list of those. And then it turned into, for a given board, show me all the things that are enabled for it. because you might have seen, if you ever go to the CircuitPython documentation, there's a lot of built-in modules, but they're not built in for all boards.

That's kind of confusing, I felt. I wish there was a better way that it showed that. Maybe you could pick a board at the top, and it would then kind of gray out the modules that aren't available to you.

Because in the case of SD cards, for instance, there's two major ways of talking to SD cards. The module called, I think it's just called SD card, And there's a module called SDIO, which is four to 10 times faster or more. But that only exists on, I think, ESP 32.

I think it might be available soon for Raspberry Pi Pico, but, you know, it's kind of a bummer. We don't have that.

Paul

I know Dan's been doing a lot of work on SD cards lately. So you're probably right that something is coming soon.

Tod

As more of Adafruit's products explicitly, but as more products in general have SD card sockets on them, to store stuff. It makes a lot of sense to use the faster way of talking to SD cards. So this tool kind of became an outgrowth of me just trying to figure out what the heck, how the CircuitPython repo works in terms of like board IDs and these various build flags that turn on and off various modules, you know, that turn on and off, say, the touch sensor or the keypad or the neopixel or, you know, talking to floppy disks, you know, do I really need floppy disk support?

Probably not. Let's turn that off. And just learning how to do all that.

And I figured how to do all that on the command line. But even when I would do a normal build, I would notice that my builds were a little bit different in size than the official builds. And it's like, oh, that's because I'm doing it on a Mac with this particular version of the ARMGCC compiler or something.

And so then I started making it again. GitHub action that would trigger on my thing. I'm like, well, it's still hard for me to get all that information into that action.

So let's build a little thing that is now a web page, lets you turn on and off these various build flags. And it shows you what command line commands that turns into if you did want to run it on your own computer. But at the bottom, you can also trigger a build on this little custom web page, and it will trigger the action, and then it will build it.

And then you can just download it from your actions directory or from your actions tab on GitHub.

Paul

I'll link to this page in the show notes, but this is fantastic. You can search all the boards so you can choose like Raspberry Pi Pico like you mentioned, give it a custom name. And then you choose in checkboxes the different features you want to add.

And you've got it split up into core I.O. Display, audio, wireless and networking. I could keep going on.

So you've made it really easy for the user to figure out which modules they might want.

Tod

This is one way, one area where I had Claude Code, help me out because, so there's this one big file that contains all of these defines. They're all CIRCUITPY underscore and then a name like bus I.O, PwMIO, you know, CIRCUITPY underscore can IO for the Canbus interface, if you know what that is. And all of these defines are defined for all the builds, but they only apply to certain what are called ports, basically which certain chips like the ESP 32 or the RP2040 or something.

And then there's also, you could, you could in theory have these defines that only work for a very specific board inside of a port. And so it was very confusing to know which of these magic defines are defined for all of CircuitPython, for defined just for, say, ESP 32, and it defined just for just for this board. And so I tried to make a little interface that split it out both conceptually, like, oh, this is for core stuff.

This is for display stuff. This is for USB. But also showed when the thing was defined for a specific port for a chip.

It's not perfect. But it does let you see that like, oh, for the Raspberry Pi Pico, if I select that, I can see that, okay, CircaPi underscore Pults IO is defined on the port. level, which means for all RP 2040s. And Circa Pi underscore PicoDVI is defined at the board level.

So it's defined just for the Raspberry Pi Pico. So it probably won't be defined for another RP2040 based board that is smaller. Like maybe the QDPI won't have the Pico DVI thing enabled because it doesn't have enough pins for instance.

And like turning on and off, each of these can have big implications on how big the eventual firmware is. If you turn on too many of them, the build maybe won't even work because you're turned on a feature that isn't available for that board, or it'll bust the amount of memory you have available to put your CircuitPython inside of.

Paul

One of the neat things is at the bottom of the page, you have the CLI equivalence. So you actually can show the user. This is what it would look like if you were doing it in the command line on a computer.

Tod

Yeah, this is actually what I use the most is I'll go through and I'll click, click, click, click on things, and then it'll tell me, okay, run these commands to do that. Because I have a CircuitPython build environment kind of set up all the time.

And yes, I could wait for the like five minutes it takes for GitHub actions to do a build if I want it to be exact. But if I'm just testing stuff out, like, oh, let's see if I can add in, for instance, one of these you can do is you can put in a bunch of what are called frozen modules, basically put in pure Python, CircuitPython libraries into the circuit. Python firmware. And so you can do that for the ones that the CircuitPython checkout knows about.

You can just go click, click, click, and turn on like the Neopixel or the MIDI library or something like that. And then you can see what those commands are, which then tells you, oh, when I do that, it's actually creating a file called user underscore pre-UMP config port.mk, and you can add extra stuff in there. So you can, oh, I can add other stuff. I can add other libraries that aren't in this list, for instance.

Paul

Could you add custom code that you've written for the board in addition to libraries?

Tod

Yeah, but then at that point, I wouldn't be using this tool. Like, this is what I did recently. I wrote a CircuitPython core module.

It's now a core module that we used to not be a core module, but Scott thought it was useful enough to be a core module. It was for this UREX synthesizer device that has a very strange digital analog converter that needed very specific types of commands that the existing CircuitPython code didn't support. And so I wrote a C code with a Python class that was custom to it, and it was inside the directory for just that board.

And it worked great. But it was like it was a whole thing. And it was basically an extension of this custom file.

There's other things you can add. But then Scott was like, hey, this should be a core module. I'm like, well, that changes.

That makes it a much bigger problem because now I have to make these files work for kind of all of Python. I'll sort of Python instead of just this board. But it all worked out.

Paul

So walk me through the process. If I want to do this, I fork your repo first. Yes.

And I get my GitHub actions token ready. And I come back to your web page. I don't have to fork the web page or anything like that.

Tod

You need to fork. Well, let's see. Yes.

You must fork this repo. Yeah, you must fork the repo. Yeah, I tried, this is the thing.

I tried for about a week to get this to work where you didn't have to fork the repo. But basically, if you fork the repo and enable actions for this fork, then it'll create the webpage for you, your own version of this web page that I'm hosting on my repo. And then at that point, you can paste in your workflow scope, personal access.

access token that you create from GitHub.com. And then you can trigger build and it will run the action for you. But yeah, you do need to fork the repo.

Right.

Paul

I was just confused about the web page, whether I used yours or whether I used the one that's in my own fork.

Tod

Yeah, I mean, for exploration, you can just use the web page to see like, oh, what command line commands does this correspond to? And also, it's fun to sort of see, like, one of things that I found really, really fascinating is to see how many different devices and types of processing or whatever that CircuitPython supports. There's this thing called Font I.O. That is built in. I didn't even really understand that was a thing. You can go in and look at it and go, oh, that's pretty cool. But, you know, one of the things that I've had to do in the past is I've had to turn off a bunch of stuff. Like, when I was doing a bunch of CircuitPython with Sam D21, the original cutie pie, it's got no space.

It's filled to the brim. And so any little change you make will like overflow it. And so I was used to going in and turning off on the command line, turn off this library, turn off that library, turn off this other library.

And so I could add my extra code to it. But it was always kind of a, it was always kind of hard to figure out quickly at a glance which things are enabled, which things are not enabled. And so one of the things I like using this webpage for, even if you don't trigger a build is just, oh, this is what it's, this is what's enabled.

For this particular board, these are the things that enable. So you can like, right now I can go into the board. I can type in QD-Po.

There we go, QDipi. And I can choose the QDiPiM-Zero, which is the SAMD-21. And I see that, yeah, most things are turned off.

But one of the things that is turned on is the Circupi underscore PS2 I.O, which is for the, sorry, the PS2 keyboard and mouse support. You have the old, old IBMs. Like, I can turn that off.

I can probably save like maybe 100 bytes from that. It adds up. And that might give me just enough, yeah.

Paul

So most folks might know us from hosting the bootloader, and recently you shared serial plotster. And we're all sad that Mova's been sunset and won't be getting any more updates. So you took it on yourself to write your own serial plotter in Rust. Tell me a little bit about serial plotter.

Tod

I don't know if many people actually use the serial plotter that's built in to say the Arduino IDEE, or I think even Thani has a plotter now, but you knew had a platter, and it was a very good plotter, and it was a multi-value plotter, so you could, like, print out a Python array, and it would know how to plot that. And so it was a really great way to, like, do a level up from printf debugging. You can actually see value debugging, where you can kind of see how values change over time.

I'm a command line guy. You know, I edit my files and a text editor that isn't part of an IDE. I use Tio, the commandling tool to talk to serial ports.

in a terminal window. And so I'm like, well, let's have another program by itself that is a serial plotter. And I had one several years ago.

And of course, because of time, you know, it doesn't work anymore. And I'm like, well, you know, the serial plotter isn't that hard. It's just reading values and graphing them on an X-Y. And there's this toolkit called Tori, T-A-U-R-I that is a, it's a rust environment that lets you web pages for the GUI and then Rust for the back end.

If your application has a back end, like a lot of people, like if their application is entirely a web page, the actual Rust involved is very little. It's just all JavaScript in a browser window, basically. And it's basically like a Rust version of Electron, if you know what electron is.

But the benefit of Towery is that it like makes executables that are 10 megs instead of 200 megs, because it uses the OS's built-in, web render, which on Mac is WebKit on Windows, it's Edge or something, which is chromium-based, I think. And so, I don't know Rust, but I love this idea of Tari. Let's have Cloud Code help me write the Rust to graph stuff on an HTML Canvas, because you know, that's a real solved problem.

That's easy. You know, the GUI for that kind of stuff, you just do HTML elements and canvas commands to draw lines, but how do you talk to rest? How do you write the rest to talk to a serial port?

And so I had, I had cloud helping out with that. Talking to serial ports is pretty easy. Once you know how that works, seeing how it works in rest is pretty obvious. The main thing for me was once I got it working was trying to get it to work at audio rates. So for instance, if I'm like reading data from an audio device, I want to be able to maybe see that as an audio waveform on little plotter and doing that quickly is hard.

Mew had a hard time with this. I think serial ploster actually works pretty good at that. So I'm pretty proud of that part.

Paul

Yeah, the only thing that threw me with the serial ports and I use Tio like you do is once serial plotster's running, you can't connect via Tio.

Tod

Yeah. Yeah, this is the terrible problem with serial ports is that only one program can talk to the serial port at a time. So you have to do the dance of disconnecting tio.

and then opening up your serial plotter, and then disconnecting the serial plotter, reopening T.O. If I was serious about this, CircuitPython does have the, if you're doing CircuitPython, CircuitPython has the ability to open up a second USB serial port, a second USB CDC channel. And so you can have your data on that one and then do the Ripple on the original one.

And then you don't have to worry about disconnecting. And so next time I'm going down any sort of serious path where I'm graphing data, I'll probably turn on the second serial port and use the serial plotter on that than on the Ripple because I agree. It's a real pain in the butt to sort of like dance between the two programs.

Paul

Yeah, it threw me at first and then it clicked. Oh, yeah, one serial port at a time. One serial port. Sorry.

Tod

Yeah, and it's really frustrating too because the Arduino serial plotter is I think one of the best serial plotters out there. But unfortunately, the Arduino IDEE is really greedy with the serial port because there's no explicit connect disconnect button because it's trying to be kind of friendly like oh once you've got the board configured if there's a serial port there I'm going to connect to it for you. It's like no.

Paul

I'll make sure to link to the download for serial plaster in the show notes as well.

Tod

Oh yeah, yeah. I've not updated it in a while but it should still work great. There's pre-built versions for Mac Windows and Linux and yeah, if anybody has any questions about it or has any suggestions on how to improve it, Let me know.

Paul

So you just opened a store on small run.net where you sell since running CircuitPython. It's been a couple of years since you've been on the show. Have you been working on any new hardware to add to the store in the near future?

Tod

Yes and no. Yes, I've been building many, many little random boards over the last couple of years. But no, I don't really have any new ones, I think, for the last time we talked. There's one that is really close.

And Cooper, who I think, has, has Cooper been on the show? A couple of times. Yeah, Cooper Dalrymple.

He's really good with doing synthesizer stuff. And he wrote a really nice library for this work in progress scent that I have that I'm calling Synthiota, which if you're watching this on video, you can see a little prototype of it. And it's a little synthesizer thing with 16 touch pads with LEDs and eight knobs and some sliders and a display and a good high quality stereo DAC output.

And it's driven by a PICO or PICO, too. That all sits inside of a little 3D printers enclosure. And it's pretty cool.

Cooper's library for it makes it really easy to get going. One of the things that's been sticking on me is that I've been working on trying to make some good synth engines that I like. Like one of the ones that I did a couple of months ago was this TB303 inspired one that hopefully might end up being used in an ATAFruit, used by ATAFruit at some point.

But the TV3 is like this very squelchy bass sound that was used a lot in acid, acid music, I guess, back in like the 90s and 2000s, sort of the burbally synthetized stuff. So trying to do that in synthio, the synth engine inside of CircuitPython was a bit of a fun challenge because of the troubles of making digital algorithms sound like analog circuits. Sure.

But yeah, so probably the next thing that will be on the stores, both Small Run and maybe Tendi, is the synth iota board, which I think is a lot of fun.

Paul

We'll have to keep an eye out for that. Tod, thanks so much for coming back on the show.

Tod

Oh, thanks for having me, man. It's always fun to talk CircuitPython stuff.

Paul

Thank you for listening to T CircuitPython show. You can learn more about Tod at his website, todbot.com, or listen to him on the bootloader podcast at the bootloader.net. For show notes and transcripts, visit www.CircuitPythonshow.com. Until next time, stay positive.
