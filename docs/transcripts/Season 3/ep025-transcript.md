---
date:
  created: 2023-04-10
title: "Episode 25 - Danny Staple"
---

## Show Notes

[Show notes available here.](../../episodes/Season 3/ep025.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode I'm joined by Danny Staple, who is a robot builder and programmer.

He has been a professional software engineer since 2000, uses Python professionally, and regularly contributes to open source projects. Danny has been building robots at home since 2004 and has a cupboard full of projects, including robots with wheels, cameras, tank tracks, legs, and arms made from plastic, cardboard, metal, kits, launch boxes, and modified toys. Danny has authored multiple books, including Learn Robotics Programming, published in 2021 by Packet Publishing, and its most recent book, Robotics at Home with Raspberry Pi Pico, which was released this past March.

He has also written magazine articles for the Magpi Magazine and runs the robotic YouTube channel Orion Robots and brings his robots to events such as Pie Wars and Arduino Day. Danny also mentors at Coder Dojo, KU, where he shows kids how to program in Python and has run Lego Robotics Clubs. Danny, welcome to the show.

Danny Staple

Hey, how's it going?

Paul

It's going great. How did you first get into computers and electronics?

Danny Staple

The story starts around in the 80s, so I think at home we ended up with a ZX81 and a specie and eventually a Commonwealth 64, and that was, the Commonwealth 64 was mine. I think I reached the point where I got kind of bored of the games, was typing in, cheats from the back of magazines, got into programming, making my own, mostly in basic, but I tinkered a bit with assembly, I think, had the, there was an awful assemble at the back of the input, somewhere in the input magazines, which half worked some of the time. And I also had my appetite wet for robotics.

There was like an Osborne book, the Vicrell device book, building robots. Never built that one, but I still had the book, and I definitely wanted to build it then. I've been pretty much programming since then.

Paul

Your latest book, Robotics at Home with the Raspberry Pi Pico, was recently released. What can the reader expect from the book?

Danny Staple

The first deal is, by the end of the book, they'd have built a rover and programmed it. And that rover is entirely intended as kind of an experimental platform. They'd have built the chassis from parts themselves that they designed in free CAD.

They'd have put together the electronics. It totally invites them to hack and to modify and to make it their own. You can buy some much cheaper, complete, productized robots.

This is not that. This is you have put something together and you've. you've hacked it and you've riffed on it and that that's the entire point of that.

They'd have also gained a bunch of skills. So robotics's got this nice intersection of programming, electronics, mechanical skills. I've added in the CAD element, which was brave and interesting.

But that means they've got a springboard into either other robotics projects, maker projects, programming projects.

Paul

That's great. So they can build a base and almost go in any direction that they want to continue to learn from there.

Danny Staple

Oh, yeah. Absolutely encourage that. I guess towards the end of the book, you know, There's even perhaps going as far as not just encouragement, but it'll shove to, right, and no plan your next project.

Paul

So in addition to the Raspberry Pi Pico, you put together a shopping list for building the robot in the book. What other hardware is used to build the robot?

Danny Staple

Yes. Okay. So as you mentioned, there's a Raspberry Pi Pico at the heart of it.

But I also kind of recommend hardware like motor controllers. I'm using the TB6612 FNG. But I encourage readers to riff on it and to adapt it. Maybe that requires a little bit of thinking, and remapping in terms of pin numbers and maybe some of the code should change, but I also try to layer the way the code is, so things like heavy, that motor controller is hidden in a layer, so they can change that.

The code on top shouldn't change that much. There's other things like there's a pair of distance sensors. I've encouraged the motors that have encoders built in so we can use encoders as a sensor.

A Bluefruit BLE Bluetooth module. So you can talk to. the robot remotely, an immersion measurement unit.

So you can measure the robots facing, compass headings on that. Things also like the simpler things like battery box and a UBEX power adapter. And again, I guess I encourage the reader to riff on all of these.

The easiest path is to buy the same things, but I also understand that readers might have things in their own parts bin. They might want to find something cheaper or try something more interesting. Interesting. Absolutely encourage it. Go for it.

Paul

Were there any challenges with the park shortage that we've been going through for the last year or two?

Danny Staple

Oh, yes. So at one point, just the motor controller went up three or four times in price. They were, I think there was a point when this particular controller was, I don't know, three pounds, three British pounds apiece.

And at then one point it went up to 24 pounds, which is just a shock. At the moment, I've been getting these so there's a place in Nuka I think I can get them for six pounds with headers they're currently cheaper with headers and without headers and maybe they've just got a stock of those things like inertial measurement units so I'm using the BNO 055 and it's the older Art of Fruit module because I know there's a newer version and so you know it's slightly different CAD drawings and so on same wiring same code just which place you put your screw holes in but at one point that became hen's teeth to get, really hard to get, and quite pricey. And then it came down again, but yes, definitely caused me to think and adapt a few things.

Paul

Putting together the robot, do you know roughly how much you could expect to pay out of pocket to build what you have listed in the book?

Danny Staple

I would say for parts, maybe £100 to $120, which is going to work out was about $150, I reckon, US. It's just a rough guess. I guess there's another section of tools and consumables.

So there may be another kind of hundred pounds on top in terms of tool of consumables. But the idea being is actually those start you off on a simple, kit-it-out lab. So we're not talking, you know, like the £1,000 or £900 market.

About £200 all in gives you tools and the robot and stuff to carry on making with.

Paul

Oh, that's great. That's really reasonable. What made CircuitPython a good choice for building the robot?

Danny Staple

initially it was about this drag and drop business where one of the big advantage of circuit Python is you've got this file device you could just throw things at and that made it really easy so you could kind of edit stuff and then if you've got more than one file and there is definitely an element of having more than one file because there are as I mentioned kind of layers of code so there might be layers to deal with specific sensors specific algorithms you can copy those all across to your CircuitPython device to the PICO now Thonnie has made Fileman easier on both CircuitPython and micropython, mitigating some of it, but I still think just being able to plug it in and drag-drop files is brilliant. So the other thing I've found is just having that CircuitPython library of, you know, things like talking with the BNO-055 or the VL-53, whatever the X, there's many of them. But talking with those devices, again, you can use the CircuitPython library.

And I think being able to, say, reach for other devices, or indeed. adapt the pico. So perhaps, if someone wanted to say try, I don't know, a teen C, something with a different feature set, beefier in some way, more memory in some way, or even smaller and cheaper, they could do so because it's CircuitPython everywhere.

Paul

What were some of the challenges you faced and how did you overcome them?

Danny Staple

Right. I think we've already covered the chip shortage, which was one of the interesting ones. So I did pick some quite ambitious chapters and there were some that kind of really did cause some issues. So I did a chapter on FreeCAD. Now, I guess the ambitious part, and in fact, the original design of the book was to do FreeCAD and putting together, cutting the chassis into one chapter. That never happened. I split that. FreeCAD in one chapter was perhaps very ambitious, because FreeCad is quite complicated and we did run into how many screenshots do we get before we completely bust the page count, because there are page count limits, a book can't be infinitely long, That was quite challenging, but I think we got there.

There was then an aspect of the SP32. So initially, this was going to be a PICO plus an airlift module for Wi-Fi. And the airlift module, I tried to adapt some of the code I'd done with one of the earlier Learn Robotics books, where a lot of things were being sent across, basically served up as a web page.

And I managed to consistently make the airlift software crash. And it was at a time when it's, well, you know, I've got to carry on. I can't. I dived in quite deep to the point where I think I was flashing custom code onto the SP32 before going.

I have to abandon this and find another way. I pivoted to Blue Fruit BLE using Bluetooth and using the Blue Fruit Connect app, which was very handy. because you kind of just get graphing and you get a U-art terminal you can interact with really good fun.

I pivoted to that. It was, I think, about three or four weeks after I reached the point where I couldn't go back and edit those chapters because there is a, there's kind of a lock that follows up behind as it gets copy editing, and gets closer to publishing or closer to that chapter's kind of put away, where the publisher will say, you can't edit that now. It's too big a thing to go back around technical review, editing, proofing, all of these things.

And it was about three or four weeks after I'd done this pivot and rewritten an unlocked chapter, so I'd actually broken some of their rules to get there, that I heard about the PICOW. And it was both amazing and frustrating. I still think the Pico Plusa device is the right thing, though.

Because I think there's an MCL memory hog that may conflict with the Pico. blue stack. Not sure. I have to test that out. And we'll get into it, but the MCL itself, the Monte Carlo localisation, was a huge challenge. It's possibly one of the most complex things I've tried to get a robot to do.

Paul

So what did you end up using for Bluetooth?

Danny Staple

The, so it's the Adafruit Bluefruit module and it was the BLE-Uart module. Now hindsight says, and sometimes it's good on reflection to get into what I learned later, later learning was always a, a, thing in the book because I started off using Mew and got into finding Thoney a bit later. But one of the late learnings was actually, I backed the blue fruit U-art, but perhaps it should have been the SPI.

And that's a simple matter of rates, transmission rates. So the UArt is, for the bluefruit U-R, a BLEUR, it's limited at 9600. You can kind of extend it, but it's so-so, and that's also a bit tricky for the reader, whereas the SPI run on just runs as much fast.

faster in terms of board rate, in terms of sending data.

Paul

For those who may not have used it, can you explain a little bit more about the Bluefruit and how a reader controls their robot?

Danny Staple

So the Bluefruit you are, or the Bluefruit, it's a Bluetooth adapter, or Bluetooth BLE adapter, that you can connect to any kind of microcontroller. You can send data to and from it from either a phone or from libraries on a computer. If you're using Python on the computer, the bleak library, lets you send data to it.

It has two modes. One represents just a U.R. transmitting and receiving plain text.

So you can kind of create wrappers around handling plain text. And I took this route because this was the simplest route. Again, when doing the book, you know, there's an element of take the simplest route.

So the reader has the least to do to get something to work. And also for this whole page count as well. It has another mode that's a more advanced control mode where you can send control signals to it and go outside of just sending this plain text.

the handy thing about this BlueFruit module is this the Blue Fruit app so BlueFruit Connect it's I think it runs on iOS there's an Android version there's a Mac desktop version there might be a Windows desktop version and as well as being able to so you get to transmit and receive data to anything connected to Blue Fruit there's a mode that gives you like a control pad with up down left right and a couple of buttons and there's a mode that graph data So if you've got sensor output or if you're logging something, you can then get real-time graphing of data on your device, on your phone, which I just thought that's a really handy way to start visualizing what's going on in any of the kind of numerical output or any of the sensor data.

Paul

How did the RP2040s programmable I.O or PIO help when building the robot?

Danny Staple

One of the cool, it was one of the things that actually I found really cool about the whole PICO experience as well is this having this PIO. So encoding, this is taking motor odometry when motors are moving, you start to get pulses on, to tell you how far a wheel has turned. And this is actually based around gear motors.

If you've got a gear motor, and the gear motor is, say, so I've gone with 298 to 1, that means that one whole revolution of a wheel is 298 pulses. And so those numbers can get pretty quick, pretty far, you know, and if the robot is moving, you need to not miss those pulses. You need to be counting them as quickly as possible.

So I guess I was able to use PIO in a kind of a sneaky way to monitor these encoder inputs and take the load off of the main PICO processor to monitor those outputs, sorry, those inputs, and always increment or decrement the right counters based on them. It meant I was able to, I guess, not be concerned about missing those pulses. I was able to get that data straight into a variable I could then use in circuit Python.

Yeah, it was definitely very handy. It was kind of one of those fun areas, and I've dug into it in the book in the encoder chapter. We build it around using PIO and lots of sneaky things that remind me of, I guess, the days when I used to do assembler.

Paul

You mentioned it earlier, but what is the Monte Carlo technology?

Danny Staple

Right. Yes, MCL, Monte Carlo technique. So one of the problems for robots, and I guess any moving device, is this idea of registration.

Where is it exactly? So you can have the simple kind of situational sensors that will say, avoid a wall, we cover that, so they avoid a wall, they'll steer away from the wall. Great, okay. But where is the robot? It's responded to a wall, but it doesn't know where it is in the room or where it is in a particular spot.

So Monte Carlo localisation, you build a model of a space. In this case, actually, there is a kind of specified in arena that the reader can build. You mathematically model the space, so having a known space helps.

And then you start saying, well, based upon the sensor input I've got, where should I be? Now, that's a fairly complicated problem. And so you kind of flip it on the head, okay, I'm going to make a load.

to guesses about where the robot's going to be, where it is positioned in terms of space and orientation. So there's an X and a Y and a heading. And I'm going to throw them into, here's my two sensor readings, transform each of the sensor readings so they match the position, the guess position of the robot, and start placing a probability on how likely is that?

Given I know what the mathematical model of the arena is supposed to be, I should be able to to say, well, these positions are more likely than those. And I'm also then accounting for, sensors are not 100% accurate. There's always some variance in what you get.

So then the next trick from that is to take those poses, if you like, the positions with probability and recreate another population where its distribution is based upon the probabilities we have before. This time they'll have uniform probability, but those that were more likely before are more likely to come up multiple times in the new population. There's some trickiness then about how you move the poses.

So when the robot moves, based upon sensors like the encoders and the IMU, the robot will move with it. Now, there was a challenge in here, so at the moment the IMU is a suggestion. The IMU is not included because it became very large.

The code became very large. But I have given the reader pointers towards doing it, whereas it's mostly now based upon the encoders and the distance sensors. So the distance sensors are used to observe the world and inform which things are going to be probable.

The encoders are used to move all those poses. So you kind of end up with many dots that start to coalesce into blobs, where the blobs are estimated positions of the robot. And it's quite exciting to watch it start to converge on where it is.

It was challenging. It was another one of these challenges, the MCL, itself is extraordinarily complicated. There was learning things about probability distributions that I thought I knew, but not at the depth that I now know.

There was also finding out that things like, so C Python, there's a random Gaussian, and numeric Python, Numpi, there is NNPy random normal, which also gives a Gaussian. CircuitPython random does not have a Gaussian, CircuitPython ULAB does not have a Gaussian. ULab is a kind of a numb pile CircuitPython, which is absolutely awesome because if you're going to do lots of mathematical transformations like the trigonometry involved in moving poses and estimating sensor distances, it makes those much quicker and it makes you use a lot less memory.

It was, because the MCL, you've got to work with a population. I ran out of memory many times until I got this right. I ran out of memory.

I ended up with some interesting transformations that went the wrong way. I ended up finding some actual issues that I returned back in ULAB. We found a problem where it did some of the vectorizing.

We got that fixed. I updated documentation in various, some of the other fruit docs on some of the CircuitPython things because it necessarily meant diving quite deep into a lot of things I'd not had to before. But I think I'm very pleased with the result.

There's still, so one of the things I tried to do with the arena was eliminate rotational symmetry because that's where the robot could end up guessing, I'm in one of eight places or four places or other probable places. So having rotational symmetry out helps it find the right place sooner. Because it's kind of an optimising technique, you end up with this concept of local maxima, where it finds what it thinks is a pretty good guess, eliminates all the other guesses, even though one of them might have actually been more accurate, but it's got this blob here and it's sticking to it, even though it's way off where it really is.

It's sticking to one blob instead of the one that's perhaps more probable. And the only real ways to deal with this is either to A, make an arena that's far more complicated or to go with a far larger population, which maybe going into further optimization could be done with more memory. And again, this is I ran into the constraints of it being in a book, because every time you optimize you add complexity, increases a page count.

Because not only if I've got to show the code, I've now got to explain the code, someone else can reproduce it. So again, I've kind of hinted towards the end of this, you know, the MCL area, that these are ways you could optimize it. This is where you could investigate further ways, larger population sizes.

Paul

That's fantastic. We're almost out of time. And the last question I like to ask each guest is, you're starting a new project. Which microcontroller do you reach for?

Danny Staple

That's easy at the moment. It will be the PICO. I do need to dig at the PICOW.

I think I've already said there's some concerns about memory with the Wi-Fi and if there's a HTTP stack or something there. I do want to play with the TNC because I believe it's kind of, it's a lot pricier, but it's also got more memory in a faster CPU and there's a flexible I-O thing that could be quite interesting. I don't think it's quite the same as PIO.

But at the moment, yeah, it very much is the PICO.

Paul

And if people want to learn more about you, your projects are the book, where should they go?

Danny Staple

So, starting place for me probably is Twitter, and that's Orion Robots on Twitter. I am Orion Robots on YouTube. I am Danny Staple on LinkedIn.

I definitely do the LinkedIn thing. I have a Discord server. That's probably one of those, I guess it's a URL I might have to send because it's not easily pronounceable.

Paul

Well, I'll make sure to include links to the Discord server and your book where it's as well in the show notes. Danny, thanks so much for being on the show.

Danny Staple

Cool. Thank you very much for having me on the show.

Paul

Thank you for listening to the CircuitPython Show. For pictures of the robot, show notes, and transcripts visit CircuitPython Show.com. Until next time, stay positive.
