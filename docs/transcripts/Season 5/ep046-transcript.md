---
date:
  created: 2025-05-19
title: "Episode 46 - Justin Myers"
---

## Show Notes

[Show notes available here.](../../episodes/Season 5/ep046.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. This episode, I welcome Justin Myers to the show.

Justin is a software engineer living in the Pacific Northwest with a passion for open source development and recently contributed the new Connection Manager Library to CircuitPython. Justin, welcome to the show. Thanks very much. I'm glad to be here.

How did you first get started with computers and electronics?

Justin Myers

So I was a child of the early 80s. My family, my mom was really into it. We got a computer connected to like the bulletin board systems really early on. So it's just something that was always there and just kind of gravitated towards it.

It's always been something that's interested me and fascinated me. I remember the first program I wrote was from a we had a Commodore 64 and literally coding out of a magazine. I had no idea what I was doing, just writing verbatim what was there.

And then just kind of continued and was like, oh, can I make it do this? Can I make it do that? And then I've been doing that for the last 35 plus years at this point.

Paul

That's how I got my started too, programming that assembly code right out of a newspaper like magazine. And then I spent so much time on BBSs as well. How did you first get into electronics?

Justin Myers

Electronics was interesting. I'd always kind of dabbled at weird things, pulled stuff apart, whatnot, kind of looked under the hood, but didn't really do a lot. And then a number of years ago now, I don't even remember at this point, there was a company doing a And the company at the time was called Spark. It's now turned into a particle, who I know has partnered with ATAFruit on a few things and whatnot.

But they had a Kickstarter out for these like Wi-Fi dev boards that you could code and do over there updates. And I was like, that seems like a good thing to donate to. And so I donated to them their Kickstarter or whatnot.

And I got them. From there, I was like, oh, well, I've got these small chips. I don't know what really to do with them.

And so I did some searching. And that's when I found AtaFruit for the first time is like, oh, I need more stuff. I need sensors.

I need all of these other things. And then I just really started, you know, diving in. And I kind of add different things and played with things and just kind of continued down that path for a while.

And I had built some, you know, small, fun things to use and whatnot. And yeah, really just enjoy it.

Paul

So how did you discover CircuitPython? Was it part of that process or something that came later?

Justin Myers

So I kind of watched it. So a lot of my development originally started in C. I'm now a Python developer for the most part. But kind of with that, so Arduino.

know and everything made sense to me. It was really easy to kind of jump in. And then I saw when CircuitPython came out and I kind of looked at it. I'm like, well, that's pretty limiting. And I just kind of walked away from it. I'm like, maybe someday. I think it's kind of when version 8 came out.

I had looked at some stuff and I was like, oh, they've added quite a bit to this. You know, they've added some of their Wi-Fi stuff to it and things like that. And I was like, no, this might be worth giving it a try. And so really kind of started digging in around there and then really started kind of playing with it more. At this point, I still kind of swap between the two, depending on kind of what I'm working on.

Paul

Speaking of Wi-Fi, over the last year you've been working with the underlying networking code and CircuitPython. What is Connection Manager and how does it make networking easier for users?

Justin Myers

I'll kind of step back one level to kind of where it kind of came from. So I joined Discord because I had a question about something and was looking and kind of saw all this stuff, these users that was constantly just like, where they're here? like socket stuff, everything.

And it was like, just kind of noticed there was a hole there and noticed kind of when looking that, you know, there was a handful of other people that would help. And at that point, like I had an airlift board and I had, I don't remember what it was at the time. And went to ESP S2 or S3 or whatever and kind of noticed as I was playing with them.

It was like, oh, wow. Like these two things are totally different. Like there's no similarities between how you set them up.

And so kind of through that, decided, you know, kind of reached out to a few people and it's like, hey, I think there's a better way to do this. And both, like, whether you're using requests or, like, through ATAFruit I.O., everything was separate. And so once you use more than one of the services, things really started getting complicated.

Paul

How was your suggestion received on a better way to do it?

Justin Myers

I thought it was received pretty well. So basically, there was a session manager that was in requests that did a lot of this already. And so I had done a PR to basically kind of just separate that piece out in requests.

And then from a couple of people, they kind of mentioned like, oh, maybe we could break this out into its own thing. They were really for kind of breaking up and making it simple. In the end, it of fruit and specifically CircuitPython, right?

They've got their goals, right? And so they've only got so many people and so many dollars to move things forward. So when people come up with a different idea to help and they don't have to do much, other than maybe review some code, It seems like they're pretty good-ho about being able to add it in.

Paul

So you mentioned that there's a few different ways to get networking to work in CircuitPython with add-on boards like the airlift or Wiznet or native networking. How does Connection Manager work behind the scenes?

Justin Myers

So in a super kind of like high level, right? So you, like everything in the end is a radio, right? So you have like if you're using one of the newer boards, it's literally Wi-Fi.

If you're using the SP, you're going to define, you know, the SPI, like you define that. or same thing with the WISNet. And so the Connection Manager, like in the end, you just pass it to the radio, right?

And then it then goes, oh, what kind of radio is this? And then from that, it then does. So before you'd have all these imports to be as you needed the radio and the pool and the SSL stuff.

And so it goes, oh, it's this type of radio. And so it'll then do the imports for you. And so you don't have to think about that anymore, right?

It's a single import for Connection Manager. And then it'll figure out what you need. There's different versions to spend what very.

version of CircuitPython you're on for like the Wisnet that'll actually allow us to sell or won't. And so it just handles all that for you. So you just pass it a radio and then they can do everything. And then there's even a software defined radio if you're doing native networking.

So if you're in C Python that you can actually use Connection Manager the exact same way. And so you can actually write all your networking code and test directly just in Python on your laptop. Like you don't even need blink or anything like that if you're just doing regular internet connection stuff.

and you can use that to pre-write all of your code, which I now do all the time because my regular net is way faster than trying to do it on a microp controller.

Paul

Oh, that's neat. I had no idea that you could do something similar in C-Python with Connection Manager.

Justin Myers

Yeah, it was like, and especially as I was testing stuff, like that was kind of a big part of it was, okay, pulling out an airlift and kind of trying to work through this stuff and make sure it works, especially when you're trying to work through like multiple connections and things like that. like they're small chips. They're not super fast.

And so especially trying to iterate and things like that makes it a lot harder. So changing that and everything, especially when I do bigger projects and things where I'm doing things like say, OA through Google or something like that, having a connection that is strong and stable. And I'm not going to run out of sockets or anything like that was really helpful.

Paul

What kind of challenges did you encounter along the way?

Justin Myers

Kind of the biggest one. So as I said, like I started a lot of my series. serious development in C and even did some things in some memory constrained areas.

And so I was originally very familiar with that. But then as the Earth went by and I no longer had to compile my own special Linux kernel for my web hosting and everything and like CPU and memory and all that stuff was just enormous and free, right? Like you had as much as you wanted.

I think with a lot of people, my programming style got, I wouldn't say lazy, but not as far focused. And so kind of one of the biggest things was as working through this was, oh, yeah, I'm now on a constrained device again. And not only that, right? Like, not only memory and CPU and speed, but these can only do so many connections, right? You can only have a few before they just run out of memory, whereas, like, I can open a socket, hundreds of sockets all day long on my laptop. So kind of re-going through that switch and trying to think through it for all the devices and everything like that.

It was a good challenge and a good remembering of like, oh, be a little bit more focused. And I've even now re-implemented some of that stuff in my daily life to be, you know, think through a little bit more performance level, you know, taking the extra time to think through that.

Paul

Very cool. As part of creating Connection Manager, you developed a testing framework. Tell me more about the framework.

Justin Myers

Yeah. So kind of one of the big things was so after the initial. part of Connection Manager was created, still realized there were a bunch of different ways to do things.

For example, there was one way to get the IP address from the native radio and a different way to get it from the airlift. And so I wanted to go through and make sure all of these things worked, especially as we moved stuff around. And so kind of built this testing framework that I could, you know, plug in any chip and then run this set of tests.

And it would go through and go, like, it would even detect the radio that it had connected to it. And then go, oh, great, you're on a WISNET. And then it would run through a series of just standard tests to make sure nothing broke.

Like it would go through all the different things, you know, HTTP, HPS. It would connect to NTP for time. It'd even, you know, run a micro server to basically go check.

And it was basically like, did any of this break? Like the goal was always to actually have something. And hopefully someday I might try to push this down the line again.

But like as they come out with new versions. So like another big part of it came out because we were right between eight and nine for CircuitPython. And they were, you know, making some changes or whatever.

And it was like, oh, did we break this? Or did we break that? Like I'd see someone testing.

They're like, oh, this isn't working anymore. And so it's kind of like trying to build something to go, oh, does all of this stuff work? it kind of built out of that.

And like ideally it would be something that somewhere, like whenever they do a release, these things would get wrong, right? Because we see with every release, like sometimes they'll see, you know, whatever it is, 0.7 and then like the next day, 0.8 comes out because you have some regression that some user finds. So if there was some way to build some testing framework around it, I'm definitely not in their build system or anything like that, but it was something that I could do to kind of test to make sure things weren't breaking or whatnot.

Also help find all the, ways that the different radios were different so we could slowly work towards getting them so they're all the same.

Paul

Do I want to know how many different boards you ran through those tests?

Justin Myers

I know we're not on talking only, but I'm going to adjust my camera just so you can see it. That whole stack there is almost as tall as to me. So it's all my electronics gear. I probably have about 50 different boards at this point that are all different. Ran it through all of them, which obviously is painstakingly when a new release comes out and you've got to go download 50 firmware and update them and everything like that.

And then, of course, then my router started having problems because I had too many connections to it because everything was connected and everything. Sure, it's always something. Yeah, it's always something.

Paul

So last question I ask each guest. You're going to start a new CircuitPython or microcontroller project. Which board do you reach for?

Justin Myers

So this is always a hard question. Like, I love asking this in a very different thing when I'm interviewing somebody. Like, if you were to build a new thing, what software would you use?

And my goal is always to find out, like, is this person a, I'm a hammer and everything's a nail type of person? Or are they not? So it really depends on what you are doing.

So good, solid Wi-Fi and everything like that, good powerful chip, if that's what you're looking for. The ESP32S3 is one of the ones that I use often. If I am doing something specifically that is more Bluetooth-focused, the NRF-52 series, so that AetaFruit has the bluefruit scents.

I really like that board. That's really a fun one. It has a couple sensors on it and things like that.

And if I'm not doing any sort of Wi-Fi and I just need something that's nice and strong, like I really enjoy the M4. It's been around for a while. It's a pretty powerful chip.

It's got floating points. I do a lot of stuff with math and things like that. So having that floating point processor actually built a library or ported over our library for not determining declination that NOAA has built out.

And so having that the floating point makes it a lot more accurate and things like that. I've started diving a little bit more into the Pico series, but in the end, still not my favorites. So I recently did get a 2350 and I'm going to play with that one.

I think the hardest part of not is since I do do do a lot of circuit points. Python and it can't take advantage of the dual processor, the dual cores. It's kind of like, I get a lot of something that I can't quite use.

Paul

Right.

Justin Myers

I keep hoping that there's a way to run a second, like, Arduino something on the other core that just sits there and listens and then you can have this powerful, like, go do this math. And then, you know, do my easy coding in CircuitPython. But someday.

Paul

Someday. Justin, thanks so much for making time and coming on the show.

Justin Myers

You're quite welcome.

I enjoyed it.

Paul

Thank you for listening to The CircuitPython Show. That's a wrap on season 5.

I hope you enjoyed the new topic-based episodes in addition to the interviews. Show notes and transcripts are available at www.circuitpythonshow.com. There are links to follow the show on Mastodon and Blue Sky in the show notes. When the show comes back, I'll share it on the socials. Until next time, stay positive.
