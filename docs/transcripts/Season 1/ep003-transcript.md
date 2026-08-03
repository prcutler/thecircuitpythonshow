---
date:
  created: 2022-03-15
title: "Episode 3 - John Gallaugher"
---

## Show Notes

[Show notes available here.](../../episodes/Season 1/ep003.md)

## Transcript

Paul

Welcome to the CircuitPython Show. I'm your host, Paul Cutler. Today in episode three, I'll be talking with Professor John Gallaugher of Boston College.

As founding faculty for the Boston College TechSpark programs and the former co-lead of the school's graduate field studies in Europe and Asia, Professor Gallaugher has had exceptional access studying technology growth and impact worldwide. Professor Gallaugher and his students spend several weeks each year, visiting with and attending masterclass sessions hosted by technology executives, entrepreneurs, and venture capitalists. This unique opportunity helps provide his teaching and writing with a broad, deep, and continually refreshed perspective on key industry trends and developments. Professor Gallaugher also works closely with collegiate entrepreneurs and his co-advisor to the Boston College Venture Competition in an organization whose affiliated businesses have gone on to gain admittance to elite accelerator programmers, such as Y Combinator, Tech Stars, Mass Challenge, and more, to launch multiple products and raise millions in capital.

Professor John Gallaugher, welcome to the show.

John Gallaugher

Thank you so much for having me.

Paul

I wanted to talk to you because you're currently teaching two classes at Boston College with one featuring CircuitPython.

What inspired you to add CircuitPython to your curriculum?

John Gallaugher

Sure. Well, first, thanks so much for having me on. I mean, it's always such a wonderful thing if somebody takes an interest in your work.

So it's my pleasure. It's really great. And good luck with a podcast, too.

I think that this is going to be a wonderful thing for our community. Thanks. And it's worth saying thanks to the community.

I mean, you say, who inspired you for that? It's really, you know, the people who took a Python together. This wonderful open source effort and really all the things that Limor and PT have done at Adafruit have been just amazing.

I love sharing their story with students. I love using their products with students. And so, you know, that really prompted me to go ahead and start to experiment with this stuff.

I'm not an engineer. So I was computer science as an undergraduate. My PhD is an information system.

So half in tech and half in business. I've been teaching managerial classes for 20 years and worked closely with our student entrepreneurs. One of the biggest issues that they had was they couldn't build their vision.

So about six years ago, we did a zero to full stack app development class. I don't think anybody really had anything like that. So we could take somebody in that did nothing.

We move really, really fast. And by the end, they build something, which is, you know, it's a real iOS app and Swift.

Paul

Oh, that's awesome.

John Gallaugher

Yeah, they're doing their stuff in the cloud. It has multi-user login. They're saving images and data.

It's like Yelp. And so that was sort of the second bit of a stool. So we had the managerial piece, and we had a programming piece.

And a lot of our students were really interested in hardware. And the fast, cheap hardware revolution, the maker revolution, they sort of go hand in hand. CircuitPython makes things so much easier than, you know, in the Andredo world.

You know, there are so many wonderful standards like Qwiic Stemma QT. Right. And so, you know, you could really get students to do some fairly sophisticated engineering stuff that was, you know, responding to distant sensors and doing, you know, wild anima and I know you had catney on, I guess. Did she come on yet? We're using her library, which is just wonderful with our students. And so, you know, a student with just a few lines of code and not even having to break out a breadboard can build amazing things.

Paul

You know, I didn't even think of it from that angle that you don't require a breadboard, right?

John Gallaugher

We're so used to thinking about microcontrollers that way, but when you grab a circuit playground, Bluefruit, Express, it's all right there. It really is. And, you know, it makes things easier for me as an instructor. and it's tough to tell, sort of looking at me, but I have really bad vision, so bad that I can't drive. So I'm working with a breadboard, I usually put these magnifiers over my eyes so that I can see things. And I'm still constantly getting stuff in the wrong pins.

And I think everybody does that, even if you have decent vision. I do it all the time. And so by taking that out, that's yet another, that's, I think, sort of the engineering equivalent of having not enough parentheses or too many parentheses or getting your indentations wrong in Python.

It's the stuff that kind of gets in the way of learning. So, you know, these standards are just so wonderful to be able to get students up to speed really quickly. And the glow that you see on their faces, when they accomplish things, they get stuff to happen that they didn't even think that they could be doing a few minutes ago

Paul

is great. I know the first time I started playing with it, just getting a simple LED to turn on or blink, you're just like, yes, I did it. So I can only imagine what it's like for college students.

John Gallaugher

It's super fun. And, you know, one of the things here at the university, so Boston College is a Jesuit University, which there tend to be some students. Part of the mission of the university is people for others, men and women for others, people for others.

So there is a lot of civic-mindedness in the student population. And I think that happens with undergraduates in general. I think we're probably a little bit more weighted for that.

Even in the school of management, there are a lot of students that want to use their powers for good. And I think low-cost hardware provides a way for them to think about that kind of stuff. So, you know, we do some interesting things in class where students partner with an on-campus school that's actually, so we have a campus school which is run through the school of education are partnered with our school of education where kids from three years old to 21 years old that have pretty severe developmental and physical disabilities it's a school for them. And so our students work on physical computing products for the campus school and we just started this last semester but we bring in folks they work with the client base there and it's just so empowering I think for students to see, hey I can take things from class, I can build real projects, I can see them deployed, and I can see them impact somebody else's life.

And that's so much of a difference from a conventional class where you might be working with somebody else's data for data analysis to learn data analysis or writing a paper that just you and your professor will see. So it's a real privilege to be able to teach this way and share that experience with my students and with campus school.

Paul

Accessibility is something that I'm really passionate about. Are there any examples that come to mind of what your students have built that the students in the school are using?

John Gallaugher

Sure. They actually have a coffee shop on campus, so they just have a few things on their menu. But as you can imagine, you know, somebody that's very, very restricted in a wheelchair and has really serious mobility issues. So, you know, maybe you can only tap accessibility buttons on their chair.

And maybe they're nonverbal. You know, running the coffee shop is a real challenge for them. But one of my students did a cash register.

So, you know, they could control via light touch switches on their wheelchair that just plug into a standard RCA jack, which is common in accessible technology. They could control the cash register drawer, you know, make it open and close, and they could also trigger a thank you across the back. So if you're nonverbal and most of the kids are, you know, they can thank books.

Genius. That was really nice. Oh, this is great.

Another group said, you know, kids are kids. They want to play. And, you know, if you have certain physical challenges, you can't throw a ball back and forth.

But they took LED matrices and the kids can pass the animations back and forth with LED matrices. And it's Bluetooth that communicates between the matrices. And again, not a breadboard involved in this.

It's just, it's wonderful. So really, I want all the people that are volunteering in the CircuitPython community to hear about this stuff too. Because I think they know that they do really great work and they should and be really proud of it.

But man, there just have to be tens of thousands of people out there that are really changing lives and impacting their own lives through their good work. So if we can get Scott and Dan and Kattni and all of those other wonderful folks, Liz from BlitzCity I know has contributed. and I know I'm going to forget some folks.

I haven't met any of these people in person, so hopefully at some point we will. Right. That's the beauty of open source.

But all of you, you know, you get big thumbs up, and thank you, and I raise a beverage to you guys.

Paul

Going back to something you said a minute ago about conventional teaching, how are you teaching your undergrad's hardware? I believe you shared a video with me that I'll put in the show notes, and I think you called it a flipped class. So how are they getting hands on?

John Gallaugher

So this sort of came out of, there was a lot of talk about flip class and teaching innovation, And there's certainly a lot of talk about this kind of stuff. It's tough to sort of change your model if you've been brought up in a model, and this is what teaching looks like, and these are the materials that you're provided with. But when I had planned to do the programming class, the zero to full stack class, I had recognized if we want to try to teach somebody app development programming at the same time in a class that may have programmers, but that invites non-programmers in, and about half the students haven't taken a collegiate coding class.

We also get fourth-year computer science students. If we try to have them all in one space, that can be messy. And sometimes students are going to ask questions or want to roll back what I just said.

And so there's this idea of the flipped classroom, which is you take your lessons and you have that outside of the class in homework time, usually delivered via video. And students follow along and do something with the lesson. And then in class you would do what normally would be in homework time, which are assignments, that extend and really emphasize and make sure that students are taking away the things from the lessons that they should be taking away.

So the real challenge for faculty is that means you've got to film everything. And I guess like a lot of content creators, like I'm not really happy unless the quality is decent. So I spend a lot of time there's usually a couple of days ago in every single video.

I know that feeling. I'm sure you do. And I keep thinking, well, I'm going to get better.

And it still takes just as long. But what's I think really special for students in this kind of experience. And so, you know, my class uses just CircuitPython just to kind of give you an experience.

There are no requirements for this class. We start off with a circuit playground bluefruit. We migrate to about a third of the first of the first of the, the way through the course to the Arduino Nano RP20 Connect.

So that runs CircuitPython. It's one of their new boards that use the RP 2040. And we finish up on a Raspberry Pi. So they all get three A pluses.

So it's Sips Power, but it's cheap and it has an audio jack, which was important for some of the things that we wanted to do. But they're using CircuitPython straight across on all of that stuff.

Paul

Including the Pi?

John Gallaugher

Yeah, they are. Yep. So I have them put Blinka on there.

And they do robotic stuff and they actually do MQTT. by the end. So we have students that have never written a line of Python code that are doing MQTT stuff by the end and real internet of things. I've written an app for them to be able to trigger stuff over Wi-Fi on their pie. So, you know, they can do really whatever they can code up.

But what's wonderful about this stuff is first of all, I think a lot of students get discouraged in coding who have not had the experience of being able to code before. So you get the ringers that have had engineering in high school and have been coding since junior high or earlier. And they can intimidate the other students, and it's so easy to see a few students that are succeeding and getting it all right away. And learning to code is like learning a foreign language. I mean, you have to kind of go through the pattern several times before it clicks. So what's nice about the flipped class is if it doesn't click the first time, you just rewind it. If it doesn't click, you can rewind it again. You're never in the class with, you know, again, it's so dangerous making gender generalizations, but most of those high-performing students are like the dudes that were attracted to something as undergrads.

So I think physical computing is something that is easier entryway. It's fewer women, fewer students that may have had not have had the privilege of having a classroom with high-end computing that was involved. They will be more likely to be less discouraged in a class, I think, because you're not there feeling like everybody else is getting it.

What else is really special about that is, you know, if you've been sitting in a class and you had to go to the bathroom When a professor introduced something that you were going to use for the rest of the semester, I mean, you were hosed. So, you know, with this, you can continue to rewind. But as a faculty member, too, I enjoy having office hours.

I think one of the toughest things in office hours was to have students that would show up and say, I'm totally lost. And in a flipped class, you never have that happen. A student will say, I was trying to do this and I'm not really sure why I did this.

Or, you know, I've been trying to repeat it and I'm not sure why my code isn't working, but the code on the screen is working. So they submit stuff, and they submit in GitHub and the, Swift class, they submit through Canvas our learning management system in the CircuitPython class, but they're coding in moo. And yeah, so that's how it works. So in class, we have challenges for the most part. I will introduce some new things in class from time to time or just say, hey, does everybody understand this? I'll bring in stuff too. So for example, here on my table, they were learning last week how to do LED animations with Katney's stuff. And so I've got this little Fibonacci 64 from the evil genius labs folks. And, you know, I mean, it's the same library that you use on this. All you need to do is just change the pin number.

So just showing them, hey, the possibility of what they've learned because of CircuitPython, you know, it works on other boards. Their code can migrate. You've just got to change these few attributes or parameters.

It's kind of like the Java promise that we had where you write once run everywhere. We really see that with CircuitPython. So those guys are delivering. But the classroom, and I'm so sorry to win back on you.

This is why I wanted you to be on the show. Well, good. But the classroom atmosphere, I try to make it fun. So we just had a class last night, which was similar to I did like sort of a little summary video that I shared with you.

So if it's in the links and so if you can check that.

Paul

Oh, the video you shared that I'll put in the show notes is fresh, brand new.

John Gallaugher

Oh, good. That's wonderful. So I actually did that last semester, but this week we did the same exercises.

And so, you know, I'll say, okay, students, you know, you learn how to do animations, you learn how to work with different sensors. So we'll work with potentialometers. So I'll have them use a potentialometer to control a servo because they have one lesson on potentialometers, one lesson on servos.

and I'll set up a little piece of paper and candy around the piece of paper, and they bring their potentialometer and servo and their circuit playground bluefruit up and turn the potentiometer and point to the candy that they want, so they can leave with that. Or we have another thing where they build a goblet of glory, and so they learn how to play sounds. So they also use the accelerometer.

So when they lift up their goblet of glory to toast, the CPB is in the base of it. It detects movement along certain axes, and will play the Boston College Fight Sals, or the Harry Potter theme or the theme to be your clones. So yes, all this fun stuff.

But they love it. And I tease my students, and I mentioned this to my wife earlier this week. I said this before, though, to my colleagues.

I really think that you should teach programming like a Peloton class. I mean, I think that you should be shouting out and celebrating student success and encouraging them. And it's a little tough to do that first if they've never done it before because they kind of freak out like, whoa, he's out here with us and stuff.

and he expects us to hoot up. But after you break through that, you give him some candy and things, it's a really fun place to be. And coding class should be a fun place to be.

And if folks flub, you know, you can see other people struggling around that or, you know, plugging things in the wrong way. And we encourage students to talk to one another during the in-class exercises and the flip class. So there is a much more collaborative environment.

I find, you know, since the students are walking around and coming up to me, I'm getting to know the students better. I get to know their names faster. Oh, sure.

So it breaks down a lot of the barriers where a 19, 20-year-old may be kind of reluctant to come into a professor's office that has all of these books in them and stuff. I have lots of geeky projects in my office, too, to let students play. So that's another thing that's a good thing for educators to do is build lots of fun stuff for students to try out.

Paul

Hi, it's Paul. I'll get you back to the show in just a moment. I wanted to say thank you for listening.

If you like the show, please hit the subscribe button, write a review or tell a friend. You hear that a lot, but it really does help. For other ways to help the show, visit CircuitPython show.com slash support.

Now, back to the show. So in addition to collaborating amongst each other, you recently challenged your students to also collaborate with the greater CircuitPython community. What did you have in mind there, and how has that been going, in your opinion?

John Gallaugher

Yeah, and I'll be really frank. I have a PhD. I was a coder in industry.

I led software development teams, and after getting my PhD and information systems, I've been teaching managerial courses for 20 years. So I had to relearn to program when I decided I was going to program. And I'd actually experimented with Python on hardware.

The university gave me a grant to buy 100 circuit playgrounds and share them with my students so we could see before I built this class, how did students receive, being able to do just a little bit of Python in that? It was a great thing. But I have had to learn myself, and there's plenty of stuff that it takes a while to figure out, or I'll read online, and the technical description in the documentation isn't clicking, a wonderful learn guide just tries to implement things in a different way that I'm trying to do it.

And the Adafruit community has been wonderful for me. And I think one of the things that's important is just feel comfortable letting your guard down. So I think the thing about having a PhD is all it takes is time and commitment.

And sometimes you don't have that. So, I mean, there's so many people out there that are way smarter than I am. But I have no problem saying, hey, I don't know how to do this really basic thing in Python.

Can somebody help me out? Or, you know, I think I knew how to do it, but I don't know why I. this data structure is behaving differently than I expected it to. And the Python community, they're like this antidote of, at least, I should say that particularly the Adiferate communities, and the maker community, I think you can say in general, it's the antidote to sort of toxic Twitter culture and tech culture.

You know, they're so kind and they celebrate each other's work and they're funny. And so the Discord community, I can't believe that there are these, you know, brilliant geeks that lurk and are willing to just, like, throw down knowledge within minutes of you asking a question. And so I encourage my students, money of the students are getting it.

And really what you have to do as a faculty member, I think sometimes is to continue to remind students two or three times, and then what will happen is a student will do it, and then they'll tell everybody, hey, I use this thing, and Gallaugher is it fleecing us. There's a real value here. A little validation.

Yes, oh, it's great. So I've been trying to get them to do, I've encouraged them to sign up for the podcast. Thank you.

But also, for my students, they're working on original projects. So the class is called Physical Computing, art robotics, and tech for good. So there's sort of a mix of different projects they're doing three different projects during the course of the semester.

And so like the Python and Hardware newsletter, they end puts together every week. That's really cool because it sort of is a one-stop scroll through take a look at inspiring stuff that the community is doing. I encourage them to follow a bunch of people on Twitter that I've thought have been really great.

Debra Ansel with Geekmom Projects has been doing some wild stuff. I think everybody that I mentioned earlier, and I want them to see that stuff because they'll say, hell, I wonder if I can adapt that for myself or, you know, take a look at a learn guide or something. So it's a new way for students to think about this.

And I think that they've had, you know, the history professor that has said, you should read these five books, and they don't have time for that. But proving to students that, hey, this really is worth your time, and it'll help you do more, and it will inspire you more. The community really deserves big ups and props for all of their kindness in helping newbies get in there.

just definitely make sure that you're aware that students may have zero knowledge when they're starting, but it's been wonderful. And again, this is, I think, a really great thing about the Ata Fruit Company is that they have each week their show where they celebrate cool stuff that they do. They put together the newsletter, and there's no marketing in there other than that it comes from Ata Fruit.

So they have really led with culture in the community they're trying to create, and I think that they've done it. It's really fun as a business professor to point to what Lomor has done and said, Here's a woman engineer who founded her company, who's manufacturing in New York City. Companies clearly built with values and passion, and you don't necessarily, the model isn't always Zuckerberg.

And if you build a billion-dollar company, that's awesome. But I think ladies really inspired a lot of folks, and she deserves more credit than I think she's receiving in terms of being a real role model for another way to build a business that sometimes isn't seen. I mean, she hasn't accepted any venture capital.

Right. It really is very different from many of the firms that we otherwise talk about in class and celebrating class.

Paul

So in addition to your class, you've shared almost all of these videos online. I think the Swift video on building a full stack app is over 125 videos. You've got maker snacks, little bite-sized CircuitPython. Tell me a little bit about your YouTube channel and how that came to be. Sure.

John Gallaugher

I figured if I was going to do a flip class, why should I put it behind the firewall? So initially I thought, oh, what if people find the stuff? And what I'd realized was sharing stuff, it's useful for a bunch of reasons.

One is sometimes it's just hard to stay motivated. Even in a faculty member, and being a faculty member, I mean, it's just such a wonderful job because you're constantly getting feedback in terms of your performance. And if students like what you do, it's great.

You know, you've got to see it in their eyes and you hear from them. Being a faculty member in the age of social media, I'm really active online, but one of the reasons that I do that, I tell my students, I look forward to exploiting you, but in the most positive of ways. So, you know, one of the things I did on LinkedIn yesterday I had a student that was applying for a particular consulting firm and said, hey, do you have any former students that I could chat with before I interview?

And so, you know, I was able to throw that out. So this generation of faculty members that I'm part of, we have these resources where we can help students, if we're motivated to help students, if that's what drove you to be a faculty in the first place, and it has for me, and we can really lean into that. But, you know, what's great is, you know, sometimes you get down.

And, I mean, COVID has just been terrible for everybody, I think. And, you know, I have kids that are going through their stuff. and it's such a challenge.

And so when you hear from some truck driver in Australia that says, hey, mate, thanks for your stuff, that helps me want to get back in there and try to create some cool stuff. So my motivation as an educator was really to reach other people and to help them learn. And YouTube helps them do all of that.

So I started first with the YouTube stuff and then I wrapped a cheap book in the app store that's less than $10 as students can get that just got reference material. Hopefully I'll do something like that with CircuitPython. at some point. But yeah, for the most part, it's just the motivation of being able to reach more people.

It would be nice to see it become really big, but I don't know if what I do is really gets that, that kind of stuff. You know, it's nice. I'll probably continue to do it into retirement, even if that ever happens. Who knows? They let faculty teach till they're really old as long as they're able to deliver the goods.

Paul

Well, I'll make sure to include those links in the show notes as well, because those videos are really cool.

John Gallaugher

Thank you. I'm really glad to hear that. It's nice to hear.

Paul

Well, everyone learns a little differently, right? Some people might want to read a guide on Adafruit.com. Someone might want to, you know, watch the video. Someone might need a friend to show them how to do it. So it gives them another avenue to learn. Absolutely. Yeah.

John Gallaugher

Thank you very much. It's a very kind of you to say.

Paul

So you mentioned one of your students is applying for a job. What are some of the cool things your former students have gone on to do?

John Gallaugher

So, you know, I'm really lucky to have the flexibility that I've had in my career. So I'm a tenured professor of Boston College. So what typically happens is, you know, you're hired as a faculty, you have a research commitment. You've got to meet a teaching bar to. And then when you're promoted from assistant professor to associate professor, you're sort of a junior partner and you have a job for life. Really, the difference between an associate and a full professor is, for the most part, just high-end research. I'm fortunate to be in a department where there are a lot of really great high-end researchers, and I'm also self-aware enough to recognize that that's not motivating for me. Even though I met the bar, and it was great to get tenured, it is much more of a struggle for me than sort of writing wider market stuff. So students like some of the smaller things that I was writing.

So I wrote a managerial textbook, and it's being used in a lot of programs and stuff, which is great. And I found a low-cost publisher that sort of strikes the balance between, I don't feel like it's the evil $200 textbook, but when you create content like that, it's a lot of work. So the fact that there's at least some kind of benefit for that is great.

It's like Ata Fruit wouldn't give all their stuff away for free kind of thing. Right. Yeah, it's nice.

It's expensive. We reach a lot of students, which is great. At the university, after getting tenure, I tried to look at some interesting teaching experiences that we could do.

Because students really, while we gave them a lot of value in class, they really enjoyed connecting with people in industry. And it's especially important in business school. We're almost unfair to students in suggesting to them that they've got to choose a major for their career path when they're 19 and 20 years old.

Paul

I agree.

John Gallaugher

You're going to be an accountant for the rest of your life or whatever. So we have this unfair advantage being in Boston and that it's a wonderful city where there are lots of different businesses and especially for me being in tech.

So I would take students on the subway. It's a trolley and it becomes a subway that's right on campus and at the bottom of campus, and I'll take them into town every weekend, or every Friday, I should say. And we would visit with Google's office, Microsoft's office.

Microsoft has an office called Nerd, New England R&D in Cambridge. They're down by MIT. They met with Rodney Brooks, who's one of the great robotics pioneers when he was running a company called Rethink Robotics.

And the list just goes on. So one of them that they meet with in this class is a guy named Brady Knight. These are young people out of MIT.

They found it a few years ago. They have a robot restaurant in Boston called Spice, SPY, CE. And Sweet Green actually bought them at the start of last semester.

But it's, yeah, robots sort of prepare your food. And they started out with Arduino in the basement of where they were living. All of their hardware runs on Python.

So for my students to see somebody just a few years older than them that's built this wild business with Python on hardware, they're using servos, they're using DC motors, so they can kind of see a path for them if that's of interest to them. So we can do all this unfair stuff. A few years ago, some of our alums in California had said, hey, do you want to do anything for our students out here?

And at the time, I was running our East Asian field study program. So I had worked abroad myself, and they'd asked me to do this program. And the model was, you know, students would be in the class, and then for half the semester, we would just compress that within three weeks and we would go abroad.

So we did the same thing with this program that we call TechTrek at Boston College. Students study how companies go from startup to blue chip. And then in the Valley, we would visit with 20 firms.

And they were mostly alumni connected. And it's so hard to get exact time, but there's such a sort of attachment to the alma mater. So part of the access that we had, for example, was we have an institute on campus that was just started a year ago called the Schiller Institute.

So Phil Schiller is the marketing head of Apple. And he was up until last year. And Phil was always on stage with Steve Jobs.

He's always on stage with Tim Cook. Most of the time, he was the guy that held up the new iPhone when they were introduced. Say for the year when Steve introduced it, and my students were actually there at the launch of the iPhone.

So the last six Apple introductions, Phil had invited us out as part of our tech. We ran our tech track experience then before the semester started. One of my students was sitting next to Larry Page from Google.

So we'll do 20 visits like that where we'll go to Sequoia Capital and we'll go to startups that, in many cases, some of my former students have started. And Twitch and Facebook and Twitter and Zinga. So this started more of a pipeline for our students to work on the West Coast.

It started more of an interest in student entrepreneurship. And one of my first students built a company sold at the Chase for $400 million. It was just crazy.

A company called WePay. And he started hosting our students and hiring our former students. We've had three other unicorn companies.

So Uber bought a company called Drizley a little over a year ago, I think. That was started at Boston College. I sort of teased my students.

Of course, it was students at the university who created the business where you press a button and beer shows up. But, yeah, Uber bought them for, it was a billion dollars. It's just crazy.

And what's fun for me is, you know, when my students come to office hours, say, you know, you're sitting in the exact chair where the three Drisly guys, the three founders, had set. Right. So, you know, the people that go ahead and start these businesses, they're way smarter than me.

I mean, I'm just fortunate to sort of be in this role where I can provide them with rocket fuel, I can provide them with connections, I can create experiences where, you know, alumni or other executives really like speaking with young people and they'll drop knowledge. So it's great. And so we've done programs in Silicon Valley.

Valley in New York City. I ran an experience called TechTRAGana with my colleague Betty Banyani at Boston College for three years where we would study tech firms in West Africa. And that is really inspiring because when you think about what low-cost tech can do, in terms of mobile money, in terms of what it's doing to empower farmers with farmer information, lots of people don't know that Google has an AI research lab and a craw in sub-Saharan Africa.

All that's super fun. We ran a boot camp in Dublin, Ireland, so BC's got a facility in Dublin, so we back my class into three or four weeks over the summer. So if there are any faculty that are at cool international locations and want summer programs, let me know.

Maybe I'll bring my students over and we'll do something jointly for app dev or for hardware. That would be a lot of fun for me.

Paul

There you go. Well, you're doing great work, both with your students and then sharing that all online with everyone else, and we can't thank you enough.

John Gallaugher

The reason we can do that is because of everybody that contributes in the Python community. And the people that are running really great companies and everybody that's been so supportive. Thank you for providing a platform where we can learn more about each other's work and get more inspired. And this is a really cool idea. So kudos to you and congratulations to you.

Paul

Thanks. So I've been asking all the questions. In addition to CircuitPython, I'm a huge vinyl record collector.

So I like to call this Turn the Tables. So what's your one question that you have for me today? So who are your go-to bands?

Oh, boy. You know, I used to joke that my collection was split into thirds. I had a third of the classic rock, easy-to-find vinyl, right?

Boston, Journey, Queen. Queen's a top five band for me. And then a third of it was 80s pop, which is very hard to find used on vinyl.

Just not as much was made. And then the last third, what I would say is modern indie music from like 2010 on. That's great.

Spoon is probably a top five band for me. So Spoon, Queen, Pearl Jam, just off the top of my head. It changes on a daily basis, to be honest with you.

That's awesome.

John Gallaugher

Oh, wonderful. It's funny, I'm vintage enough myself that the 80s were where I was in high school college. So that's kind of my musical knowledge. And it sort of stops at 1990. It's like, you know, just my life changed and I wasn't listening to radio as much anymore. So I feel like I don't know at all, you know, I'll watch who the musical guesses and set her alive and I have no idea who they are.

Paul

There's been studies done that most people's musical taste stops in the early 20s. And it really doesn't evolve much from there, which I found interesting.

John Gallaugher

Well, I salute your outstanding taste in music. That's really wonderful.

Paul

Thank you. So the question I ask at the end of every show, you're going to start a prototype or a new project with a microcontroller. Which board are you going to reach for first?

John Gallaugher

Oh, probably a feather board, and I like projects that have Wi-Fi. So, you know, if there's a feather board that has Wi-Fi, and if it's remote, something that's got a battery capability built into it. Although, I've got to tell you, the new ESP cutie pies are awesome, so they don't have the battery add-on, but I guess, you know, there are ways that you can do that. You can buy third-party stuff, and Native Fruit's fooling around with some.

Paul

some add-ons too. And I was just looking today, there's a QtPy, I want to say, RP2040 with a STEMMA connector,

John Gallaugher

a STEMMA QT connector as well. It's actually what I'm using on this guy here. I attach this.

So that QD-Py with STEM is awesome. And then there's one that's the same profile that has Wi-Fi on it. Okay.

Like $10, more or less. So that's crazy. So one of the things that I want to do with that actually is, but I'll have to add some kind of battery capability with it, is it has a low-power mode.

And I've not done anything with low-power mode, but I'm notorious for killing plants, so we see that there's a plant that's here, but especially the ones in my office. I'll go away for a week, and then I'll say, ah, they're dead. So I want to build something that I can check in every now and then and that will relentlessly tweet me or send me text messages if it gets thirsty, so I don't forget.

Adafruit did a wonderful thing a couple of years ago with a Bukaru bonsai, where they had this little sensor that was built into it. So you can do really cool internet of things, projects are super, super easy. And that's one of probably, I think every maker's got 20 different things that they're working.

I mean, my lab is just such a mess. If you were to look around, you would see all kinds of weird crap on the floor.

Paul

Well, if you watch this on YouTube, my desk behind me is no different with my workbench with half a dozen projects. Thank you for being on the show today. I really appreciate the time, and it was great learning about the work that you're doing.

John Gallaugher

I'll say to not only to you, Paul, but really to anybody in the community, if you're in Boston, shoot me a note. And if I've got time, I would love to grab a beverage of choice with whomever that's out there. It's interesting.

So I had not known that Dan H, who's on the CircuitPython team, Liz Clark, are both in the Boston area. So we have yet to get together because of COVID. Liz had been so kind and reached out and said, hey, can I do anything for your students?

So we have this wonderful maker space that just moved out of Somerville. It's in Cambridge called Artisan Asylum here in Boston. It's massive.

But there's no reason why we can have a better meetup here in town. I'm going to try to go to, so I'm supposed to go to Italy in between semesters just for vacation and meeting a friend over there. I'm going to try to go to Pycon in Italy.

So if anybody's going to Florence, let me know. I would love to say hi to folks. I have a lot to learn about Python.

Again, it's sort of like I look up half of the stuff I'm using. But, yeah, I want to make friends.

Paul

There are going to reach out in Python in Italy or in Boston. Reach out to Professor Gallaugher. Thanks very much.

John Gallaugher

All right, thank you. Be chatting. All right.

Paul

Thank you for listening to the CircuitPython show, an independent podcast with the people in and around CircuitPython. For show notes, transcripts, and to support the show, visit CircuitPythonshow.com. I'm your host Paul Cutler, and I'll be back next episode. Don't forget to hit subscribe and stay safe. You know,
