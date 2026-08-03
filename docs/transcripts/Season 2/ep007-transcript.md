---
date:
  created: 2022-04-18
title: "Episode 7 - Alie Gonzalez"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep007.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Alie Gonzalez, who, even from a young age, had an intense passion for technology.

She taught herself how to program at the age of 10. She ran her high school's FTC competing robotics club, and while still in high school, she joined the team at AdMobilize, a computer vision analytics company as the third employee. Immediately after high school, she co-founded Matrix Labs from within AdMobilize, and for five years led the team at Matrix Labs and creating cutting-edge development boards while making guides and videos which have had over a million views.

In early 2021, AdMobilized Matrix Labs were acquired for $20 million. Later that year, Alie was honored as an official ARM innovator. She then joined the team at SparkFun, where she now leads their services division.

Alie, welcome to the show.

Alie Gonzalez

Thanks, Paul. Great to be here.

Paul

So tell me how you first got involved with being a maker.

Alie Gonzalez

Well, it was from when I was really little. When I was around five, my dad had me put together his computers, like putting all the wires in. Pretty easy, just color coordination.

But then from there, he would give me his old computers that he didn't use anymore, and I could just take them apart and do whatever I wanted with them. And I remember one old laptop, I took out, I fully gutted it, took out the keyboard from it, and then rearranged all the keys so that they'd be an alphabetical order. I was maybe, I don't know, seven at the time when I was doing this.

I'm not really sure. It was before 10. That was fun.

It was like I was really early introduced to hardware and tech. And then when I was 10, I was introduced to Roblox, back when Roblox was like three years old at the time. And now it's this huge thing.

But I was there in the beginning with the DSL connection. It didn't load very fast. We could program it with Lua.

So I started learning how the program in Lua. And it was very simple stuff. But like, that was my first.

real introduction to programming. Then from there, in high school, I was president of my school's robotics club. It was like a first competing robotics club. So I worked super long nights, got sponsors.

That was the main person working on the robot, really. And we did pretty good. We won a couple times, even though we didn't have a very big budget. So yeah, I've just always been interested in tech.

Paul

Well, that's awesome. So how did you start your professional career?

Alie Gonzalez

Well, I actually started pretty young. I went to a special high school. It was a public school here in Miami. But in our junior and senior year, everybody in the school had to have an internship.

It counted us two classes. You had to be there 10 hours a week. So I applied at a local startup that was doing computer vision running at the edge for advertisements.

Ended up getting the job. I was like the third employee. I really loved it.

I was working on Raspberry Pis. I was soldering. I was given the independence of an adult, which as a 16-year-old, was amazing. So I ended up working there 20 hours a week instead of 10 because I loved it so much.

Wasn't doing homework, but I wasn't going to do the homework anyways. So at least I was spending my time productively. And then when I graduated high school, I co-founded a company within it with the CEO of the company and with a few other cool people in the company. And that company we co-founded was called Matrix Labs. And it made dev boards for the Raspberry pie with 15 different sensors on them, and FPGA and RMCU, went on a Raspberry Pi.

We launched it on Indiegogo, and over the years, we made a bunch of content and guides and videos for it, which I think at this point, last time I checked, it was like over a million views collectively, which foggles my mind. Yeah. Yeah, I ran that company for five years, you know, learning everything along the way.

I didn't go to university. I went for a month, and I felt like I was wasting my time. I spoke to the president of the I triple E club in the university one time, and he spoke to me at first as if I was a normal freshman, not knowing anything, as most freshmen in high school.

But then I started telling him what I was doing and what my company was doing and everything. And I just blew his mind. And at that moment, I knew, okay, the university's not for me.

If this guy's a senior and doing all his things and he was doing great for himself, but if I'm already past that, why am I going to the university? So I dropped out after a month, just wanting to do my own thing.

Paul

So you ran Matrix Labs for five years and it got acquired last year and now you're at SparkFun.

Alie Gonzalez

Yes.

Paul

How do you describe SparkFund to someone who's not in the maker community?

Alie Gonzalez

Ooh, you know, that's always, that's always a hard question. So someone that's not in the maker community, I would say SparkFund makes products to make it easier for you to make your own thing. Like make your own product, make your own project, whatever it is.

If you're, I mean, if you already know what SparkFun is, you know, we make boards. We make dev boards. We make micromod boards so that you can add things to it.

And it just, we make the whole dev board ecosystem so that it's easier for anybody to do things with all the latest sensors and processors that are coming out. Yeah, it's always a hard question to answer.

Paul

It is. And what do you do at SparkFun?

Alie Gonzalez

So my role at SparkFun is the services manager. But me being me, I'm a jack of all trades and I'm pretty ADD, so I like being everywhere. So I run our custom manufacturing division, like doing, if you have your own board design, we can manufacture it for you in our U.S. manufacturing warehouse in Colorado, because we do it all ourselves for our own devices.

I run our custom kitting division. So everything having to do with like putting together our product or someone else's products in a kit so that a university or a company wanting to do a workshop, can just provide that for their people easy. And then I also run our a la carte service.

So that's a product that it's a website. You can go to pick what components you want, like what processor, with connectors, with sensors, and then it will automatically generate the board for you. So that's all under my services hat.

And then I also have a marketing hat. And that's where I run a live stream for SparkFun every month. I do content for them on the side, like in my free time, Sparkfund pays for all my hardware.

So if I want to make a cool project, which I do a lot, and SparkFund will just buy the components for me. And I just have to write a cool blog or make a cool video. So it's a pretty sweet gig.

I'm enjoying it.

Paul

That's great to hear. What's the last blog post or last project you worked on?

Alie Gonzalez

So the last blog post I worked on was actually a recap of the Miami Hackweek, which was this big event that happened in late January. It was essentially a whole week where a bunch of people, got together in different Airbnbs around Miami. The Airbnbs were sponsored by some big companies and small companies so it ranged from mansions that cost millions of dollars to, you know, like a normal house.

And each house had a theme, a lot of them were crypto. I helped organize the hardware house, the hard tech house. And then I was just supporting the teams there.

So one of the teams made a weather balloon that took a picture from the edge of space and minted that as an NFT. That team ended up winning the hackathon, which I'm very proud of them for doing. That's the one I worked the most closely with.

Another team made this really cool mushroom incubator. So essentially, like mushrooms have very picky growth cycles. You can't just put them in the same environment and expect them to grow, like from the mycelium up to the spore and everything.

They need to have like varied temperature and humidity conditions. and it varies for the different types of mushrooms that you're growing, whether it's like portobello or elephant ear or whatever. So they made an incubator with the entire sensor suite of like CO2 sensors, temperature, humidity in order to monitor the environment.

They had little humidity creators, which was basically just a little, essentially like a speaker resonating at a specific frequency, and that would cause the water to turn into mist, which is super cool the seeds. It's a really simple thing, but it's cool. They had like heaters and coolers in there.

And then the coolest thing was they had a robot arm that would go over the mushroom pod. Look, you do run some CV that they trained on like an invidia Jetson Nano. And it was able to identify the mushrooms on the field of like mock mycelium because a week is not enough to grow their own.

And then it was able to like go down and actually pick the mushroom, kind of like a claw game. So with all of these parts, you could make either like a small-scale mushroom growth area, like incubator, for your house to have, like, fresh mushrooms to eat. Or you could have like a small-scale, like, grow lab, and you can make mushrooms and sell them at, like, farmers' markets or whatever.

Just making it easier to grow mushrooms in a more, like, contained, manageable environment. Plus, they collected all the data so that as an open source, the whole project. So as you went, as different people, monitor the conditions of making different mushrooms, that data was collected and aggregated, and then they could find the best settings for each type of mushroom to optimize the growth cycles. So that one's a super cool project. It got like third place with it. A good friend of mine made it, and I'm like really excited for that one, because that has like a real utility in the world. Right. And yeah.

Paul

That sounds fantastic. Now, tell me more about the weather balloon. What kind of hardware went into that to actually lift a balloon that high up?

Alie Gonzalez

Yeah, so it was pretty simple hardware-wise. There was like an Iridium satellite uplink module. That took up most, that was most of the hardware, really. And that was able to send data to a satellite up in space to Enridium satellite. It would then go to another satellite and then go to a base station and then back to us. It also had an ESP 32 camera module. So it was an ESP 32 with a little camera and then just some batteries, all in like a case that was about this big, this thick. And the balloon itself was six feet wide filled with helium at ground level at its final altitude, which was, we estimate, like, max altitude it could really go to is like 150,000 feet because we did all the math to do it. And it would be about 30 feet applied at that altitude because the pressure is less so it expands and then it eventually pops.

Yeah, that was a crazy project. They did it all in a week, which this is an advantage of a week-long hackathon. You can do real hardware projects where you can't do in a weekend.

And believe it or not, they actually ordered everything like Monday of that week. And then it got there on time to get everything working. Yeah, that was such a grind for them.

It was amazing.

Paul

What were some of the biggest challenges they had to overcome?

Alie Gonzalez

There were a couple. So the satellite uplink, it was not clear how much it was going to cost. Their first estimate was that it was going to cost $4,000 for the uplink.

Mind you, the prize for the hackathon was like $10,000. And they were already spending over $1,000 on the hardware alone. So it was pretty rough to then spend another 4K on the satellite uplink.

Luckily, when we finally got it and we started testing it, it was much cheaper than that, but we still spent like a few hundred dollars on it. That was one problem. The other problem, the night before we were supposed to launch it, the balloons got stolen out of our car.

Paul

Oh, no.

Alie Gonzalez

One of the people lives in, I think, Ohio, and is not used to locking their car because why in Ohio? but in a big city like Miami, you need to lock your car. So they went into a gas station.

Five minutes later, they come out to the car. All the doors in the trunk is open. And like whoever stole it, like stole our two biggest balloons, plus like some a bathing suit and some socks and like a garment like satellite phone, which, okay, that was expensive.

But like the rest of it wasn't. Like, they just took everything they could. So that was nerve-wrecking attack. I was around midnight on Thursday, and we had to, like, we had a friend of mine's dad offered to, like, take us out on his boat out into the middle of the water, like, passed any type of, like, flight restrictions or flight paths because, you know, we don't want to get in trouble.

We want to do this all legally and safely. And so we were worried that, like, in some of the way. Instead of having to use helium, which is inert, and it's good and easy and safe, we would have to use hydrogen to fill the balloon.

And if you know anything about hydrogen, I'll give you a hint. It was used in the Hindenburg disaster. It's flammable.

It's extremely flammable. And imagine filling a six-foot-wide balloon with hydrogen. Like the nerd, like it's a bomb, basically.

And we were very much worried that we'd have to use it. So we just, like, over a few hours, did way more math, see if there was some way that we could just use helium, and if we overinflated the balloon maybe. So that's luckily what we were able to do.

And also, we weren't going to take hydrogen on my friend's boat. Like, it's so dangerous.

Paul

Yeah, I would think so. That's what you want to combine.

Alie Gonzalez

Exactly. Yeah, yeah. So those were like the two big issues.

It was pretty nerve-wrecking. And then we launched the balloon, like, right as they were doing the judging. And we were, like, FaceTiming so the judges could see it.

And then we rushed back to the convention area where they were presenting everything. Within, like, 15 minutes, we had to go on stage and actually talk about what our project was. And 30 minutes later, they announced that we won, which still, like, boggles my mind that that happened.

But I'm so proud of them and that we actually got. like a hardware team to win this mostly crypto hackathon. That's fantastic.

It was a good feeling.

Paul

So Miami Hack Week was sponsored by Hard Tech Miami. Tell me about Hard Tech Miami.

Alie Gonzalez

Yeah. So Hard Tech Miami is an organization that I help run. It wasn't founded by me, but I was one of the founding members of it.

And essentially the idea of it is to bring together hardware and deep tech people that are in Miami, but also from other areas of the U.S. or globe even. And bring them together, have to develop this community here. So it's not just crypto in Miami. Like we do real hardware things, real AI, machine learning things here. And there's a lot of companies already doing it. It's just they're kind of like in the dark. Like the engineers don't come out of their offices or homes. So we're getting more people engaged. And then we're getting people to move to Miami. Like in the hackathon, the entire team that did the NFT balloon, they're all moving to Miami.

Some of them are moving to Miami in the next month, and they've all gotten, or three of them have gotten brand new jobs making way more than they ever imagined, thanks to the hackathon, which is such an accomplishment. And I'm from Miami. I'm native to Miami, so bringing people here, getting tech people here, getting people interested in the things I'm interested in, it makes me so happy, and it makes me so happy to see the city itself growing and maturing and actually being more than just a party city like it's been known for the past 40, 50 years.

Paul

Well, that is an added benefit to moving to Miami is the weather.

Alie Gonzalez

The weather, totally. It is currently 73 degrees at this time today in March. And then, yeah, it's nice.

The weather is very nice. There's tax benefits. No state tax.

You save 8% or more, which I'm not complaining about. COVID regulations are kind of loosey-goosey that has its pros and cons. I won't get into it.

But it has its pros and cons. So, yeah. And there's just so many people, like, it's buzzing.

Like, there's daily tech events. The community here is really nice. Everyone's happy to talk to you and, like, support you and make become friends.

And it's a really nice atmosphere. I'm really proud of it. It doesn't, it's not, it's not, it doesn't feel like the old Miami where it was very, status driven.

That's not what the tech ecosystem is here. Makes me happy.

Paul

Well, that's great to hear. Yeah, there's definitely a lot of buzz that Miami is one of the hit places to be in tech right now. Yeah.

Well, we're running out of time, and before we do, I like to do a segment that I call Turn the Tables. I'm a big vinyl record fan, so it's kind of an in-joke for me. But I like to turn it over to you.

You can ask a question of me that I get to answer.

Alie Gonzalez

Totally. So, hmm. So I love hardware, and I've done some things with CircuitPython, but I've also heard a lot about micropython. So what's the difference between the two? Why should I use one over the other?

Paul

So there would be no CircuitPython without micropython. It's a derivative, and it's a fork. So everything that CircuitPython does is built on the backs of giants already.

CircuitPython, I think their goal was to be a little more simplified, easier for learners. Some of the other key differences is it had to have native USB. I'd be able to plug it in and it had to show up as a circuit pie drive, though that's starting to change a little bit.

And then the code's got to run as soon as you save it, which is a little different than Micropython as well. But syntactically, they're very close, very similar, but I think the audiences are just slightly different.

Alie Gonzalez

Got it. Okay. Yeah, CircuitPython seems more approachable.

Paul

I would agree with that. Last question I have for you is you're starting a new project. Which microcontroller are you going to reach for and why?

Alie Gonzalez

Oh, that's a good question. Lately, I have been really into Spark Fund's thing plus line, especially like with ESP 32s, but I've been really wanting to dive into the RP 2040. I have a few Raspberry Pi Picos here. I like how small they are, like great for wearable applications.

And they're cheap, so I can just throw them into whatever. So, yeah, I'd say the RP 2040. And it has an arm processor, and I am an arm innovator, so I've got to rip arm with it.

Paul

Yeah, you can't go wrong with an RP 2040. Yeah. Thank you to Alie for being on the show. You can find Alie on Twitter at Al-I-E underscore G-G. This was episode 7, recorded March 3, 2022.

Speaker 3

For show notes, transcripts, or to support the show, visit CircuitPython show.com. Thank you for listening, and until next episode, stay positive.
