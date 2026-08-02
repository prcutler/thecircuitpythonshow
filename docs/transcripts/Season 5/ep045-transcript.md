---
date:
  created: 2025-05-05
title: "Episode 45 - Cooper Dalrymple"
---

## Show Notes

[Show notes available here.](../../episodes/Season 5/ep045.md)

## Transcript

Paul

Welcome to T CircuitPython Show. I'm your host, Paul Cutler. This episode, I welcome Cooper Dalrymple.

Cooper is a web developer and musician and has been contributing to the new audio effects available in CircuitPython. Cooper, welcome to the show.

Cooper Dalrymple

Hey, Paul, how's it going?

Paul

It's going great. Thanks for making time today.

Cooper Dalrymple

It's always a pleasure. I mean, hey, this is only my second time, but I'm excited each time, so it's great.

Paul

How did you first get started with computers and electronics?

Cooper Dalrymple

Well, I've actually been working in this field, I guess, for a really long time. I started when I was a young kid, probably like 10 or so. But really, the first big thing that happened, I guess, in this field, if anyone out there maybe has heard of the Science Fair, right, Intel, ISF, it's like the International Science Fair. I kind of got into that, it roped into it.

And I actually started experimenting with electronics back then with Arduino, even some like atom computers and stuff like that, doing a lot of computer vision. And it's really funny because I look at what I did back then and it seems so primitive now. I was literally using Game Boy cameras.

I would strip out the sensor from it and plug some wires in and use an Arduino library, etc. But now we've come so far. In fact, I know with Adafruit and stuff, they recently gave some support to the Open NV project, which seems super cool and leagues beyond what I was doing back in, what, 2012 or so. So that's kind of what got me started like really getting into hardware and programming.

And I kind of followed along some of the companies around that time like spark fun stuff like that

Paul

how did you discover circuit python?

Cooper Dalrymple

well i known about it for a while though i hadn't really dived into it you know i was definitely for a long time i was hardcore if it's not c or c plus plus you know what are you doing but i think a lot of that mindset came from i think that early air i say early really you go back to intel 8080 etc but really that early era of mcUs in you know the 2000s and early 2010s yeah i'm talking about like the At Mega 328. Well, I mostly dealt with the At Mega stuff. And those processors, you know, you're going at like 8 megahertz or something with an 8-bit, you know, core or maybe 16-bit.

It's not really possible to do the kind of stuff you can do now with CircuitPython. That overhead of Python and all these awesome libraries was just too much to even consider. And then I think that started to shift.

You know, we started to go implementing all the arm cortex, cores. In fact, I remember my first chip that was kind of in this realm was the arm embed, the original, I think it was blue or something like that. Pretty cool chip. I didn't get that deep into it. It was a little above my level at the time. But all of a sudden, you started being able to have all this power. We're talking about dual core, hundreds of megahertz practically, and a 32-bit instruction set. And then you can start not worrying about it, right? You can start abstracting all of that.

starting to work with something like CircuitPython and micropython. What did I learn about it? Well, I knew about Adafruit from purchasing just Raspberry Pi stuff back in the day.

Especially, I really used to love the Pi Zero quite a bit. I still do. I really do.

If you need Linux and everything in a small form factor, inexpensive, et cetera, it's a great board. And they have the zero two now, I believe, which I haven't really played around with much. But I really like that point factor.

And I used to purchase some parts and stuff. but I didn't really get into CircuitPython until I discovered synthio, right? Thank you, Jeff.

I feel like every time I talk about synthio, I have to give him some kudos. Absolutely. Yeah, Jepler on Discord and so on.

So I had some experience, because I was always into synthesizers and stuff, and I had some experience with Mazi on the Arduino, which I think is still around, still supported. But that was definitely kind of designed for those 8-bit micro-controllers where you're really constrained within that space. And on top of that, like, having, adding in control logic, you know, driving displays, stuff like that, like, you start getting really limited.

And then when Synthio came out, I don't know, it was just really excited, be like, hey, I can just build a synthesizer, I can give it my notes, I can, you know, control some basic parameters. I don't really have to think about it. It all works in the background, and I can focus on what actually makes my project cool.

So I started working on some projects back then, but it was just kind of slow moving. That is until, I think, about 2019 or 2020 or so. Well, actually, not 2020.

That would be COVID. But somewhere in that time span, I'm from Pensacola, Florida, which is this little Navy town, you know, on the coast of the Panhandle of Florida. We don't have a whole lot of tech going on here.

There's not a ton of maker spaces or anything like that. It's pretty sparse. But all of a sudden, somebody roped in, I think it was UWF, our local college here, roped in Maker Faire and started a Pensacol mini maker fair and all of a sudden, you know, the lights are flashing. I'm all excited. Like, I got to do something with this, right? And they were inviting community members because I wasn't a part of the university at the time. They were inviting community members to contribute to this.

And I was like, well, let's make some music, right? And make it approachable. Because I know with a lot of these maker fairs, there's a lot of younger students, people that are just, don't know this whole world that we know, and they just want to see something fun and cool and whatever. And for that. So I started a project called the PicoSynthsandbox, which was supposed to be kind of like a do all synthesizer with microphones, touch pads, MIDI, a display, etc. that utilize CircuitPython.

So I put it on the back burner for a while, but that's something I'm hoping to revisit in the future. But it was a total success. A ton of kids had fun at that. I actually did two years in a row and I kind of expanded upon it. And I wish I had like some numbers here, like the number, students that came and interacted, but it don't. But it was a really good time.

Paul

You were part of the panel discussion in the recent episode about audio effects and shared that you have a background of music, which you've also touched on. What is your musical background?

Cooper Dalrymple

Good question. So I don't do as much as I used to do now. But back in the day, I used to playing a bunch of bands in high school and stuff. Always kind of loading myself out to whoever need help as well as doing my own music and writing and recording, you know, especially being kind of tech literate, I guess. If you're into music, you usually get really into the weeds and all the recording and the hardware and, I don't know, tweaking up guitars, things like that.

So I did that for a while. I had a pretty good band for a while called Crystal Coast. You know, we have a few music videos, that kind of thing. But we didn't really go too far.

But since COVID happened, it kind of shut everything down for me with that. I kind of had to reevaluate. And I found some other hobbies I was really interested in that were a little bit more, I guess, independent nature.

And so for music, what I ended up doing is I tried to go with this relic idea that I had, which you might notice by my tag on GitHub and all that kind of stuff, Relic SE or just Relic depending. But basically, I wanted to focus more on the synthesizer side of things. I wanted to create some electronic songs.

I had all these ideas. Once again, like I put everything on the backburn. I put this on the backburn a bit.

I'm going a little slower now, whereas I was really putting out songs for a while. And that was like on SoundCloud, nothing big. I only played one show so far.

I ask people every now and then if they need an electronic band. But that's not very popular where I'm from. There's not a whole lot of this kind of shows.

Sure. And fun fact here, the reason I came up with a name Relic, it's not because I'm 100,000 years old. It's actually for resistor, limiter, or inductor, sorry, capacitor, right?

I was like, I had this cool idea about, like, hey, the essential components of a passive filter. But now, right now, I mostly play drums. One thing I always like to say is once you learn how to play something like drums or bass, you will always play drums and bass.

Because every band doesn't have a drummer or bass. Everybody plays guitar. So as soon as you pick up those skills, that's the only thing you're going to be doing for a while.

So I mostly play in like metal bands and stuff like that on the side.

Paul

You recently started designing hardware to use with your music. How has the learning process been in designing hardware? It's been a steep one.

Cooper Dalrymple

I feel like with every design I do, I learn a new skill, which is really scary. Because when you create one of these designs and, you know, Kikad or Kikad, I guess, or Eagle or whatever, you're like, yeah, everything works. This is great.

My schematic's good. My hardware is good. So on.

Send it out to a PCB manual. and it comes back and there's problems. There's almost always problems. And I wish I could know where the problems were right from the beginning, but I don't. So I've kind of been leveling up.

Like honestly, I only learned how to do SMD like reflow soldering and stuff probably like two or three years ago. So for a while I was only designing through whole stuff, even then very limited because I'd always be scared. The whole process is scary. And when you're doing something as a one-off, I usually just, you know, perf board or do crazy wire jobs, and it's a mess.

I've since learned it's typically better to get a PCB manufactured if you can. You know, it's so inexpensive nowadays. It's really worth it.

It's just scary. That's it. So lately, I've been getting more, you know, my components have been shrinking and shrinking and shrinking to the point I'm finally starting to design stuff with like the RP 2040 and 2350 in mind.

that small QFN size with very specific capacitor placement, etc. And I can solder some of that stuff, I will admit. I have some experience with it. But I'm finally trying to do the assembly stuff with these PCB-8 manufacturers.

A, to save time, probably save costs, because it's always hard to source some of these components by yourself. And I don't know, just be better because I feel bad for the people I've, like, sold boards for and stuff in the past. Like, there's probably flux on them and, like, the solder.

job is just inadequate, but as long as it works, right? So tell me about one of the boards that you've designed. So I've done a couple.

Probably my most popular is what I call the Pico Prom. It was actually a project started by George Foot on GitHub, right? And he just breadboarded a Raspberry Pi Pico.

And you're going to hear me mention that a lot. It's one of my favorites. But it just a breadboarder to Raspberry Pi Pico to program E. prompts, which are electrically erasable, programmable, read-only memory, which are commonly used in old computers, like the Apple II, things like that, as well as game cartridges and so on, like the NES and SNS and so on. So at the time, I was actually really into the Atari 2,600. I'm a little bit of a masochist when it comes to programming sometimes, and I really like assembly code.

Like something about that, it's just so raw, and you're just, you're in control of everything. You're the that has to write every single little instruction that that CPU processes. It's just really exciting.

And the Atari was a great platform for that. So I actually made one game. It's called SpiderWeb.

Nothing special. It's kind of goofy, a little arcade game. But I wanted to actually create physical cartridges, right?

And so I needed to figure out a way to program these cartridges. And so I found that project, which is super simple. You know, the PICO has a ton of GPIO, and they're bidirectional.

You can really control them how you want. and so they literally just plug straight to this chip to program it, which is great for like if you're programming one or two chips and you're in a rush or something, but if you're like, I need to make, you know, 30, 40 cartridges, I got to program a lot of chips for that. You need something a little bit more durable.

So I took that design and I expanded it and, you know, added a few features, you know, rewrote a lot of the software to be a little bit more dependable and create a PCB for it and a case and everything, the whole shebang. And that did pretty well. I was pretty excited about that.

Other than that, I've done a few small, smaller little boards, like little chip adapters, things like that. I've been working on two other projects. My synthesizer, I mentioned earlier, the little sandbox, which, you know, at some point you have to decide when to stop.

And so far, I've done, like, four different revisions before even releasing anything. And I'm still not done. So, and then the other one is I've been working a lot, like you mentioned, the guitar audio, say.

guitar. The audio effects stuff with CircuitPython, I've been working on a guitar pedal design. That's kind of been my dream, right? It's to have a guitar pedal that you can just program how you want.

You know, I probably have a shelf of like 50 pedals over here that all do very different, very weird, bespoke things, which are really cool. But I feel like if I was starting out from scratch, I would, and, you know, I like tinkering with this stuff, et cetera. I'd really like a pedal that, okay, when you get it, maybe it's a delay, something simple.

But hey, I want to play around with distortion. I'm playing, you know, some Metallica or something. You want something a little different.

And instead of having to go off and get another pedal, hey, why don't we just upload this Python script to it? Boom, totally different pell. That kind of thing.

So I've been experimenting with that, and I'm on to my second revision.

Paul

So hopefully it's the last, but we will see. Nice. You've contributed to both CircuitPython and Arduino. What are the advantages to each that you see?

Cooper Dalrymple

You know, both environments are a bit of a means to an end. You know, with Arduino, to me, I really see that as bare metal programming, right? Like you, yeah, sure, you have a lot of libraries. There's kind of a uniform framework, and that helps you get started with certain chips, and you can port things between chips, where you can't necessarily do if you program specifically for one chip, you know, bare metal, whatever, within their SDK. So that's nice. And, you know, Arduino's been around forever. You know, back in 2012 when I was doing some of this stuff, I was coding an Arduino. And here in 2025, 13 years later, it's still around. And so there's a lot of information out there. However, I do find that the documentation, there's no standardized format, right? And the documentation gave it a little hairy, even, I'm sorry to say this, even with some of the Atifruit libraries, I find it a little bit hard to follow. And so what I end up doing, and thankfully, I have the knowledge to do, do this. I end up going to the libraries GitHub or whatever source code they're using and looking directly at the header files and just reading the C++ itself or C. And that's good. I can use that in a lot of cases, but I would definitely say for a beginner, that's pretty daunting. Doing basic stuff, blink and stuff like that, you know, not a problem, but when you get into weeds, you might as well be writing in the SDK for the hardware platform itself sometimes. However, I don't really poo-poo on Arduino too much. Except I will poop-pooh. Sorry, I don't know if that's the right word, on its IDE. I really am not a fan of the IDE. I feel like it has a lot of growing pains, and hopefully they make it better one of these days. I know there's V2 out already, and it's okay, but it's not my style. On the other hand, CircuitPython, anytime I want to just make something happen, I want to prototype something really quick, it is the way to go. There's so many libraries built into it that are at your fingertips that are dependable, a very good documentation.

I think that's one great thing they did, like with read the docs, making that the format across the board. Everything's written out exactly as you need it. Now, there's still room for, you know, more learn guides, more examples, you know, it's, when, do you know when Circa Python came out?

2017? Wow. Okay. Okay. Yeah. Yeah. So, I mean, there's still room for more examples, more learn great, but that will always be the case, especially as new hardware comes out. But that, the art, out of fruit supplied libraries, and even better the community libraries, just fantastic.

Everything's, I like what Scott does the, he has a name for it, where you're like the property-based APIs where like, hey, you're using a temperature sensor. Instead of, hey, dot, git temperature, you're actually just, what's the temperature, right? And that's really nice. I like that approach.

I know when I wrote my first libraries, it was hard for me to get a feel for that. But now that I really understand how all that works, it's very cool. And I like working in it quite a bit.

And also, on top of that, Circup, and I just learned about Circ firm, that tool. In fact, it was in the last, I'm sorry to date this, but it was in the last weekly meeting they mentioned it. I was like, I didn't even know that exists.

And it's just a quick, you know, command line to just install the firmware and upload any libraries, et cetera. It's awesome. Honestly, the device, even being used as a USB drive, super cool. So I'm actually taking some classes right now in a community college of mine, just furthering education, et cetera.

There's a student there that I've grown pretty fond of, and they're a little bit newer, you know, a little younger than me, and they have no experience in this. And I started introducing, like, telling about, like, how all this works. And we were in, like, a robotics class, right?

So they were just getting a hand of some of this. And anyway, I ended up giving him, an extra pico I had laying around and I was like I'm going to load this thing up with CircuitPython, put some a little blink script on there, just getting familiar with it. And it kind of blew his mind that you just plug it in and just shows up a flash drive and the code's right there.

There's no compilation, no nothing. And in fact, in the robotics class we were using Arduino and I remember it was so confusing when we first did it, he was like, wait, so I have to compile, it doesn't just upload to the board and compile there, you know? it was new to that whole workflow of having to compile things for a different platform beforehand and then uploading that firmware through the bootloader, all that.

It was too complicated, et cetera. Now, I think there are still some growing pains. I probably said that a couple times now with CircuitPython.

I know we're making the switch to Zephyr eventually, but I would really love to be able to use multiple cores. A lot of my programs, they typically have a core that's like for real-time processing, audio, stuff like that, and then another core for updating displays, handling controls. I'd love to be able to use that in CircuitPython, especially because you do have a little bit of overhead, and I think that would drastically improve on boards that can support those multiple cores.

Paul

Yeah, it'll be pretty interesting to see what Zephyr brings to the table once that's integrated.

Cooper Dalrymple

For sure. I'm excited. I know right now it's mostly focused on Nordic chips and some other stuff that I've never heard of But I'm excited to see what the process is going to be like when it moves to Sam D21, ESP 32, PICO, etc.

Paul

That'd be great. So we've mentioned the audio effects a couple of times. What are you working on next as far as audio effects go?

Cooper Dalrymple

I have to admit, I'm a little bit stale right now. I've mostly just been providing tweaks as we work towards the 10.X, you know, alpha and beta, just improving things on existing effects. However, I still have some long-term features I've been working on, but they're hurdles, for sure.

One thing that is incredibly important is bidirectional I-2S. You know, in case viewers aren't familiar, I2S is pretty much the standard, I guess, for audio data transmitting real-time DACs and ADCs and so on. There are other standards, PDM, or you could always just do PWM-out, etc. But for a lot of the projects that I want to do, I want to have audio input. And right now, that's very difficult within CircuitPython, just with the way that the framework is constructed.

I've begun the process of introducing some, you know, actual audio input that goes into the whole audio stream. So just like it is now where you can, you know, bring up a wave file or, you know, synthesizer and play that out through an audio output, you can do the same with real-time audio. But it's not great.

There needs to be some core changes, and I've done some of those changes, but I'm still dealing with some intermittent, you know, just issues. So right now there's a PR on CircuitPython with some of my work on that. That's just a draft.

I haven't touched it in a while, but I really need to, especially if I want to realize some of these projects I've been working on. And I think it's just cool. It's just really cool.

I agree. I've also been playing around with a lot of different audio effects in Arduino. In fact, the pitch shift effect I recently added to the core.

That was kind of one of the foundations of what I was working on there. And there's a couple other effects that we've been working on, you know, flanging, things like that, which aren't quite ready that I've been playing around with an Arduino that hopefully should be pretty easy to go in. I've also been wanting to streamline the entire effects system.

Right now, there's a lot of duplicate code. And I'm sure some of the other contributors aren't a huge fan of that because we're reducing that flash size little by little. So I think there's a lot of room to streamline that and save a lot of flash and make it easier for other people to add effects in the future.

You know, where you don't have to worry about all the frameworks so much, you can just be like, hey, here's my effect. Here's the properties I need. And here's the process.

That would be great. If anyone wants to learn more about your work, where should they go? So if you want to support my work, right now I do have a Tendie store.

I kind of took some notes from some other contributors to CircuitPython and put up some my products on there. And so far it's been cool, but I've kind of slowed down a bit. Some stock is, you know, I'm out of stock on a couple of my big products, which I need to increase on.

But there's still a few things on there if you want to check it out. But on top of that, for my music, I do have SoundCloud, which I'm sure will be shared in the description on this. And then for my just general stuff I'm doing, I do have a blog.

It's weird. There's like four different blogs on it for, you know, different projects I'm working on, my music. And then also just some old stuff I have up there.

It's probably not great. But, you know, better there than the way back machine. So that's generally how you want to get in touch with me.

I have contact forms, email, et cetera. I'll link to all of those in the show notes. Oh, I forgot to mention.

I do have a YouTube channel as well. I'm not as prolific now, but every now and then when I have a big product update, or if I CircuitPython libraries, I've been working on little projects. I do my own little show and tells on there sometimes and deep dives.

I'm taking a lot of keys from Attafruit on this one, but if you're interested in some of the work I do, that's where you can find it.

Paul

Last question I ask each guest. You're starting a new project or prototype. What board do you reach for?

Cooper Dalrymple

So I am a glutton for the pico. I got to say, you know, there's a lot of boards out there. but the Raspberry Pi Foundation has done a great job.

And they always have providing documentation. I was going to say supply, but I know there was a big shortage on pies a couple of years ago, reasonably so. It's just such a cool, little fun, inexpensive.

That's another thing. I'm very cost-driven. Because anything I work on, I want to make sure that I could take something like that to market at some point if I really wanted to.

And when you're working with a platform where it's like, well, it's 30, 40 bucks for this dev board, it makes it a little bit harder to recommend, you know, and potentially sell at some point. So the Pico is great for that. And I love the cast-laid pads where you can just plop it on a board and solder it down, make it pretty permanent.

It's just awesome. And I use some other Pico-based boards, you know, some of the add-a-fruit ones, some of the smaller form factors. But I just, I love that platform.

Paul

That's a great pick. Cooper, thanks so much for coming on the show. No problem.

Cooper Dalrymple

Thank you so much for inviting me, Paul. I really appreciate it. I love what you do here.

and I love listening to the podcast.

Paul

I'm looking forward to it. Thank you for listening to The CircuitPython Show. You can find links to Cooper's blog, YouTube channel, and Tindie Store in the show notes. And if you'd like to learn more about the new audio effects in CircuitPython that Cooper has contributed to, check out the panel discussion in episode 43. Until next time, stay positive.
