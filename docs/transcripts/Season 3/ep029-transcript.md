---
date:
  created: 2023-06-05
title: "Episode 29 - Martin Tan"
---

## Show Notes

[Show notes available here.](../../episodes/Season 3/ep029.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cuddler. This episode I'm joined by Martin Tan.

Martin wrote the first Code Club moonhack projects in Scratch and Python, used by over 10,000 kids in Australia. He also blogs on Maker Topics, runs a Maker Store, works in IT security, and contributes to various open-source projects and community conferences. Martin's latest book, Microbit projects with Python and single-board computers, building steam projects with Code Club and Kids Maker Groups was published this past April.

Martin, welcome to the show. Thanks. Great to be here.

How did you first get started with computers and electronics?

Martin Tan

I used to do a paper round when I was in grade six, which would probably be maybe 11 or 12 or something. Parents really, they initially wanted me to do it. And then they realized that it cost them too much to repair my bike and everything.

So eventually they got a computer and I quit my paper around and I'd come home and play with this computer. It's the usual thing, get sick of playing games and we used to have to type in all our games as well. I noticed that, you know, it was basic and then there was a semi-language.

I just went straight to a semiling language and started looking at how things worked. And I looked at, yeah, how's this work? Oh, it starts this code here.

And then I went through and, yeah, one thing led to another. And I'm like, oh, a system call, print something on the screen. And I'm like, oh, okay.

And then I was like, that worked. So wait, what does that do on the becubbers? And so I looked in the system call and I just copies a byte from one location to another.

So what if I copy something to, you know, copy something to, you know, 1.2.4 in memory. And it appeared on the screen. And so I'm, oh, well, that's another shortcut.

And then after that, it was, oh, you can do interrupt-driven programming and you can make all these things happen really quickly unless you just really loaded up, which I did. And the whole computer started to slow down. But, yeah, it was pretty exciting.

And that's sort of how I got started. And fast forward to, yeah, when I got into security, and strangely, all these useless things became really useful for, you know, reverse engineering malware and things like that.

Paul

Your new book, Microbit Projects with Python and Single Board Computers, was released this past April. Tell me a little about the book.

Martin Tan

Yeah, Aaron from Apress hit me up and said, oh, because I've been writing some tutorials on a blog. And he said, oh, who does these? I don't know, that'd be me.

Yeah, we had a brainstorming session, and it just worked. It was in the middle of, probably in the middle of the pandemic, where everyone had crazy hair and was getting up at silly times of the day. and working from home a bit more than they normally do.

It just came together and pretty much I did several years of Coat Club. So there's Code Club World, Code Club Australia, Code Club UK. At my son's school, I volunteered, well, I actually asked how, they registered for Coat Club and I asked how it was delivered.

And that seems to mean I want to volunteer. So I ended up volunteering for that. Yeah, the teacher who'd been there from the start, so I said, oh, it's like several years now.

This is quite an epic thing. All these things that we learned from making lots of mistakes and getting really frustrated and having lots of false starts, turned out they would be really good to put into a book. And that's essentially in a nutshell.

That was, this is what we did. This is, yeah, I'm not a teacher. I do have a certificate in course development and training.

And I do train people in secure development. But other than that, I hadn't really taught kids. For those who might not know, what is a code club?

So it's an extracurricular activity, a way of getting kids coding outside of school. Some code clubs run in conjunction with a school, which is what ours was. and others are at the local library.

Coding over here in Australia is in the curriculum, but it wasn't so much. And I really like the idea because I sort of feel like coding and those kind of other skills, they seem to be more empowering when there's something that's yours rather than something that's thrust upon you. And so, yeah, so Code Club is essentially a bunch of volunteers, group of kids sitting down and going through a bit of a curriculum and we just sort of pushed it harder and harder.

It ended up venturing into things like electronics, trade-due printing, that sort of thing.

Paul

Who is the book intended for? Is it more for the kids or more for the folks running the code club?

Martin Tan

So the book is really for anyone who's keen to run a code club or make a group for kids. So that could be kids. There's quite a few teenage kids who do that, but also parent volunteers who are really keen.

There's also a lot of teachers that are quite keen, which is really, really good to see. There's a big difference between when a teacher embraces it and does this sort of tinkering for fun rather than just part of their job. It's a hard message to get across.

you get that look where are you some kind of weirdo who likes this stuff, you know, and it's always a little bit disappointing when I get that. But then, you know, you get the teachers and they get really excited about things. And that's where you're, oh, this is really good.

Paul

Kids learn in different ways and at different speeds. How do you keep the kids interested and not get discouraged?

Martin Tan

I guess a lot of it is reading what the kids are into at, The start, you know, we were just really happy to get through one session. It's strange because, you know, not much should have changed since we started to now. But when we started, we had a lot of kids that had grown up with, you know, tablets, you know, iPads and phones.

And we would say something like, you know, I'll go to the drop-down menu. And they would just look at us blankly. And they're like, oh, these, like, that's interesting.

Or they wouldn't know how to use a mouse. or they would touch the screen and be like, don't touch a screen. And yeah, so there are a few challenges with that, but we started to read what different kids were into.

So, for example, if you get a kid and sits his fingers on, you know, W-A-S-D and holds a mouse, then this kid plays games. So you can kind of hook into that. Other times you might just see different things, that the kids like about things and you know you can you can talk to them about that and the other thing is just i guess telling them what we're thinking so so we would sit down and verbalize and that's something that i talk about in the book is verbalizing what you're thinking your thought process and and then we get the kids who've coded before so yeah they're pretty easy i guess that there were limits, though, with that, we did try and just focus only on Python because, you know, if everyone's doing the same thing, it's just so much easier. But I feel like we had one hour a week.

If we showed them five or six different languages, they just wouldn't get fluent in any of them. And the whole idea was to empower kids and give them something that they could, whatever language it was, stick on that language and get them at least fluent enough. to be able to, you know, not just follow, you know, copy directions, you know, to actually think of something that they want to do and be able to express themselves by creating this with code and communicate with it.

And we did see, we did see a few really good school projects that came out of it as well. So we would go along, you go along to some kind of open day or something like that. And there'll be one of their code club kids and they've written something.

So, yeah, it was always really good to see that.

Paul

So in addition to the Python, the book talks about the Microbit and MicroPython. Did the kids favor Python or the Microbit projects one over the other, or does the curriculum take them through both?

Martin Tan

The Code Club curriculum does have microbits, but more the sort of drag and drop type of thing. So they've got to scratch modules, and so there's a whole curriculum of scratch modules. I can't remember how many there are, but I think there's over 100.

modules there and they're all free and it's free to sign up for a code club which I think is a really really good thing I think the kids just with Python they they saw it as Python and it was it was pretty universal so I would talk a lot about hey why don't we do why don't we do this project because you've learned about lists you've learned about these and we try and put in a bit of terminology in there I guess not to make it technical but just to give them a way of, you know, if they talk to someone who was accomplished programming, they could communicate with them. And that collaboration is something that we talk about as well, that co-club. And I've also included a lot of that in the book as well.

Paul

How did the kids collaborate rather than working on each project by themselves?

Martin Tan

I think it was just inevitable that they would start to collaborate because we'd end up with a bunch of kids who were a little bit ahead. or had finished a bunch of projects. And then we wanted everyone to complete projects.

We did find that when people stopped, when it got hard, they wouldn't learn. I mean, we all know what it's like when you start debugging things yourself and then you realize you actually understand more from that, but it's quite easy to just stop there. So we're really focused on completing the projects, not just for the sake of completing them, to make sure that people broke through that gateway of understanding how to overcome the adversity of, you know, things aren't working as they should.

How do I, how do I fix it? You know, how do I discover what went wrong, that sort of thing? And so then it just came into, I think the first project that we did as a group was called devs and testers.

Essentially, the kids just had a, they picked a project that one of them made. It was a pretty generic little game. Some of them were devs.

Some of them were testers. And I just had a Canban thing on the, you know, with three columns. Much like GitHub, a very simplified GitHub on the whiteboard.

And they had Post-it notes. And say, all right, you need this group of testers needs to, you know, to find bugs or find things that can be improved. And then you put them on a post-it note and the devs team will look at it and work at, you know, they'll prioritize which ones are worth fixing and adding.

I thought we would have, yeah, issues with collaboration, you know, because you can't. It's really hard to merge code on something like, you know, scratch.

Paul

Kids like to surprise us. Do you have a favorite story from your time running a kids club that may have surprised you?

Martin Tan

We had this one guy, Jamie, and I wouldn't say he was, he came back as a volunteer as well later on. So when he was in Code Club, he would, and this was back in the scratch days, but he would, he was just so prolific with, he would sit there and he would work out what he wanted to do. do and he would just sit there and nut out.

And he'd have all bits of code, you know, back in scratch that would be, you know, a bunch of blocks just sitting somewhere orphaned. And he would have all these things so he could remember in case it didn't work. But one time I do remember, he came back from holidays and he was messing around with the game and I said, oh, I was that, your new game.

And I knew he made multi-level games. I said, how many levels have you got? And he's gone 13.

And I'm like, say, you just, over a couple of weeks, you've just written a 13 level game. And they would just jump in blocks and things like, as the type of thing that you would see is, I don't know whether he ever went on to, you know, make a mobile game and that. But that would be the type of game that would just take off on mobile.

And I think that was one of those times where it was just mind-blowing that, you know, someone did that. And the other time was where I was on one of the school camps that I used to go along. So I had one of the students sit next to me, you know, as your bus buddy, you had to have a bus buddy.

Didn't say a word. But this is a different person who didn't say a word. It's interesting that people who like coding that don't talk a lot.

They said, ah, she loves Code Club. I'm like, oh, right, okay. And as soon as I mentioned Go Club, she just did not stop talking.

It was super, she's like, I can't wait to get home and go and program things and scratch again and that. And so that was one of those things that we really wanted because those kids will probably still be doing that stuff even, you know, long after Coat Club. And that's, you know, it's become theirs.

And I think that was one of the one of the things that makes Code Club make a difference because you're giving the kids, you're empowering them to be able to make a matter. their own things and to also teach themselves.

Paul

So we're almost out of time. Last question I like to ask is you're about to start a new project. Which microcontroller do you reach for?

Martin Tan

So typically it's the most minimal board, microcontroller board, that will do the job and is currently available in large enough quantities for their job, which really, really knows it down these days. So, you know, sometimes that will be an ESP 32. or, you know, an RP 2040 is probably one of the most readily available for us.

Paul

Well, I'll make sure that I link to the book and the show notes. Martin, thanks so much for being on the show.

Martin Tan

Thanks so much. It's been great.

Paul

Thank you for listening to The CircuitPython Show. You can buy Martin's book, Microbit projects with Python and Single Board Computers, building STEAM projects with Code Club and Kids Maker Groups, directly from APress or from Barnes & Noble or Amazon with links in the show notes. For show notes and transcripts, visit CircuitPythonshow.com. Until next episode, stay positive.
