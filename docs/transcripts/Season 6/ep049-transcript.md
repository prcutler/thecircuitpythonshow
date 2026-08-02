---
date:
  created: 2025-10-27
title: "Episode 49 - Sam Blenny"
---

## Show Notes

[Show notes available here.](../../episodes/Season 6/ep049.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I welcome Sam Blenny to the show.

Sam is the author of more than 30 playground notes on Adafruits Learn Playground, with topics including 3D printing, the Adafruit Fruit Jam, Zephyr, and more. Sam, welcome to the show.

Sam Blenny

Hi, good to be here. Thanks for having me.

Paul

How did you first get started with computers and electronics?

Sam Blenny

As a little kid, starting the 80s, then going on to the 90s as I got into middle school and high school, I was from a musical family, so there were lots of choir and orchestra concerts and musicals and plays and things going on around me. And I spent some time entertaining myself, waiting for rehearsals or whatever. And during all this, I noticed they were using lots of interesting equipment, lights and sound and microphones and mixers and lots of stuff.

and so that caught my attention early on and I was always interested in that. And then another thing that sort of got me going early on electronics was, you know, this was back in the 80s and we actually shopped at shopping malls. And so, you know, you'd go in through one store and you'd have to look at all their stuff and then you'd have to go past all the other stores to get to the thing you were actually trying to find, like in the middle somewhere or whatever.

So we passed by the toy display at Radio Shack a lot as we were just going to, about our business, and I always was sort of interested in that, and that led to further interest in electronic project lab kits. I'm pretty sure I got a couple of those for Christmas at different years in the Forrest Mims books and all that stuff. So this was like early on setting the stage, there were electronics around me and I found those interesting. Then for the computers, we got a hand-me-down Atari 400. This was back in the 80s and had it hooked up to a black black and white TV, and that was the ones with the keyboard. So it was an 8-bit computer, not just a video game thing. And then it had ROM Basic and Facemaker and Frogger and probably, I don't know, some asteroid thing. I don't know. So that got my attention. Then there was also desktop publishing stuff around me for the music people, because, you know, if you're doing a musical, you've got to have a program, and so somebody has to make the program. And if you got this computer with the desktop publishing, that's a lot easier than doing it by hand with, I don't know, copy and paste and typewriters and all that. So people got pretty excited about the Macintosh desktop publishing stuff with the old laser writer and whatnot. Then we had a Mac 512KE at home.

So there was some Dark Castle and Crystal Quest and Mac Paint and those things. So that was just setting the stage. Then come the 90s, I got kind of serious about all of this.

People knew I was interested in things, so I'd get hand-me-down equipment and old computers. I had a Radio Shack, TRS-80 Model 100 with ROM Basic, and that was a pretty pivotal thing. I spent a lot of time there. And so TRS-80 ROM-Basics spent a lot of hours on that, and then at some point I got a TurboC compiler.

and by that point it was maybe a Mac plus or maybe it was still on the 512K. I think it was a Mac plus. And then I had some old PCs that ran MS DOS, and so that got me going on Q Basic. And I did a lot of programming for school stuff.

I had a hard time with algebra. I got sick, I don't know, it was maybe like seventh grade or something. I got sick and missed one week when they went over something and it was just blowing my mind.

I couldn't figure it out. And then at some point, somebody got me in this book, and I got started doing some graphs and things in QBASIC. And it's like, oh, so that's what functions do.

It's like you put this number in and you do this math, and you put that number, and then you make a pixel there, and then you get these curves. And somehow in school, that just never made any sense to me. But when I got going in QBASIC, it was like, oh, that's what this is.

And so a lot of my experience with computers in middle school and high school is it's a thing that has extended my ability to understand stuff. And this was all like pre-internet. Most of this was pre-internet at home before the like scourge of AOL-CDs, like carpet bombing, everything.

And it's before all that. So it was like reading printed manuals when that was a thing. And figuring out how to do stuff in books and a little bit of bulletboard.

So that's what got me going on computer. computers about electronics. And then there's a third component of this, which is really significant to me, was my high school didn't have first robotics, but a friend from across town did.

And one time I got to visit them. And that was another sort of mind-blowing, oh, this thing exists. Why didn't somebody tell me this earlier kind of experience?

And I got to help them debug some of their code. I think they were having troubles with the dead zone on their joystick or something, because it was an actual analog joystick. And that was kind of more important with that.

And so I learned about these basic stamp microcontrollers, and that was a life-altering experience. And that was all a long time ago. Much has happened since then.

Paul

How did you discover CircuitPython?

Sam Blenny

So if you do anything with I-squared C sensors for whatever purpose and you're reading about them, it's pretty hard not to come across Aida-Fruid stuff, Lidi-A's drivers are they're going to come up if you start searching for things. And so I'd been aware of that for, I don't know, I don't even remember when. And then I think maybe about eight years ago or sometime around then, I was trying to do some data logging stuff for indoor plant things. I wanted to know what the temperature was and make some graphs.

I used, I can't even remember which board, but it was one of the boards that is capable of running CircuitPython. And I used some sensors. I don't know if it was Adafruit sensors or Sparkfund sensors, but at that time I was researching a lot of what was on the market.

And so I probably, I can't remember, this is when CircuitPython wasn't all that far long and it was a lot more Arduino things. Ever since then, I had been paying increasingly more attention to what Adafruit was up to. And then last year, I got going on the CircuitPython stuff a lot more seriously.

Paul

You've written over 30 playground notes on Adafruits playground sites. A number of them are about Adafruits new RP 2350 powered microcomputer, the fruit jam. Tell me about the game pad tester and how you started working with the fruit jam.

Sam Blenny

Okay, yeah. So with the playground guides, I enjoy technical writing, and I had been watching the Ask an Engineer show. I follow Adafruit stuff on YouTube fairly regularly.

And P.T. AKA Mr. Lady Ada on that show, he mentioned that they were doing on this playground guide stuff that they built this system. And they were hoping to get writers interested in putting content there.

And I thought about that. like, yeah, that sounds like a good idea. I'm going to do that.

And so I did that. And I started off just doing some projects with the boards I had on hand. And, you know, I have a limited parts budget.

I don't let my spell just spend wildly on this. So I started off with what was laying around. And eventually that worked out to doing a game pad tester on an ESP 32S3 with the TFT display, the little feather boards.

And I think they may have meant. mentioned that on the Asking Engineer show, and then later I did this pumpkins and skeletons game on that same board, and they thought that was interesting. And so I had this conversation going by email with BT, and then at some point it was like, hey, this Fruit Jam board, you want to prototype? You want to do some projects with it? And I was like, yes, please. That sounds awesome. And so they sent me one of those. And they had mentioned that it would be interesting to have a USB game pad tester for fruit.

jam and I was like, yeah, that'd be good. So I did that. And because it has the USB host and the DVI display, it's possible to do a lot more than with the little tiny squinty little display on the feather that's so hard to see. Like you can get it with a camera to put it in a guide, but you've got to get your lighting careful. Like you've got to do the side lighting carefully so that the display doesn't wash out the exposure on the rest of the board. And it's also tiny. And if somebody tries to do it. They're like, wow, the screen is really small. But if you use the DVI up it on the Fruit Jam, you can just put it on a monitor and plug in a gamepad or a keyboard, and it's just fabulous. That's how I got started on that. What about the USB host MIDI tester?

So the Fruit Jam thing, you know, if you look through my Playground Guide author page, there's like Fruit Jam, this, root jam that, fruit jam the other thing. And it's kind of, I do one project, and I go, oh, there's this other thing I'm curious about, but that's too much to put in this one because I've got to write this up, and I want to have it finished in a reasonable time. So put it on the list of things to do next.

And one of the obvious things, once I had gotten the game pad stuff sort of figured out, I was like, oh, what about MIDI? And, you know, like as I said, I come from a musical family, so I'd been aware of MIDI since, you know, a long time ago. And, you know, it's always been kind of interesting.

And it's also a pretty good stress test for the USB stack because you have to pull, because of the way things are set up with this, to get MIDI input, you've got to pull and you've got to pull fast, and you also have to do the display updates. And there's all this stuff going on. It's like, yeah, this would be a good stress test.

And so I did that. And yeah, it worked out pretty nice. One of the things that I enjoyed doing with that is since I had so many pixels to spend, I made a grid of USB channels and notes.

So you can see as you blink on it, which channel stuff is coming in on, and which note number it's coming in on. And sometimes, like if you're doing a percussion thing or a keyboard, you won't necessarily have the note range mapped where it needs to be for the software instrument that you're using. And so, like, you'll bang on stuff, which are on the wrong octave so nothing happens.

It can be confusing. So it's nice to have stuff like this. Oh, that's what's going on.

Paul

What about the Fruit Jam Color Checker?

Sam Blenny

So one of the things that came up when I was working on that Pumpkins and Skeletons game, or maybe it was the original USB tester that I did for the Feather, USB 32 S3, TFT thing, I had made my sprites for display IO tile grid using, oh, I can't remember the name of the app, but one of the iPad apps for working on pixel art. Or maybe I used something on Linux.

I can't remember, but it was on a color managed display using 24-bit colors, and I just picked out some stuff that looked good. And then when I got it onto the display, and I looked at it as like, whoa, that is not color-match to what I was doing. What happened?

That had puzzled me, and I couldn't really figure out what was going on. At that point, I didn't understand that when you're doing the 8-bit color or the 16-bit color, which can happen with display I.O., depending upon the hardware and how you initialize things, that you're actually getting RGB-332, so three red bits, three green bits, right, two blue bits, I guess. And then there's all this quantization and filling of the low bits when it gets moved to actually, display on hardware that uses more colors.

And then there's the 16 version of that where you have RGB 565, 5 bits, 6 bits, 5 bits. And what you really want, if you're doing a color match thing, is RGB 888, but that's not how these displays work. And I didn't understand that until I did that Fruit Jam color checker thing and really worked through it and tried out the different video modes and saw whatever.

it did. That process for me was about how do I get sprites that have the colors that I want when I'm trying to make a little thing that uses sprites. And so people who are trying to make games for fruit jam, if they understand that the RP 2350 is doing these things when it does the DVI output, then they can make sprites with colors that, they'll end up being happier with, hopefully.

And like one of the things that can happen is they can be dimmer because the hardware does a zero fill when it does bit extension to go from, say, five bits up to eight bits. You get zeros on the low bits, which means things can be darker.

Paul

For CircuitPython's upcoming 10.0 release, you've done some work to improve USB host. What kind of improvements have you been working on?

Sam Blenny

So as I was doing all this stuff and playing with all these game pad things and all I noticed in the media stuff, sometimes there would be a drop-to-note or a stuck note. Or as people are building things with the USB host on Fruit Jam, you definitely need to catch exceptions. There will be exceptions.

There'll be timeouts because not all USB devices will answer you every time you ask them for something. You have to pull them, and they won't always have something ready, and then you'll get the timeout maybe. Or maybe not.

Maybe you'll get something with like zero bytes. So you've got to check. otherwise your code won't work.

And then if somebody un plugs a device or if certain other things happen, you may get a USB error exception. And if you don't check for that, you won't have any way to know when somebody unplugs something, so hot plugging won't work. So as I was in particular trying to get hot plugging to work reliably, I noticed that there was some stuff that I couldn't do anything about at the Python level.

And I wanted to get to the bottom of it so that people would just plug stuff in of at work and not have to worry about all that nonsense. And so I got on a little quest to try and figure out what was actually going on, and I made some issues on GitHub, and I did a PR, and Scott did a PR, and we managed to track down and fix. One of the things was that there was a bit of an impedance mismatch between the tiny USB library underneath and in CircuitPython that was using time USB.

They didn't quite agree on some of the error handling. Like there were things that could come up from Tiny USB that CircuitPython would treat as if it was something else instead of the right error condition. I'm a little fuzzy on the details.

The way I handle all of this stuff is like, you know, I write it down and then I move on with my life. But the basic idea was there were some error codes that weren't being checked for at the interface between Tiny USB and CircuitPython. And so I added a PR to check for that.

And then there was this other thing, which was with DMA stuff that was over my head, and Scott sorted that out, which is related to some of the things that had been having DMA trouble. I think it's, if the DMA is coming, if it's two or from the S-Ram that's on the RP 2350 itself, everything's cool. But if you're trying to use the PSRAM chip that's external, then things can get weird.

So if you don't prevent the PS RAM from getting included in a DMA transfer, you can have strange things happen. And we were having strange things happen. And Scott figured out how to fix that.

Paul

Well, that's pretty cool. I'll make sure I link to some of those PRs in the show notes as well. Last question I ask each guest.

You're going to start a new project or prototype. Which board do you reach for?

Sam Blenny

It depends. There are a lot of reasons why you might want to do one thing over another. you know, like maybe you're broke or you've got a big parts of pile that your wife or someone is wanting you to clean up or, you know, whatever. There are reasons why it makes sense. Just use the thing you have. If you're just messing around and you've got some stuff, use what you have.

There are times when you need to hit specific functional requirements. Like, say you want to do something to monitor plants and it's going to be potentially exposed to moisture. like if you put things outside where it's not temperature controlled, it may be like not out in the rain and the snow, but there's going to be condensation because there's going to be so much temperature change and you're going to have to account for, you know, okay, I need to put a desk in pack in there.

And when you're in that kind of a situation, you need to think about your requirements. Like if this is going to run a battery, how long do I need to go before I can charge or swap the batteries? What does that mean about which boards I should use?

like the ESB 32 variants do quite well on low power, but they're not all the same. And then say, okay, I want to do solar, then you're going to have to think about, well, I need a battery and I need a charger, but which board that can run on a battery is compatible with a charger and that will narrow you down to a couple things. Like, Lady Ada has introduced recently some feather boards that have a jumper on the back that you can cut.

it'll be like CHG or charger or something, and you cut that, and it pulls the normal feather charger out of the circuit, so then you can use one of the solar charger boards, and it won't burn anything up. So that's just kind of an engineering thing, and that's how I think. It's like sometimes it doesn't matter.

Then you can understand your requirements are, do whatever you want. And then sometimes other things do matter. You've got a budget.

You've got, you know, maybe you, got a deadline. You know, maybe it makes sense to spend more and get something done fast. Or maybe you need to make a lot of them.

So you really need to think about how much it costs. Or maybe you have some weather thing that you're like, you need to make it sure it won't get wet and die on your second day out or whatever. So it depends.

Paul

Sam, thanks so much for coming on the show.

Sam Blenny

Thanks for having me.

Paul

Thank you for listening to The CircuitPython show. For show notes and transcripts, visit www.CircuitPythonshow.com. And if you're enjoying the show, please leave a review. It really does help. Until next time, stay positive.
