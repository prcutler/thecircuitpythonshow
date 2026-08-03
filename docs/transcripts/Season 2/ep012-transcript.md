---
date:
  created: 2022-06-27
title: "Episode 12 - Guy Dupont"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep012.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode I'm joined by Guy Dupont.

Guy is a software developer, audio engineer, artist, and seltzer aficionado. Guy, welcome to the show.

Guy Dupont

Thank you very much for having me.

Paul

I wanted to ask you about your Subaru backup camera project that you released a couple months ago. I watched the YouTube video and got such a kick out of that. How did that work?

Guy Dupont

Yeah, so that project's interesting because it actually dates back to, before I got Mary, when was that? 2018, I think. And it was my first hardware project that I actually, like, put any real work into.

And, yeah, it came from an actual need, right? So if you haven't seen the video, my wife's Subaru had a, like, third-party backup alarm installed that when you get close to something, when you're backing up, it beeps the most annoying sound you've ever heard. And there was one day where we were parallel parking somewhere in Boston where we live.

And, you know, it was one of those situations where it took a lot of back and forth. And by the end of it, we were just cracking up because the sound was so annoying. And she turned to me and she said, if you can do anything, like, because she knows I like to mess around stuff around the house at that point.

I was just kind of getting into hardware stuff. I do a lot of software stuff. She was like, if you're going to mess with anything, mess with this, like make this better.

So, yeah, so I replaced the sound, the beeping sound with a recording of my own voice, making kind of like scared noises, like, oh, oh, oh, oh. And as you get closer, I get louder and more annoying. So yeah, so that project has managed to survive however many years in the car.

I just put out a video where I rebuilt it using some more modern parts, I guess. I don't know if three years makes that much of a difference. But yeah, more modern parts.

I just, you know, I designed it a little better because I know what I'm doing a little more now. And I made it so that you can add custom sounds, which is really fun. And I got a lot of good suggestions from the internet as well.

Paul

Oh, I bet. Well, it always helps with those kinds of projects when your partner encourages you to do it instead of like going against the grain and building stuff that just kind of annoys them.

Guy Dupont

Yeah, I don't get that very often. And especially because like for folks who aren't familiar with my projects again, like they're all a little bit tongue in cheek. Like all of them have a little bit of a kind of silly edge to them. And so yeah, usually when I'm doing something, it's not the most practical thing. You know, my wife rolls her eyes, but it's a good, it's fun when people get in the car and I get to show them.

Paul

And it's

Guy Dupont

fun. Absolutely.

Paul

What does the CircuitPython code in that project kind of look like?

Guy Dupont

So it's pretty simple. So basically, the way the sensor works is, I don't even know what the sensor is. There's something someone installed in the car and there's a little brain living somewhere, some little microcontroller, I'm assuming. And what it does is it just pulses a little buzzer. It used to be a little buzzer with 12 volts on and off when you're getting closer. So it's, if you know PWM is, it's like a very slow PWM where it's just on, off, on off. And so what you hear is beep, beep, beep. And so what I did, I didn't even look at what the sensor is. I didn't take anything apart. All I did was snip off the wires going to the buzzer. And I have the 12 volts, like the lines going into an optocoupler. I think you could also probably use a transistor. But basically, I turned it into instead of being used to generate a sound, it's used to toggle a switch virtually. The octocoupler is tied to a GPI open on a, I forget what I used. I used like a Seeeduino Xiao the little tiny boards. And so really what the code is doing is just looking for the pin being pulsed by the, you know, 12 volts, which gets converted to 5 volts. And I measure the distance between those pulses just by using the clock. So I just say time, now and, you know, figure out when the pulses are.

And since I know those pulses are a fixed space apart, you know, they get closer, but they're always the same intervals. I can basically say, if I detect two pulses between, this amount of time, I know I'm roughly this close, or the car is roughly this close to the thing it's backing in. And so I use that logic, and then I just send, I have a little MP3 player module also in there attached to a speaker. And I just say, you know, anytime I detect a change in the perceived distance, I just send a new sound to the player. And it's a little tricky because I wanted the sounds to sound as continuous as possible. I don't want things like restarting. So if you dig into the code, it's a little trickier than that, but that's essentially what's going in. I'm just measuring the time between these pulses, knowing that they are fixed within the car. The car only has a certain number of options, and then using the measured distance to trigger sounds.

Paul

Well, I'll make sure to include a link to those videos in the show notes as well for people who actually want to see how it works or see it on video. Hopefully the code is legible.

Guy Dupont

I'm not known for my Python skills, but does what it needs to do.

Paul

Tell me about the custom macropad that you created that uses CircuitPython. where you recreated Nokia's T9 predictive text so you can type one-handed.

Guy Dupont

This project has changed a lot for me. Not necessarily in terms of my job or anything, but just how I think about hardware projects and the stuff that I put out. So I have it here, but I'm not going to hold it up because we're on a podcast.

And I imagine only a certain percentage you are going to get to see it. So, but yeah, so I basically, I've always been kind of fascinated with T9. feel like my generation, like who came up, I'm 31. So we came up kind of the dawn of cell phones as a commodity, as a common thing. And the memories I have, like strongly tied to the cell phones are like stealing my parents and playing snake and, you know, sending messages to grandma or whoever was using phones. There's a thing I feel like with my friends and folks in my generation where people have said like yeah smartphones are amazing right but like there's something about texting t9 like people are really nostalgic for t9 and if you don't know what t9 is it's a very primitive predictive text algorithm so you know on those old phones you only had you know it's like 12 keys basically for the buttons and so t9 let you type full words using only those 12 buttons so yeah so there's a certain nostalgia for it and i think people genuinely felt like they could type faster than they can on a touchscreen and i get that because it's tactful and, you know, it was predictive text. It was pretty good. I was talking to folks about it and I was like, oh, yeah, it would be such an interesting thing to explore today, right? And I looked, and there are actually smartphone keyboards that you can download that are just the T9 algorithm baked in and you can use that, but I thought it would be really interesting to make a hardware keyboard because, like, I associated this with these old tactile devices where I wanted T9 built in in some way. It ended up being a pretty simple design. It's a very standard macropad design. It's just a key matrix with a bunch of diodes. I actually designed my macropad that I have available to support any dev board in the QDi Pi Jiao shape, including the ones with the RP2040 like mounted on the bottom. I actually have a cutout in the PCB. So I wanted it to be as flexible as possible. I wanted, you know, because I didn't know what I was going to be able to buy. So I tried to accommodate as many things as possible.

I realized that with CircuitPython, I could pretty easily implement all the T9 logic on the actual microcontroller itself. So that means when you plug this keyboard into a computer, you could just type on it and it will act as a keyboard like any RP2040 CircuitPython keyboard. It'll act like a keyboard to the computer.

But what it does is it replaces words as you type them with predicted versions of what you might. want to be typing. And the way it does this is it actually injects backspace characters very quickly to make it seem like the words are being replaced wholesale. But actually what's happening is it's just like typing a bunch of letters and then very quickly typing a bunch of backspaces.

So yeah, so the cool thing about that, one, I can write it in Python, because CircuitPython, which made it a lot easier to test and develop on my MacBook, whatever computer I want to be working on. The nice part about using CircuitPython is, since I'm writing it in Python, I can develop it and test it on my local machine. It's a relatively simple algorithm, but it's still, you know, it's a good chunk of code.

It was really nice to be able to iterate very quickly and get, you know, feedback knowing that things are working or not working before I even ran it on a microcontroller. And then, yeah, the fact that I can just drag the library file, so there's a file that backs all of the predicted words, right? I can just drag and drop that onto the keyboard and update that as I please. So that's been really, really nice. And to be honest, I felt confident enough in my ability to coach people through editing this thing that I've started giving them away, selling them. And it's so, I think that's a very profound thing that CircuitPython enables, right? Because I'm not, I'm not a hardware developer. I've written a lot of software, not all of it embedded. And so I'm kind of new at this. But the fact that I have this system where I can put this in people's hands, give it to a friend, give it to a parent who's not a tech person. And if they have an issue or they want to change something, I can just send them a file that they can drag onto the board and it just magically is good to go. That's huge. That's huge, right? Like, if you think about the alternative, like, if I had to push a firmware update, if I found a bug, like, how do you get that to people? And there are ways, right? Like, we have real products that do that. But to know that I could coach anyone, like, on an email, anyone to drag and dropping a file, especially when it's this thing that people are going to want to customize. That's so cool. That's like that's, that to me is actually, that's the most exciting part about CircuitPython. Because to be honest, I don't really like writing in Python that much.

Paul

What do you prefer?

Guy Dupont

I work as, and mostly with Kotlin and Java. So I've done a lot of Android applications. That's kind of been my primary gig for the past eight, almost 10 years. And even in school, the first language I learned was Java. Android, we did all Java for a while, then picked up Kotlin. Kotlin is by far my favorite thing to write in. I think a lot of Python folks would poke fun at the verbosity. Not as bad as Java, but I like my type system.

I like my generics, my covariance, contravariance, all that stuff. I want more of it.

Paul

One of the things that you did mention towards the end of that video is one of the other advantages that you thought CircuitPython offered over C was just development speed as well.

Guy Dupont

So like I said, like one, just being able to write the code, I have, if you look at the repo for this project, the code is set up so that there are basically different board. There's directories for every system that it runs on. When I say system, I mean like macOS, Windows, but then specific boards like RP 2040. I think I have a version that runs on the JOW, but not very well. So that's like a SAMD board. Yeah, so I have it all broken out. But the thing is the core of that code, like 90% of that code is just a single file that's the same across all of them. The point is the Python that I'm writing to run on my computer here is not very different from the Python that ends up getting run on the board. So that's one thing that makes it super fast, right? Like I would much rather be iterating on my computer and then when I know it's done, when I know it's tested, dropping it on the microcontroller and, you know, figuring out the whole other host of issues that come with the hardware. So that's one thing that's huge.

The other thing is just like, you know, Command S, like save, reboots. You don't have to compile, rebuild. That is, that's another huge, huge, huge speed boost.

Paul

So. A lot of the projects that you've done have been related to music and I can see a couple of guitars in the background. Do you play an

Guy Dupont

instrument? Yes. I play a number of instruments. Not super well. I don't think any of them. And yeah, It's funny. It's like folks have pointed out that a lot of my projects have some connection to music or audio. And like I never, I don't think of myself as like the music project person. But like it's obviously true. Like there's no denying it. And I think that's just like because I care so much about it. And it's just such a bit been a huge part of my life my entire life. So I just naturally gravitate towards things like that. So yeah, I play the guitar. I play the guitar on a bass. So, you know, I have a bass.

I can make noises with it, but respect to basses just because you can make noises on it, doesn't mean your bassist. And actually, my primary instrument is the drums. So I've been playing that longest.

I was in, you know, my high school jazz band, college pet band. So that's one that I actually have a little bit of real training on. And I do, so another music connection is I work not so much anymore, but I spend a lot of time working as an audio engineer.

That's kind of how I work towards a lot of the projects I'm doing now, too, is I spent a lot of time recording. I spent a lot of time working with other people recording and producing music. A lot of time in studios playing with all that fun hardware.

That's something that I love doing and do it whenever I can still.

Paul

One of my favorite projects that you did that is music related is you put a Raspberry Pi into what must almost be a 20-year-old iPod. Yes. What were some of the challenges with that project?

Guy Dupont

That project had so many challenges. Really, it was a fun project, but it's one that I don't look back on as fondly as some of my others, which, you know, I love what I made. I think it's really cool. And I think that one has done exceptionally well in Internet land. I'm so very grateful for that. But because it was so challenging, like I don't look back positively on that experience and I have a hard time like diving back into that project, which I know I should.

Like you said, I took a Raspberry Pi Zero and I put it inside a fourth generation iPod. So I basically got it the iPod except for the click wheel. I really wanted to feel like I was still using a real click wheel.

So that was challenge number one was just kind of reverse engineering how the click wheel was talking to the actual iPod hardware and make it talk to my hardware instead. And fortunately someone, and I forgetting his name, I think is Jason Gar. had already figured out the pin out of the click wheel.

So it wasn't that bad, thankfully. And I used PiGPIO, just using it to like bit bang the input. So yeah, so I'm using the original click wheel.

I put a new color screen, one of the little composite ones from Adafruit in there. And then, you know, like a lipo battery and a little charger board, also from Adafruit, I think. It's very cool.

It looks great. when it's on and working, it feels great. But yeah, just like getting things to fit in small spaces is not a trivial thing.

You know, that was pretty early on in my hardware experience. So I picked up a lot of tips and tricks since then for how not to break stuff. And I broke a lot of stuff making that project and it lingers with me.

That one's still pretty painful. But yeah, and again, like to tie back to the Python thing, That was another project where I was able to do a large, large bulk of the development on my local machine rather than trying to get it to run right away on the final hardware. And that was really the first, like, bigger Python project I picked up.

Again, reluctantly, it's not my favorite, but it just, it was so clear with the Raspberry Pi and just, I used T, TK Inter, TK, I always called TKinter as a joke. But, you know, the Python UI framework for building the UI for that. Those were just obviously the right choice given the constraints.

And then there was a Spotify API library written in Python. Yeah. So again, I built it all on my machine and got it 90% of the way there before putting it onto the Raspberry Pi.

I highly recommend folks do that whenever you can. Like, you will be thankful.

Paul

So before we wrap up, I have a segment I call Turn the Tables. I, too, am a big music fan and I've got a record player on a turntable here at the house. But I've been asking all the questions. Here's an opportunity for you to ask me a question.

Guy Dupont

Sure. Can I sneak in two quick ones?

Paul

Let's do it.

Guy Dupont

All right. One, if CircuitPython wasn't Python, if Python disappeared from the universe, what would you rather be writing your projects in?

Paul

You know, Python's really the only language that I know. Now that I know enough Python, I can read other code, but it would probably be JavaScript. The first itch I scratched was building a web app for some friends of mine for a major league baseball pool, almost similar to fantasy baseball, but different. So since I started down that web-depth path, it would have probably have been JavaScript.

Guy Dupont

Yeah, I hope nobody unsubscribes to your podcast for this very hot take. But see, I secretly wish it was JavaScript instead of Python. I would take JavaScript any day.

But that's an unpopular opinion. Don't get mad at Paul for my unpopular opinion. Hit me up on Twitter if you want to fight about it.

Second question, what's the best set you've seen at First Avenue?

Paul

That is such a great question. And I have been so lucky to live in Minneapolis all these years. And for those that don't know, First Avenue is where Prince recorded the Purple Rain concerts that you see in the movie.

So it's kind of an iconic nightclub from that perspective. My favorite show, actually, is in 1994. I won tickets on a radio station called Rev. 105, Rest in Peace.

But I won tickets to a Best New Band Showcase. And I went and I saw some bands that I had never heard of. One was called Zuz's Pettles, which turns out their lead singer was the wife of Paul Westerberg from the replacements, which I found out years later.

And I saw this little band, little-known band called Pleasure. They blew me away. I've been going to shows for years, and I had never seen a band so tight.

They were a three-piece. I ended up moving to the East Coast a couple months later, and a friend of mine moved out about a year later, and I said, hey, whatever happened to pleasure. I'm like, I never really heard anything, and I really thought they'd make it big.

And I was working at a Best Buy store at the time, and he goes. out to the music area, grabs a CD and brings it back to me, and that was semi-sonic, who's, you know, known for closing time. Yep.

But this was their debut CD that he handed to me. I've seen some great shows there, but, you know, for a band that was just starting out, they were so tight, so put together, so polished, that it still sticks out in my mind to this day.

Guy Dupont

That's awesome. It's on my bucket list to catch a show out there. I have a number of Twin Cities friends and Twin Cities live music friends specifically. So I think it'll happen soon or rather than later.

Paul

Before we go, speaking of looking people up, if people want to look you up on the internet, where can they find you?

Guy Dupont

My YouTube channel is where I try to funnel everybody to, and that's just my name. My name is Guy DuPont. The spelling will be in the name of the show, I assume. And then I spend a little too much time on Twitter, and I literally have to use the internet to find my own Twitter username.

Paul

I'll link to it in the show notes. I'll make it easy.

Guy Dupont

Yeah, link to it in the show notes. It's my name, but the U's are V's. Gvy Dypont.

Paul

Guy, thanks so much for being on the show.

Guy Dupont

Thank you again for having me. It was a lovely chat.

Paul

Thank you for listening to the CircuitPython Show. For show notes, transcripts, and to support the show, visit CircuitPython Show.com slash support. Until next episode, stay positive.
