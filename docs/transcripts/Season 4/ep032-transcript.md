---
date:
  created: 2023-12-04
title: "Episode 32 - Max Lupo"
---

## Show Notes

[Show notes available here.](../../episodes/Season 4/ep032.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. This episode, I'm joined by Max Lupo.

Max is a Canadian multimedia artist who constructs odd inventions. His work strives to find meaning in process, value and translation, and creativity in discarded or mostly useless things. In 2017, he graduated from Okad U's interdisciplinary art, media, and design program with a Masters in Fine Arts. He teaches sculpture at a community college in Ontario, Canada, and is the community librarian for the Innesville Idea Lab and Library. Max, welcome to the show.

Thank you.

Max Lupo

Thank

Paul

you for having me. I'm glad you're here. How did you first get started with computers and electronics?

Max Lupo

Once upon a time, way back in my first round of art school, I was gifted a MacBook, and that was fun for a long time. And eventually, Linux ended up on that computer. I started using Debian for a while. And once that got there, it was kind of a gateway into tinkering in the computer itself. And that was necessitated partly because Debian at the time didn't have great control of the fan or temperature of the computer, it seemed. And so I had to do something about that.

I wrote a Python script that later became kind of a graphic user interface for myself to manually turn on the fan. And then from there, learning more about Python. through some great books by Al Swigert, making little games, text adventure games.

And some of that was able to intertwine with my arts education and making projects that had some degree of interactivity to them, whether that was a simple button press or later on more complicated interactions. But yeah, it all started wanting to solve a problem for myself and then kind of learning Python as a way to do that.

Paul

Your art pieces over the years have used Arduino, MicroPython, and CircuitPython. How do you know which language is best for each piece?

Max Lupo

When I first started making projects, the Arduino was available and it was great. Being able to use a microcontroller for the first time and having resources and guides available. It was so exciting being able to add interactivity into a project.

And so the Arduino Uno really did a lot for me for a long time. As projects became more complex and as the Raspberry Pi kind of became available, those first single board computers, it again, and felt like a kind of a new world opening up in a lot of possibilities. As it was described to me many years ago, trying to choose between an Arduino or Microcontroller and a Raspberry Pi, thinking about how many ands are in your project.

And so if you need to create a text model and make an animated gift and display that onto a screen, a Raspberry Pi is probably your best option. Later on in my art education, I was working on my master's thesis, MicroPython burst onto the scene. And again, it was this opening up of creativity and possibility, just by virtue of being able to do so much on one little board. And then, of course, this time goes on, CircuitPython became available. And so now it's really kind of about the availability of the hardware itself, the availability of learning resources through Adafruit, which really makes kind of CircuitPython a great package deal. And that's, and even so far now is when I'm thinking of a new project and it might need a Risbury Pie, I'm inclined to try to think of a version of that experience that could live on a CircuitPython board by maybe pre-computing a text model and then just dealing with the text itself on a CircuitPython board perhaps. So yeah, that's, that's mostly where I'm at now these days.

Paul

Let's talk about some of the pieces you've created and shown at various exhibitions. You have a master's in fine arts, and your master's thesis abstract starts with, Beep-Boopatronics addresses discarded consumer goods, nostalgia, and the creativity inherent in adapting one object into another. Tell me about Beep-Boopatronics.

Max Lupo

Well, I'm so glad that we got to Beep-Boopatronics. So this, yes, was part of a master's thesis project. It works something like this.

I had a discarded chord organ. This is, imagine kind of an accordion, but standing still or sitting still. and so it needs air.

Air comes from somewhere. You depress the keys, and then sound is generated. And originally it had kind of an internal motor to make sound, and you would play your kind of composition.

So that's the central piece in the show in a way. But of course, the motor was broken, the outer shell was broken, so it was kind of garbage, except for the fact that the keys themselves still worked. You can press the keys, and that was just fine as a starting point.

Elsewhere in the installation, there was a small radio, that I had taken apart and reworked so that where you would normally choose a station, the little kind of slider, that was now just an opening to accept a punch card. And so this huge punch card role had a composition, a musical composition, punched in it as a series of holes. You would put it in the radio, and it would generate MIDI notes.

And so kind of musical information and put that over a wire. How did that musical information get there? Well, of course, it was a MicroPython board that accepted the light pulsative.

as notes corresponding to positions on the grid, all that information was piped through MIDI over a wire to a second micro-Python board that controlled an array of servos to depress keys on the chord organ. So we have, of course, now a musical instrument. The chord organ, as I mentioned, needs air.

And so part of this installation, if you haven't kind of seen the mild humor in play, the part of the installation was me constantly pushing up and down a hand pump to create enough air pressure in the system when a composition would play, you would be able to hear the sound because the servos would press the keys, I would be making air, it would all make terrible kind of music. It would make something similar to music, but only just barely related to it. And then eventually, of course, I would have to stop pumping, put in a new song, then run back to the pump.

Eventually there was a motor, a fan involved to kind of keep some baseline pressure. But the whole idea of it, Like why do any of these things? The thesis project generally was about this idea.

What do we do and how do we think about all this stuff? The chord organ, certainly for a modern musician or really anybody, isn't maybe that appealing. The radio on its own, you know, places all around the world are discontinuing analog broadcasts.

And so there's a future where that analog radio doesn't have a purpose anymore. So these two almost useless objects are here, and I have them, and I can think about them for some reason, and the reason being to kind of just see what happens when we make them interact. The thesis, you know, because it was a master's thesis, it had to really sit in some sort of ideological space, this idea of like adapting one thing into another and all these kind of maybe bigger ideas, but in a simple way it was just kind of a challenge in a way.

We have these two disparate objects. They're both related to music some way. They're both mostly discarded.

What can I do to make something interesting happen by kind of forcing them to interact together?

Paul

Sure. And I'll make sure that I link to all of these in the show notes, too, so people can see pictures and not just have the audio descriptions to go with it.

Max Lupo

Oh, great.

Paul

Your latest exhibition ran through December 6th and is called Continuous Memory, where you explore the power and playfulness of words using technology. But not just any technology, you used obsolete technology.

Max Lupo

Yeah, and so it's all kind of, yeah, part of this, these little pieces of the puzzle. We have all these items. And so continuous memory was a two-person show created and put up here in Ontario.

And the show itself has a old Centronics electric typewriter. And so, yeah, definitely. an obsolete little piece of equipment, but in itself was a part of an ecosystem. And so the typewriter, you could type on it as much as you wanted, of course, using the keyboard, but then also it had a parallel port on the side. And so how interesting that it had like this connection to the outside world. And so the obsolete aspect of it is in some ways an opportunity to, again, try to create something new, a new experience using like a CircuitPython board that then communicates over the parallel port to make it type out, you know, whatever I wanted to type.

And in this particular exhibition, it was meaningful because the things that would type out were sort of selections of stories from my own family's history as part of their kind of immigration to Canada from Italy. And so my father came over when he was 13 or 16. And I was able to take those stories and the typewriter at the press of a button will type out a story from his perspective, but then elsewhere in the show, there's a phone, there's these old rotary dial telephones, and when you pick it up, it tells perhaps the same story or a similar story from one of my other family members' perspective. And so this whole idea of like the past, nostalgia, these obsolete objects, in a way as you go through the show, or at least my work in the show, is meant to sort of push you towards kind of these feelings of memory and trying to pick up the pieces between something familiar, this typewriter, this story, for example.

And then as you find these other objects, you know, that story becomes more complicated. Hopefully your memories about your own sort of past experiences become more complicated. And so the obsolete objects are, in this show anyway, are kind of a way into hopefully that feeling of the past and recollection and things like that.

Paul

Tell me about your collaboration on the margin maker, which is described as a meditation on space, time, and the body, and the ways in which our corporatized nation-state enacts order on all three and how one becomes marginal when they are unable to follow acceptable sociocultural margins.

Max Lupo

Yes, and so this was an exhibition in Montreal with a fabulous exhibition partner, Pascaline Knight, another great artist. And Pascaline is left-handed. And in Canada, we have copious examples in our education history of this.

History exercise book. It's a pastel color book with a map of Canada on the front. And inside, it's, you know, these beautifully set lined pages, of course, the classic blue and red little margin lines and things like that. And so for Pascaline, in her experience, being left-handed and having to learn how to write in these little books and things of that nature, the left-hand goes forward as the right hand does, but your arm, if you're left-handed, is constantly covering the margin. So when you go to return back to that line, you're always obscuring your point of return, your writing looks messy, you're scolded by your teacher for not having good penmanship, and all these little things start to happen, and your approach to language is kind of informed by those experiences. And so Pascaline and I set about to take the form of this exercise book, these blue and red lines, and complicate them, make them strange in a variety of different ways.

And so Pascaline in her practice, she's a printmaker, so a lot of screen printing, different versions of the exercise book was her contribution to the show. And then I made a little circuit playground express power device, which draws a circular margin around a page, kind of like what a record player would do if you put some pens on the arm. All these things together are meant to kind of complicate and challenge this idea of, yeah, that perfect ruled line that we're all bound by when we're trying to write on a page.

And then the essay that you quoted was by a great curator and friend who wrote some observations on the show. And her observations, yeah, we're kind of extending this idea outward into what happens when you don't fit into a box. And I'm sure we all have experiences on a government form or something like that where you're trying to write your answer.

And literally your answer doesn't fit into the box, like your penmanship cannot be contained inside the little box. But then also potentially like the boxes that are available for you to check or fill out, don't really match your lived experience and you have to just do the closest one. That makes sense for you.

And so there's all these little examples where as soon as there's a rule, there's a margin, which is technically passable. We can always write in between the margins. But doing so comes with some sort of usually like weight or at least some degree of consideration on your part that we no longer fit in between these lines.

And so the show is playful. All these kind of big ideas sound like big ideas, but the show is very playful and silly. There were opportunities for people to run, or their own little drawing devices that were more mechanical and had that kind of experience of making those lines in red or blue ink, for sure.

How did CircuitPython help with the installation? Ideally, CircuitPython was there to kind of be a, collaborative point since CircuitPython text is just Python and it's almost plain language as if you were to read, you know, what a program was doing. And that was ideally meant to kind of be a point of collaboration between Pascaline and I. As the show went on, you know, I became kind of just more responsible for the coding part of it. But having that opportunity there to quickly prototype and be able to get feedback from Pascaline about what machine was doing and how she would like it to work or this or that or seeing her kind of work work.

with a certain part of it, just being able to kind of go back to the code so easily, um, make minor adjustments. And since it was a circuit playground express, being able to give kind of feedback to the user in the sense of like the LED lights and things like that was really useful, uh, for sure.

Paul

That's fantastic. Last question I ask each guest.

You're starting a new project or prototype. Which microcontroller board do you reach for?

Max Lupo

Ah, yes. So, so these days, I'm really excited by, the KB 2040. It's the Adafruit board that fits the Arduino Pro Micro footprint, and it's great. It has a USBC port, which apparently is a requirement for me these days.

I don't know why. It has a lot of onboard storage space, very compact. It used to come in purple.

I still have a few of the purple ones. I wish the purple one would come back. But yeah, that's my favorite these days, for sure.

Paul

Well, if Lady Ada's listening, Maybe she'll get that feedback. And I'm with you on the USBC. I've got a couple Picos, and every time I have to use micro-usb, I just kind of sigh and wish for a USB-powered board. I know. And if anyone wants to learn more about you or your work, where should they go?

Max Lupo

Yeah, and so please go to maxlupo.com. It's a blog. You can subscribe and get an email update or put that URL in your favorite RSS reader that should know what to do on Max Lupo underscore on Instagram, which where more of the art stuff is. and then follow the links to find where I am on Mastodon. I never remember the full URL, but I'm there too for more of a technical kind of approach to my work and what I'm up to those post ended up there.

Paul

Well, that's great. I'll make sure to link to all of those in the show notes as well. Max, thanks so much for being on the show.

Max Lupo

No, thank you, Paul. Thanks.

Paul

Thank you for listening. For show notes, visit www.circuitpythonshow.com. And transcripts are available in your favorite podcast player. Until next time, stay positive.
