---
date:
  created: 2026-05-04
title: "Episode 59 - Tom Fox"
---

## Show Notes

[Show notes available here.](../../episodes/Season 7/ep059.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode I'm joined by Tom Fox. Tom is a teacher, creative technologist, musician, and artist, who specializes in human music interaction and exploring physics and electronics to create new musical devices or interfaces. He runs Acoustic, a London-based group that specializes in showcasing musical innovators and makers and have showcased other people's work through curating events at locations like Tate Modern, VNA Museum, Royal College of Music, and Abbey Road Studios. Tom, welcome to the show.

Tom Fox

Hi, Paul. Thanks for having me.

Paul

How did you first get started with computers and electronics?

Tom Fox

I first got into coding and computing when I was very young. Our home computer was a BBC micro. So it ran basic. If you wanted to play a game, you would have to write it yourself. I really enjoyed it. My dad was always very into computing. So, I mean, this was back in the late 80s, early 90s. And then it sort of dropped off for quite a long time. And then later on, when I started making things, I was building musical instruments. And I wanted to add a bit more interactivity to it. So it really, when I came back to coding, was when I was starting to build interactive musical installations. And that's when I sort of rekindled my passion for coding, electronics and that kind of stuff.

Paul

How did you discover CircuitPython?

Tom Fox

When the Raspberry Pi Pico got released, so I remember buying the magazine, which had the Pico on it. And at the time, I was building, I was using a lot of Raspberry Pi projects in my work. So I had some quite advanced coding things using, like, Twitter APIs and all of this stuff. And I was using Arduino at the time, but I never really quite, I didn't enjoy using Arduino. There was always a bit of a struggle for me. And then I got the PICO and then I think a bit later on, they ported CircuitPython for the PICO and everything was so simple. And it could do basically anything that I wanted it to do. And I mean, I've been sold ever since. For me, it's the easiest language or coding language to use. And for the various projects that I do and for when I teach as well, it's always my go-to code. If I can't do it in CircuitPython, I will find a way around it. I love it.

Paul

In 2025, you ran a successful Kickstarter for the SPOKE board. What is the SPOKE?

Tom Fox

So SPOKE is a capacitive touch board. It's a piece of hardware that turns any kind of conductive object or material into a computer input. So it has 27 different inputs, and it uses true capacitive touch, not resistive, touch so you don't have to be holding a ground plane or anything you can just touch different sensors my background has been in like education and workshops and like public facing events where we've used other boards like makey-miki and the bare conductive boards and all that kind of stuff and i've used all my knowledge of using those kind of that kind of hardware in those different settings to make this SPOKEboard as easy to use as possible. So there's lots of different things I've put into the design and also the code side of it so that the barriers to access are super low. You don't need to know anything about code in order to get it working, but then you could use it to start learning to code or start debugging or start getting into the nitty-gritty and go, oh, this kind of makes sense, hopefully. I mean, yeah, it was, the Kickstarter was successful, and we're now going through Pimeroni, who are a maker company based in Sheffield here in the UK. And yeah, it runs on Second Python because it has brilliant native touch I.O. libraries just in the build. So again, that just makes making this board so much easier.

Paul

You mentioned that you don't have to know code to use the SPOKE. Who would you say the SPOKE is for?

Tom Fox

I'm aiming it to be for anyone. So it comes as a USB device. I've made a custom UF2 that I'm already put on there. So it comes with the MIDI libraries and the HID libraries. And it's got a bunch of neopixels on it so that when you touch your sensor, a light next to the sensor shines, which is a really simple but really powerful sort of feedback tool for using this in like workshop settings. So it's complete beginners, could plug it in, make some fun noises. I've got some web-based tools for like making sounds or for playing games or even editing the code. But then it's also at the far end, you can get into it. It's basically, it runs on the RP 2040 chip by a Raspberry Pi. So it's the same chip that's in the Raspberry Pi Pico. So if you wanted to get really deep into the tech, you could if you knew how. I've added some sort of stemmer connectors to it as well. So if you wanted to add I2C devices or if you wanted to daisy chain a whole bunch of them together or access for PWM stuff, then you can do that as well. So it's for beginners and experts and sort of anyone in between is, that's my target.

Paul

In addition to the SPOKE, you've also created the SPOKE mini. How is it different from the SPOKE?

Tom Fox

Yeah, cool. So the SPOKE Mini is basically a blank PCB that makes connecting to the PICO really easy. This project kind of came about when I was playing around with Pico and playing around with CircuitPython. And for my own uses, I wanted to find an easy way to build some interactive installations. So I was building these instruments that were basically little miniature models of buildings and landscapes and stuff. and you would touch bits of the landscape to play music. And that's when I found that all you need on the Rajpupai Pico to turn one of the GPIO into a capacity of touch sensor is a one mega on resistor. And that's it. There's no extra shields or extra circuitry. It's one resistor per pin. So when I first discovered this, oh, this is actually really good. I wonder if it would work on every pin. So I breadboarded 26 resistors to the 26 GPIO, and it just worked perfectly straight away. It was a real like, oh my God, this is incredible. I made the PCB for the mini version so that you can basically assemble it yourself, and then that could be embedded inside projects on a more permanent basis. But I've been using it in my classroom this year to teach my pupils how to solder. So they basically made their own capacitive touch hardware, learning how to solder, learning how to put second Python onto the pico like flash in the firmware. And they've made some incredible things with it.

Paul

So for both the SPOKE and the SPOKE mini, you've mentioned that you've got a class and you've shared it in workshops. Have the students surprised you with anything they've made with the SPOKE?

Tom Fox

Yeah. So one of my pupils, she's made a. a bird house and the different touch points are like different leaves and like very like jewelry like pendants which we sold it wires to and then they became like she made just like really amazing like little art piece and like you touch the leaves and the feathers on the birdhouse and it would play bird sounds got one pupil who's making his own oboe he's made like a select he's got like a hard cardboard tube and he's putting the touch points on the outside so that he can hold it like an oboe and it might be like a MIDI instrument. It was used actually at Kingston University for, as an amazing professor called Leah Cardas, and she really wanted to use this for her university students. So I got them a bunch of prototypes, and they built some incredible things with it. One group made an interactive installation where you would touch bits on like the whole soundscape of the room would change. One group made an accessible instrument for kids with like tactile, how sensory sounds. So they built like a tree that was like flat and different parts of a tree would trigger music. And another group of students, they did something with it, which I didn't realize you could do, which is they connected it up to like coffee mugs full of water. And then when they dipped like a spoon in the water, like you're like mixing tea, it would play a note. Because obviously you're changing the capacitance. And so they did a cover of massive attacks teardrop, just using stuff around the kitchen.

Paul

That's ingenious.

Tom Fox

Yeah, yeah, it's so good.

Paul

What were some of the challenges you had to overcome to bring the SPOKE to life?

Tom Fox

Yeah, it's a good question. My main challenge was time, I guess. I'm a full-time teacher. I also run events in London. I also work for a company in Sweden called Music Tech Fest. So luckily, for circuitry, is fairly simple. So there have been lots of iterations and the team at Pimeroni have been just incredible like actually getting the circuitry to a point where it's like manufacture ready. So like prototype ready is one thing but actually doing like a big bulk run of it is a lot more different than I expected. So they've been a massive, so there's been lots of backwards and forwards of like time. tiny changes and stuff like that. So, I mean, yeah, I think time is the biggest issue. But it's, I mean, it's, it's been worth it because it's been, it's already being used in incredible places by incredible people. What I love about it is that they're finding things it can do, but I didn't know it could do. So that's, it's been really, really exciting.

Paul

You mentioned the online SPOKE CircuitPython editor. Tell me a little bit more about that.

Tom Fox

Yeah, so one of my main focuses for this whole project is about removing barriers to access. So one thing I have found in my own classroom is, like, the IT department, I'm always happy about, like, uploading new IDs to their computers. If you're going to start messing around with, like, Python, that's if you get really, really clever kids who know how to exploit that, then that puts the whole schools network at risk. So I'd seen a few different online browser-based idees for Cycopithon. I thought, that's incredible. I'll link to those, and then that will solve all my problems. But then one of the other things I wanted to do was to make it super easy just to find the different examples and stuff. I jumped onto Claude, and I gave it some prompts, and went back and forwards, blows. And it took a while. It took a couple of days of, like, actually getting it to do what I wanted it to do. But then now there is a SPOKE specific online IDE where you can change the code. You can load up different examples of different things I can do. You can do, like, melody generators if you're building a musical instrument. It's got example code for like games controllers because a lot of it has been MIDI based because I'm a musician. I use MIDI a lot, but it can also just use for HID library and be a keyboard and mouse. So there's like you can play Minecraft on it. You can key map commands, consumer commands. So I had one pupil who wanted it to have like different buttons, like shortcuts for like copying and pasting and locking the screen or I had print. screen and stuff like that. So there's example code now on the browser so that you don't need an IDE, you don't need to download any software like Fonnie or MU editor if your school happens to not need that. Or if you're in a workshop and you get participants to bring their own laptops, they don't need to download extra software. They can just do it from the browser. So again, it's about making it easier to get into an issue gritty. You can still use whatever IDEe you're used to, but the web tools just make it that much, just a little bit easier, which I think is really important to introduce people to this world, because I think it's quite important. That first step into this kind of world needs to be quite an easy one. We don't want to intimidate people to say, you're going to learn code, but first of all, you need like a degree in Python. That's not how you get people to get excited about this stuff. right we don't want them throwing up their arms up in the air and just walking away because it's too hard exactly yeah there's a fine line between like inspiration and complete boredom or frustration like inspiration and frustration there's like a fine line i found and i'm just trying to keep it on the line of inspiration rather than why isn't it's working what's next for the SPOKE hopefully by the time this episode comes out it will be on sale primarily um i've been it's been So many delays. Actually, straight after this, I'm going to call them up just to say, what's going on? But yeah, it'll be available there. I think this has got like a global reach and has a huge educational, educational value. So I would really love to start doing training with teachers, workshops for people. It was just there was just a hackathon done at Berkeley Music College with some of them. And they loved it. So they're quite keen on doing some more workshops with it. Also, I'm really excited to see where it goes. And I'm really excited to see what kind of stuff people build with it because that then feeds back to inspire more people to, oh, this is cool. I want to do that. So yeah, it's a combination of working out how to do this full time and then also keep just building the community of makers and builders.

Paul

If anyone wants to learn more about you and the SPOKE, where should they go?

Tom Fox

Any of the socials. My tag is SPOKEboard. SPOKEboard.com. And then my personal one is Volpesinstruments. So I do have other projects that aren't just SPOKE related. I do lots of creative technology installations and artwork pieces.

Paul

I'll make sure I link to those in the show notes.

Tom Fox

Thank you very much.

Paul

And you said it'll be available soon on Pimoroni. How much will it go for?

Tom Fox

The main boards will be 40 pounds, which is, I think, a reasonable amount.

Paul

Last question I ask each guest. You're starting a new project. Which microcontroller do you reach for?

Tom Fox

Oh, the PICO. Easy. Straight away. Not yet for Pico 2, because for Pico 2, silicon can't currently handle capacitive touch stuff. I heard rumblings that they were going to change that. But at the moment, the Pico 1, yeah, it's my... my go-to.

Paul

It's a great pick, especially the performance for the price.

Tom Fox

Oh, yeah, yeah. I mean, in my classroom as well, I use it in the classroom because it is so affordable that they can build a project around it and then take it home. Whereas, like, other boards, I would need a much larger budget if that were the case.

Paul

Tom, thanks so much for coming on the show.

Tom Fox

Thanks so much for having me. It's been a pleasure.

Paul

Thank you for listening to The CircuitPython show. For detailed show notes and transcripts, visit www.circuitpythonshow.com. Until next time, stay positive.
