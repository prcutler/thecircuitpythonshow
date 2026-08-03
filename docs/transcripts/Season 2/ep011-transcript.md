---
date:
  created: 2022-06-13
title: "Episode 11 - Anne Barela"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep011.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host Paul Cutler. This episode I'm joined by Anne Barela.

Anne is a professional STEM and maker, educator, and advocate. She is the author of two published books on microcontrollers and numerous electronics tutorials. Anne, welcome to the show.

Anne Barela

Thank you very much, Paul.

Paul

You've been with Adafruit for a few years now. How did you first start working with Adafruit?

Anne Barela

I'm an electrical engineer, but I really hadn't been doing hobby electronics for a number of years, I wanted to pick it up again. So around 2013, I started, like many people with Arduino and making simple circuits and that type of thing. But back then, Arduino's were like $35 a board. And that just seemed a little expensive on my budget. So I saw Aidafruit came out with a small board named Trinket, and I started playing with that. That caught Adafruit's attention because no one else has been really seeing that the stuff for the AT Tiny 85 was a little different than the larger Arduino.

So we had to use some different techniques to get it to do the same thing. So they asked me to start writing guides on what I've been doing. It kind of evolved from there.

Paul

You went on to write a book about that trinket chip, didn't you?

Anne Barela

I did. So Make publishing had asked Aafruit if they would do a book on the Trinket. And the folks that they do for really don't have a lot of time for writing, you know, they're running a company.

So they saw that I was doing things. So they said they passed my name on and they Make came and asked me. And I said, foolishly, okay.

And yeah, the book came out 2015, 2016.

Paul

Well, it must have done pretty well because you went on to write a second book, getting started with the Adafruit Circuit Playground Express.

Anne Barela

Adafriut positioned Circuit Playground Express as kind of their learning board. Again, MAKE was looking for somebody to maybe write a tutorial on it. They came back to me again, and I kind of hesitated because it's like, you know, I already know all the pitfalls of writing a book. But you could say I didn't want to be a one-hit wonder, so I went ahead and tackled that, and that was finished in 2018 in time for Maker Friam.

Paul

So you mentioned the pitfalls. What are some of the challenges that go into writing a technical book?

Anne Barela

Kind of like maybe fiction, you have to do a lot of research. You have to dig into all the resources available. And books like that have a lot of projects.

The first book on Trinket, I reused a lot of the projects I'd done as tutorials and added some more. For Circuit Playground Express, I didn't have quite that same resource, so I had to come up with new projects. That takes time.

Paul

What was your goal with the circuit playground book? Were you focusing more on the hardware, the software? How do you introduce a reader to both of those concepts?

Anne Barela

Both books were getting started with books. And I approach it, you know, I try to put myself in their shoes. Like if I don't know anything about it other than maybe some simple electronics, how would I get started?

So I broke it into starting with make code, which is easiest on programming, introducing what the board is when it has, using make code to do some projects. CircuitPython, it's a little more in-depth. And finally, just how to set up Arduino for it, but not really showing how to program it specifically.

Paul

Having been around Adafruit since 2013, you've really seen the birth of CircuitPython. It's been five years this July since the 1.0 releases come out. What are some of your memories over that time on how the community or CircuitPython itself have changed?

Anne Barela

I was working for the U.S. government as a diplomat up until 2018, and I retired after 30 years, and then I went up to New York City and Adafruit, asked me if I'd like to join the company, and I said, yes, I mean, that sounds pretty good. And so, Circut Python back then was only about a year old, and those early releases really kind of mirrored some of the micropython work and adding some libraries for data-proof hardware.

And they were just getting their feel for what did they want to provide in their version of Python for the customers, and a lot of that was ease of use. So the early years were saying how to make it easy to use Python on microcontrollers. And the main thing, as many people know now, a lot of microcontrollers have USB controllers built in, and that allows someone to plug in a microprocessor, microcontroller, excuse me, and use it like a thumb drive who present the memory as based in which people can copy files on.

That was kind of a breakthrough because prior to that, the program boards, you needed special hardware on your computer, You needed a cable to connect things, and then the software, after you do something with software a compilation or something, you would download it to the board. And that's all very labor-intensive and fraught with learning issues. And CircuitPython avoids a lot of that complication.

You can just get any text editor, put some code in, and try to run it. And if it doesn't run quite right, it tells you. And you can try again very easily.

The iterative process is cut down significantly.

Paul

I couldn't agree more. There are over 75 learn guides that you've written. What goes into writing a learn guide? Originally, it was Limor Fried, Lady Ada.

Anne Barela

She comes up with a lot of the concepts. She sees all and says, well, I'd like to see a project with Trinket and a foot pedal. It's one of them.

And it's like, okay, that's not too hard. And it's like left up to the author to build the circuit and write the code and test it. present the material and document it in a way in which somebody without a lot of technical skills might be able to recreate the project. And again, I use that kind of put myself into their shoes concept to start from basics and lead a person through and getting the project completely.

Paul

Is there collaborative nature involved with it? Are there other people who are proofing the code or proving the actual guide itself?

Anne Barela

Yeah, we have a number of people on the CircuitPython team, for example, who help maintain code and can do reviews of other people's code. I am the initial moderator for all guide. I can get somebody to look at something, but usually it falls back onto me switching hats to moderate the code. Lady Atom does final moderation on every single guide because it has to be up to her standards and, you know, her breadth of knowledge.

Paul

Hi, it's Paul. I'll get you back to the show in just a moment. Thanks for listening, and if you're enjoying the show, please tell a friend or write a review.

You can also support the show financially. Your support helps cover the cost of podcast hosting, recording services, and transcriptions. For more information, visit CircuitPython show.com slash support.

Now, back to the show. You publish the Python and Microcontroller's newsletter every Tuesday. What goes into writing the newsletter?

Anne Barela

A lot more than people might think. There are a lot of different corners of the Internet in which interesting information might be gleaned. And there's like an email address people can use to send in information.

They can hashtag it CircuitPython in various ways. But that doesn't tend to be used much, even putting in PRs on GitHub where we start the publishing. Most of it is hunting through places like Twitter and instructables and hack it.

day and just any place on the web where there's interesting information. Oftentimes I come across it through my Twitter feed, which I've gotten kind of tuned towards this particular subject. And my colleagues at Aida Pro help quite a bit in letting me know what they've seen in their feeds.

So all that is collated and categorized and placed into the newsletter. Oftentimes news comes right to the very end on Monday night, something might happen, and it will get in the newsletter. So I finish on Mondays, and then it's out Tuesday morning.

So it's quite an active process.

Paul

It sounds like it. When you think back over all the newsletters, was there a hardware project or two that sticks out as a favorite?

Anne Barela

I really like the projects that emulate classic computers, one by Raspberry Pi when the Raspberry Pi, when the Raspberry Pi people. first came out emulating a ZX spectrum, or no, excuse me, BBC Micro, which was really interesting that you can get a $4 microcontroller board to emulate a whole computer that costs, you know, several hundred pounds back in the day and still do all the graphics and everything. In that same vein, I'm a PC enthusiast, so anything that emulates classic PCs like IBM PC and that type of thing, I love those too.

But also, I really like projects where people are making something for somebody else. In the last newsletter, there was a box, and on the front was a depiction of Duren's gate from Lord of the Rings. And you had to do certain things to get it to wake up, and then you had to say, enter, or no, say friend in Elvish.

And it actually listened to somebody's voice, and if it heard the right word, it would click open some solenoids and let you inside the box. And that's just brilliant. It's nice.

It's finished. People really don't know that getting a circuit together is one thing, and getting all the software to work is another. And then finally packaging it up.

That third leg oftentimes is just a bridge too far. And when you see people really do it up nice, it's a... great thing.

Paul

Speaking of Retrocheck, when did you first get into computing in electronics?

Anne Barela

It was in high school. I was able to take an electronics course in my sophomore year. You know, I really took to it. I mean, they really weren't teaching us digital electronics at the time. It was much more power electronics and lighting light bulbs and that type of thing. But I really liked it and I thought, yeah, I could do this for a very long time. So I took electronics three years in high school. And my senior year, I also took computer programming, and it just kind of all made sense. So I was looking to go into college to continue that, and I didn't get into my first couple schools, and I kind of had to think, and then I got this brochure that said, well, if you come to our school and you go three years there, and then you can transfer to Caltech, which is a school I really wanted to go to, for two years, then we'll both give you a degree in that.

okay, you know, that's an extra year of paying. It's not so great, but I mean, I actually get to do what I want to do. And that was cool.

I was able to get a electrical engineering degree from Caltech, and that set me off.

Paul

When you have the time, do you have a retro tech project that you're working on or want to work on?

Anne Barela

I do. I mean, lately, I haven't had a lot of chance to be hooking up discrete electronics, but Aetafruit's been working very heavily on floppy disk technology, which is really great. And people wondered why. It's a dead thing. There are so many floppies, and I just didn't have my whole floor over here filled with floppiness that I have from back in the day. But how do you read them? There's a lot of interesting data, and you want to preserve, say, I want to run an IBM emulator or IBM circuit. Eventually, I'll need software. On those disks, the software I can use, how do you get that software onto maybe a flash drive or something to get into your emulator?

That's a head scratcher, and I actually was trying to do all sorts of things a couple years ago to do that. But Aida Proof has been working on the problem, and now they're working on an interface board for a feather, which hooks to a floppy drive. So I wanted to be able to work with very old computers like IBM PCs and be able to transfer data, like on this fast computer in front of me.

There's this concept of a tweener computer, and that's what I've got going right here. So this is a Pentium 3 computer, circa around the year 2000, and it's got Windows 98 and Windows XP dual boot, except it's not booting from a hard drive. It's booting from a SD card right here.

I've got floppy drives. I've got a little bit of the technology is upgraded. The CD DVD ROM is maybe from 2002 or later.

It is a flat panel display, GASP. I'm sorry people, it's not CRT, but it is vintage and the zip disk and the external floppy. So I can do quite a bit of data archiving and playing around on a machine like that, which is not very easy with the modern motherboards in our computers, or very old computers.

I can use this to kind of talk the language of the very old computers while still using, say, the Internet to download maybe some other technology or to upload it to, say, Internet Archive.

Paul

We're almost out of time, but before we go, I have a segment called Turn the Tables, where I've been asking all the questions. Now it's your turn to ask me a question.

Anne Barela

Well, I believe this is your second season. You interviewed a number of very interesting people, and it's wonderful. I love hearing these things. I'm sure you had some ideas on how this show would go, but now that you got several under your belt, what surprised you about the show? I mean, technology, people, how things are used, what caught your interest that you didn't know before?

Paul

There's two things that come to mind right away. The first is the guess. I think I've only had one person say no with a very valid reason.

Everyone else has been totally open to appearing on the show, especially before I even had an episode out. So that was a huge surprise. I thought it would be harder.

The second surprise, which is also great and probably shouldn't surprise me, is the community. The number of comments on tweets I've gotten on Twitter and a couple of emails with encouraging statements have just been wonderful to hear. And it really gives me encouragement to keep on going.

Anne Barela

Well, I think you're broadcasting about a topic that a lot of people really like. That's one thing about Python in general on CircuitPython in specific. is that it's built around a community and not necessarily just a technology.

It's available for people. So there's so many online resources. There's a community of people that one can reach out to.

It really is embracing what open source has wanted to do. And the simple fact that it is open source, there's no costs or licenses or anything involved. Most of it's MIT Open License.

So it really brings together a diverse group of people into a community that likes what they're doing and likes sharing it with people.

Paul

I couldn't agree more. One last question. You're starting a new project or prototype. Which microcontroller are you going to reach for?

Anne Barela

Well, if we had done this interview a year ago, I probably would have said the SAMD51. It's a great microcontroller from microchip has a lot of RAM and flash and peripherals. I mean, you can do just incredible things with it, you know, emulating a classic computer.

It's like snap pretty much as long as you got the software. But they've been very hard to get as of late. While not equivalent, if I were starting a project and I thought it could most likely do most of what I wanted, I'd probably pick a Raspberry Pi R.P.2040 pico-based board, the PICO itself from Raspberry Pi, or AidaFruits come out with a number of boards based on the RP2040 chip like Theather and Itsy Bitsy and the Qie Pie, a little tiny one.

It also has a good deal of RAM and Flash, and it just goes way fast. And that with the programmable PIO capabilities, it really has. has changed the market as far as price performance-wise.

So I'd likely give one of those a shot to see what I can do with it.

Paul

That's a popular pick. And thanks so much for being on the show.

Anne Barela

Thank you for having me. It's been great.

Paul

Thank you for listening to the CircuitPython Show. For show notes, transcripts, and to support the show, visit CircuitPython Show.com Until next episode, stay positive.
