---
date:
  created: 2022-05-02
title: "Episode 8 - Melissa LeBlanc-Williams"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep008.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Melissa LeBlanc-Williams.

Melissa is a maker, embedded software developer, technical writer, 3D printing enthusiast, and the maintainer of Blinka, a project that allows users to run CircuitPython libraries on Linux. She is sponsored by Adafruit to work on CircuitPython and Blinka. She also has her own YouTube channel called Maker Melissa's Lab, where she showcases many of her own projects.

She has also contributed to Tom's Hardware as a freelance features writer. Melissa, welcome to the show.

Melissa LeBlanc-Williams

Thank you for having me here.

Paul

You're the maintainer of Blinka. What is Blinka?

Melissa LeBlanc-Williams

Blinka is Adafruit CircuitPython compatibility layer that runs on MicroPython and single-board computers such as the Raspberry Pi. This means it runs on top of Python and allows libraries that were written for CircuitPython to just work with minimal changes. such as making the pen numbers different if you need it to be.

Paul

So it's not using the CircuitPython interpreter. When you say compatibility layer, it's hiding all of that Python and GPIO stuff from the user. They don't even have to worry about that. Is that right?

Melissa LeBlanc-Williams

Exactly. It just actually uses the full Python library itself.

Paul

So you should be able to do a couple little more probably powerful type things since you have a single board computer rather than a microcontroller. What are some of the benefits for someone to run CircuitPython on a Raspberry Pi.

Melissa LeBlanc-Williams

Well, one of the biggest advantage is you have full access to the full version of Python along with all of its libraries, whereas CircuitPython is actually just a subset of the Python language. And then you also have access to like more I-square-C and spy ports and the internet access is much more stable.

Paul

How does something like I-squared-C work? So you have the GPIO pins on the pie. Is it as easy as it is on the microcontroller, just saying board dot whatever the pin number is connected to another microcontroller?

Melissa LeBlanc-Williams

From the user's perspective, it's the same as doing it on CircuitPython, but underneath, it actually uses the iOctal library that is provided on the Pi. So I'd actually rewritten the one for the Spy that was using a C library, and now it's actually going through Pure Python on that.

Paul

Oh, neat. Are there any downsides to using Blink on a CircuitPython compatibility on a Pi?

Melissa LeBlanc-Williams

Definitely. The Blank of Library tends to run behind the development of Circa Python because there are fewer people working on it. So many of the modules that you may be expecting just haven't been added.

When it comes to certain pin types like PWM, even the analog inputs, the Raspberry Pi has far fewer PWM pins. Actually, I don't even think it has any analog pins. On a project that I was working on, when one of my requirements was to monitor the battery level, because I had a battery running the pie, I had to wire up an MCP.

3,002, which is an analog to digital converter, and just have that connected via spy.

Paul

So what goes into being the maintainer of Blinka? What are some of the things that you do that people might not know about?

Melissa LeBlanc-Williams

Most of it is reviewing poll requests that come in, fixing bugs, sometimes adding features, but generally it's just keeping the project in as good as shape as it can be. And sometimes it involves making decisions about what will be best for the most people, such as like what our minimum version of Python should be to give access to the latest features, but also not abandon some of the older boards that need older versions of Python. And sometimes external things change, such as CircuitPython recently added typing support, but in order to do that, we had to bump the minimum version of Python up to 3.7. And actually one of the boards that was kind of stuck on version 3.6 was the Jetson Nano. So I went ahead and figured out how to get folks updated to 3.7 and on that board and updated our guide so we could continue supporting it.

Paul

So do you try and keep up with the different Python versions when they go end of life, or do you keep supporting older versions like 3.6 or 3.5?

Melissa LeBlanc-Williams

We tend to update the minimum one, and it kind of sticks around what CircuitPython is targeting as well.

Paul

So how many bug fixes or pull requests come through on a weekly basis?

Melissa LeBlanc-Williams

Well, Blinka is pretty stable at this point, so bug fixes can vary from no bug fixes to maybe like three to four in a busy week. So most of the bugs are usually caused by like Linux updates or other changes outside of Blinket itself.

Paul

That makes sense. Anything planned for the future development of Blinka?

Melissa LeBlanc-Williams

Nothing really concrete planned at this time. It'll probably be either like adding new boards or porting over modules from CircuitPython.

Paul

How did you first get involved with CircuitPython and later Blinka?

Melissa LeBlanc-Williams

That's a great question. I actually was working on my YouTube channel, and one of the projects that I was doing, I had created a little board where you could light up. I'd actually taken like four of the, I think they're called Matrix pixels or something like that.

I can't remember the name. And I'd wired up four of them, and I was coming up with an example, and I wanted to do it in CircuitPython because I wanted to give it a try. And so I basically took one of the examples, and I just modified it until it was doing it.

I wanted it to do, and I made it so you could, like, cycle through different colors in order to draw on the board. And that worked pretty well. So then later on the following year, it actually written some improvements for a library that Ata Fruit had that was actually for the Arduino, the RA8875.

And I increased the speed of the drawing in an example and added a function to be able to drop faster and I submitted that and it was right away. And eventually they had asked me if I was interested in writing a library for CircuitPython for that display as well because I had expressed interest when they were kind of doing their yearly, what would you like to see in CircuitPython? So I decided to give it a shot. Originally I thought that the libraries for CircuitPython were written in C or something like that. So I was like going like, I don't know if I can do this.

When I found out they were actually written in Pure Python, I decided, okay, well, let's give it a shot. And I went through and I ended up writing. I think at the time I submitted it, it was actually the biggest library there was, because there was so many functions on there. I've shranked a little bit since, but it really hasn't shranked all that much. So I guess I did a pretty good job on that. So after that, I just kind of started helping out in the community and just helping out with different libraries. And eventually I talked to Adafruit about actually joining with them and working at least on a part-time basis to start with. And eventually, oh, you know, actually I had gone to PyCon in 2019 and got to meet Scott and Katney and Brian at the time. And that was a lot of fun and I think right around then is when I talked to them about going full time.

Shortly after that, I've been working for Adafruit.

Paul

So you mentioned your YouTube channel. You have dozens of videos on your YouTube channel. Of all the projects that you've done, what are a couple of your favorites?

Melissa LeBlanc-Williams

My favorite was probably the animated message board that I did just because it was a project that came out so nicely. It was really something I had been wanting to do since I was a teenager. I think mine actually turned up better than the original boards that inspired me because it's completely scriptable in Python, which makes things so much easier, plus it's color and everything.

Paul

What does it do?

Melissa LeBlanc-Williams

Well, you can have it so it scrolls messages, pictures, you can just type out messages, add, like, effects such as if you wanted to kind of come in from the side or kind of come together. You can add like shadowing and glow and everything. It actually came out really well. It's a library I had written called OpenSign, and it made the whole scripting a lot easier.

Paul

I'll make sure to link to that in the show notes. One of the things that you've been sharing on your YouTube channel last year was you built a CNC machine from scratch. How did that go and what were some of the big challenges?

Melissa LeBlanc-Williams

It's still going, actually. I actually was working on it, in fact, a little bit last night, And probably one of the biggest challenges right now is trying to interface with the VFD, which is the very well frequency drive that controls the spindle speed. And this is mostly challenging because the VFD, which I got from Alixpress, is actually pretty poorly documented.

And trying to get to do what kind of claims it should do is not quite working out. I currently have the speed control working somewhat properly, but I'm having trouble with the forward and reverse functionality. I've been considering getting a controller upgrade, but I think I'll actually just leave that for a future video because I just want to really finish up the current video at this point.

Paul

How similar is building a CNC from an equipment's perspective with what you would see in a 3D printer?

Melissa LeBlanc-Williams

You need it to be much more rigid, so it has a lot of steel plates on the one I'm building. I do have some 3D printed parts. The stepper motors are a lot heavier duty, but the electronics are quite different actually because, for instance, With a 3D printer, you use a lot smaller, stepper motor drivers, but you use these pretty big ones for the CNC.

Paul

Everyone seems to be working on a retro tech project right now. Do you have any currently on your workbench?

Melissa LeBlanc-Williams

I actually have a couple at the moment. One of the projects I've been working on is an old Pentium 3 server, which I bought from somebody for a dollar, and thought getting that working would be as easy as just turning it on. And it turned out I actually needed to recap the motherboard, fix the heat sinks that I broke while I was removing.

them and I get some PS2 accessories for it. But it does at least boot consistently now. At this point, I'm not sure if I'm willing to sink any more money into it and may end of just testing that everything works and then selling the parts on eBay.

Paul

After 20 years, what did you have to do to the motherboard to fix it?

Melissa LeBlanc-Williams

I pretty much had to go ahead and replace all the capacitors on there because the electrolytic ones just generally have a certain lifespan, whether you use them the board or not and they start leaking or bulging. I wasn't getting any video and what I was kind of doing some research on it, that's what somebody else was saying. So I decided to give it a shot and it actually worked.

And then the other thing I've actually really been enjoying are retro Max. And it's because I actually grew up with PC, so I never got to experience some of the older Max when they were current. And learning all about them and repairing and upgrading them has really been such a joy.

I actually have one right behind me here that you can see that I've been working on. I have another one. I got like this old Power Book 180 that just came in the mail today, actually, and I'm looking forward to working with that.

Paul

Apple's often in the news because of the right to repair bills that are circling around the country. Are there older Macs much easier to upgrade and fix than their current ones?

Melissa LeBlanc-Williams

Yes, they are. In fact, it was probably around 2014 when they were really making their math. a lot less repairable.

Paul

Which version of MacOS are you running on some of those boxes?

Melissa LeBlanc-Williams

I actually have that little Mac Mini running MacOS 9. It has a G4 processor in it. And the one behind me is running MacOS 8.

Really old? Yeah. And then the PowerBook that I got, I think it had, well, actually the one behind me was running System 7.6 and then I upgraded it to 8.6.

Paul

What's it like to use some of those old operating systems?

Melissa LeBlanc-Williams

It's fun. It's a lot of learning and that kind of goes in hand in hand with the repairing and learning how to do that because I end up just watching a lot of YouTube videos on how to do that and just kind of increase my knowledge a little bit at a time.

Paul

Hi, it's Paul. I'll get you back to the show in just a moment. Thanks for listening. And if you're enjoying the show, please tell a friend or write a review. You can also support the show financially. Your support.

helps cover the cost of podcast hosting, recording services, and transcriptions. For more information, visit CircuitPython show.com slash support. Now, back to the show.

Late last year, you shared a picture on Twitter of a mysterious crate that showed up at your door, and I think you unboxed it and shared recently what it was. What was it?

Melissa LeBlanc-Williams

It was actually an Elugu Jupiter pre-production model. Late last year, Tom's hardware was in need of a new 3D printer reviewer, and had asked me to a review and I had agreed to it though I did have my reservations because my time was kind of limited with the YouTube channel and all. I agree to do it because I figured it was good practice and maybe it'll help them make it like writing guides with Aetacrut and stuff. So the Algu printer was actually was the first one that I received but I actually had a second printer that came that was the Vauxelab Akila S2 that I ended up writing review for first because I had more experience with FDM printers. I took a while to get everything set up for doing reviews, though, because the lighting in my office was pretty bad, so I didn't have a great place to photograph, and the printer felt like a weight 100 pounds. So moving it around between my home and office was actually not easy. I ended up setting up a little nice photography area in my office with good lighting and took the photographs there, and then I moved the printer to my garage and did most of the printing there because of the smell. And then I just took the printer and I I inspected the office to photograph.

Well, all in all, writing the review itself was fine. It was just trying to use such a huge resin 3D printer when I actually had very little experience with resin printing that proved to be the most challenging. And I ended up writing from the perspective of sharing the details that I learned along the way.

And Tom's hardware was actually very happy with the review itself, but because I didn't have a lot of time, I think it was taking a lot longer than they were hoping for. And I would say the thing that I got most out of the experience is that it gave me better confidence in my running ability.

Paul

Well, that's great to hear. We're almost out of time, but before we go, I've been asking all the questions, and I'd like to turn the tables and let you ask me a question. I'm a big vinyl record fan, so I enjoy the in-joke. What kind of question do you have for me?

Melissa LeBlanc-Williams

Okay. What is your favorite project that you've done using Python or CircuitPython?

Paul

My favorite project is there's two that immediately come to mind, and they're both to my run. and they're both music related. One, I have a feather with 8x4 neopixel matrix on top of it, and I soldered on a microphone, and it sits inside my speaker base.

So the speaker's on top of it. So as my music plays, it's sound reactive, and the neopixels change. And then I have a Raspberry Pi project.

There's a library that connects to Denim Audiovisual receivers, and I programmed it to control my receiver zone two in my office from that so I can change the inputs, change the volume, I can mute it if a call comes in. So those are probably two of my favorite projects that I've done so far. Last question.

You're about to start a new project or a prototype. Which microcontroller do you reach for?

Melissa LeBlanc-Williams

It kind of depends on the project. But in general, I'd go for the feather form factors. Like, if I need internet connectivity, I may reach for a board with an ESP, 2S2 chip, or maybe a Raspberry Pi that's more appropriate. If I need a funny Bluetooth, I'll probably reach for an NRF 52 board like the NRF 52840 feather. And if I just need something in general, I tend to just go for a feather M4.

Paul

Before we go, if anyone wants to follow you on Twitter or subscribe to your YouTube channel, where can they find you?

Melissa LeBlanc-Williams

They can find me on Twitter at @MakerMelissa, or on YouTube you can search for Maker Melissa's lab. And I should just come up on the results.

Paul

Thank you to Melissa for being on the show. You can find Melissa and her projects on our YouTube channel at Maker Melissa's Lab. For show notes, transcripts, and to support the show, visit CircuitPythonshow.com. Until next episode, stay positive.
