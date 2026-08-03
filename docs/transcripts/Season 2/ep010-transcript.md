---
date:
  created: 2022-05-30
title: "Episode 10 - Pierre Constantineau"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep010.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Pierre Constantineau. Pierre owns Blue Micro, which creates and sells custom mechanical keyboards, macropads, and more. Pierre, welcome to the show.

Pierre Constantineau

Hi, Paul. Thanks for having me.

Paul

Glad to have you. Let's start at the beginning. When did you first get into computers or coding?

Pierre Constantineau

Well, it was actually quite a while ago. My parents, my dad mostly bought me like a ColecoVision Adam. So that was like early 80s, and then that was a very short lived computer, but it was a computer that I started like just basic programming.

And then after that, I kind of like abandoned it and just got a PC and just started using it and went to like high school, university and then. But I was always in the RadioShack catalogs and like kind of like almost like lusting it were like resistors and so on. But then when I got into college, I actually first got into.

to a course of electronics. And it was probably the first maker space, and that was like in early 90s. It was kind of like the maker space at a time where you can learn about just basic electronics and digital chips. And then during that same year, also did like a Turbo Pascal course.

Then went on into university. And then at that point, I thought I'd wanted to go, like at the high school, I wanted to be all chemical engineer. And then college, oh, I want to be electrical.

and engineered, then first got into, like, really my engineering degree, and then, oh, no, okay, there's this material science course that I think I like even more. I went to do material science as a career, and it wasn't really material science, it was like, metallurgy, really. And then I kept on going, doing more studies and went into more, like, chemical engineering. And then when you kind of look back, all of the different studies and interests, well, now going today, what I do for electronics?

is really the marriage of a bunch of different things.

Paul

Let's talk keyboards. You have a Tindie shop where you sell a few different kinds of keyboards. How did you get into that?

Pierre Constantineau

Well, it started maybe about four or five years ago when I first started with it like just, I wanted to know about keyboards and mechanical keyboards. And I first started with like just a plain 60% keyboard, probably from L.E. Express.

Then moved on into building a split keyboard. And at the time it was like a like split. So essentially a smaller keyboard that's literally split, it can be a little bit more ergonomic.

And if I can go in it, it runs on two different controllers. So if you can look inside right here, they're pro-micros. So pro-micros really, they're probably still one of the most common chip for making keyboards.

They're getting harder to get because of a chip shortage these days. And that's how I got into keyboards. But then a little bit later, there was a, like, a fellow on Reddit on one of the mechanical keyboard Reddit that kind of like said, oh, here's my split keyboard that uses two feathers, an RF 32, like the original feather.

And they made himself a split keyboard all wireless. And like feather like this is actually pretty neat. And I thought, oh, wow, well, I've got this whole keyboard, like that lead split that I talked about, and it uses the pro micro.

And I thought, ah, I've got to make myself something to fit on there. Because, like, a feather wasn't really used for pretty, like, I'd say, 99%. If you build your own keyboard, it was very likely going to be using a pro micro.

So I thought, okay, I've got to build myself something. And that's where I can, like, first started the blue micro. blue for Bluetooth and micro for micro size.

So that's where the name comes from. And I create literally this blue micro here, and I'm just going to go back into here, literally to make them fit just as a one for one replacement. Obviously, they're bigger because the modules are not very small, and then they're smaller than the ESP 32, But they're definitely larger than the pro micro.

And then that's when I first really started, okay, I got to build my own firmware for this because the existing firmware for the AVR boards, like the Arduino-based boards, they don't really fit because this is an arm processor. And even if you look at some of the common firmware, like QMK, they might have a branch and area where, oh, yeah, we support ARM as well, but it's very specific chip. And if you go outside of that, it's not supported.

And then the complicating factor with these is there's a Bluetooth stack on it that's a Nordic firmware. It's a bit like a bias for computer. Well, there's essentially a bias that takes care of all the Bluetooth things.

So that gets flashed to the chip. And the interface to it, the software and dev kit, the licensing isn't quite compatible for QMK and a library. So there's been more like legal reasons and technical reasons for people saying, no, no, I don't want to go there because it's one of those kind of worms that, okay, let's not touch it because it just might be a mess.

Or if somebody comes bagging up, okay, it's not going to be there. So we had to look at, okay, what do I do? So I first looked into, okay, let's get like just a plain SDK from Nordic and just try to see if I can build something.

And it was just impossible. It's like after like hours of just trying to get a blinky light. It's like, ah, okay, that's just too complicated.

And just kind of looking back, well, there's that feather. It's like, it's on Arduino. Within minutes, I had it running.

Well, yeah, minutes. I had it running on here. So that made it like, okay, going from hours or work with no success to minutes with, okay, something that flashed on here, I can make a light blink.

I can build a whole lot more on this.

Paul

There's nothing better than that first feeling of seeing that blinking light, no matter which program language you're using or what board you're using, that sense of accomplishment. It always feels so good.

Pierre Constantineau

And then after this, so this is really where the blue micro firmware really came because I essentially took the, I got inspired from QMK and said, okay, I want to build something that's flexible enough for other people who want to build their own keyboard to be able to just say, I want to just drop in that blue micro and just go on and have my own keyboard. So I kind of built my own firmware and then added a fair bit of functionality over the years. And I just kind of looked back.

And it was almost four years ago when I first had my first commit to GitHub on that. I actually forked it from like that first code that the Reddit, like I on Reddit had. And it was like, completely different from what it looks like today.

But then after that, obviously the 840 came along, which kind of brought in USB. So nowadays, it's like it's like a full keyboard. It's actually pretty neat.

Paul

So you started with Arduino. What actually goes into making your own keyboard? When I look at some of the kits, there's the firmware piece, and then there's like the overlay software to help program it, and then some of the kits require soldering.

Pierre Constantineau

So let's just say this is probably my first keyboard. that I've actually built with Blue Micro. So it's essentially a 60% as well.

And for those that, like, don't quite understand 60%. So you've got, and I'm just taking like my wife's keyboard here. So you've got a standard size, which like 110 key, well, remove the numpad, and you've got what's called it 10 keyless.

But then remove the function. key in the navigation, then you get 60%. So it's like close enough like 60 keys over 110, close enough to 60%.

And then so my first keyboard was literally a 60% that I actually plugged in a blue micro underneath and obviously you need a battery because it's wireless. So, but this actually this PC board is essentially not even my design. It was somebody, I don't even know his name, but it's like 40% club on the internet.

So if you just go 40% dot club, you'll have a whole blog of somebody who builds just keyboards, one-off and just documents it all. But he actually makes those, his design open source. And I got myself the keyboard and then soldered in all the diodes.

And then you can see here, this is the format of a pro micro. But how do you go from like a pro-micro width that is on here to essentially, well, 61 keys? Because if you look carefully, pro-micro only has eight input-output pins.

So going from eight-input-output pins, this is where the firmware and the hardware, the design of the keyboard really kind of comes in. So the firmware must know, okay, one, which pins are connected where, and then also which in what organization. Let's just take the example of the Aedofruit Macropan.

I think a lot of people will recognize this. Well, this is probably the simplest, if you just disregard the screen and the rotary encoder. This is probably the simplest because literally what you have is 12 different buttons connected to control it.

So it's a one for one, a pin to a key, and well, a key is a button to switch. It is probably the simplest because you only have like one to one, it's 12 and then you've got enough pins. How do you go from 12 to 60 or 87 or even 100?

Well, this is where you need to have a matrix. And in a matrix, what you do is you essentially have rows and columns. So here's a keyboard with 75 keys since you've got columns and rows.

So each row will be assigned a pin or an input. And then each column will be assigned another pin or another input. Now, typically the way it works is the matrix, either the rows of the column are going to be an input, the other one's going to be an output.

So that this way you can scan one row at a time and read the entire set of columns. And then you just say, if I turn on this row, read all columns, and then there's a match. Oh, that's because you have to have.

key here. So what you need to do is to scan over all the rows and all the columns to say, am I on, I am on, am I on? And then you have your entire matrix of keys of 100 or 80 or 60, all depending. That's what powerful controllers, microcontrollers do, is really do all the scanning.

It's constantly scanning. And that's the first part that the firmware must do is to understand what that mapping between how to scan. So is that my only scanning just pins or a matrix?

And how is that matrix organized? Because obviously if I have, let's go back to that one here. So if I have 18 pin on the pro micro and then I have 61 keys, okay, well, there's multiple ways you can go and divide those.

So 18, it could just say, okay, well, I have 10, could I have eight rows and 10 columns? and then that gives me 80 keys. But then if you count, you've got, I think, 14.

So if you do the math, like 14, that's already 14. You've got four pin left for the rows, but you've got five. That doesn't work.

So the way that this actually is organized, it only uses 16. So it's a matrix of 8 by 8, and it moves some of the keys around to give you a potential. and is 64 keys, even leaving you with two extra P to do other things. So if you look, this one I've got a little speaker, so it does beeps.

And it's got a MOSFET, so it does underglow lights. So it's got all 18 pins used for something.

Paul

Hi, it's Paul. I'll get you back to the show in just a moment. Thanks for listening, and if you're enjoying, Join the show, please tell a friend or write a review.

You can also support the show financially. Your support helps cover the cost of podcast hosting, recording services, and transcriptions. For more information, visit CircuitPython show.com slash support.

Now, back to the show. So you've been working with Arduino the last couple of years, and then last year you launched a new keyboard that actually uses Python. What led you to that?

Pierre Constantineau

Essentially, last year, like it was a great chip shortage of, well, we're still in it, so we can't just. say 2020 or 2021. But last year the RP 2040 came up came about a lot of the other chips, including the NRF 52s, were getting scarce. So I thought, okay, I got to do something a little bit different. And then this RP 2040, like Raspberry Pi, they've made it really, really simple to build your own PCBs and chips because they've got a really great guide on, Here's how to design your own device with the, with the RP 2040.

They've got a, essentially a hardware building guide. And they even have a Kikad set of file that you can use as a reference. I said, okay, well, I got, like, I know how to build keyboards.

I know how to design keyboards. I've done quite a few. And I thought, okay, well, let's just take the RP 2040 and just, like, put it all in.

And it all kind of about. But then, like, for example, like at work, this is, like, I used my keyboard and it's just like, it runs. It's got, okay, I don't use the RGB, but it's got RGB and hot swap sockets and all the nice and sexy things nowadays.

But I built it and said, okay, well, let's make it like available and it's actually open source, but I do have quite a few available if anybody wants some. But it's, it's, and I actually created it and it's like, okay, well, with circuit Pycom. Just previously to that, I actually put my microphone controller on there, like the W micro H40, and it was really simple.

So it was, like, I really, really can't attest how simple Scott and the editor for the team has really made it simple to take your own controller, take an example that already exists, and then just say, okay, the only differences are these. I push it up and then I think the most complicated thing was actually getting all the documentation lined up to be able to get my own USB product ID for a disk because there's open source projects that can use those. That was the hardest part because getting the keyboard or the controller in and a circuit item was simple.

So the next step with the keyboard is like, well, I just need to do the same thing. And then that came along. I've got this keyboard running CircuitPython.

And it was very, very simple to get it on there. And then I've even had people, oh, yeah, I want a bigger keyboard. And this is how, like, this one came along was somebody came last December and says, well, are you okay if I kind of like design like it larger?

And I said, yeah, sure. Like if you want to contribute it back and I'd be like, just set up a small production run. so you can have your own and we can test it out, make sure you're all worths fine.

So this is where the larger E7 came along. And they both run CircuitPython. They both, even setting up on QMK, or KMK was very simple because the examples are really simple.

It's just a matter you set up which pins are mapping to which rows and which columns, and then send disk key press whenever you, the deck that this key is the deck. So it was very, very simple.

Paul

Well, that's great to hear. How has CircuitPython helped you with troubleshooting?

Pierre Constantineau

This is where, like, when I went going back to Arduino, and if I even go back to the days of QMK, when you look at QMK, let's go to like the hardest, difficult start first. If I want to create my own keyboard, or if I build my own keyboard, just even when I have it my own PCB, you're going to have a hardware problem. You could just say, oh, I have a short between these two pins, and then I've got like press a key, and then there's like three that are showing up at the same time.

If you have QMK that's like all a prepackaged firmware with no troubleshooting tools of any kind, then it's very difficult to figure out what's wrong. Then you go to Arduino where, okay, you've got to create a small program, compile it, and flash it, and then quite a few people are not comfortable programming. I'd say in the mechanical keyboard community, there's like really two groups.

There's those who like the keyboards and that's really what they're in for the keyboard feel. And then there's those leading programmers that, yeah, they're not scared of diving in and doing programming. By selling a number of keyboards and chips and having that firmware, like having troubleshooting tools handy, to be able to troubleshoot your own keyboard when something on the hardware does not work well is very useful.

I actually built a number of tools to be able to help people troubleshoot. Oh, well, is this thing working? Is it shorted?

Is it like just like not connected? So I've had a few tools there. But then I can't like look at CircuitPython.

It's like, oh my God. Like you don't have to compile anything. You just copy the files and it's like, is it working?

No. Oh, just change a couple of things. Is it working? Oh, yeah.

Okay. Found the problem. Found the solution.

It's so much faster to be able to iterate. Because when you troubleshoot, it's always like your mind is working, okay, do I need a multimeter? Do I need, like, try to see what's connected and not connected?

Well, you've got a microcontroller right there with all that spins already probing what you want to, like see. Is this connected to this? Well, you can ask these two bin, are they connected?

And then you'll be able to tell. So it's, with CircuitPython, it's a whole lot easy. to iterate so much faster on identifying the root cause of your problems and then moving on into, okay, I've got to pick up the soldering iron and fix this little piece or that little piece.

Paul

Well, that's great to hear. We're almost out of time, but before we go, I'm a vinyl record collector and I have a segment called Turn the Tables. I enjoy the pun.

I don't know if everyone else does. I've been asking all the questions. Now's an opportunity for you to ask me a question.

Pierre Constantineau

Yeah, I'm going to go a little bit different. like out of fruit has been going retro lately with all the floppy disk stuff but i'm going to go with a retro question here if you go back maybe in your childhood or maybe the first computer you have first computer game and if you would pay okay here's the one game that kind of like okay i played it from end to end or it was like the one thing that really kind of like hooked me or kind of like okay i've got fond memories off what would that be for me it would be for me it would be

Paul

Broderbund's Lode Runner on my Apple 2C. And it was a kind of a platform scroller, and you could drill a hole and the bad guys would fall in the hole, or you had to drill more holes to go get the gold that was there. But what I loved about it is you could design your own levels. And that was the first game I ever played that I could design my own levels.

And I remember just spending an entire summer just doing that over and over again and making it so, making it near impossible to play at times. But it was so much fun. If I had to go back, that would probably be the game that I would choose.

Last question, if you're going to start a new project, which microcontroller do you think you'll reach for?

Pierre Constantineau

It's going to be one of two, and I'm going to kind of like divide it maybe even four ways. So if I just want to prototype something very quickly that I don't want to design, like, my own PCB, I would either pick the KB2040, I've got a handful of them, or if I need more pins, I would probably pick a PICO. But if I need Bluetooth, I got to go back to the NRF 50 to 840.

It's got obviously it's got USB as well, but it's got Bluetooth. And I've got quite a few of those of my blue micros, but I could go for a feather or even go like the bare bone module, which I'm just going to pull out this one because I actually, if I build my own PCB, I could actually go and say, let's put the modules right on to build my own. next keyboard.

So, and this is probably an adventure. I've kind of like started last November, probably. For like a super thin keyboard, like very, very tin.

It was more of an experiment than just to say, let's see how low can I get it. And it runs again because it's based on my, on that same chip. I was able to load CircuitPython and get KMK running on it for a little place.

Paul

That's so cool. Well, we're out of time. Pierre, thanks so much for being on the show.

Pierre Constantineau

Thanks again for having me.

Paul

Thank you to Pierre for being on the show. You can find Pierre on his YouTube channel at Blue Micro Wireless keyboards. You can also find Pierre on GitHub and his Tindy store by searching for Blue Micro. For show notes, transcripts, photos, and to support the show, visit CircuitPythonShow.com. Until next episode, stay positive.
