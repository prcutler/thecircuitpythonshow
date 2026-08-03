---
date:
  created: 2022-08-08
title: "Episode 15 - Joshua Lowe"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep015.md)

## Transcript

Paul

Welcome to the CircuitPython show. I'm your host, Paul Cutler. This episode, I'm joined by Joshua Lowe. Joshua is a Python entrepreneur who invented Edgeblocks to help bridge the gap from scratch to Edgeblocks and then into Python 3. Joshua started learning Python in 2013 and wanted to find a way to make it easier for others to understand.

Josh, welcome to the show. Hi, thanks having me. Tell me about Edublocks. So Edublocks was a project that I started about six years ago now.

Joshua Lowe

it all surrounded this idea of, you know, I've always been interested in like computers and technology from a very young age. You know, being the age I am 18, I've always been surrounded by, you know, technology. And we were talking a few days ago about you not having an internet for a few days.

I can't imagine life without the internet or, you know, technology just because I've always been surrounded by it. I've always been interested in technology. And it was around the time the Raspberry Pi came out.

which was 2012 now, 10 years ago, which seems like a crazy, crazy thing to me. Yeah, when the Raspberry Pi came out, it kind of stand this interest into the coding and programming side of technology. You know, I'd always been curious about messing around with laptops and stuff, but I never really had any exposure to being able to code, being able to program, messing about with hardware, that kind of stuff.

And yeah, so in 2012, the Raspberry Pi came out, and about a year later, I joined a Raspberry Jam event. So Raspberry Jams are all across the world now. I'm sure most people know what they are.

But they're like coding meetups for people interested in the Raspberry Pi or other related things like CircuitPython, Micbit, those kind of things. And yeah, I went along to this event and, you know, I was really interested in, you know, the coding side of things. And I started learning off Scratch.

So learning Scratch, the Dragon Drop program language. And, yeah, building lots of different. projects with Scratch and, you know, that's something that I really enjoyed for a few years and all the different things you can do with it, you know, even programming stuff with the Raspberry Pi and like GPIO, that kind of stuff. But then after I'd learned Scratch for a few years and, you know, done lots of projects with that, I kind of realized that, you know, if I wanted to do this as a career, which was kind of set on at that point of, you know, this is something that I'd like to do in the future that I'd have to learn a text-based program language. And kind of like the main one that you go to scratch, or at least in the UK anyway. I'm not sure how it is in other countries, especially in schools, you go from scratch, and then you go to Python. So yeah, I was kind of making this transition from, you know, I've done scratch for a few years. I was kind of used to how all the visual stuff worked, and now I have to make this jump to Python and, you know, the text-based program side of things. And like a lot of people who have picked up Python from nothing or, you know, made the transition from block-based, text-based, using Python.

It was kind of a big jump between the two because suddenly you're having this environment of a drag-and-drop block-based environment where it's very visual, it helps you along the way. You can't really get any errors of that kind of stuff. To Python where if you make the littlest mistake of, you know, a missing capital letter, punctuation, indentation, that kind of stuff, you know, you can get a red wall of text that, you know, to a beginner, means absolutely nothing.

So I kind of wanted to create something that would bridge the gap between the two of, oh, well, you know, bring this block-based environment back, but also, you know, have a text element to it of, oh, well, why don't we put the text on the blocks that you drag and drop in lines of code? So as you've got started as a platform where you could build stuff with the Raspberry Pi. So one of the early examples was Minecraft Pi, so you could interact with Minecraft on the Raspberry Pi and build projects with that.

Paul

Oh, neat.

Joshua Lowe

Yeah, so that was a very example. really kind of popular thing to key it off and later down the line there was projects with GPIO pins and electronics so that was kind of like the early start of Edgebox and then from there it extended to the mic bit, then CircuitPython and then Python the web so that's kind of like how it started.

Paul

Wow, that's a heck of a story. What inspired you to make EduBlock's open source from the beginning?

Joshua Lowe

It was through going to events like the Raspberry Jams and later Pycons and conferences like that. You know, I got to meet a lot of people in the open source community and kind of learn how GitHub works and the benefits that making a project open source can bring. A lot of the success of Edgebox is kind of down to making it open source. I didn't really fully understand the impact of it at the time because, you know, I'd seen like these big projects from like Microsoft and companies like that who would open source things like, not at the time, but make code as an example of an open source project.

You know, I've seen that they got a lot of contributions from community members to make the project better. I never really thought that would happen to Wedgivox or, you know, making it open source, you know, would bring that kind of impact. But there was a big community around it that would submit issues, submit pull requests, and, you know, really dedicated to a project because, you know, they saw an idea and they, you know, they believed in it and they wanted to, you know, help out.

So, yeah, it's been really helpful to make it open source and, you know, kind of that community aspect of it is, you know, really important to the project and a lot of the work that I do. And, you know, being able to give back to the community and, you know, kind of have that community spirit around it. So that was kind of the main reason.

Paul

That's awesome to hear. So tell me a little bit more about EduBlocks. EduBlocks has different modes and some of those modes can work with hardware. How does that work?

Joshua Lowe

Edublocks started off as a tool for the Raspberry Pi. You could do basic stuff like the GPI opens, some projects with using them, and also Minecraft Pi. I say we're kind of the two things at the start.

And then it's solely extended into doing more basic things with Python. So, you know, print hello world, that kind of stuff. And then later Python Turtle.

Yeah, that was kind of like the first mode, if you will. And then from there, the kind of whole EduBlock's tool, gained in popularity and people wanted more things like port for the mic bit was next so being able to build projects with the mic bit scrolling stuff on the display same thing with the rosby pie being able to plug stuff into the pins on the mic bit to build like physical competing projects and then the next one after that was actually CircuitPython and that came about so meeting scott and catney and dan from the CircuitPython team at pycon in 2018 i think it was hopefully i got that right so yeah Pycon 2018, I kind of met them. And I'd heard of CircuitPython before.

I never really had an exposure to it. So I hadn't really played around with the circuit playground and the other circuit Python boards. And, you know, after playing around with them at Python, I was like, yeah, I think this is the next kind of mode that I want to go for.

So, you know, I introduced very similar things, being able to build physical compute projects, interact with the speaker and the Neopixels on the circuit playground. So the modes are kind of like different sections of hardware that you can use. And then also alongside that, there's like a Python mode, which is, you know, there's basic Python, which you can run in the browser.

And more recently, which isn't Python, HTML, so you can build websites and stuff like that. But it is mainly dedicated to Python because of the range of hardware that supports it. And also Python just being, you know, the main text-based program language that's used in schools here in the UK. And it is mainly a program for schools, but there are lots of home users that use as well, enthusiasts who just want to learn how to code on their own. So it's a really wide range of users, and that's kind of like how the modes integrate with it.

Paul

Out of all of those users over the years, have you seen one or two projects that really stand out in your mind, things that people have done with edu blocks that maybe you didn't expect? I think probably

Joshua Lowe

instead of projects, I would probably say that the stand-up thing for me is, you know, being able to see people who were kind of put off by that transition from scratch to Python and then going back and using Edgebox and being able to, you know, pick up, you know, text-based programming language. I think that's kind of like the stand-out thing for me, if I can think of one thing in particular, because, you know, I've always wanted to be able to pass on my knowledge and love for coding and computer science, all those kind of things to other people, but especially the problem that I was seeing in UK schools at least was people were being put off by the idea of coding and programming because they saw this horrible red line of text when they were learning text-based programming and they had all this visual element of it taken away from scratch when they were learning Python. So being able to provide something that helps people to kind of follow a similar path to me and be able to share the love that I have for it, I think that's really kind of really kind of like the lesson legacy of it that I see and, you know, the kind of a big standout thing, you know, that I can think of.

Paul

Where do you see Edublocks going next?

Joshua Lowe

It's a difficult question because it changes, it changes all the time. It kind of like what I want to do next with it. Yeah, I think obviously, you know, expanding the feature set. So one of the big things that I'm working on at the minute is tutorials and examples. So, you know, I really want anyone to be able to load up Edgeblocks and, you know, kind of had this guided tutorial experience where, you know, they can learn themselves and have, like, a self-guided learning experience. So that's kind of the main thing that I'm working on, lots of content and lessons and that kind of thing. So, yeah, expanding the tutorial set and also, you know, I've got some different mode ideas that I want to kind of work on. And, you know, last year I introduced the ability to have extensions in the mic fit mode. So being able to type in a GitHub URL are very similar to how make code works and extend the capabilities of the microchip mode to support different microbit libraries.

Alongside the tutorials, the other thing that I want to do in the next release that I do is expand the extension capability to the CircuitPython mode and the Python mode. So you're able to use third-party libraries with those modes, which will be pretty exciting to see what that opens up.

Paul

We've been talking a lot about education. you graduated high school in 2020 just as the pandemic was starting to hit. What role do you think remote learning can play in education going forward?

Joshua Lowe

I think the pandemic has kind of brought forward the use of lots of technology in the classroom, you know, forward. And I think we're always going to see the shift to, you know, using tools like Google classroom, Microsoft Teams and things like that, to be able to provide education to a wider range of people. But yeah, through the pandemic, you know, all of a sudden people were forced to, you know, kind of learn from home and, you know, use all these new tools.

And I think, you know, the use of things like Google Classroom probably has, you know, kind of died off a bit as people moved back to the classroom. But I think things like that are always going to have a place now, you know, where other subjects, you know, when I was in my last year of high school, you know, we used Google classroom for all of our classwork, all of our homework. and, you know, it was just a normal thing in that subject, but, you know, I think things are going to move across all the subjects where we kind of embrace technology and, you know, technologies used across school.

And I think also the pandemic's highlighted the need for wider access to internet. You know, we just take for granted that everyone has an internet connection, but, you know, the pandemic's kind of made us realize that, you know, technology is not accessible to everyone. and the things that we enjoy, you know, not everyone can access.

So I think over the next few years, we're probably going to see a push to, you know, make internet, which at this point is, you know, kind of something that's fundamental to, you know, modern day life, but we just take it for granted. So I think we are going to see a big push, you know, for making the internet more accessible for everyone and also bringing more opportunities to people who might not have had them before. And, you know, it's things that were really interested in, like filling things with CircuitPython devices or learning how to code. You know, these things are going to be really big over the next few years, I think, you know, where more jobs are involving technology. And, you know, there's a greater need for people in software engineering and computing in general. And I think there was a statistic that I learned at an event that I went to the other year where 60% of jobs, that all exist in, I think, 10 years it was, or the age group that were there, 60% of jobs that this age group are going to, you know, go for in the future, you know, don't exist yet because they're all related to future technologies and augmented reality, artificial intelligence, that kind of stuff. I think there is a real need to kind of push this whole switch to virtual learning and being able to make sure coding is accessible for everyone. I think the pandemic's highlighted that, you know, everyone needs equal opportunities to be able to access these things.

Paul

I absolutely agree. Well, we're almost out of time, but before we go, I have one last question I like to ask all of my guests. You're about to start a new project. Which microcontroller do you reach for?

Joshua Lowe

This is probably quite an easy one for me. So it has to be the Microbit, specifically the Microbit v2 that came out over a year ago. No, actually, which is pretty hard to believe.

And the thing I really like about the Microbit is, you know, it's a really cheap. device, £13 in the UK, if I've got that right. But it's got lots of capabilities as well.

So you've got Bluetooth, you've got a display where you can scroll messages. So that's a really fun, beginner project. But you've also got the pins at the bottom where you can plug into lots of different add-on boards to be able to extend the capabilities. And yeah, I think the Microbit and the features that the V2 brought, like the better processor, the onboard speaker, the touch logo which is pretty cool.

I think it's a really good beginner's board, but also it provides, you know, the capability to be extended and to do lots of different advanced projects as well. So there's no kind of like limit with it. I think that's what I really like about the mic bit.

I think whilst the Microbit's a really good general board, and there's so many like other boards that I really like, like the Circuit Playground Express is one that I've really liked to use before, and some of the smaller trinket boards. Whilst the microbit's kind of like my favorite, favorite all around board. There's lots of others that I really enjoy using as well.

Paul

That's a great pick. If people want to learn more about Edublocks or you, where should they go?

Joshua Lowe

The best place is Edublocks.org. You can find all the social links on there and also the guides and resources to get started and places to contact me if you've got any questions or you've got any queries or need any help with the project if you want to start using it. So that's probably the best place to go.

Paul

Josh, thanks so much for being on the show.

Joshua Lowe

Thanks having me.

Paul

Thank you for listening to the CircuitPython Show. For show notes, transcripts, and to support the show, visit CircuitPython show.com. Until next episode, stay positive.
