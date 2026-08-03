---
date:
  created: 2022-12-12
title: "Episode 24 - Alec Delaney"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep024.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Alec Delaney.

Alec is sponsored by Adafruit to work as a part-time developer on the CircuitPython project. He works on the Python libraries, as well as the continuous integration across the organization. He's also a maker working with CircuitPython to create robot friends, and currently works full-time as a mechanical engineer for a medical device company.

This episode is brought to you by PCBWay. With over a decade of experience, PCBWay is one of the most experienced manufacturers in PCB prototyping and design. Whether you're an engineer, students, or hobbyist, PCBWay offers a simple and fast prototyping service, and it's cost effective at only $5 for 10 PCBs.

And check out PCBWay.com slash project where PCB way helps makers and hobbyists collaborate on their designs and projects. Make your design a reality and check out PCBWay.com for all your PCB needs. And they also now offer CNC machining and 3D printing services.

visit PCBway.com for more information. Thanks to PCBWay for their sponsorship. Alec, welcome to the show.

Alec Delaney

Thanks for having me.

Paul

I'm glad you're here. Tell me how you got started with computers and electronics.

Alec Delaney

The first memory I have really of programming on a computer actually was, I think back in grade school, it was with JavaScript. So I started off. I know a lot of people start off with like C or, you know, whatnot.

But I started off with it with a pretty dynamically type language. So that's how I got my start. And then I went to school for engineering, but I actually went for mechanical.

But one of the courses we had to take was a kind of like a programming course where we had MATLAB, which is a language used pretty much a lot by mechanical engineers and electrical. And then the other one was actually C++. So that was kind of my second language.

But then being in a field sort of next to hardware and data collection and therefore data science, Python came up pretty quickly thereafter. And so I found Python. And then being in hardware, knowing Python, it was only a matter of time before I stumbled upon CircuitPython.

And I fell in love immediately just to be able to have an idea and know Python and get started on a microcontroller to remove that barrier of knowing how to. compile or set up a tool chain, it just, it was, it was magic to me.

Paul

You're sponsored by Adafruit to work on continuous integration using GitHub actions for a number of the CircuitPython repositories. For those that might not know, what is continuous integration or CI?

Alec Delaney

Continuous integration or continuous development is the process of basically removing the manual steps from parts of the code cycle. So of course, there's, development and there's writing code, but there's all the other parts like testing and shipping that need to happen to kind of create good code and best practices. And so what CI does, continuous integration is the process of constantly doing those, right? So instead of, you know, asking people like, hey, do you mind testing that code or, hey, do you mind zipping it up and, you know, uploading it, it does it automatically, basically. And so it's that process for, just really, you know, those are just some parts of the CI for the CircuitPython project and the Adafruit uses in general is pretty varied in what it does, but it all does that, basically. It all automates these, you know, sometimes critical processes behind the scenes so that everything just kind of works seamlessly.

Paul

So tell me about some of those things that are behind the scenes that, you know, the average user doesn't see that makes all of this happen to bring CircuitPython to that user.

Alec Delaney

So the CI that Adafruit uses, for CircuitPython and really the whole CircuitPython ecosystem. Some of them are kind of where you might expect in that traditional side of things, right? So, for example, one important job the CI does is for actually taking all of the library code and kind of bundling it, quite literally, you know, for the CircuitPython bundle, and, you know, creating that bundle and uploading it to various places.

For example, CircuitPython.org, it handles uploading it to there, also handles creating GitHub releases. So likewise, it helps put it on PyPi. So it does all of these, you know, more traditional things that you would expect a CI to do.

Again, you know, there's a whole bunch of infrastructure for testing code. All the code comes whenever you create a library or submit a change to a library, all the formatters, a linter runs, all of these very traditional CI things. But what's really cool is that we actually use the CI for some other things that are, you know, I would say are pretty important, even if they aren't the most traditional use.

For example, the weekly meeting that's held every Monday, the meeting notes for that are actually generated by the GitHub action CI, which is really cool because a lot of the stats were reading, how many pull requests, how many milestones, who are our new contributors, right? That information is GitHub information. So we just were able to take that and run it through the CI and get that almost natively, if you think about it, and then create this document and upload it to AWS.

And so that whole process is completely obvious. automated. It's actually automated daily. So at any point, you could see that information.

We only read it once a week. But yeah, you know, I think that part of the cool thing is that we use CI pretty regularly, pretty widespread across the whole project.

Paul

How does the continuous integration make it easy for developers and or the users?

Alec Delaney

Yeah, that's a great question. I would definitely say that, you know, for sure, it's probably felt most palpably by developers or even just contributors in general, you know, especially with those traditional things. One of the most important things as a developer when you're writing code is that, you know, when you submit it for a pull request, other people are going to be looking at it.

So you don't, you not only want to make sure that it's good code, but that other people can follow along. And so, of course, that means things like commenting and whatnot. But part of that, for example, is readability.

So part of what the CI's job does across all the, the libraries is formatting, right? So we use black. It is, if I remember correctly, the tagline is the unrelenting formatter. It pretty much standardizes what code will look like. If I ran black on the same code as you, we should get the same thing. So what's great about that is that when I write code and other people are going to look at it, I can focus on really what it should be doing, I focus on, you know, is it doing what it needs to do?

And then kind of throughout the process or even at the end as well, I can have all these automated tools run and say, okay, I'm going to move this over here. It seems more readable. Or I can have the linter say, oh, hey, I noticed you aren't using this variable.

Like we should remove it. So I can focus on writing the code and anyone who's contributing can do the same. I would say for the users, it's definitely the more not fringe, but the other uses of that.

When we talk about how people load code onto the Feather M4 Express, which can hold, I think it still can, all of the libraries, and so that's where the bundle comes in. That bundle is created by the CI. From the user's perspective, it's as easy as going to CircuitPython.org and just picking up this zip file.

But behind the scenes, there's the infrastructure to make the zip file. And before that, there's infrastructure for making sure if someone updates one of the repositories that that gets put in the bundle. And, you know, you can go up the chain a long ways from there.

But, you know, in the same way that CircuitPython makes, you know, editing code really easy, the whole project, and ATIF root in general, uses CI to just make the whole development and user perspective a lot easier.

Paul

And all of this is done using GitHub actions?

Alec Delaney

Yeah. For the CircuitPython project and Blinkin related things, I know that GitHub Actions is used. I think before that they used Travis.

Paul

That was a popular CI back in the day.

Alec Delaney

Yeah. I think I came, I think even the Arduino Library still use it. But yeah, everything is pretty much all GitHub actions.

And that's its own ecosystem of cool tools and whatnot. One of the projects that's on my plate now is a lot of that has. to be updated. So I am actively taking a look at that all over again.

Paul

One of the other projects you're working on is moving packaging to use the PyProject.toml files. What are some of the challenges in moving to that system?

Alec Delaney

So one of the biggest challenges of that is honestly just how to do it. You know, the task, this is one of those things where the task is really simple. You know, a lot of the information is already there in what was set up.Pi.

so the previous file that had all of the information for, you know, PyPI, and if you installed locally how to do that. But moving that to a new file format is tricky because you can't just blanket copy things. So you can't just copy paste things, of course, but you also can't just use, it's hard to use a template because some of that information is specific to those files.

So some repositories, for example, have keywords. so that if you're on PyPi, you can search for them. So those are specific to each file.

The real challenge there was a blend of how do you use templates, and there are some tools like, I remember correctly, format patch, so you can make a commit in one Git repository, and Git can kind of try to apply it to other ones, and that's actually something Atabot does, which is really the mastermind developer tool for helping with some of these things. but it's hard to do that here because some of the things, you know, you can't do that with keywords, for example. So it took a lot of manual tooling behind the scenes along with the CI to kind of create a hybrid solution that could, you know, template these files and upload them.

And then, of course, there's all the whole tooling for getting it, you know, checking it and making sure that everything went correctly. One of the classic failures is, and I still have to remind myself that they aren't the same, is their Python, in the packaging world, there's modules, which are these like single files, and then packages, which are a folder of files. And from a user's perspective, they're entirely the same.

But when you're writing these files, it's really important to tell the file which it is, and if you get it wrong, it may not be clear, and it sometimes even slip through the CI. So, you know, how do you check things that sometimes can silently fail? So it was all around just a conglomerate or a conglomeration of different problems with unique solutions.

So it was definitely one of my favorite little tidbit challenges so far.

Paul

What are the benefits to using PiProject.toml instead of Setup.py.

Alec Delaney

So PyProject.toml is a configuration file for PIP. So setup.pi is an executable file like any other Python file. And the way it works is you import setup tools and you give this setup function all the information you need and then it builds.

The issue with that is you already need setup tools to use it. And so it kind of creates this chicken and egg problem where you need. set up tools to call that setup function, which in turn has a setting in it that you can tell it what dependencies you need. But in order to do that, you already need it. And so that was the major problem that moving away from setup.t. Pi to project that toml solves, that wasn't necessarily an issue for us. A lot of builds come with setup.tut tools. It might even be default with Python, which is how it gains such a foothold.

But there are other build packages or build tools, like Flit is another one. And they use Pipeproject.comble for that same reason where they specify what they need to build, and then PIP will go install that, and it will do that in a virtual environment, and then build the package. It'll build a source distribution.

It'll do all of that. That isn't to say that setup. pie doesn't have a place anymore. I know one of the major places that I see it a lot still is with the use of cython. So cython is a language that you can write, and it basically is kind of Python-like, and it gets basically compiled down to C code like any other Python C extension, and then that gets compiled like any other Python C extension. But in order to do that, you need to do a couple things in the setup.py file.

So moving things to piproject.comble at least gives them the chance to say, hey, these are the build dependencies we need. And in that, you can even specify psychon. That's definitely the predominant reason.

And then it also gives us the ability to, if in the future we want to move away from setup tools to something like flit or poetry, that both use pieproject.comal, it gives us a better way to do that now that we already have that. And to be fair, I know that Blinka, for example, still needs to use setup.Py. So again, as an executable file, it's able to do runtime dependency.

So one thing that Blinka does, when you install it, it checks for specific libraries that are only available on the Raspberry Pi. So what it's able to do is as you're installing, they can say, hey, are you a Raspberry Pi? Great.

Here's the libraries. I'm going to throw in as a dependency. And if not, then it doesn't do that.

Even on our own projects, there's still a place for setup that pie.

Paul

Switching gears, I wanted to ask you about one of your personal projects, the Circuit Pythonukkah. Tell me about that.

Alec Delaney

I had for a while been wanting to make a project that I could share with people. So a lot of my robot friends that I had made, you know, when I'm not working on the CI, I love working with the CircuitPython boards themselves. I wanted to make a project that wasn't hyper-specific like some of my other ones had been because I wanted to share it.

And one of the things I've really enjoyed about being, you know, working with Adafruit and just working with open-sources in general. And some of your other guests have mentioned how great it is and how much you can learn from people in the community. And there's a lot of great makers that do open-source hardware.

And it was really inspiring to me. And so I wanted to do something that wasn't hyper-specific. and I wanted to do something that I could share.

And so when I was thinking of things, I think one day I had come home, you know, much around this time when, you know, up in the Northeast, it gets dark so early, around the holidays. And I was thinking, you know, oh, man, like, I'm going to be late to light candles for my, for my Hannukkah, or, you know, you may say, menorah. And it kind of hit me that I was like, I could probably automate this.

Like, I could probably come home and it could be lit. So it kind of like, what started off is this neat idea of having that happen turned into this project. So the circuit Pythonukia is exactly that.

So it's a custom PCB, which was fun. It was my first PCB I've made. And what it does is it's got LEDs on it and it runs on a QTPI S2.

And it's got the LEDs. It's got a Piazo electric buzzer on it. And what you do is you plug it in.

The QtPyS2 connects to the Wi-Fi, and it looks up the date. It looks up when Hanukkah is, and then it says, you know, either, hey, it's Hanukkah, and it lights up the correct candles and plays a little tune, or it will wait to do that. And what's really exciting is I just, it was the first, it's been the first project that I've done in open source that I went and got open source hardware certified.

So I went and got it, and now as it's, I just reordered the boards with its, certification mark on it, and I'm excited to hopefully, if the holidays slow down a little bit in how fast they're coming, I'll try to get those out to people before Hanukkah starts.

Paul

What a great project. My last question for you, you're about to start a new project. Which board do you reach for?

Alec Delaney

Yeah, I'm definitely biased after the Circuit Pythonukia project. I would definitely have to give two answers. I think that any of the RP 2040 boards, especially with, you know, ship shortages and whatnot, how available those have been and how cheap they are is it makes it just a fantastic chip to work with, you know, knowing that I can grab any one of the CircuitPython boards that has the RP2040 and start, you know, hacking away and not have to worry about too much is great.

And how on top of things they are, you know, shout out to Jepler, who with the Pico, the Pico-W, how great that is any chip. Now it has Wi-Fi built in, right? So now you can use the RP2040, and great, you have Wi-Fi included.

But I also do, there's a special place in my heart, not just from this project, but more from my mechanical side where when I'm thinking about, you know, how I'm going to make things and make things small, especially, the QtPy format, and specifically I really enjoyed S2, just knowing that if I'm doing something smaller, or I want to, you know, there's a lot of constraints, and I only need a few inputs and outputs anyways, just knowing that I can make something and add that to the board really quickly and, you know, have a lot of flexibility on just one tiny little format is just a joy.

Paul

I'm with you. My current projects are using the ESP 32S2 as well, and it's just a great chip to work with. And having Wi-Fi just changes the entire game.

Alec Delaney

Absolutely. I figure if the CircuitPythonukkah had, you know, perchance doesn't happen this year. I've already made the order, and I already have 15 cutie pies here. And, you know, if I have to use them for other things, then oh, well, so be it.

Paul

I'm sure you'll find a use for them. Alec, thanks so much for being on the show.

Alec Delaney

Thank you so much.

Paul

Thanks to Alec for being on the show. That's a wrap for season two. Thank you to everyone who has listened and the show will be back in early 2023. Until then, stay positive.
