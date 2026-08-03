---
date:
  created: 2024-01-01
title: "Episode 34 - Debra Ansell"
---

## Show Notes

[Show notes available here.](../../episodes/Season 4/ep034.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. This episode, I welcome Debra Ansell.

Debra studied physics and applied math before becoming a software engineer in the mid-90s. She quit to stay home with her three boys after the internet bust, then rediscovered her love of technology as a first Lego League robotics coach. She has been making open-source projects ever since. Debra, welcome to the show.

Debra Ansell

Thank you, Paul. It's really nice to be here. Thanks for having me on.

Paul

How did you first get started with computers and electronics?

Debra Ansell

Well, I got started with computers. Those are actually two slightly different topics. I got started with computers in graduate school.

I had taken a year of coding in college and felt a little bit intimidated, frankly, because I think most of the people who took the class, I was a novice and a lot of people had been hacking either, you know, TS80s or whatever in high school before I got there. But I knew enough to code. And then in graduate school, I did a fair amount of coding with Fortran and numeric recipes to analyze my data. So I was in graduate school for physics and decided against an academic career and came back to Los Angeles and ended up working for an internet startup as a software engineer. And I've been fairly comfortable with coding for a while, though I did retire from that job about 24 years ago and have only coded as a hobby since. I had technically learned electronics in graduate school. You know, I'd learned a little bit about circuits and things like that, but only in the lab and only in very small amounts. So really didn't have any practical experience with that. That part all started when my middle son turned eight and was an enormous Lego fan and decided he wanted to join a Lego robotics team. But we couldn't find a local team.

And given that I was a stay-at-home mom with coding experience, I figured I could coach it. And yet, and I have told this story before, but it doesn't get old. It was a blast of coach, but I was very jealous of the kids because if you're a good coach, your job is to stand back and let them do the work while you just stop them from doing anything dangerous.

But I really, really wanted to, you know, get in there and build robots and make them do the things the kids were doing. And somebody said to me, another coach from another team said, well, if you think the robots are cool, you should look into Arduino. And I said, what's that?

And I went on to explain. And I did a little research online and found a great deal of information on people's blogs on the Internet. And I also managed to attend a workshop nearby that had an Arduino lily pad.

And so my first exposure to Arduino in person was Blinky Lights. And it seems it never really left. I never really kind of graduated past that.

Just the complexity has grown, but the focus has stayed. But that just started everything. I started building projects on my own.

And then writing my own blog once I started doing projects that were original so I could kind of give back because I'd gained so much from what I'd read on other people's blogs.

Paul

You're well known for your LED projects, and earlier this year you shared the orb-sessed LED sphere. How did you make an LED cube into an orb?

Debra Ansell

Thank you for asking. I'm very proud of that project. That was one of those aha moments that just worked.

In general, I have a lot of ideas, and, you know, about 80% of them just never go anywhere, but they're fun to think about. I think most people, when you're talking about electronics, it's just cooler to see them in shapes that aren't, you know, that aren't square, that don't have sharp corners. So a sphere is obviously the ultimate interesting shape, but it's very hard to get circuit boards into a spherical shape or make the light, you know, get lights on the exterior of a sphere unless you're, you know, pushing a string through holes or something.

And so it always been in the back of my mind, you know, to do an LED sphere. And I'd never really come across a good idea until unrelated I was, I can't remember quite what I was looking for. I was looking for a way to map, just map computer graphics.

And I found this projection mapping that people often use to go from the surface of a cube to a sphere called a quad sphere. And they use that rather than the traditional latitude, longitude mapping, because you don't have the singularity at the poles that you normally do. And I saw that, and I said, well, wait a second, I know how to pipe light.

I spent a lot of my projects or how do I get light from one place to another. You get very interesting diffusion effects. So this is a mapping that if I could make a cube would really make it look nice in the sphere.

And I just began to obsessively work on it. And there's a reason it's funny. It's a joke, but it's also true.

The title of the article is Or Obsession. And it really did become an obsession for a very long time. It's just seeing how far I could take that project.

So, yeah, it was kind of an aha moment that said, wait, I got to try this. And everything really, it was the click that everything fell into place from. It was so satisfying.

It only took a couple of iterations to really get a working shell that I could place over on the outside of a pre-built LED cube. You know, people have done LED cubes for a long time. And I've seen LED spheres, by the way, too.

In clever ways, but nothing quite like the way I did it. So that was very, very satisfying when it all came together.

Paul

How did CircuitPython help with the project?

Debra Ansell

Well, I used CircuitPython for the version I wrote up for Make Magazine. And I always prototype. With few exceptions, most of my LED projects are prototyped in CircuitPython because I like the dynamic interactive nature of being able to, you know, change the code and see it, see the changes instantly in the LED patterns.

I was using a small microcontroller, one of the JOWs, I think the one with Bluetooth, NRF 52840 that runs CircuitPython. And what's nice, of course, is there's a wonderful LED animations library. that Adafruit is written.

So it's got a bunch of pre-built animations, and I often will use that and extend onto that library. So it was made mapping the sphere much easier because the order in which the pixel, I wanted to know where the pixels were in 3D space because it's much cooler if the patterns respond, you know, have a 3D spatial orientation. I was able to use the CircuitPython libraries.

First of all, the controller I used, I use the NRF sense. I'm going to get the numbers wrong. So it had a built-in accelerometer.

and microphone, and there's an Adafruit library already ready to how to get that data out of the accelerometer. And that was great. So I'm very lazy.

I'm not going to do any more work than I have to. So I could use the library for the accelerometer, the LED animations library, and then combine the two very simply to create a new animation that responded to orientation of the sphere. And then when I'm mapping the sphere, if I were very organized, I would have planned ahead for where the orientation of the pixels are going to be, given the mapping.

but of course I didn't. But the nice thing about mapping the sphere is to figure out the orientation of the matrices that made up the side, I could just light up a few pixels at a time with just a few CircuitPython commands and figure out what the orientation was as I went. So it just makes my life a lot easier. I'm a big fan of the interactive nature of the language for prototyping and the vast array of libraries that let me take advantage of a lot of hardware that's out there.

Paul

Your projects often combine a variety of skills, including CAD, 3D printing, coding, sewing, and more. Is there one skill you enjoy more than the others or one that you find more challenging?

Debra Ansell

The answer to that is I like all the skills. I love gaining new skills. And probably my favorite skill is whatever I'm working with at the time.

And I don't like anyone more than any of the others, but I love to combine them in unusual ways. Like sewing and electronics is one of my favorites. I love wearables where you're creating an accessory or a clothing item that's designed specifically to hold the LED strip or string that you're wearing with a pocket for the controller or 3D printing and electronics, which a lot of people do. It's a great way to, you know, protect your electronics. But if I can come up with a new, you know, way to combine skills that I've learned, it makes me really happy.

And frankly, the more, the better. I think the one I published recently in Make Magazine was LED tote bag, we called Back to the future, combined 3D printing and sewing and. and electronics and a PixelBlaze controller to make the patterns work.

So that was really fun to see what you can do. Anytime I learn a new skill, it kind of guarantees that I'm going to come up with a new idea, which I really enjoy.

Paul

You mentioned sewing and PixelBlaze, and I wanted to ask you about the PixelBlaze pillow project that you did earlier this year, which uses the PixelBlaze controller. What is PixelBlaze and how did it help with the project?

Debra Ansell

Pixelblaze is a wonderful, wonderful controller that makes, like CircuitPython actually just makes my life easier when doing LED projects. It was designed by a very smart programmer named Ben Henke, who does wonderful LED installations. And it is its own controller.

It works as its own access point to launch a web-based coding interface, which has a JavaScript-based editor window. And you can code your LED patterns and see the changes on the fly, which is wonderful. again, makes seeing how the code your writing affects the patterns very easy, because it's sometimes hard to predict how things will look versus the code you're writing on the page.

And it has a large number of preconfigured patterns that people contribute to the library and a very active forum that you can ask and answer questions in. So it's a very active kind of user base that's very helpful. My favorite thing about the PixelBlaze is that it has a pattern of libraries separate from the So you can specify for any project you do, you can go ahead and use whatever patterns you've written.

And then in a separate area of the controller, you can specify, well, here's where my pixels are in space. And it will automatically map whatever pattern you've created as long as it has the correct number of dimensions to the location of your pixels. So that's very nice too.

I can take patterns, you know, that I've written and I frequently do. There's some patterns that run on my sphere on my orb that the large version of my orb, uses the pixel place. The smaller version uses CircuitPython. But I can take patterns for the large version of the orb that will also run on my tote bag. That will also run on a pendant. The versatility and the ease of use and the built-ins on that controller are very, very nice for anyone who works with LEDs.

Paul

One of your first CircuitPython projects combined a Trinket M0 and a Raspberry Pi Zero to control LEDs sewn into a jacket. How did they work together?

Debra Ansell

That was a great project. I really enjoyed that. There were a couple of steps in that process. I'd been playing with jackets and LEDs, and they'd all had controllers based on CircuitPython and the LED animations library. And I was going to wear the jacket to Maker Faire, the last one right before everything kind of shut down. And last minute, I decided, well, it'd be really cool if people could program this jacket on the fly. So I wanted to use an access point, you know, an access point, have people be able to via a web browser be able to log it to the jacket and change the animations remotely.

So I set up a Raspberry Pi Zero and didn't then and still know very, very little about Apache, but set up an Apache server. And I could figure out just enough about the Apache server. I could get it to serve a web page that allowed you to use a drag and drop block code to create CircuitPython patterns.

The block code is based on the Blockly coding language. That I could get set up. But I couldn't, for the life of me, figure out how.

to get those new patterns onto the jacket until I realized that the, I believe it was a Trinkin M0 I was running the CircuitPython code on initially worked as a separate drive for the Raspberry Pi 0. So all I had to do was then once the code was generated in the web interface, save the Python file directly to the drive. And that I could do relatively simply without having to go into any kind of operating system or anything like that because you just save the file and Circa Python automatically picks up the code and runs it in the jacket.

So there's probably a better way to do it. But the thing, the way that works is always the best way at the time. And it worked and I got it and I was thrilled.

And it was just a nice little bonus of just the convenience of Circa Python showing up as, you know, the controller showing up as a drive on whatever computer you attach it to. So that was a lot of fun. And I was very proud of myself for getting it working and I still have no idea how Apache actually works.

Paul

I don't think anyone knows how Apache really works.

Debra Ansell

Probably true.

Paul

If people want to learn more about your projects, where should they go?

Debra Ansell

So my older projects are available on my blog, geekmomprojects.com. Those are mostly the kid-friendly ones. And the really well-documented ones, you can find I've written seven or eight articles for Make Magazine.

You can look at, that's a good place to go to look up archives of some of my more interesting projects. Those are the two best places to go. If you'd like a full instruction set, I do tend to post finished builds to social media, Instagram, and Mastodon.

But for instructions, my blog and Make Magazine are best places to go.

Paul

I'll make sure I link to those in the show notes as well.

Debra Ansell

Thank you.

Paul

Last question I ask each guest. You're starting a new project or a prototype. Which board do you reach for?

Debra Ansell

It's almost always the smallest CircuitPython controller I have on hand. So these days it's a QtPy or a Xiao because there's such a range of both of those. I think they just came out with a Xiaowith a camera and I've been dying to work that into a project.

And the QtPy is great. I'm a big fan of that too. I like the little connector.

What's the stem a cutie? I think connector, which makes it very easy to, you know, when you're prototyping, attach a variety of peripherals very easily and access them. So both of those are kind of my go-to boards and they're cheap, which is great.

Paul

Debra, thanks so much for being on the show.

Debra Ansell

Thank you for having me, Paul. I really enjoyed it.

Paul

Thank you for listening. Transcripts are available in most podcast players, and show notes are available at www.circuitpythonshow.com. Until next time, stay positive.
