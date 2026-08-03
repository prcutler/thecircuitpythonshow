---
date:
  created: 2022-03-22
title: "Episode 4 - Tod Kurt"
---

## Show Notes

[Show notes available here.](../../episodes/Season 1/ep004.md)

## Transcript

Paul

Welcome to The CircuitPython Show, an independent podcast with the people in and around CircuitPython. I'm your host, Paul Cutler. This week I'm joined by Tod Kurt.

Tod is the co-founder of ThingM, a ubiquitous computing and Internet of Things device studio, based in Pasadena and San Francisco. He is the creator of the popular Blink USB notification light and BlinkM the smart LED prototyping device. Tod is a contributor to Make Magazine, the author of the book Hacking Roomba, an active member in the Arduino community, and co-founder of the Los Angeles Hacker Space, Crashspace. His past work includes being the original systems architect of go-to.com, the first public paper-click search engine in a researcher in Yahoo Research Lab. Before that, Tod was a hardware software and firmware engineer working on robotic camera systems for probes that went to Mars.

Hi, nice to meet you.

Tod Kurt

Great to have you.

Paul

So when I was reading your bio, it mentioned that you founded Thing Am, a ubiquitous computing and an IoT device studio.

What exactly is that?

Tod Kurt

Well, it was back in 2006, and that was when the whole idea of imagine a world where devices all around us are talking to each other and maybe talking on the internet, that was sort of a fantasy. And so me and my co-founder, we were trying to make a, imagine a world where devices were smart. Like, everyday household devices, be they dressers or coffee tables or coffee makers, and then trying to answer the question of like, well, what would they have to say if they were smart?

Turned out that was a little bit too soon, but we didn't have to wait very long because in 2007, the iPhone came out. And suddenly everyone started to realize that, oh, wait, maybe there can be this world where a computer is everywhere, because now we all started to have them in our pockets. Right.

And we started to see these phones as computers rather than just as telephones. And so, Thingham really struggled to get its concept off the ground, partly because of technological reasons, partly because of just like societal reasons. It's hard to imagine these worlds.

From our research of prototyping various things, one of the things I came up with was the Blinkum, the little I squared C Arduino add-on that let you control an RGB LED very easily, which back in 2007, 2008 was like a really cool thing because it was hard to control LGBLEDs with Arduino, especially if you want to do more than one, if you want to do like four or five, it was just kind of not possible. And then that led to the Blink 1, which is our current, it's a USB LED that is our current big product.

Paul

You know, that's a great segue. So you've been around Arduino then since back then, and it sounds like both your work and your personal life kind of cross with the whole maker community.

Tod Kurt

Definitely.

Paul

What led you into Arduino?

Tod Kurt

Really, it was my co-founder. He knew a lot of the original Arduino co-founders, sorry, a lot of the original Ardovino team. And we do this yearly conference called Sketching and Hardware, which at the time, back in 2006, 2007, was trying to imagine what would be the, perfect Lego-like system for sketching electronic products.

In the same way you can just sketch a piece of paper and show it to someone and they get the idea, is there a similar thing that you can just quickly plug together stuff and show it to someone and go, oh, I get what you're trying to do for this burgeoning world of Internet of Things and ubiquitous computing. And we thought at the time with like, oh, if we get all these great thinkers together, we can figure out the one true system that'll work for everyone. And Arduino had just been sort of invented at Ivrea out of the wiring project.

And so Mike, my co-founder, got a bunch of those people in, got a bunch of other people from academia and from industry. And we all had this like, you know, four-day-long conference of like, let's try to figure it out. And, you know, and we've kept doing that conference ever since pretty much.

Oh, no kidding. And it turned out, you know, very quickly that there is no one perfect Lego-like solution for sketching electronic ideas. Arduino is a really powerful one.

it abstracts away a lot of the stupid problems. One of the best things Arduino does is it gets you to blinky. How fast can you go from opening up the box and having a little board to blinking LED on that board?

In the 90s, 2000s, you had to install the, well, first you had to purchase the integrated development environment from the vendor. They had to install it. And then you had to get the compiler working.

You had to figure all the compiler flags for that chip. but then the BSP for the board that the chip is on, da-da-da-da-da. And so it takes you like maybe a week to get just a blinking LED.

And then Arduino made it so you can get to blinking on an LED in like five minutes.

Paul

Okay, that's, yeah, a week to five minutes is a good story to have.

Tod Kurt

Their focus was more on pedagogy. Let's figure out how to teach people what to do with these boards once they work. And so like, okay, let's, so assume you can read buttons and light LEDs and make tones on a beeper.

Now, what are you doing with that? And so that was really their focus. And so they made this very nice, simple, essentially set of macros and libraries on top of C and C++ for the ATMEGA that was a really good model for how one should do sort of platform-independent software design.

And so that's why I think that's one of the reasons why we've seen the explosion of Arduino for everything. Like any board that comes out, there's almost always an Arduino core for it very shortly. And the other thing that I think that made an Arduino successful was it has, has holes instead of pins where you can plug wires into.

Whereas all the other boards before then, they had mail pin headers. And so you had to figure, well, what do I plug onto a male pin header? Whereas everyone can just know how to stick a wire into a little tiny hole, right?

Paul

Yeah, absolutely. The things we take for granted, I wasn't doing anything in the maker community, you know, 10, 15 years ago. So to me, to hear that could take a week, I'm like, my eyes go wide just to make an LED blink, much less trying to figure out what the plug-in where.

Tod Kurt

Totally. Yeah. So seeing this just explosion and ease of use, as someone, me, who struggled for the week on multiple chips to get it up and running, I was like, okay, I'm all in an Arduino. And I really liked Arduino because not only was it easy to use to do the normal stuff, but because it was just a thin framework on top of C, you could delve into low-level C, you could delve into assembly if you needed to do stuff. And so, like, oh, I need to make this signal actually output in the megahertz range.

I can do that with a couple of assembly instructions. I can't do that in normal C. I can't do that in Arduino. That's okay. I can just make a function that looks to Arduino like a normal C function, but then does the magic fast twiddling in assembly.

Arduino doesn't really present you with a floor with what to do with a chip. You can just go down as far as you want. It is present you with a ceiling because it's really hard to do certain common things that you might want to do with embedded systems, like just adding two strings together, like incatenating two strings, in C++ is hard.

Even now, it's still hard. I mean, it's kind of harder in Arduino C++ than it is in normal C++ because normal C++ has all these new fancy classes. But yeah, still, why is it so hard?

Why is memory management so hard? And it's just like, well, that's just the nature of how it all works. And so doing anything network-based where you're talking with HTTP URLs, getting down text and parsing text, that's pretty hard to do in CNC plus on Arduino.

And so, Arduino very good. No floor, but it's got a hard ceiling to get through. Sure.

Paul

So one of the things you've been sharing on Twitter lately as you play with Arduino is your synthesizer sounds. So you've got a couple of different synths out there. Where does that passion come from?

Tod Kurt

I've been doing music stuff since basically the very beginning. I use some extra scholarship money in college to get my first synthesizer and sampler. Nice.

Back, yeah, back in the long ago time. And so I've been doing synth stuff in various ways and various kinds of things. for the very beginning.

Our mutual friend John Park has been doing Eurorack stuff for a couple years. That started me getting into making little Eurorack modules, which this is one of, this is actually, this runs on a trinket from Adafruit, which also runs CircuitPython. But usually you need to do something Arduino-like or C-C-++ base to do actual audio output from these modules. And so, yeah, so all my little modules nowadays, home-ed old synthesizers have been looking like this, which is a little C-plus, T-Jou with a bunch of knobs and it makes noise.

Paul

I'll have to get a picture of that included in the show notes for those who aren't watching on YouTube. Sure. So tell me about some of the synth projects that you've been sharing on YouTube. How do you make those sounds? How do you combine them?

Tod Kurt

Ah, so the cool thing is that there's two really interesting projects out there, if you're interested in doing this. One is called Mozi, M-O-Z-I, and it's been around for about a decade made for the original Arduino. And it is a synthesis library.

So it's got, it's sort of like a little modular synthesizer. You've got an oscillator object, and you've got a filter object, you've got an envelope object, and you connect them together, much in the same way that you might connect modular synthesizer modules together. And so when a standard signal flow in a synthesizer, you have an oscillator, and that goes to an envelope to control like the loudness of the oscillator, and then that goes to a filter to control the brightness or dullness of the sound.

It's like the bwau you'd hear is. Is the filter being modulated? And then you might have modulators coming in from the bottom to modulate, like say the pitch of the oscillator or the cut off of the filter.

And so the pitch of the oscillator is how you change the notes, you know. And it's really just you describe a signal flow, and then you describe like how the signal is being modulated. And it's pretty easy to hook up.

And so I had seen this a long time ago, totally ignored it. A friend of mine online, Emily Velasco, she's been doing some fun little art projects using Mazi. And I'm like, oh, I wonder if Mazi works on these newer chips.

Yeah. The little QtPy, the ones that are based on the SAMD-21, the arm processor. And somebody did the work of making it work on the SAMD21.

So I was like, awesome, I'm going to do that. Because for a bank for your buck, a little cutie pie is a lot of computer in this little stamp size package. And a cutie pie runs how much roughly?

Like, I don't know, $8, something like that. There you go. Yeah.

And sometimes you can find them on sale. And so they are a really good Arduino platform because they're so powerful compared to what Arduino was originally designed to run on. And so Mazi runs great on this.

You can run like 32 oscillators and multiple filters and all this modulation. I'm not even hit the limit yet on what's possible using these chips. I've been working towards to see where can I make it break?

That's always the fun part of these projects. And so you have to fix it. Yeah, and that's sort of like the lo-fi library is Mazzi because it was made for Arduino.

Everything is kind of 8-bit, 8-bit sound. Now, if you get into the teensy world, teensy by Paul Stofford. Stoffergen, I forget how I said his last name, but PJRC.com, they make this great line of boards called Tiencies, and he made this really great library called the Tiency Audio Library.

And in it, it's got a GUI, web GUI, where you can describe how all those objects connect in terms of the signal flow, and that generates a little chunk of Arduino code. You copy into your sketch, And then all you have to do is kind of set up all the modulation, like, oh, I want to have the pitch change, and I want to have the envelope change or whatever. And that sound is made to sound like CD quality.

Okay. And so I've been playing with, on the sort of higher quality and playing with teensies. And there has been a port of the teensy library for the SAMD-51 ships, which are like the Feather M-4s, and that's pretty good too.

I think the audio quality isn't as good as on the teensy, but I've not looked into this much, because I actually kind of like a lo-fi sound. It's kind of fun. It kind of reminds me of the 80s almost, you know?

Paul

Oh, it totally does. And I said it to you on Twitter. It takes me back to those John Carpenter movies, like the thing or, you know, any one of his movies that he composed the music for himself, because that's all he does is synths. No, totally. I'm instantly transported to being a kid again.

Tod Kurt

When the only sounds you can make are 80-style sounds, I've been making 80-style sounds because of the fact that, like, okay, this is what I can do. And so that's what's, once I actually start playing around with the tainty stuff more, I might make stuff that sounds like it's from the 90s maybe.

Paul

Okay. Got a little grind in there somehow.

Tod Kurt

That's right. Some distorted guitar samples.

Paul

So what does CircuitPython need to do to kind of catch up in that sound space? Because I think a lot of what you described it can't do today.

Tod Kurt

Yeah, not really. One of the really interesting things is that CircuitPython just out of the box supports the ability to play a wave file, which if you ever try to do that in Arduino, it's a real pain in the butt. Because CircuitPython has all this other stuff happening.

for it. It's got the idea of a file system, you know, like a directory with files in it. It's got the audio driver, low-level DMA stuff set up on almost all the chips that it supports.

And so you can just say play wave file, like audio.complay and give it a file name and it'll play that wave file. And that's amazing. And you can even tell it to loop, so it'll loop seamlessly. So if you've got a perfect little rhythm sample and you just help to play, it'll just keep playing it. And that's great. And it's even got an audio mixer object. So in theory, you could have multiple wave files. You just tell to play.

And they can then like overlap each other. And so you can kind of create a little, little sample player. Interesting. I did not know that. So there's a couple problems, though.

One is that you can't really change the pitch of the samples without changing the sample rate of the entire system. So basically you could change the pitch of everything, but not, not of just one sample. Yeah, that could be a challenge. And doing pitch shifting is a non-trivial task. So it's not like, oh, I didn't these bozos think of this.

No, no, it's actually a really hard problem. And the other thing is the audio mixer seems to not quite work for, in some of the cases, I was using it with. And so maybe I'm just using it wrong.

But I was having a hard time getting the audio mixer to work with more than one object. So, but then there's the whole, that matches like sample playback. If you're doing synthesis, like what I was talking about with Mazi and with a teensy audio library, that's a whole other can of worms.

It's very similar in that you often create a small. all buffer that's sort of like a sample, the thing gets played out, and then you just refill that buffer and just keep playing it out. There's a whole level of I don't know what I would say, like just objects and a framework for how the data gets fed regularly into the system.

The Teensy Audio Library has solved a lot of this, but it's solved it in an Arduino way, which is you can make a lot of stuff very efficient at compile time with Arduino that you can't do in CircuitPython because CircuitPython, everything is done at runtime. Right. And so there's, I think, the taincy audio library and Mazi does a bunch of stuff where it allocates a bunch of buffers statically and sets up pointers to them in various ways statically so that it's all very fast and efficient and can operate a maximum rate. And you just can't do that in CircuitPython because of everything kind of, the system doesn't know what libraries you're going to load when you say import library name. And so it has to be very flexible and that flexibility comes at a cost of speed. But I think it's possible. There is an open issue on the Circuit Python GitHub for adding the teensy audio library. So if anybody has any thoughts on how to do this, please add to the discussion there because I'm super, super excited to see it happen.

Paul

We'll link to that in the show notes as well. So the takeaway there is audio is hard and we need someone to come help us get sense on circuit by that. I think it's within the realm of possibility. One thing at a time. Yeah.

Hi, it's Paul. I'll get you back to the show in just a moment. I wanted to say thank you for listening. If you like the show, please hit the subscribe button, write a review or tell a friend.

You hear that a lot, but it really does help. For other ways to help the show, visit CircuitPython show.com slash support. Now, back to the show.

So you started using circuit Python, after all those years of Arduino to kind of start to learn Python, see Python itself. How is that journey been? Has it been easy to pick up some of the big Python stuff, starting with the smaller building blocks? Oh, very much.

Tod Kurt

Yeah, if you have not learned much Python, I would say just ignore all the other Python stuff out in the world and try CircuitPython first, because Python is used for a lot of really big projects, and there's a lot of heavy prerequisites that can be used for doing what are seemingly simple things. And, like, for instance, oh, I want to, like, I want to brighten this image, and suddenly you're installing NUMPI this huge numerical analysis package, and like, no, no, I just want to brighten this image. You know, it's like, I don't want to, like, load up this gigabyte library for Python and that requires all these C library it's like no, no, no. It's like choose a smaller thing.

Like maybe choose, I want to build a small robot. I've got two little light sensors and two little wheels. And I, you know, because like I, you know, I've been programming C for most of my life.

And I'm a big believer in the curly brace. And the idea of not having block markers like Python, you just indent to indicate a block. It just didn't make any sense to me.

I still have hard time with it sometimes as a way of Python can do so much and CircuitPython is a really interesting way to think about microcontrollers because it's this very high level like it has a much higher floor than Arduino you start out being able to add strings easily. You start out having a little file system with a bunch of files you can just read from you can store like a JSON file for configuration on the circuit pie drive and just load it up and say okay how much is it to behave. you can then write back to that file if you want to save the state of your program.

These are things that are really hard to do on Arduino, and they're just like, bam, easy. You don't have to think about it.

Paul

So it's much more like using a computer, right? I'm used to saving a file on my drive. I can save a SecretStap Pi file with my wireless ID inside of it.

Tod Kurt

Exactly that. And so for doing, but at the same time, it is super constrained. You can't do everything, all the possible things you want to do on a computer with Python.

You can't do insert a Python. on motion CircuitPython boards you can't access the internet. You can't draw to a screen because there's no screen.

And so it's a fun like sort of micro-universe of a problem. It's like, okay, well, I've got the ability to read buttons and I've got the ability to write to a little LED strip. And just that will teach you a lot about how Python thinks about data structures and about Python thinks about structuring code.

And so just thinking about the small parts of Python for me was really helpful because now I feel like I can actually look at the larger projects in computer Python, desktop Python, and go, oh, I see what they're doing. Because I looked at trying to do a static website generator that was using some Python framework. I was just like, man, this is assuming a lot of knowledge about how Python thinks that I don't even have because I don't know how Python thinks yet.

And CircuitPython kind of helps you think about Python the way Python thinks about itself.

Paul

Well, that's the beauty of being built on the backs of giants, right, between C Python and MicroPython doing a lot of that heavy lifting to help get us where we are today with CircuitPython is just absolutely

Tod Kurt

amazing. Yeah, exactly. And so one of the differences between CircuitPython and MicroPython I think is that Scott with CircuitPython has very explicitly tried to make CircuitPython work like and look like normal desktop Python.

Whereas MicroPython is okay with saying, okay, we're going to go away from how desktop Python does things because it's less efficient because we want to do these micro control or specific things. And so there's like, that's two different ways, two different philosophies of approaching the problem. And they're both valid.

You know, like I use MicroPython for some things. But if you are looking to learn more about how desktop Python works, doing CircuitPython will be, I think will help you more.

Paul

I agree. And, you know, I came late to the party. I didn't learn how to code until I was well into my 40s. Oh, wow.

And started with Python. This is, you know, four or five years ago. So coming to CircuitPython was a little easier.

You know, the code's readable. I understand what it's doing. But whenever I talk to someone and they're like, well, how do you know what you want to build or what you want to do?

I think the best part about CircuitPython is go to learn.adafruit.com, and I don't mean to sound like a commercial forum, but there's 2,000 guides there. Wow, that's that maybe. Yeah, that's awesome.

If you're one of those people that learns by hands-on doing, they've got it all laid out for you. Here's the parts you need to buy. Here's what you need to do.

And then go try and hopefully it works. Yeah.

Tod Kurt

There's a great amount of learning to be had just by going through the GitHub. for various CircuitPython libraries, be the Adafruit libraries or other libraries, just go like, oh, you know, how come the neopixels look like a list where you can do a little like subscripting of like, you know, zero, one, two, three to access the zero's one second LED? It's like, how is it you can do that with an object in Python?

It's like, well, you just look at the neopixel library on GitHub being, say, oh, there are these special functions you can do. And everything is an object. It's Python.

Yeah, yeah, no. And so it's really, it's really, cool. I see a library doing this interesting thing. How does this library do this interesting thing? You just look at the source code and go, oh, I see.

Paul

And that's the beauty of it being open, open source and free software is we can keep giving back. You can learn from it. You can modify it.

Tod Kurt

You've got to love it. But I must say there are some Python things, some circuit python things that have totally just kept sleeping out of my brain. And so two years ago, I forget what it was, but I started, because I'm a big fan of these little cutie pie, things. I started a QDiPyTrix GitHub repo that was just a list of things of me. It was around Halloween, so a lot of the tricks are how to do Halloween-themed sort of things. But it was essentially a list for me to remind myself, oh, how do I control a servo? How do I read a button?

And then Halloween passed, and then I decided, you know what, this really should grow into a larger thing. So I made a CircuitPython tricks repo. There's just a list of all the same things.

So I always go back to that. I'll like, Oh, that's right. How do I do a debounced button?

Oh, that's right. I use this library and I create the button this way. And it's like, how do I?

Paul

It's fantastic. I was just looking at your repository. There's over 50 tips and tricks in there.

There's that many now. And it's like I'm mentally marking them down as I'm reading in my head. Like, I need to make a note of that.

And that, oh, that's how I do that. So that's awesome that you shared that with everyone too. I mean, you know, I got to write things down as I get a little bit older.

So I totally get where you're coming from. to take that extra stuff and actually share it out. That's fantastic.

Tod Kurt

In my home directory on my laptop, I have a Git dashhins.t. A Imagemagic dashhins. TXT, image magic is a tool used to do various image editing on the command line. I have all these text files, just like me writing down things that I've typed into the command line to or typed into program languages to remind me like, how do you do that? Like, how do you list all the tags and Git? Because I always forget that.

Paul

Well, that's my biggest problem, right? And I'm sure other people do this is I've learned a program, but I go solve my problem, and then I don't have to visit it for another six months. So when I come back six months later, I'm like, I really wrote that code?

So this is a genius idea. This is why Stack Overflows, like the most popular website or whatever. All right, well, next up, we have a segment that I call Turn the Tables.

I mentioned earlier, I'm a big vinyl record fan. I've been asking all the questions. Here's your chance to ask me anything.

All right.

Tod Kurt

I'm going to have a little prologue to this. Right now, as we're recording this, it's at the end of January where everyone in the community, or a lot of people in the community, sort of post their public wants and desires for CircuitPython, either their personal desires or the desires for the language. And mine was, like, let's have an audio engine, like for synthesizer type stuff. Do you have any desires for CircuitPython in the next year?

Paul

Off the top of my head, I don't. And the reason being is that I'm still fairly new to the community. I've been lurking for the last year, maybe a year and a half, but I'm still getting to know a lot of folks, and the podcast is a great way to do it. I'm not ready to jump out there and say, these are the things I want to see from CircuitPython.

I'm excited to give back what I can, right, starting a podcast, blogging a little more about my journeys and the things I'm trying to build. It's a great question, but I'm still at that stage where I'm just soaking it all in, trying to figure out, okay, who does what, or where are those gaps? Because I don't even know what I don't know right now.

Tod Kurt

Totally, yeah. That's the problem you all have, right? So besides the podcast, what other CircuitPython-related projects are you anticipating for yourself in the coming year?

Paul

My PiyPortal just arrived yesterday. So my big project is I built a, so again, I'm a big vinyl record fan. I'm just going to, you know, like a broken needle, keep making bad jokes about it.

But so I built a website using Fast API, and it's a random record generator. So I've got about, let's say, a thousand records. I hit a button on this website.

It says, hey, go play this record. so I get up, I put it on, I come back in my office, and my record players in a separate room, and I had it so I could draw an 8-bit map on a 64-64-l-D screen of the cover art of what was playing. So I'm using MQTT, it will send a message that if I'm the one who requests the random record, push that image to the Pi Portal now.

I'm going to change it out for a Pi-Portal so I can get a higher-quality image and see the cover art of whatever's playing. I can walk 10 feet and pick up the record, But it's one of those things like I mentioned earlier. I learned by that hands-on.

And this has got a little bit of everything, right? There's that C-Python and building a website, which is hard enough to, I had to build my own MQTT server, which still the server is running. I haven't figured out how to use it.

So, you know, one thing at time. And then learning all the CircuitPython that goes on the boards. And my first couple tries with the Matrix Portal I was running into out-memory errors.

So that was fun. And I literally do mean it was fun learning. about memory management and CircuitPython and what the constraints are there.

It wasn't fun that it wasn't working when I thought it would work, but eventually I got it there.

Tod Kurt

To kind of go back to the whole Internet of Things stuff that we kind of started with, this is one of the biggest problems that I've had with people advocating the Internet of Things stuff, is that to be a really good participant on the net nowadays, you have to have a pretty deep networking stack. It's not just, oh, I can can get an IP address from the DHCP server and I can make this request. It's like, no, no, you've also got to do it securely with HDPS or TLS, whatever.

You've also got to have certificate management so for when the certificates get expired or whatever. And there has to be a mechanism for updating the system for when the inevitable problems happen in the underlying libraries because there's usually like, you know, some crypto library that gets bonged and so you've got to like update that. And so that's a lot of effort to put into a tiny market controller.

and the fact that Circut Python can fetch you or else at all is amazing. But it's often frustrating because a lot of the data sources that are out there assume that you have the full weight of a computer behind the thing fetching. And it's like, no, no, I just want 10 kilobytes of data.

I don't want this 1.2 megabyte XML or JSON file you're given me, let alone parsing that. And so a lot of times when you run into out-of-memory errors, when you're doing network fetches with CircuitPython, it's probably because the data feed is just too big for the RAM on the chip. And it's not really a fault of CircuitPython so much.

It's the fault of the fact that we've got a technical culture of the feeds are always the biggest feeds possible because we won't include all the information. And there's no way of including asking for summaries or something.

Paul

And so like you said at the beginning, We've taken, in 2007, the iPhone launched, we take for granted having these supercomputers in our pocket, right? If I want to pull my phone out and check the scores on ESPN to see what the latest football game is, they can deliver a big JSON packet with all the team, scores, times. But if I only want that one little team, yeah, I can absolutely see how memory being constrained on a microcontroller is very different than what we want to do with our smartphones.

Tod Kurt

Yeah, like before the iPhone, there was this thing called WAP. Wireless Access Protocol, I think. I wrote a couple of websites for this, and there were phones that had WAP browsers on them, and they were a special cut-down version.

Even HTML was too big. It was a special cut-down version of the tag language of HTML that was minimal, and you'd create a separate little index page instead of the normal index page, so you could browse it on your little Nokia phone or whatever. And it's sort of that, We need that level of ability to funnel down the data feeds that are out there, that like Circa Python is perfectly capable of fetching, but it's not capable of fetching at all.

And so, you know, maybe, yeah, since we probably can't change the world to have the ability to have succinct data feeds, maybe we could create some sort of a streaming parser in CircuitPython, or maybe someone just like, like, Adafruit came out, like AttaFruit IO, their sort of MQTT server thingy, has some ability to do some sort of collapsing of data feeds, I think for certain data types like time or date or something.

Paul

It does, and I know on the PyPortal, you can even send it a photo and I'll send you back the bitmap to get that size down.

Tod Kurt

And so if there was like a more extensive version of that where you could, I don't even know how one would configure it, but you could give it a big data feed URL, and you could tell it which parts you wanted. Like, oh, I only want the artist and title or something.

Paul

Almost like build your own API out of the feed. Yeah, yeah, exactly. Tod, last question for you that I like to ask each guest.

You're starting a new project or prototype. You reach for a microcontroller. Which one is it?

Tod Kurt

So I think in the world of CircuitPython, it might be useful to ask what board should I not start on? One of the sort of like super starter boards was the CircuitPython Express. It's got the SAMD21 chip on it and has an extra flash chip for more memory.

Paul

Yep, that's the one I started with.

Tod Kurt

Yeah. And so in early CircuitPython, and in our digital. We know this is an amazing powerful chip, but as CircuitPython has grown up, its memory requirements have grown a bit, and also the things we want to do with CircuitPython has grown.

And so you start to run into lack of RAM problems pretty quickly on this board because of the chip that's on it. And so I normally issue people away from the SAMD21-based boards, like the Circuit Playground Express. Okay.

And so now, and also because of the global component shortage, the global electronic component shortage we've had for last couple of years, getting the chip that's on this and similar ones has been hard. And so that's why you've seen a lot of RP2040 based boards and a lot of ESP 32 based boards because those two manufacturers have had a different resource allocation budget or something. So they actually have chips available.

And so I would say, so it is the itsy-bissy line from Adafruit, which is not a lot of love because there's the more powerful feather format that's basically the same thing, but a little bit bigger. It has like battery circuitry. This has no battery circuitry, but this also has a level shifter up to five volts on one of the pins for driving neopixels.

So if you're into LEDs, this is a good one to get. Yep, three to five volts can make a big difference in how bright. Yeah, yeah. A lot of neopixel strips will work just fine when you feed them with a three-volt data line, but a lot don't. They get like weird flicker.

And so like, hey, just avoid the problem, get the level shifter built onto the board. So that's if you want to like start. if you're like an Arduino, like a fairly experienced Arduino person and you're used to breadboards and all this kind of stuff, and you used to, you used to doing like little jumper wires and things like that, then the ITSI, I think, is one of the best deals.

It's like pretty cheap, cheaper than the feather because it doesn't have all the battery handled or circuitry. And of course, you know, Arduino and CircuitPython. If you're not in like a coming from Arduino and you're kind of coming to CircuitPython from like just the computer world, and you probably want to be doing a lot of networky stuff. So I'd say use a board that's based off of the ESP32 S2 chip, which is a Wi-Fi chip that can run Circa Python.

And one of the best boards I've found for this is the Adafruit Funhouse, which has a really great high-res 240 by 240 LCD screen on it. And it's got a couple of buttons, and it's got a couple of cap sense, touch sensors, and it's got a little thing up here for a motion detector. It's got a beeper on it and a bunch of like you know, I.O. Connectors on the side.

It came with a little plate, the laser cut plates, you can, like, hang it on a wall. But it's super handy because, like, you know, when you're doing Wi-Fi stuff, having a screen to tell you what the heck is going on, can it find the Wi-Fi? Is it connected to Wi-Fi?

Can it find the server it's trying to send data to? There's all these ways that network devices can go bad. And so having a screen can be really easy because CircuitPython will automatically use a display as its display outputs.

Even when an error happens, when it airs out and crashes, it'll print the error message on the screen. That's super handy. If you want something a little cheaper, there's a really great board using the same chip from a company called Lily Go.

They're available on Ali Express. And the cool thing about this is if you can see, it's got a little SD card holder on the back so you can actually put more memory on it. So you can store like a whole bunch of data, like if you're pulling data down from the internet or if you're pushing data up or whatever.

It's only got, I think it's got one button that's usable. by the user on the front, which isn't that cool. But the display is really crisp and clean and fast.

Also, the antenna on this is a bit better, I think, than what's on the Funhouse. So I think it seems to get a little bit longer range. And they'll just like, you know, it'll be there in a couple of days.

Ali Express could be a month. Yeah, exactly. And the other nice thing is that if you're getting started with CircuitPython, and you want to play with a bunch of the interesting sensors based off of the Stemakut protocol, it's got a stem a QT jack so you can just start plugging connectors and start plugging sensors in.

And so that's kind of my two forks in the road. Is like are you an Arduino person wanting to play the CircuitPython, then use the ITSE. And if you're a kind of Python person wanting to get into CircuitPython, then get something like the Funhouse.

Paul

Well, those are great picks. I'll make sure that I linked them in the show notes too for those. Yeah, yeah. Can't see us through the podcast.

Tod Kurt

Yeah, I'll give you links to all these if you need them.

Paul

Awesome, perfect. Well, thanks again, Tod, for being on the show.

Tod Kurt

Thanks, man.

Paul

Thank you for listening to The CircuitPython Show. This was episode four with guest Tod Kurt recorded February 1st, 2022. Thank you for listening to The CircuitPython show, an independent podcast with the people in and around CircuitPython.

For show notes, transcripts, and to support the show, visit CircuitPython Show.com. I'm your host Paul Cutler, and I'll be back next episode. Don't forget to hit subscribe and stay safe. You know,
