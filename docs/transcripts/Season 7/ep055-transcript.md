---
date:
  created: 2026-03-09
title: "Episode 55 - The Open Pressure Sensor Device"
---

Paul

Welcome to the Circuit Python Show. I'm your host, Paul Cutler. This episode, I'm joined by Michelle Hui and Reitwiec Shandilya. Michelle is a master's student at Cornell Tech and AI and Urban Technology. Her practice includes accessible technology for good across health and climate. Previously, she has worked at Wing, Google's drone delivery moonshot, and the United Nations. Reitwiec is a master's student at Cornell Tech and a fellow at 645 Ventures, where he focuses on early stage investments in AI infrastructure, security, and hardware. Previously, he was an early member of SAP's AI team working on Enterprise AI Solutions. Michelle and Reitwiec, welcome to the show.

Michele

Thank you for having us, so excited to be on.

Reitweic

Yeah, it's great to be here Paul.

Paul

You've worked together to develop the open pressure sensor device or open PSD. What is the open PSD?

Michele

So the open PSD, we began working with Weill Cornell - New York Presbyterian. But after, you know, female patients have cancer, specific breast cancer and they get mastectomy, it leads to a serious loss of quality of life because they often say that their chest feels like it doesn't belong to themselves anymore. When they hug their children, they can't feel their children. So there's a surgeon at Wilde doing super cutting edge research where he essentially can reconnect your nerves and help you regain sensation in your chest. But they had been using this proprietary medical device. And the private company decided that it was no longer profitable anymore and they essentially abandoned device. And not just this surgeon, but essentially all the research labs across the U.S. doing any sort of nerve sensation, whether that's diabetes and you do sensation in your foot or your fingers, essentially lost access to this one device. So what we did was we actually engineered that from Blackbox and we rebuilt this pressure sensor device, hence the name, open PSD, open pressure sensor device.

Reitweic

Well, yeah, I go with this was essentially to quantify sensation. and their function and help expand it to other clinical and neuroticetics as Michelle's

Paul

what were some of the problem gaps that you were trying to resolve in addition to that

Michele

I think beyond just this proprietary medical device before that they literally used to use one monofilament and you would just use a filament to poke at various areas of your skin so it's the super outdated archaic method and so our open source device isn't just replacing a abandonment medical device, but it's actually innovating on this super archaic nerve sensation method. And on top of that, we're also working with OSHWA, the Open Source Hardware Association, to explore, you know, what happens to any medical device, when expensive med tech decides that it's just not profitable in pain anymore, how can we democratize healthcare medical devices, how can we make a framework for open source, but also reliable? And so those were the two, I think, larger impacts that we're trying to address with the project.

Paul

How did you collaborate with clinicians during the design process?

Michele

Something that we discovered when we saw the proprietary device was that had been completely over-engineered. It had been super expensive. They came with this giant briefcase, you know, almost Matrix-style supervillain-style briefcase. And they pulled out like a proprietary tablet, almost their own iPad, and it had their software installed, And then they had this giant acquisition unit. And then they had this, like, this super boxy handheld device. And we just felt like it had been so over-engineered. And we could tell that they're probably trying to upsell it, you know, have software maintenance. And so we came in and we asked them even on the first day, like, if you could get rid of all of this, what would you want to get rid of, right? And we were able to change that, all of that giant briefcase into literally the size of a screwdriver. And that's all you needed. It was a screwdriver. And it was, you know, software that you could install in your own Mac. And so we work in the clinicians. Every single couple weeks, they would come back and give us feedback. I remember one time the surgeon came in and he felt our device and he's like, oh, your wires that are doing the sentencing need to adjust because it's actually hitting other areas in the skin. And it was just something we had totally, you know, not thought about and we didn't understand how they were using it at all. And so I think what we're able to do in open source and what we discovered is that because open source isn't meant to make money, you don't have to try to. start upselling everyone and you don't have to create this black box med tech industry, we can actually go back and forth with the clinicians and really improve and do exactly participatory design and create a participatory framework to improve like clinician efficiency and just improve the workflow overall.

Reitweic

And something really exciting here was that, I mean, I don't know, we had really thought about before was the initial device that they came up with was, I mean, it looked really daunting as well. I think as a patient, you're really in a very vulnerable state when you're going through this entire process. Imagine someone coming in with a huge briefcase and takes out this huge gigantic device. It's really, really unnerving sometimes. And so our whole goal there as well was we want to make patients safe, you know, we want to trust that device. And I think since since it has gone to the clinic, we're still waiting for for the PI's feedback, but we're looking forward to them.

Paul

You mentioned that you got it down to the size of a screw. Tell me a little bit more about the hardware, and then tell me what role Circuit Python played in the development of the firmware.

Reitweic

CircuitPython was our firmware, and the idea, the way it was we had a load cell, and we have filaments attached to it, and we had sort of custom-wired and custom-twisted this filament at the end of the load-cell. And this load cell then had a sensor, a pressure sensor, which is attached to the load cell, which then goes to our firmware where we processed these signals, and we had some custom logic. Just for getting, let's say, set a ton of values, taking an average out of it. And whenever someone presses the button, it calculates a set pressure that's being applied to the load cell. And from there, we display on a UI that we had created, which is running locally as well, because we want to keep it on cloud, but it was personal patient data. as well. But yeah, that's how the overall device was set up in the hardware.

Paul

What kind of screen was the UI displayed upon?

Reitweic

It was just a laptop. It was also, I mean, we just coded up and React. And I think, so the other goal that we want to see with this project was how quickly can we actually get feedback? And surprisingly, AI did a pretty good role there, and it helped accelerate quite a bit of her stuff. Since going into it, I did not know a lot about, let's say, how load cells work or just the tech behind it. Because when we were reverse engineering stuff, we came across the small parts, which we hadn't really seen before. So I think doing the initial research and getting some other information and then helping with some initial setup, because our main rule was to focus more on the device itself. And the secondary things that came up with it were, let's say, the UI or whatever else. and so we want to completely focus on the hardware and AI help in finishing up the secondary task here really quickly and we were able to write it really quickly we got the PI to the lab and we were just helping him go through the the interface and then we got some feedback here that this can be here this can be done this that was pretty exciting yeah

Paul

sort of the AI help with writing the actual circuit Python code that you used on the device

Reitweic

it was a mix honestly um so initially it was just going to all the different documentation that we could find online for. So let's say our sensorware at S-H-X-7-11. So figuring out information for that. So the initial boilerplate core was provided by AI. That was pretty helpful. And then just fixing it by bed by bit, piece by piece was more of our own experience and just our own software experience.

Paul

You mentioned a couple minutes ago that you had to reverse engineer the proprietary device, how did that process go?

Reitweic

That was interesting. So we had, the device, it was like this, imagine a square Mac mini style, but small Mac mini style device. And so it was just a lot of unscrewing stuff, taking it all apart. And then when we opened it, there were these small, small cables inside and these small, tiny load cells. And we were like, okay, that seems interesting. Then the next part was, we had a balance between buying stuff. that's already out there and making users that and making our own custom things. Because the whole point of open source was that if we're going to build something from that, we want it to be accessible. For example, let's say if we were to go ahead and build our own load cell, then for someone to build it and replicate it, it's going to be really hard. So we decide we go on a YouTube, we find a relevant load cell, and then we'll design it on that. So that was another key thing that we had to keep in mind. Then, well, as you were exploring, we're trying to see what materials were used because the filament that's used to poke on the skin needs to be flexible. enough, but it also needs to be rigid. So we tried experimenting with different materials and then eventually, I think we resulted with an aluminum kind of thing.

Michele

Yeah, to add on to that, I think one of the challenges, the overarching challenges to everything we would describe was we didn't know what was good enough, especially because it was medical quality, right? I think if it was another open source device for tinkering or a watch, I think you can get away with a lot of loose. or things and can get away with different parts. But we were always like, is this good enough? Is this accurate enough for medical application? And the Mac mini device that came to us, as Roque mentioned, like we had started hacking it apart because we didn't know how it worked. Like we literally took a saw and cut out pieces of the aluminum and then we like pulled off the prongs and we started using it ourselves. But it was broken. So we truly had no idea how it was measuring and how accurate it was. And so when we were building our stuff, we almost hit a two-month delay or like stock point because we were just not only sure where to proceed. We were like, we don't want to build our own custom load cell. You know, we want to use what's off the shelf, but we don't know if this load cell is good enough. For example, our load cell, I think, in a range of up to, I think, 10K, 1KG or 10KG, if I'm not mistaken, but we only needed a 10th of that. We literally only needed 1 to 100 grams of measurement force. And so we're like, if we're only using such a minimal part of its range, is there too much noise? Are we able to detect it? And so we truly had no clue how to reference it. And then another issue we face with reverse engineering from Blackbox, we thought the whole time that it was measured in this measurement called like grams force over area to get pressure, if that makes sense. So, you know, the tip of the wire is like a diameter of like one millimeter. And so we're like, oh, we have to calculate the pressure and then calculate. like the force and divided by that area to get pressure or whatever. And so we're going through this complicated, convoluted conversion. And then the clinician comes back and he pulls out the real functioning device and realized they didn't do any of that. We realized they were literally just converting directly to force and just doing it and just reading out that measurement. And we actually felt totally lied to because all the papers had said that it was over area. And I was like, wow, no one actually even knows how this device is working. And they just had some arbitrary readout. And we found out that our device was almost just as accurate, if not more accurate, than their current device and was able to read forces better. It was able to read closer to zero as well. And so I think that was one of the big challenges we faced was just validating against medical accuracy and having medical standards. And this is important because, you know, as we're trying to build a framework for all of the open source devices out there, especially medical devices, I think this is a challenge everyone will face. How can we validate with the scrappiness of open source but also make it reliable in protection grade for the medical industry.

Reitweic

Yeah. And I think like something else that was while we were going through this process, we, and as we did this, as they called, contextual inquiry, we were looking at the PI, do we use the device proper on his own. And then I think there was a part where you had to ask important questions like when it comes to to accuracy, right? Something that we realized was, because the device is measuring the sensation over a period of time, we wanted to know what our tolerance was for accuracy. Because at the end of the day, fundamentally we're seeing whether the sensation is improving. So even if, let's say, they were, let's say, a small, I mean, a one person, two person error, it would have been sort of acceptable because in this particular situation, the main fundamental use for the device is to see, like, an overall growth over time. So I think the important part was asking important questions like, hey, what's the real use for it? That's because it needs to be done this way doesn't really mean that it has to be done that way. So I think when it comes to open source medical hardware, it's important to understand what your tolerances are, acceptance is are. And the second part was these guys are really busy. So we had to really plan one of our first calls with the surgeon was he literally stepped out of the OR just to talk to us for like five minutes. And it was, it was, it was so I think the second point was, we'd have to plan it out properly, and it was interesting.

Paul

So you've been talking a lot about open source. Will you be certifying the open PSD with the Open Source Hardware Association?

Reitweic

So we did talk to our point of contact with OSHWA. And he did say that I think OSHWA would be really, really happy to have his certify. They would also want to do some sort of blog about us and, you know, just, sort of help us reach out to as many people as possible. Because the whole point of the NSF grant that was given to OSHWA was to promote such devices. So, I mean, they said that we're really excited and really happy to collaborate and certify this.

Michele

Yeah, I think I remember before we started this project, actually, we had done an interview with a couple people from OSHWA. And it was essentially us giving feedback on what we think should be a more certifiable framework on what open-sourced hardware or medical devices look like. And it was this ongoing debate because, you know, as we're saying, I think medical devices need more reliability and validation. But you can only get that validation once you've completed the device, right? But then part of the ethos of open source is, hey, maybe you get 75% there, you put it online, and then someone else takes it forward. And so we were having this giant debate as to is validation one of the things that require in order to be certified? You know, like how does that kind of start veering into, you know, like a research paper publication style, is that too high of a barrier to entry to get people to do a medical device? And so we're just having this giant debate into what a proper framework for an open source medical device looks like. So, you know, open to end in a question for the audience to think about, for everyone to think about, what do you really need to certify a reliable open source medical device?

Paul

Yeah, for medical, you would want some kind of. a validation because if you're putting out the design out there and someone builds it and it doesn't do what it's supposed to do, even though it's an open source license and it could be built,

Michele

they're still not getting what they expect. Exactly. And we, I think, had some other problems too. We are saying when we're building this wire prong, originally we were thinking of creating this giant wire bending jig when we're going to screw some things in and then it would wire automatically with a feed machine. But then we were thinking and we're like, well, how many people we're going to have this complex wire bending jig that the resources of Cornell do. And so we ended up just buying jewelry pliers on Amazon. And we're like, okay, well, just hand wire it, hand bend it. But then in that process, we're like, how can we communicate across the screen that this is exactly the dimensions that they need to do it at? And so I literally ended up tracing the shape of the wire on a piece of paper and then putting like a quarter next to it, took a photo. And I was like, okay, everyone, print this out, you know, zoom into your photo to size. and this is how you're going to bend your wire. And so it was trying to assess the accuracy, but also balance the scrappiness of what open source is.

Reitweic

Key part here is the way we convinced the surgeons and the doctors to come work with us because we wanted to keep them, I mean, place them on the driving seat and draw the device around their use. I think that was really important. A lot of times medical equipment that would be designed are really far apart from what the actual use case. sometimes. I mean, that's something interesting. Yeah, we can focus on it.

Paul

Michelle, any thoughts as we wrap up?

Michele

There were other things that we also had to do, including the 3-D printing, the form factor prototyping as well. I think one thing kind of, I think, elaborating into that tension of scrappiness versus medical grade hardware, you know, we were literally just building in the maker lab. Like, we're quite literally, you know, just scrapping it up in the maker lab. And so all of our prototypes for the physical, like the hand-held portion and casing the hardware. It was all 3D-printed. And honestly, it had like a lot of bumps and I tried to sand it out. But it just kept making it worse and worse because the dust is getting everywhere and into the crevices. And so highlighting that tension, again, we're like, how will a patient feel if their doctor's holding a little 3D-printed screwdriver toy? And then we're like, how will this hold up over the years? And that was one of the issues and the tensions we had faced as well. So I think as a clinician right now is using it, we're excited to get feedback. And perhaps we'll have more resourcing to cast it better or, you know, wrap it up in silicone. But I think our first version was definitely perhaps not built to last, to say the least. And I think adding on to that tension as well, me and Rick are both in grad school and this is our final year here. And so we are wondering about the open source maintenance of a medical device as well. And we were wondering, like who will carry this forward. You know, the clinician and, you know, they're not necessarily the most technical people in terms of being able to install the software, the software breaks. And so one of the kind of lasting questions in the back of our head is how is this going to go forward? And that was originally one of the issues, the original proprietary medical device, was that they're being charged every single year, essentially, to have some sort of maintenance certification. But we realized the certification didn't actually do anything. Like the device is so simple of load cell and the calibration, all you have to do in order to calibrate it is hang away on it. And that will be your reference point. And once you reference point it, it'll just reset the calibration. It was so simple. I was like, no one needs to be charged for this. This device is none we sent in to maintain every single year. But in the back of my mind is what are we going to do? How are we going to communicate the disclination? How are we going to validate that there has been no measurement drift across time? And so that has been one of our longstanding questions of open source as well, especially in the medical use case.

Paul

Yeah, that's a great question. I know I don't have any answers off the top of my head for that.

Reitweic

At least talking about the wear and tech, one good thing about open sourcing this is even if it wears down, you can just reprint it. That's like the part about this. Like the main core part still stays. They can just reprint the whole outer casing if they want to with different colors. Honestly, if they want to use it on different age groups of patients, they can make it if they want to do it. So there's this endless possibilities in terms of making the device look approachable and safe.

Paul

What's next for you with the device?

Michele

I think what's next right now is, as we mentioned, because it's a medical device, we really invested into making really extensive documentation. As I mentioned, even drawing out how the wire should be bent. For example, we had to drill a hole into our load cell. And I was like, how do I map out and communicate to someone where to drill this hole and like how deep the hole should be and all of these things? And so we really invested a lot of energy into making extensive documentation. So we're hoping to get like a V1, V2 out soon. Other things that are next is obviously iterating clinician feedback. Other things is also building that framework out with OSHWA. So scaling the impact. And we're also interested in perhaps some sort of publishing commentary that we're working on. to I guess propose this new framework as we're saying of how open source has enabled participatory med tech development. In contrast to what industry proprietary black box looks like, it's you build the device and you put it and you sell it to hospitals that are super expensive. I'm highly dubious that there's any sort of clinician iteration loop that's happening there. And so we really wanted to publish on what a new framework could look like.

Reitweic

Yeah, and we're also waiting to hear back in the BI. because I think he was planning on using this as part of his research as well as he uses it on patients. So we're looking forward to his findings and his results and how that goes. Yeah, super exciting.

Paul

That is exciting. Reitwiec and Michelle, thanks so much for coming on the show.

Michele

Yeah, thank you so much for having us. That was a really fun chatting about all this.

Paul

Thank you for listening to the Circuit Python Show. For show notes and transcript, visit www. www.circuitpythonshow.com. Until next time, stay positive.
