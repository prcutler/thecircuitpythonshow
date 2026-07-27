---
date:
  created: 2026-02-23
title: "Episode 54 - Sean Carolan"
---

## Show Notes

[Show notes available here.](../../episodes/Season 7/ep054.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Sean Carolan. Sean is a maker and gardener in upstate New York who enjoys playing video games and building projects with CircuitPython. Sean got his start with computers on a Commodore 64 and worked for Electronic Arts as a systems administrator. Sean works as a sales engineer for Grafana Labs, an open source monitoring and observability company. He lives with his wife, two cats, in a Shiba Inu near Albany, the state capital. Sean, welcome to the show.

Sean Carolan

Hi Paul, thanks for having me.

Paul

Glad you're here. How did you first get started with computers and electronics?

Sean Carolan

Well, as a child, I went to a computer class with my parents. They decided, let's go and learn more about computers. At that time, like, it wasn't really that common for folks to have a personal computer in the home. I was just getting started. And I took this class and I was terribly shy and nerdy, but I had a really nice lady instructor who took a liking to me and encouraged me. And she told my mom and dad, "Hey, you should get this kid a computer." So I was really, really lucky. And a few months later Commodore 64 showed up and I was, you know, love at first sight. I jumped right in and, you know, typed in the program from the magazine. And it's been a lifelong journey since then, you know, watching the technology evolve from these 8-bit machines, you know, to, you know, supercomputers that you hold in your pocket.

Paul

You've created a Pac-Man clone written in Just Circuit Python. Why choose Pac-Man?

Sean Carolan

Yeah, that's a great question. Pac-Man was one of the first video games I remember playing as a kid. You know, kind of a fun way to gauge someone's age. Just ask them, "What is the first game you remember playing?" You can kind of tell what era they're from. So, meet Pac-Man. It was in an ice cream parlor. And we walked in and there was this machine making beeps and boops and had color graphics. And this was kind of mind-blowing because before Pac-Man we had Space Invaders and Pong. And they were okay. But then all of a sudden there's this game with color and ghosts and a little guy eating stuff. I begged for a quarter to play the game and I've been hooked ever since. I've been playing Pac-Man ever since 1981.

Paul

Before we get into how you coded it, tell me about the hardware you used to get Pac-Man up and running, the Seeed WIO Terminal.

Sean Carolan

Yeah, so the Seeed WIO Terminal is a nice all-in-one microcontroller that comes with some fun accessories like a display, it's got a little joystick, a few buttons. even a light sensor on the back. And typically you'd program these devices with like Arduino or something. And you know, Arduino is hard. You've got to download the IDE and learn how to get the libraries in place. And I learned that this device was now supported on CircuitPython. So I flashed it with CircuitPython and all of a sudden it became really easy to program. With CircuitPython, you just basically edit a file, hit save, and then immediately it runs on the device. So it's a really fun little device for prototyping. I had it sitting in a drawer. I'd actually taken a stab at trying to build Pac-Man several months earlier. I got as far as moving Pac-Man with the joystick. There was no maze, no ghosts. I put the Wio back in the it's gotten easier to write code, you know, using like a coding assistant or copilot. So I thought, well, why not give this a try, you know, pull the device out. And I looked at it and thought, it's got a joystick. The screen's about the right size. This would look great, you know, running Pac-Man.

Paul

And so you were able to do that in just a day. How were you able to code all of Pac-Man in CircuitPython in under a day?

Sean Carolan

Well, I had some help. I did use AI and AI Copilot. So it was actually Visual Studio Code, which is your programmer's editor. And I used the built-in GitHub Copilot feature with the Cloud Opus 4.5 model. And it took a lot of iteration and different exploring different avenues and kind of like coaching the AI. I was able to build it in a day with this co-pilot assistant, sort of doing the very technical tasks like drawing the maze and working out the logic for the ghosts. And I ended up actually acting more like a QA tester, sort of architect/tester, where the co-pilot AI would write some code and then we would flash it to the device, and then I'd play the game for a little bit and see what happened. So that was the process. Starting in the morning and by evening time, I had Pac-Man ready to ship.

Paul

Where did you get the art assets for the game?

Sean Carolan

So the art assets came from a site called Spriter's Resource. Now this is a huge database of game sprites. A lot of them are commercially owned, though. So just a warning for the listeners out there. Don't try to take Mario and build a game and sell it, because Nintendo will send its lawyers after you. But you can use these assets for free projects, demos, proofs of concept, as long as you're not trying to commercially benefit from some licensed character. It seems like it's an okay thing. So Bandai Namco, please don't sue me. I love Pac-Man. This is a tribute to your awesome game and I don't make any money from it. Anyway, Spriter's Resource. Check it out. There's a ton of cool sprite sheets that you can use. There are also some other sites out there too where you can get free sprite sheets. Another one I just found recently is called KENNY. This developer kind of makes money just selling packs of assets for people who want to develop games. So you can download some of them for free. If you want the whole collection, you pay. It's kind of really cool because I'm not a graphic artist myself. So it was really nice to discover that someone else had graphic titles and textures and things that you could use right away for your game.

Paul

That's pretty neat. I'll have to link to both of those in the show notes. How did you replicate the sounds in the game?

Sean Carolan

The sounds of Pac-Man are very classic. You know, they're sort of unforgettable. like the waka waka waka, you know, Pac-Man's eating dots. And there's a little music, you know, kind of a little jaunty little tune that plays at the beginning of each level to get you fired up and, you know, get the player ready to play the level. On the microcontroller, there is a little speaker. And so with these microcontrollers, you can actually kind of make beeps and boops without having to download an MP3 or a digital sound file. So I thought, let's just go retro. we'll just try it, see what happens. You know, if we send a signal to the speaker, you could tweak it to get different notes, right? And so I worked with, again, the co-pilot and said, could you make the waka waka sound? You know, and it's pretty close. You can hear it when you play the game, you know, Pac-Man just sort of doing that thing. And then I really wanted to have the music, you know, the start level music is so iconic and it just sets the Pac-Man mood. But the AI wasn't quite getting it right, you know. So I went and found basically sheet music, the musical notation of the Pac-Man startup song and fed that to the co-pilot AI. And then it was able to write the song like, you know, pitch perfect.

Paul

No kidding.

Sean Carolan

That little doo-doo-doo-doo-doo-doo-doo, like music that starts the level. It's very recognizable, right? who played the original game will go, "Oh yeah, that's the song."

Paul

Pac-Man also runs on the Adafruit FruitJam. How did that come to be?

Sean Carolan

That was entirely organic. And it's one of the things I love about working with open source software and frameworks is the community will pick up something and make it better. So my afternoon project on one CircuitPython device, the WIO terminal, became something that a whole lot more people can enjoy on the Fruit Jam. Because the Fruit Jam, you can hook it up to a TV, and it's got proper peripherals and sound and all of that. So I just got this notification in GitHub one day, and I looked, and someone had basically ported the entire game to the Fruit Jam and sent me a pull request, all tied up with a neat bow. And it was really, really a nice thing. So the community member, Cooper Dalrymple, he's relic-se on GitHub, took what I wrote and spent another afternoon porting it to the Fruit Jam. So this is kind of the beauty and strength of the CircuitPython platform. These are two completely different microcontroller chips, but because the code was written in this CircuitPython language, it was easy to map everything over. So Cooper was also able to get that version working in one day.

Paul

That's amazing. You mentioned that you used Copilot with Cloud Opus 4.5. What was your overall experience using AI? What worked well?

Sean Carolan

I'm kind of an AI skeptic, at least I was until so very recently. Previous attempts to code using AI didn't go well. This Opus 4.5 model though seems to have finally reach a useful enough stage where you can give it instructions, complex instructions, or even have it help you make a plan. And it gets eventually to the right answer. And so that was the game changer. Working with Claude Opus 4.5, I was able to just express what I wanted out of the game without having to worry too much about the technical details. So there are a lot of small details in Pac-Man that you'll notice if you study the game. Each ghost has its own personality and behavior. And they actually change the behavior from kind of go back to the corners, and then about 9 or 10 seconds later, they flip. And you can see the change in the movement. Like if you watch the game of Pac-Man, the ghosts will be sort of looking like they're just randomly moving. And then all of a sudden, the red ghost starts coming like, you know, for Pac-Man, like the Terminator, you know, beeline. You know, the other ghosts have complex, like AI that tries to chase, you know, four squares ahead of where Pac-Man is. Here's a pro tip. If the pink ghost is in front of you, run towards her.

Paul

Good to know.

Sean Carolan

Pinky will run away. So it's the one ghost you can do that with. Don't panic, just run towards Pinky if you get boxed in, and then you might be able to escape. That was one of the things I really wanted to replicate because the original arcade has the ghost AI that is unforgettable. And so I just told Claude, "Could you please make this just like the arcade, authentic AI?" And it knew what I meant. And that was really insightful to me. I didn't have to go explain or figure out, to go research what Blinky was supposed to do. And that all just came in organically. And then I was just able to test the game and play it and go, yeah, that looks right. That feels right. The ghosts kind of are acting the way they did in the arcade.

Paul

So it's really like you said before, you were the architect giving it the strict prompts or re-prompts to do it again. And then you just got to play it and be the QA tester over and over again.

Sean Carolan

Yeah, that's what's new and game changing, if I may make a pun about this whole thing, is that you can now write code entirely without an IDE, right, without a text editor, and actually build useful and entertaining software.

Paul

So that's what worked well. What were the challenges in using AI?

Sean Carolan

Oh, there were lots, especially in the beginning. I spent a ton of time just trying to figure out how to not get the ghosts to get stuck in the walls. It sounds silly, but these are the things you have to account for, you know, in an arcade game. It's like, well, where am I allowed to move? And, you know, in every loop of the program, you have to detect, am I touching a wall or am I close to a wall? So there were some weird bugs that emerged, right? Like Pac-Man goes out of the maze and just disappears. Whereas, you know, he's supposed to go through the tunnel and come back through the other side, right? So we had to iterate through that. Another bug that I found was that Pac-Man could get inside the ghost box. And in the arcade game, Pac-Man doesn't go in the ghost box. It's a one-way door. So each of these things came up and I had to tell Claude, no, can you please fix this or make it like this? It's not quite right. Yeah, so it's sort of weird, right? Because now the computer or the AI is doing the work. and you are the organic eyes and fingers that play the game and test it. It's a strange feeling, you know?

Paul

What recommendations would you have for someone interested in programming with AI?

Sean Carolan

Start small and pick a little project that you can tackle. I recommend a browser-based retro game. Because web browsers nowadays are very powerful. They come with all sorts of built-in stuff that you can do with JavaScript that lets you build almost any classic video game, especially Atari games. You might start with something like Breakout because it's very simple. You don't need a bunch of graphics because it's rectangles and a ball and basically some physics, right? but start small and have a plan. When you start to code with AI, especially cloud code, you can use directly in the terminal, or you can do this with GitHub Copilot too. But the first step should always be, let's make a plan. And most of these AIs will understand what you mean and go into sort of plan mode where they deeply research a topic and try to work out any kinks ahead of time. And then it presents you back the plan. So you can review the plan and say, yeah, that looks good, or I'd like to make some changes. Sometimes it'll even interrogate you a little bit. I noticed Cloud Code does this, where it'll say, do you want retro sprites for your Space Invaders game? Do you need a high score thing at the top? And it'll ask you some preference-like questions before it actually initiates and starts building stuff. Other point of advice is don't over-task the AI. Make it break all of the things down into stages. The way I was able to build Pac-Man in a day was just in little bites, again with the puns, but I can't help it, sorry.

Paul

No, it's all good.

Sean Carolan

Bite off a little bit at a time, right? And get something working and then iterate, add some more and keep going. And then, you know, you'll eventually get to the goal, right? But do it in smaller steps. So those are my pointers for like coding with AI.

Paul

That's good advice. If anyone wants to learn more about you and your work, where should they go?

Sean Carolan

I've got a GitHub pages site. So it's just scarolan.github.io. And that's got my portfolio and a bunch of stuff. You can also find me on LinkedIn, just search for Sean Carolan and I'll show up somewhere in the top five.

Paul

I'll make sure we link to that in the show notes as well. Last question I ask each guest, if starting a new CircuitPython or microcontroller project, which board do you reach for?

Sean Carolan

So it depends on the use case. If we're talking about like a wearable, I would go with the Circuit Playground. So Adafruit makes this gorgeous like round device that is so fun and it's got Bluetooth and NeoPixels around the edges. You can even use it without soldering. So you could take alligator clips to this thing or even like conductive thread, right? If you are into like textiles and sewing, you can literally like sew an interactive costume using a circuit Python. If it's a smaller like IoT device or something that needs to be very low powered, I'll typically go with like the Seeed Xiao. It's a tiny little, you know, like stamp sized microcontroller. Also the Adafruit QT PY. My go-to chip is like ESP32 S3. I like it 'cause it's got really good like deep sleep capabilities. So I actually have outside in the garden, a device that spends most of its time sleeping, but that's 'cause it's got a battery and a solar panel, right, so it just wakes up, it does its little thing, and then it goes back to sleep. And you can run all these things. CircuitPython runs all of them nowadays. It's amazing.

Paul

Those are great choices. Sean, thanks so much for coming on the show.

Sean Carolan

Hey, thanks for having me.

Paul

Thank you for listening to the CircuitPython Show. For show notes and transcript, please visit www.circuitpythonshow.com. Until next time, stay positive.
