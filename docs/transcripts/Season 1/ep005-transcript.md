---
date:
  created: 2022-03-29
title: "Episode 5 - Rose Hooper"
---

## Show Notes

[Show notes available here.](../../episodes/Season 1/ep005.md)

## Transcript

Paul

Welcome to The CircuitPython show. I'm your host, Paul Cutler. This episode, I'm talking with Rose Hooper, author of CircuitPython's LED animations library.

Rose is a lifelong technologist and has actively participated in many aspects of computing since childhood. Rose now spends her time leading and mentoring software development and DevOps teams of all kinds, enjoying the ability to give back to the communities that have helped her. You can also find Rose participating in open source projects like Home Assistant and CircuitPython.

Rose, welcome to the show.

Rose Hooper

It's nice to be here.

Paul

Let's start at the beginning for you.

When did you first get involved with computing?

Rose Hooper

Probably before I was eight, but really remember the moment when my dad brought home a Hyperion PC compatible. It was a portable with a three-color, I guess you call it a four-color monochrome display and two built-in floppies drives. And it came in a big, heavy case, and they were very expensive.

That would have been more than 30 years ago. I'm failing to do the math right now, but what my dad did is sort of unpacked the computer, showed me around how to start it up and shut it down, and then pulled out a bunch of floppies. These are five and quarters.

So they were floppy and it was fun to flap them until I got in trouble for doing that. And that sort of was the beginning for me. My dad showed me about bulletin boards because there was a modem in the computer, showed me how to code a little bit by handing me magazines that had some basic code snippets in them.

And trying to sort of remember what else I got started with their, I guess, how it would have been WordStar and Lotus 1, 2, 3, D-Base 3. And these sort of created a foundation on which I've built pretty much all of my career.

Paul

That's awesome. Do you remember how fast, how many bods the modem was?

Rose Hooper

It was a 300 baud modem. That's what I started out with as well. And it was not an acoustic couple. which was kind of rare at the time. And it was, I don't think it had touchtone.

I think it was until I got a 1200 bod modem that I had touchtone. So that was through my intro decoding. And I got into electronics around the same time when my dad got me one of those Radio Shack, 60 and ones or 210 in ones.

I can't remember what number of projects. I just remember the springboard and the components and the diagrams. I remember building a crystal radio and there's something that, oh, a spark gap oscillator, which you're really not supposed to do, but they had it in there and it was using the relay to make it buzz.

And it was really just terrible for EMI. So you've been a maker from a very young age. I have.

Like creating software was something that I've been doing since the early days. I ran a bulletin board for quite a while and ended up writing a BBS. kit. What the heck is the phrase I'm trying to think of? Oh, a door kit in QuickBasic of all things that made it easy to write some sort of little games and apps that interacted with the volunteer software. I don't remember what happened to the source. It's probably long gone on a hard drive that died that was barely spinning. So I'd actually open it up and help it start and put the cover back on and it was getting more and more errors and spin right and all sorts of other tools to try to recover data. I think it was spin right.

Paul

What was the BBS culture like back in the late 80s, early 90s?

Rose Hooper

So it would have been early 90s. The culture was very open and it was a place where I would get together with SISOPS or yeah, I guess we were calling ourselves SISOps back then. There was a wide range of ages. There was people my age at the time, which would have been probably age 10 or 11 and all the way to retirees.

And everybody just sort of talked about technology and hung out and eight wings and the adults drank beer. And just it was a lot of fun. Got to learn a lot about people and technology. Met some interesting people.

Paul

So from there in the 90s, from working on a BBS, you got started with some small ISPs and free nets.

Rose Hooper

Right. So I started using a free net. one of the few ways that I had access to the internet back in the, I guess it would have been around 92-93.

I also had a UUCP node connected via dial-out to one of the SISOPs that I had met while at KMahas. I guess it would have been Fidonet meets. And then from there, pretty quickly sort of spent a lot of my time on National Capital FreeNet, where I would eventually work for a couple years around.

1995. So I got to experience the internet in a way that a lot of people didn't. I was sort of involved in getting dial-up, PPP, and slip available to the free net users back when it was actually modems, literally modems in Iraq. And you couldn't, like the modem concentrators didn't come till a bit later. And then I went to work for commercial ISP in 97 and kept working at sort of related technology companies for a while, ended up working at registrars and registries and various other things in between building software and systems of all sorts of kinds.

And my language of choice back then was Perl, mostly from sort of the Sysadmin side of things. And it was one of the first languages that you could really build web apps with that was well supported. And I learned a lot about the innards of Pearl how it dealt with all sorts of things, like how it handled strings and such.

And these little nuggets of how to do things just gradually collected over time. And that interest in how the languages work sort of was a step towards sort of my later involvement with CircuitPython and some of the stuff I ended up learning about the innards of how Python works.

Paul

So how did you come to discover Python as a Perl user?

Rose Hooper

So for me, it was actually a choice in probably the early two, 2010s. I'm not sure the exact year, but it needed to start some new web services that were going to be the foundation for some domain-related thing and decided that Python that I've been hearing about a lot from friends and colleagues was something to look at. That was back in the Python II era. And it was a wonderful language once you got past the indentation chain being important. And it created a, sort of a new understanding of how languages shape how you think about coding.

How so? Well, with Python almost everything back then being an object, and sort of just a lot of the helpful conventions and the approach to dealing with things was quite natural. And even in modern Python today, everything is still an object.

Even more so. Like I remember when sort of the object, object showed up. And Pearl's object model was very different than the Python one.

And it took some getting used to. And I still felt for a long time like I was missing something about Python and what made it so powerful. And it wasn't until a couple of years of using it that I learned all about co-routines and generators and all the other goodies that make Python super powerful and ideal for incremental development and data exploration.

and stream processing and all sorts of other goodies and also for commerce and related activities.

Paul

So you've also been active in the Home Assistant community, I believe, which is also written in Python.

Rose Hooper

Right. So I went to one of the PyCons, probably 2015, because it was in Montreal. And Montreal wasn't far away from my hometown of Ottawa.

So I went to one day of it at the urging of a friend I made back in the Freenet days and sort of fell in love with Python. And at the time, I didn't really get into CircuitPython then, but I did learn that Micropython existed. And I'd be messing around with home automation stuff.

Things like automating the humidifier, because in the house, the humidity would swing. You'd have to go and manually adjust the humidifier and the humidistad on it based on what the weather was going to be at night. And I was getting tired of having to go down into the basement where it was a little bit too low for me, so I would bang my head going into the space.

And so I made a, and I discovered various different sort of communication modules that weren't your typical. I can't, I think, I can't remember which one it was, but it was enough for me to make a mini-sensor network where I had a temperature probe outside in the garage, and I had humidistat in a couple of spots around the upper, floors of the house where I needed to know that the humidity was up there because they were the warmest and most humid part of the house. And so they were prone to the condensation more than the ground floor and basement. So I made a micropython powered humidistat control, but I kept running into limitations to do with memory because I was using ESP 8266s and Arduino. And it was okay, but it never really sort of won me over. And then I went to.

to PyCon in 2018. So somewhere in there was Home Assistant. So I met the Home Assistant people, one of the PyCons, and realized that it was what I was looking for, for Home Automation, Glueware.

And prior to that, I'd been looking at some of the Java-based ones and Parole-based ones. And they just didn't, they weren't easy to use. They weren't easy to extend.

And Home Assistant was. Home Assistant became sort of a fun playground. And I remember, I think it might have been one of the first Sonos modules, and it wasn't much code.

It was very easy to do because I just used the existing Python library and contributed some changes to get sort of the data storage that was direct to the MySQLDB module using SQL Alchemy. So it would be able to be, actually it was the SQLite module directly. So getting it onto SQL Alchemy suddenly made it so that MySQL and other storage and Mongo and all that became just possible.

because you had the database abstraction finally. That's awesome.

Paul

Hi, it's Paul. I'll get you back to the show in just a moment. Thanks for listening.

If you like what you're hearing, hit the subscribe button and leave a comment that you subscribed. For other ways to support the show, visit CircuitPython show.com slash support. Now, back to the show.

So from MicroPython and Home Assistant, how did you come to CircuitPython?

Rose Hooper

So that was sort of a fluke. I was looking around at the spring. at 2018's PyCon.

And I kind of sort of tired myself out on home assistant because I didn't really feel like I needed to automate that much more stuff. I got it all working. And so I got bored of the project is, I guess, the best way to put it.

But it was great, fun. And the community around it was wonderful. And it was just a sort of a fun project that's still growing.

And it's nice to know that in the past I contributed to something that a lot of people now use. I'm actually thinking about bringing it back into my life because I want more automation and I realize that home assistant might actually be better for coordinating it than trying to do it. Well, right now I'm trying to do it all with CircuitPython and hardware, but it might be easier with just a bunch of different separate modules.

Sure. So yeah, so I dropped into the CircuitPython open space and it sounded really interesting. And then there were Kattni and Scott.

And I think Dan was there. as well. This is PyCon 2018.

It was the first time that CircuitPython had shown up at a PyCon that, well, okay, since I'd started attending, which was not as long as many of the others. And by that point, I'd already fallen in love with the Python community and PyCon and just the open and giving nature and generally harassment-free, not completely, but compared to many other communities, it was a very safe place. And so I went into the CircuitPython open space and was not chatting with Kattni and chatting with Scott and Dan and ended up working on pretty sure it was, yeah, it would have been something to do with the restarting of the board and like making it so that I think it was the reload exception or something. Okay. Which was used by the soft. Like it was raised during reboot or something. I can't remember the specifics of the issue. I just remember working on that. And that got me deep into the guts of CircuitPython and realizing that it's just a pretty straightforward C program in the end. I'd done some C on and off regularly throughout the years because I've just touched just about any language that comes near me if I've got an excuse to, and that gives me an opportunity to learn it. And then towards the end of the session, started to play with the LEDs, and I think it was a Gemma, an M-Zero Gemma, that was in the PyCon bags and that got me kind of interested in the LED bit, but it was sort of, it was the end of the sprints and PyCon was over. And a couple weeks later, I was talking on the CircuitPython Discord with Katney, and she noticed my interest in LEDs and got me, I think I ordered myself some hardware and then, like, I can't remember what it was. It was one of the many LED strips with NeoPixels or one of the matrices or all of the above.

And the animation supported the time. It was really basic and fast LED was sort of the one that people kept referring to. And there was fancy LED, but it wasn't really animations.

And what I wanted was a way to, or eventually wanted it as a way to create sort of a sequence of animations. But back then, I just wanted to fast rainbows. With Neopixel and dot star libraries being pure Python, they were pretty slow because you had to do a lot of byte order manipulation.

So somehow along the way, started working on, ended up being called PixelBuff. And it was basically an acceleration for doing the byte mapping so that you could just quickly and easily and rapidly emit the byte stream to the dot stars and neopixels.

Paul

And once you have pixelbuf, you would go on to write the LED animations library itself using that, correct?

Rose Hooper

Right. And I may have written some of the animation library before, Pixel buff was actually available to a wider audience, and it was using the animations for the Christmas tree back in probably 20, either 2019 or 2020. It would have been 2020 Christmas.

I've lost track of time. It was one of those Christmases.

Paul

Sure.

Rose Hooper

I had an artificial tree, and Katney had grabbed a bunch of the LED strips, and I wanted to animate the tree. And Pixel Buff came out, and ended up on one of the NRF feathers and drove the tree. And it was a lot of fun.

And then sort of people noticed the animation library. And Katney had been helping steer the direction of the library, sort of being the advocate for users and API interfaces. So she was the product manager and I was doing the coding.

And that's how it sort of evolved. And the parts of the API that she didn't help with are some of the worst pieces of it. It does need some, it needs me to jump back in there and clean it up and really make a version 2 of the API that's simpler, faster, and takes advantage of all the new features that are in Circa Python that weren't there back then.

Paul

We can always make something better. Every maker is always tinkering with a project that they've started or finished.

Rose Hooper

Yep, yeah, that's for sure. And eventually the Christmas Tree LEDs turned into a wall of LEDs and when there was a wall that we could do that with back in Ottawa at my apartment. I did all sorts of stuff on it like text and various different animations and wave patterns and color blending and stuff, most of which are just sort of garbagey kind of code, a lot like what I had done back when I first started playing with graphics in Basic back when I was eight. And that was mostly just loops and just random algebra. I'm not really understanding any of the math. This time around I had a bit of an idea of what I wanted to do.

And any time I went and spent too much time trying to make it do what I wanted, I never quite got the effect I was looking for. So it was when I was just fiddling randomly that I eventually got something different than I wanted but looked good.

Paul

That's amazing. We're almost out of time, but before we wrap up, I want to give you the opportunity to ask me a question in a segment I called Turn the Tables. I've been asking you all the questions. What can I answer for you?

So what got you started with Python? I had a specific project. I found that if I don't have a goal in mind, I'm never going to learn that thing.

And for me, it was a sports app. A good friend of mine ran a major league baseball pool where you just picked all the winners at the beginning of the season. And then at the end of the season, it calculates it.

It's not fantasy, nothing in between. So he needed a program to do that. So I'm like, I've been wanting to learn a language.

I had been around open source for many, many years, but didn't know how to code outside of a little XML. So I took one of the classes online, and then I bought a training from Talk Python training, their first Kickstarter, and I've been doing that for the last five, six years. Really enjoy Python.

There's still so much that I just don't know. I'm still very much a novice coder.

Rose Hooper

That's one of the fabulous things about Python is like a few other languages. You can just jump in and start doing stuff and then realize how much the more there is to learn. Absolutely.

Paul

So last question for you. You're going to start a new project or build a new prototype. Which microcontroller do you reach for and why?

Rose Hooper

The first question to myself would be how much I owe do I need and how much CPU performance or processing performance do I need and is battery life a concern? If it's going to be a plugged-in project, it's probably going to be something RP2040 base these days. It just makes sense and it's readily available.

I've, like, the M0 microcontrollers and the M4s are sort of the ones that I use the most these days, mostly because Aative Fruit makes such wonderful hardware. And the macropad is actually the one that I've been working with the most recently, and it's got I squared C on it. So it's easy to connect it to more things.

Paul

Yeah, my macropad is by far the favorite thing that's on my desk right now. I share your enthusiasm for that. Well, that's all the time we have.

Thanks so much for being on the show. You're welcome. It's been a pleasure.

Thank you for listening to the CircuitPython Show. This was episode 5 recorded March 4th, 2022. For show notes, transcripts, and to support the show, visit CircuitPython Show.com.

Hit subscribe and stay safe. Thank you for listening to the CircuitPython Show, an independent podcast with the people in and around CircuitPython. For show notes, transcripts, and to support the show, visit CircuitPython how.com.

I'm your host Paul Cutler, and I'll be back next episode. Don't forget to hit subscribe and stay safe.
