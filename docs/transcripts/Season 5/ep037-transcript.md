---
date:
  created: 2025-01-13
title: "Episode 37 - Aaron Pendley"
---

## Show Notes

[Show notes available here.](../../episodes/Season 5/ep037.md)

## Transcript

Paul

Welcome to The CircuitPython show. I'm your host, Paul Cutler. This episode, I welcome Aaron Pendley, also known as squid.jpg in the Adafruit community.

Aaron started his career as a game programmer, programming games for the Game Boy Advance, Nintendo DS, PlayStation 3, and Xbox 360 before transitioning to iOS development. Aaron, welcome to the show.

Aaron Pendley

Thanks, Paul. It's an honor to be here.

Paul

I'm glad you could make it. How did you first get started with computers?

Aaron Pendley

I've always been interested in computers since I was a kid, but my first real experience was in the fourth grade. I had this fantastic teacher who once a week would take us to the computer lab where we had a bunch of Apple 2E computers. And he taught us how to program in Basic.

And for the most part, that's all I did for most of my teenage years. My grandma got me this K-Pro 2 computer at a garage sale, for like $25 and it was basically like this, this metal briefcase computer with a couple of floppy drives and like one of those green phosphor screens. And it was already like old at the time, you know, but on one of the floppy disks was the basic programming language. So I was still able to just take that and keep hacking on it, you know, all throughout kind of my teenage years.

And that was really like my main introduction to computers and programming.

Paul

And I understand that you actually won a contest back in 1990 for Game Boy programming.

Aaron Pendley

Yeah, that's right. So at the time that the Game Boy Color came out, I was working as a Bell man slash shuttle driver at a Holiday Inn. Pretty great job for kind of just like a slacker, you know, a teenager who just graduated.

But I got this Game Boy Color and I was just like floored by it. It was amazing. And I didn't know how, but I knew that I wanted to write software that would play on it.

And so I dug around a little bit and I found some kind of gray market Korean hardware. Basically, they sold like cartridges that you could put your own software on using a flash chip and then a little programmer devices to go along with it. So using that, I was able to write code and actually see it run on the hardware itself, which was really exciting.

And the main way that I was able to do it was I learned to see because there was a tool set available called GVDK, Game Boy Developers Kit. Incidentally, that developer kit is still around now, and is still maintained. And it's the basis for the popular GV Studio, which, you know, John Park on his show lately, did a series on how to make games with it.

So that's pretty cool. It was cool to get to kind of use those tools then and they're still around now and still kind of being actively developed and flourishing. So, yeah, with that, I then tried, I don't really have a lot of artistic capability.

So I then tried to recruit basically everyone I knew to help me make a video game. Most people's responses were pretty tepid, you know, like, oh yeah, that would be cool, but they didn't really want to work very hard at it. So I had one friend I knew he was a really great artist and he was studying animation at the time.

So I went to him and was like, you know, hey, do you want to make a video game? And he was just like, yeah, of course. Like, you know, it was a silly question.

So yeah, around that same time, we had just kind of been goofing around with stuff and this competition was announced called Y2 Code. It was right at the end of 1999. And I think we had maybe like three or four months to get something together.

So, you know, in between our day jobs and whatever we were doing, we basically spent all of our waking hours just like working on this game. The idea was kind of as like a platforming game and you had a sword and, you know, you ran around and, you know, killed a bunch of bad guys or whatever. It was our first, you know, game that we ever made.

So it wasn't particularly well designed gameplay-wise. And we weren't able to get sound effects into it. But the art style was really cool, and we had a couple of really cool, like, technically impressive tricks that we did in the game.

And that ended up getting a second place in the competition, which was basically the start of my career. I was then able to use that to get a job working on Game Boy Advance games a little while later. Incidentally, with that same friend, we both got a job at the same studio.

And yeah, that was the start of my career, really.

Paul

That's pretty cool. Thanks. Adafruit community members might know you by your nickname squid.jpg. How did you pick that out?

Aaron Pendley

So I have been a fan of this video game, this Nintendo video game named Splatoon, probably since 2017. And originally that was my name that I used whenever I played Splatoon. And after a while, I joined Twitch with the hopes of finding other people to play Splatoon with.

And eventually ended up streaming a little bit as well. So that's kind of like the name I became known by, and it's the name of my Discord. And so it just kind of stuck.

Even now, what's kind of funny is that a game that I made on iPhone is my avatar for a lot of things as well. I mean, this game called Cow Trouble after I was kind of done with the industry at large. And if you go to the Aidford Playground page right now, you'll still see the little icon of the farmer guy who's the main character in our game.

Paul

How did you discover CircuitPython?

Aaron Pendley

Probably it was around 2020, early pandemic days. I was bored out of my mind. And I wanted to do something that reminded me of some work that I had done in a job previously where I worked with vending machines.

And basically at that job, I wrote iPad apps that would interface with vending machines in various ways that our customers who were vending machine companies, like their technicians would use them and their drivers and stuff like that. But that was my first experience using an Arduino. We would sometimes use them to simulate the vending machine so that I could write my software when I didn't have access to like an actual vending machine.

And so, yeah. So when the pandemic came around, I was very bored and I had a lot of fun doing that. So I thought, you know, I'll buy the Arduino student kit and I'll learn a little bit more about this Arduino stuff.

And so I did like all the basic things everyone does, you know, like LEDs and potentiometers and seven segment displays and all that stuff. And eventually it just got to the point where the programs I was writing were too big to fit on an Arduino. And at that time, I had already bought, like, some basic components from AtaFru.

So I had some kind of awareness of who they were. And plus, you know, it's virtually impossible to work in the Arduino ecosystem without coming across ATAFru libraries. So I looked around on their page a little bit, and they just started selling this really cool microcontroller called a QDPI.

I'm using the San D21 shit. And they were $6 at the time, which, you know, the cost of an Arduino was multiple times at. So when I came across those, I was like, well, I'm going to buy a bunch of those.

I didn't know how to solder, though, was kind of a problem. So I also bought a pack of 25 breadboard neopixels and a soldering iron and just kept soldering until all that was done, and I knew how to solder. So from there, yeah, I just did a lot of various neopixel projects.

So where CircuitPython comes into it is one day I wanted to build a kind of a macro pad using arcade buttons. And the idea is, like, now that I'm using several different, like, There's, you know, X code that I used for my job and an Arduino at the time for doing Arduino development. I wanted, like, a set of buttons I could press that would be the same, you know, to, like, build my code or clean it no matter what environment I was in.

So, CircuitPython has the killer feature of just being able to plug into a computer, edit code, and the changes are instant. And that seemed perfect for that kind of a project. And it was.

If I remember correctly, I also soldered one of the little flash chips onto the Qiepie at the time to make a QDiPi Haxpress so that I had enough resources to do all of that. Yeah, that was my first Real Circuit PIPOP project.

Paul

Let's chat about some of the projects you've shared on your AidaFruit Learn Guide playground page. I think my favorite project of yours is the top secret lunchbox. How did this project come about?

Aaron Pendley

So I'm a big video game player since I was a kid, obviously. And one of my favorite kinds of games are these survival horror games. And kind of a key feature of these games is they typically involve kind of like ham-fisted lock and key puzzles or brain teasers that you need to solve in order to progress throughout the game.

A classic example would be like Resident Evil or something like that. And kind of aside from that, I also, you know, in the last like maybe 10 to 15 years like escape rooms, you know, kind of have branched off of that same idea. where you're kind of like in the game and you have to solve these puzzles to get out of the room.

So I've just always loved that kind of thing. And one particular game came out earlier this year called Lorelei in the Laser Eyes, which is kind of like those ideals distilled into, you know, to me it was like the perfect game of that type. You know, you're in a mansion and you have to solve all these puzzles and there's just like really cool kind of ghost story.

And so what I wanted to do, like coming off of playing that game, I was really inspired to try and make my own escape room puzzle. And so I'll confess it wasn't my first attempt. It was actually my third attempt at doing something like this.

My first two attempts, they were neat, but they were really, really too ambitious. Hardware-wise, software-wise, just conceptually, you know, the ideas were too broad. And so kind of after playing Lorelei, it kind of clicked with me that actually what I needed to do was distill, like, my idea for this down to a single interaction.

you know, like a core interaction that I could build puzzles off of it and make like a game. I also had around that time watching an episode of John Parks Workshop where he was doing this cool connect the wires type puzzle where, you know, you had to like connect the wires in a certain way to, you know, light the lights up and solve it. And so I kind of took those two ideas and mesh them together. And I made that kind of switchboard idea, the core mechanic for this lunchbox game. And yeah, from there, I was able to start prototyping things. The idea that I had was that I didn't want to like, I didn't exactly know what I was going to do at the beginning of it.

I had some rough ideas. And since I had attempted this a couple of times before, I could reuse some of my ideas from that. But, you know, going into it, I needed to still, like, prototype to make sure my game idea would work and things like that. So I used these cool, like, swirly board PCB things that Aidafruit cells that lets you easily attach, you know, all kinds of various microcontrollers and breakout boards. So I was able to bring up this project before even considering the design and the case and everything, you know, just functionality with just that and adding the functionality that I wanted in writing the program and bring up code. And then from there, once I knew everything that I was going to use, I could build my panel and my enclosure that I could stick into the launch box. And yeah, since that was like my third time doing this, this process at this point was a lot smoother. And so from, you know, starting to do the design work to actually having the full project built probably took about a week. The hard part honestly was writing the software for it because games are just kind of hard to write. So it took me about another three weeks to write the software for it.

Paul

So for listeners at home, can you describe when you open the lunchbox, what's inside of the lunchbox?

Aaron Pendley

So when you open the lunchbox, one thing you'll notice is how you turn it on. There's a little slot for a key. And so you need a key to turn it on. And then once it's on, various lights and sounds and things happen.

And so there's 10, like, headphone jacks, basically. And each one has its own LED. It's an RGB neopixel LED on the side of it.

And so basically, that's the core of the game. There's also, like, a little compartment where I can hold all the little cables so that they can travel around with it. And I keep the key in there, but kind of one thing that can be fun to do with is just to hide the key and present a clue to a player, you know, so that just adds kind of like an external elements to it. And then there's also an arcade button with a neopixel inside of it that I can use just for various interactions.

Paul

Okay, cool.

Aaron Pendley

Yeah.

Paul

Tell me about the Zapper Light Sound Mod project where you reused an NES Zapper from Duck Hunt.

Aaron Pendley

Nintendo made this cool game, Duck Hunt, you know, back in the 80s, and to go along with it, they had this cool Zapper gun, like this light gun. Fast forward kind of to today, and these guns can still be found pretty cheaply. You can get them to game shops on eBay, you know, ranging for anywhere from like $10 to $20.

But unless you're like a hardcore, like retro game enthusiasts, they're probably not very useful to you because you need an old school CRT TV to use them. So my thought was I wanted to take one of these and just kind of like take all the parts out that didn't really, that I didn't need and instead replace them with parts that would allow me to make sound effects and light effects or whatever. And so, yeah, a couple of years ago I took on this project.

And it was a very complicated project. It had several boards. There was like a ditsy-bitsy microcontroller and a battery charging board and an I-2S audio board.

And I had to take flush cutters to the inside of the shell and cut out all kinds of bits so that I could fit all of this in there. And it was kind of a complicated film. And for whatever reason, a couple of months ago, I decided I would go on Aida Free Show-and-Tel and finally show it off.

And so, yeah, I was showing it off. And Liz Clark asked me if I was going to write about it. And I was like, well, I hadn't really planned on it.

But yeah, let's go ahead and see what I can do. So I took the Zapier that I had made and opened it up, and it was a nightmare. As much of the nightmares it was to build is even more of a nightmare to write about and to try to relate to somebody how you might actually replicate this.

So instead, I decided to maybe take this opportunity to try and redesign my mod to make it more approachable and to take advantage of some things that I didn't have a couple of years ago. And one of those was a 3D printer. Since then I got a 3D printer and I learned how to do some basic CADs, you know, stuff.

And another thing that happens, Adafruit released probably like my favorite microcontroller. It's the RP2040 prop maker feather. This board already had everything that I needed, all those other boards to do.

So my idea was that I wanted to make a mod that was easy to do and was not destructive to the shell. So, you know, for whatever reason you regretted it and wanted to go back to having, you know, that. the original Zapper, you could do that.

And what I did was there's a little piece of geometry on the bottom of the grip where normally the cable strain relief is for the cable that plugs into the NES. If you take that out, you can 3D print a piece of geometry to put just a slot right back in there, and it makes like a great base or like fixture for anything you want to put there really. So I kind of extended that into a box-like enclosure.

And from there, I was able to put a switch and a battery and the prop maker feather into. and wire all the rest of it into my speaker and my neopixel and the trigger mechanism of the Zapper. And from there, that was much easier to write about.

And, yeah, I was able to write that guide and put it out. And it's probably been one of the most fun projects I've ever worked on. So I'm really glad Liz kind of gently prodded me to revisit it and do that.

Paul

So when you press the trigger, what happens?

Aaron Pendley

So the trigger has a really neat actuator mechanism where when you pull the trigger all the way back, it has like an auto release. So that's like the classic kind of, you know, click mechanism that everyone associates with these weapons. So what it actually is, it's just a simple, you know, just a simple button, really, except for that mechanical thing.

So when you barely pull the trigger a little bit, that's when it actually makes the connection and closes the circuit. And then if you pull it back the rest of the way, it clicks back and opens the circuit again. So the way I actually programmed it is when it first detects that closed circuit is when it plays the sound effects and shows the lights because typically you're you're mashing it all the way.

But those mechanisms are pretty old by now and they don't always work. So I wanted to also, you know, I did it rather than making it when the circuit opens again to play the sound effects. I did it when it opens so that you could pull the trigger more slowly and it would catch it if you were having issues with that.

Paul

I'll make sure that I link to all of these projects on the Aterfruit Learn Guide system too.

Aaron Pendley

Great, thanks.

Paul

I like on this next project that you confess that you don't love to play video games with a keyboard. What did you build to help with that?

Aaron Pendley

I was playing Xcom and using the keys to control the camera and that uses the Wazdi keys like most PC games do that use keyboard. But I've never really been a fan of that because it hurts my hand really. You know, it causes a lot of cramps and some of just like the configurations you have to put your hand into to hit some of the other keys too can be just really uncomfortable. So as I was playing XCOM too, it dawned on me that I could probably take a wee nunchuk and plug it into this cool little adapter that Adafruit makes, pair it with a microcontroller, simple microcontroller, and just reprogram it to remap it to those keys. And it worked out really well. I just slammed out a little 3D printed case for it and put it all together and wrote the code and it worked so well that I figured I would write about it as well.

Paul

I know this next project is done in Arduino, but you mentioned it could be possible to do it in CircuitPython 2. What is the Wi-Fi Matrix Keypad Remote?

Aaron Pendley

So the only reason that I actually did this project in Arduino is definitely possible to do this in CircuitPython. But the main thing is that CircuitPython typically when you boot it up, can have like a two to three-second boot time. And so what I wanted to build was like I have maybe a couple dozen or more various lighting devices around my house that I build with microcontrollers.

A lot of them using W-LED as well. And I have an MQTT network, like a local network that I've got all these plugged into. But no real great way to control them.

I could bust out my phone and use W LED's interface or some other things. But what I really wanted was just something I could pick up, press a button, and turn on a light or turn on all the lights in my office or change the theme of the lighting or whatever. So, yeah, the main reason that I went with Arduino is just because it boots up much more quickly.

And given that I also had to connect to a Wi-Fi network and then connect to the MQTT broken. I wanted, you know, to try to shorten that wake up time as much as I could. And so as it stands right now, it only maybe takes two seconds tops for my devices from the time I picked them up to when, you know, they're ready to receive input.

So I think that worked out pretty well. And really just with CircuitPython, it would have doubled that time. And so that's kind of what I was trying to minimize.

Sure. But yeah, this remote, you know, I'm not a big fan of touchscreens. And I'm not a really big fan of using my phone to control everything.

you've typically got to pull your phone out, find the app that you got to use it, wait for it to initialize. And then, you know, at some point between five and ten seconds, you might be at a point where you're ready to, like, press a button to make something happen. And so, yeah, I just, I really just wanted, like, you know, a remote, like a TV remote that you could pick up and press a button and it would just work.

And that was pretty much with this all. But one thing that I don't possess yet is the skills to design a PCB. What I kind of had to do was find a good alternative for buttons, you know what I mean?

It's not easy to find great, like, buttons that feel really good that are, you know, low profile that are easy to include into a project unless you're going to design your own PCB and find your own buttons to put on there and stuff. So this keypad remote, you're just the classic like 12 key key keypad remote that you see in movies or, you know, anywhere you go. It turned out to be kind of the perfect solution for this.

And yeah, I just connected it to an ESP 32 QD Pi, put a 500-mph battery on it, and a little bit of custom. code and I was able to make a few of these now. And I keep one in each room. Each one is customized to change the settings in each room.

Paul

I have a pair of the LED glasses from an Adafruit Adabox. Tell me about the custom firmware you created for these.

Aaron Pendley

I love those glasses. I remember getting that, getting that box too. And I just would devour every single demo that I could find, you know what I mean, trying to write my own. And so probably like the one thing about those glasses, though, is if you want to take them out and show them off, you're kind of stuck with one mode, you know what I mean? There's a lot of great examples out there, but there's nothing that kind of consolidates it into, like, one package where you can go and change the mode on the fly, you know what I mean, or change it to react to whatever's going on in your situation. And so that was my main motivation for it, is it was around Halloween, and I wanted to take these glasses out, and I wanted to just show them off and all the stuff they could do. So I went and looked for all of my favorite examples and compiled them into this firmware and added a couple of my own and added a couple of features that are probably like over the top and ridiculous but I think they really make it a lot more fun to use and one of those is integration with the Adafruit Connect app on phones and computers.

So you can connect to it with the app and you can change the modes, you can change the colors and do all kinds of customization with that. And then kind of like as a further, you know, ridiculous stretch goal. I also integrated a Bluetooth Nunchuck adapter with it so that you could use the nunchuck to kind of puppet the eyes and the glasses or do various things depending on the mode.

And so kind of one thing that I didn't like about this project, kind of the downside a lot of times to using Arduino or something like Platform I.O. is it's not always easy to just put this in somebody's hands who just wants to see something cool on their devices, right? So, yeah, if I'm someone and I bought these glasses and I'm looking around, I'm probably just going to want to take the things that I can drag and drop and put on there.

I don't want to, like, download platform I owe to figure out how a compiler works and all this stuff. So this was a cool project, too, because I figured out how to take that and bake it into a UF2 file so that it works similar to, like, CircuitPython. You could just drag and drop a file onto your device, and there it is.

And I was really glad that I did that because probably, like, the perfect demo of this firmware came a couple weeks later when Noah Ruiz on his 3D printing show was kind of showing off a prototype that he was doing. And he basically just went through the whole firmware and showed off everything. And, yeah, it was just, I was just smiling the whole time.

It was so cool to see that.

Paul

I bet. I think my favorite effect is the Cylon from Battlestar Galactica, where you've got the red LEDs going back and forth.

Aaron Pendley

Yes, I love that one, too. I think pretty much every device that has LEDs on it than I can, I ended up putting that on there.

Paul

Last question I ask each guest, you're about to start a new project. Which microcontroller do you reach for?

Aaron Pendley

Definitely the prop maker, a feather. It's got most of the things that I typically want to do, which is audio support, neopixels, even servos if you want to use those. It's just kind of perfect for that kind of thing.

There is like a runner-up, though. When I need Wi-Fi or something like that, I will also reach for an ESP-32 S3 typically. They're great for CircuitPython.

They're fast. They have tons of resources. Aside from Wi-Fi, you can use ESP Now to communicate with other ESP-32 devices.

Yeah, they're just fantastic.

Paul

I agree. I think the S-3 is typically my go-to pick when I need Wi-Fi as well.

Aaron Pendley

Yeah.

Paul

Aaron, thanks so much for being on the show.

Aaron Pendley

Thanks for having me, Paul. It's been great.

Paul

Thank you to Aaron for coming on the show. To learn more, visit the show notes to see photos of Aaron's projects, links to his Adaruit Playground pages, and his Blue Sky profile. For show notes and transcripts, visit www.circuitpythonshow.com. Until next time, stay positive.
