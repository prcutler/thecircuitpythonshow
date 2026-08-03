---
date:
  created: 2023-05-08
title: "Episode 27 - Ben Shockley"
---

## Show Notes

[Show notes available here.](../../episodes/Season 3/ep027.md)

## Transcript

Paul

Welcome to the CircuitPython show. I'm your host, Paul Cutler. This episode, I'm joined by Ben Shockley. Ben is a program manager, aerospace engineer, geek and explorer who loves to tinker, research, and learn. Ben, welcome to the show.

Ben Shockley

Thanks a lot. I'm happy to be here. Happy to support it.

Paul

How did you first get involved with computers and electronics?

Ben Shockley

It's been a while, and this may date me, but let's see here. Back in school, I remember the very very... first real computer experience would be how to be Oregon Trail on the Apple 2 and the green screen and everything and you know that was just a little bit of usage here and there I think my real foray into computers started when my parents got one of their very first multimedia computers I started to really figure out all the different things that you can do with this and then I started tinkering with it and you know after a while sometimes a computer would I'd mess it up and family would get mad and then I'd fix it of course the back working again. But after that, I just, I think they decided to go ahead and get me my own computer in high school because I think more or less they were tired of me messing with theirs. But so, you know, ever since then, I've just been tinkering with computers and building them myself and, you know, pretty much doing everything I can think of with a computer and enjoying every minute of it.

Paul

That's great. I have a similar story with Oregon Trail and Apple 2. It's still very fun place for me.

Tell me about the mini-figure circuit boards that you do. design. Well, first, what are they, and how did they start?

Ben Shockley

Sure. So they are basically a development board similar to many dozens of other boards available today that run a micro little chip on it, and you know, you can think of it as a small computer with I.O. on it. But what makes them a little bit unique, I think, and kind of special, is that they're shaped just like a mini figure and their size.

I tried to match it as best as I could one for one with a mini figure. And they started many, many years ago, what really started was I kind of got interested in circuit board design. I wanted to see, hey, is this something I can do myself? Is it possible? Can I teach myself how to do this?

And, you know, started searching and researching about it and quickly figured out, yeah, I think I could probably do this. And it started with very basic audio circuitry. I wanted to make like a headphone amplifier. And, you know, started digging into that and researching that and kind of quickly said, okay, I think I could do that, made a couple of things here and there.

And then it moved over to, well, what if I could do something a little bit more? And, you know, I had seen all these various boards out there. I think we all kind of at one point maybe started with an Arduino, and I think I kind of started with that.

At the time, Adafruit had some new boards coming out with, you know, some different ships, something, you know, into a 32-bit range. And I thought, oh, that looks kind of cool. What if I try something like that?

And, you know, the first board that I made was a basic rectangle shape thing. It was pretty much mimicking what else I saw. But I thought, you know, that's kind of fun.

But what else could I do? And I started to morph it into this. I love Lego and grew up playing with it.

And I thought, that would be kind of neat. So it started to morph. And the first few rounds of design were more of a blob that kind of looked like a mini figure.

And as I started to explore the capabilities of really the PCB manufacturers, I might have designed anything in the world, right? But whether it could be built or not was a different question. And I started learning, yeah, they can really start to do some of these finer details that I was wanting to put in there.

And so, you know, I think at first there was no gap between the legs and the arms just kind of were stuck right at the side of the mini figure and that kind of thing. And I soon learned, no, I can put these smaller details in here. This is all the hobby stuff I do in the, you know, my free time.

I just developed it more and more and more, and it became more like an actual mini figure. I think the first one that I would call a success was based on a Sam D-21 board by Atmel or Microchip, I guess, now. Made a bunch of those by hand.

I think I started sharing my results on, like, Twitter and various places of like that, hey, you know, this is kind of fun. And to my surprise, maybe I shouldn't have been, but to my surprise, people were really loving these things. then I started getting questions, hey, can I get one for me?

Can I get one for me? Sure, yeah, hold on, let me do this. And it was all assembled by hand at the time.

You know, in my designs, I kept trying to do that because I had no idea how to engage someone to go manufacture these for me. So I just had to work with what I could possibly do. I think I bought myself a hot air gun, and then I started thinking, okay, I guess I got to get templates for solder paste and, you know, things of this nature as components started to get a little bit smaller because it is a very small.

board to work with, so the components had to be pretty small. Yeah, I guess I, you know, I just started making them by hand and then moved up, saw an M4 chip, the Sam D-51, and I thought, ooh, you know, let's go to that one and see what else we can do. And so, you know, made a, my mini-sam M4 was kind of the one that I'd made for a while, and I've made hundreds of those. That was the one I started to actually get produced by someone for me because I just couldn't, couldn't hand-make them in the quantities people were wanting them. And that was several years ago. I think I had my last major buy for that. Unfortunately, like a lot of people, the chip shortage hit me pretty hard, and I couldn't find those anymore. At the same time, Raspberry Pi Foundation came out with this RP 2040 chip, and I thought that's a nice looking little chip. I started reading about it.

Their documentation was great. The support looked great. The chip itself was less than a dollar, and I was paying several dollars per chip for the microchip version.

I thought maybe it doesn't need something like the M4. Maybe an RP 2040 is more like what it really takes. And there were times when there might be several months between development work or effort on it that, you know, life takes over, right?

And I think in between all of this, my wife and I had a daughter, she's six now. So that kind of dates how long I started all this many, you know, years before that. But eventually, I finally picked it up again in the last couple months, really been running with it trying to finalize that RP2040 version of the chip, which I named Fig Pie, for semi-obvious reasons.

Yeah, it's been, again, a pretty big hit, I guess. And I've got a few boards on hand that I, you know, had assembled. And I think there are about three or four iterations of prototyping before I got it right.

But I'm getting a little bit better at it.

Paul

How did the two boards compare? Were you able to add any new functionality to the mini-fig?

Ben Shockley

Yes, a little bit. I think one of the biggest issues that I had personally with the Minnesam M4 was the fact that I just didn't have any good way of putting I.O on there. So it currently has these 1.27 millimeter spaced holes, and they're pretty small. And it just honestly trying to actually work with it is pretty hard to do. And so one of the goals with the fig pie was to make connecting to it a little bit easier. So what I ended up, up doing with that one is on the back of it I've got several their JST I might get this wrong but I think it's SH they're the one millimeter spaced connectors they are and they're their most of them are four pin which matches the Stema QT or the quick style connectors and I did that on purpose for a couple reasons two of the ports are actual Stema QT quick ports they're I2C based with the right the pins in the right order and everything so any of those boards that you find on Adafruit, the Stem & QT boards, or any of the quick boards you can find on like SparkFun.

And I think the Seed Studio Grove boards also have the same kind of basic wiring setup are all compatible and should just plug and play. And all the wires and the connectors are available for, you know, a couple dollars here and there. And that was intentional because I wanted, again, I wanted people to be able to connect to it.

And I didn't want to have to design my own sensors and whatnot. I wanted to have this great, already developed ecosystem that I could just plug into. So that's what I added there.

And I think that's probably the thing I like the most. The other addition that I kind of enjoyed doing was I added some additional RGB, I guess you could call neopixels basically. The original, the Sam M4 has just a single one, which is more or less to support the circuit Python.

What's great about CircuitPython is it does give you feedback. you know, if you made a mistake here or there through that, RGB LED. Well, with a 3 by 3 now, you can also use that to, I don't know, kind of create other little things like I had made a heart or I made it count to 10 or, you know, stuff like that.

So that's kind of nice.

Paul

Speaking of CircuitPython, how has CircuitPython helped with designing the boards?

Ben Shockley

So I will say, without a doubt, without CircuitPython, without Adafruit supporting it, without all the great people, many of whom you've interviewed supporting it, There would be no way I would be where I'm at today. I would have no idea how to write firmware. I'd have no idea how to write the boot software for the SAMM4, which you have to do.

It would have been just me completely lost. Their support, again, has been invaluable. They've been excellent at answering questions on Discord and places like that.

If I run into an issue, I've just pushed real quick, hey, I can't get this to work. And I think, you know, a couple times they've piped up, hey, I think you've got the wrong size capacitor in there. You really should probably put this one in there.

or, oh, yeah, you need to change your firmware or your board definition to say this and that, and that'll get you what you're looking for. And so, again, it's just been invaluable. And then just without that community, I don't know where I'd be.

So, yeah, I love it.

Paul

That's great to hear. As a self-taught PCB designer, what advice would you have for people just starting out designing their own PCBs?

Ben Shockley

Do your research on the tool you want to use first. There's a lot of good ones out there. I started with Eagle CAD back when it was, you know, it was its own company.

I think Autodesk bought them. I still used Eagle for a while because I have a grandfathered-in license, and so it's kind of hard for me to give that up. But I have, the Fig Pie actually was designing K-KAD.

And so I have moved over from Eagle to a K-KAD setup. And I like them all. They're all very similar.

just like any sort of CAD tool. They all have the same type of thing as just learning where each of those tools is. And then once you kind of, once you find your tool, just jump in.

Spend a little time, goof around. I downloaded a lot of examples from other people just to see how they did it. I think that helps a lot.

You know, it's just, it's like anything, there's a learning curve to it, but anyone can do it. It's possible.

Paul

Are the minifig boards open source? Do you share the design files as well?

Ben Shockley

I do. Everything I have is open source. So I use GitHub or I'm kind of moving maybe over to my own GitLab set up on my own server. But yeah, I share everything out there. I even have OSHpark.com. I don't know if you've ever used them, but they're great for prototyping circuit boards. They've been also very helpful and very supportive of me throughout the years as well. And that's, I use them for all my prototyping because they're fast, great quality, really helpful.

I have some of my boards already added to that. So if you don't even want to do the design aspect and you just want to order a board, I have links on my website to just click order a board and you can get some boards sent to you, the bombs available, stuff like that. So yeah, everything's open source, ready to go.

Paul

Well, that's great. Last question I like to ask each guest. You're about to start a new project. Which microcontroller board do you reach for?

Ben Shockley

Well, I would say my own. But the reality is, yeah, I've got a lot of things. the Adafruit boards as well, including the CircuitPython Express, I think, was what it was called, but kind of the round one that has everything built into it. It's a great board because it has so many peripherals built in, so many things to try out and test and figure out, and it's been a great tool to use as well. But, you know, sometimes all, whatever, whatever board happens to be, whatever's closest to my hand when I'm, oh, I need something real quick and reach out and grab it and whatever's there is what I use.

But I think we all tend to have like that drawer full of boards, right? That you open up and which one do I want today?

Paul

Just full of boards in antistatic bags everywhere.

Ben Shockley

Yep.

Paul

And if people want to learn more about the minifig boards, where should they go?

Ben Shockley

So minifigboards.com is, what I'll say is a great place to start. It has details about the boards there. And like I said, it has links there to my GitHub, repository to links to directly to order boards.

Again, if you don't want to have to open up a tool to look at the design or whatnot, then you can go directly there to get a board. You can also order boards through the website as well. If you want to skip all of that and just order something already made and tested.

Paul

Ben, thanks so much for being on the show.

Ben Shockley

Yeah, I appreciate it. It's been a lot of fun.

Paul

Thank you for listening to The CircuitPython Show. For show notes and transcripts, visit CircuitPythonShow. com. Until next time, stay positive.
