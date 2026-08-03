---
date:
  created: 2025-01-27
title: "Episode 38 - Building a weather system with Jan Goolsbey"
---

## Show Notes

[Show notes available here.](../../episodes/Season 5/ep038.md)

## Transcript

Paul

Welcome to the CircuitPython show. I'm your host, Paul Cutler. This episode, I welcome back Jan Goulsby, also known in the Adafruit community as CGrover.

Jan first visited the show back in episode 33, which I've linked in the show notes. Jan, welcome back to the show.

Jan Goolsbey

Hello, Paul.

Paul

How are you today?

Jan Goolsbey

I'm doing great.

Paul

Thanks for making time and coming back on. I really appreciate it.

Jan Goolsbey

Well, I enjoy the discussions with you, and I'm looking forward to this one.

Paul

I am too, so you've been working on a while. weather station for a number of years. Tell me how it all got started. Well, it got started many years ago.

Jan Goolsbey

When we moved into this house, we have this detached garage that I call my workshop. It does have an area set aside for that. And I brought a collection of my electronics projects. And back then, I wasn't doing a lot of software. It was mostly hardware. So I had, you know, an IBM 5150 personal computer. I had Intel 80 parts and resistors and capacitors, you know, the whole thing. And I was throwing them out in this detached garage we have in the workshop that was unheeded. And I noticed after about a year, components started to decay. And especially the metal leads like on integrated circuits would get this corrosion layer on them. And it made it really difficult to solder. They didn't work in the sockets anymore. And so I was getting a little bit to I also noticed some damage to my metallic tools, you know, things like wrenches and screwdrivers.

We're starting to show some corrosion on the outside of that. And I never thought that would happen because we live in the desert here in Washington State. You just don't expect that to happen.

But we have wet winters. You know, even though we get less than six inches of rain in a year, it happens in the winter, and that's when things are colder, and that's when condensate forms. Well, you get the drift there.

I was needing to upgrade the garage so that I could store things out there and work on things out there without worrying about corrosion. So I get this new obsession. The new obsession was, how do I solve this corrosion?

So I did some reading about it, and the first thing I needed to do was measure temperature and humidity, and that was really where it all starts. And if you can determine when condensate forms, then you can probably, be prevented. And that's really what I wanted to do. I didn't want to put a heater out in the garage right away. I wanted to figure this thing out first. So that's where this started. And fortunately, about that same time, Micropython came onto this scene. And Tony DeCola was working on putting micropython on some Aetreut M-Zero boards. And I thought, well, this is perfect. I'm okay, you know, I had done some Arduino programming. But Arduino doesn't work with my brand. I'm a hardware guy and so I had to do compiling and all this kind of stuff. Yeah, I know how to do that, but that's not the fun part of it for me. So I wanted to get something like Micropython where I can very quickly put together in prototype, start to characterize what the temperature and humidity issues were and see if I can solve this corrosion problem. And Tony did some great work with getting Micropython introduced in some ATA proof boards. And I, at the same time, Lady Ada came up with a board with an RF transmitter on it.

It was the RFM 69 and 800 megahertz transceiver that could send and receive little tiny data packets, you know, 10 to 15 character data packets. Nothing fancy, nothing fast, and I thought that's perfect because I just need temperature and humidity. And since it's a detached garage, I didn't want to have to go out there and read the display all the time.

So I made a little unit that was an M-0 RFM 69 built into it, put micropython on it, stuck it out in the garage, transmitted it to a tiny little remote that I made with an OLED display. All I did was I just watched temperature and humidity, just to try to figure out when this erosion occurred. Meanwhile, I'm doing some studying because when you get that data, well, what's the first thing you do, at least for me, throw it in a spreadsheet, start looking at things like DuPoint and the capacity of the air to hold moisture, and all the kind of stuff that leads to corrosion.

I started to refine the software to convert the humidity and the temperature into something that looked more like an index that was related to whether I was experiencing a corrosion event. I was hoping to get to the point where I could predict when a corrosion event. That took me to the next phase of the project.

The next phase of the project was setting aside that RFM69 and M0 and go to more of an internet solution where I put a pie portal out in the garage and with the same temperature humidity sensor, transmitted the data up to Aetafruit I.O. And you know, you've got a great browser-based dashboard tool that I could use to look at the data and compare and get some feeling for even deeper feeling into how to solve this corrosion issue. And by about that time, I figured, well, I better remodel this garage.

It was built from surplus government lumber. The whole garage was, it was very functional, and it was retro-fantastic. It was raked.

Matter of fact, a friend of mine came out and filmed a short video in there about time travel because they needed a workshop that a crazy scientist would use, you know, to build this time machine. So they filmed the time machine portion of in my workshop. And the next week was when I had the crews come in and tear down the garage and put up a new one and build on the same footprint, build the garage.

And PyPortal was perfect timing for that. And I also put in a heat pump out in the garage. Because what I had determined by then I was using CircuitPython with the PyPortal, I determined that even though there are some complex equations for figuring out how much moisture there is in the air and how it forms.

and there are some standards for when you can expect certain kinds of materials to corrode. It really boiled down to keeping the garage above 32 degrees. And that way you avoid the condensation that obviously occurs when things free.

And as long as you keep it at a comfortable temperature, somewhere above 32 degrees, you can pretty much avoid corrosion issues. And so if we finished the remodeling, we got the pie portal out there, I'm watching the data, And we had this great snowstorm, and I, you know, back the car back into the garage next to where the workshop is. And about 15 minutes later, the corrosion alarm goes off, and I brought moisture into the garage that wasn't natural.

What happened? And the snow melted. We get this corrosion event, and that created a whole new set of concerns for me.

Now, how do I get rid of the moisture in the garage? And thanks to CircuitPython, I can modify the pipe. portal monitor to give me the data that I need to look at different algorithms for solving these problems and prototypically almost immediately you can study the data change the algorithms and completely change the functionality of the monitor to suit your whole new set of theories about how you're going to predict and prevent these things. Well since I was in the problem solving mode there needed to get rid of the moisture in the garage that's when I determined there's a really tight link between internal corrosion and external corrosion.

The data and the conditions that can cause internal corrosion are driven by the exterior weather conditions, as well as the heat pump and all those things. It got me thinking about how do I incorporate external weather conditions with the internal workshop conditions and get a better feel for how I can prevent and how I can meet, even in this case, mitigate the collection of the moisture in the workshop. That's when I started going down this path of taking a look at openweathermap.org because they have a free weather condition service for local conditions.

And that worked pretty well. I had one device that looked at the external weather and one device that looked at the corrosion monitor stuff. And I went between the two and started to try to make correlation between those.

it became rather difficult to do that. I had spreadsheets and I couldn't correlate the data very well because I couldn't collect it in one place. That's when I had the idea of uploading the weather condition data that I was getting from openweather map.org into AIO, so I had streams that would show up on my browser dashboard.

And then I could start mapping one temperature set against the other and make a determination in weather. what the relationship is between inside and outside conditions. So I knew when to open the garage door, turn on the fan, and blow the moisture back out into the environment.

Which doesn't work, by the way, when it's rained, because you can't fit any more moisture in the outside air, which makes sense. Good to know. Yeah, I'll have to write up this whole corrosion monitoring obsession one of these days.

I'll let you know when that comes about. I'm having too much fun programming what I'm working on right now. And what I'm working on right now is this evolution of that into a combined weather system that looks at internal sensors, specialty sensors that I might have locally and weather conditions.

And it was kind of all spawned by this AIO collection of the data feeds and the way that I could look at that. So I've worked on an architecture where I can upload that data, where I can bring it down to devices. And I got to the point where I could put it in, I could take all the data and put it into spreadsheets or make comparisons, but I had the collection of the data from the two sources.

And that whole thing was working fine. And I was learning more about how I'm going to do this corrosion monitoring, how I'm going to set these alarms, and there's still work to be done. You know, a wrench got thrown into the works, and that was OpenweatherMap.org decided that they were going to start charging for their service, and I can't blame them. It's a great service. But the model that they used was, at least the time when I was making a consideration, I don't know if it's changed. They required a credit card to be able to get data from them, even though they called it a free service.

And, you know, I'm just not trusting enough to give somebody my credit card and say, here's a blank check for you. You know, and I thought, well, I'll just look for some other ones. And I ran across weather.gov, which is a NOAA service, the National Oceanic and Atmospheric Administration there. I knew I figured that one.

Noah had this really great service that had this fantastic detail of these weather stations that were really close to my home. And I thought, this is two miles away at an airport that's real close by here. They had a weather station. I thought, this is perfect.

It's not just some consolidated weather data that I might get from open weathermen. out, which they do a good job, but they average weather stations in the area to come up with their number. I thought this is going to work great.

Well, what I found out was these little tiny weather stations, and they have peppered all over the place, if you just look at one of them, it's not very reliable. And I thought, okay, well, that's fine. I'll just go, I'll do what OpenWeatherMap.org does.

I'll look at 20 different weather stations, and I'll average the day in. And you can imagine I'm taxing CircuitPython pretty significantly. I'm trying to do this on a pie portal with an M4 processor even though it has a separate ESP 32 processor on there the M4 just doesn't have enough memory to do all that internet downloading all the JSON files that are necessary decoding that and then of course I kind of went nuts and I needed a fancy display and that eats up memory too and the poor little pipe portal was just suffering.

Pretty soon I found that that would be an impossible task and I really didn't know where to go from there. I didn't want to have to go back to openweathermap.org, although that would have been a viable solution. I was pouring through some AETFruit IO documentation because I'm trying to solve some of the reliability issues I was having using the M4 and memory capacity issues.

And I found out that there's an Apple Weather Kit Plusup in AIO Plus that I hadn't realized it was there. And I've been using AIO Plus because you know I have lots of AIO feeds. Because I have lots of data sources.

So I was already paying for this, but I just didn't realize that this busup to the Apple Weather Kit was out there. And it gives an open weather map kind of view of the world, including five-day forecasts and, you know, some data that I wasn't using that could be very useful. This is a no-brainer, which is going to go with that.

And that's where I started to think about this collection of data that I had as an architecture. Since I was facing that choice of determining where the source was going to be for this weather data, I got about a dozen pie portals. I needed to make it compatible with that.

That's when I started to develop that architecture. And version one of that architecture is in an article, it's documented in an article out in Avaigr playground. That was something that the objective of that architecture was to get the two weather conditions, you know, the internal and external weather condition data into a single place.

But it was also to try to preserve the pie corals that I used for displays. Since they were limited, I had to try to find an architecture that could support the need for the pie cordal to have a bunch of data, but keep it from having to go out to the Internet and get it. get these gigantic data files, JSON files, and decode them itself.

They just couldn't do that. And so the first architecture was designed to take care of it.

Paul

So what were the challenges with the first architecture of the weather station?

Jan Goolsbey

Well, let me recap just for a second and go back to the zero architecture was just a point-to-point thing with that 2-8 radio kind of a setup. And then, you know, I saw the obvious need at that point to use AIO. So the architecture became more AIO-Centure.

And then I started gravitating to the PyPortal, and that's kind of the nexus of the issue. And when you work with the PyPortal, you have a lot of overhead contained in the drivers that make the PyPortal easy to use and easy to program. But if you're trying to expand and take in a bunch of feeds, and I had a lot of AIO feeds, of course, you start running out of memory with that M4 processor.

So I got to the point where I saw the need to do something different, and yet I still tried making an M4 work. I bumped up against their memory all the time, and I got rid of some of the fancy graphics and put in some more pedestrian stuff, and I just wasn't very happy with it. So I came up with this idea that I needed to modify the architecture so that I could still look at weather data.

And the other goal was I wanted to continue to use the M4s, the pie portals, but be more sensitive to the memory issues and some other issues that they have so that I could still continue to use my investment in pipe portals because I have many of them. But I needed to move to something. And I'm very reluctant to move to something new because I had it working, I thought.

And, but also I'm cheap and I'd like to use the pie portals wherever possible. I struggle with the notion that once you write some software, you make it as good as you possibly can, and you shouldn't ever have to change it, which that's a myth. And so I get trapped into that often.

And I try to talk myself into a philosophy that I learned a while ago when I was making printed circuit boards. Yeah, it's okay to start from scratch. It's okay to start over.

You probably learn something since the last time you coded that, and it's okay to recode it, and you'll probably use something better than the time around. So I decided, well, it's time to move to a new architecture because of the limitations and the pie portal predominantly. I wanted to have multiple display devices.

And the first architecture was kind of funny, the way I tried to synchronize all these asynchronous devices. If you have four or five displays, they're all accessing AIO, you run into the throttle limits of the AETAPUD IO. And if you have a free subscription to AIO, you're limited to 30 transactions per minute, which, you know, doesn't sound like a lot.

And it isn't when you have multiple devices. Fortunately, I was using AIO Plus, and I had the limit of 60 transactions per minute, and, you know, double that other rate. And I certainly appreciate the fact they're trying to give this service to a whole bunch of people, and they need to throttle it that way.

So I would go to each one and in my devices, they'd say, okay, the corrosion monitor, you can go out to AIO at 10 minutes past the hour, get your business done. And then the weather monitor can go out to AIO and extract weather information at 15 or 20 minutes past the hour. And the second weather display, the one for the, yeah, the second weather display that I have that's in the living room, is a matrix portal.

And I said, you can go to 20 or 30 minutes past the hour and get the data. And you can only go out there every 20 minutes and get the data. I had this really complicated formula trying to synchronize all these devices that were, that I wanted to be autonomous.

And it just couldn't do it. Because if you ever had an internet error, if you know what. what those are, which we have a few, the wireless connection would break or something, and then the device would have to re-synchronize and it would petrodine with the other devices, and you'd still end up with throttle failures.

And I just didn't know how to fix that. Well, I think Brent and Tyet, who do the development work for AETA in the AIO realm, they came up with a really simple scheme for providing throttling information, And then I thought, well, I tried everything else. Let's try this and see if we can make work.

And I hesitated to try their new scene for throttling because I figured it would be way more complicated than what I could do. I'm not an expert programmer. And I thought, I ran into so many troubles trying to synchronize anyway that this throttling stuff is going to be a scheme that it'll take me a while to learn how to do.

That was wrong. It was so simple.

Paul

That's a good problem to have.

Jan Goolsbey

It was surprisingly simple, and I should have known better. I should have checked it out and played with it. Well, anyway, I know better now.

But Tyap did most of the work on that, and it's just brilliant what he did. It's brilliant. And I put in, you know, one or two extra lines of code whenever I had to go out and do something with AIO.

And all it did was it did a query, and it says, how much throttle do I have left? And that's all controlled them by the server rather than by my devices. and my devices is just wait until there's enough throttle left to do something.

Paul

So Adafruit IO actually has part of the API that you can query it to say, how many throttling requests do I have left in this minute?

Jan Goolsbey

Yes, and surprisingly, that going out and querying how much throttle you have left doesn't seem to affect your throttle limit, which is, you know, that's a real plus. So whenever I have a transaction with AIO now, I go out and check that throttle. That forced me to go to a new architect.

So I have an architecture version 2 that I put in place. And this is, the version 2 is called Remix, and it's out in the Playground. If you're interested in it, there are two articles that I wrote Playground.

One is the structure of the first architecture, and the second is the structure of the second architecture. And it also gives the code examples.

Paul

And I'll make sure I link to those in the show notes as well.

Jan Goolsbey

And I welcome as many comments that I can get on that because I'm hoping that I'm using a throttling correctly. It seems to work because now with the second version of the architecture, I've tested it with six devices. And four of those are pie portals.

One is an ESP 32 S3 repeaters, what I call it, but it takes the place of the corrosion monitor out in the garage. And it picks up the Apple Weather Kit information, translates that, and moves it back into AIO feeds that I can then access with PyPortals, and I'm only getting that small chunk of data that I need rather than the old JSON file. So I can get the pie portals to continue to work because I limit how much data they get when they're accessing AIO.

They don't have to get the whole thing. They only get what they need. So I've had six devices running with the new throttling stuff, and it's just been flawless.

The only errors I have much more related to, you know, my need for fancy graphics and things like that where I ran on memory. And that, you know, that's a personal issue that I'll just have to resolve somehow.

Paul

Well, tell me a little bit about the interface, because I've seen pictures, and I think most of the listeners would be interested in knowing more about it.

Jan Goolsbey

Right now, there are four different user interfaces that I use. The corrosion monitor, even before it came into this new architecture, was an Elkhars Star Trek style interface. It isn't touch-sensitive or anything, but it still uses that feature.

And it's built very similarly to the displays that they actually use, not necessarily in the code or the graphics design, although that does kind of mirror it. But it uses a layered graphics approach. So the background image has all of your indicators in it, like I'm using the Internet now, or I'm going out and looking at my thermometer, or I'm using the SD drive to store information for that wonderful spreadsheet that I always keep track.

And you cover those up with masks. Instead of drawing the object like an antenna or wireless app says, that's in the background, and you just cover it up with a colored square. So the interface really is kind of graphical, reminiscent of the L-Cars, and it uses some trickery to make that work, which is a little stage magic, which I think is kind of a nod to how they do things on Star Trek, too.

So that's the corrosion monitor, and that has been modified somewhat in this coming to the new environment. The weather monitor was one based on something that John Park did quite a while ago on the PyPortal, And I've adapted it and changed the graphics a little bit. We call it Mikey because our local weatherman's first name is Mike.

And I recorded a snippet of his voice introducing the fact that we've turned the weather monitor on. So every time we turn it on, we get our favorite forecaster telling us that he's going to give us the wind.

Paul

That is pretty neat.

Jan Goolsbey

The other interface is the Matrix Portal Weather Stinction. And I used an M4 initially, but there again, I started to start a weather. running in performance problems. So I switched that one to the Matrix Portal S3. So it's a fully capable ESP 32S3. Lots of memory available from goofing around with graphics and doing things.

Technically I could download entire JSON files and things like that, but I still kept it in kind of a simple display, and it shows an abbreviated version of the weather. And then in the scrolling bar down below. It tells us what the wind is gusting to. It tells us what the shop temperature is and it scrolls by. We find that one probably to be the most useful out of those interfaces, the first three interfaces.

And the fourth interface is one that I'm not happy with. Well, it kind of looks like a Raspberry Pie booting up. It's just text. And that's the translator that sits out in the garage. And I really need it to be more of a clock.

And I need it to, well, frankly, I needed it to look more like an Elkhars interface. So the next version of that, which I'm working on right now, and I do have a link and some pictures in that second playground article, it shows a more expansive Elkhars interface, and it combines the external weather with the internal shop conditions in a single display. It can either be used as that repeater that translates data and sends it back to the AIO, or it can be used as a standalone display.

That's the up and coming for it. Will there be a modification to the architecture? Well, I don't sit still on this stuff, so probably a version 3, but right now I need to perfect that new L-cars interface.

And that's running on a, let's see, that's running with a 3.4-inch TFT feather wing with an ESP 32S3 feather plugged into the back of it. So it's kind of like a pie portal, which I dearly love, but it's not yet a pie portal. I hope in the future to add some other bells and whistles to it so it has sound because we've got to get mickey and talk.

And also, I like to, when I put these in an enclosure, I like to have a temperature sensor in there that monitors the temperature inside the enclosure. In case here in the desert things get hot, you know, and you've got to turn on the fan inside the enclosure. and those are things that I need to add.

Paul

Is there anything else that comes to mind for what's next in the project?

Jan Goolsbey

Of course, I'm still on that journey to figure out how do I adequately predict corrosion? What weather changes outside and conditions inside, including, you know, back in the car and that's snow wall over and under it that's going to melt? How do I predict when that corrosion events going to occur?

And there's some science in that. And, you know, right now I focus on dew point. Because dew point seems to be, you know, that's a magic number because that tells you when the air is saturated with water.

The temperature at which the air gets saturated with water is the dew point. Well, that tells you a lot about corrosion because if the air is saturated with water and you have something metallic that's a little bit colder, it's going to condense water on that right away. And if you compare internal dewpoint to external dewpoint, that tells you a little bit about the other condition I talked about work.

If I want to take the water in the workshop and push it outside with the fan, is there a room outside to accept that moisture? And DuPoint can tell you some of them. It's not a true measure of capacity of the air outside, but it's a pretty good indicator, I think.

But what I struggle with is really gaining an understanding about, you know, how much moisture do I have in the workshop and how much moisture can the outside tolerate it? How much can I give? So that's the next step is to do a little science and try to figure this thing out.

And then you would think that would be enough. The natural extension is, now, how am I going to use the features of AIO to control the Internet-connected heat pump? that's in the garage so that I can have it automatically abate it while I'm sitting on a beach soon.

Paul

Sure. Well, a good project is never over.

Jan Goolsbey

No, I'll find something.

Paul

Well, that's fascinating. I appreciate you coming on the show.

Jan Goolsbey

I appreciate you letting me talk about this because I really like the feedback that I get. And there's one thing I need to add to this besides thanking you for the opportunity to have these discussions that I really enjoy. I would like to thank, of course, Tyeth and Grint for the work that they've done on AIO to make it so easy to use.

And for adding all these features in AIO Plus like, you know, Apple Weather Kit that I'm using now. But I also like to go back to like the first architecture that I put in place with the two-way radio kind of set up. That was made possible by a lot of work that Tony DeCola did because he introduced micro-reaching.

Python into that environment very creatively and made that really useful. So I appreciate all the work that he put into that and the leadership that he had shown back then to see the possibility to put Micropython on these little devices. And of course, the evolution of CircuitPython has just made them even easier to use.

And then Jerry Ann, Jerry Neal, he was a developer for Apple back in those days. and I think he's a part-time developer now. Jerry N. is his handle on Discord.

He did some really breakthrough work in getting the to-a-radio drivers for CircuitPython. And those were game changers for me that got me into this whole rattle that I'm traveling through now and having fun with the corrosion bond.

Paul

That's great.

Jan Goolsbey

So I want to thank those people. You know, the community has really been supportive of all these things and giving me lots of suggestions and ideas. And so I appreciate that.

Paul

I'll make sure I share the learn guides in the show notes and hopefully you'll get some more feedback from it.

Jan Goolsbey

That's super. It's something I look forward to.

Paul

Jan, thanks so much for being on the show.

Jan Goolsbey

Oh, you're welcome and thanks for having you.

Paul

Thanks to Jan for coming on the show and sharing his weather station, its architecture, and how CircuitPython and Adafruit I.O. Plus have helped his project. And remember what Jan said.

If you have any feedback after listening or looking at it, at the project on the Adafruit Playground, let them know. For show notes, transcripts, and more, visit www.com. com.

Until next time, stay positive.
