---
date:
  created: 2022-04-05
title: "Episode 6 - Scott Shawcroft"
---

## Show Notes

[Show notes available here.](../../episodes/Season 1/ep006.md)

## Transcript

Paul

Welcome to the CircuitPython Show, an independent podcast with the people in and around CircuitPython. I'm your host, Paul Cutler. This week, on episode six, I'm joined by Scott Shawcroft.

Scott, thanks for being on the show. Thanks for having me. I was listening to a podcast you were on last year on the real Python podcast, where you mentioned that you had gone on show and tell a few times before you had the opportunity to join Adafruit.

It was a really cool story. How did that happen?

Scott Shawcroft

I worked at Google for almost six years, and I decided that I was done with that. So I took about, it ended up being about a year, but I was really into drones at the time. So I did, taught myself PCB layout and PCB manufacturing and all this stuff.

And then I ended up porting an open source flight controller software to the flight controllers that I was making. I started going regularly to show intel to show that off because I was also watching a lot of Ask an Engineer and Descalatea to learn the tips and tricks for doing electronics manufacturing. So at some point I started just going on and being like, today on Show and Tell I'm going to talk about motors or I'm going to talk about speed controllers or flight controllers and kind of chronicle all of that as I was going along.

I actually did like one manufactured batch from Macrophab and started selling it. But I quickly realized that like to do a business, there's a lot more than just the engineering side. And I really am like, my strength is in engineering.

And I really had no interest in doing product market fit analysis and product design and marketing and all of that other stuff. So I was keeping track of, like, I had set aside a certain amount of money to basically burn through. And I knew that I was like coming to the end of my time to not being employed.

And so I was starting to look for jobs. And so I literally went on show and tell one of those weeks and said, hey, I'm looking for a job. And, you know, Phil is really welcoming.

So he had like gotten my info before and like blog, some stuff up that I had shown before. And so the next day I got an email just sitting here in the office and got an email from just two sentences that said, hey, do you want to do stuff with us? And I was like, yeah. And they were like, well, we have a particular project in mind. Is that okay?

I'm like, yeah. And then they were like, hey, there's this micropython thing and we'd like to experiment with getting it on our boards. And I hadn't heard a micropython. I had done Python for ages. Like I started doing Python in like 2005. So, like, I had done a decade of Python by this point.

It had always been my tool that I really liked. It was never really my day job to do Python, and it's still not really my day job to do Python. But it was a really good fit, because not only did I have all this experience with Python, but I had also spent the last year learning all of this embedded stuff.

At the same time, I was getting kind of burned out on the quadcopter stuff, but I really learned that I liked hardware, and I liked embedded a lot. So it was like perfect timing for me and it worked out really well.

Paul

That's awesome. So that was just over five years ago. Is that correct?

Scott Shawcroft

Yeah, that was like August of 2016. So yeah.

Paul

As you think about the last five years, what are some of the biggest changes you've seen, you know, starting from scratch to now? Or maybe I can rephrase that and say, what are the accomplishments you've done in those five years that you're most proud of?

Scott Shawcroft

Yeah, I mean, I think it's important to say that we didn't start from scratch at all. Like Micropython was two years or maybe even three years old at that point. And Damien and all of the other contributors to Micropython had done an awesome and continued to do an awesome job with Micropython.

So we're very much standing on the shoulders of giants. There was a few things that I brought kind of in that fall of 2016 that I think have really, over the last five years, shown that they were the right calls. One was really focusing on USB.

So actually for the first three versions of the CircuitPython, we had ESP 8266 support as well. And that was good in its way, but we really had to narrow down and say, we're just going to do USB. That was a really good call, and we continue to do really well with keyboard mouse support from CircuitPython, for example.

So really focusing on USB has really been a great call. And then the other thing that we did in that fall that kind of we started with was we chose to have a different layout internally to our source code, so that we can know that our hardware APIs were identical across all the boards. Because my argument at the time and continues to be that I had seen Adafruit really succeed in Arduino because they had built all of these drivers and examples on top of this uniform API that Arduino provided.

So it made a lot of sense to me to really push to have what became CircuitPython also had that really pretty strict API to build on top of as well. And we've seen just the API that we have, ended up with has been really, really versatile and has actually, the core of it has not had a lot of changes since then.

Paul

Oh, that's awesome. So speaking of USB for the first time and a long time, some of the USB requirements are changing where it doesn't have to have a physical USB report? Is that the change?

Scott Shawcroft

Yeah, that's definitely fast-forwarding five years. One thing that I've wanted to do for the last few years in particular is support a wireless workflow. So I kind of think of a workflow as like how do you actually program circuit by on right?

And we had focused really narrowly in CircuitPython 4 down to the USB stuff. And we were very strict until 7, where we relaxed it to include Bealey. Bealey is Bluetooth low energy.

It's a very common protocol that phones and tablets and laptops in particular can speak. And so by supporting a Beale workflow, what we're doing is we're allowing people to use phones and tablets in particular to program their device. So it's well worth the risk, but I'm definitely.

foreseeing that we're going to have to do a lot of messaging and marketing around like, this is not the CircuitPython you think. And we were, yeah, Phil Lamore and I were just talking about how we can make it clear which version of CircuitPython you're actually dealing with.

Paul

That makes sense. I'm embarrassed to say that just a couple weeks ago, I got to the last Adabox and started setting up the glasses that came out around Halloween. I just wanted, you know, I put it on Twitter.

I had the text scrolling across that said, Welcome to the CircuitPython Show. And when I went to do that, it's like connected via BLE, and I grabbed my iPad and type the text it on my iPad. I'm like, oh, my goodness, this is cool.

Scott Shawcroft

Nice.

Paul

That's got to be, that's got to make it so much easier for people that are new to hardware or new to the CircuitPython to actually get involved and get their hands on and start programming it.

Scott Shawcroft

Yeah, I mean, that's my hope. The other thing that we did, the technical things I just talked about were things that happened kind of in that fall. And then in the spring was really when we had to make a. decision about, were we going to try to upstream everything, or are we going to kind of establish ourselves as something separate? And obviously, we chose to be something distinct.

Separate is maybe not the right word, but that's when we settled on the name CircuitPython. We decided that we would keep this going ourselves for the longer term. And also, that branding gives us the very clear of like, this is what you can expect from CircuitPython, and this is what is compatible with CircuitPython.

Paul

Sure. So you mentioned upstream. How many of the things that you work on today do you actually push back upstream that they accept?

Scott Shawcroft

It's not a lot. There's not a lot that goes back upstream where our repository is structured very differently for, like most of the work in both Micropython and CircuitPython is port work, meaning supporting particular chipsets. And because we have a different hardware API, it's really hard to upstream that work, where you will see some stuff kind of flow from CircuitPython back into Micropython is more like we find bugs in the Python core.

And the way that that works is it's not really, it's not usually a poll request from us. It's more like an issue saying like, hey, we found this issue. Here's our copy of how we fixed it.

And then they may or may not do it that same way.

Paul

But at least they know about the issue then.

Scott Shawcroft

Right. Like we talk with the MicroPython folks. Like we're friendly with them.

So they let us know the things they're excited about and we let them know the things that we've done. The bigger example is compressing error messages. So we did that in CircuitPython first in order to save space.

And at the same time, we did translations. So we can get a French version of CircuitPython that will have error messages in French and other messages in French, for example. But in MicroPython, they chose to do a different approach.

They do compression, but they don't do translation.

Paul

Speaking of localization, how many languages is CircuitPython translated to today?

Scott Shawcroft

I think it's over 10. but the quality of those will vary. So if a particular message is not translated, it will still show up in English.

And we try to have the core messages about, like, hit Control D to reload. We try to have those translated before we'll turn it on. But yeah, we're always looking for folks who speak other languages because that is not my strength.

Paul

Or mine. I have so much respect for people who can write documentation or contribute code in multiple languages. So you mentioned a lot of the work is around porting to different pieces of hardware. You spent the last couple months of 2021 porting into the Raspberry Pi single board computers. What were some of the biggest challenges in actually bringing it to a full-blown computer and not just a microcontroller?

Scott Shawcroft

It was very different. So I've been really interested in supporting the Raspberry Pi proper, the Broadcom chips, because they have really good HGMI support. So whenever we're working on something, it is a question of like, what does this new chip provide us that we can't get in other chips?

Raspberry pies, everybody's got one. They're usually not being used in my experience. And so it was like, hey, this is how in CircuitPython I can get access to a display.

And you could already do that with Blinka, but you still have all of the setup from Linux. And so I was really interested in this idea of blowing people's minds of taking something that you would just put Linux on and make it so that you don't need to put Linux. You can get more similar of an experience to what Circup Python has on a micropriton.

controller. So that's why I did it. And the challenge was different, somewhat different, because there is a lot of differences in the way that the CPU actually works. How it handles interrupts.

A lot of them are multi-core, although we're not using the multiple cores. And there's memory mapped unit that doesn't exist in microcontroller land as well. So there was a lot of the CPU side to do. And then the peripherals are actually like not great. So the peripherals were actually not as good as the ones that you'll find on a microcontroller.

So figuring out how to get those to work okay was some of the challenge as well. So I'm happy where it's at, but there's definitely more work to do there.

Paul

There always is.

Scott Shawcroft

Yeah.

Paul

So when you mentioned the HDMI support, is it truly just plug and play, you flash it to the card, or you flash your SD card, plug in the HTML cable, plug in your power, and it boots right up to the REPL? Yeah. Yep.

Scott Shawcroft

Yeah. So just like all of our displays, if the board has a built-in display, you'll see the terminal on the screen. That's true for the Raspberry Pi boards as well.

One of the caveats with Raspberry Pi's is that they don't always have the USB plugs to act as a USB device. So you'll want to check the learn guide I made for which of the many USB connectors on those boards is the one that you want. But for example, on the Pi 4, the USB Type C that you use for power actually can act as a USB device as well.

So that's where you'll get your circuit pie drive, and you'll get your CircuitPython serial. And in fact, it's just USB, and we use the same USB stack. So you can actually do the HID stuff that you can do.

You can do the MIDI stuff that you can do because it's all the same code.

Paul

So it's almost like we're back to the 80s when I was a kid because I'm old, and you would take those Commodore 64s or a TRS80 and plug it right into the TV. Yeah. You're just programming. Right. It's like you have basic, and now you just have CircuitPython instead of basic.

Scott Shawcroft

I've actually experimented with how you can edit Python code like you can edit Basic on those computers, where you put the line number and then the line of code that goes there.

Paul

Oh, neat.

Scott Shawcroft

I experimented with that. It's something I love to do, and in fact, the Commodore 64 is definitely one of my inspirations for this. The Raspberry Pi released the Pi 400, which is actually a keyboard with a Pi 4 inside.

Right. And probably the next thing I work on when I circle back to that is going to be getting the keyboard working. Okay.

So that we can literally have that circuit, CircuitPython 64 experience or whatever we want to call it, where you can edit it directly.

Paul

We're just going full-on retro between your work on that and Lady Ada and Jeff Epler working on floppy disk support.

Scott Shawcroft

Yeah, I didn't know they were going to do that, but I'm pretty excited by it. I have an uncle that has a bunch of eight-inch floppies that he wants to archive, so I keep asking them when they're going to get to eight-inch.

Paul

Nice. Hi, it's Paul. I'll get you back to the show in just a moment.

I wanted to say thank you for listening. If you like the show, please hit the subscribe button, write a review or tell a friend. You hear that a lot, but it really does help.

For other ways to help the show, visit CircuitPython show.com slash support. Now, back to the show. So now that you've wrapped up your Raspberry Piwork, you've started working on the ESB 32 boards.

Is that correct?

Scott Shawcroft

Yeah, so particularly we have existing support for the ESP 32 S2, which is the first Dispressive board that has native USB sport. So we were really excited about that. That was the first time we could actually put CircuitPython on a Wi-Fi native board because the other previous chips did not have native USB and therefore couldn't show up as the CircuitPi Drive we all know and love. And since then they've come out with the ESP, or they're kind of coming out with the ESP 32S3, which is kind of a newer, beefier version of the S2, and it also has Bluetooth Low Energy in it. So this will be the first chip that we have CircuitPython support that can do Wi-Fi and Bluetooth.

Paul

Oh, that'll be really neat.

Scott Shawcroft

At the same time.

Paul

Yeah, I'm very excited about it. So can you bring that experience that we were talking about earlier that I brought up with the glasses via BLE here right on an ESP chip then?

Scott Shawcroft

That's the hope, yeah. We're not there yet because it's not done. One thing at a time.

I'm working on implementing it. But yeah, that's the hope is that we'll be able to do, we'll be able to do the BLE workflow. you may have seen that we're also supporting the ESP 32C3, which does not have native USB, but it does have Bluetooth, does have Bealey, and it's their first Risk 5 core, which is what people have been kind of excited about too.

Paul

And for those that might not know, the Risc V is...

Scott Shawcroft

Risc V is like the API to the processor. So there's this notion of instruction set architecture which is like what the numbers mean to the CPU, basically, what the data in terms of commands actually means to the CPU. So it's not necessarily the CPU design itself, but it's the API that you use to use the CPU.

And the nice thing about that is that's the API that compilers produce code for. And so the benefit of having a open, so Risk V is open, standard, license-free, so anybody can implement a CPU core. And if they implement that CPU core, whether it's open or closed, they can use all of the tool chain compiler infrastructure that have been built upon that API.

So I think people get more excited than they should because the reality for somebody like me writing software is that you're really just using a different compiler. But on the hardware design side, it's pretty neat because they're going to get a lot of different implementations of CPUs that can all use this existing infrastructure.

Paul

So what is the benefit for the makers?

Scott Shawcroft

For Risk 5? I think it's probably just a few cents and cost, right? So every arm core or extensa core is a licensed core, and that will add a little bit of cost to chips.

The other thing is that because there are open Risk 5 cores, if you had an FPGA design that you were doing, you could just plop that in and use that as well. That makes sense. But I don't expect a lot of people to be doing FPGA design.

Paul

Probably not at this point. No. In your spare time, you've been working on a website at W.A. law.org focused on Washington State.

Scott Shawcroft

Yeah.

Paul

What spurred your interest in local politics?

Scott Shawcroft

This story kind of starts last year. I am obviously a very technical-minded person, and one of the things that is pretty common in the different states here in the U.S. is that some states have laws that prevent public entities

Paul

from providing Internet to people. Community broadband.

Scott Shawcroft

Community broadband. There's a great podcast called, community broadband bits from the Institute for Local Self-Reliance, if people want to go down that rabbit hole. Lots and lots of awesome people around the country who are doing municipal broadband and related things to get people primarily fiber internet, but not always.

So in Washington State, we had had a law that prevented public utility districts and port districts from providing internet to folks. And last year, there was two different bills that got passed by the to remove those restrictions. And one of them was more permissive than the other one.

And so that got me kind of more involved in this process of figuring out, hey, there's these two bills that are going to get rid of this. But one is only like public utility districts and one is like cities and counties and public utility districts and port districts and stuff. So there was some drama around that because both bills passed and they both went to the governor, which is the next step after it goes through the legislature.

And the governor signs them concurrently, one in each hand. That's awesome. Which is not the governor's job.

The governor's job is to pick, in my opinion. Oh, I see. Okay.

And so there was actually a lawsuit, the Secretary of State, whose job it is to order the laws and the order matters for precedence if there's overlap. So the Secretary of State had to file a lawsuit, said, hey, do I actually have the right to pick? And if I have the right to pick, what they did was they went by the order.

it was passed from the legislature, which turned out to be a good thing because the more pervasive one was past second or first or whatever the better one is.

Paul

Okay, good. That was my next question. That's good to hear.

Scott Shawcroft

So, yeah, so as of July in Washington here, there's no longer this limitation. So public utility districts can provide retail service to customers rather than just wholesale to other entities. So that's really good, and that got me more involved in promoting public broadband throughout the state, and there's a lot of money coming in the U.S. here for more broadband. And so as I learned more about how the legislature works, I got interested in collecting public data and trying to repost it and share it with people to make it easier to understand and potentially better cross-linked than the existing public resources are. So, for example, look at a bill, see who sponsors it, and then go to a page that not only says this person is on these committees and has these bills, but also their last campaign, they got this much money from these top donors, for example.

Paul

Which is good to know, and that should be public knowledge.

Scott Shawcroft

And it is. It is publicly available. Easier to access.

But like those two worlds, the legislative world and the campaign finance world are very two different websites right now. And so like, I haven't done it yet, but my intention is to like kind of like make wah-law, or somebody mistook it for a different name, WALGE, for like legislature. So I'm like, I just bought the domain and I might switch it to that.

We'll see. But kind of making that kind of a one-stop shop for like all the information about the campaign stuff and all the legislative stuff.

Paul

And one of the benefits I think that you're doing on the site is that you're reformatting a lot of the text. That's difficult to read for the average.

Scott Shawcroft

Yeah, a lot of it is if you go on the regular site, A lot of it's in PDFs, and I don't know how good of a job they do of making those PDFs accessible, but they do have a website where you can get XML copies of all of the bills as well, and they don't do any sort of formatting. And the thing that bothered me the most was some of the sections of the law include a lot of nested lists, like deeply nested, like four levels. Sure.

And they don't indent them in the actual copy of the the law. And so it's just like, how are you going to know whether you're three deep or whatever? And so Markdown's great for this. So one of the first things I did was I was converting the legal text, the revised code, into Markdown as a way to format it better.

And I actually did, like the very first version of this website was actually a GitLab instance that I was running because I really wanted like the Git workflow for laws so I could do like, who do I blame for this? Like, you know, Git has blame. So you can see the history of different components of the law.

But I'm not really a sysadmin. So this current version is just a GitHub repo with Markdown that gets converted to HTML and then statically served.

Paul

Well, that's great work. I mean, I think the key theme there is accessibility, whether it's accessibility to get broadband or accessibility to understand what the laws that are being passed and who is supporting them.

Scott Shawcroft

Yeah, and also one of the main things that I'm trying to do with, like, So there's like a two-year cycle to making laws. And I have this landing page where it's like, here's all the laws for this biannium, which is the two-year cycle. And here are the ones that are coming up for committee. So when you can actually do, well, it's executive action or public hearings. So like trying to be more involved in actually giving testimony when there is public hearings for or against bills.

Paul

That's great work.

Scott Shawcroft

Thank you for doing that. I'm nerding out on that. One of the themes between all I do is the things I do usually involve a lot of learning. So always looking for new topics and new things to learn. And how the law is made is one of them.

Paul

I can relate to that passion for learning. It's one reason that we're here today and listening to a podcast. Yeah.

So the next question I have for you is one that I is a segment that I call Turn the Tables. I'm a big vinyl record fan. I've been asking all the questions.

Here's your chance to ask a question of me.

Scott Shawcroft

I was a little worried that there would be duplicates on this, But I was curious just how you found CircuitPython and how you got into it.

Paul

I attended a Microsoft conference a year or two back, and I've been working on learning Python these last couple of years. And they had a Python workshop as part of it. I think it was probably PyCon.

And if you completed a couple of the tutorials that Microsoft put together, they gave you a $50-Aid-fruit gift card. So I bought a Circuit Playground Express, and it sat in my drawer for probably a good six to eight months before I got it out. And then I did.

And like everyone else who starts playing around with CircuitPython, you realize how easy it is to do some of these things with the various sensors, the neopixels built in. Then I came across a project that I was really interested, speaking of vinyl records, where someone had used a Raspberry Pi to actually put neopixel strips. And when they wanted to go get a record, the neopixel would light up on where the record is on the shelf, which got me thinking, okay, what other projects can I do?

So my office is on the other side of where my record player is. So now I'm working on a project with CircuitPython that will display the Elmart on my desk, even though the record is 15, 20 feet away. So that's kind of how one thing just led to the other.

And, you know, like all the other makers out there, you can always do it better. And I keep learning. And, you know, just like we talked about, I have a passion for learning.

And it was a, I had been learning Python. And now I'm learning CircuitPython, which, has just been a great experience.

Scott Shawcroft

Yeah, and those things are, like, a lot of the things you'll learn do apply across them, which is awesome.

Paul

So the last question I like to ask all of my guests, you're going to start a new project that uses a microcontroller. Which one are you reaching for and why?

Scott Shawcroft

Well, for me, personally, I'm very excited for the S3. I was, like, up late last night thinking about the Bluetooth things that I could bridge to Wi-Fi. And so I'm pretty excited about that.

Of course, it doesn't work yet. Well, one thing at a time. And most of my projects I get excited about, and then I do the thing I needed to do, and I, like, lose interest after I've learned all the stuff I need to make it happen, but don't actually make it happen?

Paul

I know that feeling very well.

Scott Shawcroft

Yeah. The new ESP 32S3 I'm very excited about. The RP2040 with the PIO is really interesting, too.

There's lots of good options. I think I wouldn't really reach for a SAMD21, the M0, of the first chip that the Adafruit brought me in for. However, I have one on my desk that I'm using every day because it's literally just doing a touch sensor.

So when I do capacitive touch, it sets a pin high. And it's how I have this setup where if I put my hand on my trackball, it changes what my keyboard does. And so I just have the Sam D21 that is my hand on the trackball.

And if it is, set this pin that then makes like, pretends my keyboard has a pretend. key pressed, which then changes the layer of everything that it's doing. And that allows me to do left-hand trackball, right-hand, just mouse clicks.

So I don't actually have to do mouse clicks on my trackball. I can do it on the other hand. Oh, that's awesome.

Let my left hand do all of the moving.

Paul

Well, that's all I have for this episode. Thank you for being a guest.

Scott Shawcroft

Thanks for having me. Thanks for doing this podcast.

Paul

It's my pleasure. We'll talk to you soon. Thank you for listening.

This has been episode six of the CircuitPython show with guest Scott Shawcroft, recorded January 27th, 2022. That's a wrap on season one. Thank you to everyone who has subscribed, left a review, told a friend, or supported the show.

Your support has meant a lot, and I'll be back soon with new episodes. Visit CircuitPython show.com for show notes and more, and until next episode, stay safe. Thank you
