---
date:
  created: 2026-07-27
title: "Episode 61 - Michael Czeiszperger"
---

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I welcome Michael Czeiszperger.

Michael, who described himself in a bio he wrote in 1991, as an engineer who dabbles in writing, musical composition, and computer graphics, skillfully avoiding the mastery of any one field. 35 years later, the list has only grown. Real-time synthesizer prototypes at Yamaha R&D, where he demoed the entire lab's work for Yamaha's president, Solaris Audio Libraries at Sun Microsystems, and since 1998, his own company, Web Performance Incorporated, building load testing tools used by the U.S. Census, Statistics Canada, and the New York Marathon, most recently shipping agentic AI systems into a 25-year-old Enterprise Java platform.

Michael just released ScrollKit, which exists because he wanted LED signs showing live theme park wait times, and found that most CircuitPython Matrix libraries get you a scrolling Hello World and stop. It handles everything after that. Over-the-air updates to boards in the field, fault-tolerant data refresh, transitions and effects, and a built-in web server, all running at once on boards like the Matrix Portal S3, plus a pixel-accurate desktop simulator, so debugging doesn't have to happen on hardware. Michael, welcome to the show.

Michael Czeiszperger

Hey, how's it going?

Paul

How did you first get started with computers and electronics?

Michael Czeiszperger

If you want to talk about electronics, my dad was a real big believer in the value of hard work and other people. And so he had a buddy who had a TV repair shop and it sent me out to Apprentice there. Look, I was 14. And so they put me to work first sweeping floors and then soldering used parts off of old TVs to go in the bins to be used. And so I thought that was the coolest thing.

Michael Czeiszperger

how does it all work? You know, and the other thing I thought was, I do not want to repair TVs. I want to build stereos.

Michael Czeiszperger

That sounds way cooler.

Paul

How did you discover CircuitPython?

Michael Czeiszperger

I discovered CircuitPython because I've been following Adafruit since it started.

Michael Czeiszperger

And so I just think it's a cool company. I like the way they're run. And CircuitPython happened to be a good way to learn how to use our hardware.

I've already done C++ programming on ESP 32s, and I thought, I know how to do that. But a buddy of mine says, you have to learn Python. And so what a better way to learn Python than to make LED screens light up.

Paul

Speaking of LED screens, you recently released ScrollKit for CircuitPython. Tell me about ScrollKit.

Michael Czeiszperger

I wanted to learn Python, but I also wanted to make a product, because I'm kind of like an entrepreneur or product engineer. And the product I would make was kind of dumb. And that is a box, which would tell me what the wait times were at theme parks, because I'm a theme park net.

And as a professional programmer, I sat down and all the different bits and pieces that you needed to put together, I'll hold it to do by hand. It's like, why don't any of these libraries exist? This is a, you know, I don't mind writing them.

But, I mean, it should be a few lines of code that somebody else wrote, not me. I mean, all the different pieces. I was looking at page after page of like gobbly gook of trying to get the boards configured.

And I thought, you know, somebody else could be saved a lot of time if I just pulled out all the commonalities and made it into a library. And so I happened to be on the API team. It's on microsystems back in the day for audio.

So I had like an I for, I'm just a real stickler about it should be as simple as possible and extensible. So that I just love looking at a program. It's like line one, set everything up, line two, run the program.

You know, it should be logical and easy for even non-programmers to use.

Paul

This is version three. How does it differ from the first two versions? What have you learned along the way?

Michael Czeiszperger

Well, I learned a lot. As you can imagine, version 1.0 actually shipped and people like paid me to shift these boxes out. And it was pretty much crap.

I mean, I had tested it at home, but these, you know, people would run it on spotty Wi-Fi networks and it'd be up for six months and they were naive users. And so if the box happened to go blank for 10 seconds because the data feed locked up, they would panic and send an email or unplug the box and then it hose it. I rewrote the thing to version two and I thought I was going to fix all those things.

And it was more solid then. It was better. it was just completely hand-coded.

And then about the same time, AI coding came along. And I thought, you know, I would rather risk learning how to program with AI on this than at work. The first time, I said, all right, refactor this into a library, separated it.

So I gave it instructions. And I let it run overnight, and it came back the next day. And it was literally 20,000 lines of gobbly gook.

I mean, it was just horrible. So it was a long process to figure out, all right, how do I, as a former engineering manager, tell my AI team how to do what I needed to do, which is to create a professional-looking library.

Paul

So tell me a little bit more about ScrollKit. How does it work?

Michael Czeiszperger

You know, it's a Python library, but when you make a, there's a big difference between just running a little demo app on your CircuitPython device. and coming out with a product. And so one of the first things that happens is when you give a person a box, it has to connect to the Internet.

And all of the CircuitPython documentation that says, first mount your drive and then edit the file with your Wi-Fi password. And no, people are not going to do that that have paid for a product. They just aren't going to do that.

And so the first thing is there were some regular Python scripts, but I wrote it from scratch that when the box comes up, it throws an actual web server up with instructions for the user. So across the device, it scrolls, log into here, and then it allows you connect your internet. So it's polished.

It's basically product polish. So what happens then? The next thing that happens is, what if the user wants to modify it?

You don't want to write an app for that. And then they have to download an app. So then the web server that's running on the box automatically picks up all of your settings you specified for app and shows them in a nice GUI should use her and go and change parameters for all speed colors.

Whatever parameters you want, it automatically throws it up. You just define what your parameters are and the GUI just takes care of it. Now, if you want to do something complicated, you could write your own GUI to.

But the philosophy here is what 99% of people are going to be doing is handled in just the simplest way possible.

Paul

Now, when you say box, what hardware have you targeted? I believe it's an S3 Matrix portal, and is it Hub 75 displays?

Michael Czeiszperger

Yeah, yes. That's pretty much the first case. I have a list of other hardware sitting.

I might ask right now that I'm going to be adding just to add something else. I really like that device, the S3. It's so, I mean, it's so easy to put together. It's just a couple of wires. You plug it into a box. The thing runs. There's nothing to solder. I mean, it's it's dead simple for a hobbyist for me.

and I actually went and cadded up a really nice enclosure for it too. So the whole thing just mounts. It's got a holes in the right place from the side.

You just plug in your USB power kit, power cable, and it just works.

Paul

I've got a project that uses two 64 by 32s together with a nice 3D printed cases. We might have to trade designs at some point here.

Michael Czeiszperger

Oh, yeah. Well, that's the next step. Once you get one, then you went two, right? That's right.

Paul

How do over-the-air updates work?

Michael Czeiszperger

Over-the-air updates, basically it looks for a live branch on a GitHub feed. So you can do your development, and then when you're ready for a ship, you can tag it with a release number, push it to the live branch, and then all the boxes have a little button at the bottom under GUI, and you can say check for updates. What I typically do is I have a list of people who are using it, and then I just send them an email when there's something with the description and they can upgrade. great or not. Sure. I just remember, we haven't talked about graphics.

Paul

Right.
That was the next question. Perfect timing. Yeah, we haven't talked about graphics.

Michael Czeiszperger

So one of the, the first thing that really made me excited about doing this was that, I don't know if you had the Aterfruit demo where they have a sort of like a flocking thing. I've seen it. It was in C++.

Yeah. All right. So first thing I tried to do is write that in Python.

Oh, my God. It did do was just glacial. I mean, it was just one thing at a time.

And then I looked into it. I realized that some of the calls, graphic calls, and circuit bython are really fast because they're in C and some are. So what I actually did was wrote a program that went through and timed each of the graphics calls and made a table.

All right, which ones are fast and which ones are slow. So all right, now I know which ones to avoid. And then I said, OK, what higher level constructs do I really want to do to put together?

other animation to make things walk and make things fly and just came up with a nice, very simple little kit in order to put sprites in there that all used the fast thing. So the first thing I did was try to redo that flocking algorithm and it worked this time. By using the fast calls, I've sort of timed it so I could create a flock of about 20 separate birds. That seems to be optimal for the S3. Once you get over that, then it slows down.

Paul

That's still pretty impressive, that you can get 20 other birds animating at the same time.

Michael Czeiszperger

On CircuitPython, to me, the thing is as slow as on that hardware, it's kind of like writing and basic for old Commodore 64.

Paul

And I think that's part of the appeal of learning CircuitPython, and it's got some of that back-to-basics feel to it.

Michael Czeiszperger

Well, you know, I think you get some of the best creativity when you're restricted. If you had a limited compute power, what would the fun of that be?

Paul

That's right. It's all about those constraints.

Michael Czeiszperger

Yeah.

Paul

So you mentioned the speed is one of the challenges. Were there any other challenges you had to overcome?

Michael Czeiszperger

CircuitPython is different because they rewrote. They have a different HTTP stack than regular Python. They have a different graphic stack.

And so trying to get everything running at the same time in the box was challenging because the HTTP is synchronous. But in order to get simultaneous scrolling across the screen and the web server running and the data being updated simultaneously, the background would block every time there's HTTP call. And so I put a lot of effort down the drain and trying to make that I-O asynchronous that just never panned out.

So I decided to work around it by putting up a screen that says, I'm updating now, don't unplug. So the end result of that architecture now is that I can have multiple graphics processes, is running and egg secrecy. So at the same time as there's a message scrolling across the screen, I can have an animated swarm, form the wait time for the ride.

It's so cool. It just sort of like call comes in from everywhere and swirls around and then makes the number. And I think when you have a simple little box like that, it's those fun little animations that make it interesting, that change every time.

Paul

I agree. You mentioned that you wanted to start the project off by learning a little bit more about how AI might be able to help. I believe you used Claude. How did Claude help you?

Michael Czeiszperger

Yeah, well, I came back. I left this project sit for a year, and I learned how to use AI in a corporate setting, doing production work. And so I brought that skill set.

Michael Czeiszperger

I thought, you know, what would be fun? I want to have little animations for each ride. There's a ride at Magic Kingdom with the Big Thunder Mountain, and there's this goat that's sort of the mascot, and the goat sort of shakes his head up and down with dynamite's mouth.

I said, I want that, but I want it for every ride. So I thought, let's try the new Fable. The big model right now that came out as Fable.

I thought, you know, I'm going to create a list of every ride that are my favorites and then put out a text description of the animation that I want. And then I'll just let Fable chew on that overnight. So I came back and like some of them were really cool and some of them were blobs.

And so when I realized that I can't tell it to make a guitar, I have to describe what a guitar looks like. And so that was a process. It took like three different revisions.

And then every time it was says, you know, I don't want the head to bob up and down. I want it to rotate. So then every time that happened, I would update ScrollKit.

So now you can have little bitmaps that rotate. And then I did a walking mechanism. And I did a bird flies and flaps.

And then I did vehicles where you can have a road and things walking over the road where the road stays the same and the people walk. So basically, I just iteratively went through each of the rides and thought, all right, what would that be cool? Had the AI crate that for me, iterated on it, and then moved all the reusable parts of the code over to the library.

Paul

Is there the ability for users to fork your repo and actually give prompts to their AI? to build animations for the LED matrix themselves?

Michael Czeiszperger

Yeah, that's the whole point, is that built into this whole thing is and instructions for the AI of your choice of how to use this, where you could go plug in some thing in your head of how you want it to look visually and it will try to create an animation that does that. So I think that's really fun. You can look at the code yourself and it's just so cute to see these blocky little things go across the screen.

Paul

It might be a great way to introduce someone to CircuitPython, too. Put them in front of it and get them interested in giving the prompts, and then over time they might be interested in going under the hood and learning how it actually works.

Michael Czeiszperger

That's the idea. People can use as little or as much coding themselves as they want. I think the end result would be if somebody says, You know, I want to do an asteroid game or something silly. And then they end up having to write code to do that.

Paul

So you wrote a simulator that works with Pye game. How does that work?

Michael Czeiszperger

Yes. As you know, professional programmers, we like debuggers. I love debuggers.

There's nothing faster with a bug to go stick at a breakpoint and then look at all your parameters, see all your values. But when it's running our hardware, I don't know of a debugger that runs on that. Maybe there's one now, but when I started the project, there wasn't a debugger that would tell you what was going on the hardware.

And so it was always putting these output statements. And I'm learning a new language. You know, it was so tedious.

So I thought, why isn't there a simulator? This is a simulator for everything else. I Google and I found some very complicated things online and I couldn't get them to work.

I thought, you know, let me just see what Opus is going to do with this. So I expect out what a simulator would work. It took me like several days to iterate on it.

And unbelievable, you can hold up a box with the hardware right next to the simulator, same speed, everything. So the simulator actually uses those timings I created for each of the calls. So it knows exactly how long it takes on the S3 to execute each of the calls.

So it knows how to do the exact same speed and color. It knows bitmaps. It looks exactly like the hardware.

Oh, that's great. But you can debug it. You could throw it in the debugger and you know what's going on.

So that, to me, that was like really fast.

Paul

So you mentioned that you're really into theme parks and you have another project on GitHub called theme park weights, where you've used an API, I believe, to display all the wait times on these devices. Is that what people are using out in the field that are purchasing this from you, that they're also into theme parks and they want to understand what the wait times are out at the different theme parks around the world?

Michael Czeiszperger

That's exactly it. So the use case here is that people have scheduled a big vacation and it's six months out and they want to get their kids excited. So there's a countdown on it.

And so they can stick that in the kitchen and every morning the kids can say, all right, here's what's going on at Disney today. Look at that cute animation. You know, isn't that going to be great?

Look, we've got only 93 more days.

Paul

Well, that's great. Build that anticipation up.

Michael Czeiszperger

Yes. And, of course, I just like having it in my office. I think my wife's tired of it by now, but I'm still in my office.

Paul

What's next for ScrollKit?

Michael Czeiszperger

I was just thinking about that. And I was thinking I really want to make the animation more complicated. Because right now it can do simple little things, but I thought it would be fun to try to do simple games on it. Like turn it upside down and do Tetris or asteroids or a scroller game.

Paul

If people want to learn more about ScrollKit or your work, where should they go?

Michael Czeiszperger

Well, ScrollKit is at scrollkit.dev. And it's got a whole bunch of sample animations. Every single effect you can do has sample code and then an animated gift showing what it should look like.

So it's fun. You just look at it. My personal work is just CZEI.org.

Paul

Last question I ask each guest. You're starting a new project or prototype. Which board do you reach for?

Michael Czeiszperger

Which board do I reach for? I have been doing Unix since BSD. And so Raspberry Pis are just like, they're so capable.

And I've, you know, you can SSH-in into them. So to me, that's comfort zone, right? And so trying to use the S3 was me trying to stop using the same ball.

Paul

Michael, thanks so much for coming on the show.

Michael Czeiszperger

Hey, thank you. Appreciate it.

Paul
Thank you for listening to The CircuitPython Show. For show notes and transcript, visit www.circuitpythonshow.com. Until next time, stay positive.
