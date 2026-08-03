---
date:
  created: 2022-11-28
title: "Episode 23 - Mark Komus"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep023.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode I'm joined by Mark Komus.

Mark is a geek, maker, computer architect, and general nerd. When he isn't using CircuitPython to build his own projects, Mark is a community member who contributes to both the CircuitPython core and its libraries. This episode is brought to you by PCB Way. With over a decade of experience, PCB W is one of the most experienced manufacturers in PCB prototyping and design.

Whether you're an engineer, students, or hobbyist, PCB way offers a simple and fast prototyping service, and it's cost effective at only $5 for 10 PCBs. And check out PCBW.com slash project where PCBway helps makers and hobbyists collaborate on their designs and projects. Make your design a reality and check out PCBWay.com for all your PCB needs, and they also now offer CNC machining and 3D printing services.

Visit PCBWay.com for more information. Thanks to PCB Way for their sponsorship. Mark, welcome to the show.

Mark Komus

Thanks for having me here.

Paul

How did you first get started with computers and electronics?

Mark Komus

So I think my path is like a lot of other people in this hobby is I started getting a Commodore 64 when I was a kid. I started learning to program in Cub Scouts actually. One of my neighbors down the street was also into computers at the time and taught us.

And it was just something immediately I loved doing as, I think, an eight-year-old. It was people thought it was strange, but just fascinating for me. And I progressed that way throughout elementary high school.

I always knew I wanted to go into computer science to pursue that as a career. I was never the kid that you asked, what are you going to do when you grow up? I knew what I was going to do when I grew up.

And that really got me down the path. it was interesting once I actually got a job out of university, I found that I wasn't doing programming on the site anymore. I wasn't doing my own projects. Now that I was doing it sort of nine to five, that part went away. I got into other interests at the time. Probably things I should have been exploring more when I was younger, but now as an adult I was doing more in terms of like recreational sports and just getting out in the world because by the time the day was over, I didn't want to sit down anymore.

Paul

How did that change for you? How did you discover CircuitPython?

Mark Komus

Eventually my job moved from more of a development job into a computer architecture job as I got more seniority. And I got sent on a conference. They had a workshop about the iot internet of things and they gave us all these intel edisons you can't find them anymore it was a little system on a chip it's the first time i'd seen something like that i started building a weather station one of my first projects and then eventually it got shelved put on a box like a lot of projects do and then it was years later i wanted to continue found out the edison was no longer supported and it's just like well i've heard about arduino and other projects like that so let's see what's out there And that's what led me down to discovering Adafruit.

And the first microcontroller I really bought was Feather M0 with Wi-Fi because I wanted to actually be able to check on the weather. That eventually led me to going on show and tell, the Ata Fruit Show and Tell, because I wanted other people to see what I was working on. I'd been watching the show for a while, and this was something I thought, hey, this would be neat to do.

I hope no one goes back and watches some of my first appearances on Show and Tell. They were fairly rough. But during that time, I was on the Adafruit Discord, met a lot of people, and it was Scott, of course, who's like, you have to try CircuitPython.

You'll love this. And I think when I really realized I was getting into it was when I was working on my Arduino code and started forgetting semicolons and C. And that was the moment when it's like, oh, this Python thing is pretty cool. CircuitPython's really neat.

I'd never used Python before. I'd had coworkers tell me how much they loved it, but I had never even looked at it until CircuitPython.

Paul

Never having used Python, what were your initial impressions of CircuitPython?

Mark Komus

It was quick and easy to do things. As Phil always says, it's too easy. People get mad.

They've made development and programming too easy. Where I've found it going forward in my life now is I can work on a project, be working on the circuit boards, the electronics, wiring, at 3D printing, and come to the end. And now the development side of things is that final mile.

And it's no longer hours and hours and hours of work. Like, I've finished projects in just a couple hours coding to hook it all together. Versus when I found myself in Arduino land, that could be a long time.

oh, is this library right? Is this compiling? Even just the turnaround cycle of compiling it, uploading it to the board, starting CircuitPython, you hit Control D and it's just back again.

When you're prototyping and developing is so valuable.

Paul

Speaking of show and tell, Halloween was last month and one of your projects went viral. Tell me about your monster eyes.

Mark Komus

So the monster eyes, the original code, full credit, was written by Philby from 8.5. He's done some amazing work. Highly recommend anyone that wants to check out his projects.

Some of the coding you will learn in there is just amazing. So I wanted to get it working on one of these new round displays that have been making their way around Twitter. They're the GC9A01.

I just forget the driver name. They're just little circular displays. And I thought they would be perfect for an eye.

I initially got them for a totally unrelated project. I wanted to do something with a heads-up display. That project is now also sitting in a box.

So this eye project, the first step, was to get it running on the circular display. That actually wasn't that difficult. The code was already written for the Ata Fruit Monster Mask, which is just an M4 baseboard.

And I had a feather M4 express sitting around that I was able to put it on. I posted the original little video just as, hey, this is something I'm working on this afternoon. And then as I continued to work on my project, my phone just like, I looked over and there was like 50 notifications.

I'm like, what's going on? And it just kept going all day, all night. I woke up the next morning to just hundreds.

I was trying my best to respond to people. People wanted to know how to build this themselves, how I'd built it. But then my goal was finding an M4 right now is very difficult.

The SAMD-51 is basically impossible to find. So I wanted to try getting it to work on RP 2040. That became what I thought would be a quick and easy project, became a much longer endeavor.

Because of the supported libraries, they had never been moved to the RP 2040. There was a lot of library support to get it to work. Eventually, a week later, I managed to go not quite as fast as them, But one thing people might not be aware of is the M4 has got a floating point unit in it versus the RP 2040 does not.

So the speed of calculations is always going to be a little bit slower when it comes to that. But yeah, eventually got it working, got the eyes placed in a pumpkin, literally just in time for Halloween and was very happy with the result.

Paul

Yeah, it looked fantastic. And it was, I love seeing all the likes on the Twitter post just keep going up and up and up and up.

Mark Komus

It was something that, yeah, you hear about, and it was unreal just to see something. And I know compared to some posts that get tens and hundreds of thousands. But for electronics, I'll take what it was.

Paul

Yeah, it was huge. It was great to see. And it inspired so many different projects, as you mentioned.

I think, you know, DJ Devon 3 built the project. Todbot had eyes going. So it was, you know, it was the zeitgeist of the moment.

Mark Komus

Yeah, I'm really happy about how it came out. and I'm really happy so many people said they want to take this and do their own projects, because that's really the goal.

Paul

You mentioned earlier coding in C, which is what the CircuitPython core is coded in. If you're in the CircuitPython community, you probably know of the core developers like Scott, Dan, or Jeff. You've been contributing to the core. How is being a volunteer working on the core different than maybe being one of the paid developers?

Mark Komus

It's different because I'm not beholden to anyone. I got interested in programming in the core because I still wanted to occasionally get my hands sort of dirty at that low layer programming level. I enjoy that type of development.

It's really nice to have CircuitPython to make your projects polished and quickly get them out, but it's fun to get your hands dirty at times. And I also wanted to contribute back to the community. That was part of my reason on it.

And I had embedded development C experience in my past. So I started, I was watching Scott's deep dive stream probably a couple years ago, and they had talked about wanting Ata Fruit Bus device in the core. It's a library that helps a lot of other libraries talk to I2C and SPI devices.

And putting them in the core, everyone hoped would speed up this rather than having it in Python. So that was my first contribution of substance to the core was something that I thought would be simple and ended up being this rabbit hole I went down. And then it just built up from there.

It was areas I was interested in or if I saw a community you need that might not be a priority for Adafruit, but was a priority for a lot of other people. When the RP2040 came out, the main libraries were all done for launch. But there was a lot count IO comes to mind, just a simple counter.

That wasn't a high priority, but still has a lot of functionality. And I'm like, okay, this is something I can get into. It led me to the first time of really looking into the data sheet for a microcontroller, 650 pages of fun technical specs if you ever can't sleep at night.

A lot of the core development I've done has just been areas that I wanted to see improved. The IS31 FL 3741 LED glasses came out as an ATA box about a year ago, and there is no display I.O. support.

Display I.O. for the graphics and for the text was something I really wanted on the display to put on the glasses. So I worked on adding that in, similar to the RGB Matrix.

Those glasses actually got me media coverage. I'm from Winnipeg. the Winnipeg Blue Bombers football team or one of my favorite teams.

We won the Canadian Championship last year, the Great Cup. I was at in Winnipeg Portage in Maine, one of the big gathering spots traditionally after sports teams or any big celebration. I was there wearing my LED glasses and I've never been in so many selfies in my life.

And people were asking, well, how, where did you get these? And it was like, well, I got the board and then I programmed it myself. I had cameramen coming up to me from the media saying, I need to interview you.

So it was an unreal experience on top of the team winning.

Paul

What other opportunities has working with the CircuitPython brought you?

Mark Komus

Since getting involved in the community, written in a couple of magazine articles, and seeing yourself published in print is something that's really exciting. And it just let me to meet a lot of people and get involved in a lot of projects and see what's out there. Like I've had companies reach out to me with samples or to ask questions, things that I never thought were possible before I got involved.

And I still have that imposter syndrome, which I know a lot of us have. You're like, am I really good enough for this? Are people really asking my opinion?

And it's trying to get over that and always thinking, yeah, yeah, I am. I'm not promising answers to the world, but if it comes to CircuitPython, hopefully I can help somebody.

Paul

Last question before we go, and you've listened to the show so you know what's coming. You're about to start a new project or prototype. Which microcontroller board do you reach for?

Mark Komus

I thought about this question quite a lot because I've listened to all the podcasts. I very much will vary which microcontroller I pick based on my project, but if I had to pick one, one of my favorite is unexpected makers, Feather S2. It was one of the first boards I had that had the Wi-Fi built in, Bluetooth built in, it had lots of I-O. It had everything you expect in a feather.

And for some reason, even though most of my projects don't incorporate Wi-Fi, I like having it there. With the new CircuitPython 8 and being able to edit over Wi-Fi, that's an even bigger reason. And Unexpected Maker, again, isn't a huge company, it's a person.

But all his boards that I've used have been amazing. They're well-made and has made working on any projects really easy. And they've been durable.

I've thrown them outside in a cardboard box for a year and it kept working.

Paul

Mark, thank you so much for being on the show.

Mark Komus

Well, thanks for having me. It was a pleasure to be here. And I look forward to listening to more podcasts.

Paul

Thank you to Mark for being on the show. You can follow Mark and his projects on Twitter @MarkKomus or on mastodon at Mark Komus at mastodon.comas at mastodon.com. Thank you for listening and thank you to PCBWay for sponsoring this episode. For show notes, transcripts, and to support the show, visit CircuitPythonshow.com.

Speaker 3

Until next time, stay positive.
