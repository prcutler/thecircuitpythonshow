---
date:
  created: 2022-08-22
title: "Episode 16 - Brent Rubell"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep016.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Brent Rubell.

Brent is an engineer at Adafruit Industries and a graduate student at the University of Massachusetts start with. He works on all things embedded, but especially devices which connect to the internet. Brent has worked for Adafruit for five years, first in the Adafruit factory within the PCB fabrication department, as an intern, and currently as an engineer.

Brent, welcome to the show.

Brent Rubell

Thanks for having me.

Paul

Let's start at the beginning. What is your origin story? How did you first get involved in computing and electronics?

Brent Rubell

Those are two completely separate questions for me because they take different forms. Computing, I got my first computer. I'm not very old. I'm 26. So I've listened to previous backstories of people and they're like, oh, I started on a mainframe, but I started on a Dell dimension to Pentium 4. I upgraded the GPU as much as I could really. And then for programming, I got into it via scripting for Flash games. So I basically wanted to cheat at them. But I I also didn't realize I was learning as I was cheating.

I used a scripting engine called cheat engine and I let you make these things called trainers for games where you like manipulate the memory of certain things. So like if you want unlimited health, you would essentially like freeze the memory address on the health bar and then it wouldn't move. Or if you wanted to increase a value, you would like increase the memory.

Before I knew how to even program really like how to find the things I'm looking for within like an application. And then I got into program. programming more so in like junior high to high school and then more and more and more in college and got into Python as well via scripting things I wanted to do. And then I had familiarity with it when it came time to actually apply it to work.

Paul

So you're currently working at Adafruit on internet of things. What does IoT and the internet of things mean to you?

Brent Rubell

So to me, like the IoT is a way to link physical objects to the internet. So physical objects can take entertaining electronics in them. So either some type of instrumentation, like they'll have sensors that will report data on the physical world, like a weather station, or they could also report data on the device internally, so like the device's battery, or actuators, so things like motors or LEDs that interact with things in the physical environment. And then those things, like the things on the internet are networked and like the internet to network. So they send and receive data either to or from the internet itself or an application on the internet or gathering data from other devices or they talk to other devices. So it's best described as a network rather than the internet because it contains like kind of nodes and graphs between devices and things.

Paul

That makes a lot of sense. Adafruit's known for a lot of those products, but they also have an internet and other thing service, kind of like what you were touching on just now called Adafruit I.O. Tell me about that.

Brent Rubell

Adafruit IO is a platform. I started working with it in 2018, but it's older than that. It's a service and a platform that is used to simplify connecting things to the internet. So specifically, Adafruit looked at existing solutions when it was made and decided they'll write their own that has a lot of simplicity in what it does. And then they also wanted privacy and user controllable privacy, which is something also important.

in the internet of things. So it's a platform that you can send data to the Adafruit I.O. server and it can be displayed on charts. You can interact with the data with dashboards.

You can click a button in your device will do something. But you can also send values from your device to the service to have it graph, to have it stored, and you can download the data. You can destroy the data. It's your data and it's your devices, pretty much.

Paul

I've seen some really neat learn guides that show how to use Adafruit I.O. I think you might have actually written a few of them. Are there any that come to mind that people should check out or any user-created projects using Adafruit I.O. That you've seen that kind of highlight what it's capable of.

Brent Rubell

The COVID lockdown period was definitely, or shut down however you want to view it, was CO2 monitoring was really hot during that time. And then any type of gardening project, like Adafruit sells these capacitive soil sensors. So using those to monitor plants and people were starting to grow stuff at home.

and like kind of explore that they had a backyard. And those guides are always interesting, especially due to, like, anything of this physical process is interesting to me because a lot of like the physical world is modeled better with the internet of things. And Adafruit I.O. has a free tier.

Paul

Is that right?

Brent Rubell

It does. There's two tiers.

There's a free tier and it's like 30 data points a month. And you can have like on our services, you can have two devices, connected through the Swipper-Snapper firmware that we'll probably talk about. But you can only have 10 feeds.

And then for $10 a month, you can have more data points per minute. You have unlimited devices, unlimited dashboards. The only thing that's limited is how often you can send data and receive data with the service.

I think that maxes out about 60. Request a minute? Yeah, it maxes out at 60.

And then you can actually boost that value per month via, like we have a system called boosts. So it doesn't get you up to the data rate of something commercial like AW. US IoT or Azure IoT, which are really meant for commercial applications of IoT projects that have fleets of sensors, right? Like, Adafruit I.O is meant as an experimentation platform, not as a commercial platform.

Paul

And if someone is looking to get into Azure IoT, Liz Clark just published a guide a couple of weeks ago on how to do that as well.

Brent Rubell

Yeah, it's a great guide. I wrote the library, like, originally for work, and then Microsoft came along and, like, did a really good pass over it. and sleeped it, and Liz is like taking that and ran it even further, and I'm happy to see that.

Paul

That's awesome. You mentioned Wippersnapper. It's a new firmware. For someone who's never heard of Wippersnapper, what is it?

Brent Rubell

It's an application written for Arduino. It contains basically everything you need for your board to communicate with the internet. And specifically, it communicates with our Internet of Things platform called Adafruit I.O. And it allows your hardware to be controlled from the internet and configured from the internet. and send values to the internet. And this is all no code, no programming involved, and visual on a website.

Paul

For the no code solution, how do you define no code? What are some of those building blocks someone might see on a web page? Can you walk me through that and help our listeners understand?

Brent Rubell

Yeah, sure. So there's a few different types of like solutions for programming, right? So there's straight programming, which is text-based, and you type into a computer, and it's either compiled are interpreted, so like Python or C, in that reverse order. And then that code produces an application. There's another way to produce code, which is no code, which is starting to gain a little bit of popularity. There was a few articles around it in the Times. And no code, the gist of why it's interesting to me at least is it increases the amount of people who can make and develop software applications. So these are people who never learn programming, but want to build something. And when I was teaching a class a while ago at New York City, resistor about CircuitPython, actually, somebody working there wanted to create a monitor for their, they were a construction worker, and they wanted to create a monitor for their construction site to track, I don't remember, but they wanted to track something.

But the intricacies around doing an Internet of Things project versus doing a regular embedded project were too much. So this is something for scientists, students, people who are wanting to build something, but may not have the knowledge base. Like, the internet of things requires a huge knowledge base, right? Like, you need to know web development and some level.

You need to know how you're going to send the data to the internet. You need to know what type of data you want to send. You need to know what you're actually sending. And you need to be able to display this on the web somehow. So, like, that is a huge swath of like computer, electrical engineering and computer science. And it's difficult. So this like no code solution through Wipersneper and Ataford.I.O. is designed to be super simple for people who couldn't build these types of projects before or stopped on these types of projects because the level of complexity was too much.

Paul

Is there a hope that they might transition into something like CircuitPython or learn programming from them?

Brent Rubell

Yeah, I hope so. Back when CircuitPython was first introduced to me, one of the like I guess pitches for CircuitPython was that a student would be able to purchase a board and maybe use midcode and then they'd be able to like graduate I guess so to speak to CircuitPython then they would be able to use the same board and graduate to see so this is once again like using the same development board that they're comfortable with using and then they can move to a more like if they want to add features to it or low power modes to it or other like they want to calculate a rolling average on a sensor measurement that they can't do in Whippersnapper, they can move this project to CircuitPython, but at least they proved it out, and they started to gain familiarity with the hardware and what it's capable of, right?

Paul

So the Wippersnapper firmware runs on about a dozen boards right now. I think Wi-Fi is probably one of the requirements. I had an ESP S2 lying around, so I hooked it up, and it's pretty neat.

You have the ability to update the firmware right from the web page. And then you can add, I think they're called actions or components. You need to add a component first.

So tell me about how you, once you've got the board and the firmware installed, how do you add some of those components? And then how can you add them to a dashboard on Adafruit I.O?

Brent Rubell

Yeah. So once you have your board set up, generally when people build projects, they'll have something in mind that they want to build. So hopefully, like, or they'll have some parts left over from a previous project.

You essentially can add components visually. by clicking, and these components need to be physically plugged into your board. And if they're physically plugged into the board, you can click on add a new component from the website, and it will drop down this whole parts list of all the parts that are compatible with your boards.

And we have, like, nice 3D renders of everything, and we also have pictures of them. And while some things are similar, like you and I both know that a button and a switch are both digital input components, they will send a Boolean. value 1 or 0 if they're open or closed, the target audience for whippersnapper might not necessarily know that. And like an absolute, absolute beginner, like we're talking about somebody who has the part on their desk and is looking for what to hook it up to, we'll look at the part picture and say, this is what it is. So it kind of like looks like a video game inventory and it's supposed to. You're supposed to visually identify the part with what's on the project.

So you click that and you click create component. And what happens when you click that button that says component is the website over Wi-Fi sends a command over a protocol called MQTT, and it tells the board basically, hey, I would like to create an LED on pin 13, and the device will execute a command and create that pin. And then the dashboard will show that pin's been created, and you can interact with it.

You can turn it on or off, or you can read data from it, if it's an input pin, I guess.

Paul

Wippersnappers currently in beta, are there any big gotchas that people should be looking out for if they try and test it?

Brent Rubell

Every little piece of feedback, especially when beta, like as far as user interactions, buttons being in the wrong place, software crashing, software doing unexpected things, typical beta things I'm interested in. There's nothing that at this point, there's nothing that's super limited. There are some peripherals that are in the pipeline, like one wire for the Dallas semi temperature sensors and then Neopixel dot star API is Servo API, display API.

So there's things that are like still being worked on, but generally the service itself is like the features are there for somebody to start working and experimenting with it. And it'll just improve over time. Where do you see some of those improvements going next?

Sometime in the spring, I wrote a few guides, and I wrote a guide for adding a new board to whippersnapper and then adding new components. And I saw a community contribution go by earlier. So a lot of the model for this is definitely taken from the CircuitPython project where we have this open source firmware for CircuitPython and parts of the web application they can interact with.

So each component that you'll see in the component pickers actually JSON file and their data-driven. files, which means that if you go into the repository and you add a new JSON file, it will actually add a new component to the website. So this is a way of opening Adafruit I.O. up to user contributions that aren't impacting like the application is quite big, but these are the types of contributions that would be beneficial for Whippersnapper. So I'd like to see more community contributions as we start to head out of beta, increase sensor support as we head out. Maybe every sensor Adafruit makes would be pretty cool. And externally submitted sensors, like from companies that aren't Adafruit and boards that are from companies that aren't. And I also want to do low power mode sometime in the summer. I think that's very crucial to IoT projects.

And I think that over the last two years, like Webbersnapper is a pretty cool interface for configuring a device and then sending it into low power mode. And that's kind of what I want to do.

Paul

Internet of Things projects are really hard, and finishing projects is really hard. What advice would you give someone that's starting or trying to finish an IOT-type project? I mean, the simple answers get paid for it.

Brent Rubell

Right? Like, the more pressing answer is like, how do I finish project? And the stick-with-itness is, like, crucial to finishing an Internet Things project because there's so many different layers associated with these projects.

It's not a typical electronics project where you'll revise a PCB, but you'll maybe revise the software as well that runs on the device, and you'll maybe revise the interface on the web or the mobile app that the device connects to. So getting it to a good enough point, I think is important. And then everything can be made faster, like, especially even as we worked on Wippersnapper, like it originally wasn't as quick as it currently is.

It takes time to revise. Maybe you want to use a faster communication protocol. Maybe you want to change the communication protocol.

Maybe you decide Wi-Fi doesn't reach long enough and you want to use a different transport. Getting the project complete is important and then revising it after I've always felt is the way to go for finishing projects.

Paul

I couldn't agree more. When we were preparing for the podcast, it turns out that we both have a love of newsletters. And I'll make sure to put some of these in the show notes.

But I wanted to ask you for just a couple. of your favorite newsletters and they can be on any topic. I'll give you three.

Brent Rubell

I won't plug the one I work for until the fourth one. That'll be the secret one. So I hit open on three newsletters basically every week.

I was trying to think of like three I continuously hit open on. One of them is the prepared. If you're an engineer, I can't recommend it enough.

It's written by multiple authors and usually changes every week or every few weeks. So like a civil engineer in architect, people who are really into bicycles, people are into environmental city design and has like news analysis vectors of videos about that sector of manufacturing right so like videos of this really cool manufacturing process i've never seen before or like a guy making something or under craftsman making something out of a material i've never heard of before that one's really good that's the prepared i like a newsletter by alison roman it's a recipe newsletter she gives you a story and a recipe every week i recently got a larger kitchen that's not also in my living room. So I've been cooking a little bit more and enjoying her recipes and like, oh, I need to actually get some equipment to cook with.

I definitely need a link to that newsletter. Yeah, it's good. She has a really good burger recipe, even if you don't like burgers, they're pretty tasty.

And then the last one is Blackbird Spyplane, which is a newsletter. It's written by this guy, Jonah Weiner, who's out in California. So clothing, it's about design.

And I like it because his voices and author is super jarring. but it's really fun to read, and he kind of, like, uses this weird mixed capitalization style, and it feels like you're being yelled at, but, like, in the military, and it has this weird, like, mix of, like, technical lingo within the design world, like, aesthetic, and then also technical lingo in the military world, like intelligence and reconnaissance, but applied to something completely different, and it's really fun to read. And your fourth Adafruit newsletter would be?

Yeah, so the Adafruit newsletter, I'll plug it, is. I write their IoT newsletter comes out every single month. I basically gather information about IoT projects that either get sent to me.

I pick up on Twitter or I just pick up from being on the internet, put it in an Evernote, and then convert it to Markdown and send it every month.

Paul

I'll share two quick newsletters and I'll link to these in the show notes as well. If you like to read and you enjoy sci-fi and fantasy, Transfer Orbit is a newsletter that's out there. And I forget the gentleman's name.

But he does great reviews of both new books and some older books from time to time. He's written for I-09 and a couple other sci-fi-type websites, and I really enjoy his reviews. He and I have very similar taste as is what I've learned.

And it's always nice to find a reviewer that has similar taste to you because then you know that you can trust them a little bit more as well. The next one, speaking of similar taste, I've shared how much I love music on the podcast, but one is called indie mixtape with Stephen Hayden. Stephen is a music critic author and podcast host as well, who actually lives here in Minnesota like I do.

But it comes out weekly on Monday, on Fridays, I should say, and it just touches on some of the big new releases. There's usually an interview with an artist, but I'll put links to those in the show notes as well. Sweet.

I need more music to listen to, so that'll work out very well. Last question for you that I ask each guest. You're about to start a new project.

Which board are you going to reach for to prototype with?

Brent Rubell

Usually I have a project in mind for what I'm applying this to. I really like the feather format. I think the feathers at this point, especially like the newer feathers.

So the feather ESP 32 S3 and the ESP 32V2, like the ones with the charger. And like there's so much circuitry built into them that it's hard not to reach for them. And they have a pretty nice pin out.

I started with an Uno and the feather is pretty good for IoT projects. It has the battery. most of them now have Wi-Fi.

Probably a feather ESP 32V-2.

Paul

And I have to ask, is that Wippersnapper compatible? Oh, you know it is.

Brent Rubell

Of course it is.

Paul

Brent, thanks so much for being on the show. Thank you. Thank you for listening to the CircuitPython Show.

For show notes, transcripts, and to support the show, visit CircuitPythonShow.com. Until next episode, stay positive.
