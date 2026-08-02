---
date:
  created: 2025-04-21
title: "Episode 44 - Designing Games for CircuitPython with Tim \"foamyguy\" Cocks"
---

## Show Notes

[Show notes available here.](../../episodes/Season 5/ep044.md)

## Transcript

Paul

Welcome to T CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Tim Cocks, who is known in the Adafruit community as FoamyGuy.

Tim is sponsored by Adafruit to work on CircuitPython, and you can catch Tim's live streams on Saturday mornings at 11 a.m. Eastern. Tim, welcome to the show.

Tim

Hey, Paul. Nice to be here.

Paul

How did you first get started with computers and electronics?

Tim

Yeah, great question. So I had a family computer when I was young. that was really my first start to computers generally.

I don't remember exactly what age I was, but the things that stand out to me and my memory were getting involved in programming, which started for me in middle school. I had like a sort of tech class where we would get in groups and then go around and there were different stations and you would do a couple, maybe one or two weeks at each station. And one of them, I think it was like programming one of the robotic arms, but it also included a little bit of learning basics.

programming. And I got super excited about that. And then sometimes shortly after that, I ended up over at my aunt and uncle's house. And they're both software developers by trade. They worked on kind of airline industry stuff for as far back as I can remember. And they gave me a floppy disc, which had MS. DOS and Q Basic on it. And I was able to take that home and play with QBasic at home, which was kind of really my launch point into programming more generally.

I made all sorts of stuff with QBASIC, mostly just kind of visual paint pretty colors and do fun stuff like that, but a couple of basic games and a couple of basic text input and output type stuff. So yeah, that's what I really credit as my first kind of leaping into programming and getting the bugs, so to speak. Sure.

Paul

How did you discover CircuitPython?

Tim

So for CircuitPython for me it came out of a project at work my work was around digital signage and at one point we wanted to make a sort of specialty display setup that would play different videos on a screen whenever various different things happened in our case it was like smartphones that were on display and you would kind of like pick it up off of the shelf with its little retractor thing and we wanted that to trigger a video And so we had this whole software system that handled the videos and everything, but we needed a way to get the trigger from the actual pulling of the little phone holder deal into the computer that was playing the videos.

And one of the people that I worked with was aware of CircuitPython, and this was around the era of the Trinket M0, which was a very cheap device that supported CircuitPython, and we ended up using that little device, the partner that I worked with who knew of it, designed a little PCB for us to just stick those trinkets on top of it had our four outputs so we could hook it up to the four different pedestals that would that would trigger the different videos and then we could send those signals in to our player. So that was my first introduction to CircuitPython was using those and we built a handful of those. I think we made around a hundred or so of those when we first did it and it ended up being that the order was large enough like Adafruit, as I'm sure you know, when you make an order that's large enough, they tend to have some kind of freebies that they throw in. The freebie that we ended up getting was a circuit playground express, which we didn't have otherwise a use for. And I ended up taking that home and kind of really diving in and discovering a lot more of what CircuitPython could do beyond just the simple, you know, read the switch and send the keyboard, which is what we were doing for that project.

But yeah, I kind of fell in love with it with the CPX because it's so visual and fun to play with the LEDs and the speaker and all kinds of stuff that it can do. So that was my that was my my first entry really into CircuitPython.

Paul

Yeah, the Circuit Playground Express was my first board that I ever bought from Ata Fruit as well, so I share that love for that board with you. Nice. You've created a number of games, including some live during CircuitPython Day and on your live streams. Where do you get inspiration for the games you've created?

Tim

Yeah, I think my inspiration largely comes from just games that I have played in my life. I've been an avid gamer my whole life. I got a Game Boy when I was really young.

I had an NES, super, an Intent. Nintendo 64. That's kind of around the era where I stopped, so I didn't really continue on to the PlayStation 3 and the Xboxes and all the modern stuff, but I kind of transitioned over to PC games, and games are still a relatively big part of my life.

So my inspiration comes a lot from the games that I've played, in particular the games I make for CircuitPython. A lot of them are inspired by the old handheld stuff, the Game Boys and the other little handheld games. Like back in my childhood, there were just loads and loads of little handheld games that you could buy and play, and it was a purpose-built one.

I remember I had, I think it was basketball or something like that, but I played the heck out of that thing. And it was just very basic. It only played the one game.

And I think those things are a big part of my inspiration for CircuitPython because they remind me the form factor of them, the way the graphics work, and the types of things that they can do and kind of how powerful they are in terms of games and graphics and stuff like that remind me a lot of CircuitPython. And so lots of my ideas come from there. But there are cases where outside influences come in.

So working for Adafruit, PT is always keeping up with the latest stuff that's going viral on socials and everywhere else. And so he's always seeing the latest cool projects that are popping up and he'll send ideas my way for like, hey, you know, this thing is kind of getting popular on Blue Sky or Macedon or whatever. And it's this little simple version of this game.

Maybe we can make a CircuitPython version of that. And so that's where some of it comes from as well is just ideas from out in the world that's like, hey, can we take this idea and get it into CircuitPython, which I find a lot is a lot of fun for me as well to do that kind of work. So it works out nicely.

Paul

What kind of planning do you do when developing a game for CircuitPython?

Tim

Yeah, planning, I will say generally, for my software development, I am not huge on planning. I didn't go through formal training and learn all of the different methodologies. for planning out software and stuff.

And I've always worked on very small teams, worked by myself for a very long time, only more recently even got a team at all, and it's always been very small. So I think that I am not the best. I will freely admit that I don't think that I am the best at planning, but in terms of the games that I make and the planning that does go into them, there's kind of a couple of main ways that it sort of reveals itself.

One of them is just inside my head thinking about it, you know, in the background as I go throughout my day, I've got this idea for I want to do this or I want to do this, want to do that. And those just get kind of filed away in my brain. Sometimes I will scratch a few of them down just if I don't think I'm going to remember it or if I really want to remember how a couple of ideas fit together in a specific way. I'll usually just throw those down into a text file or something like that that's alongside the code or assets or anything else that I have started already for the game.

And then the other way that I plan is with software. So if I have an idea for how I I want to show different types of graphics or how I want different menus to work or how I want to be able to jump between the game and the different menus. All of that stuff is kind of hyper-specific, but it tends to be the kind of thing that I kick around most when I do kind of do my planning.

And so that sort of stuff for me is a lot of proof of concept. So I will write a script that does one little tiny piece, you know, that renders this sprite or brings together a couple of sprites and does this one little proof of concept. And those scripts, even though they all kind of just do their one thing and that's it. Those kind of serve as a good chunk of my planning because I can go back through them and eventually copy paste out of them, but also look back through the history of like, here's where I tried this and this and this and it didn't work for that reason. And maybe I want to go back to it and tweak it somehow. Maybe I have a new way I can take it and maybe it will work a bit better or what have you. So yeah, a lot of my thinking is in code in scripts and stuff like that, just because that's kind of where I'm basically most natural, I guess, with my thoughts.

Paul

What challenges do you run into designing a game for a microcontroller? I have to believe that there's a number of constraints because they're just such small microcomputers.

Tim

Definitely, yeah. So the constraints, you know, particularly the amount of storage space you have, especially if you want fancy graphics and stuff like that, you tend to eat it up fairly quickly. Although we're getting to the point where we've got a couple of megs on some of the devices now, which is like small by computer standards, but pretty big by microcontroller standards.

And so it's cool to see some of those where we don't worry as. much about that kind of stuff. So the amount of space for your actual assets and your code and stuff like that, the amount of RAM that you can actually, you know, store graphics and code and things in during runtime.

And then just the CPU itself, although, you know, all three of those, as the years go on, I've kind of been involved in CircuitPython, you know, moderately to heavily for probably getting close to five years now. So it's actually been a little while. And steadily you can kind of see year after year the new microcontrollers coming.

you're bigger RAM, faster, more storage. And so it's kind of like going through that same cycle that computers did. I will say, though, the constraints that CircuitPython and microcontrollers in general bring are one of the things I find super fascinating, super interesting, and just like a fun challenge.

It's a fun puzzle for me. Not necessarily going super duper deep. I have no aspirations for like writing assembly or anything full time.

But working within those constraints is kind of fun because the entire sort of history of my software development career has all been in environments where resources are essentially infinite. I did a lot of work on mobile devices, which were a little bit constrained compared to PCs when they first came out, especially I worked on Android stuff when it first came out. And at that time, the phones weren't quite as powerful, but still effectively infinite for anything I was doing with them. I wasn't doing anything hardcore. I branched into Python and web development and stuff.

And it's the same deal there where it's like anything I want to do just uses a tiny fraction of the computer, a tiny fraction of the RAM. It doesn't really matter. I can just write my program and not think about it.

Whereas coming into the microcontroller world, you can take that approach for a little while, just write your program and don't think about it. But in particular for games, or if you've got lots of assets or something like that, you will end up running into the RAM limit. And then you can kind of start coming up with different ways of like how can I combine some of my spreads?

together or how can I, you know, maybe offload some of the sprites to an SD card and only load them whenever I actually need them, like load them and display them and then get rid of them and throw them away when they're not in use, stuff like that. So those kind of constraints are actually pretty interesting to me as just problems to solve. And that's one of the things that I think has hooked me with CircuitPython. I'll give you a quick example from one of the games that I have been working on recently. One of the ways that I kind of got worked around these constraints, so to speak, was it was with RAM and it was with the amount of sprites that I wanted to be able to use.

The newest game that I'm working on is kind of a jewelry crafting game. And as part of this game, we've got various different items, which you can then craft together into final little bits of jewelry that add stats and do all kinds of other different stuff. And so there's a couple of different types of metal and there's a couple of different types of gemstones.

And then the goal is to be able to combine them to make a couple of different types of finished jewelry. And quickly the number of permutations of the final items just multiplies out. And so it explodes on you really fast.

And I started going down the road of like, well, you know, I'm on a ESP 32 S3. I've got a fair bit of RAM to work with. So maybe I'll just throw a giant sprite sheet and it'll be okay.

I started measuring that out with one of those proof of concepts like I was talking about before. And I was realizing even with just a small subset of what I wanted to end up with, finally, I was still already taking a noticeable chunk out of the RAM. And so the way that I solved it in this case was figured out how to kind of remove the color, remove the different gemstones from the equation by exporting only one of my sprites in a specific color and then also exporting just the palette information, just the actual list of colors that I need to represent visually the other gemstones.

And then at runtime, inside the CircuitPython code, I can load the one sprite, I can get its palette, and then I can manipulate just that one little sequence of colors and kind of substitute out reds for blues or greens or what have you. And that allows me to really drastically reduce the number of sprites that I'll need in the end. And I kind of wrote some helper code that makes it so I don't have to deal with the nitty-gritty details of all of that.

I can kind of just tell it like display the red, you know, gold one and it will do it without too much hassle. So that's one example of one of those types of challenges that I solved recently that was a lot of fun. for me.

Paul

Let's chat about some of your current projects and games. What are they and were there any challenges in building them? Let's start with the 1D Chomper.

Tim

Yeah, 1D Chomper is a fun one. That one was, that was the first of the ones that I kind of built a, what I kind of lovingly call Cardboard arcade or Cardbacade, if you want to get fun with it, where I built it into a little cardboard box because I like that sort of physical kind of not quite arcade. It's not a full stand or anything like that, but it's just kind of sit on the countertop and you can play it. I like that physical nature of it. And I really like the idea of stuffing it into a cardboard box as well, because it's really low barrier to entry. Pretty much everyone this day and age has got a cardboard box line around, and you can cut it up and bold it to whatever you need. So it's a fun medium to build a project into. But yeah, the 1D chopper, 1D chopper was built into that. It uses the qualia displays, the really, really long one. And the idea there was, just like the old school Pac-Man. You've got the blue walls. You've got Pac-Man roaming around, eating the little pellets and trying to stay away from the ghosts. But the twist in the 1D chomper is that you have sort of only a single hallway for Pac-Man to run back and forth in. It's a very narrow sort of hallway. And you just go back and forth. You try to eat the big pellet. I think they call them fruits in the original game or maybe there are fruits that spawn. I don't remember. But yeah, it's just the sort of back-and-forth. There's only one big red button. You just hit the button to change directions, make Pac-Man go the other way.

That one was fairly straightforward, I will say, in terms of the constraints and stuff. That qualia, I don't have it in front of me, but I think that Qualia driver board was an S3, so it was fairly beefy in terms of RAM and space and all that. I didn't really run into many issues with that.

And then I will say on that one, I lucked out a little bit. That was one of the ones where the idea came through Adafruit. I don't remember if it was PT or somebody else saw that.

on social somewhere and was like, hey, could we make a Circa Python one of this? So that's where the idea for that one came through. It was pretty straightforward to put together, and I kind of lucked out a bit because I had actually implemented parts of Pac-Man before.

I started making a Pac-Man game maybe two or three years ago at this point for a different screen, for a different device for everything, and I was building out some different parts of it, and I was able to reuse actually a lot of it from back then for this more recent project, which was really nice. I didn't necessarily know at the time that I would have a use in the future for these like Pac-Man entity classes. But yeah, it came in real handy for that one.

Paul

That's pretty cool. Another cardboard arcade project that you'd built was Blinka Says.

Tim

Yeah, Blinka Says was another fun one. That was my second cardboard one. And it is a take on Simon says.

So the kind of traditional game, well, Simon, I guess, is the traditional game. And then Simon Says is kind of the kind of idea, I guess, the core idea. but it has got the four different buttons, red, green, blue, yellow, and then it's kind of shout and response type thing.

The game will play a certain sequence of colors, and then your job is to go through and press the same sequence for all of those buttons. And then as you go along, it adds one additional button for each round. So it gets harder as you go along because you have to memorize the sequences, and they get longer, so it's harder to memorize.

I think in the real sort of released one of these, maybe it speeds up as well and it plays some music or something like that. Mine's got just a little screen for the high scoreboard. It doesn't have a speaker, and I don't remember for sure if it speeds up, but it definitely could for sure if you tweet the CircuitPython code if it doesn't, and it does get one longer each time.

That one, I would say the biggest challenges for me on that one was the physical side, the wiring, the hardware, which, you know, my background is all software. So realistically, the hardware side is generally the hardest for me. But on that one in particular, it took me a little bit to get that one finished because I started down the road of using or trying to use, wanting to use some different connectors for the buttons.

On that one, going inside the cardboard, with a lot of my projects, really, my goal is typically to keep them as easy to build as possible. And another thing I really like is the ability to take it apart, much to the the chagrins sometimes of the folks who want me to build the guides and the finished products and stuff. But I like that idea of being able to reuse your components, right? Not everyone can afford to always just buy the new thing when they want to make the new projects. So I really value that when someone builds a project, they take the time to make it so that it can come back apart and you can reuse the major components, especially the ones that are the priciest, at least.

So in that one, it's all wired with alligator clips on the inside. And initially, I wanted to use one of the Grove expander ports, like a feather grove wing, which would let me plug in the four different buttons. And I thought the Grove cables were going to be nice, but it turned out to be just a little bit too thin and a little bit too short for my needs. The size of my box, the distance the buttons were away from the middle, caused them to be not quite long enough. And then the actual wires themselves were fairly thin. I found as I was trying to get them clipped up onto the buttons and fiddled around and stuff, I was breaking them or they were getting kind of like spotty and not connecting very well.

So I swapped over to some different little alligator jumpers, and it worked out quite nicely on the inside of that one. So, yeah, the biggest challenge there was on the hardware size. The software on that's fairly straightforward.

It uses, I think uses async I.O just to pull the digital button inputs, and from there it's very basic of just keeping track which one got pressed and building up the list so that you know when the user got it right and when they got it wrong.

Paul

Lastly, and I know this one isn't a game, but tell me about Carol or Carol the robot.

Tim

Yeah, yeah. This is one of my favorites recently, Carol. It is, it's not a game in the traditional sense and that, you know, you're not necessarily playing against the game as the player, but it's in the same vein as a game.

It's got graphics that are very game like and stuff like that. And you could consider it kind of a game that's meant to teach you to program, essentially teach you the basics of programming and logic, if statements, four loops, functions, things, like this, so the basic building blocks. So Carol was originally created by a person at Stanford in the 70s for the purpose of teaching other people to program. And then I ran across it more recently through an issue on GitHub. I'll say shout out to folks who leave issues on our GitHub's with ideas like this. This was posted a while back in an issue. It took a while to come to fruition, but it was a really great idea. And I appreciate the person who left it there. Unfortunately, I don't know their name, but it's on the turtle.

repo if anyone wants to find it on GitHub, the CircuitPython turtle repo. Someone put an issue for like, hey, it'd be cool if we had this thing one day. Yeah, it was really fun to implement in CircuitPython.

It's built on top of display I.O. And the idea is you kind of write some Python code that controls this little animated robot. So you can say like step one and it will move forward one.

And then you can say turn left and it will turn 90 degrees to the left so that the next time you step, you'll be going, you know, a new direction. And your goal, as the student, as the player, is to go through a series of challenges learning all of the different bits of programming. Each challenge kind of requires you to learn a new piece of those basic fundamentals of software development. And so, you know, you kind of need to go to a certain location and then, you know, eventually you need to go to a certain location and call a function to pick up a little beeper. And then eventually you need to go take the beeper to a different location that's been specified or, you know, eventually maybe there's multiple beepers and you need to like pick up each beeper or you need to check whether or not the square that you're on now actually contains a beeper or not. And so there's all sorts of different little puzzles and challenges that you can run through using what you have learned through programming in order to drive this little robot around and achieve all these different goals. Yeah. And it was it was really fun to work on. I would say it's probably, man, I'm putting myself on the spot here, I would say, but I think Carol probably would be my favorite, the favorite thing that I made in, in 2024.

Yeah, because it's just such a cool little, I love the idea of helping teach people to program. I love the idea of gamifying, almost anything, just because I love games so much. So gamifying, the learning of programming, and being able to put it on to CircuitPython like that was a real joy for me.

so that one was a lot of fun.

Paul

And that was on a PyPortal. Is that correct?

Tim

It was, yeah, it runs on a PyPortal. It can also run on a couple of other different things. I tried to keep, with a lot of my projects, I go and try to keep it generic enough to where if you have a little bit of experience with CircuitPython, you'll be able to swap it to different displays and stuff like that fairly easily.

They're usually targeted at one directly where like, this is the plug and play one. If you just take my code and drop it onto there or run, you don't have to do anything else. But I try to break them up to where usually, you'll be able to just pass in a display to the helper object or something like that.

And so you can, if you want to, you can go and initialize an external display. And so that one, it does run directly on a Pi portal with no modifications, but it's very easy to run it on any display. The one other thing I will throw out, which actually brings us back a little bit to the constraints, which I didn't mention, was the display size itself, which is obviously typically fairly small for microcontrollers.

And I would mention that for Carol as well. In order to complete all the challenges you do need, I want to say off the top of my head, it's maybe 8 by 8 or 10 by 8 or something like that. You need a certain amount of size in order to complete the challenges that come with it.

You could make new challenges that fit in a smaller screen, but that would be my one caveat is if you do end up running that on a different screen, it does kind of at least the challenges that are built expect there to be enough room for that. So a comparable size to the Pry Portal will work fine. you could go a little bit smaller, but if you get too much smaller, then you'll need to modify those challenges.

Paul

Last question for you. You're starting a new project. Which microcontroller do you reach for?

Tim

So the first one that I always reach for is one of the feather TFTs. Lately, the feather ESP 32, either S2 or S3, TFT. They have a lot going for them.

I'll probably stick with the S3 moving forward because it's a bit bigger. It's got a bit more RAM and stuff like that until we get the next one in that generation. but for me, the reason why it's my go-to is I do a lot of work on displays.

So having the built-in display is very nice. Even though it's tiny, I can still get a lot done. If I'm working on some changes in the label or the shapes library, or if I'm tinkering away at something inside the core in display or anything like that, it's more than enough room to just do quick little tests on.

It's plenty powerful being ESP 32S3. It's got lots of RAM. It's got lots of space.

It's really fast. It has Wi-Fi so I can grab stuff from the Internet if I want. The feather form factor, generally I will say, is just kind of my go-to these days.

I've got a load of different feathers and then the feather doublers and triplers and even quadruplers at this point. I've got some of those all set out and loads of different wings. And the hardware is usually the hard part for me.

Software is super easy. The feathers and the feather wings with the doublers and everything, just being all super plug-in-play. that kind of stuff is perfect for me.

Like I've gotten really good at soldering, you know, is it 10 millimeter or whatever, the standard breadboard pins. I've gotten really good at soldering that. But once I get outside of that little box, my soldering is not so great.

And so feather wings, I can solder those up really nice and easy. And then just being able to plop them on together and not worry about wires and jumpers and anything else is really nice for me. So yeah, I've got TFT feathers with pins for when I want to use the doublers.

I've got a couple without the pins that I can still plug. stem a cable's into and stuff. There are probably three or four of them on my desk total right now.

So that's definitely my go-to. I do typically, for my actual games and my other projects, I end up usually graduating to something with a bigger screen, especially for the games and stuff. But that is always my go-to anytime I just need a random let me try this out or whatever.

Paul

That's a great pick. I have an S3 reverse TFT sitting on my desk as well that I've been using for prototyping. So I know exactly where you're coming from.

Tim

Nice.

Paul

Tim, thanks so much for being on the show.

Tim

For sure. Thanks for having me, Paul. I really appreciate it. And thanks for making the show as well. I love listening to it.

Paul

My pleasure. Thank you for listening to the CircuitPython Show. For show notes and transcripts, visit www. www.circuitpythonshowcom. Until next time, stay positive.
