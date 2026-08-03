---
date:
  created: 2022-07-11
title: "Episode 13 - Nicholas Tollervey"
---

## Show Notes

[Show notes available here.](../../episodes/Season 2/ep013.md)

## Transcript

Paul

Welcome to the CircuitPython show. I'm your host, Paul Cutler. This episode, I'm joined by Nicholas Tollervey.

Users of CircuitPython might know Nicholas as the creator of the Mu Code Editor. Nicholas is also known for music, philosophy, teaching, writing, and computing. Nicholas, welcome to the show.

Hello there. I'm glad to have you. You've had a very interesting career.

How did it all get started for you?

Nicholas Tollervey

Back in the 1980s when I was a kid, the UK government decided every school should have a microcomputer and that was the BBC Micro. My mum and dad were both teachers and my dad one half term brought home his school's BBC Micro thinking I'll just figure out how it works and what it does and how I can use it in the classroom and it took about half an hour for my brother and I to sort of prize it out of his hands and for us to get going on it. It's basically started from there.

And so all the way through my teenage years, I was using these sort of baked computers and things. And then I kind of got distracted with music, which I'm sure we'll come back to. And when my own children arrived on the scene, I got back into computing because it was a lot more lucrative than being a freelance musician, I can tell you.

And that eventually led to some work for the BBC. The BBC, as you probably know, created a device called a microbit. where they wanted to recapture those heady times of the 1980s, where kids were learning to code on BBC microprocomputers, and they asked for people to contribute to their project, and I was a PSF fellow at the time, and they mentioned Python, with the blessing of the PSF boards, I said, well, hey, you should talk to the PSF, I'm a PSF fellow, we can coordinate.

And so I became involved in the BBC Microbbit Project. I wrote a lot of the software that's to do with Python for the BBC Microbbit project. A lot of the documentation is mine as well and a whole bunch of other stuff.

And I got to meet an Australian gentleman called Damien George, who is, of course, the creator of MicroPython. And Damien, I don't know, it took him a weekend. He's got to brain the size of a planet that chap to basically get MicroPython running on this device.

And so that's how I got into Python, hacking, computer. uses the CircuitPython, MicroPython ecosystem. And it kind of all went from there, really.

Paul

So you started working on the Microbit. When that first came out six or seven years ago, how did that lead you to the Mu code editor?

Nicholas Tollervey

Well, one of the tasks that I had been assigned was to create a browser-based editor or MicroPython on the Microbit. And being the sort of engineer who likes to check their work, I ran a series of workshops with UK-based teachers and developers, and I would bring them all together, and all the developers would want to play with the microbit, and all the teachers would want to have a go with it and see what they could do with it in their classroom. And it was a good place for me to try out the tech that I was creating at the time to see, does it work?

And it became clear that, actually, it worked, but it could work better. And things like back then, anyway, it's changed now. back then if you wanted to flash the device, you had to download a thing, you had to find the thing in your file system, you had to copy the thing, paste it into the other thing, wait about 10 seconds, and then see, scroll across the screen, syntax error line 3.

Okay, so it's a bit of a pain in the neck. And so the other aspect of MicroPython is that you get a REPL on your device, as you know. And this is great for interactive programming.

And when I demoed this with a hacky script that I'd created in Python, teachers were like, whoa, It's like talking to the microbit directly. I was like, yeah, yeah, absolutely. This is what Python can do.

And developers enjoyed the fact that there's a Ripple because it's an exploratory, playful way of getting into the hardware and seeing what it can do. So putting all that together, I decided one afternoon, one Sunday afternoon, how hard can this be? If I were to write, a very simple code edit to that had a flash button instead of all the download and blah, blah, blah, blah, chigree, you just click flash and then it just kind of worked.

So you reduced the sort of dissonance in the development cycle. If you see what I mean, you were writing code, flashing, writing code, flashing. Or you could drop into a REPL and then type away.

And that's the origin story of Mu. And for a Sunday afternoon hack, I think I'm doing quite well.

Paul

I think it's turned out great. It's the go-to editor for so many people because, like you pointed out, having access to the REPL right there makes it so much easier trying to troubleshoot or change whatever you're trying to work on.

Nicholas Tollervey

Yeah, yeah. The other aspect of Mu is because it's a beginner's editor or it's aimed at people who are supporting beginners, we are not trying to do the big whizbang effects of an IDE or something like that. We just want to do the simplest possible thing so that people can graduate away from Mu and then use their VS code or whatever it is they graduate to.

But the side effect of that is it just does what it says on the tin. It means, you know, you've only got a few buttons across the top. What does it do? It does that. Go look at those buttons and explore and play, and we feel it in such a way that it has to cope with the working practices of 11-year-old beginners. So, you know, they are clicking like nobody's business. So we try and make new quite robust in that sense as well. I'm really pleased that people find it useful. Oh, it's great.

Paul

You had mentioned when you first tried starting to code move that you were looking for an online code editor. Is that idea still in the back of your head?

Nicholas Tollervey

So the online code editor was a part of the BBC's requirements, and that ended up becoming MakeCode. But the folks at MakeCode have taken out the MicroPython bit of that and put in their own Python thing now. But I do know that the MicroBit Foundation have a new web-based, browser-based Python editor, because handily enough, Carlos, who works for the Microbit Foundation, is also one of the core Mu contributors as well.

So I get to chat with him, perhaps every fortnight, and see what they're doing looking over the fence. So I'm very excited to see what they've been doing with that. And I've heard just yesterday from an electrical engineer friend who's been testing it, that he said it's amazing.

So when I see that, I'm going to be a happy little chat. You and me both.

Paul

It's great to see that there's continuing innovation in that space. Yeah, absolutely. You're active in music making. What is your music background?

Nicholas Tollervey

Okay. So the part of the UK where I grew up is, I guess, well, it's called up north, really. And up north, there's lots of coal mines and pits and all that sort of stuff.

And each of those villages has a brass band. And I grew up, there's a band in my village, and I'm a tuber player. The way music education works in the UK is once folks realize that you're enthusiastic about music or talented about music, you're kind of put on a pathway of what's called the grading system, where it's a bit like belts in martial arts, really.

You know, you start with your white belts and eight or nine belts later you're a black belt. It's the same sort of thing in the UK and other Commonwealth countries as well. And so I was put in one end of this sausage machine and went round and round around this mechanism and out came Nicholas attending the Royal College of Music.

It's one of the world's top music conservatory arts, really. I wasn't really expecting to get there, but they let me in. And within about six months of arriving, I realized that actually a professional musical life wasn't what I wanted to do.

I wanted to do other things. I wanted to complete my degree. I met my wife while I was there, which is the best thing that came out of that.

And I also worked as a freelance musician for a few years after graduating, and importantly, as a music teacher, which is what all musicians do when they want to have a stable salary. because clearly being a freelance musician is the worst job in the world if you want to earn regular money. So that's my background.

I'm a tuber player. How is learning the code and learning music similar? That's an awesome question.

To learn to play, I don't know, something like a tuba or a violin to a very advanced level takes many years of practice. Sustained efforts, self-analysis, if you see what. I mean, you have to think about what it is that you're doing, reflecting on not only how are you holding the instrument, but how are you engaging with the music.

It means learning from lots of different people. It means putting yourself into lots of interesting situations like playing in an orchestra or playing the string quartet or a brass band, blah, blah, all of these things. And the music world knows this. And so there are structures in place, like the grading system mentioned, that help you get from scratching away and entertaining the local cats to, I don't know, being Nicola Benedetti, a virtuoso concert violence. Okay. Now, the coding world has yet to catch up with this, but I think we could all agree that to become a good coder takes a long time. It requires self-reflection. It requires getting experienced by learning from others and all those kind of similar things to the music world apply to becoming a good coder.

Sadly, in the coding world, you'll see, you know, learn Python in three months and, you know, learn Pearl in 24 hours or everything you wanted to know about JavaScript, but we're afraid to ask in four easy lessons or blog posts or books to that effect. And that's great. We want people to feel empowered to learn to code.

But I also feel a little bit sad that actually what they're being sold is a bit of a false promise. You know, you and I and anybody listening or watching will know that coding is, I don't know, 99% being frustrated at why the damn thing doesn't work in finding out on Stack Overflow. And, you know, maybe 10% actually writing code.

it takes the acquisition of a certain sort of mindset and skill set that gets you to a place where you can be effective and autonomous as a software developer. And I think those in the coding world could learn a lot from the music world as a result of that. Because they're both very similar trajectories.

Paul

I didn't learn to code until I was older. And I came across this, I wish I could give credit to whomever said it. But they said, I'm not self-taught.

I'm community taught. It really stuck with me because as someone who it was, quote unquote self-taught, how much I've learned from other people. And one of the reasons I started the podcast was how much help I got around CircuitPython a year or two ago when I was starting and realized, okay, that kind of a community is so important.

Nicholas Tollervey

And just to shout out to the folks at Adafruit who have helped build this community and guide this community, what they are doing is best in class. They are phenomenal at this. we could all learn from the way they do their community management, the way they welcome people, the way they organize things, and just the way they embody what it is to be a friendly coda in the community is something to behold.

I have a list of names that I'm thinking of, and I'm sure you have, and they might even have been guests on your podcast, but I won't embarrass them by mentioning them now. But, you know, awesome work, AdiFruit, great stuff. Keep it up.

Paul

Your current passion project is called Code Grades, directly based upon your music education. Tell me a little bit about your project.

Nicholas Tollervey

Okay. So, I spent, I have spent since 2012, a awful lot of time thinking and working in coding education. Actually, 2009, that's when I set up the Python Code Dojo, where beginner coders got together.

I set up the education track at Python UK as well and did a whole bunch of other stuff. It was actually going to meet Dan, you know, CircuitPython, Dan, in Boston. on a train journey that I had the idea of, well, what would music education look like if we taught it like we teach coding?

You know, learn the tuba in 24 hours. You know, everything you wanted to know about the violin, but we're afraid to ask in three months or four easy lessons. You know, that's not going to fly.

Would you hire a musician to play at your wedding if they've just been to a three-month boot camp? That sort of question. Okay.

So that led me to ask, well, how could I flip that table and flip, flip the tables and say, What would coding education look like, if we did it like, we do music? And I realized, you know, I'm a classically trained musician. I could use the stuff that I learned, both as a student and as somebody who had to teach this sort of stuff.

And bear in mind, we've got a thousand years of Western musical history to draw upon. So part of me was being that lazy engineer going, well, surely somebody's done this before, that I can borrow the ideas and so on and so forth. The other aspect of this is that my wife's still a music teacher, and she's a very good music teacher, and I see what she does all the time.

And she sort of inspires me to think, well, how would that work in the world of code? So we get code grades, which is just one aspect of music education here in the UK, which is that kind of pathway. Like martial arts belts, you start at grade one or white belt.

You present a very simple project that demonstrates certain core concepts. that are quite simple because it's grade one. You present that to a mentor, and in a process that's a little bit like code review, they assess you, they get an idea of your level of attainment, and then you get a written feedback and score at the end.

So you've passed your grade one with a marker of 75, which is a pass with merit, and you go, oh, that's good. And at that point, the requirements for grade two come on your radar and feel within reach. So it's like stepping steps.

You know, if you were to look at grade eight or black belts and you're from the perspective of a white belt or a grade one, it would look impossible. But by going through all this process of the stepping stage, you're moving towards gradually a place where you feel that you can do those things. And the other aspect of this, which I have personal experience of, is that it's a great antidote to imposter syndrome.

So when I was a young musician, one of my music teachers said, you should audition for the local. youth orchestra. And I was like, oh, gosh, I can't do that. They're so amazing. And they're also all big kids, and I'm only 14 years old, blah, blah, blah, blah. But the minimum requirement, Nicholas, is that you're grade five, and you've just passed your grade six. So you're definitely qualified enough to do this. You can't argue with that. And actually, it made me feel, well, okay, maybe I am good enough. There's a lot of imposter syndrome in our world of coding.

And by having an independent third party, a code mentor, who's a professional developer, assess your project for a particular grade, demonstrates that, you know what? Yes, you are at grade five Python level. You know, don't get yourself down.

You deserve that. And you deserve that mark at 75 or whatever it is, a high-ish mark. So, you know, it's a way of helping people get the wind in their sales, interact, you know, learning from the community.

as you say, by interacting with professional software developers who are going to be their kind of mentors, assessors. And it's a way of finding the smaller steps that get you across the big step that is the chasm between, you know, a complete beginner to somebody who's a competent coder. That's code, it's in a nutshell.

Paul

We've been talking a lot about education. You've taught music when you were younger to the work that you mentioned earlier at PyCon to the microbit to code grades. Was that a purposeful decision, a conscious decision, or just coincidence on your part?

Nicholas Tollervey

50-50. I'm a very intuitive sort of a person, so I follow my nose. And perhaps the places where I go orient me more towards perhaps educational things or, you know, show that that's the case.

But I have this theory. When I want to learn something, actually I try and teach it as well. Because in order to be able to teach the thing, you have to have internalized what.

what it is that you're trying to teach. And you have to understand it well enough that you know how to make analogies or use metaphors or given that this is a particular sort of beginner, I'm not going to blind them with all this science. I know which of the simple concepts to introduce them to without overburdening them or what order to introduce those concepts.

And that clarity of thinking is a really great way of learning yourself. So teaching is a great way of learning. And I often say to folks, you know, let me try to explain that back to you and tell me when I'm an idiot when I've got this wrong.

And that just works for me. I guess, yeah, that's part of me, really.

Paul

We're so grateful that you've been involved with education for all these years. All the things that you've brought to the table have just been great. Thank you.

Thank you. I've been asking all the questions. And before we run out of time, I wanted to give you an opportunity to ask a question.

Ah, why, yes.

Nicholas Tollervey

I do. So you're an experience today. other sorts of collaborator and sort of member of the CircuitPython community.

So, I don't know, an educational event here. So what piece of advice that you didn't know you needed to know would you give to your beginner self? Okay, so this feels very Donald Rumsfeld, kind of there are known knowns, there are known unknowns.

What's your kind of unknown unknown that you now know? And you've touched on it.

Paul

And it's kind of simple. It's just do it. jump in the deep end. Put that imposter syndrome aside, and it sounds so much easier to do than it is. I understand that. But I was lucky to have a mentor in open source when I first started in the Ghanom community, and that was basically her advice was just go do it. This is open source. No one's going to turn you away. The very rare project that's toxic and is an open to newcomers who want to help. The best advice I can give you is reach out to someone, tell them you want to help, or submit that pull request, submit that patch, write some documentation, help with project management marketing.

There's so much more to coding in open source projects than just coding as well. That would be something I would tell myself because I didn't know how to code when I first got involved, which didn't help with the imposter syndrome either because everyone else around me could code. But honestly, that's the one thing I wish I knew then that I hadn't waited as long as I did to get involved. And those are some lifelong friendships I've made in open source community.

And it means so much to me. And this is just, you know, one small way of giving back the other podcast.

Nicholas Tollervey

I was just going to say, and here we are.

Paul

Exactly. Nicholas, last question for you. You're going to start a new project. Which microcontroller are you going to reach for?

Nicholas Tollervey

Circuit Playground Express. It's kind of the mother ship, as it were. It's the first CircuitPython board that I became familiar with. It's the one I used in the MicroPython book I wrote for O'Reilly.

Limor and her colleagues, Adafruit have put so much cool, funky, stuff on something that's so small. I wanted to do an example project on code grays. The thing I thought of was using one of these with a COVID mask to do a kind of an emoji type thing. You know, you could make the LED, neopixels, you know, make it look like it's smiling or it's frowning. You know, it has to be this. It's so fun. It's so easy and it's so cool.

Paul

I couldn't agree more. It was the first CircuitPython device I bought and it was a gateway. it just opened up all these doors for me.

Nicholas, thanks so much for being on the show. You're welcome. Thank you for having me.

Thank you for listening to The CircuitPython Show.

Speaker 3

For show notes, transcripts, and to support the show, visit CircuitPythonShow.com. Until next episode, stay positive.
