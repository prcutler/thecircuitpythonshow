---
date:
  created: 2022-10-31
title: "Episode 21 - Jason Pecor (and the Trolls)"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep021.md)

## Transcript

Paul

Welcome to a very special Halloween episode of The CircuitPython Show. I'm your host, Paul Cutler. I took the show on the road this episode as I traveled two hours east from my home just outside of Minneapolis, Minnesota.

I met up with Jason Peacore, a Valorium technology, who introduced me to the trolls. Jason and I are outdoors at a park, so you'll hear some background noise, and I'm a little too far away from the microphone. Sorry about that.

Also, you may want to check out the show notes and YouTube link at CircuitPythonShow.com for some photos and video that I took as well. You'll meet Jason and the trolls right after this word from our sponsor.

This episode is brought to you by PCB Way. With over a decade of experience, PCB Way is one of the most experienced manufacturers in printed circuit board prototyping and design. Whether you're an engineer, student, or hobbyist, PCBway offers a simple and fast prototyping service, and it's cost effective at only $5 for 10 boards.

And check out PCBway.com where PCB way helps makers and hobbyists collaborate on their designs and projects. Make your design a reality and check out PCB.com for all your PCB needs. And they also now offer CNC machining and 3D printing services.

Visit PCBWay.com for more information. Thanks to PCB Way for their sponsorship. Jason, welcome to the show.

Jason Pecor

Thanks, Paul. Appreciate it. I've been looking forward to something like this since you started your show, so I'm really excited. Thanks for having me.

Paul

I'm glad I could come on site and I wasn't too far away.

Jason Pecor

Yeah, it's great. Knowing how close you were in Minneapolis, I was like, if he could come on site, this would be really, really fun. It's a pleasure to meet you.

Paul

Tell me how you got started with computers and electronics.

Jason Pecor

Let's see. Well, when I graduated from college, I went down to Cedar Rapids, Iowa, and worked for Collins down there and worked in a GPS group doing GPS, actually, simulators, and then moved into FPJ and ASIC design group down there, which is how I got my feet wet doing that. And that was in Cedar Rapids.

And then after a few years, I came back here to O'Clair, Wisconsin, which is the area that I'm from originally to go to work with an ASIC design services company. And we did primarily, I was a verification engineer on the design services side and did that for a number of years. And we did a lot of stuff in the networking space, high-end networking, supercomputing, things like that.

And our company went through a handful of acquisitions over the years like most companies in the high-tech space do. And the last one kind of ended in 2013. We were part of a company out of the Silicon Valley called Open Silicon.

And they went through some bumpy times, ended up shutting our design center down. So we started another company called Superion Technology in 2013. And at that time, I'd kind of moved mostly into doing business development type of stuff.

I still like doing the technical side of things when I could, but mostly responsible for business development and marketing, that kind of thing. So we continued doing the ASEC design services work. But around 2015, we had this idea to do a product, and we saw the whole Arduino thing coming alive and the whole maker movement.

And we thought, man, it'd be really fun to do something. in that space that tied in the FPGA side of things because that 8-bit micro on the Arduino is just underpowered for a lot of stuff. And we saw people trying to use it for things like motion control and servos and motors and thought this would be a great place for an FPGA. And we came out with a board called Accelerate, which was our first product, which is based on a max 10 FPGA from Intel. It's got an embedded 8-bit micro in it, AVR compatible, fully programmable with the Arduino IDE. And we launched this company called Ellorium technology at the time just to change the branding to not confuse our AIC design services customers. And that was really the beginning of this. And I came out of the world of doing the electronics hands-on and doing the chip design stuff to business.

But then when we started Allorium, I couldn't resist getting my hands back into the hardware, specifically for our demonstration videos and things like that on YouTube. So I would write code and hook things up. And that's kind of how I got back into getting my hands on to hardware and writing code with the Allurem technology hardware.

Paul

How did you discover CircuitPython?

Jason Pecor

Oh, man, CircuitPython. So I think I got into CircuitPython around 2019 or so. I think that's right. Maybe late 2018, maybe early 2019. What I know is this is at the time I got involved, Lady Ada was still lurking around the Discord server and actually answering questions. And you don't hardly see that anymore. So it was a while back. And because I had a few questions where she just directly answered. And I used a lot of AtaFruits stuff already. We used a lot of it in, even with the stuff that I would use with our hardware, I was buying Adafruit accessories, like the, I love Neopixels, some of the other hardware they have. We were using those already. And so I just was naturally tracking with what ATAFruits are doing. I think I'm a big fan of Adafruit. And I think Lomor is a genius.

technically, and I think that Phil is a genius in the marketing world. And they're just super fun to watch, not only as a consumer of their products, but as someone running in electronics business, there's a lot to learn from what they do. So when Circa Python came along, I'm like, this is great. I like Python anyway. I had designed some stuff in Python just on the side for my own stuff, and not in the micro world, but just for some amount in raspberry pies. And so I naturally found it through that progression. And I think the first thing I ordered was like a Metro M4 Express, I believe.

So again, Arduino Uno footprint, but with the M4E. And it was right around the time Pi Portal was being designed, is when I kind of got involved with it. So that was one of the first pure, like, really exciting purchases I bought was the Pi Portal.

Paul

So I'm standing here in a park. We have a bubbling brook behind us. Right. And I'm looking at three trolls.

Jason Pecor

Yes.

Paul

Tell me about these trolls.

Jason Pecor

Sure. Well, these trolls are an interactive art exhibit that the city of El Tuna commissioned in originally in late 2019, I think early 2020 was when we first got involved with it.

And the idea was to create something that kids could interact with that would be touchable art that they could play with. And there's a designer in Sweden that specializes in interactive children's art displays and artwork and sculpture that they found, I don't know the story on that. But then they started working with a local fabricator to do the metal work and the actual design of the structures.

And that's how I got connected and how we got connected on the electronics. So what these are, and I'm going to walk here in front of your camera, if that's all right, and you're going to see my microphone because this is what we got to record with today. But what you see is there's three trolls, and you can kind of stand in the middle of them.

And every one of these trolls has four panels on it that will activate audio and turn the lights on. and so what we've got is, so I'm going to touch this one, because I know that this is one of the things. So the hammering in the background's construction, that's not coming through the trolls.

But what will happen, there's four panels on each one of these that when you touch them, it enables a signal, it enables an audio track, the eyes light up, and altogether there's a total of 12 tracks with this consistent audio, and all the audio was recorded by the designer, one of his partners in Sweden. They're very culturally correct for kind of the lore around the trolls. And so if you have all 12 being touched, you get this 12-track audio piece that plays.

It's about 30 seconds long or something like that, and it just continues to loop. And the idea is the kids can come down. They can search for the touch panel that plays the audio and that lights up the lights.

And it's a huge, huge hit with the kids. Kids love coming down here and playing with it.

Paul

We've already seen one group of kids come and play. and we're here today about a month into the school year, so not a lot of children around. Right. What's it like in the summer?

Jason Pecor

Man, in the summertime, it's really fun. Every Wednesday night, there's a concert series here in the park in the evenings. And my wife and I like to come down.

We listen to the music. I like to walk around and see it happening because there are kids just lined up everywhere. Everyone's touching it.

They want to play with it. They're playing games and things like that. Of course, the panels are the same.

They've been the same the last two years. And so the kids that know it, know it, right? They know how to get to it and they know which ones, but there's always new kids and they're teaching them how to play with it.

We see adults coming down and checking it out, and it's a really fun thing to watch them play with. Yeah, it's very popular. Some of them like to kick it. If you look closely, you know, you can see shoe marks on there.

But I think it's really a testament actually to Artisan Forge is the name of the company that designed the structures. And this is all anodized aluminum on the faces and steel all around it. they're extremely robust physically for sure.

Paul

Well, they're going to have to be to survive the Wisconsin winners.

Jason Pecor

Right, right.

Paul

Tell me about the CircuitPython gear that's inside here.

Jason Pecor

Okay. So CircuitPython was absolutely instrumental in the genesis of this idea because when I got contacted by the owner of Artisan Forge, he told me about the concept, told me how it needed to do. And the original designer from Sweden had kind of an idea of how it would work, but didn't have the electronics background to really know how to do it.

And the first thing I thought was touch, play audio, light, lights. I mean, it's the ATA Fruit world, right? It's the CircuitPython world.

It's blinky lights. It's things that move. It's things that make sound.

It's interactive. And I just happened to have a circuit playground express on my desk. And so I grabbed that and I hooked it up to a little tiny speaker that I had just this little really small battery powered thing.

And I put a few sound effects on there. and I walked into his office to talk to him about, and I said, is this what you want? Something like this only on a bigger scale.

And with just a few lines of CircuitPython code, I was able to demonstrate, touch the touch thing, it plays some audio, he gets all excited, right? Lights up the little light on the board, everyone's excited and happy, and then it just scaled from there.

Paul

Now, did they have different ideas that they wanted to do before CircuitPython?

Jason Pecor

So I brought in this little Circuit Playground Express demo, and it was really based on a description original designer had done. But his idea involved more like really expensive synth modules and other control things and MIDI stuff running around. And that's still left open. Like how are you going to detect it's being touched? There were some other ideas that they had based on talking with people kind of in the industrial controls world. So using PLCs and very expensive solution. And again, when I saw it, I thought this is this is a perfect fit for these kinds of electronics. And when I was able to just so quickly show up with this thing working. And again, it's, I mean, it's no genius on my part because the libraries are there, the hardware's there, everything's there. It was just sort of being able to think through, well, I could just stitch this stuff together and just respond to a touch and play in audio. So, I mean, all the pieces already existed. It was just putting them together to create the right picture with it that did what they were looking for. So what are those pieces that you're using to actually do it? Sure. There are, so each troll has a box in it that handles the input from the touch sensor and lighting up the lights. And that's a, that's a feather M4 Express and then a touch sensor breakout board is got is in each one of these. And those are all running CircuitPython. So those detect the touch. So I think, if I'm remembering correctly, I think it's a spy connection or is it I squared C. I can't remember which one to the touch breakout. And then I think it's spy. So spy back and forth to the touch sensor breakout. That detects the touch communicates to the feather, which lights up the LEDs. And then those each send, signal back to a main troll.

So one of the trolls has kind of got the main. This one's the main troll. This has got not only a similar M4 Express running CircuitPython to detect a touch and light the lights.

Those all talk to a fourth Feather M4 Express that is running, that one's not running Circa Python. That one's actually running Arduino code. And that one is communicating with the board that's doing all of the audio, which is another board.

It's a tsunami super wave trigger.

Paul

And what does that do?

Jason Pecor

The tsunami super wave trigger is a spark fun board that is specific for playing audio and doing MIDI stuff. But what's awesome about it is it can handle, like I've got 12 tracks of independent wave file audio running on that. That as soon as this powers up, it plays all of those at the same time in sync.

And it just turns the volume down on all of them. So as you touch each panel, I can independently turn the volume up on every one of the tracks. So as you add panels, you can hear the different audio playing for all 12 tracks.

Paul

Let's take a moment and play some of that audio. So people can get an idea.

Jason Pecor

I'll do this one. It's tough to get all four. That's the part that makes it really fun with kids because one child can't touch all four panels at the same time.

so they kind of have to work together. So that's why you get a group of kids around here to get, if you want to get all 12 tracks playing at the same time, you need a lot of kids. At least six, right, to get them going.

And so it makes it a lot of fun. So there's a lot of CircuitPython running in here. Each one of these has a feather running CircuitPython.

And then there's another feather running Arduino code to handle the communication with the audio board.

Paul

So for folks who haven't been to Wisconsin, it can get hot in the summer and it gets cold in the winter. Yes, right. How have these survived the climate?

Jason Pecor

That has been kind of an interesting part of the journey. And we've experienced troubles with both, I think. And the first one was really this spring.

I showed up this spring. So these get powered down in the wintertime. I mean, it's just running on a battery.

There's a solar charging station here that's powering a 12-volt battery, and that's what powers the whole system. So there's a marine amplifier in there and speakers, which is how the audio is running. So all of that's being controlled by that, and all the electronics are being controlled by that battery.

And the battery gets charged in the summer with the panel. So they shut it down in the wintertime. And then this spring, when we came to, when they powered it back up, I got a call that, hey, they're not working.

Something's weird. And I generally can tell, because I know the architecture of the thing, it's like, well, if I do this and it lights up but doesn't play audio, I mean, it kind of get a vibe for what's probably wrong. These didn't make any sense what was going on.

What we ended up doing was took the faces off, got into electronics, and just the board wasn't behaving. It was weird. It wasn't right.

And it had been out here in this all winter long. It gets really cold, right? Below zero.

You get January, February, you have strings of days that are 15, 20 degrees below zero. And these parts aren't industrial design parts, right? They're just commercial grade stuff.

So we are asking a lot of this hardware. And it has performed magnificently, honestly. All I did in the spring was I had to reinstall.

CircuitPython so i actually got up to the most i moved to version seven or i can't remember what version i went to upgraded some libraries put the same code back on and and also just reprogram the arduino one just for a good measure and then everything just worked just worked and it worked all summer with no issues it's really funny because paul you and i had scheduled this time and i'm not i'm telling you like two days after we scheduled learning to get together i got a call that one of the trolls is experiencing some issues what i think happened in the winter it was just it's really cold, and I'm not a devices guy. I don't know enough about ICs and stuff to know how all that works or flash memory, but my guess would be it got cold enough that some bits flipped somewhere in the memory, in the flash that's on board that thing, and it just didn't work. As soon as we reprogrammed it, everything worked.

Now, people out there that know how this stuff works probably laugh at that hypothesis, but I don't know. Something weird happened, and it happened after winter, so who knows what it was. The summer one, there's this one troll here, that this, we call him the blue troll, he's kind of bluish gray. You can see the sun shining on it right now. This gets full sun pretty much all day and in the afternoon really, really bakes. And this is the one that stopped working about two weeks ago. Came down, did some testing, tried the whole reprogram approach again, and that didn't work. I don't know what's going on. When you power up the M4 Express, the lights just come on all the time, which doesn't make any sense because that's not what it should be doing. There might actually be something going on in the neopixel rings. Oh, that's more Adafruit stuff, right? Each one of these eyes has a small, I think they're the seven, or I can't remember how many are in the little tiny ring. Each one of these has a little neopixel ring behind it that turns on. It might be the I see's in those for all we know, but there were some other things not quite working, right? So we pulled the control box out of that, figure that out over the winter.

It wouldn't surprise me if just the heat from this did some damage. I mean, this thing's out here summer long, but it went from May until middle of September with not a single glitch, and these things get used hard all the time, all summer long. So I would say we're expecting a lot from these electronics for what was completely an experimental concept and design and implementation.

They are working fantastically. And we may need to do some things to figure out how to mitigate the environmentals, but otherwise, we've been super pleased. The city of Altoona loves it.

They love it because it's a great attraction. And CircuitPython's running right at the heart of every single one of these. So really cool.

That's awesome.

Paul

Yeah. Before we go, I have one question that I ask, each are my guess. Right. You're going to build a project or a prototype. Which board do you reach for?

Jason Pecor

My go-to board on the Circu Python side is a Pi portal. It's sort of my original love. You know, like it was the first thing I bought that was just purely CircuitPython.

And I love the UI piece of it. So there's something, it's a little bit I-O-bound. So if you're going to do a lot of things that have a lot of I-O, it's not the best solution.

But most of the time I'm not. You know, I'm doing something with I-squared-C or one or two outputs, and it's internet connected. If you can do, you can touch the screen.

You can do a, I think it's a fantastic device. I love, love, love the Pi Portal. And I keep waiting for an excuse to buy the, the giant, what's the big one, the Titanic?

Titanic. Titano, yeah. I haven't found a good enough excuse yet.

The last thing I bought along those lines, I actually bought the, the macropad kit. I love that thing too.

Paul

I was just about to say that my macropad gets the most use. So my PyPortal is also my favorite device.

Jason Pecor

It is. And it's just so much fun to work with that stuff. And just that immediate gratification of being able to change those is awesome. That's my favorite, honestly.

Paul

Jason, thanks so much for being on the show.

Jason Pecor

Absolutely. Thanks for coming over. It's great to meet you.

Paul

Thank you for listening. Transcripts and show notes, including links to photos and video of the trolls, are available at CircuitPythonshow.com. Thanks to PCBway for their sponsorship. Until next episode, stay positive.
