---
date:
  created: 2025-04-07
title: "Episode 43 - Audio Effects Panel Discussion"
---

## Show Notes

[Show notes available here.](../../episodes/Season 5/ep043.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Cooper Dalrymple, Jeff Epler, Mark Komus, and Tod Kurt for a panel discussion on the new audio effects recently added to CircuitPython.

Welcome everyone to the show. Hello. Hey, Paul.

Mark, back in September, you proposed adding audio effects to CircuitPython. What inspired you to add the audio effects?

Mark Komus

It was something on my mind. for quite a while after the initial synth I.O. release that Jeff had put out when I was trying to add drum effects in. And I found YouTube is a really good source of seeing how other people use synths to make drum effects, other types of synth effects, pianos, keyboards, basses, whatever. But where I hit a stumbling block for most of them was that I couldn't add things like reverb. The filters were in and they worked great. But like reverb, little echoes, little things that would make it sound better.

So it was in the back of my head to do something with that. And then I just had some time, was looking for something to work on. So eventually that's how I ended up starting on it.

Jeff Epler

A little bit of a big thing to bite off, but you've been kind of working up to it. I think over time with CircuitPython.

Mark Komus

Yeah, I first started doing audio stuff with audio mixer, I believe, and bringing that to the RP 2040 at the time. Something else with Raspberry Pi, but I can't remember what it was for audio now.

Cooper Dalrymple

I have a quick question for you, Mark. You mentioned the drum sounds using synthio generating those. Did you put out a gist for that about a year or two ago?

Mark Komus

Yes, they did.

Cooper Dalrymple

I think I might have copied some of that.

Tod

Yeah, everyone has been using that.

Cooper Dalrymple

Yeah, yeah, you were like mixing three different voices, I think.

Tod

The decays, it was really good.

Cooper Dalrymple

Yeah.

Tod

I found it in many different people's projects. And they're like, hey, look, I made a little CircuitPython drum machine.

Cooper Dalrymple

And I'm like, hmm, there's no samples here.

Tod

How is he doing it?

Cooper Dalrymple

Yeah, I think I credited it to my, you know, I think I credited it in the source code. But still, that was incredible.

Mark Komus

That's really awesome to hear because that's what I I was hoping with anything I put out. And I've seen a couple projects that had drum effects that was like, wait, that sounds like what I made. But I've never looked into it further than that. Wow.

Jeff Epler

I've seen that commonly on like older systems. The sound of one voice is just kind of not as exciting as you'd like it to be. And so you double up or triple up voices.

Mark Komus

And I have to give credit to Toddbot for that. you were mixing multiple voices and detuning them slightly to get a cooler sound. And then when I started doing the drum effects, I was like, hey, wait, that can work for this as well. I can mix two or three or four voices to get something that sounds more noise-like and not a sine wave from synth. Yeah.

Cooper Dalrymple

When you made that, did you look at, I don't know, like a TR808 or something, some other analog drum machine to see how they did it to build that sound? or were you just kind of playing it off?

Mark Komus

I googled a bunch of YouTube videos of various people making drum sounds on SINC. I can't even remember what videos they were at this point. And then how to adapt them for CircuitPython. As he said, we didn't really have audio effects at the time outside of basic filters and then multiple samples at the same time. So it ended up being sort of a hybrid of what I saw online and what I was able to play with myself.

Tod

Yeah, adding the delays, you mentioned having, like, voice detuning, like having multiple voices where they're detuned to make a fatter, you know, more interesting sound. But, like, you can get the same effect in a lot of ways just by using a delay at much lower CPU cost. And so for, like, if you're playing a chord, say. And so I'm so happy that we have this audio effects and audio delays packages now because it's kind of cruise control for cool. You can make almost any sound a little bit better when you add a little bit of delay. delay to it.

Paul

That's interesting. For those that might not be aware of the new audio effects, what are some example effects that are now available in CircuitPython?

Mark Komus

The first one I put in was an echo, which is really a delay. I put it in because I didn't know what else to do to make sure things were working. I don't have the knowledge that everyone else on this panel does about since in musical knowledge. But it's something that you can quickly and easily take.

test. I can play a note. I can wait half a second and see if I've heard the note back to myself again.

So it became really good for debugging and troubleshooting and learning to pick something simple where you're not trying to troubleshoot your effect on top of figuring out how to do effects to start with.

Cooper Dalrymple

Yeah, I think I can touch on that a little bit as well, if that's okay. First of all, I'm the new kid on the block here. I've only been contributing for about half a year or more to CircuitPython.

I'm named Cooper, I guess. And I come from a musical background and a lot of guitar, piano, stuff like that. And I think what a good place to base this selection of effects that we eventually choose is in guitar effects.

You know, I'm sure many of the listeners here are familiar to some degree with effects pedals for guitar, which are ubiquitous nowadays with guitar players since, you know, the 60s with Jimmy Hendricks and all that, fuzzes, et cetera. I think some of our selection, it may be a little bit more utilitarian in, you know, usage, but kind of takes some of its, I guess, DNA from guitar pedals. So the other effects that we've developed beyond delay, which was a great start, of course, to set this up the whole pathway and how these effects are made. Since then, we have filter, I believe, which is in a different module, audio filters. And then recently just got emerged is distortion, which actually covers a couple of bases. I think that filter one especially, it was, it's probably, probably the easiest one.

I think it was easier than the echo effect to create because it was using the biquad system that you developed Jeff with synthio and then hence the block biquad system which is super cool. But with that, yeah, with that you can build a multitude of effects, things like waos, EQs, just basic filters, low pass and stuff like that.

Tod

Yeah, totally. Because one of the things that, I don't know who it was that set up the initial audio system for CircuitPython, but it kind of was informed by how pedals work and that they have got an input and an output. And if you want to hook things together, you just hook the output of one to the input of the other and you keep going.

And that's how all the new audio delays and audio effects have been set up as well. So you can just start plugging things up and see what they do. And every module or every function has these knobs.

And Jeper made these cool LFO automated knob turning functions that you can just plug into the various knobs of the, the filter and the delay and all that kind of stuff so you can do the was and distortions and dynamic stuff. It's really fun. Yeah.

Jeff Epler

I mean, when I was creating synthio, I did a lot of reading about sense. I'm more of a music enjoyer. I'm a little bit of a vocal musician, but I don't know the instruments. I don't know since. And I got the opportunity to work on synthio. And there was a lot of reading. And I'd learned about something like LFOs, and I would try to create a structure that would allowed to be expanded and elaborated upon.

And I think in some respects, I've succeeded because now we have audio filters. And they're reusing these other things like the LFOs that existed already in ways that repurpose them and increase what they do. And Tod Bott, I don't know if you said what an LFO was.

What is an LFO?

Tod

LFO. It's from the Spanish LFO. No, it's a, it's a low frequency oscillator.

In synthesizers, for reasons back in the misty times, people divided up oscillators into two kind of classes where there's oscillators that made noise and there's oscillators that are really slow, basically at sort of human knob turning rates. And so instead of you sitting there to your hand on the filter knob going waw, wab, wab, you can instead have a low frequency oscillator, essentially turn that knob for you and do the wab, wab, without you having to do it. In practice, a lot of oscillators can be both.

But for code reasons, like with synthio, there's a nice efficiency you can do by having oscillators that are only updated at a lower rate. You can, like, save some CPU instead of having them be full audio rate oscillators. So, yeah, so we have, in synthio, Jeff made real audio oscillators that can be arbitrary waves, and then we've got the low-frequency oscillators that are, that update, I think up to around 50 or 60 hertz.

I've never really tested with upper ranges on how fast they can go.

Cooper Dalrymple

Well, it's 256 samples, isn't it? So depending on your sample rate, I think it's faster than 50 times for a second. I have to do some calculation here.

Mark Komus

Yeah. The whole LFO system and the block input system work amazing. Like, that was one of the first things I ran into when I started the draft PR for audio effects was people saying you need to add in this feature. You need to let people change the delay and the mix level and everything based on these LFOs. And it was so simple to add in.

Cooper Dalrymple

Yeah. And a great example is that is within the audio mixer, we recently added support for block input on the level. And one of the original audio effects, you know, it's in like amps and stuff from like the 50s is Trimel.

which is where you just increase and decrease the volume, like sweeping that knob. And now you can do that very easily using Synthio LFOs and stuff. So that's pretty cool.

Tod

That's cool. I'd not really noticed that in the PRs.

Cooper Dalrymple

That was in like the last two weeks, I think.

Tod

Oh, that's awesome.

Mark Komus

The other bonus with a lot of this stuff now being an audio mixer and all these audio effects, as we realize, they don't have to be just for the synth. The synth was what inspired me and what I think Cooper and myself spent a lot of our time in. But then we realized raw sample and wave files and any other audio files played through CircuitPython, we can add these effects to.

So now you could have an MP3 playing. And if you want to add an effect to it, you can. You could put the filters on it.

You can put an echo for some reason. I'm not sure why.

Cooper Dalrymple

I'm looking forward to Halloween. I have a feeling, you know, there's some spooky sounds that could be put in there. Definitely that.

Jeff Epler

Yeah, although just like an equalizer-style control over your MP3 playback is something people I've requested. And I think that's possible now. I think we have the pieces and somebody should put them together and let us know if it works.

Cooper Dalrymple

Paul, did you suggest that? Because I hadn't actually thought about that until I saw that question.

Paul

That was actually a question that Toddbot came up with was, could we see someone adding based in trouble controls to MP3 playback like an 80s boombox.

Cooper Dalrymple

If you hear me, Jeff, poking you in the future to clean up that PR there for, was it, shelf and everything?

Jeff Epler

I would love to get to that. You know, I just have a lot of other priorities in my work right now. And some of you have probably heard I'm planning on stepping back from A to Fruit this April, going to take a vacation and do some other stuff. But, you know, when I'm back in the right kind of space and not as much focus, on 80 for priorities as stuff that feels cool to me. I hope that's one of the things I'll come back and pick up, but it may be a while. So you might also pick that up and see if you can get it over the finish line because I think

Cooper Dalrymple

I'd be great.

Jeff Epler

I think you could. I think you could do it. It's mostly just edits onto the existing filter system, right?

So it was like I changed the way that stuff was calculated and that's all in. And I think it may have been a matter of being out of space on some of the boards when I added in all the other goodies. Yeah, that's not the fun part.

The fun part is the coding, not making sure that it still works on a board that you wouldn't recommend to a person for a new project. Yeah.

Mark Komus

Great. That's actually a great point about also why I got into this is the RP 2350 came out. And it had built in floating point.

And so much of what's involved in the effects is floating point math. So when it was just like audio mixer and playing an MP3 or playing the synth, that was enough to play on most chip sets. But now we've got this chip with both space, RAM and storage-wise, as well as the processing power to actually power this.

So now it's possible to put it through multiple effects at once. I've tried five or 10 at once and was able to play successfully. It's not until you sort of get to a bit bigger than that where it starts to have issues.

But compared to what you could before, it's a lot more.

Cooper Dalrymple

In that chain, did you happen to use the distortion overdrive effect? I have not tried that one yet. That's the one I'm really nervous about. There's a lot of floating point going on.

Jeff Epler

It really is a game changer. When I was working on synthio, I was very much thinking about the RP2040. kind of as the as the target system because we were looking at making the RP 2040 prop maker feather I think the product ended up being called and so that was a good reason to take time to look at synth and that didn't have the floating point unit so I was reading all this like 1990s here's how we do all of the math for synthesizing without using floating point just using integers so there's a lot of code in there that like treats a 16 bit integer with a virtual decimal point after the third bit and crazy stuff stuff like that. And now if we say, oh, well, we're going to have a floating point unit, a lot of that stuff becomes much simpler than I made it. But we want to keep like the main part of Synthio still working on all the microcontrollers, but it's really neat in these distortion. Which specific one was it that you're talking about? Say the name again.

Cooper Dalrymple

The overdrive. The overdrive. For listeners, there's multiple modes of the distortion effect.

Jeff Epler

And that's one of them. Yeah. I remember I was reviewing this.

pull request, thank you for your patience waiting for me to review that pull request. And I'm like, it looks like you're calling a trig function for every sample. Are you sure that's going to work?

Because I was just in this mode of thinking with 1990s constraints or with two years ago microcontroller constraints. And we can do a lot more now. And I'm glad that y'all kind of breached that frontier and said, I'm going to see what happens if I call exponent or whatever that function.

was trig, I don't know.

Cooper Dalrymple

Yeah.

Jeff Epler

Every sample.

Cooper Dalrymple

I would love to use integer math for all of that. But besides the bit crush effect, and that one actually avoids all the floating point and just use basic integer, you know, bitwise functions. Besides that, it is very difficult to do a distortion effect without integer or floating point math.

Jeff Epler

Just because you need that larger range of values than it's convenient to represent.

Cooper Dalrymple

The functions themselves, I think the only other way to do it would be to use a lookup table of some sort.

Mark Komus

Then your space becomes your constraint, which is always in demand.

Cooper Dalrymple

Definitely.

Tod

Yeah, it's amazing how like the things that we kind of got for free in the analog world of like, oh, if you make your recording to tape a little hot, or if you like turn up the gain too high on your on your guitar amp, it distorts.

Jeff Epler

Something really interesting happens.

Tod

Yeah, it sounds cool. It doesn't sound gross, whereas like when you distort, like over-gain on a digital system, it just clips and sounds harsh and terrible. And when you try to model that really soft distortion that happens in the analog realm, you start calling exponential functions because it's like a really weird nonlinear output. So, yeah, trick function for sample.

Cooper Dalrymple

Sorry, Jeff.

Jeff Epler

If it works, it's great. It's just, I'm telling you what my first reaction was.

Tod

No, totally, totally. Yeah, I'm more in your realm because I started doing synth stuff with Arduino 8-bit.

Jeff Epler

Yeah, you can't do that. Mazi, am I right?

Mark Komus

The other thing I noticed right away, too, is we went from 22 kilohertz on most of our samples to 48 kilohertz stereo, and it was handling it. And it was handling it with a fairly large effect workload on top of that. And if you try that on an RP 2040, it'll do it to a little bit, but not for very long.

Paul

So is it fair to say that you really do need an RP 2350 to make most of these effects work?

Mark Komus

If you really want to take advantage of them. But if you want to use one or two, depending on the effect and depending on your sample rate, the 2040 will work. And I haven't actually tried it on other microcontrollers either. Right now it's port limited to the Raspberry Pi family, but in theory, I know there is somebody's working on getting audio for the expressive family. And I don't see why it wouldn't work on there either.

Jeff Epler

Yeah, that was an interesting development. Somebody popped up on GitHub with a pull request and said, I added analog audio to ESP 32 and I think ESP32S2. And this is something that Lamora had me look at like two years.

ago and I looked around and I said, I don't think I'm up to this. I don't see how it would work. And now that the code's written, it looks really straightforward. So it's just, you know, one of those things where somebody else takes a look at it and they had some piece of knowledge that I didn't have or some piece of experience. And now everybody's going to be able to use this functionality in CircuitPython and do audio on more boards. So I'm really excited about that,

Tod

that little bit of functionality. The ESP32 also is a very, very nice chip set for having native floating point, all that kind of stuff.

Jeff Epler

I think it's plenty fast. I wanted to say that it had floating point, but I wasn't sure. So thanks for that confidence, Tod.

Tod

I think right now, if anyone listening wants to play with these things, definitely RP 2350 is kind of the most tested system out there. Like, I've added some of the delays stuff to a custom build of RP 2040 because it's turned off for RP 2040 just because it doesn't always work. And it does work, but man, I really wish there was some sort of modular system for these core modules so that we wouldn't have to go through that dance of like, oh, I added this new function in the core, and now the CircuitPython build won't fit on a trinkie or the cutie pie M0 or something. I know that's impossible, but it's something that I've been dreaming for years for CircuitPython.

Paul

So we were talking about guitar effects earlier. Do you see the ability for someone to actually build a guitar pedal using these audio effects? I'll get ready for this.

Cooper Dalrymple

Here is a guitar pedal. And this audio listeners, this is not going to make any sense. I'll describe it in a second. So, it's beautiful. And sorry to take over here.

Mark Komus

No, no.

Cooper Dalrymple

This is something, which actually I didn't think I was going to do it first. when I was first working on these effects, I was really thinking about synthesizers, and I have used it, the delay, especially, on some of my synthesizers. But then as soon as I started playing around with it, I was like, wait a second, this would work really well in a guitar pedal, you know, and controls, and like, you're not doing too much else in a guitar pedal except for just processing those effects and, you know, pulling knobs and stuff.

And so I started doing the research, figuring out how to build them. Of course, what I ended up building is definitely a prototype and I need some revisions. But what I did is I took an – it's actually an RP 2040 right now.

It's an RP 2040-0, I believe, manufactured by WaveShare, just because the form factor worked nice for this because they lost my RP 2350s in shipment, which I'm really upset about. I know, I know. But it's that combined with an audio codec, which once again for listeners, an audio codec is essentially an input-output analog system that your microcontroller can talk to and manage those analog pathways without having to use independent chips for input, output, which is a lot more digital in a ways.

So what I really liked about this chip I chose, which is the WM8-960, which I wrote a library for CircuitPython a couple months ago, is that you can actually mix the analog input with that output. So for a lot of effects.

Jeff Epler

Oh, so it can pass through what's coming in.

Cooper Dalrymple

And, oh. And it sounds pretty clean. I actually designed this with a true bypass, which if you're not familiar with, it's pretty much it just takes your guitar totally out of the pedal and just passes straight through to the amp.

I designed that with it thinking that there'd be noise, digital interference and stuff, but it actually sounds pretty clean, so I think in a future revision I'll change that around to just rely on that codec. But yeah, in that regard, you can take that audio into the codec, have those samples come in over I2S as an input, and then process whatever you need for it, and then output it back again on the same bus over I2S into the codec and then mix that process, like say if you're doing a filter or something, mix that with the original signal as you need, as the user decides. And then it sounds really good.

I was actually very surprised. I do have a confession to make because right now CircuitPython does not support bidirectional I2S input and output. I've worked to add that support.

Jeff Epler

Have you done sins to get this to work? Did you sin? You did something bad.

Cooper Dalrymple

Say that again. Oh, I have a sin.

I have a sin. I have a sin. I have a pending a draft PR that adds bi-directional I-2S, but it's very shaky.

And I'm kind of, I probably shouldn't use this language, but I'm a bit in DMA hell with that right now, where it's just you're dropping buffers and all this kind of stuff and sounds bad. It does work, though, surprisingly. So I would love for someone else to help me on that at some point.

But what I ended up doing is actually my sin is I ended up going to Arduino. And I've actually been working on the Arduino Pico library to add that support in, which unfortunately was a lot, oh, I guess fortunately, was a lot easier than to do in CircuitPython. So I have this RP2040 running through that, and I'm building a library to manage the pedal and have all these effects process.

and have a very simple interface for, you know, changing the audio. So you pretty much kind of like Mazi. It's actually very similar to Mazi where you have a control loop and an audio loop and you just separate your processing and it does it all.

Even utilizing both cores of the Pico, it's pretty cool. And so I've been able to do distortion, delay, filters. I stole your bichweds, Jeff.

I'm sorry. It's so good.

Jeff Epler

You're absolutely welcome to them because they're open source and that's one of the reasons. And, you know, I'm not judging. I think it's great when you use the environment that's good for you. I mean, we're here to talk about CircuitPython, but it's important to acknowledge there are other environments out there, and they've got a lot of strengths that we don't always have, and maybe we'll get there by studying them, or maybe we won't. And for something, another environment will always be better. But yeah, no shade for using Arduino, absolutely not.

Tod

Yeah, it's also really good when you want to think through an algorithm that would have to be written in C, and like, oh, I'm going to just like punk this out either in PICO SDK or an Arduino or whatever, see if it actually makes sense before going through all the trouble of making all the CircuitPython bindings to the C code that's underneath. So, yeah, go Arduino to prototype with.

Cooper Dalrymple

However, I think CircuitPython, if all that worked as I wanted it to work, I think it would be a better platform in a lot of ways because next thing you know you have to do the display management. Yep. All the CENTIO, because one thing I would love to do is be able to take. take a guitar in, you know, use a tuning process, read what note you're playing, and then play it through synthio.

Mark Komus

Like that would be incredible.

Cooper Dalrymple

But now that I'm on Arduino, I'm like, oh, well, now I have to figure out how to get all the synthesis working, whereas it'd be so much easier in CircuitPython. Right.

Jeff Epler

Yeah. Just the, once all that core code, that fast code that has to be written in C is done. If you can bolt the parts together in CircuitPython and express in a hopefully simple way, I want this thing up here to control that thing down there.

I think that is where CircuitPython has. a big advantage. Oh, yeah.

Mark Komus

Yeah, I've found that so much. Like, when I was working on the drum effects, I could iterate through their blazingly fast. I was just in the ripple.

Trying, okay, let's try these three things. No, okay, let's change the filter, the low-pass filter, the high-pass filter. And it made it so much quicker.

Like, and again, nothing against Arduino. I've used it a ton. But if I had to build, compile, upload, and test it for all those, I'd still be working on those effects if I hadn't have just dropped them and given up.

Tod

Yeah, it's almost like a live coding environment, because you can be there on the REPL and actually create a synthesizer just by typing in real time.

Mark Komus

Yeah, it's amazingly fast, and you can just play, you can record something through MIDI tracks or just, I've had lots of test files, which are just a bunch of notes from some song that I put into test, and then listen to it right away and be like, not quite right, I need to adjust this. Oh, this is better. It becomes a really quick iterative process to come up with what you want.

Paul

So Cooper's been working on a prototype for a guitar pedal. Do any of you have any other projects in the back of your head that you want to try with these effects now that they're available in CircuitPython?

Tod

Yeah, I mean, I've got a little, what I've been calling the Pico Touch synth that I've been sitting on for about, a year. And I think I'm going to make a custom build of CircuitPython that includes some of the delay functions just to get fatter sound, the ever, the ever, uh, infinite quest for like a fatter synth sound. But that'll be in my tini store. It was in my tending store for a while, but I had to turn off my tending store because of all the fires that have been happening around me.

Cooper Dalrymple

You mentioned custom build. Is that because it's on RP 2040?

Tod

Exactly that. Yeah. Yeah. Yeah. Because the RP 2350 doesn't do.

cap touch yet because of the problem with their pins. So, yeah, it has to be cap touch, has to be RP2040 and thus has to be a custom build. Yeah.

Mark Komus

Well, and that being one thing I was looking at before I got busy and unfortunately and it takes some time away from working on it was a chorus effect. So not just the delay, which is really a delay, but just a slightly different type. So the chorus of fact, just for those that are listening, we'll break up a note and slightly delay it, one, two, three, four, five, whatever many times.

But over a small time frame, so you get all the waves instead of being in harmony together, I guess, or lined up or slightly out of phase, and just comes up with that richer, fatter sound. So that's on my plate. One of the things that I still want to work on, and I mentioned earlier, was one of the first things that I thought of with the facts is a reverb sound.

Yes. I think it'll just make things sound better. And I've looked at a code.

I vaguely know what I'm doing to put it in, but it's just a matter of getting the time and patience to put it in and get it working. That one, again, the 2350 really shines because of the addition. memory and storage, because especially the memory on that one, if you need to record 100, 200 milliseconds of 48 kilohertz audio, that starts eating a lot of RAM really fast.

Jeff Epler

Yeah. So are you getting into PS RAM territory there, or is that fitting in the 512K for what you're

Mark Komus

thinking about? I think it fits in the 512. I've had the audio delays up to a second.

and I think we capped them in a second on purpose. Otherwise, you'll start running into RAM limitations. I haven't tried it with PS RAM yet.

I don't think I've got a 2350 with PS RAM, but I can solve that problem easily enough quicker than I can write reverbs.

Tod

All right, so the reason why reverb will be important for a whole different class of people than us who want to make synthesizers and stuff, is that once we have the ability to do a guitar pedal like audio in, then audio out, plus reverb, plus CircuitPython can already do displays and play MP3s, we can now make a CircuitPython powered karaoke machine. Oh. I expect a learn guide for that sometime this year. Yeah, I'm going to try to sell John Parker in this idea once all the pieces come together.

Mark Komus

That would be an amazing. amazing project to see.

Cooper Dalrymple

You know, what I think is really important for us to work on soonish or one of us, I know, Tod, you have your synthio tricks repository, which I'm sure all of us have referred to at some point. I know I have. Thank you.

I think we are due for an audio effects tricks at some point. Yeah, yeah. Because you mentioned the chorus, Mark.

I've actually been able to do that to a degree, but it probably needs some refinement. And if we had some centralized repository of stuff like that, examples of people to use, I think that would be great.

Mark Komus

That's one thing that I wish I've had time to work on is an intro guide for using audio effects, because at this point, there isn't. There's sample code that a bunch of us have put out there, but there isn't actually a guide on doing it. And the second is an intro guide on how to make your own audio effects. Cooper, you've been amazing, And I can't see this.

Like, I was always hoping somebody would jump in and build on what I started. And you've done a whole bunch more work that I couldn't have bit off on my own. And then between everyone here, it's great.

And the community is great to bounce ideas off of. So you're not just working in that little silo by yourself, wondering if anyone is paying attention to what you're doing. Like, even hearing from Tod tonight that he's seen my drum effects all over the place.

That feels amazing to hear. And this whole project has brought in so many different people that didn't expect to hear from to start with.

Cooper Dalrymple

I think CircuitPython, you know, it's able to cater to a lot of different groups of makers. But I think especially once we really hash out this audio effects, get the live input working, all that kind of stuff, I think it just adds a whole other category of makers, a whole other community to this project that can utilize these resources. and that's just really cool, you know.

Paul

Well, that's a great place to wrap it up. I want to thank each of you for your time. Cooper, Mark, Tod, and Jeff, I really appreciate you making time to come on the show.

Jeff Epler

Thanks so much. Thanks for having me. Thanks for the invite.

Cooper Dalrymple

And Cooper was good to meet you face to face. I know. Hey, anytime you want to hit me up, I'm around. All right.

Paul

Lovely to see y'all. Thank you for listening to the CircuitPython show. A special thank you to Cooper, Jeff, Mark, and Tod for joining the show and sharing their experience in building the new audio effects in CircuitPython.

For show notes and transcripts, visit www.circuitpythonshow.com. Until next time, stay positive.
