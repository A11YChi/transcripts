# Real-world Techniques for Accessible Design
## Joe Welinske - Wednesday, August 2, 2017
[Source recording](https://www.youtube.com/watch?v=HslE_I_yRNo)

**[Dennis]:** Up now for tonight's presenter ... Joe, you're up!

Joe is a UX professional out of Seattle. He works for UX Blink ... Blink UX ... I figured I'd get that wrong. He's also the organizer or assistant organizer ...

**[Joe]:** Co-Organizer

**[Dennis]:** He's the co-organizer of the Seattle Accessibility Meetup. I actually watched a session the other day ... a fantastic, very engaging crowd that they get there. So please ... give a warm Chicago welcome, to Joe Welinske.

[Applause]

**[Joe]:** Well, thank you very much for having me here. I'm really happy to be here with your group and I'm from the Seattle area and one of the areas that I'm involved in is accessibility design. And as I am one of the co-organizers, we have a accessibility group like this one and we have monthly meetings and so I'm happy to be involved in that and regular basis because it's something that I do as part of my activities being a consultant with a user experience research and design firm in Seattle called blink UX. I also teach at the University of Washington and that includes class on accessible design principles and so this is an area that I'm really interested in and first got exposed to through the W3C, working as part of a working group for the Web Accessibility Initiative some seventeen years ago, and still, still involved.

Before we get started, I did want to mention that I'll make sure that my email address is posted on the meetup site. Because one of my graduate students has put together an accessible version of this presentation in a Word document format, so it's in a linear format with images and essentially the script or the things that I talked about. And so anybody that's interested in that, please send me a note and I'll be happy to send that to you and you'll have the whole presentation in that manner and you can deliver that to your colleagues as well. And by the way, I grew up here. So one of the reasons I come to Chicago on a regular basis is I have family in this area, going to "Lolla" tomorrow and checking that out, so. In fact, I worked in this building in 1988 for what was Quaker Oats. I don't know if they're still over there. But they're right across the street, so. It was a lot different, the offices weren't as comfortable and trendy and nice as this one, but it's a great place to work, looks like. 

Alright, well, so the point of all this is to provide information about a case study, just one of many case studies related to accessible design that Blink UX is done with one of its clients and I already know from talking to people here that we have some people that are very experienced in this area. Hopefully I'll be we'll provide some nuggets that you aren't ... you are already familiar with. And then for people that are newer to accessibility, just kind of talk about, sort of a day in the life a typical project that we might encounter for one of our clients. And in this case, our client was VeriCite and we're involved in helping with the design, redesign of their website and their service and their software is used by universities, by educators to be able to check the originality of submitted papers, documents, text and that type of thing. In fact, at the University of Washington, it's tied into the learning system that we use there. And so, you can, students post papers and it can be instantly evaluated to find out different levels of originality associated with that. And so, being a software that's used widely in universities, that obviously, there are certain accessible design requirements associated with that. Fact, one of my colleagues at the University of Washington Tacoma is an educator who's blind. And so it essentially, the software wouldn't be available to him without having accessible design associated with it. But I did ... one of the things that I wanted to mention is a lot of the things that we talked about, or that we do at our organization, we can't talk about because it seems like everything's under NDA. And so, yay for VeriCite. And they've said, let's talk about it. We knew it was a good experience and so these are you know just kind of under the hood things that happened with this client project. And I'll just go over it in three areas; process findings and reporting. And then we can open it up for questions. I have the microphone here we can pass that around. And then I can also stick around until you know we get kicked out for anybody that wants to, you know talk about things, get in the weeds about any of the these issues, as well.

So process is the the first area and so in doing an accessible review for this product,

0:06:52.060,0:06:58.680
first thing that we always have to figure out is, you know, what level compliance is appropriate.

0:06:59.880,0:07:05.940
And even though this was software that was being used at the university level,

0:07:06.140,0:07:12.260
contractually, there weren't set compliance standards for that.

0:07:12.500,0:07:16.740
It wasn't strictly ... it wasn't a federal government contract and so

0:07:17.160,0:07:21.460
the Section 508 didn't specifically apply to that.

0:07:21.460,0:07:28.480
So one of the things was to identify what level compliance we're going to be reviewing the software for

0:07:28.480,0:07:31.520
is part of our accessibility review.

0:07:31.780,0:07:35.760
And by the way, she mentioned, the product had already been designed,

0:07:35.760,0:07:39.020
and so anybody here that's a designer knows

0:07:39.020,0:07:44.820
we always like to be involved with these types of things as the project moves forward.

0:07:44.980,0:07:49.360
In fact that's where we get our best accessibility solutions

0:07:49.360,0:07:53.880
when it's ... if you know it's a universal opportunity throughout

0:07:54.120,0:07:59.420
But here, we were coming in when the product was already mostly put together,

0:07:59.420,0:08:02.860
and so we're checking to make sure it was working well.

0:08:04.140,0:08:16.880
Since there wasn't a contractual level for this, we went with the W3C's double A level of recommendations

0:08:16.880,0:08:23.960
through the Web Content Authoring Guidelines.

0:08:24.320,0:08:29.220
And that's a standard that we've used in many projects.

0:08:29.220,0:08:35.620
It aligns very closely with where Section 508 came from originally.

0:08:35.840,0:08:43.060
It also aligns closely with the regulations that are established and in the European Union

0:08:43.060,0:08:44.480
and other parts in the world.

0:08:44.480,0:08:47.620
And so we felt that that was appropriate,

0:08:47.620,0:08:59.020
and we always do document all of our ideas, our thoughts, our reasons, throughout the process.

0:08:59.360,0:09:05.780
Because that helps us to be able to understand why we did what we did,

0:09:05.780,0:09:12.540
and if questions come up later, to understand why we did things at a certain level of compliance.

0:09:14.960,0:09:22.440
Now this client, it had not gone through a formal accessibility review before,

0:09:22.720,0:09:28.220
and there's certainly a lot of different tools, commercial, non-commercial,

0:09:28.220,0:09:32.940
that can be used in order to be able to do evaluations.

0:09:33.320,0:09:36.020
But one of the things that we wanted to be able to do was,

0:09:36.440,0:09:44.320
have tools that the client would be able to work with later on after the project.

0:09:44.760,0:09:50.920
And so, one of the things that we used is a tool that anyone can use,

0:09:51.660,0:09:58.300
which is publicly available from WebAIM.org which is Wave.

0:09:58.300,0:10:05.020
Which provides ... sort of a top level overview of software

0:10:05.840,0:10:10.940
and matches that up to the guidelines established by the

0:10:10.940,0:10:14.720
World Wide Web Consortium's Web Accessibility Initiative.

0:10:15.200,0:10:18.100
And it's fairly easy to work with.

0:10:18.340,0:10:22.460
We work with other tools as well that are a little bit more powerful than that,

0:10:22.620,0:10:26.860
but I bring this one up because a lot of people that are just getting involved in this,

0:10:26.860,0:10:33.180
I find it's a good starting point, because anybody can get Wave for free

0:10:33.180,0:10:38.000
and you can check out any webpage that's on the public facing web

0:10:38.260,0:10:47.320
and be able to get an idea of what it means to to see what complies and what doesn't comply

0:10:47.320,0:10:50.000
with different levels of the W3C.

0:10:50.000,0:10:56.360
And so, on a typical Wave screen,

0:10:56.640,0:11:00.540
it'll provide a representation of a particular webpage

0:11:00.920,0:11:08.180
and then that web page will also have icons associated with different parts to it,

0:11:09.300,0:11:18.580
and represent issues that it's found related to those W3C Web Accessibility Guidelines.

0:11:19.540,0:11:23.820
And each of the individual icons is then something that you can use

0:11:23.820,0:11:27.640
to delve deeper to find out particular problem.

0:11:29.460,0:11:38.160
Now, in doing this accessibility review, one of the things that I that I always do is keyboard only testing

0:11:38.840,0:11:44.340
and to me, that's extremely important and fortunately,

0:11:44.720,0:11:53.380
like I'm old enough where actually I did work with software where you had to use a computer.

0:11:53.380,0:11:59.180
I realize that a large portion of the audience has no idea what that's really about.

0:11:59.460,0:12:06.340
But I ... keyboard access is more than just the keyboard,

0:12:06.340,0:12:15.460
because keyboard access also is closely tied to the ability for other assistive devices

0:12:15.780,0:12:23.140
to be able to understand what's going on with the software and to be able to communicate that

0:12:23.460,0:12:26.260
to users through different assistive devices.

0:12:26.660,0:12:31.460
and that may be something that's very different from a physical keyboard

0:12:31.460,0:12:36.560
and so, it does take a little bit of work to to get used to that,

0:12:36.940,0:12:45.860
just navigating through a system using only navigation keys, using control key combinations,

0:12:45.860,0:12:48.340
which isn't something that we do very often,

0:12:48.600,0:12:54.280
and completely eliminating your use of a pointing device.

0:12:54.600,0:13:00.320
And one of the things that you find as you do keyboard only access

0:13:00.320,0:13:07.480
and you identify issues where you're not able to control all the features of the software is that

0:13:07.760,0:13:13.160
very often it comes down to some aspect of the coding,

0:13:13.160,0:13:20.960
where it wasn't put together in well-formed HTML, CSS and so on.

0:13:20.980,0:13:26.620
So organizations that I have very tight libraries that have been vetted,

0:13:27.260,0:13:31.840
I tend to not have a lot of keyboard control issues,

0:13:31.840,0:13:40.200
but I'll show a couple ... as we go through where it wasn't just a coding issue.

0:13:40.620,0:13:44.820
By the way, I associated with the slides

0:13:44.820,0:13:49.160
and in the support document, the accessible support document I have,

0:13:49.480,0:14:00.840
I include information about the associated guideline, as you see, as is numbered in the document

0:14:00.840,0:14:02.120
and in the slides.

0:14:02.860,0:14:15.900
In this case 2.1.1 Keyboard Level A, which is a foundation aspect of the W3C recommendations,

0:14:16.180,0:14:24.560
so we felt that everything ... we demanded that everything had to be at the double A level,

0:14:24.560,0:14:28.900
which means it's certainly to pass the A levels.

0:14:29.680,0:14:33.600
Also screenreader testing and ...

0:14:34.040,0:14:40.480
I have a colleague who uses a screen reader on a regular basis with his laptop who's blind

0:14:40.480,0:14:53.760
and there's no way that I'm able to use the screen reader to the robust level that my friend Taylor can.

0:14:54.280,0:15:01.100
But I have taken the time to learn how to use a screen reader

0:15:01.560,0:15:07.840
and so I do reviews of software only using the screen reader.

0:15:08.120,0:15:16.060
And so being a sighted person, I'll put something over the screen

0:15:16.300,0:15:23.180
and attempt to work with the software only working with the screen reader.

0:15:23.760,0:15:32.220
And that's a skill that, I think people it just start using with a screen reader,

0:15:32.220,0:15:40.600
whether it's NVDA or JAWS or Voiceover with the iPhone, it can seem a little challenging,

0:15:40.600,0:15:49.380
But it pays off so much to be able to get that extra bit of understanding and clarity

0:15:49.380,0:15:52.860
about where there may be gaps in the system.

0:15:52.860,0:15:59.720
And by the way, I want to mention that there's no substitute for

0:15:59.920,0:16:08.300
also having as part of your team, people with various challenges that are then going to vet the findings,

0:16:08.540,0:16:14.280
and do testing in a real-world capacity.

0:16:14.280,0:16:16.000
And that's something that Blink does do.

0:16:16.300,0:16:25.700
So usability testing is a big part of Blink's work and fortunately Blink also happens to run a recruiting agency.

0:16:25.700,0:16:32.000
And so we have the opportunity to find people that can do that kind of testing for us.

0:16:34.620,0:16:39.180
Now, to make sure that I'm able to work through a review

0:16:39.460,0:16:45.680
in an organized manner for the keyboard-only testing and working with the screen reader,

0:16:45.680,0:16:57.460
I'll put together a script for myself, that has all of the key use case scenarios that we want to be able to test for.

0:16:58.020,0:17:04.580
And so, then, that's what I'll do. I'll go through that using the screen reader and keyboard access

0:17:04.580,0:17:09.980
and try to identify various issues with the software.

0:17:12.300,0:17:16.840
If you have existing documentation for your product or service,

0:17:16.840,0:17:20.200
that helps a lot, because you can just work with that.

0:17:20.600,0:17:24.220
And that will come into the process, in the reporting, a little bit later.

0:17:24.800,0:17:27.020
So now, I'm going to jump into the findings

0:17:27.300,0:17:35.440
and I won't be able to get into all of them, but some of the things that that we often find in accessibility reviews

0:17:35.740,0:17:40.400
and one of those hidden messages and controls

0:17:40.700,0:17:51.920
and this is where a particular piece of the software user interface is simply not giving information

0:17:52.200,0:18:01.300
to the operating system in a way that the keyboard annal or the screen reader is able to process that information.

0:18:01.920,0:18:12.520
And in this particular example, it wasn't a coding issue on the team that was at VeriCite.

0:18:12.800,0:18:21.500
What it was in fact was that there was a certain software widget that was part of a third-party library

0:18:23.480,0:18:25.560
that was part of the code base

0:18:25.560,0:18:33.060
and that particular library item had not been built with accessible controls associated with it.

0:18:33.300,0:18:36.980
So this presented an interesting challenge, which is that

0:18:38.000,0:18:42.660
the developers at VeriCite didn't have the code for that particular widget

0:18:42.660,0:18:51.640
and so then it's either find a different library item or find source code so that you can make adjustments

0:18:52.460,0:19:02.600
but it is the case that that good software development tools

0:19:03.440,0:19:09.260
also recognized that having those tools be fully accessible is really important.

0:19:10.640,0:19:17.040
But this is an example where it wasn't just a simple coding issue.

0:19:17.500,0:19:28.400
Something that was a coding issue that that can be dealt with are where you have hover text

0:19:29.300,0:19:39.320
for example, that is usable by someone who can see and then mouse over particular piece of the user interface.

0:19:39.320,0:19:49.480
And in one of the examples, the hover text would provide helpful information but that helpful information

0:19:50.320,0:19:55.460
didn't exist unless ... except through that hover text.

0:19:55.880,0:20:00.440
And so then you're presented with situation where you have to do some thinking

0:20:00.440,0:20:10.460
about how you want to have that information, you know, be delivered to the user through the user interface.

0:20:11.020,0:20:17.200
There's different processes, different philosophies about how to approach that.

0:20:21.520,0:20:27.340
Some things that come up are directly related to code issues.

0:20:27.700,0:20:36.680
For example, one of the findings was related to labels that were on the user interface,

0:20:37.140,0:20:46.900
where it wasn't using the appropriate code to be able to make that particular form item uniquely identifiable

0:20:47.560,0:20:50.440
through keyboard access and the screen reader.

0:20:50.700,0:20:57.140
And there are a lot of examples of things like that and fortunately those are ones where

0:20:57.140,0:21:03.520
once you identify one instance of it and you make the adjustment in the code,

0:21:04.100,0:21:08.020
it can propagate throughout the software system.

0:21:09.740,0:21:18.980
So sometimes when you'll do an accessibility report, you may get this extremely long list of issues

0:21:18.980,0:21:27.200
of essentially of bugs, but you may find that one of those issues crops up 85 times,

0:21:27.620,0:21:32.900
And it's just the same issue. And if you're able to do a global replace of that,

0:21:33.000,0:21:37.500
you can often just check that one off and be able to move forward.

0:21:39.380,0:21:47.800
In that particular item again, I'm associating in this document the W3C recommendation.

0:21:47.800,0:21:53.720
So 1.3.1 Info and Relationships, again another foundation level A,

0:21:54.120,0:21:58.460
the information is either in text form or can be programmatically determined.

0:22:00.460,0:22:10.100
There's a couple of researchers at the University of Washington, Jacob Wobbrock and Richard Ladder,

0:22:10.100,0:22:12.240
who just recently retired.

0:22:12.560,0:22:22.360
But, their research includes just an amazing number of assistive devices

0:22:22.360,0:22:29.880
that have been developed over years to help people with very specific challenges.

0:22:30.200,0:22:37.460
And those assistive devices are tied to ...  those assistive devices ...

0:22:37.820,0:22:46.880
I'll share the one common issue that they're relying on a software user interface to be programmatically visible,

0:22:48.560,0:22:50.240
to how that device works.

0:22:51.600,0:22:56.140
Now, here's the next issue that I want to talk about,

0:22:56.420,0:23:03.160
is one that was a big problem for design and for development

0:23:03.400,0:23:13.580
and is just a big issue generally, which is when you're using color as a way to impart information

0:23:13.580,0:23:24.280
in the software user interface and in this case, when an instructor would process a paper in VeriCite,

0:23:25.440,0:23:33.440
it would highlight individual sentences in that paper and attach a color code to those sentences

0:23:33.720,0:23:41.440
based on the likely percentage that that information was not original.

0:23:42.300,0:23:51.240
And so it was somewhat like a heat map scale where orange was highly likely that something wasn't original

0:23:51.540,0:23:54.640
to a lighter orange to a yellow.

0:23:55.380,0:24:08.240
And the thing was, this was a very popular method of presenting that information to people that could see it.

0:24:08.460,0:24:22.060
Color in that situation is able to provide a grasp of your overall feeling about that,

0:24:22.060,0:24:30.020
and this is where we get into, what I think are the interesting design challenges for us

0:24:30.340,0:24:39.220
is not just dealing with the the technical issues of the accessible design

0:24:39.400,0:24:47.340
but rethinking the overall design so that it can be useful to anyone that's using it.

0:24:47.620,0:24:57.840
And actually, I think I would ... I'll just let me just jump, open things up here or just to ask,

0:24:57.840,0:25:03.340
what could be an alternate way to do something like this

0:25:03.580,0:25:11.900
that would provide that same value to anyone that was that wanted to get that kind of information?

0:25:13.460,0:25:14.640
Any thoughts?

0:25:14.820,0:25:15.560
Yes ...

0:25:15.640,0:25:16.880
[Attendee] [Indecipherable]

0:25:16.880,0:25:21.800
[Joe]: Oh, I'm sorry, should I do the microphone for that? Ok, go ahead ...

0:25:22.100,0:25:23.800
[Attendee]: Change the size of the font.

0:25:23.800,0:25:33.440
[Joe]: Change the size of the font, and then how is the size of the font then rendered to ...

0:25:36.020,0:25:39.220
... to people that aren't able to see the size of the font.

0:25:40.180,0:25:48.920
[Attendee]: They'd have to have after maybe every sentence a percentage or a certain interval.

0:25:49.280,0:25:54.160
[Joe]: A certain percentage ... alright, so ... and what was your name?

0:25:54.160,0:25:54.940
[Attendee]: Anthony.

0:25:54.940,0:26:01.380
[Joe]: So what Anthony is doing, he's kind of ... backing up a step on that which is

0:26:01.840,0:26:10.340
what is it about the information that we had before we applied the color,

0:26:12.120,0:26:16.680
and can we then impart that in an alternative way.

0:26:17.120,0:26:26.280
And so, it's possible then that the UI could in text and audibly

0:26:26.640,0:26:32.160
provide percentages for those different values throughout.

0:26:32.860,0:26:38.220
Now this is something ... this is the kind of thing where there's not an easy solution to it

0:26:39.700,0:26:45.380
but we kind of embrace that, which is it ... yes go for it ...

0:26:51.500,0:27:01.420
[Attendee]: I've seen some sites where the user has control over the color and the font size

0:27:01.420,0:27:08.960
and is that a possible solution, the ability to change color and change font size?

0:27:10.460,0:27:19.300
[Joe]: And what would make it something that would provide you with the mental model of

0:27:20.460,0:27:25.920
the overall feeling about the originality of the information?

0:27:25.920,0:27:36.980
[Attendee]: So, I gather that for each block of text, that for some people, they do not see the text

0:27:37.520,0:27:47.560
probably because of font size or the color contrast, and so that's why I had suggested that

0:27:47.940,0:27:53.840
perhaps if you allowed them to control that themselves, then

0:27:54.160,0:28:03.540
it would become a ... experience for the user, so some people could see the current ... yellow ...

0:28:04.520,0:28:05.080
[Joe]: Yeah

0:28:05.080,0:28:12.340
[Attendee]: That's a good idea, so the legend is actually interactive, you know, you can click on it, it's a legend that's interactive.

0:28:13.160,0:28:20.460
Therefore, keep me honest Allen if I hear you correctly, the idea is, you can customize each one of those things,

0:28:20.460,0:28:26.960
however it would make sense to you, or even ... you can click on it and maybe you can focus on it,

0:28:27.620,0:28:32.980
and then it just brings things up to the other gentleman's suggestion, the font becomes larger,

0:28:33.460,0:28:39.300
maybe it identifies it, maybe for a screen reader, it actually reads all the high matches.

0:28:39.440,0:28:45.840
So it's how you sort, how you create maybe a slightly different hierarchy of what you are looking at

0:28:45.840,0:28:50.460
and prioritize it based on whatever makes the most sense to you.

0:28:51.540,0:28:58.420
[Joe]: Yep. Any other thoughts about that? Looks like we had another comment over there ...

0:29:00.520,0:29:27.080
[Attendee]: [Indecipherable]

0:29:27.080,0:29:28.020
[Joe]: Yeah, that's good.

0:29:28.900,0:29:34.640
So there's ... oh go ahead, let's take, did you want to ...

0:29:34.940,0:29:38.840
[Attendee]: [Indecipherable]

0:29:38.840,0:29:51.560
[Joe]: This is ... this will show, other than a screen capture, normally you'll see a page of text from a student

0:29:51.560,0:29:52.940
or a passage of text.

0:29:53.240,0:29:54.600
[Attendee]: So, um,

0:29:55.640,0:29:58.200
what if you had a

0:30:00.140,0:30:09.000
sort of think of it like a tag, but it would be something that could be ... high match and high match.

0:30:09.840,0:30:17.040
[Indecipherable]

0:30:17.040,0:30:18.100
[Joe]: Yeah.

0:30:19.140,0:30:26.320
These are the kind of discussions that come up

0:30:28.320,0:30:35.380
once we've done this initial accessibility review and then I you know ideally we start you know rethinking

0:30:35.820,0:30:40.240
of better ways to do this, but in this particular case,

0:30:40.720,0:30:47.620
this then becomes a somewhat fundamentally difficult

0:30:49.520,0:30:53.820
part of the software interface to make an adjustment to.

0:30:53.820,0:30:57.660
So it requires a commitment on everyone to recognize that

0:30:59.500,0:31:07.320
things may have to go back a ways to, in the process, to be able to move forward with a better design.

0:31:09.740,0:31:12.660
Well let's ... let me go over some other things.

0:31:12.660,0:31:21.280
Now I ... whenever you're talking about color, there's also the issue of color contrast.

0:31:21.640,0:31:32.420
And I have issues discriminating between certain color combinations myself,

0:31:32.960,0:31:40.480
which you know people that don't have that issue, don't understand it my wife doesn't understand when I say,

0:31:40.480,0:31:46.000
I do not know what actually what shade that is.

0:31:46.000,0:31:56.920
But fortunately, there's been decades of research related to different types of color issues

0:31:56.920,0:32:05.260
that are related to sight and much of it, well all of it has really been converted into math.

0:32:05.740,0:32:12.580
So there are underlying tables that identify ratios between foreground and background colors

0:32:13.020,0:32:23.260
that have been matched up to common issues that people have in identifying one color from another.

0:32:24.180,0:32:31.760
And so, a lot of tools are available to be able to identify the problems and then also make the adjustments.

0:32:31.780,0:32:36.780
And so, in this case, it's going back to the Wave tool that I mentioned.

0:32:37.060,0:32:46.780
There was a failure of part of the software ribbon in terms of the background color,

0:32:46.780,0:32:52.560
which was a charcoal gray and the foreground color which was an off-white,

0:32:53.280,0:32:58.660
and this is one of those areas where

0:33:00.740,0:33:09.680
sometimes I'll encounter pushback from people that were involved with the design of the palette.

0:33:12.840,0:33:20.740
But once people understand that you can just make small adjustments

0:33:21.200,0:33:28.940
to those color combinations to make them work for people, that kind of makes everybody happy again.

0:33:28.940,0:33:35.500
In fact, in this case, for this background in charcoal and the foreground in an off-white

0:33:35.500,0:33:40.220
which did not pass the contrast ratios,

0:33:41.340,0:33:50.800
just using a tool like, for example, colorsafe.co, you can iterate and experiment with different color combinations.

0:33:51.160,0:33:57.500
And you can come up with one that has a ratio that does meet standards.

0:33:59.840,0:34:04.900
But to most of us you would never notice the difference between that background and foreground color.

0:34:07.220,0:34:12.660
Just about every project, color contrast gets flagged in some way or another.

0:34:12.880,0:34:17.440
But we also know that it's a fairly easily solvable problem.

0:34:21.360,0:34:28.940
Another item that we find in a lot of projects is the use of heading style tags,

0:34:29.180,0:34:32.400
either not using them or using them incorrectly.

0:34:32.620,0:34:40.560
For people using screen readers, properly used heading tags h1 h2 and so on,

0:34:40.980,0:34:51.860
is one of the ways that you can impart meaning that can be interpreted by various assistive devices.

0:34:53.160,0:34:57.300
so that the heading one versus the heading two and the heading three,

0:34:58.480,0:35:04.920
that's important to people that are relying on understanding that structure.

0:35:05.300,0:35:11.600
Where we run into a problem is in sites where heading tags aren't used at all

0:35:11.600,0:35:17.100
and so the screen reader isn't able to use that device to be able to do hierarchy.

0:35:17.360,0:35:24.940
But another case, and the one that we had in this product is where those heading tags are used

0:35:26.420,0:35:29.420
for presentation purposes, for sighted users,

0:35:29.420,0:35:35.740
which is, oh the h2 tag by default has the font that we like and it's bold

0:35:35.740,0:35:40.660
and it's pretty close to the size that we want to use in most browsers.

0:35:42.600,0:35:51.400
Unfortunately, that then can be a situation where you're applying heading tags to parts of the text

0:35:51.400,0:35:55.500
that aren't part of that semantic hierarchy.

0:35:55.780,0:35:57.400
And so, that was the case here.

0:35:57.680,0:36:08.900
So, there was a, for example, just a data piece in the case that I'm reading East Side King County Washington,

0:36:09.260,0:36:13.280
that had an h5 heading five tag associated with it.

0:36:13.660,0:36:20.300
So we never want to do that. The more appropriate method is to use our cascading style sheets,

0:36:20.700,0:36:31.000
develop a class specifically for data types, totally disconnected from the headings.

0:36:33.140,0:36:34.360
Yes, sure ...

0:36:34.360,0:37:04.660
[Attendee]: [Indecipherable]

0:37:06.700,0:37:10.020
[Joe]: It's an interesting issue where ...

0:37:11.700,0:37:19.180
first of all you like you have issues just about, just the development and management of the software,

0:37:19.180,0:37:30.800
but then there's also an issue about whether or not the operating system itself is already providing some ways

0:37:31.440,0:37:33.260
for people to adjust that.

0:37:36.480,0:37:41.660
I guess I don't have a great answer to your question, in that

0:37:42.300,0:37:46.040
I think on any given project, you just have to

0:37:47.060,0:37:53.640
think through it to make sure you know it's matching the needs of the project.

0:38:00.460,0:38:07.240
Let's see, so everything I've looked at so far has been an A or a double A issue.

0:38:07.500,0:38:10.660
But, there is also triple A issues.

0:38:11.020,0:38:17.500
And some sites, you know, attempt to be able to provide that,

0:38:17.500,0:38:31.960
which in the web accessibility initiative, is sort of our best our best attempt at being able to make everything

0:38:31.960,0:38:37.840
as accessible as possible to people with a wide variety of challenges.

0:38:37.840,0:38:45.120
But now, Triple A is beyond what we said is our own compliance level and triple A also ends up being

0:38:45.120,0:38:50.580
outside of most Section 508 and European Union guidelines.

0:38:51.640,0:38:57.500
But, still, there are there are issues there and the one I had just mentioned right here is

0:38:57.920,0:39:04.180
when you're using abbreviations in the software interface.

0:39:04.480,0:39:10.980
For sighted people, the abbreviations can be instantly determined.

0:39:11.340,0:39:19.900
In one case, for example, abbreviating the word points with PTS.

0:39:21.140,0:39:30.340
Now, when and in the example I'm talking about here, there's a field that has the label grade

0:39:31.500,0:39:39.440
and then that field has two data items that can be there, but in this case, the data items are null.

0:39:39.440,0:39:48.180
So there isn't data to put there and so it uses two dashes for each of the missing data points,

0:39:48.320,0:39:51.000
followed by that abbreviation for points.

0:39:51.360,0:39:59.800
And in the screenreader that comes off as ... oops, I'm sorry about that ... oh good I didn't break anything.

0:40:01.220,0:40:06.880
What that comes out as is gray dash dash slash dash dash pts.

0:40:09.760,0:40:14.740
And so, somebody using a screen reader is going to get that as their experience.

0:40:15.080,0:40:22.400
Is that going to keep my friend who uses a screen reader from understanding that?

0:40:23.160,0:40:27.840
No, but it's annoying to me, so I wouldn't you know be annoying to anybody else.

0:40:27.840,0:40:37.800
And so, I try to look at acronyms and abbreviations and identify whether something is an acronym,

0:40:38.080,0:40:42.440
that's part of a typical business case that someone would be familiar with,

0:40:42.680,0:40:49.680
or if I'm just doing something to save room and user interface, in which case, I may want to re-examine that.

0:40:50.520,0:40:54.100
[Dennis]: One thing is the about abbreviations.

0:40:54.100,0:41:00.040
Anyone, if you have frequently asked questions,

0:41:00.860,0:41:03.860
be careful of using FAQs.

0:41:04.700,0:41:08.780
You're basically communicating an F-bomb.

0:41:10.780,0:41:13.420
Of you don't believe me, listen to a screen reader.

0:41:13.420,0:41:15.420
[Laughter]

0:41:17.980,0:41:25.960
[Joe]: Well I ... so that brings me through some of the typical findings that were a part of this case study

0:41:25.960,0:41:28.140
that I thought you might be interested in.

0:41:28.140,0:41:36.480
They're a lot more than this, but I want to stay within our time amount and just talk about the reporting process.

0:41:36.980,0:41:44.980
And, first of all, just to mention that the time tracking for this project for my work

0:41:44.980,0:41:54.400
in doing an accessible review of this existing project had me spending close to 50% of the time

0:41:55.260,0:42:03.580
running the test with the keyboard and with the screen reader to work through the software user interface

0:42:03.960,0:42:12.680
and an additional 10% ahead of time to analyze the system

0:42:12.680,0:42:17.660
to see if the tools that I'm using are going to be appropriate for that.

0:42:18.380,0:42:30.020
And so, that makes up a large amount of time, which, in my examination of how I've spent time on accessible reviews

0:42:30.020,0:42:42.040
versus reviewing user interface designs for other aspects, it takes about 20 to 30 percent more time

0:42:42.040,0:42:49.160
to be able to work with the screen reader and the keyboard access, in addition to

0:42:49.560,0:42:55.000
the normal testing and vetting we might do for quality assurance of our products.

0:42:57.040,0:43:01.500
So, I just wanted to throw that metric out just as an example.

0:43:03.700,0:43:08.660
But then, and also in terms of the reporting, there's the issue of the handoff to the client,

0:43:08.660,0:43:16.180
and despite the fact that accessible design has been a thing for a long time now,

0:43:16.440,0:43:22.960
I would still say that the large majority of digital products and services

0:43:23.340,0:43:27.240
are paying a great attention to this particular area.

0:43:27.240,0:43:41.100
And so, when people decide to get involved with it, often the people in charge of our client's work

0:43:41.440,0:43:48.300
may have differing levels of experience in terms of accessible design issues.

0:43:48.680,0:43:55.360
And so, I always have to consider that when I'm talking about the results

0:43:56.040,0:44:04.020
So, if you're talking about whether a button should have been blue or orange,

0:44:04.780,0:44:10.800
that's pretty straightforward to most people in design,

0:44:10.800,0:44:17.800
but when you maybe get into a discussion of any of the things that we've just looked at, you know,

0:44:17.800,0:44:23.180
takes some understanding of what accessible design is all about.

0:44:23.180,0:44:33.980
So that's an issue and but then maybe even more difficult is being able to present the findings

0:44:33.980,0:44:40.560
to people that haven't been involved in the accessibility review, so that they can make the adjustments.

0:44:42.180,0:44:47.660
So maybe in-house designers that were handing off a report to and remember,

0:44:49.040,0:44:54.680
keyboard-only access I think is important, screenreader understanding is important.

0:44:54.680,0:45:08.320
So what I do is, I use a product like Camtasia to record every session that I do with the keyboard and with the screen reader.

0:45:08.660,0:45:15.900
An external camera and I'm able to capture each of my sessions as I do the review.

0:45:16.180,0:45:24.860
And so, that's available so that anybody can look at those go through those videos and be able to identify

0:45:25.920,0:45:32.580
what the issue was, where it occurred and match that up to the reports, which I mentioned earlier,

0:45:33.120,0:45:40.180
so those same sample use case scenario documents that I use for are working through the software,

0:45:40.180,0:45:48.080
then become the place where I embed the information about the various findings.

0:45:48.900,0:45:54.200
And I also try to do that in a way that can be searched programmatically,

0:45:54.200,0:46:00.480
so all of the findings are in this Word document are given their own style.

0:46:00.480,0:46:02.820
So findings have their own style,

0:46:02.820,0:46:11.680
you can search on those, to be able to identify those separate from all the other information in the document.

0:46:11.920,0:46:16.380
They also have a check mark, which can be programmatically determined

0:46:16.380,0:46:22.920
and also have a color associated to that particular item.

0:46:23.200,0:46:29.500
And then additional notes, I also use Word styles, give notes a different style,

0:46:29.900,0:46:36.720
precede each note with the Word note and so that information can also be programmatically determined.

0:46:38.160,0:46:43.480
But then, this becomes the document that goes to the client,

0:46:43.740,0:46:47.080
along with the repository of the videos.

0:46:48.840,0:46:55.540
And of course those videos can be closed captioned with a service like rev.com.

0:46:57.520,0:46:59.520
So a couple of final notes,

0:46:59.520,0:47:06.040
I mentioned Wave reports and there are limitations to using that tool.

0:47:06.040,0:47:15.400
But it's really meant as a way to evangelize what is possible in terms of identifying issues with software.

0:47:16.320,0:47:22.000
But Wave only works with web content that is on a public facing server.

0:47:23.460,0:47:30.260
So if it's a subscription-based or it's behind a security firewall, Wave can't access that.

0:47:30.520,0:47:42.120
This was a subscription-based product, but there wasn't a security issue about the privacy of the software service.

0:47:42.120,0:47:47.800
And so what we were able to do was, within the subscription firewall,

0:47:47.800,0:47:58.920
save copies of all the web-based pages, along with their HTML CSS and JavaScript components etc.,

0:47:58.920,0:48:07.220
and then post that on to a public-facing server and then run the web report, the Wave reports off of that content.

0:48:08.320,0:48:12.540
But for people where there is a privacy issue related to the content,

0:48:12.780,0:48:16.360
then a tool like this isn't something that you'd be able to use.

0:48:17.740,0:48:26.720
Last thing I want to mention is, I just to take aways, which I've mentioned a couple of times,

0:48:26.720,0:48:32.020
that I think it's important to gain keyboard only and screen reader skills,

0:48:32.020,0:48:40.200
think about using scripts and video recordings to supplement the work that you do in the reporting,

0:48:42.320,0:48:49.000
and one of the things I didn't mention separately is just building a library of solutions.

0:48:49.960,0:48:55.960
So we try to keep building that up and a lot of things crop up repeatedly on projects,

0:48:55.960,0:48:58.900
so it's good to remember what happened.

0:48:58.900,0:49:03.840
We have a code sample, so that you can make things easier going forward.

0:49:03.880,0:49:10.600
And, yeah and just keep trying to do better as we move forward.

0:49:11.780,0:49:23.320
And the last thing I want to mention, just getting back to testing, using participants with various physical challenges,

0:49:23.320,0:49:29.860
the employment rate of people with various challenges

0:49:30.740,0:49:35.800
in a lot of cases is extremely low compared to the general population.

0:49:35.800,0:49:44.760
And so, what you'll find is that, you know, gathering together a team of people

0:49:44.760,0:49:50.000
that you can rely on to be able to be good testers for your accessible designs

0:49:50.200,0:49:57.840
is also something that just provides a valuable employment opportunity for people.

0:49:57.840,0:50:05.720
And so, we've had really good success building relationships with people that we can rely on

0:50:05.720,0:50:09.300
to help us with different parts of the final testing.

0:50:10.980,0:50:15.120
Alright, so, that kind of wraps things up.

0:50:15.120,0:50:19.480
Again I want to thank VeriCite for allowing me to talk freely about this stuff.

0:50:19.720,0:50:27.560
I work on this stuff all the time and so feel free to connect up with me, you know, afterward about that.

0:50:27.560,0:50:33.760
I can send you that document version that I have available and so and ...

0:50:33.760,0:50:35.700
[blip blip blip sound]

0:50:35.700,0:50:37.480
[Joe]: ... there I am right at the end of it.

0:50:37.480,0:50:45.860
And the other last thing I wanted to mention is that I'm also the program manager for Blinks Convey UX Conference.

0:50:45.860,0:50:53.880
So it's a our local Seattle UX conference and I'm taking proposals for sessions for 2018.

0:50:53.880,0:50:58.700
So if you're interested in making a visit to Seattle, definitely get in touch.

0:50:58.700,0:51:04.580
And I definitely love to look at what you have in mind so ...

0:51:05.620,0:51:13.480
[Applause]

0:51:13.480,0:51:15.160
[Dennis]: Question for Joe?

0:51:15.160,0:51:16.340
[Joe]: Or generally?

0:51:18.280,0:51:24.180
[Attendee]: Do you find the screen readers to be consistent across the different ones?

0:51:24.220,0:51:32.660
Do you have to design specifically for the certain brand or the certain predominant player in that space?

0:51:32.660,0:51:34.500
[Joe]: It's a good question.

0:51:34.500,0:51:42.720
I think the question it partly is, you know, what's going to be appropriate for your particular project.

0:51:42.720,0:51:52.700
So in this project, I felt that using the NVDA freeware that's available was acceptable.

0:51:52.940,0:52:00.180
But I have a colleague of our accessible meetup in Seattle, working for Wells Fargo,

0:52:00.440,0:52:09.560
where her team regularly uses every screen reader, they check, do cross browser compatibility,

0:52:09.840,0:52:16.660
they have a whole list of various tools and issues that they test for.

0:52:16.980,0:52:22.560
And so I guess the short answer is, it depends.

0:52:22.560,0:52:28.180
By not trying to trivialize it, it's just that in some cases I think like in this situation,

0:52:28.720,0:52:39.100
that using something like NVDA can identify a good amount of the potential issues.

0:52:39.960,0:52:41.600
[Attendee]: Thank you.

0:52:42.780,0:52:44.780
[Dennis]: I need my workout.

0:52:46.000,0:52:50.180
[Attendee]: So you were mentioning you doing more, sort of heuristics.

0:52:50.180,0:52:57.980
So, what is the determining ...  [indecipherable] ... when do you determine, you know what, I need to have

0:52:58.740,0:53:04.080
three or four people looking at this, through different devices, do you start saying "Hey ...

0:53:04.960,0:53:10.380
we need to start looking at this on mobile,  and then when you sort of consolidate those ideas and say Hey ...

0:53:10.980,0:53:13.100
this is where we might need an expert walkthrough,

0:53:13.380,0:53:18.780
where we bring in somebody who is either visually, cognitive or perhaps audio

0:53:19.360,0:53:24.060
on challenges. Just give me the sense of, what are those tipping points?

0:53:24.300,0:53:28.580
Because right now, you're ... what I assume is that pie chart you shared was basically your effort.

0:53:29.220,0:53:38.460
But, you know, UX professionals usually want ... [Indecipherable].

0:53:39.340,0:53:43.900
You know, just to get a sense of the global issues and then to zero in on those expert reviews.

0:53:45.140,0:53:52.080
[Joe]: So, for example, at Blink, everything there is done collaboratively.

0:53:52.220,0:53:55.600
And there are several people that are involved in the process.

0:53:55.980,0:54:00.980
But it really does come down to, you know, every project having ...

0:54:01.680,0:54:04.720
talking about exactly the things that you talked about,

0:54:04.800,0:54:11.640
which then come up with the things such as the compliance level which then also loops in the client.

0:54:12.800,0:54:19.940
For example, in this case, one of the questions we had was to identify what contractually is an issue.

0:54:20.080,0:54:22.300
And that can vary from project to project.

0:54:24.480,0:54:31.940
And ... but one of the more practical issues that is a challenge for me as so many that ...

0:54:32.480,0:54:37.200
... that is really interested and cares about this issue is that,

0:54:38.260,0:54:45.820
for every client like VeriCite that has chosen to build this into the design and research of their product,

0:54:46.620,0:54:53.260
that's only a fraction of the work that's being done out there.

0:54:53.260,0:55:01.500
And so, a lot of the work that we've been doing over the last few years is just trying to be able to

0:55:01.760,0:55:06.420
have a conversation with clients that haven't been doing accessible design,

0:55:06.640,0:55:15.160
to make them understand that there are really good reasons to add in the 20 or 30% realistic costs

0:55:15.160,0:55:23.700
over what they're doing already for designing research to be able to effectively provide these techniques.

0:55:25.340,0:55:28.600
[Attendee]: I have a two part question.

0:55:29.900,0:55:34.000
The first question is the reason that you're saying about, you wanted to ...

0:55:34.000,0:55:38.980
you only test on the front-facing website ... [indecipherable] ...

0:55:39.160,0:55:43.840
where ... [indecipherable] ...

0:55:44.160,0:55:50.400
And, the second part of the question is, [indecipherable] ...

0:55:52.040,0:55:57.180
[Joe]: So on that first part, in terms of mobile,

0:55:57.180,0:56:07.600
one of the things that we found that just a strong hardware issue

0:56:07.600,0:56:19.120
is just the level to which people who are blind have embraced the iPhone specifically over other devices,

0:56:19.120,0:56:22.820
specifically because of Voiceover.

0:56:23.720,0:56:33.640
In those cases, for mobile first, mobile only, then the iPhone in fact becomes a device

0:56:33.640,0:56:38.740
that's the most important device to be able to test for.

0:56:38.740,0:56:49.340
And so, in that case, it's a matter of being able to have facilities available

0:56:49.340,0:57:00.580
and to be able to do the interviewing and capturing things with video as part of the testing process,

0:57:00.580,0:57:08.000
and then, naturally, I'm not sure that the design of the ...

0:57:14.160,0:57:20.920
I don't want to say that it's harder to design for mobile, because in many ways,

0:57:20.920,0:57:27.640
designing mobile first simplifies things across the board.

0:57:27.640,0:57:39.220
And so, I think that's one of the things that you notice is just you're coming from a simpler base point,

0:57:40.440,0:57:43.180
where then you have less problems as you scale.

0:57:43.780,0:57:50.940
And then your second part of your question was related to the relationship between deaf and blinder, or?

0:57:51.000,0:58:05.120
[Attendee]: [Indecipherable]

0:58:07.500,0:58:15.500
[Joe]: So, you're certainly being able to make sure that there are

0:58:15.820,0:58:21.440
text equivalents for anything that's audio related,

0:58:21.640,0:58:30.920
which is a big ... that might be very soon or maybe right now is ... could be the biggest

0:58:32.300,0:58:41.920
non-compliance issue, is just not having a suitable closed caption alternative.

0:58:42.180,0:58:50.780
But, I also really believe in having available for videos

0:58:51.160,0:58:59.280
a transcript version and that's something that some people don't like, it's like an extra link

0:58:59.840,0:59:03.180
and it's an extra document and it's extra part of the process.

0:59:03.640,0:59:09.760
But I think a transcript can be really useful.

0:59:09.980,0:59:18.960
But that closed captions is the biggest part and a lot of organizations will just rely on,

0:59:18.960,0:59:25.640
let's say, YouTube to be able to do the captions.

0:59:25.640,0:59:32.880
But anybody that really cares about that notices that the fidelity tends to be very low

0:59:32.880,0:59:44.340
and it doesn't like meet my professional quality and so you know we would use a professional caption for that.

0:59:44.840,0:59:46.380
Yes, go ahead ...

0:59:46.380,0:59:51.260
[Attendee]: ... was that, I read an article Dennis, I think it's one of the articles you shared.

0:59:51.260,0:59:56.640
And it talked about YouTube, the auto caption, it's only three or four percent off.

0:59:57.200,0:59:59.140
Then it literally, it is not comprehendible.

1:00:00.000,1:00:04.280
So, somebody who's deaf, they will not be able to understand whats there.

1:00:04.280,1:00:07.580
So, keep in mind of that. Don't worry, three or four percent. Well guess what ...

1:00:07.580,1:00:11.620
that three or four percent means they can't understand what's being described.

1:00:12.080,1:00:15.380
Now I don't have any idea why companies don't use transcripts,

1:00:15.380,1:00:19.080
you know, because, I have a cognitive disability, I'm dyslexic,

1:00:19.880,1:00:22.940
and I love transcripts, because that's my notes.

1:00:23.300,1:00:28.160
So I don't understand why companies shy away from it, an extra link?

1:00:28.960,1:00:31.160
You know, I don't understand ... sorry ...

1:00:31.200,1:00:32.280
[Joe]: No, no ...

1:00:32.280,1:00:36.580
[Attendee]: Because to me, it's such minimal amount of extra work to just help so many people.

1:00:37.280,1:00:46.420
[Joe]: Yeah, like, I'm old, so I like ... I do old things, like start with a  script for a lot of videos that I'm involved in,

1:00:46.420,1:00:55.120
and so, the script becomes a transcript, becomes your closed captions, and in your ahead of the game.

1:00:55.120,1:00:59.500
But that's not the way that a lot of that content is developed today.

1:00:59.920,1:01:01.640
Yes ...

1:01:03.080,1:01:12.440
[Attendee]: You had mentioned that you had to adjust the report of your finding for the understanding of your client.

1:01:12.440,1:01:22.500
I'm wondering is there a website or some sort of resource, a Nielsen Norman, the reports specifically on

1:01:23.400,1:01:30.280
the various communities that need accessibility? Can you point us to a great resource for that?

1:01:30.720,1:01:39.040
[Joe]: I don't have a specific resource, but are you meaning like examples of ways to communicate?

1:01:39.040,1:01:47.160
[Attendee]: So, like, I'm arguing against using color used to differentiate selections, select UI.

1:01:47.720,1:01:53.940
And when I'm advocating for that, the people who are all about the minimal viable product are like,

1:01:54.580,1:01:56.020
we'll worry about that later.

1:01:56.020,1:02:04.460
I just need the means to say, "hey look, this is ... color acuity represents this segment of the population,

1:02:04.460,1:02:09.860
this many people are not going to see this. To kind of hold their feet to the fire.

1:02:09.960,1:02:15.180
[Joe]: Yeah, I don't have something like that, but you're getting at the core that which is like

1:02:16.080,1:02:28.020
actually and run some projects like maybe someone who's involved in initiating accessibility in your organization

1:02:28.020,1:02:35.920
is interested in how is this helping with conversion, how is this helping with supporting us generally,

1:02:35.920,1:02:45.140
how's this helping us legally, but like on this VeriCite project, when I got into the report discussion

1:02:45.140,1:02:49.260
with the client, the person involved there was the head of the dev team,

1:02:50.060,1:02:54.580
who was totally on board with this entire project in its entirety.

1:02:54.880,1:02:58.660
But what that person wanted from me was a bug list.

1:03:00.920,1:03:06.000
What's the issues, how do I find them, because we want to fix start fixing them right away.

1:03:06.780,1:03:10.640
And so, it was a completely different kind of conversation.

1:03:10.780,1:03:15.720
That person wasn't necessarily interested in those issues about conversion and things,

1:03:15.720,1:03:21.980
but just like how do I fix that, and so that was what I was alluding to is, just may need a different approach

1:03:22.980,1:03:24.200
to talk about that.

1:03:25.380,1:03:27.000
How are we doing on time, are we doing alright?

1:03:27.000,1:03:28.740
[Dennis]: Two last questions.

1:03:28.740,1:03:36.880
[Attendee]: Well, actually ... about the captions, with the videos,

1:03:37.460,1:03:42.200
I'm also like you. And so I went around before there were voices on the computer

1:03:43.000,1:03:49.120
and so I find that the transcripts are absolutely fantastic.

1:03:49.520,1:03:56.020
It allows me with a screen reader to skim through, get what I want, and get and be done with it,

1:03:56.240,1:04:14.600
but also ... I use braille a lot ... [indecipherable]

1:04:15.580,1:04:17.380
[Dennis]: And the final question ...

1:04:20.000,1:04:31.040
[Attendee]: You mentioned early on that the VeriCite university had a blind educator,

1:04:31.480,1:04:35.660
that really provided context to this.

1:04:36.740,1:04:46.960
If you did not have that situation, would you have had any trouble in expenditures to pull out accessibility

1:04:46.960,1:04:52.280
for faculty staff versus student facing interfaces?

1:04:52.280,1:04:57.300
That's something I run into a lot, if it's student facing, I can sell it.

1:04:57.740,1:05:01.320
If it's faculty staff, I can't, I work in higher ed too.

1:05:02.740,1:05:06.760
[Joe]: Yeah, I think that you bring up an interesting point.

1:05:06.760,1:05:09.780
In a couple things related to that is that

1:05:10.520,1:05:18.040
I actually like, although that my colleague, I actually never discussed VeriCite with that colleague,

1:05:18.040,1:05:24.280
but I'm always trying to meet as many people as I can in every community that there is

1:05:24.280,1:05:29.920
and just be able to appreciate everybody's particular challenges

1:05:29.920,1:05:39.560
and I happen to know, you know, recognize from other things that that instructor has those kind of challenges.

1:05:39.900,1:05:47.360
But in this particular case, on this is the kind of issue where

1:05:49.680,1:06:03.940
most ... the attention was really just about the experience of the user in this case,

1:06:03.940,1:06:14.500
which predominantly was the instructor, but also was the student and so in a way to the nature of this software

1:06:14.500,1:06:22.860
kind of meant that the instructor was represented, but I felt like just from teaching generally,

1:06:22.860,1:06:30.460
I recognize what you're saying about student body generally having kind of the priority

1:06:30.480,1:06:33.920
in terms of how we work things out.

1:06:34.680,1:06:37.380
[Dennis]: I lied ... one last question ...

1:06:37.380,1:06:39.840
[Attendee]: So, it's kind of like a two part question.

1:06:40.340,1:06:42.440
[Laughter]

1:06:42.440,1:06:44.340
[Joe]: Uh oh ...

1:06:44.340,1:06:48.460
[Attendee]: It's automation and doing automated testing.

1:06:49.100,1:06:56.320
What's the best way to approach automated testing? We already have developers who ... [indecipherable] ...

1:06:56.320,1:06:58.780
but how do we roll accessibility into those tests?

1:06:59.240,1:07:00.540
That's part one.

1:07:00.980,1:07:09.560
Part two is, at what point does automation ... [indecipherable].

1:07:12.160,1:07:19.140
[Joe]: So, first of all, I'm probably not to person to answer that you know in the best possible way,

1:07:19.140,1:07:24.560
except that, we've asked actively discussed what automated testing means

1:07:24.560,1:07:27.720
within Blink's consulting organization.

1:07:27.980,1:07:34.940
Most of what we do is more qualitative, because that's just the nature of our practice.

1:07:34.940,1:07:42.880
But, it's recognized in the research design and dev for products projects that are worked on generally

1:07:42.880,1:07:47.060
that automated testing is here and it's a big deal.

1:07:47.060,1:07:51.920
And in fact, there's automated testing specifically for accessibility issues,

1:07:52.300,1:07:58.440
but we haven't gotten there, where I have any you know, anything I can tell you a good answer for that

1:07:58.440,1:08:02.220
and possibly we have people here that might but I don't.

1:08:02.700,1:08:11.820
[Dennis]: One thing I will say is, right now, I'm captioning Marcy Sutton's presentation, tow or three times ago,

1:08:12.520,1:08:16.960
on automated testing on our YouTube channel.

1:08:17.500,1:08:24.300
And with that, thank you very much everyone for sticking around. Hope to see you next time.

1:08:24.320,1:08:26.220
[Applause]

1:08:30.120,1:08:33.240
Thanks to our presenter Joe Welinske.

1:08:37.360,1:08:41.900
Thanks to our co-host, the and UX Chicago Meetup.

1:08:42.520,1:08:48.940
Visit them at meetup dit com forward slash and UXCHI

1:08:53.020,1:08:55.960
Thanks to our venue host, Capital One.

1:08:56.320,1:08:57.880
What's in your wallet?

1:09:03.120,1:09:07.840
Captions were provided by Alternative Communication Services.

1:09:08.320,1:09:11.900
Visit them at ACSCaptions dot com

1:09:12.820,1:09:15.800
Captions were sponsored by McDonald's.

1:09:16.200,1:09:17.560
We're loving it!

1:09:22.000,1:09:27.440
Thanks to our sponsor, Sticker Giant, for all the meetup stickers.

1:09:27.680,1:09:30.920
Visit them at Sticker Giant dot com.

1:09:36.600,1:09:41.540
Thanks to Rosenfeld Media for their discount for our members.

1:09:41.800,1:09:48.160
Get 20% off really great books using code a11ychi.

1:09:51.840,1:09:54.000
Join the accessibility slack.

1:09:54.000,1:10:02.140
To subscribe, go to web dash a11y dot herukuapp dot com.

1:10:03.160,1:10:11.960
After subscribing, to join in the discussion, visit web dash a11y dot slack dot com

1:10:17.220,1:10:23.740
This recording was produced by the Chicago Digital Accessibility & Inclusive Design Meetup.

1:10:24.360,1:10:32.320
Visit us online at meetup dot com forward slash a11ychi

1:10:33.200,1:10:40.640
Visit us on Twitter at twitter dot come forward slash a11ychi

1:10:41.680,1:10:51.880
Visit us on Facebook at facebook dot com forward slash groups forward slash a11ychi

1:10:53.260,1:11:04.900
Visit our YouTube channel at goo dot gl forward slash GfcU9A

