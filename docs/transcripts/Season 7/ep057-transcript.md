---
date:
  created: 2026-04-06
title: "Episode 57 - Physical Computing - Interactive Art, Robotics, & Tech for Good"
---

## Show Notes

[Show notes available here.](../../episodes/Season 7/ep057.md)

## Transcript

Paul

Welcome to the Circuit Python Show. I'm your host, Paul Cutler. This episode, I'm joined by Abby Bergman and Esha Patel. Abigail J. Bergman is a doctoral research assistant for the developmental technologies research group at Boston College. She completed her Bachelor of Arts in Psychology at Brandeis University and her Master of Arts in Learning Engineering at Boston College. Her interests include design-based research practices related to engaging young learners in science, technology, engineering, art, and mathematics. She is currently pursuing her doctorate, Informative Education, at Boston College. Esha Patel is a graduate student at Boston College in the Learning Design and Technology Program. She completed her Bachelor of Science in Elementary Education and I-Sem education at the College of New Jersey. Previously, Esha taught middle school science and engineering in New Jersey. Abby and Esha, welcome to the show.

Esha Patel

Thanks so much. Glad to be here.

Paul

You were both students of Professor John Gallaugher, whom I had back on the podcast. when I was just starting back in 2022. Abby, tell me a little bit about his physical computing, interactive art, robotics, and tech for good class, and your motivation for taking it.

Abby Bergman

Yeah, so his class is really unique in that it's a flipped classroom. So all of the lessons are done at home for homework. And in class, everything is a challenge or an in-class activity that really puts those skills that you did at home work. And so it's a really different classroom atmosphere. It's in the BC maker space. So it's not in a typical classroom setting, which makes it really special. And my motivation for taking it, so I'm a PhD student at the School of Education at Boston College, where I'm specifically interested in making and physical computing and what those opportunities to do physical computing can do for young children. So I'm part of a project right now and I knew a lot about making. I didn't know as much about physical computing. I did maybe one robotics activity. I don't think I touched anything about circuits or electricity since maybe high school physics. And so it was a great, really immersive, deep learning experience, which made me so happy that I had taken on class.

Paul

Esha, what interested you about the class?

Esha Patel

So I also, similar to Abby, don't have much computing experience. As a former engineering teacher, I did kind of dabble into Scratch Jr. and Scratch regular Scratch from my students, but not so much of actual. Python or anything like that. C++ never touched it. But I wanted to see what the course had to offer because it was an introductory course. The course had literally says that it's meant for people who are new to coding, which was me. And I love creating things I love making. And I did that with my students and my former classroom. So I took the course to see what it would be like. The flip classroom was new to me. I've never taught that way. I've never been in a classroom that way. So I was kind of scared with the concept. But I like the idea of being able to control. when I can watch each video and do each challenge on my own pace and just all in one three-hour class period or something like that.

Paul

So you both mentioned that you didn't have a lot of experience coding prior to taking the class. What kind of surprised you about the class and the coding part of it?

Abby Bergman

I think for me, my coding experience had been about statistical analysis. So it was really applied and it was very plug-in. Shug using the same lines of code, not really thinking about what the functions were, but understanding kind of more the math that's being done with different libraries. I think something that I really loved was like the hardware software integration to being able to pull in these different libraries that did things in the real world that I could see in touch made it make sense in a different way to me because if, how tangible it was. So I think I had a feeling that might happen just given the nature of the class, but it was still a totally different thing to experience it in person and really made coding more like a living physical thing to me, which was great.

Esha Patel

For me, I guess I got stuck on the concept that circuit Python at least, or any coding language is another language that I'm learning, but not in the traditional sense where you read, listen, write, and speak and all that kind of stuff. So I really honed in on that and that kind of made it harder for me. And then once we started doing design challenges, I stepped back and I realized, okay, I should take this step by step. And Professor Gallaugher wants us to create projects and code for those projects in things that we are comfortable in. So instead of me trying to learn a brand new language all at once, I focused on just seeing what my interests were. And a lot of that was sensing technology.

Paul

Can you give me an example of some of that technology?

Esha Patel

Yeah, so we did, my partner, Jennifer, she's a international exchange student from Germany. She went back to Frankfurt now. We made this interactive hopscotch that kind of similar to a distance sensor, but not really, uses a sensing kind of technology to see when a object or in this case, feet, are sensed a specific range. And we tried to use various different sensors to see what would work for us. We used an IR break beam sensor to like kind of break the sensor. And that was the technology that we used.

Paul

Tell me a little bit more about the project. How long did it take to build or what were some of the challenges that you had to overcome and building it?

Esha Patel

Yeah, of course. We started about mid-October and we finished about mid-end of November-ish. It was definitely a prototype. There's more space to grow. We created seven individual squares. So imagine a hopscotch, but you're able to take those squares apart. And we used regular black yoga mats and we cut them into like a square shape and put dowel rods in between to hold the mats in place. At the corners of each of those squares, two corners, we put the IR break beam sensors at a diagonal. It was better than side by side that the diagonal worked best. And we glued neopixel strips to the inside of the dowels. So it would kind of look like a concave effect almost. And we used a Raspberry Pi Pico to create a very simple sensing code using the ATA-free animation rainbow chase. So when the break beam was broken, they'd won the IR break beam was broken, it would fill the neopixel strips with the rainbow chase animation. And the second it was unbroken and the object or foot, whatever was being used to break the beam was gone, the strips will flow black or just look to turn off. essentially. And the idea came from just like being in the park one day, seen some kids playing hopscotch. And I'm like, huh, I wonder if we can make this similar to like that dance dance revolution kind of tile thing. And Jenny and I got to working and we came up with the idea. I have an instructable page about that too, that if you would like to use to share with people.

Paul

Oh, that's great. Yeah, I'll definitely link to that in the show notes. Abby, did you have a favorite project or design challenge that you worked on?

Abby Bergman

Yeah. As Esha was talking, I was thinking about my, tech for good project. So the final project that we do, at the time I took the class, it was our final project. Actually, that's not right. So, you know, it was our second to last project. But for the tech tools for good project, we all had to create different prototypes for the campus school at Boston College in the campus school on our campus. And it's specifically for students. of a pretty wide range of ages with complex disabilities, many of whom have different visual impairments as well, in addition to other health challenges. And part of our design challenge was to make something that either brought their learning to life, made their lives easier, made teaching easier. And as an education student, this made me so excited. I wanted to make something for younger learners. I wanted to make something soft. I'm a big crocheter, fiber arts person, and I made a very hungry caterpillar. I crocheted the whole body. I put in all the hardware elements. I use Pico. I think I used a PICO W for it, but I could have just used a regular PICO and added a RFID sensor into the head. And on the outside, there were also these is that a fruit that you could feed the very hungry caterpillar. So in the book by Eric Carl, the hungry caterpillar has like one apple, two pears, however many oranges, cherries, et cetera. And I also sewed in Christmas lights into it as well that I programmed. So I had these acrylic pieces with stickers of the fruit and RFID stickers on the back as well. So when you fed the caterpillar, you could hear it, a voice, say one apple, one red light would show up. Then on and on. So when you fed it the last fruit, all of the lights showed up and you could hear the whole story, which was really fun to make. Definitely challenging of putting the, like sewing it together, crocheting it. I had a lot of solder an issue. So it was mostly durability. But it was really fun to figure out the RFID.

Paul

Did you get the opportunity to see it in action with one of the students?

Abby Bergman

Not yet. And so part of the reason for that is so many failed soldering. That would fail inside of it. So I've had to resolder it, reattach it multiple times.

Paul

I think everyone who's made a project has gone through that.

Esha Patel

Yes. I have to agree. For the hopscotch, we had to solder pins-to-pin wires to go around from the breadboard to the breakbeam sensors on the other side. that, you know, people would think, oh, coding is difficult or measuring all this note. Sottering was the most difficult thing because it really requires the right nozzle, the right hand movement, and sometimes patience. And when you're grad students, you're losing patience at times.

Abby Bergman

Yeah. And when you're you're soldering something that goes into like an object that's supposed to be held and played with, then you have a lot of, you need it to be flexible and you need it to be sturdy. And that's where I had the failure points.

Esha Patel

Speaking of like the differences in the two projects, that's a beauty of Professor Gallaugher's class. You have the opportunity to create something for others as the campus school. And like my partner and I, we created a Tick-Tac toe board. You have something to create opportunity to create something creative. And for us, it was called the Festival of Lights. So there's like, and it really meshes, you know, personality, service, all kinds of things together.

Paul

Tell me a little bit about the Festival of Lights.

Esha Patel

So that was a new concept for our semester. I took the class in fall 2025. He kind of took the art project that he used to do and kind of combined it to create this festival of lights where in this prototyping face he basically said, we want to showcase Boston College that we are able to create these amazing light lit up structures. And there's no strict rule of how it was supposed to be. So our festival of light project was the hopscotch. Somebody else created a like with a stoplight that goes like red light green light kind of way. Another person created a jukebox. Somebody else created a Minecraft, like a Minecraft brick. Professor Gallaugher thought somebody would even, like, put lights around some of, like, the buildings and things like that. So there was huge scales and super small scale projects. But it was something new, and I hope he continues it for the spring semester. It was fun.

Paul

What advice would you have for someone thinking about taking the course?

Abby Bergman

Something that comes to mind immediately is the match between imagination and technical skill was often. and frustrating for me. And not so much the circuitry skills. That was very, I felt very well prepared there. I felt like circuit Python, especially. There was such a wide range of tools and resources available to make a software element come to life. I would say the harder part is the fabrication piece of, you know, needing to, if you have CAD skills or not, if you. you have access in time for the three new printers. I think everything, which we do at Boston College, everything fails like three times before it works. And when you're working on a semester timeline, you just have to move on. So I pivoted a lot in the class. So I would say having flexibility and being able to thinking big at the start and then carrying over your skills versus idea match is a big learning point that I would say.

Esha Patel

I would agree with Abby about the flexibility for sure. I would say if you feel intimidated by trying something brand new such as coding, you have to take baby steps with it. And that's the beauty of the flip classroom. Like you're able to pace yourself as you go through each video lesson, each design challenge. You're able to go at whatever pace some weeks. might be faster. Some weeks, but it might be slower depending on how comfortable you are with whatever topic is being covered out that week. And most importantly, just have some patience, because when it comes to making, a lot of the times you want to quickly get a prototype in or quickly finish this line of code. But some designs are just not made overnight. It takes a while to finally, like, develop a proper prototype of software and hardware.

Paul

Patience is great advice. Abby and Esha, thanks so much for coming on the show.

Esha Patel

Thanks for having it. Thank you.

Paul

Thank you for listening to the Circuit Python Show. For show notes, transcripts, and links to Professor Gallaugher's course and YouTube channel, visit www.circuitpythonshow.com Until next time, stay positive.
