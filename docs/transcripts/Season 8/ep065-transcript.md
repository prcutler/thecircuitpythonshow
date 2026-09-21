---
date:
  created: 2026-09-21
title: "Episode 65 - Andrew from Keep Everything Yours"
---

## Show Notes

[Show notes available here.](../../episodes/Season 8/ep065.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode I'm joined by Andrew from keep everything yours.com.

Andrew is a software engineer by trade, but has always had a soft spot for blinking lights and clicky buttons. Andrew's goal is to spread the knowledge he has accumulated to show people that there is no magic behind technology that they can't understand and that they can keep everything theirs. Andrew, welcome to the show.

Andrew

Hi, it's nice to be here.

Paul

How did you first get started with computers and electronics?

Andrew

So my dad, when I was a little kid, he was always messing with electronics and stuff like that. We had the propeller microcontrollers, which are, I think they're still around, Parallax. That's what the company was called.

So we started with those, and I was around him doing that kind of thing. And I kind of went away from it for a while, computers and stuff like that. And then in high school, I took an intro to computer science course.

And that's really kind of where everything really started for me. And yeah, ever since then, computers, computer science, anything to do with electronics has been what I want to do.

Paul

How did you discover CircuitPython?

Andrew

So CircuitPython, I started with Arduino, like I think a lot of people do. It's, you know, easy to pick up, all of that stuff. And I was using it.

And then with their acquisition by Qualcomm, they made some changes to their like terms of service and things like that. that I don't think I necessarily agreed with and had some confusion around them. And so I started looking for alternatives.

And I found CircuitPython. And it was basically 100% of the functionality I needed with like 10% of the effort to get set up and use and everything like that. So I guess it was a good thing in the end that Arduino move things around a little bit because otherwise I don't think I would have looked.

Paul

Your business and homepage is at Keep Everything Yours.com. Tell me about Keep Everything Yours.

Andrew

So keep everything yours is, you know, what it says. I want to make things that people can keep for themselves that are yours. A lot of services and products today are subscriptions or closed source.

You know, I heard so many stories and watched, you know, little documentaries here and there people. And they had a piece of software or a machine that was part of their daily lives. And it broke down.

It was no longer supported. and now all of a sudden, that's gone, right? Like the company went under and there's no more support for that thing.

So I wanted to avoid that and let people keep everything yours. So everything I do is open source and right to repair, everything like that.

Paul

What was your motivation or inspiration for sharing tutorials on keep everything yours.com?

Andrew

Part of keeping everything yours in my mind is being able to do what your. yourself, right? It's a give a man to fish, he'll eat for a day, teach you a man to fish, he'll eat forever. If I put stuff out there and people can repair things and stuff like that, that's great. You know, you can follow the instructions and all that stuff. But in order to really, in my mind, truly have something be yours, you need to know how to, you know, maybe not necessarily get in there and like change the spark plugs on your car yourself, but you know, how the whole engine works, that kind of thing. And so I wanted to give the tutorials so that people can keep things yours, but they can also diagnose issues with other things they may have and also have that prerequisite knowledge so that if they ever want to, I don't know, make something themselves or modify the things that I make, they are able to.

Paul

So the first tutorial you created is getting started with CircuitPython on keep everything yours.com, and you used web serial to make it interactive. How did you take advantage of web serial to make it interactive right in the browser for the folks to learn from?

Andrew

So web serial is really awesome. If you've ever used a serial monitor in Arduino or wherever else you might find a serial monitor, it's the same thing. Just the functionality is packaged into a website.

It lets you do all of the things that you would normally do in CircuitPython. It really is no different. The only difficulty is building another interface for that serial connection.

Paul

I've seen a lot of tutorials and read a lot of tutorials online, and I really really have like the interactive nature of it. What inspired you to make it interactive for the user?

Andrew

I mean, I've done the same, right? I've looked at a ton of tutorials and things like that. And, you know, it's not like there's a huge disconnect between you read the instruction, you follow the instruction, that kind of thing. But reducing that friction even a little bit, it makes it nicer, easier to use. And if, you know, 10% of people say, that's too much work to go to this other thing and yada, yada, yada, download an app, and that's 10% of people you lost and if you can increase by, you know, even 5% over a wide range of people, that could be quite a lot.

Paul

After finishing the tutorial, what will the user have learned?

Andrew

So for this first tutorial, I wanted to just basically get set up out of the way, all the way through some sort of feedback, because, you know, you can do a tutorial. And then at the end, it's like, congratulations, you did it. But you don't see anything.

That's, it's not a, not very satisfying in my opinion. So for this first tutorial, it starts with, you know, a little bit about what CircuitPython is. is how you download it, how you install it onto a CircuitPython compatible microcontroller.

And then there's a brief section about talking about the fact that you don't need my website to do it, right? You can use any kind of text editor or whatever like that because, you know, keep everything yours. I don't want to just become another person that is keeping everything from you, right? I want people to be able to do these things themselves. So it covers setup, how to use my website, how to use not my website, and then it goes through, basics of serial monitor, input, output things through there, because that's so useful for debugging and stuff like that.

And then it talks briefly about setting up how to light up an LED without any code, just for people who might not have any base electronics knowledge, talks about current limiting resistors a little bit, things of that nature. And then the final step in the current tutorial is taking all of that and then using it to actually blink that LED with code so that you get a little something. that you can have on your desk and save there.

I did that and it's doing what it's supposed to.

Paul

Right. That blink animation is always the first step on these journeys and that feeling that you get is always such a nice feeling when you get it working. What tutorials do you have plan next?

Andrew

So my grand plan for the future is that I want it to be sort of a skill tree idea. So you start with the very basics blink and LED, take button input, things like that, and then expand them and have them kind of connect to final projects. So I have like some things that are like a little desk pet that has a screen and a button, things like that.

And I want to have people be able to start with, okay, getting it set up, how to run the screen, how to run the button, and then those all connect together to a final product. So everything will kind of end at a final thing that uses all of the prerequisite knowledge. That's the big idea.

Paul

So you just mentioned the desk pets. You have some CircuitPython powered products for sale in your Etsy store, which I'll link to in the show notes. Tell me a little bit more about the desk pets.

Andrew

The desk pets, so I like them a lot. They're very simple. They're a capacitive touch sensor, which you can, you know, sense touch through like a 3D print or something like that. And a small OLED screen, I think it's an SSD 1306, something like that. It's listed on my website. And they just sit on your desk. They have friendly little eyes and you can pet the top of their head and then the eyes turn into little hearts.

They're just meant to be sort of a little companion, you know. And they're also really good for rubber duck debugging. I don't know if you've ever tried that, but it's just having little eyes and a little bit of interaction does sort of help facilitate that.

Like you're actually sort of interacting with something.

Paul

What other products do you have available in your Etsy store?

Andrew

So I have the desk pet and then I have a couple of variations of that. There's one that's like a little devil, a little robot. And then on top of those, I also have a macro pad, a small macropad that the idea with that one was there's a lot of macropads that are reprogramable, right?

But they almost always require some sort of external software, some something to reprogram them. Mine, leveraging CircuitPython and the ability to, you know, edit the files on the device, you hold the button while you plug it in. It opens up and then there's a text file.

and you just click on the text file, you know, I don't think there's a computer that you can get right now that doesn't have a text file editor. Edit the text file, save it, and then you've reprogramed it to be whatever it is that you need it to be. And so it's, you know, it's very low barrier to entry.

You don't need to download a program. You don't need to know really anything to get started with that.

Paul

Oh, that's great.

Andrew

And then the only other thing I have right now is a small media controller. So essentially it's just a volume knob that you can press and it'll pause play your music. but, you know, it's all open source and editable, so I know somebody bought one of those, and they wanted it to do, instead of volume, like Next Track, Previous Track. And so, yeah, they set it up to do that.

Paul

Nice. In addition to Keep Everything Yours.com, where else can people find you online?

Andrew

The other big place I'm online right now is my YouTube channel. Just keep everything yours on YouTube. And, yeah, I post videos. I haven't posted one in a little while, but my intention is to pick back up on that and post tutorial and build videos for the projects that I'm working on.

Paul

Last question I ask each guest. You're starting a new project or prototype. Which microcontroller do you reach for?

Andrew

So right now, the one that I reach for every time is the RP 2040. I think originally there by WaveShare, but there's tons of clones. They are small.

They have a built-in RGB LED, like a NeoPixel. They have tons of pins broken out and everything. And they are less than $2 each if you buy them in a decent size bulk pack.

Yeah. And so that's the one I'm going for every time right now. Unless, you know, I need Wi-Fi or Bluetooth, and then it's some kind of ESP-32 variation.

Paul

But you can't go wrong with the price of those waveshares, that's for sure.

Andrew

Yeah.

Paul

Andrew, thanks so much for coming on the show.

Andrew

Thank you for having me.

Paul

Thank you for listening to the CircuitPython Show.

For show notes and transcripts, visit CircuitPythonShow.com. and help keep the show ad-free. Become a supporter and get access to exclusive content and more. Visit CircuitPython show.com slash support to learn more. Until next time, stay positive.
