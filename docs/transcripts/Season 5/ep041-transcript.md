---
date:
  created: 2025-03-10
title: "Episode 41 - Writing a CircuitPython Library for the Community Bundle"
---

## Show Notes

[Show notes available here.](../../episodes/Season 5/ep041.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by returning guests, Tod Kurt, and Jan Gouldsby to talk about CircuitPython's community bundle of libraries.

Tod and Jan, welcome back to the show. Hello, Paul. Hi, thanks for having me.

Hey, Tod. Hey, hey, Jan. So we're here today to talk about the community libraries that are available on CircuitPython.org.

There's over 500 different libraries split between the official Adafruit Library bundle and the community bundle. chances are if you're listening to this podcast, you're familiar with the official Ata Fruit Library bundle. Let's talk about the community bundle, which has over 150 bundles created by community members.

How do you define the community bundle?

Jan Goolsbey

Well, I've been using the community bundle for probably about two and a half, three years now. And it was my first exposure. I'm not a programmer.

So it was my first exposure to different kinds of coding styles. and it helped me pick up and learn a lot about CircuitPython, but it also gave me some utilities and things that I could use to kind of enhance my code. So CircuitPython had both those features for me initially.

It also provided that community sharing that I thought was important, especially in my own growth.

Tod

Yeah, yeah, that's for me. I've been using the bundle since it existed, and it's where I've been learning most of my Python from, honestly.

Paul

That's interesting.

Tod

I would have never thought of that as a learning tool. Yeah, yeah. Just like, how does this class work? Well, let's just look at the source code because you can just download the bundle the bundle of bundle and zip it all and look at it. It's really handy.

Jan Goolsbey

Well, and it's wonderful for getting that kind of information because you don't have to waste some experts' time in your process of learning when you're really low on the scale and trying to figure out, you know, how do you get a four next loop kind of thing to work in a while until. And you can do that without having to face anyone and be embarrassed by how poorly your code looks. Totally.

Tod

So how do you know when your code is ready to be submitted to the bundle? I would say if you've gone to the trouble of making a Python class to solve a problem, there's probably a good chance that it could be useful for other people. And so that's where a lot of my libraries have come from.

I spent the, I spent the, whatever it was, hour to get it. it working and I'm like, well, I've got a class now. How much longer could it take to add the rest of it to be publishable? And depending on your predilections, it could be another hour or it could be

Jan Goolsbey

like a week. That's kind of my threshold too, is if it can stand as a class, a class object, then it's something that might be useful to someone else because that's how they can insert it into their code as another object that they need.

Tod

Yep.

Paul

So let's talk about the process to create a little bit. Adafruit's tried to make it easy to contribute by using cookie cutter an open source project template package. What kind of information does cookie cutter walk you through that it needs?

Tod

Well, I mean, like there's the obvious things like the, what is the name of the repo that it lives at? What is the name of your class of the library itself?

Jan Goolsbey

Well, it does ask a lot of questions. And it says, where's your documentation? And, you know, is this a driver or is this a helper? Some confusing questions like that.

Tod

too. Yeah, it is more geared towards Adafruit employees, it seems. And so like some of the questions that asks are things that you can just say nothing to because it's not applicable to you.

Jan Goolsbey

Yeah. And matter of fact, it's okay to skip over some of those things. If your documentation's not ready yet or like me, I don't want to create an account out in for Sphinx or for read the docs, some of the things that would be good to do if I was a full-time programmer, but I'm a hardware guy. and I only do one or two a year, so I skip those steps, and I try to provide as much documentation in the code as possible, of course. So you can kind of look at cookie cutter as this thing that will shape the cookie for you, but you can put all the sprinkles on it or take them off or whatever.

Tod

If you were to go full on with what cookie cutter provides, what you would be making is not only your Python code, your class, but you also are required to create some examples, at least one example, create some documentation in the read-the-docs format, make sure that it passes the PILENT and rough RUFF, Linter or whatever, and also release it on Pi-Pi, the Python package repository in addition to this thing. Most of those things are optional, which I didn't realize, and it was looking at some of JAN's libraries that I realized, oh, look, you can just not choose to do the Pi-Pi stuff, not choose to do the read-the-doc stuff. And that makes it a lot easier.

Jan Goolsbey

You just don't do it. But I'm not trying to be too flippant about that. It's really that I don't have a lot of those skills yet.

And I'm trying to develop those skills as I write these libraries and other code. And I know that all those things are very valuable, especially in a professional environment where if you're trying to share too and maintain these things. So like I said, I'm not trying to be too antisocial about doing this stuff.

But it kind of distracts from my primary objective in that is let's get something out there to share.

Tod

Yeah, I think that's a really good way to do it as sort of the tiered or the staggered, or not staggered, staged, staged approach where I just want to get my library up and into the bundle so I can have my buddy try using it and see if it works for them. And you don't have to have all those extra bits working just to get it out there.

Jan Goolsbey

Yeah, the probationary phase is my code. I go through a lot of probation with my code.

Paul

The bundle also uses pre-commit. How does pre-commit help you get your library ready to be published?

Tod

Yeah, that was really fascinating to me. I'd never really experienced that. When you change your code and you say get commit and you use a say which files to commit, It'll just commit it and push it up to GitHub or whatever.

But with pre-commit, it will run some code. And the cookie cutter setup has it run a bunch of different tests, a bunch of different linters. Like it used to be, it would run both Pylent and Black.

I think now it runs something else called Rough, RUFF. I don't know if they still use Black, but it was really strict. And it had thoughts about how Python should be formatted that I didn't agree with.

And so I really dove down into figuring out What are some of the things you can tune on black to make it a little less persnickety? Because the whole point of the way that pre-commit was set up is that you can't push your commit unless it passes the black or the lint checks, which is really important if you're working in the team, which we all are with the community bundle.

Paul

Yeah, Ruff Replaced Black. Ruff is a linter written in Rust, and it's super fast. I've used it in C-Python. I haven't had a chance to write my own library and actually go through this process.

Jan Goolsbey

You know, I think those steps for me were pretty important and kind of in my learning process. Lenting and the case of most of my libraries going through the black formatter, those taught me a lot about how to communicate my code to other people and how to put it in a format where they could recognize what I was trying to do and what I was trying to say. In other words, it helped with the ongoing maintenance of it as well.

Initially, I was kind of confused by most of the linter messages I got. And thank goodness for people like Katni . She really, she got a lot of calls from me.

And she helped me out and helped me learn a lot about that as I went through that process.

Tod

Yeah, yeah, Black was really particular about making sure you document all the methods of your class, which, you know, to you, in the depths of all, you're like, well, of course it makes sense that this method called Frobbnitz, it's clear what it does. But even me two weeks from now, I won't know what the method Frobbnitz does. But thankfully, Black would have made me write a little like one or two line description as to what this stupid method does.

Jan Goolsbey

Yeah, I had a couple of libraries I submitted where the documentation exceeded the length of the code. So when you look at that, and I don't know what the measure of success is there, If you have 80% more documentation and 20% of that is code, I don't know what the, but I had at least 50 or 60% of the documentation was explaining what my algorithms were and the algorithms were about the remainder. Yep. That's about the size of things usually.

Paul

One of the things I really like about the process is that Adafruit does require you to write documentation, which we just touched on a couple minutes ago as well, including the read me and read the docs. Do you think community libraries should be held to a similar standard as official libraries from Adafruit when it comes to documentation?

Jan Goolsbey

Well, I do have an opinion on that being, you know, I keep touting the fact that I'm not a programmer as if that's going to be some sort of a shield that I can hold up here to say, I'm not going to do the documentation. And I'm not going to, well, anyway, I think I'm someone who really documents a lot. My code has, just by my own nature, I try to, well, I try to talk to the future Jan who says, I don't remember why I did this.

And so I'm probably way more verbose than I need to be in a lot of cases. But I do think that there is some limit there that holding everybody to the same standard of a high level of detail in their documentation may actually kind of thwart their creativity or make. them feel a little bit insecure about submitting their code if they don't really know what to expect in terms of the level of detail.

So there's probably some middle road there. I'm not articulating this very well, but there's some middle road there, I think, where perhaps we allow a little bit more leeway in terms of the quality of the documentation and then just provide a lot of comments and provide a more helpful approach to that.

Tod

Yeah. I've been really liking some of your documentation because the read the docs formatting, whatever it's called, the language, makes it hard to do some things that are easier to do with other types of documentation. And your documentation has had like little animations and stuff and various graphs and diagrams to explain what's going on.

And that's, to me, harder to do in the read the doc stuff. But at the same time, I find a little bit of comfort when a library has a read the docs page. And so that's why I've been striving to make it from my life, is trying to try to make even just a minimal read-the-doc thing.

It's like, oh, it looks like all the other libraries that I see.

Paul

So you've written documentation, you've written your library, run it through cookie cutter. What are the next step to actually submit it to the community bundle?

Tod

I believe the main thing is you just go to the community bundle repo and edit, I think, just one file that is the list of the module. And I think it's a markdown file and you just add a link to your repo and add a link to your documentation page if you have it. Oh, no, that's right.

You edit another file that is the Git submodule for your library. So you edit two files. The markdown documentation that links to your repo and then a Git submodule that links to the repo of the code.

And then you submitted that as a PR. The PR gets accepted maybe a day or two. and then the next build of the bundle, which happens, I think maybe weekly, will have your library in it.

Jan Goolsbey

And if I look at my list of things that I forget to do when I'm submitting, one of them is be sure to release the code in your own repository before you try submitting it because the automated process will just ignore the fact that you've got something there unless it has a current release. That's one local step that you have to do in your own repository.

Tod

Yeah, and that's one of the, of the nice things that because the bundle build process requires certain files to exist in your repo's release latest release thing and the cookie cutter template has an action release action that will build some of those files for you so you don't have to do it yourself I'm pretty sure like one of the problems is that while there is a documentation on creating the sharing a CircuitPython library some of it's a little out of date because things have evolved like it was originally I'm looking at the page right now. It was originally created in 2017, and it was last edited January 22nd of this year, 2025, and the last major update was January 11th of 2022. So, you know, things change.

You have to kind of steal your toes. And more than once, I've popped into the Circa Python Dev Discord channel with the big question marks of what the heck is going on? I'm trying to make this library, and it's like give me weird errors.

And people are like, oh, right, we just did this change. to the template.

Jan Goolsbey

I got used to the fact that the requirements would change occasionally. Either that or I forgot what the requirements were.

Tod

Yeah, both.

Jan Goolsbey

It's not a simple process for someone who doesn't do it for a living, I think. And although I value the steps in the process for what they produce, I don't remember them from one submittal to the next. And so having the learn guide handy out there and my list of things that I forget when I'm doing this, Those get me through it each and every time.

Tod

Yeah, I've got my own little script that I run. It's called something like atafruitCircithonlibrin library development.tt. It's in my home directory. Just a list of things to make sure to do. Now, there's a good idea.

Paul

Once the bundle's been built weekly, the new library will be available in Circup. Is that correct?

Jan Goolsbey

Yes. And Circup is such a handy tool for the community. libraries. I think if there's no other benefit to putting something in the community bundle, Circup will pave the way. In other words, you can share your library very quickly because Circup makes that simple. I think the case where you've produced a library and you want some friends to test it, Circup is the best way to distribute that. Yeah. And if you're listening to this and you've

Tod

not, and if you use CircuitPython and you haven't tried out Circup yet, please use it. You can just download the library bundles, a zip file, it, unzip it, and pull out the various files you need. But circup makes it so much faster to do all that.

I really wish there was a more web-based way to discover the libraries that are in the bundle. Like right now, you can just go to the repo and just look at all the various modules in the list as a big markdown file or whatever. But it'd be nice if there was some sort of like online circup browser almost where you could type in a search term and it would like give you the libraries that might match or something.

and kind of like the way Pi Pi does it, because Circup is a lot like PIP, but for CircuitPython.

Paul

What advice would you have for someone considering sharing their first library?

Jan Goolsbey

Well, I think probably the best advice I would have would be, we talked about this a little bit ago about if you have a class object that does something useful, useful to you, it's probably useful to someone else. We talked a little bit about that litmus test. The other thing is you may have something that you've done that's pretty unique.

And there are libraries that I submitted out there because they were kind of unique in my development as a programmer. And one was a light sensor that I wanted to be able to use just a simple phototransistor to detect a motion across the front of a pie portal and detect a shadow so that it could see that I. I waved at it. Using a photo transistor to do that is a difficult thing to do because you get, you know, the LED lights that were using overhead. They produce a lot of noise, actually, that kind of looks like gestures. To make a long story short, I had to put some algorithms in there to filter out the light and make it so that it would work with any photo transistor and work with any lighting condition. So it was a very unique library to submit because of the work that I into that to make it useful for me, for my project. And that gave me the indicator that I thought, okay, there's some value to this that somebody else could use.

Tod

That's really fascinating. I didn't know you made that library. I remember seeing it in some project, maybe it was your project that I saw it in, but this to me makes me think of another reason why you should put something in the community bundle as an archival action for your code. You know, it's like, I've written so much code that I'm like, where did I put it?

You know, it's in some repost somewhere for some project that I did five years ago. But it was in the bundle. They were like, oh, maybe, you know, is that?

Jan Goolsbey

Oh, yeah. Yeah. I often wipe my brow, wipe the sweat off my brow after worrying about finding something and just being able to bring it in from Circa.

Tod

Yeah. So having the other thing I like, oh, sorry, go ahead.

Jan Goolsbey

No, I was just saying, having it out in the community bundle is saving me a lot of labor too because there are libraries that I use that are mine and others that come from the community bundle and I use them often and it really makes it convenient even just for me. It's not just about sharing. It's about making it available for your own use.

Tod

Yeah. Yeah. One of the things I really like about the process of making a library for the bundle is it makes my libraries better because I actually sweat some of the edge cases or different possible ways to library could be used that end up benefiting me because at the time I didn't really know I needed it that way. And then like a week from now, I then find out I do need it that way and I've already written it and published as a library. So it makes me more serious about the code,

Jan Goolsbey

I guess, that I'm writing. And you receive comments, believe me, you will receive comments. And it's very useful. I don't think I've ever received a comment that didn't have some use, either in the current version to fix something or for some features I hadn't even thought of for the future version.

Paul

So are users leaving comments or bug reports in the GitHub repository that you created for the library? That's where I receive them, yeah. Interesting. Is there a way or a path for a community library to be officially adopted by Ata Fruit?

Jan Goolsbey

I think of the three of us, I may be the only one here that it's had a library go from the community bundle into the regular CircuitPython library bundle. And there was no clear path for that. It was something that I created a couple of years before Adafruit had a product that was similar.

It was a driver that I wrote. So they produced a board that would kind of match the board that I made. And the library that I had for that was one that I was, I said, you can just have this.

I talked directly to Lady Ada and said, you can have this. I'll give this to you with no strings attached. You don't even have to put my name on it.

It's something that the community can use and you can get your product up and running right away on CircuitPython. They had an Arduino driver for it, but they didn't have certain Python. The process was fairly difficult to go through because they hadn't done that before.

And I can understand that, you know, you're trying to protect your own investments and you want to make sure that the code is going to be supportable and that you have somebody in place who's knowledgeable about it that can support it. And I think it was new for them to do something like that. But as a result, I still don't think that there's any documented process for doing that.

And it would be a great thing to do because there's some really inventive stuff out there.

Tod

Yeah. The example that brought this kind of concept up to me was there's these round LCDs that we were all playing with right during the pandemic, the GC9A01. Someone wrote a library for it that I quickly created a bunch of demos for because I was really in transfer these round LCDs.

and then lately, just like I think maybe two weeks ago, AidaFruit is now selling a cool round LCD using the same chip, and they have now their own library for Circut Python that is the exact library that's in the community bundle, which is copied over, I believe, with the author's permission. And I understand why they do that. They're selling this product.

They want it to make sure they have a consistent code base for their demos and stuff. But I really wish that it would have moved to the Circa Python org. in GitHub rather than the Adafruit org because there is a CircuitPython org.

It's not where the circuit Python source code lives yet, but to me that's where it should go eventually. And do we have in this process for graduating libraries to a third bundle because currently there's the Adafruit bundle and there's the community bundle but what if there was a third bundle that's like the official CircuitPython community where maybe there's a process whereby the libraries are vetted for actual functionality for continuing to work when the versions of the CircuitPython changes. And like, you know, things that, as circuit pithing involves, the APIs for certain things change.

And so some of these libraries that are in the bundle might not work anymore. And who currently goes through and makes sure of that? In the community bundle, no one.

It's like each person owns their own library, you know. But if there was a third entity, a third bundle that's sort of like, these are vetted by the larger CircuitPython community, That would require organization and some organization body, not person body, to handle all that. And we don't have that yet, but we could.

Jan Goolsbey

That's a fascinating idea. Thinking about CircuitPython as a community of its own, not just the aspects of it that are sponsored by Adafruit. And it might also mean we could get T-shirts. Definitely.

Tod

More CircuitPython merch, please.

Paul

Do you both use the MIT license for your libraries? I know that most of the Adafruit stuff is licensed under an MIT, which is very permissive, which would, you know, like you're saying, Tod, allow them to take a community library and just copy and paste it over to their own.

Tod

Yeah, for me, I don't know. I think so. Like, I have some issues.

I'm a real open source sort of zealot sometimes. And so I have issues with the MIT license because it means that any anybody could use their library for anything. And so, like, there are some libraries I've written, I think, that I have under different licensing because they're based on code or algorithms from someone else.

And so I kind of try to carry forward that original license. But I'm looking at a couple of mine right now, and they have MIT license. So I think maybe I just, that's what cookie cutter puts down by default, and so I just have to accept it to the default.

Jan Goolsbey

And I usually use the MIT license, too. My former career, before I retired, was working at a research laboratory where we protected property through all sorts of mechanisms. And when I came into the CircuitPython realm and looked at the licensing of that, wait, this is way too liberal for me.

There's no way I can do this. After a couple of years of being instructed by a lot of folks in the open source community, I went completely the other way, and now I'm very open source about things. And MIT looks like a pretty good fit for the things that I'm doing.

Paul

Yeah. Let's chat about some of the libraries. You've both written.

Jan, we'll start with you. Palet Fader is one I've recommended to a number of folks. What does Pallet Fader do?

Jan Goolsbey

Well, Pallet Fader is the first element of a family of pallet tools that I put together. And Pallet tools, the palette is associated with graphics. So you have a graphics image you want to put on the screen, or you want to put it on a Matrix Portal or something, you know, that it's an RGB LED array.

Palat fader allows you to change the brightness of the palette. And that's suitable for, obviously, I was talking before about having a photo transistor detect light in the room. I'm very sensitive about making sure the displays, the brightness of displays are controlled so that they match the ambient lighting in the area that you're working.

So a pallet fader was first put together because you couldn't dim a matrix portal. The RGB LEDs there ran it, you had two brightnesses. They were either on or they were off.

Or you had to code each LED color separately to control its brightness. So pallet fader was something that I put together that dealt with the palette of colors, all the colors on the display, and would scale them up and down based on the brightness level that I wanted. And it would do other things too.

But the primary function was to make sure that you could control brightness. and on devices that didn't have a brightness control.

Tod

Yeah, thank you so much for that. Because I fielded so many questions on like the Discord or Reddit or whatever, people asking, how do I dim this LED thing when I've got it set up as a matrix? And it's like, well, you go through each pixel and you change the color by hand. Or you use Palatator.

Jan Goolsbey

The palletator took me down a rabbit hole that was kind of fun, too, dealing with other pallet issues because, you know, a palette that's associated. with a bitmap image is something that you can manipulate. You can treat it like a list.

So you can go in there and change the values of that list pretty easily. It lacked a couple of things that you could do with lists. One was slicing, where you could just update a few values in the list and not all the values in the list by replacing the palette.

So I've built something called pallet slicer that came out of the pallet fader experience. And the last one I did in the palette zone was the pallet filter. And pallet filter looks for a color or colors that are close to that color and substitutes a new color for that one.

So you can use that. It works great for green screen kinds of things. I use it in a weather display to slightly change the color of the, it's a Star Trek Elkhars display.

It slightly changes the color of it so that it's blue at night and it's yellow like on the next generation. The yellow screens that they used to have, without having to change the background graphics itself, I just went in and changed the palette. It was much simpler.

So Palafator, yeah, that was, man, Palifator is the one that got me into the community library too. That was one of your first submissions. That was one of the first ones.

I had another one called Range Slicer that was my absolute first. the pallet fader was a close second.

Paul

Tod, one of your libraries has my favorite name of a library. It's RUTRO-I-O. Say that three times fast. What does that one do?

Tod

So if you use rotary encoders in CircuitPython, you will most likely use the built-in library called Rotary I.O. Which takes two pins, and those are the two pins that go to your rotary encoder, and it can determine whether you're turning it left or right. The problem is on RP2040, to make rotary I.O efficient, it uses the PIO part of the RP2040 chip, which requires the two pins to be next to each other, like GPO9 and GPO10.

But on some boards, like I think the QDPRPRP2040, there can be situations where two pins that are physically next to each other are actually not logically next to each other. So it's like there'll be GPI-O-19 and GPIO-21 or something. And so you think you should be able to use Rotary I.O.

For these two pins, but you cannot. And so Ro Rotary is a way of sort of faking like Rotary I.O. Using the keypad functionality built into CircuitPython.

So like, let's treat the two Rotary I.O. pins as fake buttons. And then do some logic with that and pretend to be a rotary encoder to the user.

So it's like, uh-oh. I can't use rotore I.

Jan Goolsbey

That's brilliant. And does it do with the debouncing and stuff for what the RUTROH I.O. Would have normally?

Tod

This is the benefit of using keypad as keypad does all the debouncing for you. So you just look at keypad events and turn those into like counterclockwise rotation or clockwise rotation events instead. That's super.

Paul

Is there a hidden gem in the community bundle that you want to share with folks? Is there something that you use regularly that? that most people might not know about? Is there anything that comes to mind? I've got a few.

Jan Goolsbey

And, you know, I would count some of mine in there that I use a lot. And some of those are things like temperature tools and where I do temperature conversions. And another one is daylight saving time adjuster so that it will automatically change daylight saving time based on the date that arrives with the time.

But the one that changed my perspective was one that Jepler put together. It was called, let's see, Jepler's CircuitPython micro decimal or U-Decimal. And the microdesimal is a, it's a CircuitPython library that is used, just like you would use the Python decimal library.

And that library was incredibly important when I was working on a calculator. and I was trying to emulate an HP35 calculator. And when you're dealing with floating point on a microprocessor and you're trying to get accuracy, when you're out to 20 digits or so, it's just not there.

And emulating the HP35 that has 15 to 20 digits of accuracy was something I just couldn't do at the floating point. And using this microdecimal that Jepler put together, just saved the day. But the other advantage to that was, I found myself using it whenever I needed to do kind of pseudo-scientific work.

So if I'm measuring something, I'm measuring the speed of a motor or something like that, or I'm looking for a period based on a frequency that I've measured, and I need X number of digits of accuracy, and I don't want to worry about floating points, binary rollover and roll under and averaging whatever happens there. U-Dessimal really changed the game for me and thinking about those things. And I think that's something that I go to often.

Well, let's just say I go to that often.

Tod

For me, I think all of your palette tools, Jan, are super handy because one of the fun things I like to do with CircuitPython displays is just muck about with the palette, which really brings me back to sort of the old way that like, say, the Atari's and stuff used to do some of their animations. They just would have cleverly arranged palettes and they would kind of move the colors within the palette that would cause these like waterfall effects or cool banded color effects. And by having things that let you operate on pallets inside your CircuitPython code, you can do kind of fun stuff with that.

But some of the other other ones that I am a fan of is, of course, the GC9A01 round LCD, which is just so handy for the round LCDs. There's a one by, I forget it is real name, but it handles like L. Peckinan. But the Tommel library that lets you read and write Tommel files, which Tommel is yet another little configuration language that CircuitPython uses for storing things like the Wi-Fi password and SSID name.

There used to be, it wasn't in the bundle, but there was this non-blocking HTTP server library. I used a lot called Ampule that this is like four years ago, but now there's one in the library called Byplane that seems to be fairly similar. I've stopped using Ampul because the ATA Fruit HTTP server has gotten non-blocking, has gotten better over time.

Dan H put a lot of work into it a couple years ago. But yeah, I used to use a non-Aid Fruit HTTP library all the time. Oh, wait, wait, wait, wait, wait, wait, wait, wait, wait, wait, wait, wait, wait, one more.

Also, Jan's punk console emulator.

Jan Goolsbey

I was wondering if that would come up.

Tod

All right, so they're in sort of hacking means. music world, there's this thing called the Atari Punk Console, which is like two 555 chips that have been turned into little oscillators that interact with each other. And for some reason, it's called the Atari Punk Console.

I don't know why. But hundreds of them, thousands of them have been made. And Jan made a little Circa Python library that sort of emulates that using the PWM functionality of Circa Python.

Jan Goolsbey

And it can work in stereo. Ooh. Yeah, so think about that.

Yeah, coming from a. hardware background, the Atari Punk console was something I made many of with any 555s and 56s. And it was always on my list of things to do. It's got to be able to emulate this. And I had a grand time putting that together. It was a lot of fun.

Excellent. So thank you. I'm glad you appreciated that. Thanks for the comment.

Paul

Those are all great choices, and I hope folks who are listening try some of them out. Jan and Tod, thanks so much for making time and coming on the show.

Jan Goolsbey

Oh, you're welcome.

Tod

Thanks.

Paul

Thank you for listening to the CircuitPython Show. For show notes and transcripts, visit www.circuitpythonshow.com. Thank you to both Jan and Tod for coming back on the show to share their experiences writing code for CircuitPython's community bundle.

Check out the show notes for links to their GitHub repositories. Until next time, stay positive.
