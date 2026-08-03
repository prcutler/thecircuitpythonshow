---
date:
  created: 2022-10-03
title: "Episode 19 - Bradán Lane"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep019.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Bradán Lane, who started his career as a software developer before creating new teams in Singapore, China, and Dublin.

Bradán returned to the USA to study design and built a design team focused on user research and U.X design. In 2020, Bradán started designing and selling electronics for the maker and hacker communities. This episode is brought to you by.

by PCB Way. With over a decade of experience, PCB Way is one of the most experienced manufacturers in PCB prototyping and design. Whether you're an engineer, students, or hobbyist, PCB Way offers a simple and fast prototyping service, and it's cost effective at only $5 for 10 PCBs.

And check out PCBWay.com slash project where PCB Way helps makers and hobbyists collaborate on their designs and projects. Make your design a reality and check out PCBway.com for all your PCB needs. And they also now offer CNC machining and 3D printing services.

Visit PCBway.com for more information. Thanks to PCB Way for their sponsorship. Bradán, welcome to the show.

Bradán Lane

Hey, thank you. Glad to be here.

Paul

Tell me about how you first got into computers and electronics.

Bradán Lane

Computers and electronics date back a long time. Basically, it was PCs back in the days of C and assembly language with no graphics cards or any of that stuff. That's where I really started.

But then I jumped to team building, which was a joy for mine. Eventually, I sort of retrained as a, user experience designer and user researcher. And that's now influenced everything that I've done since then.

Paul

How so?

Bradán Lane

When I look at a project that I'm going to design, it's not just the electronics or not just the software. It's how is a user actually going to play with it, how they're going to feel with it?

I was walking this morning. I was trying to figure out how to answer a question like this. And I said, I want to make sure that they actually like it.

And like is a really hard word because we use it as a base for our definition. but there's some sort of a visceral experience. And so when I create something, I want somebody to be able to say, you know, I really like it.

I like the way it looks. I like the way it feels. I like the way I interact with it.

And all that came from user experience design and user research, listening to people about how they work with something, what they don't like about it, what they do like about it. See, even I use like for everything. What became obvious in that was the more they liked it, the more they interacted with it, the more they used it, and the more it became something that they wanted.

wanted to continue to interact with. And that's what I really want for my electronics.

Paul

Tell me about the first product you design that used CircuitPython, the JoyPad.

Bradán Lane

So the JoyPad was actually a branch from, I bought a piece of equipment for my lab to start doing my own assembly work. And it had a touchscreen, and the touchscreen was okay. But it really wasn't fast for doing a lot of the operations that I needed to do. You can kind of think of it like a CNC machine. You know, there's a lot of little simple. You have to be able to jog around.

and you've got to be able to type in small bits of information normally numbers. And so I said, well, I really want is I want a controller that's got a full keypad on it, plus a few extra keys. And, oh, by the way, it should have a little joystick that I can use as a mouse.

And since everybody who is building micropads put a little display on it, I did the same thing. And then I said, well, I want to make this available to other people. It needs to be easy to configure.

It needs to be easy to change, easy to use. C and firmware and Arduino ID made no sense. that's when I started seeing a lot of content, exceptional content, from Ata Fruit around CircuitPython.

And so I said, I want to try this. I want to play with it. And there are some really affordable boards to play with CircuitPython.

And so I got a couple of them and I started using it. And I went, this is amazing. Not only can I do everything I need for the Joypad, but almost anybody with, you know, a very small tutorial can do customization.

And so I really started to gravitate towards CircuitPython for anything that I was going to have end user customization, end user control of. If it needed to just do one thing, then writing my own firmware in a lower level language was great. But CircuitPython made it just so accessible to everybody.

What were some of the challenges in building the Joypad? So the Joypad has, like I said, a full keypad on it. So it's got 19 keys on it because the enter key is always bigger than all the rest.

but you can think of it as sort of 5x4 grid. And that's a lot of keys. And so one of the things that I needed to learn, not only CircuitPython, but Adafruit was great at this, was how do you electrically design a matrix keypad to use a minimum number of pins?

And then how do you get that to work with CircuitPython? And I'm going to say Adafruit over and over again because they have just done so much for the community. But they actually had a complete tutorial.

And I was able to take that tutorial and literally with a pegboard kind of wire up a bunch of buttons to create a matrix and then code it and make it work. What was great was probably about a month into the joypad design, they added a whole new library to the base code set for CircuitPython that made keypad arrays, A, very, very fast and efficient, and B, incredibly easy to code and change. And so when they added the keypad library as a core piece, it just made the joypad even that.

much easier for me to write and for other people to customize. And so the keypad library really simplified a lot of things. Probably the hardest thing for me to deal with on that was a low-cost joystick trackball kind of thing because for my application, I wanted something that didn't move around on my desk.

It needed to stay put, which meant that cursor control input had to be something that wasn't a mouse because I didn't want to be moving it around. A joystick that you'd find like on an Xbox or any sort of game controller seemed to be the right size and shape. The problem with it was its sensitivity is really, really bad. I ended up taking over one of the keys on the joy pad as sort of an accelerator so you can run it in faster slow mode.

And so in slow mode, it's very easy to get really accurate stuff. But right conveniently under one finger is sort of an acceleration button and then it moves really quickly. So you move it really quickly to one location, release that button and it moves slowly to the final destination. So there are little things like that on the joy pad that I had to figure out. But again, it was all pretty easy to do.

do, it's an analog input, and then I was able to go from there. How are users able to customize the Joypad? That was a question that I was trying to figure out for myself, was not only how are they going to do it, but then how are they going to learn how to do it.

I looked at the community of other people who had created CircuitPython-based products, and how did they document it? And I stumbled across Winterbloom and their big honking button, and they did such a great job at introducing the user to CircuitPython if they had absolutely no background, what tools to use and then they'd step them through a small example and then a little more complicated example and then they'd provide documentation and so for the joy pad I created a library of some common things that you'd want to do like put text on a little display or change in acceleration or something like that but then I use the example from winter bloom to write my own documentation that steps the user through so if you want to change you know a really simple one I want to change the color of the LEDs underneath the key caps. Okay, here's how you do it. And I want to read a button and change the value. So for instance, I read a button and I need to go through and say, okay, I want this button to do something completely different. So instead of an escape key, I want it to do something else. Well, I can show them an example of saying, okay, here's what you do, here's what it looks like right now. And I give them a clip of the existing code. And then I describe a change.

and then I give them a clip of the finished code, and they can very easily if they want copy and paste or they can type it in. But it walks them through the most basic changes first, so then they feel comfortable making more complicated changes.

Paul

Thea Flowers was the guest in the last episode, and one of the coolest things I think about Winterbloom is not only does she make her CircuitPython code all open source, but the website, the documentation, the hardware is open source. That's got to make it a lot easier for you to build upon.

Bradán Lane

Their work is stunning, and they do set the bar pretty high. I don't even attempt to rise to that level. But it is a great example, and it helps the rest of us who are trying to build and provide content to the community as a good example of where we start from and then sort of what works, what doesn't work, and then how to build it.

And with Thea, it's a vision of good, right? It's a lot of best practices there. Everything that they do is so open and so inviting and so careful to the community that we can all start.

I have to kind of follow it. But yeah, the fact that they open source so much made my life a much easier when I wanted to write my own documentation, my own level of how much information was the right level for a novice user. And I even admitted on the Joypad example, I give content for those who don't know how to code, but also those who don't want to learn how to code, but they still need to be able to customize the product.

Paul

Everybody loves lights and LEDs. Tell me about the Lumos Ring.

Bradán Lane

The Lumos Ring and the follow on the Loomis Stick actually can. came from a bit of a dare that was given. I was on a stream probably a year and a half ago.

And somewhere along the line, somebody came up with this challenge of, let's build a really big seven segment display. And so I took a little microcontroller and I took the pre-made strips of LEDs that you get with a little bit of stickyness on the back. And I stuck the LEDs to these big, long fiberglass poles that I got and put all the wires off the end. And then you could take seven of these long poles and you could lay them out of it.

on the floor and make a seven segment, you know, display out of it. And I 3D printed some corners and stuff. And this thing was nine feet tall, almost three meters tall.

And it worked. And then I went, that's not really very practical or useful. And when I also did that, I also said, well, I can make it practical because I'll make the dot and I'll make the dot really, really big.

And then if I put a lot of LEDs on the dot, I could turn it into a clock. Oh, okay, I'll do that. Well, again, now I've got this 14-inch, you know, circle.

with all these LEDs on it, and I really wanted something that would fit on my desk. At the time, I didn't have the skills to build the electronic part of it, but I eventually gradually got to the point where I could understand the process of how to lay out printed circuit boards. So I shrunk it down to about a four inch square, so the big circle of LEDs, each segment, there's 60 segments around their four LEDs each.

And there was a big gap in the middle, and I went, well, okay, if it's going to be on my desk, I might want more than just the time on it. So I put two five by seven LED matrices in the middle. So now you could put in a two-digit number, like the temperature or a graphic or something else.

Now I had this thing and I said, okay, I've built it for myself, but I really want people to be able to play with this thing. And so I came back to CircuitPython again because the goal here was I want the end user to be able to play with this thing. I want it to be easy and accessible for them.

So that was the Lumos Ring. It has 64 LED rows around. it. So you can just think of it as a big matrix or a big array that you've just wrapped into a circle.

So there's 240 LEDs. And then two five by sevens. There's another 70 LEDs. So this thing is just packed with LEDs. So then the 70 LEDs in the middle. And you can do all sorts of things.

They're addressable LEDs. So we call them neopixels, which means you can set any color you want, turn them off on different brightnesses. I wanted to create some demos for it. So I wrote a few different CircuitPython examples so that people could think of new ideas. Basically, I did the CircuitPython examples so that it would spur creativity for people who might get them. One of them is, of course, the clock. And I didn't know what to put on the two blocks in the middle. And so I did these little blinky eyes that look left and look right. And then I wanted a few other ones. So I did standard sort of countdown timer. And then I thought about it. And if you put big buttons on the top of it, it kind of reminds you of the chess clocks that you see for competition. So I created that little demo. And that's where I first started talking to Winterbloom about their documentation, because I wanted to give people examples. So I created a library to make timing games and puzzles and stuff easy with the product. But I wanted to be able to give enough control that somebody who was just starting out with something like CircuitPython could make their own games. So that's actually how the Lumos Ring came to be. Now, if we come back to the seven segment display, I have all those bars. Well, the bars are almost a meter long. And so I went out in my shop and I drilled a little piece of wood with some holes in it. And I stuck all the bars in it. And I went and said, ooh, I got seven bars. And so I said, what can I do with it? And I wanted to do, I thought I might mount it on the wall. So I created this really fun little animation of falling little sticks that bounce. And it gradually fills up and then it cascades and falls out. But then I realized, well, if it's seven and you rotate it horizontally, five by seven is a really common.

font for display type things. So I created a 5 by 7 font and open source that for people who want to use it for all sorts of projects and then said, okay, well, if it's 5 by 7 is a common math and you put a single one, single row between it, now I need 6, then about 40 LEDs lets me do two digits and a colon, two digits in a colon, two digits. Oh, okay, this is going to work out great.

So again, another clock. But then 5 by 7, and I did some performance enhancements on the design of the actual printed circuit board, but now things like scrolling text and all sorts of things become possible. Because I used a Wi-Fi-enabled microcontroller on the back of it, an ESP 32S2, you could do Internet of things or Internet connected things.

Like you could actually get tweets and scroll them on it, or you could get the weather and scroll it on it. And I've already been approached by one person who's gotten it and said, well, you know, I'm a DJ. Can you help me figure out how to do like a spectrum analyzer kind of design?

And that's where I'm working on right now.

Paul

My love of FFT and spectrograms is well documented.

Bradán Lane

Actually, again, you know, kind of looking at the broad community, I've been struggling a little bit with the performance of the spectrum analyzer. There's another maker out there that's been doing some LED-related projects and just launched a product that has fast-fass 4A transforms and a little spectrum analyzer kind of design in it. And they've open source everything as well, all their source. And so I had been talking to them before they had launched their product.

And he says, as soon as we launched the product, we're open sourcing everything. You'll be able to take a look. And so we've been going back and forth about, you know, how did you optimize it? How did you get it fast enough?

Again, they've open source all their stuff. And so now we're collaborating on how to do FFTs as fast as possible on some of these microcontrollers that don't have floating point units. So a lot of them don't these days.

Paul

Well, that's exciting to hear. And I just love seeing the power of open source and action like that.

Bradán Lane

It has made so many of my products so much easier to get from a concept and idea that I have to something that I can then make other people have available to them so they can start playing with it. They can start growing. And then they can take it in a whole new direction.

Paul

Well, we're almost out of time. But before we go, I have one final question for you. You're about to start a new project or prototype. Which microcontroller do you reach for?

Bradán Lane

Which microcontroller do I reach for? I can't choose just one, but I'll make it really quick. If I need Wi-Fi, because it's going to be connected somehow, then I almost always end up going for one of the ESP-32-based. And there's a couple of really, really affordable ones in the marketplace right now.

The ESP-32S2, and then it's follow on the ESP-32C3. With the C-3, they even add Bluetooth, which I'm really looking forward to taking advantage of. If I don't need Wi-Fi connectivity, often I will put a Raspberry Pi Pico on the back of my product.

And the Joypad uses the Raspberry Pi Pico. I like the Pico because it's available. And it runs CircuitPython very easily.

It's actually a dual core. It's got a lot of great functionality in it. For other projects that are completely self-contained but need to be really, really small, I still go back to the days of the microchip 8-bit microcontrollers.

Because the big thing that from a maker standpoint, the thing that I end up having to deal with, whether I'm using the RP 2040 that's in the PICO or an ESP 32 chip is, it requires a lot of other pieces and components around it. And with the microchip AVR set, you literally can add power and ground and your chip is running. And so when I need to be really, really small, that's where I go for that one.

Paul

Oh, what a great pick. Bradán, if people want to learn more about you or your products, where should they go.

Bradán Lane

The easiest thing to do is Bradánlane.com. I created that page and it's got links to everything else.

It's got links to Tindue, my small electronic puzzle games that I provide. It's the easiest way to find everything that I work on and that I publish. Thanks so much for being on the show.

Hey, it was great to be here. Thank you.

Paul

Thank you for listening to the CircuitPython Show. For show notes and transcripts, visit CircuitPythonshow.com. Help sponsor the show. Your financial support helps with the cost of recording, hosting, and transcriptions.

and check out my new show The Bootloader with my co-host, Tod Kurt. Search for The Bootloader in your favorite podcast app. Until next episode, stay positive.
