---
date:
  created: 2022-05-16
title: "Episode 9 - Liz Clark"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep009.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host Paul Cutler. This episode, I'm joined by Liz Clark, also known as Blitz City DIY.

Liz is a Massachusetts based maker who dabbles in electronics, music tech, 3D printing, CircuitPython, and anything else that looks interesting that day. When her soldering iron is cooling, you can find her with her cats Winnie and Harriet. Liz, welcome to the show.

Liz Clark

Thanks for having me.

Paul

Many of the projects and learn guides that you've shared are music related. What is your music background?

Liz Clark

So I started playing piano. When I was a kid, there was a program in Parks and Record Department. That's how I started.

And then as a teenager, I picked a guitar, taught myself, and I was bands. And then I was coming up in bands just as MySpace started being a thing. And that became the thing for bands to record for, whereas before I was, you wouldn't necessarily go do that.

So it's really expensive. It gets to you a space, especially when you're a teenager. So that's when I started getting into recording audio.

And then I found I actually liked that a little bit more than playing in band. So that's why I started to study in college. And that's how I got into MIDI and everything like that.

So that's kind of been my music journey.

Paul

Okay. So you're studying music tech in college. Is that when you first started to become a maker and get into that community as well?

Liz Clark

I've always made stuff like I've done sewing and knitting, things like that. My family really had to things like that too. But as far as like electronics and coding, I didn't know that was really a thing until college.

And while I was in college, it felt risky to be majoring in music just because, you know, you hear things like, oh, you'll never be a good job and things like that. So I wanted to try to like expand my skills. And that's when I found out about Arduino.

This was like 2011, 2012. And I saw that folks were doing like DIY music tech project, like bitty things or robot instruments. So I attempted to do a little bit with Arduino.

But again, I had zero coding background. You know, folks will talk about using max of school. I never did that.

So it was a steep learning curve with really no guides. So I didn't do too much with it. But it was something I always wanted to explore more of.

So after I graduated and I did get a job and everything, I wanted to get back into doing more DIY things. And that's when I started my YouTube channel as kind of a way to not get sucked into just doing a grind of like going to work, coming home, kind of keep my brain sharp. And that's when I started diving into Arduino and really learning it and eventually, like, Python and all the other projects.

Paul

How did you make the jump from Arduino, which is, is mostly C-based, a CircuitPython, which is completely different.

Liz Clark

Again, not too much coding experience. So I barely understood what I would be doing with Arduino. I really couldn't tell you why my code would be working.

I would just be like trying a bunch of things. And then CircuitPython came out. I was curious about it because I knew that, you know, Python would get used on Raspberry Pi, and I dabbled like a little bit with that.

But AidaFruit had all these libraries for CircuitPython for, stuff and the CircuitPython Essentials guide that Katney did that kind of went through everything, I started to understand a little bit more and I understood what the code was doing, which was a big game changer for me, as basic as that sounds. And then that's what I started trying to do slightly more complicated projects with it. And now that's just my go-to for everything.

Paul

Yeah, you hit on a key point. Python, it's all about the readability. It makes it so much easier to read than some of the other programming languages out there.

Liz Clark

And now that I've worked with Python so much, like other programming languages will make sense to me. I just finished up the project with processing, which is Java-based. And I was a little nervous at first because I hadn't done Java before.

And I slightly scarred from the Arduino experiences and not being able to understand. But I picked it up a lot faster than I had. So I think that's important to if people are just getting started coding, start a CircuitPython, then it might help them to understand other programming.

Paul

You mentioned your YouTube channel, which is Blitz City DIY. Is there a story behind the Blitz City DIY name?

Liz Clark

When I was starting a channel, I wanted it to be a name that would kind of last and also be unique. I've been in a lot of bands and done the whole coming up with a band name thing. So I kind of approached it that way.

It's kind of a reference to a couple different things. The Blitz comes from Woods Creek Bob by Ramones, and it's Blitz, which is now by the AAS. And then City, I liked that because of the idea of collective, like a group that I didn't know if maybe had to work with people down the road.

And also, I've always been really community focused. And then the DIY, just to kind of give it some context. It all kind of roots from DIY punk aesthetic.

That's kind of where the name grew.

Paul

Love it. So you also mentioned when you were talking about Arduino robots who play instruments, and you built a xylophone. Tell me about the xylophone.

Liz Clark

That was actually the thing that I originally wanted to build in college when I found out that that was a thing before doing. But I did not have the skills at the time. I played some mallet stuff in high school and college because I showed up to the bandroom and I didn't play the band instruments.

But because I played piano, the band director said, well, xylophones and piano is mixed. I've always really liked the sound of that and percussion instruments, too. So I had the Glock and spiel from there and thought it'd be so cool to have it be able to play automated music from music.

Because the only thing about mallet instruments is you're limited to how many mallets you can have. And so you can play four, but it's really hard. You also, it's hard to do stuff really fast and everything.

So the idea of making an acoustic instrument that can play stuff that a human is, necessarily wouldn't be able to very easily. So that was kind of my inspiration for it and was CircuitPython and it made it a lot easier.

Paul

So for someone looking to get into MIDI, what do they need to get started?

Liz Clark

MIDI is this kind of standard way that started up in the 80s of having musical instruments communicate with each other digitally. So it's actually, it stands for a musical instrument digital interface. So for MIDI, there's really good libraries for now with both Arduino and Sergipython. Back when I was starting, which helped me up a bit, had to do weird stuff of audering, things like that.

But the Sergapython library especially is really plug and play. And basically it makes so that your microcontroller just interfaces through USB. There's other ways you can do it too, but the easiest way for some of it starts with USB. You can just have simple things like a button input or dengeometer, and you can control either software or hardware sent because it's sending these video messages and you can code it to figure needs basically.

Paul

So when you code the notes, it's actually sending it right back if let's say I had an electric piano or a keyboard plugged in. It would send the notes back to the keyboard and the keyboard, it would sound like it's playing the actual notes.

Liz Clark

Yes, yeah, exactly.

Paul

How does it work on a computer? Do you need like a digital audio workstation to capture those?

Liz Clark

So you can use a digital audio workstation Ableton for Pro Tools or Reason. Then there's also little programs that can kind of read the notes back to you, almost like a serial interface. One that I really like is called MIDIBerry.

That's why I usually use when I'm building a new MIDI project. It'll tell you exactly what MIDI notes you're sending. And that way, you know, you can have the Raffle in Mu tell that to you, but to actually see that the MIDI messages are truly going into another program is important.

And you can have like a software sentence there also. Playback the note, be affected by the different messages, because you can also do things like pitch bend or modulation.

Paul

Tell me about the MIDI Arcade project that you wrote a learn guide for.

Liz Clark

Midi Arcade Fighter is a collab that I did with the Nairus, and he designed the case. And it kind of came from a need he had, which is why DIY MIDI-Controller, I think, are so exciting. He does a lot of finger drumming, and he will take the time to map the difference.

sound to his DAW to the MIDI controller. And so he was like, it would be really cool if you could design them like on the controller, kind of on the fly. And so that's why on that particular MIDI fighter, and there was a company that used to make up things called MIDI fighters, notice these arcade button things, and it's kind of become like its own genre of MIDI controllers.

And so for our version, there's a little screen with a five-way joystick where you can adjust the MIDI notes on the fly so everything can be mapped, like, live. And then someone in the community actually made a addition to the code that you could store MIDI mapping in a JSON file and kind of call them up that way, which is really cool. That's one reason why I love learning guides.

You can kind of put like this basic version of the code or basic, and then people can build on it because that's totally something like that would have been awesome to do, but to then some of the community take them there is really awesome too. And the reason why that's, I think, a good starter one is I think most folks, when they want to start with MIDI, they just want to get a note going somewhere. And that project does that, and it also shows you how you can have stuff lighting up because we've got lights on the arcade button and also that additional thing of the MIDI note mapping, I think is helpful for folks because you can either take the really basic stuff.

crib it to your project or you can kind of build on that.

Paul

Hi, it's Paul. I'll get you back to the show in just a moment. Thanks for listening, and if you're enjoying the show, please tell a friend or write a review.

You can also support the show financially. Your support helps cover the cost of podcast hosting, recording services, and transcriptions. For more information, visit CircuitPython show.com slash support.

Now, back to the show. You just finished a MIDI learn guide, deep dive into MIDI for the AdaFruit Learn

Liz Clark

guide system. What were some of the key takeaways from that? When PT brought up the idea of the guide, the kind of midi-jured makers, I wanted to write it almost for myself like five to six years ago.

And I just thought of like, what was I looking for with no background knowledge on how to get started? There's all sorts of information, like what it is, how it works. But then also like what boards work with Circa Python and Arduino.

and the different types of MIDI communication because there's USB MIDI. There's also MIDI over U-R, which is serial communication. That's when you see those big, chunky, like, five-pin connectors.

That's how that's working. There's also Bluetooth videos. So just kind of explaining how that all works, I wanted to have three examples for MIDI-In, which is sending MIDI messages into the destination, and also MIDI-Out, steving video communication.

So there's an example for a quick-all. keyboard, having Pops control things. There's also showing how to convert MIDI U-R to USB because you can do that with CircuitPython and Arduino.

And all the examples are in CircuitPython. So folks can just use that library and just kind of go with it.

Paul

I thought it was a great guide. It actually inspired me to go get our old electric piano that we've had in storage out and bring it down near my office, trying to figure out what kind of projects I can start to do with MIDI because, you know, I need another project on my list.

Liz Clark

That's awesome. That's awesome. I'm hoping it'll be a good resource for folks, and it'll save someone from having to have like 15 tabs open when you're just concerned.

Paul

What does your music set up like at home?

Liz Clark

I've got this synth shelf that I built during the pandemic because I started getting into Eurac and other things. I've got URORAC on top, pocket operators and robot xylophones that we talked about on the bottom here. Then going down, I've got mixer and my USB audio interface for mic inputs.

And then to my right is my guitar setup, so my amps, anything like that. And behind me is actually used to be where the stintz shelf was. And where the pandemic seeming to possibly be getting better, and as a result, having folks over for dinner more often, hopefully I thought it would be better to get my table cleared off.

So now everything is kind of in one spot, which is nice before I was a little bit disjointed. I've really come to love EuroRAC. People are doing a lot of really cool stuff from open source and synthesizers like, see a flower, winter bloom.

She has some certain Python-based modules. so there's a really cool overlap, I think, with synthesizers, CircuitPython, tech is happening right now. So that's kind of why I got into that.

Paul

And for those who might not know, what is Eurorek?

Liz Clark

It's these different, they call them modules. I don't seem like these little kind of P2 thing, but circuit guts on the back and you rack them up. And basically, you got to think of them as like little pieces of a large synthesizer.

So you're taking these modules and building a, basically, your dream. And so there's all these filters and oscillators and things like that. It can get upsettingly expensive.

So I try to keep it as minimal as possible. And also, you market is the way to go. But it's really fun.

It's you patch everything with these little cables. So you're almost kind of building these little musical circuits. You can think about like if you were going to blink an LED with a microcontroller, you have the wires to the resistor and the LED.

It's similar to patching a synth voice on your RACC. You know, you have your oscillator, you have your CET, CO. It's really cool.

So it's a way to kind of keep it like a creative, musical experience, but also, like, technical.

Paul

It may have a similar community as I think we'd find in CircuitPython, which is very open, very open source oriented. Is that correct?

Liz Clark

Yes, yeah. The corners that I've been in, at least, have been very open and open source. And people are really into building their own modules to, And I hear a lot, you know, from via that, like, people ask, like, well, I know if this module is going to get. Like, people will want the kit over a fully built module, which is interesting.

Paul

Yeah. Well, before we wrap up, I have a segment that I call Turn the Tables, where I've been asking all these questions. Now you have a chance to ask me a question.

Liz Clark

My question for you is what is your favorite CircuitPython library?

Paul

That's a good question. Right now I've been playing with my Pi Portal.

Liz Clark

Oh, okay. Yeah.

Paul

So I'm cheating because it's a whole class, right? It's not necessarily a library. But the Pi Portal's got those tools built in where it can actually read a JSON file, take an image, put it through Adafruit IO, and give you the bitmap back.

So that's what I've been playing with. So I'm cheating. I'm not really answering your question, but that's currently my new favorite thing to play with is just trying to feed it.

What can I feed this class and what do I get back?

Liz Clark

Excellent.

Paul

Where can people find you online?

Liz Clark

So I post on Twitter and Instagram as with Say DIY. I also have a website that has not been updated a very long time. Let's say DIY.com.

And also, Let's Say DIY is the name of my YouTube channel. And I have also recently begun working full time with Adafruit. So I'll be having a lot more guides and hopefully videos too with them as well.

Paul

That's great to hear. So speaking of Adafruit, you're about to start a new project or prototype. What microcontroller are you going to reach for first?

Liz Clark

Recently, it's been the feather, but specifically the RP2040, because it has the stemma QT connector. And while I'm prototyping, even if it's a stemma QT, I do still like to have that base of the breadboard. So I like to have that footage into the breadboard, and then you have the ability to do the STEMA, which is really nice. So that's kind of my go-to. And the feather or two when you're prototyping, it usually has enough in, possibly more, than what you think that's my go-to.

Paul

That's a great pick. It's amazing how far the RP 2040 has come in just a year.

Liz Clark

Yeah. That was a very nice, I think, kind of jumpstart. to microcontrollers and kind of the electronics community. And I think it also got a lot more people using Python on microcontrollers because when it initially was released, there was CircuitPython and Micropython support and the Arduino core wasn't quite ready. So I think it got people to explore a little bit.

Paul

That's a great call out. Liz, thanks for being on the show.

Liz Clark

Thanks so much for having me. Great talk about you.

Paul

Thank you to Liz for being on the show. You can find Liz's YouTube channel at Blitz City DIY. For show notes, transcripts, And to support the show, visit CircuitPythonshow.com. Until next episode, stay positive.
