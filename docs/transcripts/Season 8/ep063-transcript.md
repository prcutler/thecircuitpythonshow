---
date:
  created: 2026-07-27
title: "Episode 61 - Michael Czeiszperger"
---

## Show Notes

[Show notes available here.](../../episodes/Season 8/ep063.md)

## Transcript

Paul

Welcome to The CircuitPython show. I'm your host, Paul Cutler. This episode, I welcome back Scott Shawcroft for the second time.

Scott is the project lead for CircuitPython, and his work on CircuitPython has been sponsored since 2016. Prior to that, Scott spent six years working at Google and holds a degree in computer engineering from the University of Washington. Scott, welcome back to the show.

Scott Shawcroft

Thanks for having me.

Paul

One of the things you've been working on is Zephyr, which is an open source real-time operating system.

Scott Shawcroft

That's right.

Paul

And you've been working to get CircuitPython running on top of it. For someone who hasn't heard of Zephyr, what is it and how is that progress going?

Scott Shawcroft

Yeah, so back in the old days, 10 years ago when I started doing this, what would happen is that each individual vendor would have this software development kit that you would have to do. So Atmel had their Atmel software framework. Nordic still has their own Nordic thing and expressive still has their own expressive thing.

But they got together and they said, this is kind of like a lot of work to do it all together. There's so many things like Wi-Fi and USB and networking, like, internet stuff, that like, it would be great if we just had one source code that we could use instead of having to redo it ourselves. And so Zephyr is this real-time operating system, so it's managing what is running on the CPU within the microcontroller, but it's also doing a lot of other stuff abstracting away iSquard C and spy and providing network stack and Bluetooth stack, all that sort of stuff in a general way that like any vendor can now contribute to.

And so our interest in that is primarily for the fact that like a lot of vendors have brought in support or like supporting their chips in Zephyr. So by us building CircuitPython on top of Zephyr, we kind of get a lot of chips for free where we don't have that much work to do to bring up Ice squared C or SPI or Flash or all these sorts of things. We don't have to manage compilers.

We don't have to manage compiler flags. It's just quite easy that once something is supported in Zephyr, we can get CircuitPython going in Zephyr, and it's been great. The other thing is that the real-time operating system part means that managing what is running when is kind of like not our job anymore.

So in CrcuitPython right now, We have our own system for managing things that run in the background. So like display updates and audio generation are the two main ones. And it's like kind of our own real-time operating system, but it doesn't work that well.

There's a world where it would actually be much better for us to have a proper real-time operating system to manage that. So kind of two-fold for why Zephyr is really interesting to us.

Paul

How is the progress in getting CircuitPython running on top of Zephyr coming?

Scott Shawcroft

It's going pretty well. It does work. We do have a few boards where we have two versions of CircuitPython for the same board.

One is like the classic, like, here's just the version built on the Nordic SDK, and here's the version that's more general. One of the biggest wins we would get is newer Nordic support. So for the NRF 54s. And so when I was working on that, I kind of left off in the middle of Bluetooth support.

And I've just not gotten back to that because LLMs and agents have just, changed the world. And we'll get back to it, I promise, but for now we're redefining or reworking how we work.

Paul

How are LLMs helping you with that work?

Scott Shawcroft

They do the tedious part. I think that's the simplest way to think about it. If you're doing something tedious, they're quite good. And they're quite good, especially if you have a way to feedback and make sure that what they've done is correct. So one example I did is that our expressive chips, which are Wi-Fi chips, they're built on top of the ESP IDF, which is like the vendor version of what I was talking about, right?

And I said, you know what? Like, they just released version 6 and we have version 5, and there is this change log that says, like, these are all the things that we change, and here's how you change this to that. It's like, you know what?

An LLM can do this. So I said, hey, Claude, I want you to move from this version to this version. And by the way, we have some changes we've made.

You'll probably have to do that too. And it did it. Like, you teach it how to compile, and it got it all compiling. But then the question was, is like, how do I know that it works? Like, it compiles, but does it work still? And now suddenly it's up to me to like test it again. And that's led to the hardware and the loop stuff that you wanted to talk about.

Paul

Yeah, it's a great segue. That's actually the next question that you've been working on hardware in the loop PCBs for testing microtrollers. That's right. For someone that hasn't heard of it, what is it? And how does that work?

Scott Shawcroft

Hardware in the loop is this idea that you can automate testing on device. So like I was saying, I've automatically had this LLM update from this version to this version, and it was able to do compilations on my computer, but it never actually loaded it on the device and can't actually verify that things actually work. And so this is something that on-device testing is something we should have been doing a long time.

In fact, within the first year of CircuitPython, it was something that I did try to do. We tried to do Rosie CI, and I, like, had a Raspberry Pi with a bunch of USB cores on it, and it was, like, trying to get it run every time we made a change, just to make sure that we don't regress. And we've gotten quite far not having that for the last 10 years.

But LLMs changed the game for that in a couple ways. One, it's super useful for that feedback loop for an LM. But also, two, actually, LLMs can help with a lot of the tedious work about that as well, of, like, writing a lot of boilerplate for test cases and stuff, is much easier now with LLMs as well.

So it's the perfect moment. The board itself was my desire to have a kind of standard setup for doing it. So like something that you could plug a dev kit into to find what the pin mapping to the device under test is, and then you have all the same facilities, all the same code running on the thing that's actually running the test.

And then one problem I had with the one 10 years ago was that I was using the Linux USB stack. and one of the things that we're testing is USB, what would happen is I'd actually crash the Linux kernel or the Linux kernel would get in a bad state and Dan's reached out to them at one point where like, hey, we found this bug and they're like, well, that's only a bug if your USB device is not working correctly, which we happen to from time to time. And so one thing I wanted to achieve with the hardware and the loopboard is that it doesn't do USB straight into your computer.

it translates USB over to a network connection. And once it's in a network connection, you can do all the USB stuff in Python without ever involving your actual Linux kernel. And so you could do all the testing that way instead.

And that's a lot of boilerplate code that LMs can do a reasonable job at generating in Python. So that's just part of it.

Paul

August 2026 marks 10 years for you working on CircuitPython.

Scott Shawcroft

Yeah.

Paul

We've talked a lot about what you're working on, but looking past, do you have a favorite memory that you want to share? Or is there something that you're really, really proud of in that time?

Scott Shawcroft

Yeah, I was thinking about this. I don't, a lot of the memories I have around CircuitPython are like actually me, going from this person that was on show intel to somebody who, like, worked closely with Phil and Limor. And I've been like super lucky.

And like the project, like, I hadn't actually heard a MicroPython when they asked me if I wanted to work on it. But I had done Python and I just discovered embedded. And I got super lucky with the whole thing.

So I think a lot of my, like, highlights are around that. One highlight I thought of was actually the Pycons where we gave hardware away and the swag bags, just having a lot of people excited about it. I think that because we're 10 years old, like, CircuitPython's quite mature now.

So a lot of my experience right now, because I haven't been to conferences, is around, like, somebody just randomly saying, like, oh, yeah, I use CircuitPython for that. I'm like, wait what? Like my Makerspace used it for their like authentication, like let people in the room sort of stuff.

And I was like, really? So I'm really surprised by that. And then you had said like what I was most proud of as well.

And I think what I'm proud of with CircuitPython is that a lot of the decisions that I had a lot of influence over when we first started have proven out to be good ones. Lots of small modules that are standardized across different microcontrollers, the design of that a that we've built hundreds of libraries on top of in a way that we could then come along later and make available on Linux, single-board computers like Raspberry Pi via Blinka as well. It's like that's all proven out to be the right call.

And also the behavior of CircuitPY of like you write to the file and it auto reloads. Like that was something new and still unique to CircuitPython. And I think like people think that's what CircuitPython is, even though we, we've relaxed that. For a while, that was our requirement, and that requirement's been relaxed.

But I'm very, very proud of the fact that those decisions we made in that first six months, like, I've really played out. And it's not often that as a software engineer, I'd get that sort of long, long-life feedback. So, yeah, really proud where we've come with it.

Paul

The Fruit Jam just turned one. When J.P. was on the show earlier this year, he shared a story of how the two of you talked in New York City back in 2017 about building a CircuitPython powered mini computer, which is what the Fruit Jam is. With that dream realized, what do you see in the future for CircuitPython?

Scott Shawcroft

That was definitely something I wanted to do. I only have very old memories of like those like bespoke single task computers like the Commodore 64, but that doesn't mean that I didn't think it was cool. And same with like the fantasy console stuff.

The Fruit Jam definitely, I did a lot of the foundational work for it, and then folks, especially like Tim Foamyguy, like really, really ran with it. And it's been awesome to see what people have done, including John and Cooper as well. So I think it's really cool that the fruit jam has done as well as it has.

There's this thing that I've really wanted to do with CircuitPython that I still haven't been able to do, which is being able to program from your phone. And if you see my, like, annual writings, I'm always like, we've got to crack this. Like, how do you program for your phone thing?

And, like, we did a lot of work on Bluetooth and a Bluetooth workflow, and we had PyGlider and FileGlider and these apps that can work with it, and they just never took off. We did Web Workflow, like, using the website after that, and, like, even that got more traction. And I think the core of it is that, like, it's really terrible to code on your phone.

Like, it's terrible to input text and edit text. And so my hope is that with, LLMs will be able to not need that anymore. You'll be able to tell your phone, like, make the LED blink faster.

And CircuitPython is simple enough, but it can modify that. So I'm really optimistic for that future. The BLE workflow has rotted a little bit, but that is definitely something on my vision for CircuitPython.

A lot of what my vision is around workflow, because that's core to how you interact with it. More broadly than that, like what features we have, really depends on like, what can microcontrollers do that we don't allow you to do. So one thing that we haven't really taken advantage of yet is like newer display bus protocol called DSI, which allows you to do like higher resolution screens and stuff that end up in phones.

And like, that's something that I would like, we actually do support, but I don't see us like really pushing people yet on. There's like Can Bus, I think we could do a better job with I3C is. out there. So yeah, it's a mix of like workflow thinking and what other things can microcontrollers do that we don't make easy. The other thing that we don't make easy that we could make easier is async, so being able to do multiple things at once. I want to watch a button and make an LED animation and have an HTTP request or HTTP server going at once. And I've gotten more comfortable with asyncio in Python and I think we could do a better job of having basically async versions of our APIs now so that you could do asynchronous spy or asynchronous iSquard Z, which would allow you to do kind of both things at once. So that's another big thing that that I've kind of like in my brain said like maybe Cirquiv511 is where we do that. And we could leverage like Zephyr and the real type operating system under the hood to like basically say like to really use that so that you can, none of your async IO tasks are happening. Then you can actually sleep and coordinate all the way down into the operating system underneath too.

So yeah, there's more to do.

Paul

Yeah, I did a project a year or two ago that used asyncio And it's pretty hard to wrap your head around at first. But once you do, it was just so powerful. But things that were blocking, like doing an HTTP request, get in the way of like an LED matrix scrolling. So figuring that out took a little bit of work.

Scott Shawcroft

Yeah, yeah. And I think the answer is like there's really no better way to do it. Like, ASyncIO is not great, but a lot of smart people have thought about it for a long time, and there's not a great way, more obvious way to do it.

So I think we could do a better job of, like, natively supporting that. I know it's more often used in MicroPython, but it's usually that they've built a layer on top of it that does it instead of, like, the native APIs. So, yeah, we'll take a look at that.

Paul

Tell me about the custom RP2350 Game Boy cartridge you designed that runs CircuitPython.

Scott Shawcroft

Okay, well, let me take you back seven years. I think it's been seven years, maybe eight. I had this idea that I could make any cartridge-based system programmable by CircuitPython.

They basically using, making the cartridge dynamic to basically talk to the thing through the CPU. So, like, for example, okay, I'm on a Game Boy, and I want to show this thing on the screen, well, I use these instructions, I have the CPU run these instructions in order to set the data the way that I want. And so I had thought of this, and at the time it was like SAMD51, it was kind of the new hotness.

And so I got it pretty far the ability to like cue up instructions that the Game Boy would execute for me, but it would like, at some point something would happen just like crash the Game Boy and you'd be done. And I was like, ah, this is like, I was using, DMA and the CMD-51, I was like, there's something around this that's just not quite right. So I had to basically put it away. I was like, I don't feel like I can figure out why this is happening.

So I had this design for a cart that you would insert into it. And then RP2040 came along and it was like, oh, PIO is really interesting because it can offload the, like, let me watch this Game Boy bus and make sure that I have a data back to it when it's reading. But the problem was that 2040 didn't have quite enough pins.

to be able to do both the Game Boy Bus and the few other things that I wanted to do. For example, the cart also has MIDI input and output on it. The new one also has StemaQT, so you could plug a Stemakutie board in there as well.

So the RP2350 came out. It has PIO that's a little better than RP2040, but it also has more pins. So I have lots of pins on this cart now.

And it turns out they're 5-volt tolerant as well, so it only level shift the data lines. I don't have to worry about the address lines. So yeah, it's on V8 right now, and that version originates from SAMD days.

And I've got it where it is running CircuitPython within a Game Boy Cart. I use a thicker PCB, and I made it slightly bigger, so you don't need to put it in a shell. SAMD versions, you had to, like, get an old Game Boy Cart shell or 3D print yourself one and cut holes in it or something for the MIDI outputs and stuff.

but I had seen somebody do a Game Boy cart where you just make it thicker and you can just slot it right in. So that's what I have working. It's able to boot up.

Somebody else had made an RP 2350 cart called the Crocko Cart. They're really geared towards being a loadable, like load whatever game you want on it and play it. So they actually have hyper-ram and they have to do other tricks for that.

But they did have an example where they can have PIO-read, the address, look it up in memory and using DMA and then get it back to another PIO, like all automatically without the CPU being involved. And so I've gotten that working by having like a 64K cart within CircuitPython. And then right now I'm working on getting it so that when you say, hey, like tell the Game Boy to do these things, these instructions.

I'm working to get that in memory so that when these things happens, it does the thing that you want. And I'm hoping to have it done this week. I've committed to being done with this project by the end of the week.

And it's looking like we'll probably have it available from Adafruit as well. Lady Ada was telling me that they want to get kind of in the business of having some more weird designs where we just say like, here it is. And we don't make any huge promise about how well it works.

But here's this weird thing. And the Game Boy Cart is like totally that niche of like it's not for beginners really. It's for that person that really does want want to get in the Game Boy weeds and program it from a microcontroller. And obviously, I'm interested in doing it from CircuitPython. So, yeah.

Paul

And part of that vision is that people will be able to actually program the games in Circuit Python and then run them on the Game Boy.

Scott Shawcroft

That's right. So you're running your game on the cart, and the cart is telling the Game Boy what to do. So the Game Boy says, okay, like I finished a frame, and CircuitPython under the hood says, okay, here's the instructions to run.

And I'm going to have it say, like, okay, check to make sure if there's a button pressed. And then I'll give that back to CircuitPython. So you can say, like, hey, is there a button pressed?

And then you can decide what to do within CircuitPython. And you could say, like, hey, move this sprite from here to here. And, like, that will translate to, like, tell the Game Boy to do these instructions that set the memory for the Sprite.

Right. So the game is running in CircuitPython. And CircuitPython is telling the Game Boy what to do.

So there's a little bit of subtlety there of, like, We're not actually running a lot of logic on the Game Boy. It's just more like straight line. Like, okay, load this memory, this value at this address that makes so sound play or something.

So it's this weird hybrid of it.

Paul

It'll be fascinating to see what the makers and coders out there can do with that.

Scott Shawcroft

I'm very excited to see it. I think I'm like much more confident in the ability of PIO and the RP2350 to keep up with what people want to do versus the SAMD version. So, yeah, I'm looking forward to it. I was thinking about sending John one of my early carts, but it's looking like hopefully we'll have it in the store and not too long, again, with caveats. But, yeah, it seems to be going pretty well.

Paul

Well, that's great. Scott, thanks so much for coming on the show.

Scott Shawcroft

Thanks for having me, and thanks for doing the show.

Paul

Thank you for listening to The CircuitPython Show. For show notes and transcripts, visit CircuitPythonShow.com. and help keep the show ad-free. Join the supporter tier for exclusive content and early access. Learn more at CircuitPythonshow.com slash support. Until next time, stay positive.
