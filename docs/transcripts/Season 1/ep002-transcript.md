---
date:
  created: 2022-03-08
title: "Episode 2 - Les Pounder"
---

## Show Notes

[Show notes available here.](../../episodes/Season 1/ep002.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. Today I'm joined by Les Pounder.

Les is an associate editor at Tom's Hardware. He's a creative technologist and for seven years has created projects to educate and inspire minds both young and old. He has also worked with the Raspberry Pi Foundation to write and deliver their teacher training program, Pi Academy.

Les, welcome to the show.

Les Pounder

Thanks for having me, Paul.

Paul

I'm excited to have you on.

You wrote two articles very recently that I'd love to talk to you about, both focused on the best boards of 2022. for CircuitPython, or RP 2040, I should say, and then some of the best add-ons for the PICO itself. What were some of the surprises that you came across as you were testing all this hardware?

Les Pounder

How versatile the RP 2040 is. I mean, we started off with the Pico, the $4 board all the way back January 21st, 2021, I think it was. And it just came out of nowhere.

It was Raspberry Pi's first micro-control aboard. And we just didn't know what was going on with this thing. What does it do? How do I use it?

And then the communities just sort of grabbed it. And we now see this plethora of boards that everywhere, all different shapes and sizes and different configurations, but all based on this one simple microcontroller, which, as we all know, is CircuitPython compatible, which is fantastic. It means we've now got really good hardware and really good software merged together to create some really great projects.

Paul

I think the PICO came in number one, which is no surprise based on how little it costs. Was there another board that kind of jumped out at you that you didn't expect to make the list?

Les Pounder

Hmm, good one that. So for me, I like the Pimoroni's range of boards. They have some really clever hardware considerations that they take into account.

So like the tiny 2040, so the first small Raspberry Pi Pico-compatible board. And it really was tiny. I mean, I've got one in front of me right now, and it's like a third of the size.

Okay, you don't get all the GPI-O pins. But what you do get is a curated list of GPI-O bins that you can do all the basics. So I-squared C, SPI, that sort of thing.

and standard GPIO stuff. It's smaller. It's a little bit more expensive, but you're paying for the privilege of a smaller package.

So you can stick it into projects. And I've seen people build robots with it. So we had a story on Tom's hardware about three or four months ago.

Someone had built a robot just with a tiny 2040 and a couple of motors, which were glued to the bottom of the board. There's no motor control board or anything like, no HBridge. It's just bare, run it from the GPIO, which everyone now is screaming.

No, use a motor controller. But it was just a bit of fun and it was cheap. Fantastic little project and a great little bud.

Paul

What do you think it was about the RP 2040 last year that led to so much success? Was it because it came from the Raspberry Pi Foundation? Was it just about being available in-stock compared to all the other supply chain woes? What's the secret sauce to that chip?

Les Pounder

I think it's a bit of both. It was something new. So Raspberry Pi has got a massive following.

I mean, they sold something like 42 million Raspberry Pi's since they started in 2012. It's 10th anniversary this year. in fact in about two weeks time.

Paul

That's amazing.

Les Pounder

They sold all them boards, and they're exceedingly popular, especially in the UK. So that's where I'm based in case when I was wondering. So Raspberry Pi has got this following, but also the chip shortage has sort of fueled the search for alternatives.

So STM 32 chips at the minute are like unobtainium. You just cannot find them anywhere. And it's even hit Raspberry Pi Foundation, sorry, Raspberry Pi trading, I should say.

So when they were doing their build hat for the Lego compatible projects that they were doing, so it's like an ad on board for a pie that has a microcontrolled that intercepts communication from the pie to the Lego components. They built it with an STM 32, which is what Lego uses in their original kit. The problem is you can't find them anywhere.

Even Raspberry Pi couldn't get any. So they pivoted and went to an RP2040 chip inside the build hat. So they're dog fooding.

They're eating their own dog food. And it works. It's a great little board.

And really should have pulled that out as well to show everyone. But RP 2040 is just getting everywhere. It's even in first-party Raspberry Pi accessories, and now it's in things such as I'm holding up to the camera now, PICO system.

So an RP2040-based games console from Pimaroni that works with CircuitPython.

Paul

That's amazing. And for those of you listening at home, I'll make sure to include those in the show notes, so you can also see some of the photos that Les is sharing with us. Going back to the Raspberry Pi Pico and the article that you wrote on some of the best add-ons, what were some of your favorite things that you saw there?

Les Pounder

My favourite, so all of them I like, but my favourite is something that is sheer simplicity, and it's the red robotics pico to pie. And this is so simple, but it's so expandable. So what it is, and I'm going to have it to the camera now, so everyone can see it while we're talking, and in the show notes as well, is a pico, which has been soldered to a PCB.

And then the header pins at the top of the board are Raspberry Pi hat compatible. So I can get a hat, such as Explorer hat, Pye Ruella, whatever. I fancy, put it on there.

And as long as I know how to interface with that board, so I Squared C, SPI, pins, whatever, I can use old hats with the PICO. This is really cheap. I think it's like under $10 with the Pico sold it on for you.

And it just opens up a whole world of messing around and playing. And it's all right, it's not the most technically impressive board. It's just pins that have tracks, connect pins together.

But it's so accessible for just reusing all that old kit that I know I've got loads of. And probably the people listening to this now are saying, yeah, I've got a load of Raspberry buy hat somewhere.

Paul

So you shared a photo of me of all the different boards you have. So we've talked a little bit about the RP 2040, and I'll make sure we get that photo in the show notes because it's impressive. What are some of the differences between some of the chip sets compared to the RP 2040 that we've talked a lot about? So you've got the STM that you referred to. There's the ESP series from Expressive. Help our listeners at home understand, you know, what are these different chip sets.

Les Pounder

All the different chipsets, all the different systems on chips, the SOCs, as they're sometimes called. There are all the different ways of having RAM, storage, processor power, and then such things as Wi-Fi or Bluetooth connectivity, all in a set package. So ESP, so Espressive, they have the ESP 8226, the ESP 32, which are well known for their Wi-Fi connectivity. If I had two more of these boards arrived today in the post form, you have to play

Paul

with, some ESP 32 boards. The 8266 is really popular. in the IoT world with people doing projects with things like Home Assistant, is that correct?

Les Pounder

Yeah, it's so cheap. ESP 8266 has been around for years, a hell of a long time now, and it's found its way into all sorts of projects. You can buy products in the store with an ESP 8-2-6.

I bought a light controller, an RGB light controller, a few years ago from the store. I took it apart because that's what I do. And I looked inside, and there it was, an ESP-8-2-6, and the debug pins and the control pins were all there ready to go, so I could hack it if I wanted to.

And yes, I have done that. It's a really nice sort of chip because you can also get these breakout boards. You can get one that's designed for a breadboard, or you can get one's called the Weimos D1 Mini, which are this unusual form factor.

It looks like a tiny Arduino, but they are great fun to just hack around with because, again, they're cheap. Even in the current climate where it's expensive to find chips, you can usually find them for about $4 to $8, depending on where you shop. And you can flash on a micropython, CircuitPython, and have a good bit of fun with these ones.

Wi-Fi-enabled chips.

Paul

For someone just starting out with CircuitPython, what board or boards would you recommend to them? What are the top couple to take a look at?

Les Pounder

For me, it's the Citron range. So this isn't biased. I've paid my own money for most of these boards.

Fantastic little boards. If you think of just a standard microcontroller board, you've got your USB interface, you've got your pin connections. There you go.

That's your dev environment to mess around with. With Citron stuff, they put on a few extras here and there. So if I just go to the camera now for the video, feed. You can see the centre of the screen. I've got a purple board. It's about four inches wide and about two inches tall. It's got a pico in the center of it. So this board the Maker Pi Pi Pico is $9. And we've got all the GPIO pins broken out in rows, either side or columns, I should say. I've got LEDs on those pins as well so I can see if the pins are active without connecting anything to it. So in a classroom environment or in the home, where if you're not comfortable with electronics just yet, this shows you what's going on. It shows you that are pins turning on and off to flash an LED.

We've got Grove connections. These things on the left and right, it's like a white polarized connection. We've got three to four pins inside them generally.

These work with Grove connections, so Grove components to make electronics a little bit simpler. So you can buy like sensors or PIR sensor, passive infrared, the same thing that's used in alarm systems, or you can buy motors, buzzers, LEDs, all that sort of thing. Plug them straight in.

But I'm to worry about which pin goes where. and initially the Maker PiPico and the other ones as well, there's another one to the left here, the RP2040 and the new MacaNano RP2040, they were all designed to work with MicroPython and they do, but they found their home with CircuitPython because of the ease of use of these boards and the use of use with CircuitPython. If I want to do something with, say, the MicroSD card on the MakerPyco, I just download the appropriate library from CircuitPython, put it in the Libs folder, and away we go.

Easy to do.

Paul

That's amazing. Is that the same board that you just wrote an article about in the last couple of weeks?

Les Pounder

The little one here, yes, that one there. That's about six days, seven days older article. And fantastic little boards.

So normally boards with this size, when you put them on a breadboard, you're very cramped for space either side of the board. You may have one column of pins and that's it. With this one, you've got two to three because cleverly, they've got right angles pins on the underside of the board, which means, I'd hold it up to a camera there so you can see, it's slightly narrower by about one row either side.

And that gives us just a little bit more space. But also, cleverly, we've got maker ports. Let's get this in short.

There we go. And these are Stemmer QT compatible connections. So Stemmer QT, we should be aware of from Aidafrey's range of boards, but if not, it's I squared C broken out into a proprietary connection.

It's like a polarised connection, just same as Grove, but very small. And there's even a Grove converter for this board as well, so you can use Grove components and StEMMA, at the same time.

Paul

And what are some of the examples of what you might connect via Stemma or Grove? What are the kinds of sensors that people might want to use with it?

Les Pounder

Oh, a lot. Oh, there's so many. So the first one you'll think of is sensor temperature.

Usually temperature, light, sound, the ones that we go to. That's what we experience in our common lives. We see light, we hear sounds, that sort of thing that we experience temperature.

So we want to log that and use that in experiments. But you've also got RFID readers, NFC, PIR sensors. You've got rotary encoders, you've got Pentiumometers, all of these things that can be, that will return of value when they're interfaced or interactive with.

And with Stema QT and Grove and Quick and Quest, which is Pimeroni's sort of version of Stemmer QT and Quick from SparkFum, you can just plug straight in and away you go. You haven't got to worry. And it's really easy to do and great fun.

So kids can get involved with electronics, the CircuitPython. And also if you're just starting out in electronics, it's a good way to sort of find your feet before you want to go into the big projects.

Paul

So I understand you just built yourself a CircuitPython project that you shared on Twitter. Elgado announced their new stream deck foot pedals and you thought to yourself, I can do that and do it cheaper.

Les Pounder

Yeah, oh yeah. I thought I can do it cheaper. And being a maker for it, yeah, I just want to make it anyway.

So you're going to hear some old man sounds now while I just go down and pick this thing up because it weighs a ton. Thank you. So I have my hand right now, a aluminium box or aluminum for the American viewers.

and it's got some guitar stomp switches on it. This is all heavy juice. It's meant to be interfaced with your feet.

So really heavy use. And inside here was the KB2040, the keyboard from Ada Fruit, with CircuitPython, and it was emulating a USB keyboard. And all I did was have shift A, shift B, shift C, on these foot switches.

So when I pressed it, it would change from one scene to another. So right now, how I'm controlling my OBS feed for the show is a Here we go. Let's go that in shop.

And that's another circuit pipe and device. Is that the Keebo? Yep. It is the Venus dust, the Kivo 2040.

It's actually an old one now because a new one have got Stemakutian, and mine has it, unfortunately. So I can control my video video video now, and I can go from one scene to another just by pressing keys on here.

Paul

And I'll make sure to include photos of those, but that looks almost identical to what a guitarist would use on stage.

Les Pounder

Yeah, so in my youth, my many, many years ago, I used to play guitar, not in a band, just my own personal pleasure, and I had stomp pedals, so I knew what parts to get. And I thought, yeah, I can make my own. Yes, I did.

I got something wrong, though, and I'm going to highlight a failure, because I love to highlight failures, because fail is our first attempt in learning. And that's something that a friend of mine, Carrie Ann Fielbin taught me years ago. This is a failure, because I should have had this line of switches in a triangle, because I've got size 10 feet in the UK, size, which means when I put my foot on here, I can get both of them at the same time.

Oh, sure. If I'd have done it in a triangle on the corners, so middle and then bottom, left, bottom, right, I'd have had a lot more space to do it. So that was a failure.

But it's nothing that a drill and a bit of time can't fix.

Paul

Well, it's the beauty of being a maker, right? We learn from our mistakes and we do it all over again.

Les Pounder

Yep. We do it all over again. I normally make more mistakes and then learn from those mistakes and do it all over again.

Paul

Hey, it's Paul. I'll get you back to the show in just a moment. I wanted to say thank you for listening.

If you like the show, please hit the subscribe button, write a review, or tell a friend. You hear that a lot, but it really does help. For other ways to help the show, visit CircuitPython show.com slash support.

Now, back to the show. So the other thing that you've been really into lately is retro tech. And going back to the computers of at least my youth, since I'm getting up there in age, and taking a look at the things like the Sinclair's and Commodore 64s. Tell me a little bit about your experience working with those lately.

Les Pounder

Oh, well, for the last just short of two years, I've been working with Linux Format. So Linux Format is a magazine in the UK and America as well, which focuses on the Linux scene. And I've been working with them for at least 11 years now.

And the last two years, I've been working on retro computing articles. So going back to the roots of computing. So looking at the Commodore 64s, the Amigas, the Atari STs, even further back, Commodore Pet, Apple 2, Sinclair computers, and showing how these machines were used in their time to do similar projects to what we do now.

Granted, what we have now is a lot more advanced and technical. We've got lots of better kit. But I never knew before doing my articles that the Commodore 64 had a user port that could be used to do electronics.

I had no idea. I was flabagasted when I found it. How does this work?

So I went to Tindy and I got a board to break out the connections, got a pin out, worked out what things went where, and then learn how to interface with those pins by using a series of pokes and peaks. So poking something into a memory register and then peeking to see what's changed. So it's a bit different to Python.

We just say no, LED on, LED, or that sort of thing. We actually have to know where things are. But it wasn't too difficult.

I mean, I did a personal blog post on this as well just as an aid memoir for myself to remember in years to come. And it's fascinating because basic was sort of the language of that time. It was Python, really, for the 80s. it was accessible to everyone.

It was simple enough to understand, but it could do some quite advanced things if you prepared to put a bit of time in. And, okay, sure, it couldn't throw around microcontrollers and motors and that sort of thing as easy as what we can now, but you've got fantastic results with very little code, maybe 20 lines of code to do something quite complex.

Paul

So out of all the computers that you've been going back and taking a look at, is there one that jumps out to you that's still your favorite all these years later?

Les Pounder

Completely biased, but Commodore 64. I was a Commodore kid. I went through the ranks of the Commodore 16 and Commodore 64, then the Amiga range, and it was then that I went off to the dark side of PCs, the 486 DX 33.

But Commodores are just, they've got excitement for me. It's the whole playground mentality. So everyone's got Commodores.

They're all talking about the games that they've got. But do we talk to the kids who've got Sinclair's? Well, not really.

But now we do, because it's a big open community of retro gamers. But it's fascinating. all this old tech is becoming new again.

Paul

I'll talk to Scott Shawcroft later in the season, and one of the visions that he has for CircuitPython is to take something like the Raspberry Pi 400, which has the keyboard all built in, all one device, and just plug it into a TV using an HDMI cable, which is almost the exact same experience we had as kids. So it's cool to see all the retro tech coming back, but at the same time, that vision is still being realized all these years later.

Les Pounder

Yeah, in the 80s, you turned on the computer and there you go, the basic interpreter was there, ready to go. And from there, you could type in your own codes to make something, or you could just load your discs or tapes in the UK, tapes with the main thing. And it's just immediate.

And what Scott's doing with CircuitPython, to make it immediate on bare metal is fantastic. So now if we get a Raspberry Pi 02W or a Raspberry Pi 0, put CircuitPython on bare metal, instant on. We can have kids hacking around in Python really quickly, really simply, but backed up by all this fantastic library that has neopixels, motors, sensors, all ready to go.

So the kids don't have to learn all that just yet. Of course, we want them to learn that. We want them to expand their knowledge.

But when you start learning something, you don't want to be inundated with all the technical stuff at once. You want the good stuff. That means you're going to keep learning and keep winning.

Paul

So I've been asking you all the questions. Now we come to a segment where I call, turn the tables. I'm a big vinyl record fan. I've got a turntable here at home. What question can I answer for you?

Les Pounder

Well, I'm going to throw one back to you because we've been talking about all the stuff of yesterday year. So vinyl is yesterday, but it's coming back really popular now. I want to ask you a question of, you're trapped on a desert island.

You've got all the creature comforts you could desire. So you've got food, water, heat, shelter, everything that will keep you alive. But you can only take one computer and its entire back catalog of games to entertain you for the rest of your life.

Paul

Which one and why? Wow, that is a fantastic question. the first one that jumps into my mind is the Sega Master System or here in the US, the Sega Genesis.

That was for me the pinnacle of gaming. I know I'm dating myself by that. But I have so many memories as a kid, as a teenager, and as a young adult when I first moved out of my house, my parents' house, and took that with me of playing American football or Golden Axe. There were so many games.

I was a Sega guy. I wasn't a Nintendo guy. So if I could just take one thing, that would probably be I don't need anything modern.

I have fun reliving my youth, whether it's with my record collection or some of the retro gaming stuff going on. I've been working on trying to build a stand-up arcade cabinet for literally 20 years, which is kind of embarrassing to admit to. But I love my retro tech, and I've always loved my Genesis.

I still have that original Genesis. And every couple of years, I take it out, and my wife's eyes just light up. It's so fun to go back to.

So if I'm stuck on a desert island, I know there's not hundreds or thousands of games, games for it, that's probably the one thing I'm taking with me. If it's not a Kindle full of books.

Les Pounder

I'd take a Genesis or something like that. So I had a Genesis, so in the UK it's a Mega Drive, we called it, and I had one. And for about a year, the only game I had was Altered Beast.

Yes, classic. Oh, I do not like that game anymore. It was the only one I could play.

So when I got Streets of Rage about a year later, I played that to death. And I mean to death, because I had. hated Altered Bees so much.

But then I got a Super Nintendo as SNES and Mario, Super R-Type, Super Contra or ProVetecta as it's called in the UK. All those classic games, Legend of Zelda, that blew me away. So the Genesis unfortunately got put to one side because it only had the two games, whereas the Super Nintendo had all of these fantastic games that were just coming out would just look better. And I enjoyed myself immensely. Probably far too much to do, you know, it may have

Paul

I think that goes for all of us, but at the same time, I don't think we'd be where we are today without both the retro tech and without the games. I think that inspired entire generations of folks to get to where we are today. Definitely. Tell me how you got into CircuitPython specifically.

Les Pounder

For me, it took a plane journey, and this is where we start a very interesting story. Well, I hope it's interesting for you. I was invited to PyCon in the US in 2018, along with, well, I shouldn't say along with, I was there to support a young man named Joshua Lowe. Joshua Lowe, you may know us all about code on Twitter.

He created some software called EduBlocks, which is a way to write Python code with blocks in a web browser. Very clever. Take a look if you can. And he was invited to go over to the States to talk about his project. And he did. I went to long because I was his mentor at the time. I was teaching him a bit of Python. So disclaimer, he now knows far more Python than me. He's a very clever lad.

But I went to the Education Summit at the start of PyCon, and I met Scott Shawcroft. And having a chat with him, and he says, oh, yeah, we're giving away some CircuitPython boards. And I'm like, what's CircuitPython?

And he hands me, this thing is about an inch in diameter, this tiny board, a Gemma, M0, especially made for PICOM. And it was my first CircuitPython board. And it was like, oh, right.

So he explains about MicroPython CircuitPython, the link between the two. and I then went into a session with Scott and Katney and I learned how to do some very basic CircuitPython work with RGB LED, so NeoPixels. And it just sort of got me hooked.

So when I got back, I ordered a circuit playground express and then I just went a bit mad and I've got lots of different boards now. And it just sort of clicked in my brain how CircuitPython worked. So I've used micro Python before.

I've got one of the pie boards, one of Damien George's original boards. And that worked well. and I enjoyed it, and I still use micro python, but CircuitPython for Midge was just like an abstraction which made sense.

It took away the complexity for the user, and they've got these cool little boards that can use crocodile clips and all sorts of connections to make some really cool projects. And so I just had fun. And in that session, just making LEDs turn on and off with CircuitPython and learning how it all interacted with everything.

And then speaking to Nicholas Tollabay, who created the Mew IDE, and he showed me how it works with CircuitPython. It was like blowing away because Mew was so simple, CircuitPython was so simple, the hardware was so simple, anyone could do it. So we all got in our swag bags at this PICOM, these $8 Gemma M0 boards to take away and play.

And it just started the whole thing for me.

Paul

So it seems like Neopixels and the Circuit Playground Expresses are almost like a gateway for lots of people coming to CircuitPython.

Les Pounder

Oh, yeah. Yeah, Neopixels, I have a deep love for. I use them all the time, and I'm not even joking.

To my right in front of my television, I've got a cutie pie which controls the beauty lights where you see over a mirror in like a movie studio, and there's neopixels inside them because I swapped out the LEDs. So now it glows around the television, these are lovely bright colours. At Christmas, we'll have lights in the window, and we'll have neopixel lights.

The tree is fully neopixiled. Everything's neopixir. We've got a star that has W-led, so I can control neopixels remotely from my phone anywhere in the world, with MQTT and different topics.

Fantastic. I love Neopixels. And when Circuit Playground Express has them on the board ready to go, as do other boards as well, it's like, okay, that's instant brain candy.

Paul

Les, thanks so much for being on the show today.

Les Pounder

Thanks for having me, Paul. It's been a pleasure.

Paul

All right. Check out Les's writing at Tom's Hardware and Linux Format. Thank you for listening to the CircuitPython show, an independent podcast with the people in and around CircuitPython.

Speaker 3

For show notes, transcripts, and to support the show, visit CircuitPythonshow.com. I'm your host Paul Cutler, and I'll be back next episode. Don't forget to hit subscribe and stay safe. You know,
