---
date:
  created: 2022-11-14
title: "Episode 22 - Joey Castillo"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep022.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutter. This episode, I'm joined by Joey Castillo.

Joey is a hardware and software engineer based out of San Antonio, Texas. In 2019, Joey began branching out into hardware and electrical engineering. He created oddly specific objects, a division dedicated to designing, manufacturing, and selling comprehensible open-source gadgets for hobbyists and creative technologists.

This episode is brought to you by PCB Way. With over a decade of experience, PCB Way is one of the most experienced manufacturers in PCB prototyping and design. Whether you're an engineer, students, or hobbyist, PCBway offers a simple and fast prototyping service, and it's cost effective at only $5 for 10 PCBs.

And check out PCBWay.com slash project where PCBway helps makers and hobbyists collaborate on their designs and projects. Make your design a reality and check out PCBWay.com for all your PCBWay.com for all your PCBWing. needs, and they also now offer CNC machining and 3D printing services.

Visit PCBWay.com for more information. Thanks to PCBWay for their sponsorship. Joey, welcome to the show.

Howdy. Good to be here. Tell me how you got started with computers and electronics.

Joey Castillo

So, I guess how I could start with computers and electronics, it starts way back. I mean, I was like into computers as a kid. Like, I don't know, like my aunt gave me her compact portable from like the 1980s. 80s when I was in like grade school and I started playing with that. Also tried soldering things together as a kid but never really got very far. In more recent years, I got into software engineering doing kind of iOS apps, app world, app land kind of stuff. And that's, from there, I started kind of hacking back again on electronics projects back in like 2019 or so and kind of started to really make a go of it and now I'm doing this oddly specific objects thing. Tell me a little bit about oddly specific objects.

I started in 2019 with kind of the quixotic, exotic, I forget how to pronounce that word, dream of building an open source ebook reader. And at the time, like, I didn't know enough to know how to build that. So I started up with a simple projects.

And my first project, I called it the hiking log. It was a 3D printed log, and inside was a feather and a GPS wing and a temperature sensor. And I could throw in my backpack when I go on hikes, and it would log my location and temperature data when I go camping.

I thought myself, like, it's a data logger that's shaped like a lot. log, that is an oddly specific object, and that was where the name kind of came from. Since then, I've started, you know, building more of these, like, kind of gadgets for sale. So I have the sensor watch, obviously, and then the LCD feather wing. And yeah, oddly specific object just feels like a, you know, it's kind of like the box into which I put those kinds of projects, more or less.

Paul

I wanted to ask you about the LCD feather wing. You recently tweeted about implementing the I-2-C driver with CircuitPython first before Arduino. Tell me more about the LCD featherwing and what led that decision.

Joey Castillo

So, yes, the LCD featherwing, it's kind of a simple gadget. I mean, it's making it a little complex, but essentially it's a raw LCD glass, which requires being driven by some kind of fancy analog signals, and a chip that translates between the I-squared C protocol that we all know and love, and these kind of very analog kind of LCD driving signals. When you bring up a new thing, there's all kinds of things that can go wrong.

It's like, did I, first of all, did I wire it correctly? Did I, like, mix up my TX and Rx lines? You know, did I do everything powered properly?

Am I sending the right bites over the bus to initialize it and display something on the screen? And when you're working kind of Arduino world, you can call begin on the I-squared C bus and you can send some bites, but you're kind of just keeping your fingers crossed. Whereas with CircuitPython, you know, if you forget to have a pull-up on your I-squared C line, you're going to get a message in the console telling you that you did that.

You made the mistake. So when it came time to write the I-square-C driver, there were a couple of factors that led me to go CircuitPython first. First of all, it was just really easy to get started and make sure that I had it wired up correctly.

I had one thing where I was like, why isn't it this working? Well, oh, there's no device at that address. Well, Circup Python told me there's no advice at that address, and I went back and checked my data sheet and put the correct address in.

But that's the kind of thing that could have had me flummoxed in Ardoinoland for a while until I scanned the whole bus. But seeing a really simple, like, error message telling me this is what's wrong, meant that I get it right quickly. And I guess that's the second thing, fast iteration cycles.

I was doing these character mappings where it's like which segment maps to which position in a byte. So if I have something wrong there, in an Arduino sketch, I go in and I edit my bitmasks and then I compile and I upload. Whereas with CircuitPython, if I change that bitmask and I just hit the save button, the code automatically restarts and I'm in business.

That really like super fast iteration cycle of working in CircuitPython really made it a different. an obvious first choice for developing the driver. Like, I want to support CircuitPython users, of course, but it's actually much easier for me as a builder of gadgets to get started there.

And then when it came time to do the Arduino driver, I more or less just started with my Python code, copied it into a C++ file, and started just porting over line by line what I had done. But all of the hard part, all of the thinking part, was already done by past Joey in Python. So, that was kind of the thought process behind building the CircuitPython driver first and then the Arduino driver.

Paul

That's been a common theme on the show is that fast iteration cycle and that immediate feedback you get from error messages.

Joey Castillo

Yeah, no, it's just really great. And again, it's the kind of thing that could have you flummox because you start out with this thing if you have all of these possibilities that the issue could be. And the faster you can get narrowed down to what it might be to what it is, the sooner you can address that and find the next inevitable issue. And, you know, you knock over enough issues you're done.

Paul

You mentioned the open book earlier, which is an open source e-reader using a Raspberry Pi Pico. How did you develop the user interface for an e-book reader?

Joey Castillo

I mentioned in the beginning I kind of started in like app world and iOS app world. And so in the beginning, like at the beginning, I used UIKit, which is this really cool kind of event-driven system and I still find it really intuitive. Like if you have like a window, okay, so you have a window and then into that window you add a table and in that table you have a bunch of cells, right? If you wanted to lay something like that, out, you wouldn't want to work in raw screen coordinates for that, right? So you have the window, and you add the window, and you add the cells as a subview of the table, and you have the label as a subview of the cells, and everything kind of just lays out recursively, and it, like, just works. So when I wanted to do the open book, I really wanted to have a user interface framework like that that would let me, like, kind of lay things out in an intuitive way. And this was another thing where I actually got started with that insert in iPhone, because, you know, Eventually, when I wrote this in C or C++ plus, most of my time was spent wrestling with pointers and smart pointers and weak pointers and shared pointers.

Whereas in CircuitPython, I can just, like, define my objects and define the way I want my objects to relate to other objects. And in this case, I kind of piggybacked off of display I.O. Because my views in my user interface hierarchy are actually just groups with some extra stuff sprinkled on.

So once I started to do that, it was very easy to just like, okay, now my layout is working recursively. Now I want to have a tap, and I want to see where that tap hit. So I can start with a screen coordinate and recursively work my way backwards to figure out which object on the screen received that tap.

And then that kind of bubbles up throughout the view hierarchy to a point where, like, okay, my cell can have a chance to respond to that tap, and then my table can have a chance to respond to that tap, and then my window can have a chance to respond to that tap. That's a really kind of a complex system to kind of build out from scratch. But starting in Python world, it was fun.

And it was actually really quite easy to iterate quickly on that. Not only that, but once the framework was kind of built, I was able to easily use some of the CircuitPython libraries that existed to build cool stuff on top of it, whether it was taking just sort of the, like, you know, the Adiphrut has like the little CircuitPython characters, like the little resistor named Moe and all that, you know, the little characters. Making a little table with those characters and using a D-pad to navigate between them and tapping on one and hopping up an alert.

Like, that was just a very simple way to, like, demo something out, you know, using just like the Adafruit Display Shapes Library and the Adafruit Image Loader. But then, I think it was Jeff Eppler did a MP3 player in CircuitPython. And so I was like, cool, I'll take the B3 player and I'll port it over to Circuit Pi UI, which is the name I had for this UI framework.

And in like an afternoon, I was able to put together a working MP3 player using the buttons and sliders and progress bars that I built in Circuit Pi UI. So it ends up, again, just kind of the really fast iteration cycle. I was able to build cool stuff that I actually liked playing with, but also it kind of exposed some of the, like, cracks or, you know, challenging areas or, like, the rough edges I needed to sand off of circuit pie UI.

And that, like, ended up giving me, like, a very robust kind of, like, event-driven, you know, recursively laid-out kind of UI system. At one time, I actually did think I was going to build the entire open book in CircuitPython for a couple of reasons that didn't work out exactly as I hoped. But when it came time to build the whole thing in C+++, once again just kind of like my A2RC driver, I've got this really well thought out framework that I've built in Python and I've done it in this high level language that takes care of a lot of that stuff for me like, oh my view's gone out of scope. It's garbage collected at some point and it goes away. Now it's up to me a little bit to manage that scope and to figure out whether pointers a week or how, who has to hold on to what.

But the hard part of like, how should it work, that's all something I got to think through in a high-level language like Python, which is a, yeah, it's a huge asset.

Paul

What's next for the open book?

Joey Castillo

So it's next for the open book is I've got this Raspberry Pi Pico-driven version of the open book, which is really finally easy to hand assemble. Like, this has been my main thing. The open book has always been the vision was a do-it-yourself e-book reader that someone can build from scratch and understand.

And now I've got it down to a small number of parts, all relatively large. I'm going to bring 20 of the open book kits to SuperCon in California to hopefully get to people out there. And I've also published all of the design files so folks can order the parts and build it themselves.

If they want to get 20 of them and make it a project with their hackerspace, they could do that. If they wanted to get 100 of them and sell the kits in a country where I can't sell things easily, like have that. Like, steal this book.

That's kind of phase one. I'm calling this one version the developer preview edition because it's kind of got chunky AAA or AAA batteries sticking out the back. So it's not as felt as a lithium polymer battery oriented solution might be, but that also means the part count is lower and it's easier to deal with shipping and transportation and all that.

So, yeah, what's next for the open book is the kind of developer edition. And then we'll see. Next year, I'm going to clear my plate off of a lot of things and then we'll see what I can build.

Paul

Well, that's great to hear. So between the sensor watch, the LCD feather wing, and the open book, a lot of your projects are battery powered. How do you manage power consumption to make them last as long as possible before needing to be charged?

Joey Castillo

Yeah, so this is kind of become a pretty relentless focus of mine. There's two pieces to it, which sort of boil down to like the phases of like standby mode and deep sleep mode. So pretty much all the microcontrollers you're going to work with in CircuitPython or Arduino or anything, they've got two modes.

They've got an idle mode where the CPU is running. and then they've got a standby mode where the CPU isn't running. So the more time you can spend in that standby mode, the better off you are.

It's like with the LCD wing, for example, I have a clock demo in Arduino, and it blinks the colon twice a second. So just like, you know, blink, blink, blink, like a ticking clock. So you could do that by blinking the colon and then calling the delay function with a 500 milliseconds, and then you delete, toggle the colon again, you know.

So that would work. But if you call delay, then you see. CPU is running because it's using the system tick to determine that amount of time.

But if you use Adafruit's Sleepy Dog Library to sleep for 500 milliseconds, then the CPU can actually go to sleep, or in a standby, rather. So that's 99.9 something percent of your second that is just not even awake. It only needs to be awake for that fraction of a second that it's bursting some data out over the I-squared C-bus.

So that's kind of one part of it, just trying to stay in standby mode as much as you can. In the case of the LCD feathering, I also did a kind of a cool trick with the LCD signal routing where you only have to send one byte over the bus to blink the colon or the indicators. And that's another kind of fun trick.

The less data you have to send out over I-squot-C or SPI bus, the less time your CPU is away, number one. And number two, especially with I-squared-C, there's fewer zeros on the I-squart-C bus, which means fewer, less current kind of flowing through those pull-up resistors. So that's kind of in the weeds, but that's another one where it's like, yeah, the less you can do the better.

So the other thing, and this is still kind of in the standby, well, I guess this applies to both. The other thing is just being really careful about what other gadgets in your gadget are getting powered when you're in sleep mode. So with some early open book prototypes, this is the one where I kind of threw the kitchen sink at the early open book prototypes.

It had a neopixel, it had a flash chip, it had a microphone preamplifier to do voice commands out of a headset. It was over the top. But I was looking at it and I was like, why is it consuming so much power?

It's not supposed to, like, my processor is not supposed to consume this much. And then I realized every gadget that I'd hung on the Christmas tree was drawing power. My mic preempt was drawing power.

My neopixel was drawing power. So kind of everything in your gadget, like, if you tie it to, you know, BCC or 3 volts or whatever, it's going to be drawing its quiescent current all the time. So now in the new kind of open book boards, I gate all the power to those peripherals behind a MOSFET power switch.

So let's say that you wanted to make a pigeon camera, like, you know, put next to a bird's nest or something, like take photos of the... This is actually a project I built at one point. It took photos of the pigeons on the time lapse.

At first, I just powered up one of these little serial cameras and the battery died within a few hours because... Not a few hours, but a few days, because it was powered all the time. Whereas if you only turn on that camera when you are ready to take a picture and then you turn it off afterwards, then you're going to get a lot more...

You're going to get a lot more life out of that battery. So that's one thing. The other interesting one.

So one of the early open book prototypes, I'd gated all my power behind that Mosspet power switch, but even when I turned off power to all those peripherals, it was still drawing more current than I was expecting to. So I'm like, what is going on here? And what I realized was some of the signal lines that actually went out to the e-paper driver and stuff were being held high even though I was going into the steep sleep mode.

So it was backpowering some of these things that even though their power was turned off, the signal lines from my microcontroller were backpowering the gadget. So that was causing them to draw more power than I wanted them to. So I had to drive those signal lines low before I went into deep sleep to make sure there was no current whatsoever flowing to them.

And that was another way to get a little more battery life because you just to be really careful and make sure that everything that can draw current is configured so that it can't draw current when you're in that kind of mode that you want to be asleep or drawing less current. So the other, so let's have the equation, standby stuff. But the other big side of the thing is deep sleep mode.

And this is especially interesting to CircuitPython folks because, well, first of all chips have this, but especially like the ESP32 series and the Feather M4 series, they've got a few pins that can do pin alarms, and they've got a real-time clock that lets them do alarms. So with a pin alarm or an alarm, you can put your CircuitPython script into deep sleep mode, and then it goes into this really, really low current consumption mode where it's on the order of like single digit to low double digit microampiers and it can stay there like, you know, it can stay there indefinitely until a pin gets pressed or it can stay there for, you know, seconds, minutes, hours until you're ready to wake up. And it does restart from the beginning of your script, but in a lot of cases that's fine because like, let's say hypothetically you wanted to do that clock example from earlier, but let's get rid of the blinking colon.

and let's just update the time once a minute. So you could update the display and then enter deep sleep mode for 60 seconds. And then at the end of 60 seconds, your script starts over again.

It updates the display with the value of the real-time clock, which is the current time. And then at the end of that, just go back into deep sleep. So now you're spending like 99.9% of a minute in deep sleep mode, and that's where you can get into, like, real, real, like, low power savings.

So actually, I did this kind of as a stress test. It was a weather station type gadget I made using the ESP32S2 and the LCD feather wing. And one of those little 400 million-ampere-hour batteries that fits between the feather headers.

So really small. We're talking like one or two cubic inches. So small gadget.

And the setup was it would turn on, or sorry, it would wake up, it would turn on the temperature sensor, it would take a reading, it would turn it off. Then it would turn the Wi-Fi on, upload that data at a-fruit I.O. And then it would go back into deep sleep for 15 minutes.

So it only had to be awake for maybe like 10, 15 seconds every 15 minutes. So you're up for a minute and hour. That setup lasted two full weeks on that little 400-m-amper-million-hour battery before I needed to recharge it.

And if I wanted to make a more robust weather station that I could leave out for a month, double the battery. 800-mphir hours and you get like a month of battery life. So, yeah, like deep sleep ends up being a really powerful tool for making CircuitPython scripts low power to the point where you could actually write a CircuitPython gadget, deploy it out in the world on a solar panel and a battery, and expect it to last for quite a while, just on deep sleep.

Paul

That's really impressive. Last question that I ask each guest, you're about to start a new project. Which microcontroller do you reach for?

Joey Castillo

So I've got to say it's not the new hotness. It's kind of an oldie but goody. The feather M0 basic.

First of all, I'm all in on the feather ecosystem just because I make battery-powered things. and the idea of a battery-powered gadget you just plug into USB to recharge, that's huge. That's like the framework for making all kinds of cool stuff.

And then the SAMD-21 is just kind of like the Swiss Army knife of microcontrollers. It does so many different things, and it does them all well. So I'm probably going to find whatever I'm about to do will fit well with what the SAMD-21 needs or has available to me.

And then the classic one in particular, because two things. One, I mentioned about low-power stuff. There's no neopixel and no flash chips, so there's very little in the way of extras, so not a lot can draw extra power for me.

But also the little prototyping area, it's really useful to make the gadget into whatever you need it to be. So, like, I'm building a solar power gadget for a friend who is doing an art installation, and that little prototyping area becomes a direction pad for navigating a series of menus. Or there's a feather M-Zero running my LCD featherwing testing setup, and that prototyping area gets a power switch just to turn it off.

and off so I can leave it off most of the time. If you want to make an atmospheric sensor, like solder in one of those little temperature humidity sensors and the little prototyping area, you don't need to dedicate a whole proto board wing. You can just like turn the Feather-M-Zero into whatever gadget you need it to be.

I think that's a huge usability win. So, yeah, if I'm reaching for, if you're telling me nothing other than I'm reaching for a board to do a new project, it's probably going to be the Feather-M-0 basic.

Paul

And if people want to learn more about your products, where should they go?

Joey Castillo

So at this point I'm still on Twitter. we'll see how that goes in the coming weeks. Otherwise, I've got a account on Mastodon, which is linked to my Twitter handle.

And oddlyspecificobjects.com is the website where you can check out the things I've made, and there's actually a link to shop. That oddly specificobjects.com to buy some of the stuff. Or you can buy the feather wing on native fruit.

Paul

That's great. Joey, thanks so much for being on the show.

Joey Castillo

Thanks for having me. A really great conversation, and I appreciate it.

Paul

Thanks to Joey for being on the show, and thank you to PCBway for their sponsorship of the Circuit Python Show. For show notes, transcripts, and to support the show, visit CircuitPythonshow.com. Until next episode, stay positive.
