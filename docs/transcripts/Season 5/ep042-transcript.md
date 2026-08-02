---
date:
  created: 2025-03-24
title: "Episode 42 - Project Collaboration with Liz Clark and Noe Ruiz"
---

## Show Notes

[Show notes available here.](../../episodes/Season 5/ep042.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Liz Clark and Noe Ruiz from Adafruit Industries to discuss how they collaborate on projects together. Noe and Liz, welcome to the show.

Liz Clark

Hi. Thanks for having us.

Paul

So glad you're here. I've got so many questions for you about all the projects that you've collaborated on. Let's start at the beginning. How do your projects start? Where do you get inspiration from and how do they influence your projects?

Liz Clark

It kind of depends on whose idea the project is, because we kind of have different specialties. Noe, of course, has the 3D printing and design background, whereas I'm more of the Circa Python coding background. So if it's a project idea that I have, then I'm kind of collaborating with him on how I want the enclosure to be and things like that, versus if it's his idea, then we're kind of more discussing, like, how we want the code to work.

We have a lot of these conversations on walks. For those that don't know, we are married. So we live together, of course, and we take at least one walk a day.

And when we'reout walking, we'll kind of discuss what we're working on. And if we're starting a new project, we'll kind of walk through what we're looking to accomplish.

Noe Ruiz

So for me, it's a little different. My inspiration comes from either from above, which is Limor. She'll give us an idea.

She's like, hey, I saw this or, hey, would this be cool? And then we go from there. If it's something that I come up with, it's something I see on Instagram.

It's someone else's project or something that I see at Target or IKEA. And then from there, it's like, okay, we got these new parts. Maybe we can fit this thing into that.

It's always coming back to like what is a new thing that Lamar is working on. That would be cool. So, for example, we got this new stepper motor, and I'm just going crazy with let's make everything motorized.

Turn tables, camera sliders, anything that spins. At the end of the year, we did LEDs that are spinning. It's a P-O-B motorized thing.

So I'm just all over the place with this stepper driver. So that's kind of where my inspiration comes from. A little more.

Does she have an idea or she have a new product and then I go from there? Or is it in Instagram? I see this cool prop that someone else is making.

and I'm thinking, oh, could I do something like that? And effect, a shape. A lot of the times, like, oh, I just like this shape.

I want to do the shape. And then I go crazy with it. I think you're kind of similar.

You see something that's a musical thing and, hey, I want to make a motorized robot thing.

Liz Clark

Yeah, often, you know, like I would be looking on Instagram or Pinterest. I might see something that looks unique and think, hmm, you know, could I recreate this with Sarka Python or stuff we have in the shop? And then same thing, too, when there's new things in the shop, I tend to write most of the new product guides. So I kind of get a crash course in every new product. So I'll run the examples. And then as I'm running the examples for the guide and looking at all the pins, I'll kind of get my gears turning of like, how could we use this and something? Or, oh, you know, we've always talked about wanting to build this thing. This part really makes it possible. As no, I just said, there's a new stepper driver. So that's been on our minds. And, you know, we've wanted to do a lot of step remoder projects and the new drivers are kind of getting our gears turning and, you know, motor spinning.

Noe Ruiz

We watch a lot of TV. And when it's a sci-fi show, it's like, okay, you wanted to do this prop from Severance. Yes. It's coming back and you're like, okay, the timing is good here.

Liz Clark

Yeah. So in Severance, there's these like weird terminals that the people work at and there are these like kind of floating letters on the screen and they're using a little ball mouse to scroll around. And so that's something I've wanted to try to recreate and circuit Python for a while. And now we kind of can, hopefully, with the RP 2350, because it has the HSTX peripheral for DVI output. And then that frees up the PIO for USB host. And in like two weeks from where we're recording right now, early January, the new severance season's coming out. So like, that's all the pieces are kind of coming together. So hopefully I'll be able to work on that. Use that as a project inspiration. Oh, that's great. So we've had

Paul

You've gone for a walk and you've kind of talked it through. You come back to the home office. What's next?

Liz Clark

That's when we'll kind of iterate. So often if we've discussed things, you know, we'll work on a fritzing diagram. For code, I'll do kind of a step-by-step thing where if it's complicated code, I like to break it down into different parts.

So if there's multiple things going on, then I'll kind of test everything and then put them together. So like if we have sound and lights, you know, I'll do the lights. first sound and then bring them together, make sure it's going to work as we expect, especially with props and you expect it to work a certain way for the end user.

You want to make sure there aren't going to be any like blocking delays or anything that make it kind of weird. And then we just kind of chat back and forth.

Noe Ruiz

Yeah. I'll just open a bunch of tabs on Google Chrome and look for reference images if it's a physical thing. I'll go to Pinterest and see what's out there.

Hacksraio, hackadayio. I'll just look at where has anyone made this before? for and kind of see what people have done, if anything, if it's never been done, it gets a little hard.

But there's always something out there that I can like kind of reference. Even like you're talking about the severance terminal, I could look at real things that were computer enclosures that are, you know, in the 70s because it's kind of the vibe. Yes.

And then I'll just kind of collect things. I don't have a particular app where I'll collect images, just kind of save images to my folder.

Liz Clark

Yeah, I end up just with, you know, a million tabs. A million tabs, yeah. And also like, I often will, then also have a million tabs of different learn projects, too, either ones I've written or other folks have written to be getting different code snippets and stuff.

So I try to reuse as much code as I can if I have no start from scratch. And that is good in that I know this code worked previously. And then I'm not having to do too much new testing out and stuff.

Paul

Sure. So working together, how does that improve the finished project?

Liz Clark

I like that we can kind of immediately get feedback from one another. it's more of a conversation. Whereas, like, if we were not in the same space, it would be a little tricky because you have to wait for that response and everything.

Noe Ruiz

Yeah, I don't have much of a background in code and development, so I wouldn't really not be able to do any of the things that you can do. So I think the marriage of our different skill sets really make the project possible. It's like two very experienced people in these two realms come together, and then you get this cool kind of thing that does a cool, thing and looks really cool and can be built in a relatively easy way.

Liz Clark

Yeah, and you're able to do such cool design tricks and iterate so quickly in Fusion 360 and you can easily tweak things with the way that you set up your projects. I will do a little bit of 3D modeling, but my timeline I know stresses him out when he looks at it. So he does it like the right way so that if we get to the assembly stage, it's like, oh, you know what, we need like two more millimeters here. He can easily just add that to the design and then it's perfect instead of having to redo it all over again.

Noe Ruiz

Likewise, I'll ask, hey, can we make it so that when this thing is shaken, can we have do an extra animation and you can go in there and figure out how to make it happen?

Liz Clark

Yeah, because often, I don't know, this is your experience too. Sometimes you get the working prototype of the project and just with how we work, like we're kind of documenting as we go, just because we do try to publish, you know, at least once a week with AtaFruit. And sometimes it's not until you're documenting and really like using it that you think, oh, you know what? I would love if it did this one extra thing or had this one extra feature. So it's nice to be able to quickly iterate like that.

Paul

That's great. Let's talk about some of your favorite projects. Noi, what's one of your favorites? We'll start with you.

Noe Ruiz

Yeah, one of my favorite projects is probably the ATAB. Arp. 2040 toy robot.

Just because it ticks all the boxes of something, it's a fun, interactive little robot. It has a glowing, like, mouth. It has sound effects.

It has built an exoromers, so you can kind of turn it upside down. It kind of does this sleep mode. That's kind of my favorite.

And it's just got, like, the mascot, right? Adabot is Adafruit's mascot. So it's got all the little pieces.

It's so cute as well. Having something cute is like a big kind of factor for me when I'm making a project. How do I make it cute?

You can't get cuter than ATABot.

Liz Clark

Yeah.

Noe Ruiz

That's one of my favorites.

Liz Clark

And from the code perspective, I believe when we made that the RP 2040 prop maker feather was new. So we, for the code, like, it was a really good project to be able to show off like everything that the feather could do. Because it had the accelerometer, has the onboard speaker, it has, you know, everything.

And so with that code, it was a nice way to show off. Like, you can control all these different components with just one board. It makes the wiring really neat.

Noe Ruiz

Yeah, it's huge.

Liz Clark

Yeah.

Paul

Yeah, I interviewed Aaron Penley a while back, and the prop maker feather is his favorite board. I think for a lot of people, it just does so many different things so well.

Liz Clark

Yeah, yeah. It's great to, especially, I find for audio projects, too, because the prop maker name might make people think, like, oh, I'll use this for props, but actually, I think it's a great music board, too, just because it has the I2S amp on board and then terminal block to connect up a speaker. Really cool board.

Paul

Is there a favorite project that comes to mind for you, Liz?

Liz Clark

Oh, there's so many. One collab that we had a lot of fun with was the Pico Midi Fighter. And at that point, the Raspberry Pi Pico was kind of new.

It was cool to have all these GPIO available on it. So we were able to do this 4x4 grid of arcade buttons. We had the screen.

So you were able to assign different MIDI note numbers to each button and you could change them on the fly. And that was such a fun collaboration. I know I did this great case with a handle on it, so it looks kind of like a lunchbox, which is kind of like teenage engineering kind of style, one design house that we both get a lot of inspiration from.

And folks in the community have also remixed it and changed up the code and stuff. So it's, I really like that project because I felt like it kind of laid a good foundation for RP2040 MIDI projects, to reference for and also kind of show like what you could do with CircuitPython and

Paul

you know a lot of gpio pins i like that project i mean yeah it's got 16 buttons but i like the way that you showcase the pi pico in that see-through case and then you mentioned the handle which also doubles as a kickstand for it which is just an ingenious design yeah speaking of midi projects

Liz Clark

tell me about the mx guitar yeah uh so there's two mx guitars the first one was a MIDI controller, and we released that kind of the week that COVID-19 started the lockdown. Everybody shut down. The week of Friday, 13th, March.

But that was our first guitar project, and we wanted to do a MIDI guitar, and we thought of the guitar hero controllers. Because the guitar hero controllers had like the wami bar, and it has that really cool strum mechanism. At the time, we did not live together.

So I took apart a guitar hero controller. I took like a bunch of photos and we're sending them to him so you can have it as like a design reference. And it was really fun, but a real bear to wire.

Noe Ruiz

Yeah, it was.

Liz Clark

Yeah, because each button was individually wired up.

Noe Ruiz

We ended up using the Grand Central because it's just all the GTIO. For the shape, I got like a crash chorus and like all the different guitar bodies. I actually am not a guitarist.

I'm more of a drummer, but you are a guitarist. So you know all the things about guitar anatomy. And I'm like, what's the coolest guitar?

I think we narrowed it down to the flying V.

Liz Clark

Yes. Right? So we used the flying V for that one.

I remember that night that we were chatting. Like we were just kind of going through all these different guitar shapes together and everything. And we used a real guitar whammy bar in the final design.

That's right.

Noe Ruiz

Yeah.

Liz Clark

Yeah.

Noe Ruiz

It just kind of screws into this 3D printed little adaptive thing that turns into a what was it? Is it a pediometer?

Liz Clark

Yes, it was a pentheometer. Yeah. Because if you open up the guitar hero.

controllers, that's actually what it is. It's like this spring mechanism that's turning a potentiometer. That was our first MX guitar and we always feel a little bad because, you know, it was the week of the pandemic, like truly. So I know for myself too, I had other things to worry about like once the guide went up, it got to the point where I was like, I got too much going on.

So we always wanted to revisit it because we really like the concept. So when synthio was added to the core, we thought, you know, what a great opportunity to make another guitar, but instead of it being a MIDI controller, make it like an actual synthesizer, and especially we have two young nephews, so the idea that like, you know, someone could use it as a music making tool, but then, you know, kids could also use it as a toy. And with what we learned with the first MX guitar, we wanted to try to simplify the wiring. So we were able to use two one by four neokea seesaw, breakouts. So that's I squared C breakouts so really simplifies the wiring.

And you still get eight notes and then that was also the prop maker feather.

Noe Ruiz

Yeah, it was. Yeah, it made a lot of the wiring easy with Stemakutee. You could just kind of connect those to one by four keys together.

You still got a wire, you know, some pent geometers, but yeah, I think it was a fun one because everything's self-contained. You got a built-in speaker in the head which was completely different. Yeah. We have built in batteries that are double A that are easy to change out. So it's like kid friendly. You don't have to worry about puncturing a battery because you're these nice double A batteries. And the body's different. I kind of forgot the name of the, but do you know?

Liz Clark

It's like a Gibson SG, so it has those two horns kind of

Noe Ruiz

at the top. Yeah.

Liz Clark

You know, that's a great example of, you know, we did one project and then we were able to kind of revisit it like, okay, what did we like? What didn't we like? And kind of remix it. I like when we get the opportunity to do that.

Noe Ruiz

And then I got to reuse the same mechanism. We didn't need a Bami Bar because we have the built-in acceleromers. We could just move the guitar.

Yes. So that was different. But, yeah, we had a lot of fun playing around with all the different modulation things that you can do with Sintai-O. And are they rotoring codes?

Liz Clark

Those are roter encodes. Yeah, they're, again, the STEMA QT rotary encoders. There's three of them.

Noe Ruiz

Yeah.

Liz Clark

We're looking at it on our wall right now.

Noe Ruiz

Yeah. You're like, what is this thing? Oh, yeah, that's great. Yeah.

Paul

Well, I'll make sure I'd link to all of these learn guides in the show notes. as well if people want to dig in and see the guides.

Liz Clark

Thank you.

Paul

Yeah, I love to see more people build it.

Liz Clark

Yeah.

Paul

The next project is another remix or something you visited from the past, but it's a little more utilitarian. What is the CircuitPython slider? Oh, yeah.

Noe Ruiz

Yeah, the CircuitPython slider is a remake of a motorized slider that we did with Arduino and a BLE module. So we both love doing videos. and cinematography.

And getting these nice sliding shots is something we always wanted to do. They're pretty pricey motorized sliders. I thought it would be cool to redo that Arduino project with a feather, a motor feather wing, and this time in CircuitPython with an onboard screen so you can control it all without having to like flots around with your phone and remembering like what does this number do or what does the key pads do.

So that was the idea behind that one. And we are actually hoping to make a third version this time with the silent Stepper motor driver. But yeah, that was a lot of fun to do.

Liz Clark

And I would love to redo that code. That was probably the biggest Circa Python project I had done at that point, and that's back in November 2019. And I was not working full-time with AtaFruit yet.

I was still just kind of in the community. And that was a huge level up for me as far as the coding went and also working with stepper motors. and there's a whole menu system and everything.

And I've looked at the code every once in a while since then. And I know there's definitely a way it could be condensed and be a little bit more streamlined. So I would love to be able to go back and kind of have a full circle moment with that.

Paul

Hopefully this year.

Liz Clark

Hopefully this year, yeah.

Paul

Well, that's true of any project. You get done, you look back at it and you go, oh, I could do this differently or I could simplify the code here.

Noe Ruiz

And parts are just better. Like, it's so loud. It's like, eh, eh, eh, because it's like an eight-bit chip or something. something, you know, it's very loud, you know, stuff or driver.

Liz Clark

Yeah, yeah. So it would be good to have a silent one.

Paul

Yeah. Let's talk about some of your more recent projects. Let's start with the prop maker Jackalanturn from this past Halloween.

Noe Ruiz

Yeah. That one was actually inspired by, I guess, you, Liz. You got an email because you're subscribed to the IKEA newsletter, and you saw that there's this new pumpkin that they started. selling. Yeah, in August

Liz Clark

they, IKEA had, which we also love and get a lot of inspiration from, and also the breakfast at IKEA is excellent. They're on Target. I know. But IKEA this year had this pumpkin light and I said to know, I was like, oh, you know, that could be a cool Halloween prop maybe, and then you kind of ran with it and you totally made this unique thing. At first I was like,

Noe Ruiz

I don't know what I'm going to do with this.

Liz Clark

Yeah, at first you weren't into it.

Noe Ruiz

Yeah. At all. I forget how, but at some point I thought it'd be cool to make the head turn.

And in order to do that, I need a base. So then I went down this route of like, what's a cool base that the pumpkin could sit on? And then I kind of ran with that and figuring out, how do I take out the guts of it?

It's just like a little lamp and then like fit it into a new base, add a gear, out of motor. And then were you the ones like, let's make it interactive? We can use a time of flight sensor so that as you approach it, It has different sound effects.

Liz Clark

I think that was L'Amour. That was L'Amore, okay. So, again, like, what's great is, like, we might have kind of a base idea, and then when we pitch it to Lomor Lady Ada in our meetings or, you know, internal communications, she'll often have ways to use other components or just really flush out the project to make it, like, a better, basically.

Speaker 4

Yeah. Yeah.

Liz Clark

Well, it was great, too, when we filmed the project video, a friend of mine recently bought a house, So they had like a nice stoop we were able to use because we're still in an apartment. And they have a little kid. So a little kid was able to see the pumpkin and everything.

And then we manned their door for trick-or-treat and noi was able to set it up on the stoop. So all the trick-or-treaters were seeing it and everything. So it was a really cool project to be able to then use too on Halloween.

Paul

Oh, that's great. Long-time listeners know that I'm a big fan of physical media, whether it's, you know, my vinyl music collection or collecting movies. I love these next two projects. The NFC Raspberry Pi Media Player uses Blinka for CircuitPython. How did that project come about?

Liz Clark

So I believe that Lamar saw on a blog someone else had done kind of a similar concept, which is basically you have an NFC card and you scan it on the NFC reader and then it triggers a movie or TV show to play. and we're like, you know, we could do this with just a Raspberry Pi and Blinka. And so we have the NFC breakout in the shop.

So we use that over Spy. And then the Raspberry Pi 5 has the SSD hat, which lets you have like a lot of storage on there. So it was a full Raspberry Pi project.

The hat was like kind of new. Like I think for AidaFruit, we hadn't really done a project that used it yet.

Paul

Is it the M.D.2 hat. So basically the way it works is you've got the NFC card, you scan it.

Liz Clark

Yes.

Paul

And then the movie starts playing on the monitor connected to the Raspberry Pi.

Liz Clark

Yes, yes. That sounds very simple in theory. But then in practice, it was a little tricky on the software end of things.

Not the blink apart. The blink apart just worked because it was an NFC and, you know, you can play the video file in VLC. But it got more into almost a Linux project, really, because you had to, well, I had.

I had to in the Python script figure out, okay, how do I have kind of a graphical interface? How do I get the movie to read properly from the disc? And how do I get to mount it boot and all that?

So that was, it was tricky. But I'm glad that now it's documented for folks if they want to do that with the M.D2 hat or anything like that.

Noe Ruiz

There's like a dedicated page on setting up your Python environment.

Liz Clark

Yes, that too.

Noe Ruiz

is like, okay, here's a whole new way to do Python.

Liz Clark

Yes, the Pi 5, the new version of Raspberry PiOS, you have to have the virtual

Paul

Python environment and yada, yada, yada.

Liz Clark

So that was very tricky. So that was definitely some frustration moments because also when we were documenting the project and we'd go to test it, sometimes we'd find that, oh, actually, this part still isn't quite configured right. But that's good because then, you know, in the guide we have it totally right. and hopefully folks won't have to go to the forums to be like, hey, this isn't actually working.

Noe Ruiz

From the enclosure standpoint, the pie 5 gets hot. And it turns out it can melt PLA. So I had to go back and redesign the case to allow some room for the active cooling fans. Like any pie project that we do now, you've got to have the active cooling fan. It's just too hot.

Liz Clark

Yeah, which we hadn't run into before when we've done other Raspberry Pi projects.

Noe Ruiz

I can still smell the burning PLA turning back, and you're like, is it the case? Oh, my God, it is. And it was all warped and stuff.

Yeah. So it's good to test your project long term, not just for five minutes. That does, yeah. Play a whole movie. And, you know, find out this thing working, not just from the code, but is my enclosure melting? But much like you, Paul, like I love physical media and I have a

Liz Clark

really big movie collection. So, and I've always been trying to find, like, ways to, you know, digitize it or, you know, make it so that it's like streaming, but still using it. So I, I, I really, really liked the opportunity to kind of test that out. And then you also had a really fun design thing with the cards. Yeah.

Noe Ruiz

Yeah, we could have always just put like a sticker on the NFC card, but I thought it would be cool to turn the card into a little mini VHS themed enclosure. So I created this little case that the card would fit into. And that was fun to kind of throw back to VHS, because that's kind of what we grew up on in the 90s with VHS. And then you got to use all those kind of throwaway NFC cards that you collected. And you're like, one day I'm going to use these cards.

Liz Clark

What kind of cards are they? They were MBTA, which is Massachusetts Bay Transit Authority cards for taking the train in Massachusetts. I used to have a new train pass every month.

And I never got rid of them because it felt kind of wasteful. I knew there were electronics in it. And it turns out they use the same protocol that the NFC cards that we sell in the Adafurts shop uses.

Noe Ruiz

A stack of these cards.

Liz Clark

Yeah, so we have a bunch if we want to extend.

Paul

The last project I want to ask about is this is how I started in Circa Python was doing audio reactive projects. You created the audio reactive video synth with the new RP2350.

Liz Clark

Yeah, so that was my third video synth that I've done for Aida Fruit. And for me, it felt like this really kind of fun, full circle thing. I'd always wanted to do an audio reactive one.

But for whatever reason, it was either like to resource intensive or whatever programming language I was using didn't quite work out. And this was the first time I was able to do it in CircuitPython. And the feather RP2350 with the HSTX made that possible.

So that was really awesome. I was really excited that everything I wanted to do in CircuitPython was able to be accomplished and it was working exactly how I wanted to. And then I kind of turned to you for the enclosure.

You had a good start.

Noe Ruiz

I like when you make an enclosure that has like angled faces, and that's really cool. Yeah. But when I started to remake it, I found it difficult to mount the mic.

Just because the mounting holes are in this weird spot, and they're a little close together. So it would be cool to put the mic in its own enclosure and then fit that on top of the main base of the enclosure. And that way you can have kind of fun.

And I went with like this kind of, like mics from the 50s. Like they have like the kind of the steel kind of enclosure. So it was fun to kind of break that out and make it its own thing because that's kind of calling attention to this is where the audio goes into, right? So it was kind of cool.

And then we could use different colors. Yeah. Come up with these fun kind of Fisher Price colors.

Liz Clark

Yeah, I always want a vibrant. A bunch of colors, yeah. And the enclosure is also kind of inspired by Love Holton, who's another designer we like a lot. And for those don't know, he takes these, you know, off the shelf synths or guitar pedals and he makes these completely new. new housings that look a lot like, you know, postmodern kind of stuff.

Paul

Yeah, kind of 70s vibe.

Liz Clark

Yeah, yeah.

Paul

So in the enclosure, there's built three or four pots and you can change modes. What are the different modes in the video synth?

Liz Clark

Yeah, so I used a rotary encoder for mode changing. And so the first one is kind of audio reactive bars, like your classic audio EQ. And that was kind of cribbed by Phil B had done some code using one of the major.

matrix breakouts. And that was kind of my test to see like, okay, will the audio reactive stuff work with the DVI output from the RP 2350? Or am I going to like run into memory errors?

Because you're asking the board to do a lot when you're, you know, displaying out DBI and you're using audio reactive, which is FFT, but it did it. And so then I went from there and I made a kind of bouncing circles one that had the circles change shape depending on the audio spectrum those coming in, and they're bouncing around the screen. And then the third animation is a party parrot.

So you have the party parrot in the back, and he's kind of bopping around to the lower frequency. So if you had a bass drum beat going, then he would move his head for every beat. So you kind of get this syncopated vibe from him.

And then there are these two circles on either side of him that are going to the overall amplitude. So depending on how loud the music is, that affects their size. And then I had three potentiometers that were changing color for different shapes or how reactive it was. Because the thing with the audio reactive stuff is with the music, like your music will be different levels, obviously. So I wanted to be able to control like how sensitive things were. So you wouldn't have to have the music blasting. And yeah, it was just really fun to be able to have it all come together in CircuitPython.

I'd done one in Arduino before, but waiting to compile everything for testing was always really tricky. So to be able to test those three animations quickly, the Circa Python also made it really enjoyable.

Paul

Do you have any advice for people when collaborating?

Liz Clark

I think just based on not great collabs I've had and then versus really good collabs. Because I've been in bands, too, where you're working together, people, is always being. open to other folks' point of view and always be willing to kind of step back and let other folks work on different aspects that maybe aren't your strongest suit. So sometimes, like, for example, with the video synth, I was thinking it was going to be a project that I just worked on by myself. So I had sketched up the enclosure, but I knew almost immediately that the enclosure wasn't that great. I knew Noe could do a better job. So I was like, hey, let's actually collab on this and have him come in. And he makes this beautiful enclosure that is just fantastic and greater than anything I could have done on my own. And also he did it faster than I could have as well. Resisting the urge to stay in your silo and just power through and get stuff done, kind of open things up and yeah, just be open to other folks. Liz, that's a great answer.

Paul

Noe and Liz, thanks so much for coming on the show.

Liz Clark

Thanks so much for having us.

Paul

Thank you. Thank you to Liz and Noe for sharing how they work together and collaborate on their projects and discussing some of their awesome collabs. For show notes and transcripts, visit www.circuitpythonshow.com. Until next time, stay positive.
