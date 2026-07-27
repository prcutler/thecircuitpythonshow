---
date:
  created: 2026-04-20
title: "Episode 58 - Developing for the Fruit Jam"
---

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by three former guests on the show, Dan Cogliano, Tim Cox, and Cooper Dalrymple. They've joined me to chat about the Adafruit Fruit Jam, which was first released last July and shipped to Adabox subscribers this past November. The Fruit Jam runs CircuitPython and is a credit card-sized microcomputer with display support, USB host for mice keyboards and game pads, and SD card, expansion GPIO, and more. Tim, Dan, and Cooper, welcome to the show.

Tim

Hey, Paul.

Cooper Dalrymple

Hey, Paul. Thanks for having us.

Paul

Thanks. Tim, we'll start with you. The Fruit Jam hardware can run Fruit JamOS, which is a new way to load a circuit Python application. What was the inspiration for Fruit JamOS and how does it work? Yeah, good question.

Tim

So for Adafruit generally, one of our big goals going into Fruit JamOS was to make something that sort of harkens back to like the Commodore 64 era of devices. sort of all-in-one devices that you write the programs on there, you run the programs on there. Back in those days, they had the keyboard built in. They had the little display built in. So everything was ready to go for you. Just kind of plug it in, start programming and do your thing. So that was a big inspiration going into Fruit Jam OSbroadly for all the Adafruit folks. And then for me specifically, I would say also there was emphasis on Q Basic. QBASIC was one of the first programming languages that I ever interacted with. So it's always held a sort of nostalgic place in my heart. And as I was working on Fruit JamOS, I kind of got, you know, it took me back to that era of Q Basic IDE where it was similar. It had the editor built in. You could pop over and run your code real fast right there. And it was just this all in one sort of package, write your code, run your code, see what it does right there and iterate through very quickly. So that was another big one for me was QBASIC.

Paul

What's involved that add support to a normal CircuitPython program to run on Fruit Jam OS?

Tim

Yeah. So it's pretty straightforward, especially if your program is already set up for the Fruit Jam, if you're already making use of the Fruit Jam peripherals and stuff like that. If you have something completely unrelated, like it's a Pi portal program or something, there's a little bit more converting that needs to take place. But if you've got an app that you have already used on a Fruit Jam today by just saving it in code. It's very straightforward. You can just create an icon for it, or even, even just leave it the default one if you want. Create a little metadata file that has the name of your app. It has the file path to the icon. You store that alongside your code and you copy your code with a folder into the app's directory on CircuitPy. And that's all you need to do. The next time you launch the Fruit Jam OS launcher, it scans that folder. So it will automatically find your app along with all the other ones. We'll show your icon right on the launcher there. User can launch it. And as soon as they launch it, it just executes right into your code.

Paul

code.pye file. I know Cooper you I had Sean Carolan on the show recently who did the Pac-Man clone in CircuitPython and you reached out to him and gave him a hand to and submitted a PR I believe to get it on the fruit jam.

Cooper Dalrymple

Yeah and actually I want to add to that I did create a repository and if viewers aren't familiar with how GitHub works basically repository is like a project right I did create a project that's just fruit jam application I was trying to make it as basic as possible just to be a place to store all those best practices of how to work with this hardware. Of course, many users have contributed applications in their own way that may do things a little bit differently. But it's always good to have a good foundation of where to start. And that does stuff like initializing the display properly, handling different resolutions, taking it in keyboard and mouse input and stuff, which I know we'll get into later.

Paul

Cooper, you were one of the first in the community to release a game for the Fruit Jam, Frutris, a Tetris clone. You've also done some work behind the scenes working on USB host for game pads, fruit jam OS, and more like you just mentioned. What grabbed you and excited you about the fruit jam? So I remember when the fruit jam first came out.

Cooper Dalrymple

This was last year, was it August or something? It was July. Is that, okay. Yeah, yeah. And I really wanted to be a part of that like first initial push on it, that wave. And I was playing around with Fruit JamOS because at that time, Tim, you had already had it working. and a few applications bundled in from the Learnn guides. And I have to admit, I wasn't in on the Metro 2350B days, the really early development. But a lot of that I know came from that era, I would say. And I knew I was like, I have to do something here, you know, something that I can turn around, turn and burn very quickly, just because I was excited to be a part of everything. And we were lacking Tetris. You know, we had a lot of other things. I think mine sweeper, breakout, so on. And Testris is a different beast. because there is some math involved and a little bit more management in order to make it a really good Tetris experience, right? And so I did my best. And actually, the work on that, I had actually kind of stolen for myself. I don't know if anyone here is familiar with Look Mum, no computer. It's kind of a techie, YouTuber, crazy guy. He did a thing forever ago called the Mega Machine, which was, gosh, it was like a 10 by 10 array of Game Boys in which you could control the screen of each one of them. And he was looking for input back then for like applications, stuff. He could run on these like 100 Game Boys, right? And I just thought it was very meta to make Tetris that played on like 100 Game Boys, right? Anyway, even though that was kind of a silly thing, a lot of the code came from that for the actual rotation, the different Tetraminos, things like that. So that was very important to contribute in that way. And I was able to get that out in, like, I think, less than a week or something, just, you know, off the ground. I was really happy with how, you know, people, you know, started playing around with that. It was pretty fun. And as for those other developments, I mean, there's been a lot of foundation developed by Adafruit, U-Tem, especially. For, like, I mean, USB host is really where everything goes down to because CircuitPython has a lot of features on it out of the box, but it's not an operating system. really and operating systems typically handle a lot of USB handle I mean obviously keyboard I believe is handled by the supervisor right yep but things that are a little more complex like game pads especially because you know every game pad operates a little bit differently I mean you have X input D input you have it's escaping me now but um it's not X input input there's a there's a mode for K joystick's that operate like that that you have to support. And then some game pads, including the Adafruit, SNES gamepad, operate like in their own weird mode. That's just kind of difficult to support. So obviously, for every application to include its own driver for each one of these devices, it's just not feasible. So that's one thing that I was able to contribute is creating a library to at least combine that a lot together so people just don't have to worry about it. And I think that's when CircuitPython shines, and you just don't have to worry about it, right? You just make your own fun code, and you don't have to think so much about, you know, specific device input and stuff.

Paul

Dan, what about you? What excited you about the Fruit Jam?

Dan Cogliano

Well, first of all, thanks for having me. I'm more on the application end of it as opposed to the operating system, and so I do a lot of application and user applications. And I was really excited about it. I mean, I grew up, you know, with arcade games, retroarchic. arcade games and I guess I could consider myself retro because I'm at that age. But that really excited me with the or the different emulators that come out with it. I think it's great. So I decided to write some games in CircuitPython for it. The first one was the Zork Z-Machine, which was something I wrote five or six years ago in Arduino. And I decided, well, I'm going to convert that to CircuitPython, see if I can get reasonable performance out of it. And I did. So I went from there, and then I wrote a moon miner game, which is kind of like the Lunar Lander, if you remember that from the arcades back in the 80s. So it's similar to that. And then I wrote a couple screensavers. So doing a bunch of fun projects, at least for me, I really enjoyed writing them. We've got four screens savers so far, and I'm looking at maybe adding more as I find ideas for them. And so, yeah, it's been a lot of fun.

Paul

Tell me a little bit more about the four screensavers you've written. Can you describe them a little bit? And, you know, what worked well about writing them for the fruit jam? And were there any challenges that you encountered?

Dan Cogliano

Well, you know, screensavers go back since the dawn of PCs. You know, there was actually a real purpose for them at one time. you didn't want to have the screen burn in. So now it's more of a fun thing to see on the screen. So I wrote four of them. I did Starfield screensaver, which is kind of like the Star Trek screen, you know, with the stars going on the screen. And I wrote a maze creator and a real-time solver. And that actually came from an Arduino project I wrote for Adafruit, probably six years ago, that was also Arduino. And that was on a e-paper device. So I thought, well, I want to do that one, rewrite that one for CircuitPython. And that one turned out really well. Then the recent ones I've done is a 15 puzzle screensaver. If you ever know the child's toy where you have numbers from 1 to 15 in a grid and you slide the tiles around, and I thought, well, this would be great for circuit. at Python because it has tile grid and it's really the same concept except you're just taking pieces of one image and moving around and I thought well that would be kind of a neat challenge so I did that and that turned out really well the latest one I did was just a weather clock it's very stagnant there's not much going on other than showing the updating the time and the current weather conditions and the temperature so that seemed to be a good screensaver because when you're not doing anything the time comes up and the weather comes out. I thought, that'd be pretty good too.

Paul

Cooper, you mentioned earlier that you've done some work about keyboard input and game pads. For someone who's used to writing a normal code. code.py in CircuitPython and maybe has hooked up a few sensors over STEMAQT, how hard is it to code for the Fruit Jam to set up things like the display or to use keyboards or game pads?

Cooper Dalrymple

Well, if you've ever used display I.O. at all for, you know, little OLED displays, black and white, all that kind of, it's the exact same API. So, loading up bitmaps, drawing shapes with vector, vector I.O, whatever. All that kind of stuff, it all uses the exact same principles using tile grid, et cetera. In fact, Tim, I know you helped, I believe you helped create a lot of those APIs, right? And tile grid in a way almost acts like a Game Boy or something like that in the way that. you pick different sprites from a sheet and stuff like that too. And then, of course, I know the Adafruit display text library is one that I use on basically every project. If you want to write out displays without, I believe you can use terminal I.O. directly. And I have done that once or twice. But for the most part, you want to use that to get started to write text out to your display, depending on what you're trying to do. like what those screensaver stand was talking about you probably do principles a little bit differently you know you're not working directly with input and stuff like that you kind of needs to run itself and so you might not use some of these resources which by the way I did want to mention which I love the displays a lot of times I have my fruit jam just running the background while I'm working and just running through all those screensavers sometimes random mode and stuff like that if you're interested in any of these projects which I know a lot of these resources sources come bundled in with Fruit Jam OS, but I do have another application that I know Tim and I have been talking about, the library, Fruit Jam library application, which gives you an opportunity, because the Fruit Jam, one of the cool things about it is that it has all the bells and whistles in it, right? You have Wi-Fi, you have audio, you have HDMI, you have USB host, etc. It's its own little computer, right? Neopixel even and GPIO expansion. So that Wi-Fi adds a whole new capacity. Well, now you can basically run things on the device itself and get information from the web, et cetera, as long as you're connected to Wi-Fi. And so I've been developing this library application to make it so that you can download kind of third-party applications, maybe outside of the Adafruit space, or maybe in the future, Adafruit would want to host some of their own applications through that that are maybe a little bit too big to host directly on Fruit Jam OS, you know, in that one download. And so you can download this one. And so you can download application, which will allow you to download all the applications, right? It's the idea, right? So I know Dan's, a lot of his projects, Z-machine, Moon Miner, right? And those screenshots, it actually supports screensavers as well, are all downloadable through there. And eventually, I know Tim, we plan on integrating that into the core OS. We're not there yet. Just it's more on my plate than anything.

Dan Cogliano

But, you know, those are future plans there. Yeah. I think it's great. It's a wonderful idea, and I hope you get that out there and incorporate it in a fruit jam. I think it's great. I think of it more as an app store than a library because you can go and pick and choose what you want to download.

Cooper Dalrymple

So it's great. It basically is, I don't think we'd want to use the term store per se. There's no cash transactions. Yeah.

Tim

I'm super excited about the library as well. I'm glad you brought it up, Cooper. And yeah, for folks listening, the goal is we're going to move that into Fruit JamOS. So then that will be the library itself will be bundled in and you'll be able to launch it right out of the gate and then download further stuff from there. And yeah, I did, I think I suggested to change name. And maybe even was App Store originally. And I wanted to change it to library for both the reason Cooper mentioned. We don't intend to sell anything through there, but also just we don't want to run a foul of Apple necessarily. Right. They already have App Store lockdown. But to your point, Dan, it definitely is like exact same concept of App Store, Google Play Store, exact same idea where you can distribute apps through there.

Cooper Dalrymple

I think you're right. I think we did change it at one point. But I like library. It's like you're checking out a book.

Tim

Yeah, I liked library as well. Yeah.

Cooper Dalrymple

And on top of that, some of the applications, like there's another game that I helped develop with my partner who did all the writing and everything called Speed Dating, right? Which is like a dating sim kind of featuring. featuring Blinka, well, kind of featuring Blinka and a bunch of other snakes and stuff. And that, there's just, there's just too much graphically and audio-wise. Some, the audio files are kind of big. I don't think it wouldn't necessarily max out the flash memory on the device or anything, but it would be significant enough that would be over half of the Fruit JamOS. So it's just not a good idea to bundle in with the core download. And plus the library, there's still more work to be done, but you can download. to either the flash storage directly on the device or to an SD card, right? So then you kind of remove the limits of what, you know, the flash storage limits of the device. And one of these days, I could see somebody starting to dive into more intensive graphically applications and things like that that may exceed the base storage of even the fruit jam, which I think, was it eight, 16 megabytes? I believe it's 16 megs flash, yeah, it's quite big. It's quite big, but you put in a 4-gigabyte SD card, then you have basically infinite storage in a way.

Tim

To your point there, I think the SD card and the Wi-Fi as well, the Wi-Fi was mentioned earlier with the weather screensaver. I think those two things bring a lot to the table for the Fruit Jam, being able to get stuff off of the internet and being able to cache media files, either downloaded stuff from the internet to cache, or like you're saying, apps with pre-built assets or stuff like that, those could fit on the SD card and free up a lot of. of space and flash. So those are two of my top picks for peripherals on the fruit jam. And the Wi-Fi, worth mentioning, the Wi-Fi was a relatively late addition to the Fruit Jam. There were a couple of revisions that came out, not publicly, that they were never sold, but there were internal ones we were working on where there was no Wi-Fi. There was originally an I-SPI cable connector to be able to connect like TFT cables over SPI. And then Lady Ada was playing around with it and decided, Wi-Fi would be super cool to have this whole little mini-computer. And I definitely think that was the right call in hindsight. The Wi-Fi adds a lot to it for sure.

Cooper Dalrymple

I think so too. I mean, there is GPIO expansion, and I believe there's some I-2C ports and stuff. And heck, I think there's a STEMA QT port too. Yep, definitely. So if really having another display on top of the HTML output is necessary, I'm sure you could just throw on a little SSD 1306 or something.

Tim

Yep, yeah, we've talked about like shields for the top as well. There's two rows, I don't know if it's 20 pins or however many pins, but there are two rows of GPIO pins. At some point, we may have a little shield or a hat or something that you could stick on the top to add TFT screen. And I'm hoping for a little sort of game style, like game gear with the screen in the middle and then Dpad and A.B button on the right. So maybe something like that.

Cooper Dalrymple

Do you think there's no battery capabilities on the device, is there?

Tim

That is correct. Yeah, as far as I know, there's no charging. So unlike the feathers, which have built-in charging and stuff, there's no JST connector for a battery and no built-in charging. So you have to use, like, USB battery or something to go mobile with it.

Cooper Dalrymple

Yeah, that's a great idea, though. I know one I had, is it would be really, granted, you know, you have the USB host support, which is awesome. But it would be really cool to have a little hat that sticks on top, and you can plug in SNES controllers. or NES or something like that. That would be really cool too. Maybe not a huge difference over the USB, but it would be nice regardless. Yeah, definitely.

Dan Cogliano

It reminds me at the old Atari cartridge location where you stick in a cartridge where the ports are. So it goes back to the retro styling.

Cooper Dalrymple

Definitely, definitely. Yeah, and you know, there's a lot of GPIO on there. I bet you could almost do kind of a basic cartridge loading. thing. We're definitely deep dive in here. Just a few address lines, maybe some data lines. I don't know. Get an e-prom on there. Who knows?

Paul

Speaking of displays, one of the things that I've seen, and I think other people may have run into as well, is that display out of resolution error that comes up if you don't have the right monitor plugged into a fruit jam. As a dev, how do you code for different display sizes? on the Fruit Jam in CircuitPython itself. Yeah, good question.

Tim

So it is, it's a little tricky because it can't be done, or I will say it's not set up to be super automatic. So lots of devices, lots of modern devices, when you plug them into a screen, they'll kind of query the screen to figure out what size it is and then select something that they both agree on. The Fruit Jam has a few things that make it tricky. One is that it's working at relatively small resolutions by today's standards at least, like 640 by 480 or 320 by 240 even, which ends up getting doubled anyways. So those are relatively small sizes. There are some screens out there today if you just go to the store, your average electronics store today and you buy sort of the cheapest monitor that supports HDMI. It may not support some of those smaller ones. It may be only 1920 by 1080 or 1280p, just modern sizes. And so that's when it will pop up, I think, the error like you're talking about where you'll plug it in and it will say, you know, we can't recognize this format or something like that. You can actually connect to it through I-2C. So one of the things that HDMI does is it has, I think it's called Edid. Edid, E-D-I-D is the acronym. And I'm not 100% sure what all is inside of it, but there is a little data channel inside of there. And you can query the screen to ask it like what resolutions it supports. And so you could write code that would do some of that and try to select one. The deal is that the for Jam is, again, it's only doing those smaller screens. And so then even if you ask the screen what it supports, it may still not support something that works for that smaller size. So that's one of the tricky bits. And then in terms of like, what is the developer actually, what do you have control over that's easy to do? It's super easy to change the resolution between the ones that are supported by the fruit jam. So there's a few different ways that works. One of them is the user gets some level of control inside of settings. Toml. You can actually set a configuration line where the user can say, you know, I prefer the 360 size screen, or I prefer the 320 by 240, or I prefer the 640 by 480. So you can put that in there. And then as a developer, when you're working on your app, you can read the setting there. And kind of like the ideal thing would be you follow whatever the user wants. But maybe if you're making a game or something and you really have to have a specific screen size for your assets, then you can go and sort of just change the configuration on the display. And inside of the Fruit Jam library, so we have a Fruit Jam library that's just AdaFruit underscore Fruit Jam. It's sort of like a Fruit Jam version of the portal-based libraries for folks that are familiar with like the Pi Portal and the bunch of the other ones, Fun House. There's a bunch of them that have those libraries. So Fruit Jam Library has a bunch of Fruit Jam hardware-specific stuff in it, and one of the things that it provides is a high-level reconfigure display. So I forget the exact name of the function, but you can call like Configure Display. pass it a width and height, and that's sort of the one-liner that you need as a developer to actually specify the size for your own app, is just pop that in and say 320, 240 or whatever size you want.

Cooper Dalrymple

And a lot of applications do default to that 320 by 240 game-wise and stuff, because that is kind of the easiest to work with in an arcade game format. However, it is, you can support all the support. There's four different resolutions, I believe, that the Fruit Jam really supports within CircuitPy. Python. And it is possible to have support for all those. But it can be a challenge. In fact, for the Fruit Jam version of Pac-Man that we have, which I believe I worked on with Retired Wizard, it took a lot of testing of all those different resolutions and reformatting, especially with that, because it's kind of a, was it, Tate style game, you know, with its vertical layout. It was difficult to get that to fit exactly right. But with clever use of display IOs, the group's scaling property, you can kind of achieve what you need to do. But you do get a little bit of a performance hit whenever you're scaling objects just because it has to copy all those buffers

Paul

and stuff. What are some other challenges for developers to look out for when developing for the fruit jam? I will take a quick one, which would be USB stuff. I know we talked to a lot about

Tim

USB hosts earlier and where the responsibility lies between CircuitPython core. handling the USB versus you as an application developer having to handle it in your own app. And so I think we mentioned before that keyboard is handled by the core. So if you just need basic keystrokes, you know, you just want to know when the user presses on the arrow keys or when they type in a message. You can do that very easily. You actually just see the input as though it came in over the serial line if you were writing a C-Python code. So you can kind of very easily query the keyboard to get those keys that have been pressed. What we don't have in the core is we don't have support for mice or any other kind of peripherals. So if you want to have a mice, a mouse, or a game pad in your game, you'll have to have code inside of your own code. code.py that initializes it and handles it. We do have helper libraries and stuff, but it's something you've got to put in your code. And then your other sort of choice is if you need really fine-grained control. So it's really easy to find out that the arrow key has been pressed or that the user typed the word, hello. But if you really, you know, if you think about some video games, you want to know up and down, right? You want to know, like, when the key is pressed, while it's held down, and then you want to know when it's released. For instance, if you want to have a character like run around a world using a D-pad, that's kind of how it works, you know, in most games by default. And if you do want that control where you need to know the down, the hold, the up, that is a little bit deeper of a level. So the way that the keyboard is hooked up by default in CircuitPython, you don't get that stuff. But what you can do is sort of, again, sort of reconfigure it. You can have it undo the default configuration and you can get lower level control where you actually get sort of raw HID events as needed. And you can definitely see, you know, key went down, key has been held down, and then key is released finally. So you could do that stuff. So that is one gotcha that I will throw out is depending on how you want to do that input. You may need to use that slightly lower. level API for the keyboard.

Cooper Dalrymple

I've actually debated extending the GamePad Library to include an option. It'd have to be a flag you turn on, but to allow it to automatically detach the keyboard and use that as a game pad input, quote unquote. Yeah, that would be cool. It would be cool. It just hasn't happened. Have you played around with that yet, Tim, in any of your applications? The GamePad Library? No, no, directly accessing keyboard events.

Tim

Oh, yeah, a little bit. Yeah, so I have, I did, I don't think I have done it in any of my games. So I did, the main game that I have worked on more recently uses the D-pad. Although, you know, I think the Flappy Nyan Cat one, maybe the Flappy Nyan Cat, I think, does actually pull the lower level one. No, that's not true, though, because you don't hold the button down. I don't think that's true. Sorry, yeah, I think I misremembered that part. I don't think I have done the lower-level keyboard thing for any of my games, but I am familiar with the code for it because I did the keyboard guide whenever we first launched the fruit jam or I should say when we eventually launched the Ada box the box came with a keyboard, it came with a mouse and it came with the keyboard. And when we first got the fruit jams in stock in the store, we also got some of those other peripherals. And so we wrote guides around the mouse and the keyboard that have all the different ways you can hook them up. So I was familiar with it from that, but I don't believe I have actually used it in a game specifically yet.

Cooper Dalrymple

Yeah, I myself, I just hadn't hit a point in which I really needed it yet, so I hadn't really worked on it. I would like to add to that question, though, you know, CircuitPython, these microcontrollers are super powerful for what they are, but there is a limit to how much of the screen you can draw in one time without, you know, without breaking that 30, you know, hertz cap or whatever. And so you kind of have to be careful when you're dealing with more complex scenarios to only update, you know, certain parts of the screen at a time. And the more that you can limit that, the better your game will feel and run. That's why puzzle games work really well because a lot of times you're only dealing one thing at a time. So it's not that hard. But when getting into action games, like if you're doing screens, you know, side scrolling and stuff, it's probably possible. But you'll have some challenges working with that to get it to run really smoothly. I know I've been able to get some action scenarios working in which you're just moving the characters around and that works really well. Actually, one example, speaking of screen savers, I did make one screen saver, it's the mystify screen saver from like the, I don't know, Windows XP days, right? Which is a little bit beyond, because I know Fruit JamOS comes with a lot of, you know, flying toasters and stuff, the more like Macintosh classics. And so I wanted to like get something from a different era, right? Although it was pretty, it was surprisingly easy to program with vectorio Polygons and stuff like that to get that effect. it runs kind of slow I'm surprising because every in order to do the polygons correctly and fill that entire screen with your I don't know if you all are familiar with that that style of screen saver but you basically have to redraw the screen for every frame so it's kind of like maybe three four frames per second but it still looks cool so I decided to publish it regardless but it's something to be aware of. Yeah I ran into

Dan Cogliano

the screen scrolling issue with the moon miner game. I initially wanted to have a screen scrolling when the ship is moving around the planet. And I also wanted a high resolution because I have this heads-up display of these statistics that are running. And it's 640 by 480 and sliding screens just did not work out for me. So I changed the course and went with paging one page to the other. When you get to the right side of the screen, it'll switch to the left side. So it worked out. But yeah, the higher resolution, you go, the more pixels you got to deal with, the more performance issues that you may run into.

Cooper Dalrymple

But, you know, limitations breed creativity. Yeah. So I think that's a part of the fun. If there were no limitation, if it was just a black box, I could just do anything, it wouldn't be as fun.

Paul

Well, that is the fun of working with microcontrollers. It's the constraints that you're under and what can you do with so little. Exactly.

Dan Cogliano

And a nice thing about screensavers, you don't have to worry about the keyboard. That's all taking care of at the operating system level. Somebody touches a key, your program's gone. And so it's doing something else. Totally.

Paul

What advice would you have for someone interested in creating a gamer application for the fruit jam?

Dan Cogliano

Well, you'd need to get one for one thing. And right now, I'm surprised, like, they're still hard to get after, since August.

Cooper Dalrymple

That's not entirely true, though. One thing I was doing some work on recently, in order to help iteration of developing this stuff, it's actually possible to get some components of a fruit jam application running within Blinka, right, using Tim, your PyGame display library. You can kind of simulate the environment and, I don't know, work with it that way. You still should get a fruit jam, but you can at least get started.

Tim

Yeah, I mean, even generally, that's one of the things that brought me to CircuitPython was that portability. Like not everything that works on PC, normal Python works in CircuitPython, but lots of the stuff is familiar. So yeah, we have some ways to try to do that development on the PC or on other hardware. Like it was thrown out earlier, the Metro, the Metro RP 2350 days before the Fruit Jam was out. We had the Metro RP 2350 and you could actually hook up enough hardware to that to where it can, basically be a fruit jam. You would need the Wi-Fi and the display, HDMI stuff. But there was USB connector, so you could do all of that. Back to the question about the advice for making a game, I think one of my big pieces of advice is kind of explore the different display API. So we talked a little bit about this, about how much your, how many different things on the screen are moving at once. And if you can limit it to just one or two things moving, you have a better time. But there's also just several different ways you can draw stuff. So we talked a little bit about display text earlier for text, and we've talked about bitmaps and tile grids and stuff. Vector I.O. was mentioned. So that's another one of the options if you're doing basic shapes and colors and stuff. And then the Bitmap Tools Library is another one that I'll call out that's in the core that can do lots of really interesting manipulations with bitmaps. Sometimes you might be able to get away with using the Bitmap Tools library instead of different sets of sprites or different assets or something. like that. That would be my advice is to explore the different ways that there are out there to display stuff. We have different ones are better suited for certain things than others. So you might have better luck using a different technique for your particular game based on how you want it to behave. And those bitmap tools you're talking about. That's like palette swapping and things

Cooper Dalrymple

like that, right? It's not quite. No. So bitmap tools, the core module, there's a bunch of functions

Tim

in there, the ones that I use the most, it's like rotozoom is one. So you can take a chunk out of one bitmap and paste it into another bitmap either rotated or scaled up or scaled down. And you can even do partial scaling with that. So like groups, we mentioned before, groups in display I.O, those can be scaled, but only by a full factor, right? You can scale it by two or three or four. With bitmapTools.RotoZoom, you can do partial scales as well. So you could zoom something, scale it up by one and a half or just by 10% or something like that. So there's rotozoom, there's like draw shapes. There's a circle one, a rectangle one. I believe there's polygon one. There are stuff for alpha blending. There's stuff for dithering. And it's all implemented in C. So it's like it can go really fast to do a bunch of manipulation on a bitmap, either a whole bitmap or a chunk out of a bitmap.

Cooper Dalrymple

Yeah, it'd be awesome to see some. What was the SNES? You see mode seven. It'd be awesome to see something like that, but that might be outside of the capabilities. I mean, I'm sure we can go into a whole discussion on game design. Because that's what it comes down to. You know, the CircuitPython and the Fruit Jam provides you the platform, but game design is the same across the board, you know, how you come up with ideas and explore those ideas. And, of course, the Fruit Jam is not limited just to games. I'd say actually a majority of the application are not game related. You know, you have, well, Larzio, right, paint music thing, right? That's a great application. And that's game adjacent, I would say. And there's a lot else on the board that, you know, you can make a calculator, you know, or the speak and spell. I know that was one you did, Tim. Yep. Speaking spell, IRC.

Dan Cogliano

I learned by example. So I would suggest looking at other CircuitPython projects on GitHub or GitHub or, the LEARN, the Adafruit Learn system or the circuit playground group, that's a good resource for people that are looking for something similar. John Park's CircuitPython PARSEC, he's had a couple games in there. So yeah, there should be resources that I would look at.

Cooper Dalrymple

You actually just reminded me, Dan, I did create a Pong game, super basic for the Fruit Jam, with a included tutorial that goes through everything from the bootstrap to manipulating graphics and controls and USB input. And that would be a great place to start too, especially if you're not familiar with CircuitPython and how that works. Because it's about as basic as you can get.

Paul

Is that available as a learn guide or where can people find that?

Cooper Dalrymple

So it is on GitHub and it has a GitHub pages thing. So it's like a website kind of thing that you go through each section of the tutorial. I think I kind of got inspired by Todd Bot's synth I.O. tutorials to do that one. I'll make sure to share a link with you, Paul, in case you aren't familiar with that.

Paul

Yeah, I'll make sure that I added to the show notes. That'll be great. Well, that's all excellent advice. I'd like to thank all of you for your time this evening. Dan, Tim, and Cooper. Thanks so much for coming on the show.

Cooper Dalrymple

Yeah, thanks for having me, Paul.

Tim

Thank you for having us. It has been a pleasure, as always.

Paul

Thank you for listening to The CircuitPython Show. Thank you to Cooper, Dan, and Tim for joining the show and sharing their experiences developing for the Fruit Jam. To learn more about the Fruit Jam apps the panel has discussed, visit the show notes and transcript at www.circuitpythonshow.com. Until next time, stay positive.
