---
date:
  created: 2023-12-18
title: "Episode 33 - Jan Goolsbey"
---

## Show Notes

[Show notes available here.](../../episodes/Season 4/ep033.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. This episode I'm joined by Jan Goolsbey. After a long and varied career in information technology for a large research laboratory, Jan became refocused on his first love, electronics hardware design, and all the things that go with it.

He is an active member of the CircuitPython community, enjoying learning new ideas and concepts. His current project direction involves music and sound synthesis, but is easily distracted by robotics, sensors, and anything noisy that blinks. Jan, welcome to the show.

Jan Goolsbey

Hey, Paul, how are you?

Paul

I'm great. Thanks for coming on.

How did you first get started with computers and electronics?

Jan Goolsbey

Well, I started with electronics first before computers. Oh, God, I can't remember how many years ago. Just, you know, a seventh grade kind of child, and I was very interested in electronics because I don't know why.

Some fascinating elements of that. And I started to take things apart. That was my introduction into electronics.

And back when I grew up, and I'm an older kind of a guy. So back then, there really weren't any computers around. And so if you were going to do things in electronics, it was all about radio and television.

Those are the big things, audio, radio, television. I got started by going down to one of the local electric shops that did TV repair, and I grabbed these old broken TV sets that they'd have, and I'd gleaned them for their parts. And from that, I would build circuits.

And, you know, it started to build into a kind of, you know, a habit of mine to tear things down and figure out how they work and use that to build other things. So I got started in electronics then. Computers are a little bit different because, like I said, the computers really weren't very prevalent when I was growing up. But when I was in high school, I was a junior in high school, my physics teacher said, you know, I've got all these parts that the telephone company gave us. Can you build a computer from those? And I, you know, I thought, well, I certainly can give it a shot. So I built my.

my first relay digital computer back when I was about 16, 17 years old. And a couple of years later, when I was in college, I started to build from TTR circuits and put together a computer from that. And then, you know, then I went through the cycle when computers became a lot more prevalent.

I learned how to program in Basic and a few other things. But I've always been focused on the hardware side.

Paul

How did you discover CircuitPython?

Jan Goolsbey

Well, that was interesting. I had a couple of projects, robotics projects. One was a string car.

And the string car experience is something that is kind of embedded in our family. And I won't go into too much detail. You might have some other questions about the string car a little bit later, right?

That's right. I wanted to build this robot string car, and I was using TTL circuits for that. And then somebody said, I don't remember who it was.

Hey, there's this thing called the microcontroller. And of course, I knew what they were from my work in electronics. And he said, you can buy these things from Aderfruit.

And you could use that to control this robot that you're trying to build. So I got involved with Arduino on a trinket. And, oh, Anne Borella wrote a fantastic book about how to get started with the trinket.

And that, you know, that got me involved in that. And then Tony DeCola wrote an article about Micropython. And that was before CircuitPython came out.

So I started to transition all of my robots over to Micropython and learn a little bit about that. And when CircuitPython came along, I was ready to go. It was, you know, Micropython was great.

CircuitPython was even simpler, easier to learn. And although it's slower than Arduino, it worked fine for the robots and projects that I had.

Paul

CircuitPython has the official CircuitPython bundle maintained by Adafruit. But there's also the community bundle, which includes over 100 drivers and helper libraries created by members of the community. You've contributed over 20 libraries to the bundle. What are some of your favorite libraries you've created?

Jan Goolsbey

You know, I get excited about the bundle. And before I list a couple of my favorites, I'd like to share just how important I think the bundle is. Because when you're working with the CircuitPython community, you find ample opportunities to learn and share.

And really that's the energy behind CircuitPython is about the community. So the community bundle is just a natural extension of what's already going on in the CircuitPython community, and that's sharing. So when I discovered that there was a bundle of things that people out there had put together based on their own projects, I got kind of excited about that, and I started looking through those.

And since I'm kind of a lifelong learner anyway, and I'm not that story. of a Python programmer. The community bundle gave me an opportunity to look at how other people did things with CircuitPython. And I picked up so many hints and tricks and ways to approach things that the bundle just was kind of this natural focus for me for a while. It's a hidden jam. And a lot of people don't understand that it exists out there. And it can be used not just to apply directly to a project, but also used for learning. And that's how I used it initially.

As I was building projects, I'd come up with a novel way of doing something. At least I thought was a novel way of doing things. I would put together a helper or a driver or something.

And I thought, you know, I really need to contribute back to the community. So I learned how to convert that helper into something that was community bundle compatible. It's like getting an idea ready to be a product.

I had to learn not just how to get things. done for my projects, but also how to present them in a way that other people could learn from them. And so the community bundle taught me a lot about not just how to write Python, but also how to share it.

My most favorite one was my first one, and it's this thing called a range slicer. I had a particular problem in my Euro rack system where I needed to quantize a linear signal, an analog signal. And, you know, when you're like when you're turning a knob on a potentialometer, you expect the potentialometer voltage to rise slowly and accurately so that you can use that for controlling a tone or a filter or some other setting, something musical.

But I found out the potentialometers are pretty noisy. As you turn them up, and if you stop at a certain point, they'll still continue to wiggle their value, and they're not as stable as you expect them to be. They're mechanical.

And so the range slicer is something that I use to smooth out the way that a potentialometer works. And there are a couple of ways to do that. One is to run it through a filter, but that kind of slows it down.

So I had to find a way that it used something called hysteresis. It determines the direction that the potentialometer is moving, and it waits until it gets to a certain point to say, hey, this is the value that you want, and it's stable. If you move the potentialometer up a little bit or down a little bit, that value stays rock stable.

If you move it a little bit further down, then it jumps to the next stable value. So range slicer was really great for quantizing voltages into musical notes and to filter settings and things like that. So yeah, range slicer was my first one.

That was a whole lot of fun to do. Recently, I've been working on graphics libraries for the community bundle. Palet fader, that's one.

Palette filter is another one. And palette fader was interesting because it came out of kind of a moment of desperation. I had a Matrix Portal.

I wanted to put a holiday display on the Matrix Portal. And when I first turned it on, it drew so much power. It was so bright.

And it drew so much power that it just shut itself off. And a lot of the folks that have worked with the Matrix Portal know exactly what I'm talking about. So I needed something that could control the brightness of that initial image before it shut down the microcontroller.

and pallete fader came out of that experience. And really, pallete fader is pretty simple. Getting to the point of putting it into a library and understanding how it worked, that was the hard part.

But pallete fader, like I said, is one of my more favorite ones because it just looks at the palette of the image, and it just scales down the values so they're not as bright. It scales down all three of the RGB values at the same time. And that's really how that works.

So that's one of my favorites. I have, you know, I might say I have 20 favorites, but they were all used in a project, and they all seemed very useful to me, and that's why I shared them. The great thing about the community bundle is that once you share it, you start getting feedback from people.

So Pallete Fader, for example, I've received a lot of feedback and have improved in my ability to program in CircuitPython. and also how to write drivers and libraries and stuff to share with people because of that.

Paul

What advice would you offer to someone looking to add a driver or library to the community bundle?

Jan Goolsbey

My advice is it's very simple. It's that you're probably doing something that can be shared. If you're working on a project and you have a particular approach to solve a fairly unique problem, like you're trying to get rid of noise on a potentialometer or something like that, You can rest assured that somebody else is having that same issue, or they're looking for some advice and how to approach solving that problem.

You're likely to already have something in your code that is shareable. So I'd just say find something that you think is unique that somebody else could use and share it through the community bundle. There are some particular ways of doing that because there are standards that have been put into place to make sure that the code always functions and that it's readable and those kinds of things.

There are learning guides and there are people like me that can help out. But I'd say getting started putting something in a community bundle is very easy because you're already doing it.

Paul

Synthio was one of the highlights of CircuitPython in 2023. Tell me about the IOT Windchimes project that you did earlier this year using Synthi O.

Jan Goolsbey

You know, I love SynthiO. I am so impressed with SynthiO because coming from a musical background and the, and working in the Eurorack and designing my own analog circuits to get sounds out, something as simple as CircuitPython that has a layer in there that's for generating oscillators. I love synth, I always love it. I could go on.

So the Wind Chimes project is an interesting one. I used to say, well, I have a problem. My problem is, my wife and I had this problem, we collect wind chimes, and they're out on the back patio on the other side of our house.

We love them because we're both very musical and we love having soundtrack going all the time. But the thing is, we also listen to them at night to gauge what the weather is doing outside. We live in the desert of Washington State.

That's my preface to say, wind chimes are important to us because they tell us when the wind is going to start blowing or when it has started blowing. And we can gauge the speed of the wind. by the character of the wind chimes.

But unfortunately, in my office, I can't hear the wind chimes. So the IOT wind chimes project was one where I wanted to hear the chimes in my office and wanted it to be linked to the wind speed outdoors so I could gauge how fast the wind was blowing. We get, by the way, wind storms around here can become surprising in a number of ways.

we can get trampolines coming over the fence. We can see trash cans blowing down the street. I've even encountered a metal lawn shed coming over the fence and sticking to the front of the house.

Oh my goodness. We've had some. So a wind is something that we think about a lot here.

And the Windchimes project is one way of doing that. The fun part about that Windchimes project was I used an ESP 32 S2 for it, which is a fantastic. fantastic board. I mean, it's kind of, it's one of my go-to boards now when I'm doing musical things because it's fast. And if I need an internet connection, it's got the internet connection.

And so it's perfect for the IOT Wind Chimes project because it could hold all of the musical notes that I needed it to hold. It could calculate the overtones that I wanted to calculate to get that realistic chime sound. The ESP 32 S2 is perfect for the project because of the fact that it had the memory and it had the speed and it had the internet connection that I need for that.

And then throwing synthio on top of that, I did something kind of organic to get the chime sound because chimes are, it goes back to physics and mechanics. When you think about how a wind chime works, it's a tube that vibrates. But wind chimes don't vibrate using the standard scientific model.

There's actually a little bit more to it than that. They have overtones that are related to the type of metal it is, the striker that hits it, and the pattern of the music is also, it's periodic and predictable in physics. Usually, when chimes are arranged in a circle and the striker travels in portions of the circle, that's what made that project a lot of fun, was that I could take some time and look at the physics of what it would take to make an accurate chime sound and then figure out how the notes would play. Synthio was perfect for that.

Paul

You mentioned it earlier, but one of the first projects you ever shared on the Adafruit Learned system was the String Car Racer. What is the String Car Racer?

Jan Goolsbey

The String Car Racer is a, well, let me go back in history first, because I didn't invent the string car. My brother invented the string car. He's a mechanical genius, I swear.

And he put together this idea that if you take an old D.C. motor and hang a battery from it, put a pulley on it, because the motor he had already had the pulley on it. If you stick it on a string, it's going to shoot down this tight string.

In our house, when we were kids, we would run the string from the apple tree in the backyard to the telephone pole out front. And that was a couple hundred feet. And this string car would just zip down there.

And we came up with all sorts of ways to make the pulley bigger, make it stick on the string better. You know, how many batteries can you put on it without losing the tension in the string? It was a great learning experience for us as kids because we got to experiment with all aspects of the physics around that.

So that's how the string car started. It was a single motor, single battery, it hung on the string by its pulley, and it would shoot down there. And if you weren't down to the telephone pole, when it got down there, it would crash.

And we'd have to repair it, and that gave us an opportunity to improve it. That's where the string car came from. And so we were always trying to figure out better ways to make the string card go down and back and getting the string car to reverse when it gets to the end meant we could save the life of the string car.

That was kind of important. We didn't want to keep building over and over and over. Let's fast forward.

We built these simple string cars. We didn't really have any formal rules or anything, but we tried to keep them simple. We used repurposed parts.

We'd get our motors from places. We'd build the chassis out of fence wire or whatever we had in hand. And we just tried to keep it simple.

It wasn't until I was getting ready to retire from my career. And I decided I need to work on some of these old family projects again. I got my brother interested, which is really great.

And I built some string cars around the trinket, as I mentioned. But I wanted to have this string car be smarter about collisions so that when it got to the end of the string, it would reverse and come back. And so came up with a design for a string car.

I don't know how, I'm showing one right now. But if you go to the learn guide that I wrote on the string cards, there's a section in there that talks about the advancements of the string car and some of the things that we did. So there are limits which is on this chassis that determine when it hits something and hopefully it hits something softly.

It'll reverse directions and go the other way and do the same kind of a thing. The string car evolved into this, started with the trinket. I came up with a special board that's a custom CircuitPython board, and you can find it out there on CircuitPython.org.

It's down, the only person that ever uses the download for that is me. But it's out there, and it's an M-Zero processor, but it has all the little sensors and things that the string car needs to be able to go forward and reverse. And it's evolved into, now I have a feather wing so I can plug in any kind of a board into it.

Like right now it's running an M4 board because that's just, that's floating point. It can do the calculations that it needs to do. But I've also run it with a Bluetooth board so I can remotely control it and things like that.

The string car was just a great experience in discovering physics and eventually learning how to build some intelligence into it so that it could be more autonomous. us. We didn't require us to catch it when it reached the telephone pool.

So the string card was just really a great platform for learning those kinds of things. And it continues into, you know, even today when I'm thinking about the physics of how the robot works, right now the string car is sophisticated enough to know, well, here's how it works. It goes very slowly down the string until it encounters a barrier.

And it determines, oh, I know how long the string is now. because it knows how long it took to get there, and it knows that based on the motor speed and timing. So now it can travel backwards towards the start as fast as it wants to because it knows when it needs to slow down, to keep from colliding and falling off the string or worse.

So that was a fun experience to go through the physics of figuring out how do you, without any sensors other than the time, How long does it take to get down to the end of the string and keep from colliding and falling off and getting damaged?

Paul

So great experience. What a great project. I'll make sure I link to that in the show notes as well. Speaking of links, if people want to learn more about your projects, where should they go?

Jan Goolsbey

Well, probably the best place to learn about projects is the Adafruit Learning System and the Adafruit Learning System playground, because I've been putting more projects in the playground area. I also have a GitHub repository site that is Cedar Grove Studios. And you can put the link in the notes.

I put most all of my projects out there, printed circuit boards I've designed, concepts that I've had, and many of the finished projects to weather stations and some of the other things that I've worked on. Playground is a particularly good place to find not just my projects, but other projects that they're not quite finished enough, polished enough to be a learning guide, but they contain a core idea about a project that you can learn from. That's where I put a project about a guitar pedal that I was trying to repair for a friend of mine. And I put the details out in the piglerone.

Paul

I'll make sure I link to that as well. Last question I ask each guest, you're about to start a new project. Which board do you reach for?

Jan Goolsbey

Well, you know, most of my projects, I try to, I try to complete like a product. So I really like my projects to have a front panel. And the Pi Portal is this almost perfect front panel. And it comes in three varieties. So you get the three different sizes. So Pi Portal with the M4 processor in it and it has an ESP 32, that's a great choice for most of my projects. And that's a great choice. And If I think about a project, that's the first one that I go to probably.

That being said, I kind of like the Pi badge and the Pi Gamer because they act like front panels too. I made a turtle bot where I used a robot that moves around using the turtle language. And I put a Pi Gamer on the top of that with a display, and that became the front panel for the robot.

So front panels, that's my first choice. But I really discovered the ESP 32S2, and the RP 2040, especially the QDPI version, is perfect if you're dealing with sensors. And I love sensors.

If you're trying to do something quick and dirty with a sensor and you don't want to have to solder a bunch of stuff, QDP 2040 is perfect. So that's four boards. That's about the best I could do.

I can't pick just one. Who can these days? There's so many great choices out there.

Paul

Yeah.

Jan Goolsbey

Yeah, it's fun.

Paul

Jan, thanks so much for being on the show.

Jan Goolsbey

Oh, you're welcome. I really enjoyed it. You know, I have a big passion for working with other people and learning from what other people do and the CircuitPython environment is just so perfect for that. Coming on this show and talking to you, it's just been a thrill. Thanks again.

Paul

Thank you for listening. You can find transcripts in most podcast players and show notes are available at www. CircuitPython show.com. Until next time, stay positive.
