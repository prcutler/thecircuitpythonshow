---
date:
  created: 2023-11-20
title: "Episode 31 - Tod Kurt Part 2"
---

## Show Notes

[Show notes available here.](../../episodes/Season 4/ep031.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode I'm joined by Tod Kurt.

Tod is a co-founder of ThingM, a ubiquitous computing and Internet of Things device studio based in Pasadena in San Francisco. He is creator of the popular Blink 1 USB notification light in BlinkM, the smart LED prototyping device. Tod is a co-founder of the Los Angeles Hacker Space Crash Space, the author of the book Hacking Roomba, and an active member in the CircuitPython community with his circuit Python tricks webpage.

Tod, welcome back to the show.

Tod

Hi, thanks for having me again. This is great.

Paul

I used to listen to a podcast that when they had a repeat guest, they would officially become a friend of the show. I'd like to welcome you as my first official friend of the show. Thank you. I feel very honored.

It's been almost two years since we first chatted, and the way back in season one, and one of the big things that's changed in CircuitPython since you were last on the show is the addition of synthio. This past August, We were on a panel together where we discussed Synthio, and I'll link to that in the show notes for anyone who wants to do a deep dive into SynthiO. But really briefly, what is SynthiO in CircuitPython?

Tod

Yeah, that was CircuitPython Day. That was a great sort of constructed holiday. It's a great time period now.

But SynthiO is a synthesis, an audio synthesis, musical synthesis library core module, I should say, in CircuitPython. And in CircuitPython, core modules are things that are built into Synthiotech. Python. They're written in C usually, and it means you don't have to do anything. It's just there.

And it's incredible. It does. It's polyphonic. It's got filters. It can do arbitrary waveforms.

It's got LFOs and modulators. Pretty much all the things you would want in a synthesizer, it's got. And I've been having lots of fun with it since it was in a poll request in like January or February.

Paul

Yeah, you put together a tips and trick page for Synthio, just like you did for CircuitPython. And you've also designed a couple of boards to take advantage of SynthiO. Tell me about some of the boards that that you've worked on.

Tod

Oh, sure. Yeah. So I've designed a whole ton of boards. Like, of the ones that are kind of useful, I usually do an extra run and put the remainder's up on my tindi store. So people that want to get those, they can get them there. I sort of have two main interests in these boards. One is to make the sort of really easy to build learning platforms that people with like a cutie pie or a raspberry pie pico can just drop it down, add a few extra other easy to add parts, and they've got a little synthesizer board.

And they can write their own synthesizers. I've not been working too hard in making a fully fledged thing for these kinds of boards. Because I think of it more as a, for me, it's like an experimentation platform, though, like, you know, some other, like these Arduino Experimenter kits from, you know, several years ago.

And the other kind of focus I've been on are what's the thinnest circuit board microcontroller, sorry, circuit board synthesizer, MIDI controller that I can make because I have often carried a little MIDI controller or a little synthesizer gizmo in my backpack or my book bag. And, you know, I don't want it to get damaged. So I don't want knob sticking out.

I don't want to be a bare circuit board. And so a lot of my stuff has been like, what's the thinnest thing I can do? And so on my tini store, there's a couple of examples of these very thin.

midi controllers. And the most recent one has been this fully enclosed little cap touch synthesizer that I had 50 built that I gave out as to the 50 attendees of our sketching and hardware conference that happened a couple months ago. Because those are a bunch of friends that I know for like the last almost 20 years and I wanted to infect them with synthesizers.

And what was their reaction to it? I think a lot of them are pretty good. Of course, now we're all old enough that a lot of them have kids. So they kind of gave them off to their kids.

Gotcha. But I should be having a version of that. board up on the Tendi store as well. It's basically, you know, a, what is it, a octave and a half cap touch keyboard with a couple of modifier keys. It's got some reverse bound LEDs to let you know when you're touching the pads. And then a couple of examples synthesizers that you can install onto it. One's a wave table synthesizer that makes really weird, cool, like space noises.

And another is a drum machine. And I'm hoping that I'm going to do a little bit more and get a little but more interesting examples up there that are like kind of full synthesizers because I think you can do a lot with this little platform. And it's like no parts that stick up. So you can just like slide it in like you would a pencil case into your bag and it'll be safe.

Paul

That's cool. Last year on our old podcast, The Bootloader, you shared your experience attending Hackaday Supercon. You were there this year too just a couple of weeks ago. What were some of your favorite talks at Supercon?

Tod

Yeah, Supercon is really great. Have you, like you should come some year.

Paul

I should. I really should.

Tod

Like you and me, we only know each other online. We don't, we've not been in the same physical room in the same place. We've been in the same Discord channel tons of times. Right. And so there are so many people that I know in the larger sort of hardware hacking community that I only know in this way. And SuperCon has been one of the few cases where I get to meet some of these people, you know. And so like one of the cool things is like a geek mom who Debra Ansell, she lives in Los Angeles. And so I've seen her a few times.

in reality. But she has a small business with Ben Henke, I think, and Jason Coons. I think we covered them, their product, the Lux Lavier, in one of our bootloader podcasts.

We did. And so Jason Coon, he makes these beautiful pieces of LED art that fit in the palm of your hand. These little, like, they're not grids of LEDs.

They're like a Fibonacci spiral of LEDs, and they just are jewels. And because he uses such small LEDs, these little like, one millimeter by one millimeter LEDs, but they're like neopixels. The LEDs become a surface, like a, sorry, a texture rather than like individual LEDs.

It's like, it's just incredible. And so I got to actually meet him and hang out with him and hold some of these things in my hand and just just marvel at them. Like it's one thing to see what, see pictures of them on websites.

It's another thing to actually like, you know, gaze into it. Right. And that was, and so just just seeing all these people that I've only only interacted with on Mastodon or or Discord or whatever is really great.

Paul

I know looking at SuperCon from afar, even some of my former guests have been there, right? Thea Flowers was there.

Tod

Totally.

Yeah, yeah.

Paul

Yeah, that gives me a reason to go when I actually know a couple of people already, too. So like you said, I have to find a way to get there in the next year or two.

Tod

Yeah, one of the things I noticed hadn't seen before is in some of the talks and in some of the idle conversation, people would just say, oh, yeah, and we programmed this with sort of Python. Like, it was, it was no longer a special thing where, like, you know, we're out of the talks. of this evangelization phase where it's like, hey, you should try this weird thing called circuit python.

It's like now people are just using it because, oh, it's a good enough tool and we can use it now to do a lot of the projects that we've done in the past. And that was really nice. It was just like, oh, yeah, it's just another tool.

Paul

That's great to hear. Tell me about some of the lightning talks that you attended. One of the coolest things they did this year was lightning talks.

Tod

So not everyone has the time to like prepare an hour long talk in front of, hundreds of people. You know, that's pretty intimidating. And so during one of the days, they just said, hey, if anybody wants to give a lightning talk for like 10 minutes, come on up. And maybe you had prepared slides. I think most people had prepared some slides. I think some people didn't do so much, but they were all great. It was like it was like hour and a half, 10 people. And it was everything from, you know, Scotty of strange parts talking about how his brain injury led him to a whole new hacking experiences to, you know, Ali was up there with her Pokemon ball purse, which is like a purse, purse Pokemon ball, but it also is remotely controlled light up neopixel craziness to Tina Belmont taught us all how synthesizers worked from, and she's been doing synthesizers for like over a decade.

So it's like, you know, there's here someone who actually knows, no sense. Yeah, just was every, from all over, it was like one of the best kind of condensed group of talks, and the video's up on YouTube right now because Hackaday streamed, the SuperCon has sort of two stages, the main stage and the design lab stage. And the main stage, they live stream and keep the live streams up for a while. And so for the time being, you can go to the YouTube.com slash Hackaday and click on the live tab. And then there's all the talks from the, from the main stage of SuperCon. So you can get those. And so that was great. The other one, Another one that was on the main stage was this hacker name Sprite.

I forget his real name. It's like Yorne maybe. Yeah, I can't. We'll find it and link to it in the show notes and give him credit.

Yeah, yeah. He's one of the Uber hackers. He works for Espressif.

He is responsible for a bunch of the really cool FPGA hacks you might have seen on Hackaday. And he continued that trend with his talk was about taking the old 1982 vector video game system called Vectrix that, you know, back then took cartridges because everything took cartridges, and he reverse engineered how it all worked and then recreated how that worked in an FPGA. And to be an appropriate emulation, instead of boringly driving a LCD screen, he figured out how to, he found a little like tiny portable right angle CRT and had an analog stage that drove the CRT, the way that like the real Vectrix VectorScope did. So it was like an analog output of these, you know, very clean lines that's indicative of a vector scope output.

And it was all handheld, ran off a battery. It's just amazing. It would play actual Vectrix cartridges, but also would play all of these.

Apparently there's a Vectrix demo scene of people making new stuff. And he found a bunch of that and was able to slot in those custom demo scene cartridges. And it just was like this tour to force of engineering.

That is so cool. Really brand new stuff. Yeah, really brand new stuff in FPGA's driving really old stuff of like tiny old CRTs from video phones.

Paul

No, I got to ask you about a talk that was about the cuddly companion bots. With a title like that, I have to know more.

Tod

Yeah, so Angela Sheehan, she makes this really interesting sort of snake, not a snake. It's like a fuzzy boa companion bot. So a companion bot, if you've never heard, is a robot that you have on your person somehow, You usually wear it kind of on your shoulder, or maybe it's kind of like you, it's a slung thing, like kind of like the way a purse would be or you'd wear, maybe it's a backpack.

And it's sort of the people who make these call them, call them like your companion robots. So the way you have maybe a companion animal. I find it fascinating because robots are hard and they're noisy and they take a lot of power and they are not really amenable to being so close to a person.

But here they are making these devices that will sit on their shoulder. and have to interact with the more soft human world. You know, that means, like, in the way they move, and the way they interact with the other people, with the person that they're on.

So Angela's talk was about, like, how to do some of that. And that was, that was really fascinating because I love robots. I'm not interested in making us, making a companion bot, but all the people in the bot community are really cool.

It's like, it's Angela and Ajay, which, you know, and Ali, who did the Pokemon Ball thing and geek monster. As representatives of the of the companion about community, they're just, you know, wonderful. Oh, that's great.

Yeah, yeah. And so, yeah, so it's just that video is also up on YouTube so you can watch her talk right now, too. I mentioned Thea Flowers earlier.

What was her talk on? Oh, man. Okay, Stargirl, aka Thea Flowers, for the last year so, she's been working on making a web viewer for Kekad Schematics and PCBs.

You think, like, oh, that's pretty easy. You know, you just read the file format. and you just, you know, turn that into an SVG.

And no. Like, her talk was, her talk was hilarious. It should have been a main stage talk so we could have a video of it right now. It'll, like, they'll upload the video of it eventually.

It was just amazing because, you know, KCAD, it's 30 years old. You know, it's, it's this amazingly long-lived code base that's been touched by hundreds of people. And so the fact that it runs as well as it does is amazing.

Yeah, I had no idea that it's been around that long. Yeah, yeah, it's just, I mean, granted, the people that wrote most of it work at CERN. You know, there's some of the smartest people on the planet.

But any long-lived code base has a bunch of different ways of doing a single thing. Because, you know, you do it one way, and then, like, sometime later you figure out a better way to do it, but you have to keep the old way because of compatibility issues. And then suddenly it's a couple decades later, and you've got a couple of piles of legacy This is stacks you have to deal with.

And so in navigating that to make it so the web viewer works, she had to figure a lot of that out. Her talk about how she went through it was really nerdy and really fun and really funny. That's pretty cool.

SuperConn is known for its badges. What was the badge like this year? I don't know if you've seen pictures of it yet, but it looks kind of like an old tectronics scope.

And these scopes, they had a round. CRT screen in like the top left and then they had these big knobs and buttons that kind of surrounded it and it was a sort of a vertical orientation of the whole instrument. So like a lot of the test equipment nowadays has sort of a horizontal orientation with like the screen to the left and the knobs to the right.

This thing was vertically oriented where the screen was kind of the top left and the buttons were on the bottom. That's kind of what the badge looks like. It has this round LCD and then a bunch of buttons and some little like connectors on the side.

And then when you turn it over, you see that it's a Raspberry Pi Pico and a couple of support chips. And it's a pretty brilliant little hack. There's an arbitrary waveform generator that I think is written.

So the whole thing is running MicroPython.

Paul

Okay.

Tod

The way you kind of interact with it is there's sort of two parts to the badge. There's the arbitrary waveform generator that outputs an X and a Y signal. And then there's the scope part that reads an X and a Y signal.

And so you can just use it as an oscilloscope. You can just feed in an X and a Y. and then get cool, listed you vector scope patterns. Or you can use the arbitrary waveform generator to give you, like, an X scanning time base to then be your X, and then have, then your signal, whatever your signal you're measuring is your Y. And then you get, like, more of a standard oscilloscope readout where the scan is a constant time.

And then the vertical Y axis is showing you what the voltage is over time. And you can do all of that without doing any code on the badge. You just, like, hook up wires and press a few buttons.

And it's basically like an old oscilloscope. It's all like got green phosphor look. And as the traces move, it's got this cool phosphor fade effect.

This is like a separate process on the second core of the RP2040 that's in the PICO or something. It's incredible. But of course, it's all open.

You can hack it all. And so I was like, I hacked around with a little bit. But I'm not very fast with Micropython.

And so one of the first things I did is they just blew Micropython away and Salt CircaPython. because I know how to run these GC9A01 round LCDs. I've been playing with those for a couple years.

Sure. So I did a bunch of little dumb hacks with that. And then you created a capacitive touch sensor to go along with it?

Sort of. I've been playing around, like I mentioned with the boards that I made, I've been playing around with cap touch buttons for a long time now because in CircuitPython, it's so easy. You just use the touch I.O. core module, it's built in.

And you say, hey, I want to turn this pin into a touchpad. and then it'll give you a true false value whenever somebody touches the pad. And so it's super simple.

But I knew that there was ways of doing more complex sensors with just a couple of cap-touch pins. And so you can actually make a slider, a capacitor touch slider with just two pins if the pads are shaped in a certain way so that you get sort of a ratio between the two pins depending on where your finger touches. And similarly, you can make a rotary control, a touch.

touch wheel, sort of like the old iPod touch wheels, with just three pins. And so I'm like, and this is a thing that's been known for like 20 years or something. I've not played with it much. I'm like, okay, I'll just spin up a quick board and I'll have it so the pin out matches the little expansion pin out of the badge. So in theory, you can just plug it onto the badge and have it work. I got the boards back like two or three days before Supercon, Sauted up real quick once I got the badge. And yeah, it worked great. I was like so surprised. I was like so surprised. Yeah, it was like, you know, 20 lines of CircuitPython to do the simple math to turn the three sensor readings into a angle. Yeah, so that's up on the GitHub. There'll be a link to it, hopefully, in the show notes. Absolutely. And I'm working on a board because I'm so excited now by like, oh, I can do like various types of interfaces with capacito touch, it's not just buttons, that I'm working on a little sort of cap touch explorer board that'll have some wheels and some sliders and some other things. See how that turns out.

Paul

Now, there was some controversy around the lack of diversity in the speaker lineup at SuperCon this year. Not having been there myself, was it fair criticism?

Tod

Yeah. Yeah, there's, I mean, you can just go to the, go to the SuperCon website, and you'll see that all the speakers, they're mostly white guys, you know? There's a, Carrie of Alpenglo has a really good thread on Macedon about this. And because she's been a speaker in the past, and she comes every year, and she was there this year.

But it's just, it's really hard because when, when a community has sort of a default kind of member, you know, like you and me were kind of the default kind of member. We're the middle-aged white guys. Right.

You know, that's kind of your, you know, they're a stereotypical hacker. And when you're that, it doesn't, it's not hard to get the default to, to submit talk proposal. When they just say, Hey, our talk proposal website is open.

Submit a talk. You know, because we'll have, we feel, we, we have the time. We also feel comfortable in submitting a talk.

If we can, if we can get over our own personal, like, oh, I have a fear of public speaking. Right. But like, but like, but like, we mostly feel welcome in the community.

But there are so many other people that are part of the community, but they don't feel welcome. And, you know, usually these are the non, non-white guys. And so, like, how do we get more of those?

people that are in the community but don't feel welcome. How do we welcome them in? And we really have to do the effort to make sure they know they're welcome.

And that's hard. It's a proactive reaching out rather than a, hey, come submit your talk to us. You have to actually go out and get people.

Paul

And that's hard. You're absolutely right. It's very hard.

Even with the podcast, I'm always trying to keep that diversity, you know, an inclusion top of mind and making sure that I try and balance those guests out. And there's been some criticism of the Python podcast ecosystem as well of not being as the Python community is. So you're right.

It's something that you have to work on. You have to have it top of mind. And you have to keep working on it.

And you have to let people know that you're going to be fine. You're going to do great. And welcome them with open arms.

Tod

Yeah. It's really hard because a lot of us are introverts. It's hard to reach out to people.

in general, you know, and just say, just say, hey, you know, it's like, this is the problem that we had at Crash Space, the hacker space that I founded, sorry, co-founded, that, you know, people would come in off the street to say, hey, is this a hacker space? And we'd be like, yeah. And then we would all turn back to whatever project we're working on, you know.

It's like, that's not how you welcome new people. To welcome new people, if they come in the door, you have to, like, get up and welcome them and show them around, you know, and say, here's where the laser cutter is, here's where the 3D printer is, you know?

Paul

Exactly. You're absolutely right.

Tod

But it's so easy when you're in your head, you're focused on a thing and you're like, I just want to solve my problem.

Paul

Well, we're almost out of time. And the last question I always ask is which board do you reach for when starting a new project? And in over two dozen episodes, you're the only person that's chosen a fun house and an itsy-bitsy. Are those still your go-to picks or is there a different board that you reach for these days? Yeah, probably these days for,

Tod

For I'd say general CircuitPython work, I would choose a Raspberry Pico. Because of the fact that they're sort of sold at cost at $4, they're like a really cheap way of just trying stuff out and lowering that barrier of fear of like, oh, what if I fry something? What if I burn this board up?

It's like, well, you burned up $4 if you have. But also, like, the space of things you can do with the Resbred Pipeco is really large. And so it's a really great board.

Even if you're not doing CircuitPython, like you can do a lot. of really great stuff. In Arduino, you can use the PICO SDK to get really low level.

It's got that PIO functionality that's sort of like a little bit of programmable logic inside of the PICO that you can do to do so really fast protocol-y-type stuff. And so it's a very interesting board. You can do the PIO stuff, insert a Python even, which is amazing. But it doesn't have Wi-Fi. And there's the PICOW that has Wi-Fi, but I think that an ESP-32 board would be better if you want to do Wi-Fi.

and for for for Wi-Fi CircuitPython I probably recommend an S3 board yeah yeah ESP 32 S3 and then like which one so like like like my default is a QtPy ESP 32 S3 but I think Wi-Fi devices need some sort of a display because there's this whole onboarding problem of how do you get it onto your net and like having a display is really useful for that So I guess maybe the, like if we're talking at Adafruit products, the reverse feather, the reverse TFT ESP 32 S3 feather, I think. There's also a really good lilygo board that has an ESP 32 S3 in it, I think. There's so many choices.

ESP 32 S3 and if you use display, pick one, if not a QD5.

Paul

Those are all good picks. Tod, thanks so much for being on the show.

Tod

Thanks, Paul.

Paul

Thank you for listening. For show notes, visit. www.com and transcripts are available in your favorite podcast app. Until next time, stay positive.
