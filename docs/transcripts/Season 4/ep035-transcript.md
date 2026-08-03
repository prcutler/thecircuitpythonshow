---
date:
  created: 2024-01-15
title: "Episode 35 - Jeff Epler"
---

## Show Notes

[Show notes available here.](../../episodes/Season 4/ep035.md)

## Transcript

Paul

Welcome to the CircuitPython show. I'm your host, Paul Cutler. This episode, I'm joined by Jeff Epler.

Jeff has been a computer programmer since he first started typing and program listings on a Commodore VIC-20 when he was eight years old. Jeff's hobbies include electronics, 3D printing, photography, and beer and winemaking. Since 2019, Jeff has been sponsored by AidaFruit to work on CircuitPython.

Jeff, welcome to the show.

Jeff Epler

Hi, it's good to see you, you know, here in the holidays. It's nice to have something because otherwise I'm taking this week off.

Paul

How did you first get started with computers and electronics?

Jeff Epler

So I first got started with computers when my dad bought a Commodore VIC-20, and you can type in the basic programs from the manual, and I was like instantly hooked, and I've just been doing computers ever since. So that was sometime back in the 80s. It's a few years ago.

Paul

How did you first get involved in open source? You mentioned on your blog that you've been involved with open source for almost 20 years.

Jeff Epler

I was just starting to use Unix computers at the university, and there was this Linux thing that was starting to, people were starting to talk about it, and I put it on one of my home computers, and I just thought this is great. I love the idea of sharing with people and collectively benefiting from the programming effort that we all put in. And there are some problems, like with that original generation, the philosophy of those original generation of open source.

free software people. And I think we need to work on that and make it more inclusive, but I still think that core idea of, I want to make stuff and it doesn't take anything away from me to share that with you. I think that's just one of the most wonderful things that I can do.

And I love it. I agree. How did you discover CircuitPython?

I was hovering in the 80-fruit sphere and picked up one of the Trinket M-Zero boards. I'm like, this is under $10. It runs Python.

I just have to see what this is because I had been perfect. Python since Python version 1.3. So again, a long time ago, this was the 90s, and it was my favorite programming language, and just the idea to be able to do it on hardware was super cool.

Paul

You're one of the few core developers for CircuitPython. Being a core developer is more than just writing C or Python code. How do you view your role as a core developer?

Jeff Epler

So what I like to do is enable people to do cool stuff. I'm really inspired by my colleagues, in particular, Aaron, who goes by Firepixie, just does these amazing things. And CircuitPython is inside that.

So I remember collaborating with her on the Banjo project. And this was, Lamar's idea was, let's do something that uses MicroLab, which a community member created. And it's a version of NumPy that runs within CircuitPython.

And Lamar thought, well, we can do something that is sound reactive with this because we can get the sound in. and process it and do something. And Aaron's idea was, I want a light-up ukulele.

And I was kind of in the middle and figured out how do we do some effects. And she made a beautiful project out of it. A little more was happy.

And I'm like, this is, you know, I want to help people make beautiful things.

Paul

I love that project. That was one of the first projects that I kind of deconstructed and to recreate my own audio reactive project. And that one has a very fond place in my heart for me.

Jeff Epler

Yeah, there's a lot of stuff going on in that because I think Rose Hooper had recently done the stuff that let you treat two strands of LEDs like they were one strand of LEDs by renumbering them. So it was just a bunch of things came together from the community to make that project happen.

Paul

You've shared on Adafruit Show and Tell various retro keyboards that can be used with CircuitPython and a machine you've restored. Do you have a favorite type of retro computer?

Jeff Epler

You know, I have a weakness for the Commodore computers because that's what I grew up. on. So, like, to this day, people make new graphical and sound demos for the Commodore 64.

One of my favorite people who's making software on the Commodore, and he's making music, is Linus Aikason. I'm sure I'm butchering his name, but he's created kind of a guitar-style thing with a slider that doesn't affect, and you play on the keyboard with one hand. He's created a musical instrument he calls the Com accordion, which you operate it kind of like and again with the keyboard to create the notes.

And I'm like, this, this is amazing. I don't, you know, do retro computing at this level, but I love looking at people who are doing it. And he puts out amazing stuff, and that's on Commodore.

So I'm going to pick Commodore as kind of my favorite. It was a really cool, cool company with cool ideas.

Paul

Looking ahead to CircuitPython 9, which should be out sometime in 2024, CircuitPython 9 now supports the Momento, the new open source CircuitPython-powered digital camera. What were the challenges in bringing JPEG support to CircuitPython?

Jeff Epler

If I say it was easy, so again, it's the power of open source. We had identified from some other projects we did at Adafruit that there were some JPEG libraries out there. And the one that I picked after looking at them and getting advice from other people is, I think, T.JPEG deck, which was written by somebody else.

It's designed to run on microp controllers. And really, it was quite easy to slot that into CircuitPython. and get the very first, you know, I've got a JPEG image representative memory, and now I want to put that in a bitmap and show that in some way.

That was like a day of work. But then after that, it's like, but how do we turn this into something that is useful? So, for instance, maybe your JPEG file is coming from the Internet, or maybe it's coming off of a file on an SD card.

Maybe it's bigger than your display, so you're going to scale it or crop it or, I don't know, So the process of figuring out those things and figuring out what options are we going to support. And in particular, you can scale it down by a factor of two or four or eight, and then you can crop it as you need to to fit it on your device display. And then, like I said, reading it from a socket or a file, that took a lot longer.

And then the next thing that I'm going to do, hopefully with some collaboration with Melissa, is to put this into the library we call Portal Base. And then it will start just being that much more available to use across the range of devices with screens, which includes things like the original Pipe Portal, the MagTag with the E-Inc display, although I haven't tried that yet. It should work.

It should be cool. And then newer stuff like the Qualia Board, which works with all kinds of different displays. So this is also useful relative to the camera product that you were asking about, but we kind of conceived it more relative to the display-oriented product.

The camera project has been a long time in the works, and a lot of that is because of Parts Shortage and Lemur's time, and now that we finally got the stuff to build that camera, it's really, really exciting. But yeah, the JPEG decoding is more about, you know, I want to show a picture from the internet on my device, and being able to use it to show a picture from your camera on your device is also kind of a serendipitous thing.

Paul

That's great. 2023 was another busy year with CircuitPython 9 development, synthio, JPEG I.O, which we just talked about. Tell me about the work that you did at the end of the year to add a lot of new fonts to CircuitPython.

Jeff Epler

So one of the things, you know, it's always serendipity. What did we do that enabled something else? And in this case, going back to the Memento camera, it has an autofocus mechanism.

I'm going to connect this in a minute. Just bear with me. It has an autofocus module.

And that actually runs a little program in it. So there's a firmware that CircuitPython uploads to the camera module that makes the autofocus operate. And so we needed to include that firmware file within the library, which is called Pi Camera.

And we didn't have support for that in the bundle builder. There was no way to include a binary Python. You could only include Python files.

And so I did some work. And this ends up spreading across several things because you have to make sure it works in the bundler, which creates the zip file with all the stuff inside it. And then you make sure that Circup works, and then you make sure that the system that we have on library, which I think is called Bundlefly Works.

And that worked fine. That was great. Actually, both of those worked.

But anyway, a lot of iteration until that worked. And then I was thinking, what else do we want to put in libraries? And the idea that came to mind was, well, it's kind of a pain to install a font, CircuitPython. We don't really have a way to install a font. You copy it on and then you have to write some lines to say what is the path to the font and open the font and get the font object and all this. And I had the vision that you would just be able to say from module name import font, just like we can say from terminal I.O. import font. And I wanted it to be that easy. And with this thing where we could bundle a bitmap format font within a CircuitPython library and install it with Circup, it's like, this is easy. And the The other thing that made me think of this is our community member, Naradoc has put together, I'm not going to get the name right, but it is a bundle that is full of keyboard layouts.

So like a key thing that a lot of people do with CircuitPython is they use it to synthesize, to create a USBHID device and then do things like send keystrokes. And if you want to type a string like Hello Mom on a keyboard, you need to know the layout of the keyboard. On a German keyboard, the key that we label Q has some other letter on it.

I think it's A. You can't just type A. You have to know the position and then what that's going to do. So anyway, Naradoc created a bundle with all, or not all, but a great number of world keyboards that you can easily install with CirCup. So this is the other thing that made me realize we can create a bundle not by writing each individual library, but by creating them with a series of scripts, which is how Naradok is.

approached the problem. And I'm like, we're going to put this idea together. We're going to put this idea together. And the consequence is now there are a little over 2,000 libraries that you can install. And each one is a particular font at a particular point size. And then it's either like just the ASCII and Western Europe characters, or it's all of the characters included in the font.

And then, of course, the other thing is people put amazing fonts online for free, you know, that anybody can download and use. And so it's just putting this, putting things together from all different people and then enabling people to use it in their project. And actually, yeah, it was really cool.

I'm really excited about it.

Paul

I'll make sure I link to those in the show notes as well. Thank you. Last question I ask each guest. If you're going to start a new project or prototype, which board do you reach for?

Jeff Epler

Well, I mean, the first thing I would do is if you're not totally new to electronics, check whether something that you already have run CircuitPython. We've got a couple hundred boards. You know, I talked earlier about my experience of starting with, like the very cheapest board. And I wouldn't quite go to the very cheapest board, but the QD Pie, ESP 32, S3, with two megabytes PSRAM, I was looking this up, is like $12.50. It's a cute little board, but you can add a display to it. You can add all kinds of sensors to it. And just for that getting started, it has a neopixel. So you can write a Python program to make it show rainbows, which is kind of where everybody starts. So go with the QDPy. This one I suggest has Wi-Fi. Yeah, and you can add a bunch of stuff to it. And it was about, I think it was $12.50 on the Adafruit store. So I think

Paul

it's a really good choice. That's a great pick. It has the STEMAQT, which makes it easy to add

Jeff Epler

sensors and other stuff to it as well. Yeah. And then like the, what is it? There's a display BFF add on board, which lets you put a TFT display. A lot of options to add on to that.

Paul

Jeff, if more people want to learn about you or your work, where should they go?

Jeff Epler

So I think probably the best thing to do is you can follow people. on GitHub and kind of see what they're doing because I don't necessarily write a lot about what I'm doing, which is mostly worked for Adafruit, but you can see there, oh, Jeff is working this week on X. I am on Mastodon. That's not a super technical account.

Paul

We will put that link in the show notes for you.

Jeff Epler

And then I have a blog that's very occasionally updated, more with technical stuff, but, like, you know, just a handful of posts last year, and that is at unpythonic.net, which has been my domain since like 2001.

Paul

Well, that's great. Jeff, thanks so much for being on the show.

Jeff Epler

All right.

Have a good one.

Paul

Thank you for listening. Transcripts are available in most podcast players and show notes are available at www.circuitpythonshow.com. Until next time, stay positive.
