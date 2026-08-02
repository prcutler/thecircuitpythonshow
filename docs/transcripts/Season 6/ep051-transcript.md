---
date:
  created: 2025-11-24
title: "Episode 51 - River Wang"
---

## Show Notes

[Show notes available here.](../../episodes/Season 6/ep051.md)

## Transcript

Paul

Welcome to The CircuitPython Show. I'm your host, Paul Cutler. This episode, I welcome River Wang. River was a STEAM teacher before becoming a full-time software developer three years ago. He created the CircuitPython Online IDE, a browser-based platform that allows users to work on a CircuitPython project on the web or as a self-hosted website. River, welcome to the show.

River Wang

Great to be on the show.

Paul

How did you first get started with computers and electronics?

River Wang

So unlike many guests, I didn't have a Commodore 64 when I was a child. So all the journeys started when I go to the college. My major was electric engineering.

So in my freshman year, we had a C++ programming course. That is pretty standard. So it was boring at the beginning, I would say, just as you were variables.

If it was full-loop something like that. that. But there was a homework problem to print out a pyramid in the terminal. So basically do one star in the first rule, two star in the second, and et cetera. And the problem was actually pretty easy, but I suddenly realized that even if I am in a terminal, just plain task, I'm actually doing graphics. And if I can do this periodically with slight change in the between, I can actually graphics, right? And if I can capture user inputs, and this is basically a video game. So I spent a whole night writing 200 light of C++, and I got a snake game working. So I was very, very excited, and that was the first time I found coding is pretty fun. And in terms of electronics, It's very natural because I was in electric engineering department, and what we had was we had a lot of microcontroller competitions.

We have projects, and we do presentations, and we hosted some books for our classmates to come and play with the demos. So basically, kind of make a fair thing. So my first project was an assistive device for people who cannot use regular mouse.

We put gyros and accelerators inside a hat so people can move their neck to move the cursor. And it was based on C-51 microcontrollers back in the days. And the USB part was done by a separate chip called USB D12.

And another device I joined the computation was a competition hosted by a wireless sensor lab. So they provided us a lot of MSP 430 microcontrollers, which are first ultra low power, and second they have agreed computational power that you can do FFTs on board. And they give us these chips and want to know what kind of sensor applications we can do.

But what I made was a game handheld out of it again. I just want to be fun. So instead of doing some classic games like Snake attaches, what I did was I copied many of the popular foam games back in the days, like Flappy Bird, 2048, and Doodle Jump.

And I also did a little bit of research to do Connectify, which was a strategy came up. I'll see. So, yeah, I just want to do.

to be fun. How did you get started with Python? So that was when I went to graduate school.

My research work requires a lot of scientific computation, scientific programming. And school bought us a medical license for scientific programming, and it was very popular in engineering departments. And I actually like it a lot, unpopular opinion. I even use it for my personal projects, such as I did synthesizers, I did test processing, and I think I should use this even after I graduated. So I checked the price for a personal license a year. Well, so high.

So I realized I need to look for some alternatives. So I switched to Python to use non-Py and side-Py.

Paul

You mentioned that you were a STEAM teacher. What were you teaching?

River Wang

In my last few years in the graduate school, I got a part-time job teaching. I got a part-time job teaching the Outreach Program in the Electric Engineering Department. So basically, the Outreach Program is we use university resources such as labs, faculties, to teach some field trips and summer camps to local school districts, like high school, middle school, and sometimes primary school.

So in our Outreach Lab, we got 3D printers, we have soldered stations, and computer installed with Adrenal IDE and AVR studio. So we create courses of different levels. And microcontroller was always my favorite topic because it has a bit circuit, a bit programming, and we usually use the RGB LED in our projects, and we have 3D printers, so we print out 3 cases onto that.

So it's also a very good amount of art in it. So it's a steam project, so better than storm project, I think, maybe.

Paul

How did you discover CircuitPython?

River Wang

So we had a very nice lab setup, and everything worked very well in the beginning, and then suddenly the pandemic hit us. And schools are shut down, and one can come to the lab. And many departments in our university they just shut down their outreach program because of this.

And we tried to survive, and we tried to mimic everything in our lab with the remote learning experience. So some parts are very easy. The lectures can be given by Zoom, and we use Zoom for small group discussions, and we ship the lab case to the students, and three printed models are printed, in the lab and we ship the result to the students.

And for soldering, we pre-s solder the sockets onto the PCB board, and students insert the components into the socket. But one part is actually very hard, is we didn't know how to get the students to write program to the microcontroller. So two sides.

On the hardware side, it's like we used 80 tiny chips to to lower the cost for the students. And those chips themselves are very, well, sub-dollar. And we, in the lab, we use some special device to write a program onto 80 tiny chips.

I think the previous teacher used a debugger or G-Tag or something like that. I use a programmer. And those devices are very special, first, and very expensive.

And we cannot ship these devices to students. And second, on the software side, it's like first students are at home, not in school. So they have all different kinds of computers.

And some use PC, some use Mac. And a majority of the students are actually using Chromebooks and actually locked down by the school districts. So it's very, very hard.

First, because so many platforms, we don't know how to teach them to install the ideas. onto their computers, and second, if they are using Chromebook, it's almost impossible to install anything. And even when it is possible, we just found out the setup process is not very easy.

So at that time, I was looking for solutions that students can program their microcontrollers. First, no special hardware needed, and second, no special software needed. I wasn't very optimistic at the beginning, but actually, I actually found two solutions, and MakeCode was the solution for younger kids, and I found circuit Python for older kids like middle school and high school students.

So it was in the days of CircuitPython 6, I think, and it was advertised as the easiest to set up, the bare minimal setup to do a circuit Python project is you have a USB cable, connect, the microcontroller to the computer, and on the computer, you need nothing but a code editor or just text editor to edit the code file. So that was amazing. That was so mind-blowing to me.

I never imagine such a thing can be possible. So I think this thing can be used in our alterage program online.

Paul

You created the CircuitPython Online IDE. What IDE were you using that led you to create your own?

River Wang

We set a bare minimum setup for a CircuitPython development. It's just a text editor, but the classroom experience can be very much improved if we have a dedicated IDE. And what do we want from it?

So as we said, we want the experience to be consistent across all operating systems. And we don't want to install anything, and we don't actually want to set up any configurations to make a microcontroller work. And what is that?

No installation and CIMA all operating system. And that is a website. So what features do we want from the IDE?

As we said, we need a text editor. Yes, I saw a lot of website that has a tax editor. editor. And I just happened to use a web-based serial console back in this in my own project.

So I know this is also possible in a website. Now, surprisingly, I was not the first person to think about that. So I actually found a lot of projects doing that, but it's like not all of them are very active developed. And almost all of them are missing some.

feature I like. Some of them works, but very, very bare minimum. So what if I want to add some features to that? For example, the best one doesn't have a serial plotter. So if I want a serial plotter, do I back the author to add it? So because I want this so much, why don't I start in my own project? So I call it circuit Python online ID. So around this circuit pattern online, I created three courses.

So the first one was a traffic light simulator. So the PCB board is basically a picture of a crosswork, and we put neopixels onto the PCB to mimic the traffic lights, and students write the program to simulate the pattern. And the second one, we call the sensor interface, which is a handheld device that has a screen and a buzzer.

students using alligator clips to clip sensors onto the device. And the students write programs to show the readings on the screen, and they use the buzzer for alarming. And this can be combined with a lot of science class, like they can be used in some physics experiments, so scientists' teachers like it.

The third course I created was a RGB nightlight. it is basically a trinket M0 with a photoresistor, and we really print a case onto that, so it measures the ambient light and show color patterns in the dark. So in my days, I taught the classes via Zoom calls, so everything was remote.

It worked out very well. And then I left the program. My fellow teacher actually went to the schools, And because the schools resume, but the university lab was still closed.

So she basically went to the school classrooms and teach there. It's just a regular classroom, regular classroom, but we can use the IDE, just need regular classrooms. So they simplify the setup a lot.

They don't need a dedicated lab to teach these classes.

Paul

Tell me more about the Circuit Python Online IDE. How does it work?

River Wang

The most basic part is a text editor and a serial console. So the text editor relies on a browser feature called File System API. So basically, your website can open a local folder inside your computer and edit the file in it.

And the serial console relies on a Chrome-specific feature called the WebSerial API. So that allows your website to directly talk to a serial port. These are the two foundation technology inside the CircuitPython Online IDE, and all the features are built based upon these two features, such as the plotter is based on the serial connection, and the library management is based on the file system API.

So when you use the IDE, you can go to the VALTHA, website, the circuit pi.dev. And then you first connect your microcontroller to the computer by a USB cable and inside the website. And you can open CircuitPy Drive as a folder with one button and connect your serial port with another button. And you're all set to work on your project.

Paul

What kind of challenges did you face in developing the online IDE?

River Wang

Yeah. So actually, when I started this project, I had no experience on web development at all. So basically I asked my CS major friend, and it's like, well, do you have any resource, like do you have any class material on web development?

He just dig out one homework folder and send that to me, and I started everything from there. And it was a very, very bare minimum HTML page with no aesthetic refinement. But it just worked.

There was a text editor. There was serial communication. And now I call it version zero.

And I then start to add some features to this version zero, like some short cost that I like. And I also added the plotter into that. And after I add the zero plot.

Everything is just so messed up because that was my first JavaScript project. And when I tried to add folder view and editor tabs, I just had to start over and create a new project for it. And that one was still in pure JavaScript.

And that one was called version 1. So when I was teaching online, I was using version 0, and my fellow teacher, when she was teaching the high school classrooms, she was using version one. And when I just try to fix some bets in the folder view, I found this code is too messy again.

And when people see if you are not using a front-end framework, you're basically writing your own framework. So definitely my framework was not very well. So I adopted the most popular one was React at the moment.

So I basically refect everything and rewrite the online ID again in React. And because, well, that was still my first React project. And the first trial was still very, very messed up.

That was version 2 beta until. And when I tried to release the version 2 official without the beta, that was refactor again. So I major refactoring all the time.

What was the biggest challenge is that everything was developed while learning. But I also proved that if one wants to make some contribution, doesn't have to be an expert. So you can start from zero experience.

Paul

One of the things I like about the CircuitPython Online IDE that you've created is that you can host your own version, which can probably help in a lockdown IT environment like a school. Yeah. How hard is it to self-host?

River Wang

Actually, it's not very hard. So the centerpiece of the IDE are both front-end tech knowledge. The file system API and Web Zero are just browser features.

So for years, actually, the online IDE had been a pure front-end project. So it was hosted just by GitHub page. And if you want to host your own version, you can also create your own GitHub repo and just create a GitHub page from the repo.

And in my repo, there is a release section. So actually, you can go to the release section and download the latest to release as a pure HTML page. And it can run actually locally, or you can host it online.

And this is changed recently a little bit because I added library management feature, and that one will need a backend. So the service is hosted on Google, but the front end still lives in GitHub page.

Paul

You mentioned in the repository description that the IDE is designed for education and hobbyists. How does it help educators?

River Wang

Because the idea was created inside the classroom, it was created to solve classroom problems. And this has never changed this. I always have education in the first place.

So some design principles kept from the beginning. So if you open the website, Sikopi.comi.d, it will show what the students need to finish their first class project. and nothing more and nothing less.

So all the advanced features are hidden in the manuals and shortcuts. And I also try to reduce confusion in the UI as much as possible, such as I don't often use icons. Everything is just written out as plain text.

Because I use the idea myself, if that is useful to me, it can also be useful to others. So, well, I think everyone working on a DIY project can be benefited from this. And I also remember many of my students who expressed their interesting microcontoures even after the course.

So I also want to support these students and continue to work on their projects even after the camps or the field trips.

Paul

You've mentioned some of the features of the IDE. can you share some of the useful ones?

River Wang

So in the ID, in the manual bar, there is a button called Tools. Click on that, it will show you some useful features. And Serial Plotter is going to be the most used feature.

And you can plot, zoom, truncating time, and add legends to it, and also use one of the column as X-axis. So this is a very powerful plotting tool. The plotter is actually compatible with MOO editor.

So if you have a plot code that is already working with Mu, it should also work here. And another feature I recently added to it is library management. So if you use the circup before or heard about it, it's basically similar, but with SCOWI.

So there are two ways you can use it. So first, if you use the auto installation, it will analyze your own. CircuitPython code and install all the libraries needed and also with dependencies.

And that is from the EDAFR bundle and the committed bundle. So there is also a list of all libraries from both of a bundle. You can search libraries from this list and install, uninstall or upgrade on demand.

And also there is a button in the UI that links to the library report so that you can read more documents and source code or example. And the third feature that I want to share is the camera feature, the camera tool. This one has nothing to do with the microcontroller itself, but whenever I want to show people something, I just found myself need to open a separated app for camera.

Because microcontroller projects are not just the code, you want to photo your dev board, Bradborough. And that's why you need a camera. So in the camera tool, you can point your webcam to the microcontroller and view it just inside IDE. And you can flip, rotate, zoom, everything you want to do. This can be very helpful for teachers. And you can show whatever is on your desk on the large projector in the classroom. And also, if you can be very helpful, If you're hobbyists that want to stream or record your project, this can be also very helpful.

Paul

That's pretty cool. What's next for the CircuitPython online IDE?

River Wang

Yeah. So if you go to the repo and go to the issues section, there are a lot of feature plans and enhancements plan. So there are two features I am actively working on at the moment.

One is called connected variables. So if you want to talk to a running program, usually we just use a serial console. But text flow is not the most intuitive.

Even if you can use the plotter, sometimes it's still not the best way to show what is going on in the program. So I want to provide a bunch of wedges that can directly talk into variables inside the program. such as buttons, selections, meters, and color pickers, etc. So that you can talk to a running program both ways.

Another feature is a debugger. So as far as I know, Micropycin and CircuitPython doesn't have PDB, which is the default Python debugger. So I am working on some kind of workaround solutions to provide step-by-step debugging, breakpoints, and expression wash.

Yeah, so that's it. How can people support your project? If you want to support a project, just please use it as much as possible and share it with others, share it with other teachers specifically, and give me some feedbacks and tell me how you are using the IDE, what is the story?

or if you have bug reports, feature requests, please let me know.

Paul

So if anyone wants to learn more about it, where should they go?

River Wang

I have a YouTube channel called Circuit Pythonic, and I also post on Twitter and Fosstodon. I really post IDE updates and my personal microcontrol projects.

Paul

I'll make sure I link to those in the show notes as well. Last question I ask each guest. You're starting a new project or prototype. Which board do you reach for?

River Wang

So I don't have a specific chip set to go to, but I do have a go-to phone factor, which is the Cidoreno shell or Aet4 QDPI. One of the reason is I still don't know how to do reflow. So usually I just sort of the whole data board onto the PCV.

So the smaller the deadboard is the better. And another reason is I have a very, very long commute every day. So I often work on my personal projects on the train, so I wish the databoard can be as small as possible.

At this moment, my setup is a Cidurino show since 52840, and I use a mill-to-mill adapter, not a cable, just adapter to plug into my laptop, just like a USB dungo. But, you know, what can be better? A type C train key, which doesn't exist yet.

I will surely carry one with me all the time. So, Idafruth, if you are listening to this, please make it happen.

Paul

River, thanks so much for coming on the show. Thank you. It's great to be on the show.

Thank you for listening to The CircuitPython Show. The show notes have links to the CircuitPython Online IDE available at circuitpy.dev, and I encourage you to try it out. For show notes and transcripts, visit www.com.

And if you're enjoying the show, consider something. sponsoring the show to help offset the cost of podcast hosting, recording, and more. Visit the sponsors page at circuit python show.com to learn more. Thank you for your support, and until next time, stay positive.
