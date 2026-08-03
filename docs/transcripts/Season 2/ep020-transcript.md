---
date:
  created: 2022-10-17
title: "Episode 20 - Jim Mussared"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep020.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Jim Mussared.

Jim is a maintainer on the MicroPython Project and works for George Robotics. He's a father of two, part-time student, and lives in Sydney, Australia. This episode is brought to you by PCB Way.

With over a decade of experience, PCB Way is one of the most experienced manufacturers and PCB prototypes. and design. Whether you're an engineer, students, or hobbyist, PCB Way offers a simple and fast prototyping service, and it's cost-effective at only $5 for 10 PCBs. And check out PCB.com slash project where PCB Way helps makers and hobbyists collaborate on their designs and projects.

Make your design a reality and check out PCBway.com for all your PCB needs. And they also now offer CNC machining and 3D printing services. Visit PCBway.com for more information. Thanks to PCB Way for their sponsorship.

Jim, welcome to the show.

Jim Mussared

Thanks, Paul. It's really exciting to be here.

Paul

I'm glad you're here. How did you first get started with computers and electronics?

Jim Mussared

So I was always interested in that side of things. One of the first memories I have of being really excited about electronics is as a member of a country that also says, Python, like Nicholas Tolliver in the earlier episode, I was given access to a BBC micro as a very small child. And there was an amazing system that you couldn't interact with Lego motors and sensors through it. And it's pretty much, I was very grateful for one of my teachers who took a special interest in that and gave me a lot of time to play with that. And so one thing led to another, I studied electrical engineering at university, but went off into software, did process control and software operations. And then much later, through a couple of different avenues, I sort of reunited my with electronics. One in particular was I got quite into sailing, like racing. And if you want to race at a moderately high level, you either need to be an excellent sailor, which I, am not or you need to have some sort of unique skill to add to a boat.

And it turns out there's an awful lot of electronics in high performance sailing. You know, we sail by numbers is kind of the joke. And being able to quickly repair and configure and get the most out of the electronics for the boat is quite useful.

And through that, got really into repair and reverse engineering and a huge rabbit hole in YouTube of the amazing resources that are available to really get excited about electronics on YouTube. You know, you talk to your friends who, you know, what did you do last night? You know, watch this on TV or whatever.

I watched a three-hour episode of some Scottish guy named Ian repairing an eight-digit multimeter. It was amazing. And then through that, I've always been interested in education as well.

And I got this incredible opportunity to teach at a summer school in Australia for high school kids for several years. And we taught electronics and circuit design. And through that, got involved in a company that specifically taught Python to school kids.

And with that, got very involved in the BBC Microwbit. And through that, I met Damien at PyCon, Pycom, A.U., which is a wonderful spin-ononon of the Python Conference for Australia.

Paul

And Damien George is the founder of MicroPython. How did he first start that project?

Jim Mussared

So in 2013, there was a Kickstarter for the original pieboard. And it was a combination of this electronics component and the software component to run on it. My understanding, I wasn't involved at all, and I didn't participate in the original Kickstarter.

But my understanding is that this kind of started as almost like a dare. I bet you can't make Python run on a STM 32-4. And now that I've gotten to know Damien really well, this story totally fits.

And the Kickstarter was actually quite successful, and they followed it up with another one to add MicroPython to the ESP 802C6. And I always joke to Damien, every time we have a crazy idea for a hardware project, oh, we should do another one. Another Kickstarter is never again.

Paul

Two was enough.

Jim Mussared

Yeah, absolutely.

Paul

So it's been almost 10 years since MicroPython in the first Kickstarter, and it's been about five years since CircuitPython actually forked MicroPython. What are some of the differences between the projects.

Jim Mussared

So much of this happened before I was involved really actively in the project. I was actually off on the side doing the GROC learning microbit. So I think it's really interesting to consider the idea of Python on microcontrollers as this incredible, I would say, configuration space of different options for how you want to proceed with the project and what you want available to you and how to do it.

And I think it's really actually wonderful that we have two very different solutions that cover a much widest arrangement of configurations interests and in particular that the two projects share the core i'm really really excited that in the last of a year or so circupithin have done a huge amount of work to get the core in sync effectively and MicroPython is able to specialize on things that make sense to MicroPython and circopithin is able to specialize on use cases that makes sense to circopithin and there are lots of things that are in circopithin that i look at and say oh yeah that that totally makes sense we're not going to do it that way because we have to support this other use case that's not compatible I don't know, interrupts is probably a good example there. And Cycopython, as others have mentioned before, very much built a workflow around copying files to the device through mass storage. We work really closely with Ada Fruit.

I talk to Scott pretty often and more recently with Jeff and Dan as well. We're hugely grateful to Ada Fruit for sponsoring the MicroPython Project and doing a lot of behind-the-scenes stuff that just really help the brand and the project in general. Lady Ada and Phil have been tremendously supportive.

Paul

What are some of the areas that you've had the opportunity to collaborate with Adafruit?

Jim Mussared

It's very difficult to design a system that works one way for one person and one way for another person. And Circopithin provides a whole different range of use cases that we would never think of and we don't see. And so we get quite a lot of really useful feedback from the Zerker Python team that influence how we design features.

We often talk to them before starting a piece of work and we get bug reports. and pull requests that we try and merge straight away up into upstream. We had a great example recently where Jeff had an idea for reducing the firmware size, and we took that into MicroPython.

That was really, really useful.

Paul

What do you see of some of the strengths of MicroPython specifically?

Jim Mussared

I think one of the strengths of MicroPython is that it is much more building blocks and configurable to a particularly use case, and this comes up a lot more in our professional uses of MicroPython and where we're doing very custom implementations of the core VM for a particular customer or the very specific board configurations. A lot of these customers really want to use very low-level features of peripherals and things like that. And so we need to expose much lower-level details in the APIs, and they need interrupts and low latency.

Paul

Along with Damien, you're one of the maintainers of MicroPython. What's it like to be a maintainer, especially of such a large project?

Jim Mussared

So I was quite new to open source when I got involved in the MicroPython project as somebody used a awful lot of open source software, but actually contributing and working on open source is new. It's a tough job. You are pulled in hundreds of different directions from everybody's little use case, and it's very hard to figure out what's important and what's worth prioritising.

Because ideally you'd like to do everything, and especially someone like me, I'm easily distracted by, well, yeah, we totally should fix that right now, and maybe that's not the highest priority. The other thing that's hard is that we have so much state in our heads as maintenance in terms of where we would like to go, but it's not really quite fully crystallized and coming out with a good way to get the most out of the community, to have them contribute in the most efficient way possible. It requires quite a lot of time documenting and explaining, and that could be really hard when you haven't quite figured out the direction you want to go in anyway.

But on the other hand, it is a really exciting job. Seeing all of these people come together from a wide range of, different use cases. We've got people running MicroPython on Windows in scientific systems, to people using really, really tiny micros, to people using the Unix port on quite big systems, and MicroPython in space and MicroPython and toys. And it's an exciting thing to see all this come together in a system that works. And overall, maintains really high test coverage and code quality and efficiency and code size. It's really fun. Git has completely transformed the way we do software development.

And if I could go back 10 years and only highlight a couple of things that are different in the industry 10 years from them, that would definitely be one of them. We also, as a maintainer of the open source project, we have some challenges involved in how we also mix our time with the professional work. So Damien and to lesser extent, me do consulting work with MicroPython for professional clients.

And so finding a good balance between the features that they want and the features that the open source project want. And ideally, funneling as much of that back into the open source project. as well.

Paul

For you and Damien, how do you find time to balance both your professional work and the open source needs of the community?

Jim Mussared

It really helps in terms of Damien and I communicating that we are good friends. We have kids about the same age. Unfortunately, Damien lives in Melbourne. I live in Sydney, but we find it very easy to talk and plan and have fun in that process of running the project. I'm a part-time student. I have much less time to put into this than Damien does. And Damien works really, really, really hard. And I think that's the answer.

to your question is that Damien just works really, really hard. Often the best results come when we can align the professional work with the open source work. And what the ideal there is where we have our professional customers actually contributing full requests and raising issues and basically contributing to the project as if they were open source users.

And we do have that quite often and it's fantastic.

Paul

You mentioned some of the interesting use cases for MicroPython. What are some of the favorite ones that you've come across in your years of working with MicroPython?

Jim Mussared

At the opening, I said that I got excited about. electronics through the BBC Micro and Lego. And every day, it's just amazes me that Lego now use MicroPython in their Mindstorms products.

And the follow the successor to the BBC Micro, the Micro Bit, also runs MicroPython. And that makes me very happy. There's a whole range of different things.

We do some really cool work in Australia for a company that does medical devices that use MicroPython. They use MicroPython as their primary platform for development of these embedded devices. and it's amazing working with them because they really push what we can do with MicroPython.

There's a great talk you can look up from Damien from PyconAU from a few years ago about his work with the European Space Agency for space qualifying micropritom, so the mission hasn't flown yet, but that work is still relevant and exciting. I've seen MicroPython used in bench equipment, and there's a recent example I saw just chatting to him the other day, Robin who makes the pixel pump as a crowd supply project. There's a company in Germany that have used MicroPython for car counting machines on the auto barn.

I was at university the other day and somebody showed me their calculator and said, oh, my calculator runs Python, for real? And it ran MicroPython, as it turned out. So we even get surprised by some of the places that run MicroPython.

Paul

MicroPython 1.19 was just released this past June and saw significant performance increases with the way MPY files were reworked. When you're dealing with MicroPython and Microcontrollers, performance. is always at a premium. Can you tell me about some of that work that you did?

Jim Mussared

It seems really strange to me coming from a previous job where I literally worked in exabytes and we would joke, you know, what's that number you just said? Zero petabytes and to come down to this world where bytes matter, you know, individual bites. We go to great lengths and commit extreme crimes against the Seag compiler to save 10 bytes here and 20 bytes there. But it adds up. And something like, I just looked this up before the call was F strings, the entire feature is 500 bytes.

And so if we can rearrange some structure or figure out a way to rework a few functions and change the inlining, we can offset that. And our goal is to keep the base core of MicroPython almost constant and continually to add new features. It's extremely difficult because different architectures and different configurations will, maybe the same optimization makes one smaller and the other bigger.

it's actually really fun. Some people like to make ships in a bottle, and we like making our code as small as possible, ideally without making it also really ugly and difficult to work on. Kind of related, sometimes increasing performance will also decrease code size, but often they go against each other.

So we're always sitting there with the performance test running. I have an automated thing that runs on every pool request that tells us the performance distance across a bunch of different boards, And when we can find the changes that do both, it's fantastic. I think it was actually not 119, but 118.

We put in a feature that actually has quite an interesting history, that's something that MicroPython implemented originally, which is to cache in the bytecode when you look up something in a map, which happens all the time every time you access an attribute on an object. And you cache in the bytecode where that attribute was found, so that the next time it's faster. And then Python itself added that in C Python.

And unfortunately for us, we never got much value out of this feature because most of the time our bytecode is in ROM, and so we can't modify the bytecode. So we found a way to implement that casing in a kind of a look-aside buffer and realize the same benefit in Micro Python. And that was really exciting.

It was 20% performance boost on some boards and even higher on others. You mentioned the MPY rework. One of the things here is we're constantly looking for ways to move data out of RAM and into ROM.

Chips typically have a lot more ROM than they have RAM. I'm using ROM here, but confusing I mean flash. And what this will let us do, and I hope CircuitPython maybe we'll see some benefit from this too, is have a way to dynamically update code on the board, so Python code on the board, but not have to have that code run from RAM, have it run from Flash instead, freeing up significant amounts of RAM for the programs to run.

And, you know, we might only be talking small amounts of RAM in an absolute sense, but if you've got a program that's constantly hitting the RAM limit, adding an extra kilobite makes all the difference. So it's a pretty exciting feature. And hopefully in the next couple of releases, we'll start to see that all come together.

Paul

Where else do you see MicroPython going next?

Jim Mussared

We have a lot to learn from Circopython, I think. And that's one of the things that I really want to focus on for MicroPython, community documentation, making it really easy to get started with MicroPython. One of the things that are time back to what I said earlier is that people come to us and they want to figure out how to configure MicroPython in crazy ways that are really unique to their situation.

And I want to make that really easy. There are a never-ending series of Python features that we need to consider implementing in the core, and also a never-ending series of chips and architectures that we need to add support for. Another area I'm particularly excited about is ASync IO.

So for the last few releases, we've been adding more and more support for asyncio. And having now written a few pieces of MicroPython software that use asyncio, it is transformative. Originally, Circopython didn't have interrupts because they are hard to use.

And MicroPython has interrupts and they are hard to use and lead to lots of problems. And I feel like asyncio gives you that balance of being able to write asynchronous code that is still maintainable and understandable and efficient.

So we would like to see asyncio pushed further and further into the core. I want to be able to await on a pin changing state or await on a DMA transfer and use that everywhere. One of my favorite examples of this is using asyncio with Bluetooth, which was extremely difficult to do when you have a complicated protocol that involves callbacks backwards and forwards, and now it's all just straight, line, linear, await sequences.

Paul

Yeah, there's definitely a lot of excitement around asyncio I think, in both communities.

Jim Mussared

It's difficult that there's a lot of different ways to do the idea that is asyncio, there's Trio, and so forth. I think pragmatically, we need to just focus on choosing one, and our use cases are simpler than what people are doing in C-Python. And I would like to see asyncio. Work really well and cover as many use cases as possible.

Paul

Well, we're almost out of time. But before we go, I have one last question I'd like to ask each guest. You're about to start a new project or build a prototype. Which microcontroller do you reach for?

Jim Mussared

So I've enjoyed this question on previous episodes. And I always laugh because in our work, we don't choose the microcontroller. We come in with somebody else has already chosen it.

And the idea of choosing is a luxury. Look, as an employee of George Robotics, purveyors of fine MicroPython products, the PyBoard is my obvious answer. It is a wonderful board.

I've used it in many of my own projects. I really like the way it's designed and the way the pins are laid out. But, of course, I have to say that.

I have a huge fondness for the Microbot and have enjoyed already using the Microbit with my son. I got a remote control car for him recently, and the controller was too big to fit in his hand. And one of the amazing features of the Microbit is this packet radio.

which is the Bluetooth Fi, but without Bluetooth Low energy implemented on top of it. And you can just use it to send arbitrary messages with no stack and no knowing how to do anything. And we built a remote controller for his car that he could use the accelerometer to turn and steer.

And I love using the Microbit for that reason. But on a personal note, if I were just to do another project, I would want to do something with an FPGA. Because I always love chips that have crazy peripherals.

And so I think my next project will have an ice spot unit. running microphone.

Paul

Great pick. Jim, thanks so much for being on the show.

Jim Mussared

Thank you, Paul. It was a heap's fun.

Paul

To learn more about MicroPython, visit MicroPython.org. Consider supporting them financially via GitHub sponsors. Thank you to PCB Way for sponsoring this episode of The CircuitPython Show.

Make your designs a reality with 10 PCBs starting at only $5. Thank you for listening. For show notes and transcripts, visit CircuitPythonShow.com.

Until next episode, stay positive.
