---
date:
  created: 2024-01-29
title: "Episode 36 - Paul Cutler"
---

## Show Notes

[Show notes available here.](../../episodes/Season 4/ep036.md)

## Transcript

Tod

Welcome to The CircuitPython show. I'm your host, Tod Kurt, taking over hosting duties from the show's actual host, Paul Cutler, so that he can be a guest. Paul has been using computers since a young age, but he had learned a code until he was in his 40s. Paul has been contributing to open-source projects for almost 20 years, including the Gnome Project and the Discog's Python client. When he's not in front of his computer, you can find him listening to records from his vinyl record collection. Paul, welcome to the show.

Paul

It's great to be here. Thanks for guest hosting.

Tod

Hey, my pleasure. I love The CircuitPython show. So I guess we should get to start with your background. How did you first get started with computers and electronics?

Paul

You know, I've been pretty privileged that I've been around computers almost my entire life. I was probably 9 or 10 when we got our first computer, which was a Timex-Sinclair, TS-1000, which was really a modified Sinclair ZX-81 is what the rest of the world knew. knew it as. And then we got a second one. We got the TS-1500, which was a ZX spectrum just a year or two later. And I played around with those for a couple years.

You know, I remember getting those magazines that were made out of newspaper and entering assembly code trying to program them. You make one little mistake and you just want to tear your hair out. But after a couple of years, we got an Apple 2C, and I played around with that, and we got a 300 baud modem, which was screaming fast at the time. And I got really into the bulletin board system scene. I loved BBSs. And later we had a 1200 baud modem. And I would actually go to in real life meetups with the different folks I met in the BBS as a teenager. And from there, it's just a lifelong love of computers.

Tod

That's great. So when was the time you started getting into open source? Was it during the Apple two days or was it later? Oh, it was much later. I was,

Paul

I was a full-blown adult. And it's the fault of the game EverQuest of all things. So EverQuest came out in 99.

And you could cheat at EverQuest if you had a Linux computer. And I just happened to have a second computer. I had been playing around with BeOS, actually, a little bit.

And I had actually purchased Red Hat Linux from a retail store six months earlier, but it just sat in my closet until we started playing EQ with all my friends. And I realized I could take that second computer, put Linux on it, and cheat at the game, which was great. I know.

Tod

That's cool.

Paul

So I started using Linux and I had the second computer next to my gaming computer. And the more I used it, the more I liked it. And I really love the ethos that anyone could contribute to it.

And after probably four or five years of using Linux, this would probably be around 2004, 2005. I had done all the different distro hopping that people had done. I had tried Ubuntu and I had tried Fedora.

And by the mid to late 2000s, I found a very small Linux distribution called Foresight, which isn't around anymore. But one of the things that they really tried to do was be really close to upstream Gnome. So I started contributing to Foresight, which led me to contributing to Gnome.

And I got really into that. I joined the marketing team and the Sysadmin team, even though I didn't really have a lot of Sysadmin skills, but I had project management skills, which are always needs. needed in open source projects.

Tod

Yes, very much.

Paul

And then I started writing a ton of documentation. I served one term on the board of directors.

Tod

Oh, wow.

Paul

Yeah, and it's been, you know, 10 or 15 years since I probably left that scene. But I just, I loved it so much.

It was, I've made lifelong friends in that community.

Tod

Yeah, I was going to ask you if you were a gnome or a KDE guy, but I guess that answers that question.

Paul

Oh, yeah, I'm a gnome guy. There's no doubt about that. And one of the things that I'm probably most proud of. is I was one of the first mentors for the Ghanom Outreach Program for women that was started in 2010.

So I mentored a couple of women for documentation. And that program is still around. It's known today as the Outreachy Program.

Outreachy is still around. It offers paid internships for those subject to systemic bias and underrepresentation in tech. And it promotes diversity in open source.

So it's kind of cool that it's still around after all these years.

Tod

That's great. Yeah, the whole very underlooked aspect of open source, I think, is the management and documentation of the projects. It's like, everyone's like, oh, we just write the good code, put it up on a repo, and like, you're done.

It's like, no, no, no. That's just the start, you know. You're absolutely right. Especially for really complex projects, like a distro or a big, like GUI application.

There's like so many different levels of like, you know, the code, the OS integration, the artwork, you know. It's just a huge, huge task.

Paul

You're absolutely right. And I didn't know how to code at all when I was contributing. So I'm an example that you don't have to know how to code to be able to give back to an open source project.

Tod

Right. So, but at some point you got into Python after playing on with all this open source stuff. I did. Like, how did that happen?

Paul

I had an itch. I really wanted to learn programming. My wife is a developer.

And I had an itch to do it. I had time on my hands, and it was something that I've always wanted to do, but never had the discipline to do it. So I went out and I bought a couple of Python books and realized very quickly that I don't learn from books.

I learned from video courses and from hands-on projects is what I learned through the process. So I took a course on Coursera with Dr. Chuck, which taught me the basics of Python, what's a string, what's an int, you know, how to manipulate strings and all that kind of fun stuff. And then right when I was getting into it, Michael Kennedy, who hosts the Talk Python to me podcast, started Talk Python training.

And he had a Kickstarter of Learn Python by creating 10 apps. So it was very project-based and it was perfect. So I bought that Kickstarter.

And then I kept buying classes from Talk Python to me. The way he teaches really clicked for me. And it taught me not just Python, but I learned web frameworks like Pyramid.

And a couple years later, I learned the fast API. web framework as well. So I'm a big fan of the Talk Python to me, classes and strongly recommend them for people that are looking to get into Python.

Tod

Oh, that's cool. We should put that in the show notes, I think, then, yeah? Absolutely, I'll link to that. Right on, right on. And so, and then how long did it take you to find CircuitPython? Like, when sort of in the history of CircuitPython did you come in and start playing with that?

Paul

So I started Python in about 2017, and I got into CircuitPython because, I was into Python, I attended PyCon virtually in 2020 during the pandemic. So it was the first Pycon I ever, ever attended, which was pretty cool. And Microsoft had a booth, a virtual booth at PyCon.

And if you did an exercise on, they had these exercises built into GitHub. And if you learned and did the exercise, you got a $50 adafruit gift card. And then they had a bonus exercise.

And I walked away with $100 in the Adafruit gift cards. I did what probably everyone does when you're first starting out with Adafruit products. I bought a Circuit Playground Express.

And it probably sat in my drawer for a good six months before I got it back out. But it was during the pandemic. And there was all we had was time on our hands.

And then I started playing around with that and quickly fell in love with CircuitPython. It took two things that I love, you know, the coding aspect of it, but combined with that physical world aspect of it, here's a device that you can, can touch and feel. And I just thought that was the coolest thing ever.

Tod

Yeah, I've been, I've bounced off of Python, like normal desktop Python many times over the last like 20 years or whatever, always, you know, learned enough to do a project and then kind of, you know, I finished a project and it leaves my brain. And I've been really happy with CircuitPython as a way it'll just learn Python. Like, I don't know any of the web frameworks yet.

Like you're talking about like fast, fast, fast API. Fast API, yeah. I don't know any of the real Python frameworks, but I think I'm pretty cognizant of how Python thinks in a way that I could actually learn those now as I definitely could not before.

Paul

Yeah, Fast API was a fun one to learn because it was one of the fastest-growing Python applications out there. And it's async, which is great for a web server. And learning that taught me a lot about, you know, how to program asynchronously, as well as using the latest and greatest that. things that are out there.

Tod

And you've got some project now that you've created that marries both desktop Python and Fast API and CircuitPython, right?

Paul

I do. It's probably the project I'm most proud of. I have a website called SilverSaucer.com that you can visit. It was inspired by a Neil Gaiman poem of all things. And it combines my love of vinyl records, Python, and CircuitPython. So I learned how to use the Discogs API. And Discogs is a website that's been around for about 25 years, and they crowdsource all the different records and cassettes and CDs that are out there.

So, for example, Pearl Jam's debut album 10 has almost 300 different versions worldwide. Each country had their own CD, and people have entered all this data into there to catalog each specific release. So I have a fairly large vinyl record collection, as listeners know.

And I wanted to learn how to interact with an API, and I wanted to learn how to use Fast API. So I built a site, and it only does three things. There's three buttons on the front.

One is a random button. It'll randomly choose an album for me to go play. It's just an inspiration for me.

Tod

So anyone on the internet can say, hey, Paul, go just randomly go pick an album?

Paul

Well, it'll pick an album for them, but it doesn't tell me anything.

Tod

Oh, I see. Okay.

Paul

Now, if I'm logged in, there's some different functionality when it comes to the circuit Python stuff, but I'll get to that in a minute. Right, right, right. And then there's a play button. and that shows you a list of every record I have and you can select a record and it'll show you the album art and the song list underneath it once it loads. And then there's another feature that I built called On This Day that I scraped both discogs and music brains with my collection to figure out which day in a certain album was ever released.

Tod

Oh, cool.

Paul

Which is another way that I get inspired to go listen to an album. It's like, oh, you know, for example, and this is kind of a funny one, Yesterday or today, Debbie Gibson's electric youth came out in 1989, which is a record that I happen to own. I love 80s pop music, so, you know, don't laugh at me too hard.

But it's a great way to just go pick a record off the shelf and say, hey, I'm going to listen to this now. So once I started getting into CircuitPython, I realized that I could take it a step further. Now, my record player is in another room.

It's on the opposite side of the wall of my home office down here in my basement. So it's only about 10 feet away, but the, the record player is in a step further. record sleeve is in there so I can't see the album art. So I have a Pi portal and I decided using the Discog's API, it shows me that the album art, the download the JPEG that's displayed on the website.

While using the pillow library, I took that album art and I reformatted it to a Pi portal size, which I think is about 300 pixels or 320 pixels. And when that webpage loads, if I'm the user who's logged in, it will then send a message using MQTT over Adafruit I.O. And the Pi Portal is listening for that MQTT message.

And once that page loads and sends the message, the Pi Portal goes out to my web server, downloads the album art, and displays it. So that's how I kind of married desktop Python with CircuitPython.

Tod

So it's a little thing that sits on your desk and it just displays the album art. And, oh, that's great. As soon as you played it, play an album. That's cool.

Paul

Yep. As soon as I choose that album to play on the website. And then late last year, I bought a 64 by 64 RGB Matrix and did the same thing again.

But now it looks like pixel art, because this is a 64 by 64 image. It's tiny by the time it shrinks it down. Yeah, totally.

But it was kind of cool. And now I'm actually considered doing it for a third time and picking up one of those S3 qualia boards with one of the RGV dot clock displays that are a little bigger than a Piportle. But I haven't spent the money on that yet.

Tod

Yeah, and the color rendition of those displays, like they're both like higher density or higher resolution. They're like up to 480 by 480, I think. But also they're like, I think they're 6 bit per channel color instead of the sort of mostly 5 bit per channel that the other displays use of my controllers are. So it's like, man, we get to drive these like real displays in CircuitPython. It's kind of incredible.

Paul

Exactly. And probably the next time I order something from Adafruit, I'll pick one of those up and do the whole project all over again.

Tod

Totally. Yeah, and there's no OS, so it just starts up.

Paul

Exactly.

Tod

So, where we talk about, like, Qualia is one of the new things that's going on in CircuitPython. What are some other things you're excited about that's coming up in CircuitPython? Because it's kind of ever evolving. There's new things happening all the time. What are some of the things that you've seen?

Paul

You know, the first two things that come to mind are the first is the Memento Camera. I have been waiting for that thing to come back in stock. And I just think it's so cool.

Not only is it an open source hardware camera, it's programmable. And every time I think of a different way to program it, it seems like there's already a learn guide to do it, whether it's using a remote or stop motion or creating gifts. And I just think that thing is cool, and I can't wait to get my hands on one.

The second one that comes to mind is USB host. You know, that combined with support with the new bigger RBB. dot clock displays makes me wonder, and Scott Shawcroft actually mentioned this in his circuit Python 24 blog post, how close are we to a little mini CircuitPython powered computer?

When you have a computer or a keyboard with a display, it can't be that far away. Now, I know that USB host only works on the IMX and the RP2040 chipsets right now, and those dot clock displays work on the S3. So there's going to have to be some work done probably to get to that point.

But that's one of the things that I think I'm really excited for in the future.

Tod

Yeah, we're really close to something that is very much like the old Sinclair ZX81's or the Timex one you had, where it's just this little box and you just turn it on and you've got a full little language-based computer you can type programs into without any, like, worrying about, is it on the net? Is it running an OS? All this kind of stuff.

It's just all it does is the language. It does basic in the case of the ZX81, or it does CircuitPython in the case of this hopeful new thing we could make in like a year or so. Exactly.

Yeah, the camera, the Memento camera is pretty great because it takes a bunch of stuff that's been here and there. Like there's been a camera you can hook up to an ESP 32 for a while and there's been like, you know, SD card support for a while and all this other sort of stuff, you know, screens, of course. And now it's a whole thing.

It's like it's got the camera, the screen, a little microphone, a little speaker, SD card, Wi-Fi. And, oh, yeah, and you can access all of this via CircuitPython and make it do things that a camera can do.

Paul

Right, and it just works. Yeah.

Tod

Yeah, so it'll be interesting. It's one of the things that I think people need to realize about CircuitPython that has taken me a while is, It's sort of like Legos where you can, if you've got the pieces available to you, you can sneak them together to form new things. But if you don't have the right Lego piece, you can't do stuff.

And so like for a while, like for the longest time, there wasn't camera. Like the camera Lego piece in CircuitPython didn't exist, but now it does. And so I think it's pretty cool that we're getting more and more of these cool little Lego pieces that we can do stuff with.

Paul

Oh, I agree.

Tod

It is so cool to watch the development happen in real time. So we've got all these new things that are definitely coming up. What are some of the things you want to see CircuitPython do in the future? You know, one of the things I'd like to see is more options for Bluetooth.

Paul

So we've got the NRF boards that are out there. And with CircuitPython 9, they've updated the expressive IDF, the IOT development framework. And I know or I believe that there are still some changes upstream in the Nimble Library that need to happen before CircuitPython can take advantage of.

of Bluetooth on an S3 chip. But I think it'll be, you know, considering all the different places we're seeing these S3 chips now, right? The qualia boards.

Yeah. The Memental camera. Everything we just talked about, adding Bluetooth just seems to be the next step.

And that's one thing I would personally like to see.

Tod

Yeah, yeah, definitely. These ESP 32 S3 chips are so powerful with their, like they've got dual core, I think, and they've got Wi-Fi and they've got Bluetooth. But, you know, yeah, getting the Bluetooth stuff has been not quite working.

on CircuitPython. And I think there's even been problems with it and when you're writing programs in C and stuff. And so I can't wait for that because it's pretty cool to have a little Bluetooth gizmo that talks to your phone or whatever.

Because you can pull off, you can get cool notifications from your phone. You can like control your phone in various ways, you know, have it be a MIDI device or an audio device or something. Right.

So yeah. This is at the end of the show yet, but I wanted to also thank you for the last, what, two years of doing the CircuitPython show. I think it was a very, critical tool to help get people to learn about CircuitPython and get people who are doing some of the CircuitPython stuff kind of get them out there in the world. So thank you very much.

Paul

Oh, you're welcome. It's been my pleasure. You know, the developers and hackers and makers that I've gotten to talk to. It's been so cool getting to know all these people and seeing all the cool projects that are done. You know, it's sad in a way that the show's coming to an end, but I think it's time. But yeah, the last two years have just been wonderful and being able to meet everyone.

Tod

Especially a good thing to let us do instead of worrying about the pandemic for the last couple of years.

Paul

Exactly. And that's one of the reasons why I started it is I was looking for a hobby in addition to CircuitPython and Python and just coding. And it was a great learning experience on how to cut up audio and audio production and all that kind of fun stuff. I've learned a ton.

Tod

Totally.

Paul

Yeah.

Tod

These are your two standard questions you have at the end of the podcast. If anyone wants to learn more about you and your work, where should they go?

Paul

They can visit my homepage at Paul Cutler.org. I have a blog there that I infrequently update like most people these days. But I also have a projects page that lists all the different projects I've worked on over the last couple of years with screenshots and links to the GitHub repos and all that kind of fun stuff. Oh, that's smart. That would be the place to go.

Tod

Yeah, I should do that. That's a good idea. And lastly, so you're going to start a new CircuitPython project. What board are you reaching for to first start prototyping or building with?

Paul

I'm going to go with the one that we've been talking about so much, as the same one that Jeff Epler picked in the last episode, which is a Qtpy S3 with two megs of PSRAM. I don't typically need a lot of GPIO, so the QT pys are perfect for me with that small little footprint. And like we were just talking about, the S3 is such a powerful chip.

And I've really, really enjoyed working with Wi-Fi. A number of my projects use Wi-Fi, whether it's downloading images, or controlling my home theater receiver remotely. I love built-in Wi-Fi on those chips.

Tod

Yeah. Yeah, I'm a big fan of the ESP 32 S3 chips. Also, not even when using them for Wi-Fi.

Like, I've used a ton of them for non-internet projects because their little processor in them is so fast. They can do a lot of math-y-type operations if you're doing, like, synthesizers or stuff. So, yeah, big fan of that chip as well.

Paul, thanks so much for being on the show. and hosting the other shows and creating the Circut Python show transcripts are available in most podcast players and show notes are available at www.com. Thanks for listening and stay positive.
