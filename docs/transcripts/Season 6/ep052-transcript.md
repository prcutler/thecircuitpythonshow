---
date:
  created: 2025-12-08
title: "Episode 52 - Dan Cogliano"
---

(soft music)

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I welcome Dan Cogliano. Dan is a developer whose interests include internet calendar standards, programming, retro tech and games, the internet of things, ventriloquism, and magic. Dan, welcome to the show.

Dan Cogliano

Thank you for having me. This is my first podcast, so it's a special time for me. (laughs)

Paul

How did you first get started with computers and electronics?

Dan Cogliano

Well, my first experience with a computer was in high school. I'm a little bit old, so the programming class they had in high school was Fortran. This was back in the '70s, and we had one computer throughout the whole county that would run Fortran programs, and it wasn't my school. What we'd have to do is we'd have to code our programs and send it to the school. They'd run the program and then they'd send it back. So it was like a three day turnaround. In fact, we didn't even have punch cards. We didn't even have money for punch card machines. So we had holo with cards with bubbles on them. So you would code using a Sharpie for Fortran statements and that sort of thing. So yeah, so it would take literally three days to put in a program and get your output back. So we had to double, triple check our code before we'd send it out, 'cause we won't see it for three days. So that was kind of my first step into programming. And then in college, I took some classes. I took a Pascal class. I took an assembly class, which was on the Motorola 6502, which is the chip that was used on the early Macintoshes and Apple IIs, I believe. And so I learned machine assembly language with that class, which I thought was really good. I had a programmable calculator. Those were getting very popular at the time. So I had an HP 41 calculator. So that was a good learning experience. And then after college, I got an Amiga computer and I started writing shareware programs on the Amiga. So then I got into C and C++. And then later I started getting into Arduino. And funny story, I didn't get into Arduino 'cause I didn't know if I wanted to learn another language and I realized, oh, that's C. (laughs) I didn't, it took me like a year, I think, before I realized, oh, that Arduino is C and C++. So that's kind of like how I got started.

Paul

How did you discover CircuitPython?

Dan Cogliano

Well, CircuitPython, I got into Arduino And a lot of the processors that worked with Arduino also worked with CircuitPython. I dabbled in that and one of my first projects was something called the EasyMake Oven, which it's a reflow oven. And I was looking at reflow ovens at the time and we had a lot of Chinese manufacturers And we had all these reviews and they were using paper insulation and they were not very high quality. I thought, "Well, what if I made my own?" And I kind of looked around. I looked at the Adafruit store and I said, "Hey, they've got all the parts I need except for the toaster oven." I basically converted a toaster oven into a reflow oven. So I took the toaster oven, Pi Portal, which was an Adafruit product that had just come out. I had a thermocouple, which is kind of like measures the temperature inside the toaster oven. Then there was a switch, basically a, looked like a power strip, but you can program this power strip to turn on and off. And I didn't want to do any kind of high voltage wiring. So I thought, hey, I can just regulate this by just programmatically turning the toaster oven on and off. And I can graph it, you know, the temperature versus time. And I, that's how I came up with the the EasyMake oven. So it's actually one of my favorite projects and I still use it.

Paul

I love the name of it. And that was my next question was actually if you were still using it, so it's good to hear that it's still around. Yeah, yeah. I mean, and for people who don't

Dan Cogliano

know what a reflow oven is, it's basically, you know, you could do through-hole soldering, but if you want to get into PCBs and smaller components, then that's where you would use a a reflow oven. So yeah, I have some things that have some small parts that the reflow oven is ideal for making components like that.

Paul

You've created the Z-Machine, which can run classic Zork games. How did that first start for you?

Dan Cogliano

It started out with Arduino. I wrote a, or I ported a Z-Machine to Arduino on an Adafruit itsy-bitsy device, which is really like the size of your thumb. And I ported that using Arduino NC. And I thought at the time, I'd like to do that in CircuitPython too at some point. But back then, the hardware, you basically needed a screen, enough memory. And so what I did was, I kind of put that on the side and then when I saw the fruit jam come out, I said, "Oh, this would be perfect for that." It's got the keyboard, it's got the screen, it's got memory, enough memory, you can save files to it. So it had basically all the parts that I needed for the Z machine. So I guess the only question I had was how the performance would be, since you've got an interpreted language running an interpreted computer. So I thought, well, I want to go with this and see how far I get with it. And that's kind of how it came about. And I think the performance turned out great. I was really impressed with the performance.

Paul

What are some of the features of CPZMachine? How does someone get started with it?

Dan Cogliano

Well, we have, you can run it either standalone or there's something called which is a way you can run pre-packaged CircuitPython games and applications. So you can run it either way. So the performance was one thing I was looking at, and that turned out really nice. The save game, there's an issue with CircuitPython where you have one operating system that can read and write, and the other operating system can only do read-only. So the nice thing about CircuitPython version 10 is that they have a saves or cpsaves folder which allows you to have the CircuitPython operating system read and write those files in that saves folder while the host computer has read and write access so you can copy files and you can copy the CircuitPython libraries, you know, the CPZ machine, the game files, so you can do all that and still have rewrite access for the save games. Save is really important when you're playing Zork and Z machine games, because you can die and you lose what you have. So that was one nice thing that came out with CircuitPython 10 recently, so that was a big help too.

Paul

Yeah, that CP saves partition is pretty neat for creating games now. You're not the first one to take advantage of that. Mm-hmm. Were there any challenges in creating the CPZ machine?

Dan Cogliano

Yeah, well, it's an interpreted, almost like assembly language. So I kind of resurrected my skills from college days, assembly language, and basically, there's a bunch of machine codes that you have to emulate and then you have to debug them. And so the debugging part is the hard part where you have to step through and say, you know, is this what it's supposed to be doing? So that took the most amount of time, was writing the machine codes and debugging them. And so what I did was, you know, since ZMachine's been around forever, there's other implementations of it. So I took a ZMachine that someone else wrote in C, and I put some debug statements so I could follow that version and compare it to the version I was writing and see when they diverged and say, "Oh, you know what? Why is my program diverging at this point? I'll go back to the reference C machine that I'm working with." And I said, "Oh, okay. I forgot something or whatever." So, yeah. So, that was very helpful.

Paul

So, for those that might be a little younger than us, can you take a minute to explain what game Zork is?

Dan Cogliano

The Zork came out in the '80s. It was developed by staff and students at MIT. It came off of a, I believe it was a PDP-11 computer, and they decided to commercialize it. Back in the '80s, you know, the computers were not very powerful, but there was a lot of different computers out there, they all ran different software. And so they thought, well, we're going to try to write something that will work on all these devices. And they decided to split the program in two. They took one part of it, which was the story, basically the data that had all the text and the logic. That was one part of it. And that part could run on any of the computers that were out there in the day. only part they had to write was the machine codes for that particular operating system. So that way they were able to maximize their stories and the logic there and just have to write what they call the Z machine, which is the program that runs the Zork game. And they came out with other games too, not just Zork, but they have Zork 2, Zork 3, and there's probably several dozen ZMachine type games that you could run on it.

Paul

And the CPZMachine supports all those games?

Dan Cogliano

It supports version 3, which was the first version that came out. I'm probably going to look at supporting other versions in the future, but I think the majority of them are version 3, so you get most of them with that. And I'm also working on a learn guide for the CPC machine and Zwork and all that. So hopefully that'll be out by the time this airs.

Paul

Yeah, I'll make sure that if it is, I'll link to it in the show notes as well. Tell me about the latest game you've been working on, a Moonlander type game.

Dan Cogliano

Yeah, so once I finished with the Z-Machine, I thought, well, now I think get something a little bit more graphical. Zwork and Z-Machine's all text-based, there's no graphics. In fact, the only graphics is I have a blinking cursor. It's a little square that I turn on and off. So that was that was the extent of my graphics with the Z machine. But I thought I want to try to get a little more fancy. And one of the games I liked when I was in college was this lunar lander game where you take the lunar module and you try to land it on the moon. And I thought, well, I'm going to make a version of that and see what I can do in Circuit Python. So I've been working on that. It's basically a physics-based game where you're trying to land without crashing on the moon, and so you have to deal with gravity thrust from the rocket angles. And you want to land vertically, you don't want to land on your side, which is happening on the moon recently. So I thought, "Yeah, this will be something nice to do." And at some point in the near future.

Paul

What's your experience been working with graphics and display IO? Has it been a challenge?

Dan Cogliano

And CircuitPython, it's great for a lot of things, but sometimes, heavy graphics, it's particularly real-time graphics, it's hard to do. So sometimes I have to change my mind on what I wanna do. Like I originally wanted to have a scrolling background with my Lunar Lander scrolling, looking at the lunar surface. And I thought, well, I took a look at trying that. And I was using a high resolution, which is also what I wanted to do. And so higher resolution means, you know, you got more bits to work with and it slows things down. So the trade-off was, you know, either lower resolution and higher, you know, scrolling or higher resolution. And then, so I kind of do is I just page, I go from one page to the next. I don't do the scrolling. So that was fine. I think it works great, and you just get a slight delay when you go from one screen to the next.

Paul

If anyone wants to learn more about you and your work, where should they go?

Dan Cogliano

Well, I'm on Blue Sky at Cogliano. My last name's C-O-G-L-I-A-N-O. And I do have some Learn Guides up there on the Adafruit site, so you can check out some other Learn Guides. I've got a few other CircuitPython learn guides there. I have one where I, related to the EasyMakeOven, I use the PyPortal. And I didn't, in that case, I did not use the feature where you'd be able to get to the internet, 'cause I didn't need the internet for that. But I do have another project where I pull artwork down from the Museum of Art in Cleveland. So it kind of cycles through images there.

Paul

I'll make sure to link to those in the show notes as well. Last question I ask each guest, you're starting a new project or prototype, which board do you reach for?

Dan Cogliano

Well, right now it's the Fruit Jam. I'm really excited about the Fruit Jam. I think there's a lot of potential there, and I've seen some of the emulators that have come out. There's the Mac emulator, which is something I want to try. It's not just CircuitPython or Arduino, but you know, you have these emulators. So it's got the gamut of options there for you. I'll probably be sticking with CircuitPython, but I do want to try some of these emulators.

Paul

Yeah, I agree. There's a new 286 emulator that just came out, and Apple II, Sega Genesis. It's just crazy how much support is coming out for the Fruit Jam. Dan, thanks so much for coming on the show.

Dan Cogliano

Oh, I appreciate it. I love being here and I appreciate getting invited. Thank you.
