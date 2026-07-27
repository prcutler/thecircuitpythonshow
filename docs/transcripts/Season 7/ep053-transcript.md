---
date:
  created: 2026-02-09
title: "Episode 53 - John Ellis"
---

## Show Notes

[Show notes available here.](../../episodes/Season 7/ep053.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode I welcome John Ellis. When John was six, his career ambition was to work part-time building robots and part-time working at McDonald's. Even in the 90s, he understood the practical duplicity of hacking as a passion while working a corporate job to get the drop on the latest Happy Meal toys. It guides him to this day. John started working on Apple IIe's in the only computer lab in his rural community, which luckily was run by his mother. He started by writing text adventures in BASIC and fixing floppy drives he had broken, sometimes using typewriter parts to get mechanical pieces to work. This grew into a career that required a mix of hardware and software hacking, even as the infrastructure moved to the cloud. Currently John is the CTO of the non-profit Indiana Tech for Progress, which finds ways to leverage technology in order to increase civic engagement on a local level. projects on his workbench include a Keurig that briefly caught fire, an intelligent but retro alarm clock for his kids, a continually broken SNES controller, and a Bluetooth controlled lamp made from a bottle of a since closed brewery. John, welcome to the show.

John Ellis

Paul, thanks for having me and congratulations on the new season as well. Thanks. How did you first get started with computers and electronics? So my story, and it's a lot like your previous guests as well started back in the 80s but it really started with my mother being the inspiration. So we were, as a lot of your guests were too, in rural parts of the country. I was in rural Midwest. My mom wanted to find a job at a local optometrist office and they asked her if she knew computers. If she could work the fancy spreadsheet programs that they were trying to begin to use. She had no idea but one important lesson that she passed on to me was say yes and step outside of your comfort zone. So she said yes and learned how to navigate an Apple II. And then when she went back to teaching, they asked again, "Do you have any experience with computers?" She said, "Oh yeah, absolutely. I had to do some minor repairs and work on the Apple II." They were like, "Great! We have a grant from the state to start the first computer lab here in the southern part of the state and we need someone to run it. None of the teachers know how to." So she said, "Yeah, sure, I'll run it." And so she got an extra large classroom filled with, I believe, over a dozen Apple IIe's, and I even had Koala pads. I had multiple dot matrix printers. It was fantastic. And so that's where I would spend my afterschool, before school, and summers was in this completely geeked out mad scientist lab, which was her classroom and often breaking things and then I had to figure out how to repair it, often with typewriter supplies. I did that famously to several floppy disk drives that she had. But also she would get in new software, so Broderbund wanted her to try out this new thing called Oregon Trail. They wanted her to try out the koala pads for this lab. And so from there I started to kind of learn how to not only use and implement the software and fix things, but also how to write my own text adventures. And from there, it kind of evolved into I knew how to repair, I knew how to fix, I knew how to work on these things. And I was surprised that people would actually pay me as I got into middle school to fix their computers and for small businesses, and that became a thing. And then after all, I was like, this could actually become a living where I could code, where I could write my own stuff, but I never knew quite how to angle that. And so I got involved in the startup scene here in the Midwest. One of the first ones was a company called ChaCha, which was you could text any question to their SMS number and get an answer back. It was a lot of people trying to cheat on tests, but also was Chuck Norris jokes. So I wrote an early, kind of not really AI bot, but the best facsimile I could come up with is like, human people are receiving these questions and answer, could I auto answer them back somehow? And that kind of gave me the bug on modern software as well as software as a service and cloud platforms and how to continue to grow and build these platforms. And that's where it's gone ever since then. But my roots and kind of my heart has stayed in those smaller machines where you can hack on not just the software, but the electronics itself.

Paul

You mentioned the KoalaPad, and I totally forgot about that until you said that, and it took me right back to being a kid again, playing with Apple IIs in a classroom environment.

John Ellis

I mean, it was amazing what they could do with so little. And that's another thing that's still with me today, you know, when working on like Trinkets or the M0s or the ESP32s, right? The Apple II was, and the IIes, were fairly simplistic in what they could do, but they had touchpad interfaces. They had all the modern trappings that we enjoy today, and they were able to do it with much fewer resources than what we've got right now.

Paul

One of my favorite questions to ask guests is, how did you get your handle Decker Ego?

John Ellis

So Decker Ego came out of Doom the game and id Software. So I was a big fan of John Carmack because it was amazing what he could do with, what he would say is high school math and then build an entire immersive environment around that. When John Romero released things like DoomEd and all of the hacking tools around it, I got super into not just playing Doom, but how do you hack it? How do you build new things with it? And thinking about the name of their studio, of id Software, I knew that was a kind of spin on Freud's id, ego, and super ego. So then I tried to take what I knew from Shadowrun, the RPG where you've got a Decker that has neural implants that lets them hack into the matrix and do whatever. So the Decker side of that cyberpunk universe, plus the opposite side, the rationality of ego as the post to id became Decker ego together.

Paul

I love it. You've created a few different projects for the Adafruit MacroPad. My favorite is the MacroPad Hotkeys 2. What was your inspiration in creating the project?

John Ellis

So in truth, I have very low willpower when it comes to not buying things on Adafruit. And when I saw that the back plane of it had like the Pioneer 10 golden plaque on it, as well as the image of the probe itself, and then it had that array of, you know, the 12 keys with the NeoPixels behind it and rotary encoder. It's like, I've got to have it. And I bought two of them with no real impulse in mind other than this was a cool piece of hardware. But it immediately, of course, brought to mind, like all of the keyboards that we have now are missing a numpad. And I was thinking to all of the games that I used to have or all of the software that I used to have that would rely on that numpad. It drove me a little nuts that it was on the right side as opposed to the left. And so this was, it seemed like to me, a perfect idea to use that as an extension of ye old numpad from former days. And they already had a Learn tutorial out there for how to do just that, which was really cool but the LEDs stayed on all day. I often wanted to switch between No Man's Sky or Audacity on the macros that I had. And so I wanted to keep extending that and building that out. And a part of that also is I wanted to keep the same readability that I had with the code so that it could still be extended and modified by other people, but it wanted some additional features that made it a little bit easier to use. And so that's the genesis of that idea. And then I created a second version later when I started to get into DaVinci Resolve and using that. That has multiple pages within a single app. definitely need to learn a lot of the shortcuts and the hot keys to navigate that and do your workflow quickly. And so it was around the idea of a lot like with Blender you have one hand on the keys, one hand on the mouse, and you're able to navigate the UI together. And so that was the inspiration behind that and knowing that I'm never going to be able to exhaustively code all of the shortcuts and macros that someone's going to need. How do I make it easily usable in a studio environment, even with people who have minimal experience and exposure to programming with CircuitPython.

Paul

Yeah, the MacroPad is probably my favorite product that Adafruit sells. And I even wrote the awesome guide for it to share all the different stuff out there and I featured yours at the top because I love it so much. And one of the things that I love about it is I experienced burn-in on my OLED screen. You added a timeout so that doesn't happen. How are you able to do that?

John Ellis

Yeah, so it goes into a tiny little sleep and I think about that probably more than I should, but I think about not only not exhausting the LEDs and the displays that are out there, but how do you reduce the power consumption also so that it's not constantly polling and it's constantly trying to wait for input. So you'll see a little bit of lag as well when you try to get it to wake back up where you'll notice that the rotary encoder doesn't necessarily do it every time. It's 'cause I'm trying to be cognizant both power with extended sleep operations as well as having it be responsive also. I've been this way since I was a kid that I don't want to I want things to last forever perpetually be there I want to create time capsules out of everything and so that was part it wasn't it wasn't a huge technical issue in order to make that work on the MacroPad but with all of my projects I tried to add that sleep functionality still maintain state so that it isn't forgetting where it was at or where you were in the process and can easily resume where you left off as well. So when you code first with that sleep implementation it definitely makes things a lot easier because then you have to think about state management bringing it back and it's not complex to do as long as you start with that idea

Paul

in mind. Tell me about another MacroPad project the MacroPad 4-chord MIDI.

John Ellis

I saw in a hackaday where someone had come up with a MIDI controller that would recreate 90% of the pop songs out there with just four chords. And this is someone who had done their own custom PCB to make it look like a teeny little piano and with just I think it was seven buttons total because one was like to arpeggiate one was to change the tempo. You could recreate faithfully so many pop songs were out there and it tickled the logic programmer side of my brain of like, "Oh, this seems like procedurally you can generate a lot of music. That's kind of interesting." And if you look at the Adafruit Macro Pad, it's got three columns to it, which for a chord you have three notes to a chord and then you have four rows. So that's perfect for a four chord progression and that's idea came from was like watching that and then also watching the Axis of Awesome perform their four chord song where they go through a phalanx of like, I don't know, 30 pop songs with just four chords, which was the inspiration for the earlier project. And it's like, this could be something really fun. And so it was really out of my own bemusement to say, all right, it's this is Kismet. We've got three notes, we've got four chords, That's perfect to the layout of the macro pad. Now, how do we make this work? I still want to do some tricks to that because I'd also like to add some things like drum beats to it or drum progressions I've that kind of got me on the path of like learning how Bjork used like I think is the Qy 20 of Like using these older electronics, you know that were based heavily on analog circuitry or those of the TR 808 those old drum machines So like it got me on this old bent of again the old ways these old machines How they able to do so much with so little and I'd like to see if I can continue to weave that into the macro pad

Paul

As well, that's pretty awesome You have a project that integrates with OBS. What does tally circuit pie do?

John Ellis

Yeah, so tally circuit pie was actually born out of the kovat era when everyone was moving things to an online presence, right? And so Easter services were online, meetings were online, classrooms were online, and I started to help people out with that. I came in heavily masked with sanitary wipes and stuff like that. And then I found that a lot of people were gravitating towards OBS, which I had never heard of before, but got into and it was amazing. I couldn't believe this is something that was supported by the open source community, but of course sponsored by NVIDIA and some of the heavyweights as well. So I started to help people get that set up. And then of course you need kind of a multi-camera setup when you start to do larger services or organizations or even like town halls, 'cause you need like a bail camera and then your closeup camera as well. But one thing that was tough was I would have myself and then maybe a camera operator. We wouldn't know which camera was on where should people should look and of course this has been solved back in the 60s right with tally lights you see what camera is on by the light shining on top of the camera and There were some solutions out there for OBS But I wanted to create an open source one out of just readily available hardware because also supply chain issues Let's just use what we got. I found a few people on Tindie who had crafted these matrix LED boards But also I've used some Raspberry Pis as well. And so there is a Tali Circuit Pi There's a Tali Pi which runs on a Raspberry Pi and then there's the Tali OBS repos All of which help you to orchestrate these lights and it is as simple as when you take to a camera That light shines red when you take away from it It goes back to blue when you have it in preview mode it goes to yellow and it was something you could with a 3d printer and with some hardware that you probably already have lying around You can make a way to have tally lights that are easily orchestrated Inside of OBS and so it's one of those small things that has been very handy and it has lasted these five years Without need to replace to repair really and still works with OBS to this day

Paul

One of the products that Tally CircuitPy uses is by Seth Kerr, also known as Oak DevTech, which is no longer available. With something like that or with all the part shortages like you mentioned over the last few years, what role do you think CircuitPython can play to save or recycle hardware?

John Ellis

It's a huge contrast, I feel, between a lot of commercial outfitters who are making things, let's say smart remotes or other gear where it is great, it is inspirational, it seems to work, but then they end of life it or they in support or there's an acquisition and then it just kind of goes off into the wind and you lose the ability to work with that hardware and You mentioned oak devs tech they did a you know, he did a great job with the board itself. We had great conversations on Heat tolerances and how to position things so that they don't melt the surface mounted, you know pieces And even though those boards aren't manufactured anymore CircuitPython has been a stable and reliable platform that keeps archives that work across all of these older platforms so that it stays alive. This has been in reliable use for me for the past five years. I bought some spare boards just in case, but in truth this has had greater longevity than a lot of the commercial hardware that I've bought. And so I feel like CircuitPython with its portability of code, but also the robustness in which the platform was created and maintained, it allows you to reliably use and then reuse a lot of hardware that may not be officially supported anymore. And if you can find an analog, something that is close to that, you can pretty easily port things over, either with the out-of-print libraries that they have around, you know, NeoPixels are become a universal standard almost, and it's fairly easy to port across hardware, as long as you know how big your array is. So it's easy to not only keep in life the things that you've got, but easily adapt to close analogs so that things continue to run.

Paul

Last two questions I ask each guest. If someone wants to learn more about you and your work, where should they go?

John Ellis

Oh man, that's a great question. I'm terrible at self-promotion, So I do have deckerego.net, which has a lot of tiny squares, which highlights either photography or the open source projects or the things that I've done from there. I'm going to continue to try to put out videos that showcase how these things work and are put together, because I do believe that just making things accessible and usable is a big boon for CircuitPython. So I want to encourage people to tinker, to set small electrical fires, get the magic smoke out every so often, not be afraid, right? And so decker.net showcases a lot of that. You'll see me as DeckerEgo on GitHub as well. I try to keep an honest and open list of my repositories, as well as those things that are archived as well. And then a number of guests for things that I've found along the way.

Paul

And the last question, you're starting a new project or prototype. Which board do you reach for?

John Ellis

You know, I, again, I have very poor impulse control when it comes to Autofruit stuff. So the Trinket M0s, I love. They're like, and they show them photographed right next to a fingernail, right? It's great. So they fit inside of bottles. They fit inside of all these tiny like antique enclosures. You can make all sorts of cool led blinky things with them. And I don't need that many pins really for a lot of the projects that I've got. So I love the M zeros and the trinkets there, but my challenge and my resolution for 2026, and we will see if I hold to it is to actually use the stuff that I've in my drawer today. I have some really weird AT stamps that I've got and I don't know what they even do or even how to flash them at this point, but I am resolved to figure out how to do that once again. I've got a number of ESP32s that are in a drawer back when someone discovered them in a light bulb, right? And then they started to just buy the components themselves and everyone was building their own little chipsets out of them. I've got a few of those as well. I have an old cortex that I want to figure out how to finally use. Everything needs to find... It's like the island of misfit toys in my electronics drawer. So I want to find them all a happy home before I start to open up my wallet and buy new stuff.

Paul

That's a good resolution. I think we could all probably take advantage of that.

John Ellis

Yes, put it to happy use and then they'll become Christmas presents. Who knows, by the end of the year.

Paul

John, thanks so much for coming on the show.

John Ellis

Absolutely. Thanks so much for having me.

Paul

Thank you for listening to the CircuitPython Show. For show notes and transcripts, visit www.circuitpythonshow.com. Until next time, stay positive!
