---
date:
  created: 2025-02-10
title: "Episode 39 - Designing a PCB with Bradán Lane"
---

## Show Notes

[Show notes available here.](../../episodes/Season 5/ep039.md)

## Transcript

Paul

Welcome to the CircuitPython show. I'm your host, Paul Cutler. This episode, I welcome back Bradan Lane, who first appeared on the show back in episode 19, which I've linked to in the show notes.

Bradan, welcome back to the show.

Bradan Lane

Thank you. It's great to be back.

Paul

I'm excited to have you here. Designing a PCB is something I'm hoping to tackle myself this year, so I'm excited to learn more. Let's start at the beginning, and someone wants to design a board.

What tools would you recommend for someone just started?

Bradan Lane

So designing a board actually has one prerequisite before that, and that is figuring out what the circuitry or what the design needs to do. But jumping into what about designing the board, there's a few different tools. And, you know, there's third party and commercial tools, but the two within the bulk of the community that I keep seeing pop up over and over again.

One is a web-based tool called Easy EDA, and it has a small download module if you want to do it offline. But Easy ADA, first of all, is very simple in its user interface. It's very intuitive in its user interface.

And it integrates very well with one of the PCB manufacturers that we tend to use a lot. A big step up from that is KiCad. And KiCad is an open source project.

For years, it's been sponsored and funded by CERN. And so it has a permanent staff. It has, you know, a budget.

They know what they're doing. And starting three or four years ago, KiCad shifted to a major update every year. And that really got people on board because before that it was kind of, when are they going to fix this feature?

When are they going to add that feature? And so going to point releases throughout the year and a major release that people can depend on, you know, approximately every 12, 12 and a half months really gave people who were on the fence that last bit of nudge they needed to move it in. Now, the learning curve on KiCad, some people are going to say it's pretty steep, but the truth is the learning curve on almost any design tool is pretty stiff.

Getting the basics in there, you can do that pretty well with Easy EDA, and you can do that pretty well with KiCAD. The big advantage, for me at least, I went to KiCAD almost immediately, was it let me grow as a designer, whereas within Easy EDA, I started to bump up against its limits pretty quickly. That being said, the majority of boards that even I designed today could easily be done in Easy EDA if I were more fluent in it.

So those are the two that I kind of talk to people about. If I go into a school and I'm talking to students, I'm going to talk to the teaching staff and probably recommend Easy EDA. It also has an advantage in the academic space because if schools and stuff have like firewalls and lockdowns and they can't install software, EZ EDA is a browser-based solution and that works great.

So those are my two recommendations.

Paul

What are some of the tricks you use when you're first starting out designing a board?

Bradan Lane

There's a number of different types of boards, but the boards that I tend to design are feature boards, as opposed to, say, a development board. So if you think about a lot of what Adafruit provides and what Spark and some of the other groups provide, a lot of them are building development boards. These are boards with a number of pins that run down either side that are broken out.

And so you buy the board and then you start adding capability to it external to that. And I use development boards as a precursor to designing my own custom board. Then I will jump into designing my own custom board, which has all of those extra accessories or sensors built into and on the board.

So I start with a standard PCB breadboard and I stick a development board often from AdaFruit or a third party in the middle of that and then start sticking other components off the sides to, just make sure that I'm not out in left field somewhere. I don't need everything to work, but I need to know that stuff is going to work. So as an example, getting a touch sensor to work, well, getting a touch sensor to work isn't really difficult, but understanding the nuances of how a touch sensor changes depending on the size of it or its placement or what else may be around, is much easier to do on a breadboard than it is jumping immediately to a printed circuit board.

And again, I use various resources on the internet to help me kind of get that done. So then it's time to start putting it down in a design tool like Easy EDA or KiCAD. And the very next step that I do is I start looking for resources so that I don't make, you know, beginner mistakes.

And that comes down to the open source hardware community. And there's actually an entire initiative of open source hardware and there's registration and stuff. But all I'm really interested in is I want to look at the schematic, for a board that I know works.

And potentially, I want to look at the PCB layout for certain little pieces of that board. I'm not interested in the whole board, but I'm interested in pieces of it. And so I look to the open source community.

And a couple of places that I can give examples is like the very first time I wanted to design a board around the Raspberry Pi pico. The chip on that's called an RP 2040. Well, I started with a pico on a breadboard and said, okay, now I understand how to code for it.

I understand how it works. I want to design the actual board. So I went out and looked into the open source hardware community and found two sources right off the bat.

One was Adafruit who publishes all their board designs. They publish their schematics. They published their PCB layouts.

You can see everything they do. Another one was a group out of Europe called Sauter Party. And they, too, are very big in the open source.

They open source everything they do. And so by looking at those two sources, I started to understand little things around routing, of power or routing the USB because reading the data sheet and reading the official electrical engineering descriptions of like how to route USB, there's lots and lots of constraints. The truth is for a lot of these chips, you can get pretty sloppy and it still works perfectly fine.

And there's no way to know that without either designing your own board or looking at other people's boards that you know work. And so that's kind of one of the things that I start to dig into before I design my own board is, can I find examples to help me avoid a lot of mistakes or a lot of iteration? And so that gets me, that probably jumps two or three iterations into my design because I'm taking from other people and using the work that's already published in the open source community.

Paul

Standing on the shoulders of giants, we like to say in an open source.

Bradan Lane

Yeah, or as the literary people say, you know, what is it, good authors plagiarized, great authors steal out, right?

Paul

Exactly. So it's really not that different than learning to code. A lot of people will take a look at an existing program, rip it apart, put it back together, add little bits. So you're doing the similar thing when you're writing your schematic. You're looking at other people's designs that are in the open source community to get ideas and to learn those best practices.

Bradan Lane

Exactly. And that's even more true when you start dealing with boards that you want to support CircuitPython. Because CircuitPython can support almost anything.

But CircuitPython is very easy to support if you're using stuff that other boards have already done ahead of you. So again, it's standing on the shoulders of giants. So for instance, if I know I want a board to support CircuitPython, let me use as an example, you know, that early RP2040, the Pico kind of based thing.

Well, not only did I find that Soder Party had created their RP2040 stamp, which had all the broken out capability I wanted, it also supported CircuitPython. So I knew right up front that, okay, if I use the RP2040 the same way they did and I use the same memory chip that they did and I use the same crystal and I use the same USB, then I'm very likely to be able to support CircuitPython as easily as they did. And sure enough, when I went to add CircuitPython to that design, I started with their code again because that too is open source.

I look for examples of hardware that somebody else has already tested to work together, LEDs that work together or serial that, works together or infrared was something that I started playing with last year in earnest. And so I looked at Adafruit's example from their circuit playground express, I believe, is the hardware that they use. And I also classify that as sort of a feature board as opposed to a dev board. And so I looked at their board. I looked at how they did their chip. I looked at the memory they used. And then I looked at the various components they used. Looked at their schematic.

And then I started building my schematic based partially on that and then partially on the RP 2040 schematics that I had found and kind of pieced it together. And so that getting the schematic mostly figured out came from just like you were saying with code, copying, pasting bits and pieces from other open source opportunities. Once I had the schematic, then it was a matter of the board layout.

If you think about a dev board, most of them are rectangular. Very simple, rectangular. Quite often they'll have headers down either side.

And so I'll go into the PCB layout, import the schematic data, and that just gives me all these parts and what they call Rats Nest, which is these unofficial lines that connect pins together based on the schematic. And I look at, well, what are they going to be the constraints of my board? So if I'm doing a development board, the constraints are going to be those pinheaders.

They've got to go down both sides. They have to be spaced apart a certain amount. And so I'll lay those out and then start looking at the rat's nest to try to figure out what parts most likely belong in different areas around the board.

And I'll spend a fair amount of time just moving parts around until I can see that the rats' nest don't cross over too much and they're as short as they can be. and there are logical things in the right place. And then I'll actually start doing what they call the routing.

And the routing is where they connect physical traces of copper between the different pins that represent what that rat's nest was telling me I needed to do. So the great thing about these EDA tools is when you go from schematic to PCB, they kind of tell you what work you need to do and how you need to do it. So as long as you've got your schematic correct and configured, then when you go to do your board layout, you have that information in front of you as sort of hints.

And it's sort of like notes in the margin. And so you then go through the process of laying out the parts. And there's a few tricks.

You'll notice on some boards, if there's a microcontroller, there's pins on all four sides of a microcontroller, which means you've got these routes going every which way. And if you've got those rails going down the left and the right side of a board, one of the tricks they do is they'll be. put the chip on the 45.

So instead of having a top, a bottom, a left, and right, what you have is you kind of have an upper left and a lower left and an upper right and a lower right, which now makes them much easier to get to those pins that run up and down the sides of a board. And that's a trick that I didn't understand until I tried to lay out my first board. And then I went and looked at, you know, a board layout from another company or another group in the open source area.

And it's like, oh, now I know why they did that. Sure. Little things like that.

You know, there's also hints you'll get, you know, for instance, if you've got a USB connector, the best practices, try to keep those traces as short as possible, try not to have stuff cross over and under those traces. And so there's best practices out there that over time you learn, all my first boards, no USB at all on them. They were just battery powered.

And so over time, the boards get more and more complex. But to begin with, you know, it's the schematic to the PCB. Now, that said, there's a few things that as a very early, designer when I first started out, one of the things that I did was I'd create a board that was just part of the problem that I was trying to solve. So for instance, the touch sensors example, well, okay, so I created a board that had nothing but touch sensors on it. And it cost me, you know, a couple of bucks to have made manufactured. But then I could plug it into my breadboard and hook it up to an ATA Fruit Feather or another board and learn how it worked. Same with LED.

sometimes I'll actually do that. Now, I've graduated from doing that to doing what I call a kitchen sink, which is if I'm starting down a new path, I'll design a board, I don't care what shape it is, but I'll put everything on it that I think I might want to use. And I'll populate part of it and test it and get it to work.

And then I'll add a couple of pieces and I'll hand solder parts on and hand solder parts on and figure out what worked and what didn't and what I understood and what I got wrong. And so when I'm designing a feature board, often I'll design what I call a kitchen sink. Just throw everything you think you might want to learn about it on there.

And it's great because over time, you populate the whole board. And not only do you learn about the design of the board and what worked and what didn't, we also learn how to code for the board you just created. Those are kind of the approaches I've taken.

I start with maybe designing just part of a board or a board and put everything on it, making sure that I can remove stuff and it will still work.

Paul

That's a really good tip. I would have never thought about designing almost a subboard and considering how cheap some of those fabrication companies are that it's just a couple bucks or ten bucks to get five of them to build that back into your design on the breadboard is genius.

Bradan Lane

I do that at least once a year. I'll design two or three of these little subboards knowing that I need to test them out. And the great thing about them is I keep them. So if I went like I'm working on a new chip right now, well, if I want to design into that feature board that I'm going to create touch sensors. Well, I'd go grab a touch sensor board I've got that has, you know, touch sensors of various sizes and touch sensors that are that are masked or exposed.

Same for an LED board. You know, board's got, you know, just four LEDs on it, or it's got four neopixels on it. And so I could just reuse those.

Paul

So we've got the board schematic done. We've got the layout done. And the components are picked out and the traces are all around. What comes next?

Bradan Lane

One of the things that occurs, and you touched on it, but it can actually be more work than we often imagine, which is we pick out the parts. Well, we need to pick out the parts in one of two ways. Either the parts we're going to order ourselves, or if we're going to have somebody else manufacture the board for us, we need to pick out parts that they have available to them.

I want to jump back to the ECEDA example. One of the things that's great about ECEEDA is it's completely integrated with one of the board manufacturers in China. and that board manufacturer will do assembly for you.

And the most cost-effective low-cost solution for their board assembly is if you use parts they have in their catalog. So the great thing about Easy ADA is when you pick parts, it knows what parts are in the catalog. And so it tells you right up front, this is the LED you should use.

And if you pick a different LED, it's going to warn you, well, you can use that LED, but we don't have it in our catalog. Easy EDA is great from that standpoint because they help you. with a schematic, they help you with the PCB layout, they help you with what's called the bomb, the bill of materials, and picking parts that are in inventory and cost effective. And then when you submit it, all that data, the board layout, the artwork for the board, the bill of materials, the part numbers, down to the part numbers that that company uses to do assembly of the board, is all submitted in one big bundle. When I do it, I do my own assembly. And I do my own assembly.

And I initially started out with, you know, doing hand assembly, and I created some hand assembly tools. And I now have a few pieces of equipment that kind of help me do assembly in my lab. I have a list of parts that I know I can get easily through Digikey or Mouser or LCSC.

And some of those I have in stock. And so I know, for instance, there's a thing that happens in almost every board design. And these are called decoupling capacitors.

And all they're really there to do is filter out noise on the board. they tend to always be attached to wherever voltage or ground is close to each other. You have these decoupling caps.

Well, the decoupling caps are almost always the same values. They're either 100 nanofarred or they're 1 micro-faird or they're 10 micro-faird. Well, capacitors are really cheap and so you don't buy 10 of them.

You buy 1,000 of them. And so now you've got these in stock. And so now if you know you're going to design a board, you don't have to look up the part.

You know you've got it. So there are certain parts. I don't go to the next level of finding out the actual part number because that would be a manual step for me.

But in general, yes, what you're going to do is you're going to go through and from your EDA tool, whether it be easy EDA or KKAD, you can have it generate a spreadsheet, a report of these are all the parts you have on your board. And this is how many of each one you need. And also these are where they go on the board.

And one of the cool things is with KKAD, because KKAD is open source, there are people who build custom plugins and additions to it. One of the greatest extensions somebody has created is a browser extension that takes your bill of materials and your PCB layout and renders it in a browser and it lists out all your parts. And if you click on a part, it will show you where it is on the board.

And if you click on a part on the board, it shows you where it is in your inventory or your bill of materials. and people actually, if they're going to do hand assembly of their board, can actually pull this up and have it in front of them, and it'll run on an iPad or an Android tablet. What they'll do is they'll literally have it show them what part they have to place, and it will show them on their board where it needs to go.

And then they click a little button, and it shows them the next part they have to place and where on the board it needs to go. And so they can work right down through the board and graphically see what they're going to do. In general, I would recommend for a lot of people if you are designing in something like Easy EDA, plan in advance to actually have the board manufactured by the assembly shop for a couple of reasons.

One is it allows you a lot more creativity with your board design because they're going to use what's called SMD parts or SMT parts, which are surface mount part. And they can be very, very small. And they have no problem placing a very, very small part.

But if you're trying to do it by hand, it's a lot of work and it gets frustrating and you can make mistakes. and the board might not work. If you're designing a board with what might classify as old school parts, which are through hole, then it's much easier to do by hand.

If you want to focus on the design of your board and not the difficulty in assembly, then having a board manufacturer actually go and put all the parts on the board, solder it for you, and then ship you a finished board, is a great, you know, sort of low threshold to consider. And again, with like easy EDA and the board manufacturer, if you use their inventory, it's very cost effective.

Paul

So with all that said, we've now built a board. Are there any other pieces of advice for someone just starting their journey and learning PCB design that you might have?

Bradan Lane

A lot of it's going to come back to stand on the shoulders of giants. You know, that was a great quote. I'm so glad you put that out there.

I tell people, I don't have a background in electrical engineering. You know, five years ago, I knew what a resistor was from high school. and that was about the extent of my knowledge.

And through joining a couple of discords and catching a couple of people on social media that were willing to answer my questions, I got my first board to work and I got the first parts of that first board to work. Leveraging open source projects, leveraging various communities around this is really what got me to the point where I can design a board that does what I want it to do. And now five years on, I'm turning around, and now I'm the one who's answering a lot of those questions of the people who are coming in behind me.

And as I explained to them, it's not that I have a formal education and it's not that I'm an expert in this area. I've just made every conceivable mistake you can probably make at this point. And I'm just trying to help you avoid them, just like other people helped me avoid them early on.

Paul

Sure. So I wanted to ask you about one of the kitchen sink boards that you designed last year. Tell me about the DC Next Gen graffiti badge.

Bradan Lane

I loved the graffiti badge. There was a few things that came from that. One is I wanted to design a board for learning.

I had seen the Aida Fruit Circuit Playground Express and said, this is really great, but there's a few more things I'd like to have on it. And I'd like to package it up with a 3D printed back and its own USB cable and everything it needs to work. And while while I'm at it, I might as well design an entire workshop series and some training education and a bunch of different tutorials and a whole bunch of example code.

And so I thought, this would be a great conference badge. One of the things that's popped up over the past probably 10 years is this notion of badge life, which is a few of the tech conferences started using electronic badges. And it exploded.

The complexity and depth of electronic badges that are at some of these conferences is crazy. What spawned from that is an entire indie sort of cottage group that broke out from that, which were groups or individuals that said, oh, I want to design a small badge that I can take and give and trade with other people or maybe sell. And so I had this idea for a conference badge that would be easy to program, had lots and lots of functionality on it, looked cool.

And for me, CircuitPython was the logical foundation for that. So I come back to Soder Party Express in their RP2040 stamp, right? That was the genesis of saying, okay, let me look at how they designed that.

Okay, let me put that on a board with a PCB. Now let me add touch sensors and neopixel LEDs and audio. Well, geez, where am I going to get audio from?

Oh, Aidafruit must have an example. Sure enough. Circuit Playground Express has a little PWM audio and a little amplifier.

I use the exact same one on mine. And then I wanted, since the badge wasn't going to have a battery, that was a distinct decision to not only keep the cost down, but also shipping and lithium batteries and all that kind of fun stuff. So how do you make a badge that's going to have personalization on it?

Well, an e-paper display came to mind. And so again, I went back to Adafruit and I looked at AtaFruits repertoire of boards and sure enough they had a little breakout board for e-paper. Also, WaveShare, who a lot of people use for boards, it turns out WaveShare open sources all their designs too.

And so a combination of those two, I designed a prototype that included the breakout for an e-paper display. That badge was really an amalgam of various open source capabilities that I found from lots and lots of sources. And then it was, let me tie it together with a theme.

And since it was going to be for a youth group, youth-oriented group, typically 11 to 17, I think, is the target audience for DC Next Gen. I wanted something kind of fun, a little edgy. And so this idea of graffiti on a, you know, like a tag on a wall, a PCB can be any shape you want.

So I used, I think I used Inkscape and kind of created a box. And then I kind of squished it at one end and squicked it at the other and kind of got what, you know, the artist would say is perspective. And then laid out, you know, like what would look like a brick on it.

So now it's got this brick wall in perspective, graffiti tag on it. Okay, I've kind of got the artwork figured out. Now how do I integrate the artwork with the electronics?

And this comes back to some of the other things. Like, okay, touch sensors would be kind of an easy thing to integrate. And the great thing about touch sensors is it's part of the PCB.

So there's no hardware you have to solder. It's literally part of the PCB. So DC NextGen, that's nine letters.

You know, okay. Let's put every single letter is a touch sensor. Okay, we can do that.

Not a problem. And then the e-paper display, the LEDs, et cetera, et cetera. That's a case where the art drove the shape of the badge and even drove some of the functionality of the badge or the PCB.

And again, there was nothing really special or unique about it. Almost everything on that badge came from other open source projects. I think the ultimate display driver was based off of what WaveShare had.

The audio was based off of what ATA provided. The RP2040 was from Sauter Party. It was an amalgam of all these different things.

And then when it came time to get it certified for CircuitPython, because I had leveraged stuff that was already used by other groups, most of those building blocks were already part of CircuitPython as well.

Paul

In the next episode, I talk with CircuitPython core developer Dan Helbert about building CircuitPython from Source for Boards. In your experience, how easy or hard has it been getting CircuitPython running on your boards?

Bradan Lane

There was two steps to get CircuitPython in any of my boards. One is getting it to work, and that's relatively easy. And then it's any of the customization, so it's more intuitive to the programmer.

So if we look at the graffiti badge as an example, because I had used the software, the software, solder party RP 2040 stamp as the basis, then CircuitPython already supported the RP 2040. It already supported the memory flash that was being used by that, the crystal nose one. So getting CircuitPython to run on that was very easy.

The next step was getting it to have all the integrated capabilities. And the CircuitPython core support team is incredible. AidaFruit manages a Discord server, and within that database, Discord server. There's many, many channels. The two that I spend a fair amount of time in.

One is they have a hardware design one, which is great. You can ask hardware design questions if you're designing your own board. There's also one for CircuitPython help. These are people who are trying to write CircuitPython and need some help getting things to work. There's a whole separate channel just for people who are developing customized versions of CircuitPython for their boards.

And you have an option of designing a custom version of CircuitPython for your board and just keeping it that way. Or submitting it back in in the world of source control. This is called a pull request.

And the team will work with you to make it normalized so it fits in with all the other boards. So using the same language or the same labels for things that other people are using. So it becomes much easier for the person who's going to write CircuitPython against your board.

And so that was relatively easy. when I did my second CircuitPython board, it was a little more nuanced because if you think about almost any development board that's got USB on it, when you plug it into your computer, your computer is going to recognize that USB. And often they have these things called vendor IDs and product IDs.

And getting your own vid and PID is going to be different for every board. So Raspberry Pi handles all the PID assigns for anybody who's developing a board for RP 2040, you send them a note and say, this is kind of what my board's doing, this is what I'd like, would you give me a product ID? And almost always they're going to come back and say yes.

And they send you a code, and that's your code for life. My second board most recently uses the microchip SAMD21. And that's a completely separate thing.

Microchip doesn't provide USB IDs, so they don't provide the PIDs. for those. However, there's an open source organization that does. So again, you go through the process, you submit what you're requesting what you plan to do, and they coordinate and say, well, we'll do it as long as your board is open source. So this comes back to the same community that got me started. A lot of my designs are related to open source designs that are already out there.

This organization that will provide you a USB ID says, we'll provide it to you for free rather than spending tens of thousands of dollars for it, if your board is also going to be open source, so you can help the next group. And so I have no problem. I publish all my hardware anyways.

I sent them the link. This is the link. This is the board. They said, okay, all the stuff that we expect to be open source is available online. You're good to go. Here's your ID. So then I take that ID and I have to go back to CircuitPython and make sure that my build of CircuitPython uses the ID that I was just assigned. So there's a few places where the process loops around on itself.

But again, the open source community and in particular, the resources that Adafruit provides is incredible for people who are trying to design boards.

Paul

Bradan, this has been great. Thank you so much for coming on the show and sharing your experience in designing boards.

Bradan Lane

Thanks. It's been wonderful. And I'm sure that there's lots of questions still to be had. And the great thing about it is the community that's available for answering questions is huge.

Just need to reach out and ask.

Paul

I couldn't agree more. Thanks again. Thank you for listening to the CircuitPython show.

To learn more about Bradan, check out the show notes for links to his homepage and his past visit on the show back in episode 19. Next episode, I'm joined by CircuitPython core developer, Dan Halbert, to talk more about building and customizing CircuitPython. Until next time, stay positive.
