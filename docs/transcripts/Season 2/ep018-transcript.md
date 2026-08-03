---
date:
  created: 2022-09-19
title: "Episode 18 - Thea Flowers"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep018.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Thea Flowers.

Thea is a hardware and software engineer, with a broad skill set and deep expertise in developer relations and technical writing. It is Thea's mission in life to empower people of all backgrounds using open source software and hardware. Thia, welcome to the show.

Thea Flowers

Hi, thanks for having me.

Paul

How did you first get started with computers and electronics?

Thea Flowers

Oh, gosh. I have always been a bit of a tinker. You know, I was the kid that would just take things apart just to figure out how they worked.

It's always been how my brain has worked. I've always been curious about how things are put together and all that stuff. But I really got interested in computers and programming and stuff when I was in my early teens because I wanted to make video games.

Paul

How did you first discover CircuitPython and eventually become one of its maintainers?

Thea Flowers

A few years ago, I started. started looking into making my own MIDI controllers and stuff like that. And I played around with Arduino before and that sort of stuff.

But it just so happened that right around the time that I was starting to kind of get back into making hardware, that CircuitPython was kind of taken off. And it made me really excited because I've been programming in Python for most of my life, I guess. And I was just like, this is great.

It's such an approachable way to jump into microcontrollers. And when I eventually decided to start my own music technology company creating synthesizers and stuff, I really liked the idea of having a product that someone could reprogram without having to install anything on their computer or having to learn a lot of complicated stuff. They could just plug it in and it shows up as a little flash drive and they can edit a file and it immediately starts running again.

And I built two products around that concept. And in the process of doing so, I learned a lot about CircuitPython and ended up contributing a bit and becoming one of the maintainers. I am currently rather inactive, but I have a few products that I want to bring to life with CircuitPython once the chip shortage has chilled out a little bit.

And I'm excited to start touching CircuitPython again, more in depth than I have before.

Paul

That's exciting to hear. So you mentioned your synthesizer company. Tell me a little bit about Winter Bloom. How did you take that from a side gig to being able to work on that full time now?

Thea Flowers

It's been a bit of a journey. So I started Winter Bloom in 2020, in March of 2020, which might be the worst possible time in history to start a company. It was tough going at first. And thankfully, I still had my day job then. And it really just started around me wanting to, wanting certain things to exist.

right? I was like, you know, I was getting into modular synthesis. I was like, wow, I really want this kind of module to exist. And it just so happened that CircuitPython was around and I was getting up to speed with that. And then, yeah, it just made sense for me to sell the stuff.

You know, I started with like an order of maybe 30, 30 modules. And I didn't expect to sell any of them honestly, but no, some of it really resonated with people. And since then, it's really kind of, you know, taken off a little bit and, you know, enough for me to sort of make it my main job, which is, which I feel incredibly lucky for. Well, that's great to hear. What was the first product

Paul

that you brought to market at Winterbloom that actually used CircuitPython? Yeah, so we actually

Thea Flowers

launched two at once. And the first one that I designed was called Sol, so that's SOL. That's SOL.

like our sun. And it is a USB MIDI to control voltage module. So basically what that lets you do is it led to use your computer or any other MIDI compatible equipment to talk to your modular synthesizer.

Because modular synthesizers speak in analog voltage and translating that is non-drivial. But Sol was able to do that. And it did it using CircuitPython, which meant that you could customize the way that it handled that conversion to get it to do all sorts of really interesting stuff.

So, you know, there was like an out-of-the-box experience that was generally useful for most people, but you could easily go in and remap it and change how keys are translated into notes and how knob turns are turned into other things. And it's just, it's really interesting. And it's amazing to see what people have built with it.

Like, people have built special scripts first sold that work with specific digital audio workstation. which I think is really cool. And the other product that we launched at the same time is Big Honking Button.

And it's possibly my favorite product, if not second favorite product. But it is exactly what it says. It is a big arcade button that when you press it, it honks.

It is a module for a modular sense. So it's designed to fit into the whole modular format. And it's such a wonderful product because it's actually kind of sneaky.

because it seems silly on the surface because it's a button that honks. But underneath, it's running CircuitPython. And you could control how it treats its inputs and outputs.

So you could make it where it changes the pitch of the honk that it's playing. You can change that honk to an actual useful sample like drums or something. You can have it generate all kinds of different sounds if you want to.

And it's a really useful and powerful little module that is, as disguised as this absurd, ridiculous thing. And I think that that's really wonderful.

Paul

I agree. When I was researching this episode, I came across that and I'm looking at it and I realized what you could do with it. And you've got example code for it as well. So it's easy for people to jump in and actually change things. And that's easily become the number one thing on my wish list from Winterbloom.

Thea Flowers

That's awesome. Yeah. And honestly, CircuitPython was such a huge enabler for that.

I mean, both from just the coding experience. but also just like for a lot of samplers in Euro rack, like the way that you load more samples onto them is like you have to take a tiny SD card out of the back of it and plug it into your computer and, you know, hope that you got the files in the right format and everything. But with big honking button, you plug the module itself into your computer and there's the drive and then you just, you know, you can drag new samples over and test them immediately.

And I think that that alone was worth it for CircuitPython. but the whole experience of being able to change the code as easily as you change the sample is wonderful.

Paul

Now, I know it doesn't run CircuitPython, but tell me about Castor and Pollux.

Thea Flowers

Yeah, so Castor and Pollux is really part of my deep love for the 80s and the synthesizers of the 80s, specifically in this case, the role in Juno 106. And it is basically a reimagining of the way that the Juno makes sound. and it's adapted and changed and modernized for modular synthesizer specifically.

It kind of takes the core idea of the Juno, and it doubles it, and then adds a bunch of weird stuff in between, which is really wonderful, I think, because it isn't just the straight copy of what was done before. It takes that, and you can get that same sound, but you also have so much more that you can play with, and you can explore those concepts in a much deeper way with Castor and Pollux. And it just, it sounds wonderful.

It really does. I am still amazed when I plug it up and play around litter, when I watch videos of other people making wonderful sounds with it. It just sounds so good to me.

And I'm very proud of it.

Paul

Long-time listeners know I'm a big record collector, and I used to describe my collection as a third 80s music that I grew up with when I was a kid and a third indie music and a third of everything else. some of that 80s music what would people recognize that synthesizer on? Are there some bands or albums that come to mind?

Thea Flowers

So, so many songs. One of the ones that's just so easy that everybody knows off the top of their head is sweet dreams about the erythymics. That synthesizer intro and the bass line throughout the song, that is the Juno. That is a very pure Juno sound. And yeah, that's one of my favorites and tracks.

Paul

That's a great example. Before we go, I have one last question that I ask each of my guess. You're starting a new project or prototype. Which microcontroller do you reach for?

Thea Flowers

So I am famously, or maybe infamously, a huge fan girl of the SAMD21. It is, to me, the perfect sweet spot for a little microcontroller. It's reasonably fast. It has a good amount of flash, a good amount of RAM. It can run CircuitPython, so you can prototype pretty rapidly with it. And it has just, just, just incredible peripherals.

It has six flexible serial interfaces that can be spy, I-squared-C, U-R, it has up to 20 80C channels, and it has a DAC. And you could do a lot with that, right? That is a lot in one little package, and it is so reasonably affordable.

I really think it is just one of my favorite chips that has ever existed. So that's what I'm reaching for. And you can find that on the Adafruit like feather M0, the Arduino Zero, and the Sparkfund thing, all have the Sandy 21 on them.

Paul

If people want to learn more about WinterBloom or follow you online, where can they find you?

Thea Flowers

So they can find Winterbloom at Winterbloom.com. That's Winter like the season and Bloom like a flower. If they want to follow me on Twitter, I am at Thea Valkyry, and I apologize in advance for anything that I may post on Twitter. but you got to be warned about what you're signing up for.

Paul

You never need to apologize on this show.

Thea Flowers

But yeah, that's where they can follow me.

Paul

Great. Thea, thanks so much for your time today.

Thea Flowers

Likewise. Thank you for having me.

Paul

Thank you for listening to the CircuitPython Show. For show notes and transcripts, visit CircuitPython Show.com. Help keep the show ad-free.

Your financial support helps cover the costs of recording, hosting, and transcriptions. Learn more at CircuitPython Show.com slash support. And check out my new show, The Bootloader, with my co-host, Tod Kurt.

Each episode, we will share news, projects, and other things we found interesting. Search for The Bootloader and your favorite podcast player, or visit The Bootloader.net. Until next episode, stay positive.
