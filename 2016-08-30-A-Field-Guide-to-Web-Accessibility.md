# A Field Guide to Web Accessibility with Derek Featherstone
## Derek Featherstone - Tuesday, August 30, 2016
[Source recording](https://www.youtube.com/watch?v=gf_BrfCZT7c)

**[Dennis]:** I'm very, very excited to introduce Derek Featherstone. He is a former Ironman tri-athlete, 
and a current Star Wars fanboy. You notice I saw the Ottawa meetup ... He's also been a web professional since 1999 an internationally known speaker, teacher and authority on accessibility and web design. He leads the team at Simply Accessible based in Ottawa Canada. He always puts the user first and strives to make the web a better place by designing experiences that are easy to use for everyone, including people with disabilities. Derek's ideal accessible experience is to combine engaging, rich content, with brilliant design, and technical development excellence. Please give a warm Chicago welcome to Derek Featherstone.

**[Applause]**

**[Derek Featherstone]:** I'm sweating a lot right now, with that introduction. I feel a little bit of pressure, but I think we'll sort it out.

This is a field guide to web accessibility. And the idea behind this is that this is a collection of things we've learned by actually working with people with different disabilities. On real things, and not just things we learned out of books or reading things that people said, these are the guidelines and this is how it should be. These are things that we learned doing actual testing with real people.

As opposed to fake people. It's when you test with fake people ... is well ... We're talking about sitting there... one of the thing we do at Simply Accessible, we kind of drew the line in the sand about two and a half years ago, and we said, we don't really engage in projects where there's no actual usability testing with people that actually have disabilities. And we drew that line basically, because to us, that's kind of the ultimate test of whether or not something works.

For us, the checklist, WCAG guidelines, the things we say we need to do from an accessibility perspective, that needs to be the starting point.  Not the end point. The true end point is really, yes, it meets all these technical requirements, but can it really be used by somebody that has different types of disabilities? Because if they can't, what was the point of it in the first place, right?

So this is a collection of stories and things that they kind of share those kind of concepts and situations with you. I'm really interested in this, because this is, you know, lots of people here, and I'm really interested in knowing how many people are web geeks and not web geeks. 

Some people come to these kind of meet ups and they're just interested in what we're talking about. So hands up and say "I" if you're a developer, like a web developer?

**[Multiple voices]:** "I"

**[Derek Featherstone]:** There wasn't enough "I's" there.  Hands up and say "I" if you're a developer.

**[Multiple voices]:** "I"

**[Derek Featherstone]:** That was better. Hands up and say "I" if you're a designer.

**[Multiple voices]:** "I"

**[Derek Featherstone]:** You guys are way less enthusiastic.

**[Laughter]**

**[Derek Featherstone]:** And then anybody like hands up and say "I" if you're a project manager or product owner type thing?

**[Multiple voices]:** "I"

**[Derek Featherstone]:** Good chunk of numbers there.  That's excellent. And then anybody, hands up and say if you're like a QA type of person?

**[Multiple voices]:** "I"

**[Derek Featherstone]:** There's a couple.  That's good.  See you in the corner.  Excellent. I don't know why you're in the corner but that's okay. And rest of you, how many people are like a hybrid of what you do, like whole a lot of everything. So hands up and "I" for that.

**[Multiple voices]:** "I"

**[Derek Featherstone]:** Probably most and the rest of you. Did I not cover anybody?  Is there somebody I did not cover?  I want everybody to feel represented here.

**[Attendee]:** User experience

**[Derek Featherstone]:** I consider that part of the design. UX. Anybody hardcore UX-ers? Hands up say "I".  How come you guys are not saying aye?  Say "I".

**[Multiple voices]:** "I"

**[Derek Featherstone]:**  There are 4 people are like, fair enough.  Fair enough. Did anybody just are here and doesn't know anything about the web at all.  Oh, networking, that could be fun?

**[Laughter]**

**[Derek Featherstone]** Okay.  That's fine too. It's good to kind of hear what kind of representation we have. I'm really interested in dynamics and where everybody fits. But hopefully, there's things in here that are useful for everybody.

I want to start off with this.  This is a tap from a hotel in London that I stayed at, London in UK. Not London, Ontario, which I'm from Ottawa, Canada. We have our own London. It's not quite the same but....

This is a tap from that hotel where I had a hot water tap on the left, and a hot water tap on the right. And I don't know what to do. So I decided I'm not showering that day.

**[Laughter]**

**[Derek Featherstone]:** It's not going to happen. This doesn't work for me if these two hot water taps are confusing. Until I see this sign that tells me that the left tap operates the shower and the right tap operates the bath. Now I know if I'm going to burn my head or feet at least.

The problem with this interface is that the tap is exactly where you expect it to be but the instructions on how to operate it are about six feet away on the side wall. You can all instinctively look at this and say well this just doesn't make sense. Those instructions need to kind of be somewhere in the line of sight. When you're looking at the tap, those instructions should be in the vicinity. From a design perspective, we call that proximity. We want to take these closely related items and we want to group them together.

So we're going to do a little experiment here. Very straightforward. I like you to all take your, provided you can see the screen, I'd love for you to take your left hand or right hand, either one. If you do both, it's not going to work. So take your left hand or your right hand, hold it up and make a fist like you're holding on to a straw. What you're going to do is you're going to look through the straw. You don't actually have a straw. Pretend you do.

You're going to look through the straw at the screen. What you're going to need to do is two things. One is orient yourself to the interface, and two is go through the process of filling out the form. So I just told you what's on the interface. It's a form, that you need to fill out. Does that make sense? You're holding the straw, we're going to do a test run.

Hold up your straw.  You need to actually like put it right up against your eye. And then you need to close the other eye. Okay.  Or cover it with your hand. So what we're doing here is limiting how much you can see. Now, some of you are holding on to a garden hose right now. You need to make it like a straw. Like a tiny cocktail straw. So that's what you're going to do.

I'm about to reveal the interface.  Are you ready or this?  Straw's up and the way you go! While you do that, I'm going to take a photo.

**[Laughter]**   

**[Taking photo]**

**[Derek Featherstone:]** Some of you are still filling in the form. Some of you are done. Some of you are like, I'm out. Can't do this. 

So what we have on this form, we have four clusters of information and the clusters are two questions on the left-hand side and two sets of answers on the right-hand side and then two more questions on the left-hand side and two more sets of answers on the far right-hand side. And then we have our Quit button, our Previous button and our Next button. 

This is a very straightforward form, and, yet, this was coded perfectly and it worked very well for somebody that was using a screen reader. And it was ... the developers that built it said to me, like, this is coded perfectly. This is accessible. And then we went and actually tested with people that had low vision, that weren't using screen readers. It failed miserably.

And those who were looking through the straw might actually understand a little bit about why. What motion did you have to go through 
to fill in that form? Left right, left right, left right, left right. Because of the way that this form is designed, where we have these questions on the left, and the answers way over on the right, what ends up happening is we're creating a situation like this.

When somebody has low vision, they have a limited view of the screen. So this is roughly 250% magnification. Somebody that needs 200% magnification is going to see roughly one quarter of the screen at any given time. If they need 300% magnification, they will see 1/9th screen at any given time. 400% would be 1/16th of the screen that they will be looking at. And so it's very easy to lose that context.

If you take a look here when we're magnified and we're zoomed in and you're looking at the questions, you really just see the questions. When you scroll over to the far right to get to those answers, those questions you saw are now kind of like, out of sight, out of mind. Same thing as the tap and the instructions for the tap being six feet away from each other. It's exactly the same thing.

So what we need to do in interface design is take those closely related items and group them together. There's really good reasons. We create visual relationships when we do that. We can create programmatic relationships all day long in code for screen reader users and Dragon NaturallySpeaking users. But the visual relationships are quite important for people with low vision.

The proximity of things become even more important to them. Almost more important than the programmatic side. So we're at this point here, where we've started on the left and we see the questions and gone over to the right to answer that first question. 

We go back over to the left to hit the next question. Right for the answer. 
Left for the question. Right for the answer. 
Left for the question. Right for the answer.
What's your next move?

Left for the question.  And it's not a question, but it's quit. It's a call to action that is kind of the least desirable call to action. And yet, we led them right there by that pattern of use we created. We also have things, and this is not unique to people with low vision, but there's a certain muscle memory that you've created. You probably felt it and you knew exactly how far to scroll over every time when you were looking through the straw. The place where those answers were, when we get our second least favorite call to action, the previous action. 

There's whole a lot of thing wrapped up into this. We've created a pattern of use. We have created the wrong chunks of information. And if you take a look at these three buttons, the quit, the previous and the next, from a design perspective, we say they have essentially the same visual weight. They're all the same shape. They're all roughly the same size and same color. All the same other characteristics. The only thing that's different about them is the text and the characters that are on them. So when we take a look at all 3 of these, these different factors, this design actually ends up kind of failing miserably.

Failing miserably for someone with low vision. We have these kind of the wrong chunks, right?

Question, question, answer, answer.
Question, question, answer, answer.

That's like all kinds of wrong. What we want to do is we want to take this and fix all 3 of those things at once and make this something that works a little bit better for someone with low vision. And we're not really just saying every form should be designed like this. But... well, actually we are. Every form should be designed like this.

We want to create things that work well, that have the right groupings, that have a really straightforward flow if it can, and have obvious calls to action. So we want to take this interface, and maybe turn it, and this is not the only design, but this is the one that works reasonably well.

The same interface and we design it so it's in a vertical stack. So instead of having multiple columns, we actually make things flow in a vertical stack such that we create the right groupings, and we go directly down to the call to action. So now, if you bring your straws up and fill out this form, compare the  experience. So go ahead. Straws up. And fill out this form. You should immediately recognize the difference. 

You probably will never completely eliminate left to right scrolling. That's not necessarily the goal. But the idea is, like, if this second question was really long, you might have to scroll some. You won't necessarily eliminate that. We were looking at magnification that was at like 250%. Somebody might be looking at it at 500%. But what we do by creating this vertical stack is we minimize the effort that's required to have, to fill out that form by somebody that has low vision. 

We've got the right groupings. Instead of question, question, answer, answer, we've got question and answer, question and answer, question and answer, question and answer. 

You also see what we've done with the calls to action. Right? they're now distinct. They're not all exactly the same shape. For someone with low vision, those shapes might look like the same blob, right? Whereas, here, we made it like this is a really definite, this is our primary call to action that we want people to take. Then the other ones, they look different and they have different characteristics in the interface. So all of that should make sense to you.

When we look at this even magnified and we Zoom into that roughly 250%, you can see what happens. That pattern of use is no longer left right, left right. It's straight down. The thing I love about this is that that design also works well for a mobile device. 

Multicolumn layouts on a mobile device for somebody that can see the screen are a total pain. When you have your form label to the left 
and you have the field on the right-hand side, I don't know about you, but I hate this when I tap into a form field, and suddenly, the label is gone, right? It's off the screen. I can't see it. When I move to the next field, if I hit the next, either I tap the field directly or if I use, there's usually a next field thing to go to the next field. Those don't zoom back out to let you see what the field is.

This single vertical stack is actually really good for people that are on a mobile device as well. So I love this kind of idea of creating these little things that we can do. And I want you to use that straw test. We use that straw test at Simply Accessible
to test wireframes, to test mockups, to test live designs. And that's all to try to make things better before we test with people with real low vision.

All we're doing is simulating some of the effects of having low vision by limiting that field of view. Make sense? Like use it. Every design you ever create, try it and see the impact that it has. I'm not saying you're going to make radical changes to your design, but you will find things that seem out of place. Go through flows.  Go through tasks. Like ... go and purchase Cubs Pirates tickets for tomorrow night. That's a great example. Go through that flow and what kind of things do you find that are out of place?

When we think of accessibility, we like to categorize and we say there's more or 5 major types of disabilities. We're talking about people with visual impairment, hearing impairment, mobility, cognitive impairments, you know, and even speech related impairments. We like to put categories and put people inboxes and it's really not that simple. And I really mean this. We like to put things in boxes all the time.

As an example, these are my two sons. And I have put them in boxes many times. Because it's lots of fun. This is our first son, he's 18 months here, 18 months old.  Now he's 12. I tried to get him to come tonight with me. He's here in Chicago with me. And he's like, you're going to show that photo of me in a box again, aren't you? I said yes. He said forget it, I'm not coming. And this is my other son who is now 3. This first son loves being in this box. I'm going to put my other son in a box too and see how happy he is. He wasn't nearly as happy. 

But we like to put things in the boxes and we do that in the accessibility world all the time. The reality is accessibility can be very, very messy. The real world, like real world kind of this is why this is in this field guide. We all want to believe that everybody stays
up-to-date with their technology, including people with disabilities and these are quotes from actual studies that we did.

"I should probably upgrade Jaws, but I'm going to have to manually move all my settings and macros and I just don't want to do it."

Like that's reality. This is a person that instead of being on Jaws 17, which is the latest and greatest and in the fall we'll probably see Jaws 18. This was a person on Jaws 13 which was effectively from 5 years ago. And we keep saying all these things. You know, I don't know if you guys knows this, but we're nerds and the rest of the world is not. Not that they never do, but they're slower to upgrade. They might choose not to. They're not as technically inclined as we are.

**[Attendee]:** And Jaws makes you pay for it.

**[Derek Featherstone]:** And Freedom Scientific, they make you pay. And this is another one. What is this?

"I've been using Dragon 10 for a while and it works so why do I have to spend the money when I don't have to?"

We're about to hit Dragon 15, it's coming out in September. Dragon 10 is from not quite five years ago. It works. Why would I update? That starts to get messy, especially when people are saying things, like we try to say it. I want to be just on this browser. We support these browsers and what assistive technology do we support? If we even have that conversation. Everybody wants to say, we even say when we're doing a lot of testing, current version minus 2. Well, current version minus 2 wouldn't have caught either of these different scenarios and these were people that showed up in actual testing for us.

If so it's kind of like that reality check that not everybody is like us. Even though we want to believe that everybody is. It just doesn't happen.

How many people never heard a screen reader at full pace before? Hands up and say "I." You might not know what a screen reader is. But this is basically somebody that is blind might use a screen reader to read the screen for them. And from a captioning perspective, this isn't going to work at all. Because this is just a very fast video. But this is actual footage from the user test that we did. And this person, this was how fast they had their screen reader going, pretty much all the time. So here we go.

**[Video Clip]** 
**[Indiscernible speech]**
**[Screen reader reading very fast]**

**[Derek Featherstone]** This is somebody that's going through the remote desktop software that they were using so they're looking for specific pieces of information. They're not sitting there listening to a webpage that fast to get at that content. They might slow that down to go through a form. But they had a very specific task they were trying to complete there. Which was let's log-in and allow people to access remote desktop. For that activity was completely fine. Right? For them.

Not everybody listens to it that fast. But that's an actual recording. We didn't go in there and speed this up with the magic of computer or anything. That was actually how fast it was. How easy do you think it might be to miss something when things are going that fast? An error message comes up.

This is the thing that's bugging me a lot lately. My webpages are giving me alert notifications when I'm typing. And that notification suddenly takes the focus and I dismiss it because I was typing something and I don't know what it said. Really easy to miss. Maybe that's just me, but that happens all the time. We dismiss notifications if we're in the middle of typing something, and we don't know what it was, but we feel like we've done our job. We've given them a notice. And they just, they actually, they didn't actually “notice the notice”… that's just a bad joke.

**[Laughter]**

**[Derek Featherstone]:** It's really easy to miss something when the screen reader is going that fast. And we tend to say, well, that's their problem. But actually, we have to kind of get passed that and say, well, what can we do about that? There are things we can actually, that we can actually change. When we talk about the real world of accessibility being messy, I love this example as well. Most people have talked about, and really, you can't answer this. You're not allowed to answer this.

When we say something about like the autism spectrum. People that are talking about people that are autistic or not autistic. We talk about the autistic spectrum. Just draw for me, you know, in the sky here, draw for me what a spectrum looks like when you think about the autism spectrum. So I'm seeing some people doing this putting their arms out wide. Some people are drawing a line. I don't know what this was. Somebody putting their hand up and down. I don't know what that is. But we'll go with it. That's totally fine. I saw one person do like a O and circley thing. It was like this. It was almost like jazz hands happening. Don't know where you're getting to. 

But this brilliant cartoon, that person that is autistic created to express how she feels about things and there was this cartoon, there's links to this out there. And I will tweet this out for the full version of the cartoon. She says here when people think of this word, they think of the autism spectrum like this. And it's that linear spectrum, where on the left hand side, we've got not autistic and on the right-hand side, you've got very autistic. And we have this mental model that some people have autism fits somewhere on there. And then, you know, because we think we can judge that kind of thing, we can see, or I can look at somebody and say they have autism. 

And it's totally not like that. But because of this idea that somebody is either not autistic or very autistic, or somewhere in between,
and that constitutes a spectrum. She was finding that people were constantly pushing her into situations that she was completely uncomfortable with simply because she didn't look autistic. And, so, she created this to kind of talk about that. And I love this, because her depiction in this next slide of what the spectrum actually means to her is brilliant. 

The truth is though, someone who is neural diverse in some areas of the brain will also be no different to the average person in other areas of the brain. So she took this and literally made like a circular spectrum that has the color of the rainbows, but it's kind of like different levels of saturation and different color values. And she says, so the autistic spectrum looks more like this and she has 5 aspects of kind of neural diversity or brain function that she mapped on to this.

There's many more than that, but she took these 5. Language skills, motor skills, perception, executive function and sensory filter.

So, executive function is that part of the brain that regulates, like, you shouldn't say that right now. Or you should say this right now. Or reading social situations. Your executive function is that part of your brain that regulates all of that. 

So she figures this is where she is. Her language skills are very advanced. Much better than average. But her sensory filter is much, much lower than average. Her executive function is roughly average. Her perception skills, much better than average. And her motor skills are much less than average. So for her, she's created this kind of profile of these 5 particular characteristics.

They're not "the" five characteristics that we would have for people with autism. They're just five that seemed like really convenient ones that people can easily understand. And I love this model. Because it's really not about you're either this or that. It's complicated.  It's messy. Right?

And I think about the same thing for vision. I have a friend with Stargardt syndrome. Which means he only has peripheral vision. He has no central vision, but he has some peripheral vision. So if you think of applying this spectrum model to vision, you might think of peripheral vision as one of the characteristics, central vision as another characteristics. The ability to perceive color. The ability to have stereo vision. Some people can only see with one eye, therefore, they're ... wow. You're blurry right now. Wait a second. I'll switch.

Stereo vision, you need to be able to see with both eyes and see 3 dimensions and have that depth of perception and depth of perception might be another factor that we take into account here. There's lots of different things that might make up somebody's visual profile.

We can apply that to many different types of, different types of disabilities or characteristics. So things do continue to get messy.

This is a little bit of a concept of the viewport. And I'll explain more what that means later. It goes along with us putting people in boxes. The view port is part of your browser that shows the webpage. I'm going to share this with you.

This is my father-in-law's desktop computer. A screenshot of his computer. And he passed away last summer. But when we were there, probably about … I don't know, 6 months to 9 months before he passed away, we were looking at this computer and I see things on here that scare me. And I don't really understand it. But I see here that he's got a new brief case icon. And then he's got a copy of a new brief case icon. He's got a copy 2 of the brief case icon. And he's also got a shortcut to a new brief case icon. He's got all of these things on his desktop. And I'm like .. Dude, what's going on here? Like I don't understand. And I'm looking at other things and other things scare me. He's got two copies of Apache on his desktop. Don't understand why. Shortcut to games. Shortcuts to Seahaven. And Seahaven 2. And Seahaven 3. And I'm looking at this and trying to understand it. And I don't get it.

Now, we'll talk about that in a moment. Can you tell what resolution that screen is just by looking at it?

**[Attendee guesses shouted out]**

**[Derek Featherstone]:** 800 by 600. Some people said 640 by 480. What size? Some of you don't know what 640 by 480 is.

**[Laughter]**

**[Derek Featherstone]:** That's totally good if you are actually in that place. What size monitor do you think it's on?

**[Attendee guesses]**

**[Derek Featherstone]:** Who said that? You've been to my presentation before? 27 inch monitor. At 832 by 623. I don't know why it's 832 by 623, but ... all those icons, all of those icons, the multiple copies, I start to realize as I watch him working on the computer, not only does he have low vision, and has this setting where he's at 832 by 624 in a 27 inch monitor, but he also has some dexterity issues 
because he's pushing 90.

And when he tries to double-click, when he's holding down the mouse, he tries to double-click with his left finger and his middle finger ends up tapping on the right-click as well. So he's double-clicking and dragging it at the same time accidentally moving by 10 pixels. And he's dragging right-clicking and letting go and it's creating shortcuts and doing all this stuff.

So he's not just somebody that has low vision. He's not just somebody with mobility and dexterity issues. He's got both of those things going on at the same time. He was also ... and you can imagine how this would be. He's also deaf in his left ear. He didn't drive anymore. His wife actually drove so she was in the driver seat and she's deaf in the right ear. And he was in the passenger seat and he's deaf in the left ear. And you can imagine what driving with them might have been like. They couldn't hear each other. So they were like, you know, yelling. And it just escalated and... wow! So, we think about putting people in boxes and we think about this person is blind or this person has low vision. And it's so not that simple.

People are going to have multiple things that impacts how they work on a computer in multiple ways. We cannot ... I'm going to get to the view port here. We cannot make assumptions about the device that somebody is on based on their view port. Now, he was at 832 by 624. If we were creating a responsive design for him, what size or what version of the site would he probably get? He would probably get the tablet type rendering. And he's not on the tablet. But we make assumptions all the time about the size and the view port somebody has and what device they're on. And it's so not that simple, right?

View port is not a proxy for anything. All it tells you is what's the visible size of this Window? And things are changing, you know,
changing all the time. IOS 9. We now have on iPads and iPad Pros. We have split screen capability, right? Something goes into a half screen, you've got a browser on there, maybe that's now getting a mobile view. You can even split it two-thirds, 1/3, three quarter on an iPad Pro. So it's a tablet, but maybe it's getting a mobile view port in that doc kind of stripped down on the side.

Viewpoint isn't a proxy for anything. We can't make assumptions about it. And that's becoming more and more prevalent to us. We were doing a series of usability tests right before Christmas. And we found 3 out of 8 screen reader users. And I want to think about this. 3 out of 8. That's close to 50%. 3 out of 8 screen reader users were on computers where they didn't have a monitor attached. We call it "headless browsing." They are working in a scenario where they don't have anybody that they live with. They don't need a monitor, right? They're using JAWS or VoiceOver or whatever it is. And they don't need a monitor.

So they're browsing in it, and it sounds weird every time I say it, they're browsing in a headless situation. And their screens look like this. This is our capture of their remote desktop. One of the things we find really interesting on Windows is when there's no monitor attached, instead of the screen being, because there's a virtual screen there, right? There's a virtual desktop even though it's not being displayed on the monitor. Not landscape, but it's portrait every time. That is some pretty significant impact.

This is a browser that's maximized on that portrait screen and you can see this big honking sidebar on the left-hand side. It's their favorite sidebar they didn't know it was open. But the visible portion, they're in a tablet layout. Because of responsive design. Responsive design is fantastic. But we have to keep in mind this responsive design or tablet layout is something somebody is now using their keyboard to go through. They're not necessarily on a tablet. We have to do more testing.

This is another one where, you know, their browser was actually half the width of the screen. This is real. Like we're not making this stuff up. This is real scenarios. The last one, we had to go in, this Window was I think 150 pixels by 150 pixels. We had to go in and make it a little bigger so we could actually ... as we were doing the remote session, we actually had to go in and resize it so we can even see what was going on and what they were interacting with.

So this stuff is not, like, these assumptions that we make about view port. That somebody is on mobile view and therefore using touch. It doesn't hold true. We need to do more. We have to test our mobile and tablet layouts and those breakpoints with the keyboard. We have to.

Disability is often a usability amplifier. And I am a big believer this happens in both in a positive direction and negative direction. We have done lots of work with people, people with disabilities and people without doing usability testing on the same product, same user tasks and we found time and time again that people with disabilities find the same usability problems as people without disabilities, but they find them faster and they're much more pronounced.

They're very much easier to see and kind of isolate in the interface than they would be for somebody that doesn't have a disability. Somebody that doesn't have a disability might just brush something off, and even though it slows them down by 2 seconds, they kind of move on. Somebody with a disability, that 2 second road block actually might become a 2 minute road block, or a 10 minute road block. It really depends on what it is.

We also see that making things better for somebody with a disability improves it for everyone. But maybe not to the same extent. So if I make a usability enhancement for me and it might help me get through something twice as fast, that same enhancement might help somebody that has a disability get through it ten times as fast. So we look at this and we see that disability is often a usability amplifier. We do this all the time.

All this stuff that you've taught us, yes, it makes it more accessible. But really, fundamentally, this is just a better design. Period. I'm a big believer in this. If we create things that work better for these extreme levels of ability, we're making things better for everyone.

You may have seen this stuff.  This is ... what is this? It's part of like Fast Company, the magazine? This is a design related publication. And this is from February 2006. Microsoft's radical bet on a new type of design thinking. Microsoft ... Microsoft is doing this. Google is doing this. Everybody is doing the things that we have been saying for 10-15 years now. They're doing it and making a huge splash with it. Anybody here work at Microsoft or Google? Okay, good. Cool.

But this was a big article about this radical new way of thinking. And Google is like, how designing for disabled people giving Google an edge! People are like, big companies are waking up to this now. This was in May of 2016. There's a lot of people that have been talking about this since like January 2001. Right? This has been going on for awfully long time and now people are waking up to it. It's actually kind of fantastic but at the same time, I wish we had gotten to this point much, much sooner. But the fact that Google is talking about this and Microsoft is, that's a big boom for us.

So couple of more examples and then we'll talk about some other things here. When we talk about designing for these extremes, I want you to think of this. This is an example I use very often and what we did with this straw test is to limit our view of the screens. So that's really kind of an extreme that we're expressing for that design. They're a pain. And if you were to try and work with this data table in a magnified scenario, because you have low vision, you might be faced with something like this. And your ability can be the entire scope of the table is kind of severely, you know, hampered by the fact you have that screen.

There's visual relationships that are created in data tables that maybe as low vision you're not going to see. But we can code this table of data so it works reasonably well for a screen reader user. But for someone with low vision, this might be really difficult. So we're zoomed in at this level, it's maybe 400%, and I'm on this table cell where it has a number 10 in it, but it's a lot of work for me as a magnifier user to figure out what it's about and come back down and then to go over to the left to figure out what those two pieces of data were.

Whereas, when I can see the entire thing, I can see here that this number 10 is Jupiter, and it's hours in the day for that planet. I can see that readily. Because I can see the whole table. But if I can't see that whole table, it becomes really much more difficult to do any comparison or data mining or whatever it is. So we start to play around with ideas like this. And that is functionality so that when you're magnified, you can actually pull those roads and column headers in so you can actually get that context. 

So I'll zoom it back out, so you can see that here's the entire table and as I click on a particular cell or hover over a cell, we get this little call to action to bring the row and column headers in, so that somebody that uses a magnifier has limited use the screen. We can pull those things in. It's some simple CSS and simple JavaScript. And I swear to you, and as I'm looking around the room and people nodding, oh, almost everybody that I showed this too says, I want that. And I can see the screen just fine.

Because we get stuck with dealing with tables like this that are pages and pages and pages long. I mean, that's just poor design for everybody. But the impact of that poor design is going to be more pronounced on people with different types of disabilities. So you know, what would this actually look like? Or how would that work here? That might actually be even more important. If we can, we always love to break up these big massive long tables into smaller chunks. Into smaller tables if we can. But we can't always do that.

So why don't we have a set of tools that allow us to do this. If you want to see an example of it, examples dot Simply Accessible dot com forward slash cell dash headers. There's variations on it as well that we've create that are slightly different. So we have a version where you could actually click and instead of bringing in one row header, you can actually bring in that entire, that entire column to bring that over. Or bring in that entire header row. So if you were magnified, you have the ability to kind of traverse the road or column much easier.

Now this was something that we kind of conceptualized and prototyped and put together quickly. It's not something I would say go out and take that code and put it on your tables and you're done. You would need to do work to do this, but almost everybody I showed this to says, because we deal with tons of financial data, right? Or we deal with annual reports. And we want to have that ability to do stuff like this. So this is the kind of thing that you can do when you start really think about what it means to have a limited view of the screen, and what impact that has on people with low vision. 

I'm going to share one more with you here. And this is a story about my dad. I want to ... I want people to design for extreme emotions as well. Several years ago, my parents, it's like a complicated story. So I'll tell it in a straightforward way as I can. So my father is like, he's now ... I don't remember how old he is. He's older than I am.

**[Laughter]**

**[Derek Featherstone]:** This is him and me together. He's the one with the sideburns. And you can tell it's the '70s because this lamp in the corner with that weird pattern and the spiral around the central. People would pay tons of dollar for a lamp like that right now and they would call it retro. I wish we still had it.

But my dad was a big burly dude. And there's a lot of things that have happened over time. And now he's older. And he's had a lot of things that happened. He had prostate cancer. And, so, he had a lot of treatment, he had hormone treatment. And he said, he's told me before, I'm very emotional about stuff now that he didn't use to ... Or he would say, maybe this is a little stereotypical and he was my dad and he was brought up in that age where boys don't cry, right? And, so, he's my dad.  So of course he doesn't cry. But he cries.  

Emotionally, he was being set off by certain things. He actually was at the point where he was in a very, very extreme emotional state. Because he was away on a cruise with my mom, and I had to call them, because his mom, my grandmother, had just passed away. I was trying to get them to book tickets to come back, because they needed to fly back off the cruise. And, so, he was ready to book the tickets, I ended up doing it with his credit card. Because he didn't want to do it. And I started to try to unpack why? And I said you guys should sign up.

We're Canadian, so Air Canada is our main airline. We have two airlines. That sounds really small. But Air Canada and West Canada our national airline and we can pretty much fly everywhere in the country. And you know, let's sign you up for Aeroplan, which is our frequent flyer program for Air Canada. And he didn't want to do it. He's like, I don't want to do it. I'm digging into why. 

I'm worried about how he bought an MP3 player. I won't say who it was from. But he went to register it online. Register for the warranty. My dad is the one of about 3 people in the world that actually go online and register warranty for things. And, so, he did that. And he was telling me about this form that he tried to fill in for the warranty. He said, I got through it all and I put the information in that I thought was right. And I thought everything was good. And I hit the submit button on it. And it came back. And it was basically a sea of red. And I'm like, what do you mean? And he said there's errors everywhere. And I froze. I didn't know what to do anymore.

And I said, What would have made it better? He said, well, I really felt if they knew all the errors were there, why wouldn't they tell me before I submitted the form ... he wouldn’t really say that. Before I hit the button on the form. Why didn't they tell me that before? Now it's like overwhelming.  It was too much. And he just, he lost every bit of confidence he had after this transaction. He wouldn't go back. And he wouldn't book those flights himself. He wouldn't sign up for Aeroplan, the loyalty program himself. 

He said when he did this, getting through these error messages, he felt like an idiot. Like, he's like, this is not a valid e-mail format. This is how he's seeing them. Password doesn't contain a special character. Neither does this one. [Sigh] How can you not know your name? This is how he's feeling. This data is not formatted correctly. Come on. I bet you won't even get this right. Yep. I was right. Seriously. Are you stupid? I can't wait for this to end. You're really not that smart. Odds are pretty slim on this one. Why do you use computers?

This is what he was feeling. Not quite in those words but that's what he felt the webpages were doing to him. This is my dad who doesn't cry, and webpages made my dad cry. They’ve made you cry probably for different reasons. But they made him cry too.
And I was like, totally shocked about this. And he went to fix this for 2 hours before he actually successfully got the form to go through. Because he was overthinking at this point. Error message, error message, fix that. And he couldn't get it done.

And my dad was like, my dad was from Canada. He didn't use computers. He's a mechanic. And now that he's retired, it's hard. And we kind of forget that. There are a lot of new people out there. So I want us to kind of think about all of these things. I want us to think about the extremes that people have to deal with. 

There's all scenarios, everything I've shared here today, they're scenarios that you would kind of question it and say, oh, that can't possibly have happened. Oh, that's like a one in whatever chance, right? Yeah, maybe my dad is a edge case. Or maybe your dad or mom too. The problem is, I like thinking about it this way. We say a lot of things in life. And as a teacher, I've said this,
to help one person, right? We're all excited. We give that so much weight. If I can have helped just one person and made a difference, then we're really ecstatic about that. And when we think about that one person that we actually created a barrier for, we don't give it nearly that much weight. But we're like doing the opposite. Like "Oh, its just one person."

So it's really, really something that we've kind of embraced all of these different scenarios, things that seemed like edge cases in many ways seems like the norm. The people out there that we're designing for and building for are so not like us. They really aren't. We need to really keep that in mind. And the whole idea here is that accessibility really is messy. 

These are things that ... you'll never see this stuff in a guideline, encapsulated all in a guideline. Do this, do this, do this. The real world, it's much more messy than that. I want you to be thinking about these things, like putting these extremes onto design problems and then solving them. What I want you ... you know, a lot of people that are new to accessibility go into it and they say things like this. There's only so much I can do. Scratch out the “only” word. And just go with there's so much I can do.

There's so many little things that you can do that make a huge difference for people with disabilities and how they use the web. I would love it if you would just go for it. I know. Some of you are doing this already. But I want you to think about some of the things that we talked about here as challenges that you haven't thought about before. Things you want to investigate more. How can you bring some of these things into your work? Doing the straw test on your wireframes and on your mockups, to look for those opportunities out there. And I want you to think about all of them.

I know I have successfully almost spoken until exactly 7:30. Which means I can't answer any questions at all.

**[Laughter]**

**[Derek Featherstone]:** Totally good. I am happy to kind of have really minimal discussion. Keep your questions to two words or less.

**[Laughter]**

**[Derek Featherstone]:** But I'd love to talk. And how long are we here?

**[Dennis Deacon]:** We have until 8, but, you know ... give or take.

**[Derek Featherstone]:** 8:03?

**[Dennis Deacon]:** We'll go for it.

**[Derek Featherstone]:** I would love to, if you want to ask questions, I'm happy to do that. And we can do it at this forum? So I'm happy to take a few questions now and just hang. Question, go ahead sir.

**[Attendee]:** First of all, thank you. I hear what you're saying having done adaptive tech work. At a help desk, where I had somebody once that said push the Windows keys. And they said what's that? You do have the extremes out the there. But I wanted to ask you, I do QA testing. But I'm totally blind. So my main focus is the screen reader. Are there things that I can do to maybe try to hit a few of these extremes a little bit more carefully? Things I should be listening for in that? It's really tough to cover all the basis. I feel like I can cover more.

**[Derek Featherstone]:** I know, do you use an iPad by any chance?

**[Attendee]:** I do, yes.

**[Derek Featherstone]:** One of the things that I love about the iPad and touchscreen, iOS touchscreen device. You have explore by touch. So even yourself, even though you're completely blind, you can explore by touch over the entire interface. By dragging your finger around, I don't know if you use it by touch very much. But that can easily show you some of these layout problems.

And one of the layout problems that we often see happens for people with low vision, I would look for very clearly ... change that. I would listen for on VoiceOver things like forms or content that appears to be in multiple columns. Multiple columns for someone with low vision can be a huge deal. The form button ... we see form buttons all the time that are down on the bottom left corner, bottom right corner of the interface, and they're like, always in the bottom right corner which seems really predictable and stuff.

But for someone that has low vision, if there's like massive amount of white space there, that button that's on the bottom right corner
might not be noticeable. You can, you know, it's obviously, there's a lot of more exploration that you can do there or you would need to do.

One of the things that is a huge issue is like mismatched ALT text. And when the ALT text on an image says one thing, but the actual text that's visible on it says another thing. It's creates issues for people that use Dragon NaturallySpeaking. Not that they can't get around it, but if this ... let me see what I'm trying to find.

**[Attendee]:** That one I have caught.

**[Derek Featherstone]:** Good. Mismatched ALT text can be really difficult. I'll show this desktop again. Pretend this desktop is a webpage. It's just a desktop. This is a link to Apache. Just assume for a second, that this was an image and the image says Apache on it. But beneath the hood the ALT text was OpenOffice.

If I'm looking at that screen, and I'm using voice recognition software, I'm going to say click "Apache." But if the ALT text underneath says Open Office, That's mismatched ALT text is actually ... Everybody thinks about ALT text as being like ... this is critical for people with visual impairment. Just as critical for people that use Dragon NaturallySpeaking. Particularly when things are images that are active. So if you're catching that, that's a huge boom.

The last one that I'll give you, and you're probably coming across this as a screen reader user. Things that look clickable, but aren't actually clickable. You can't tab to it. Or it's clickable, but it's a clickable div. It's not a button or a link. For someone that's using Dragon NaturallySpeaking, like there's ways around it, but that really slows them down, to click on these things that aren't natively focusable or clickable. 

So those, know that you're not just finding them for yourself, but you're finding them for every Dragon user out there as well. I'd love to talk with you more about that stuff because I love to put more thought into other things that you could find pretty readily. So, let's talk more about that. What's your name?

**[Attendee]:** Ray Campbell. I am a QA with United Airlines. I work with Dennis. Don't hold that against me.

**[Derek Featherstone]:** I wouldn't think of it. Question in the back.

**[Attendee]:** Text-to-speech, or speech-to-text in Dragon is from people that are focusing in on different aspects of accessibility and they find that to be the most challenging right now. [Indecipherable] And I'm trying to learn more about that.

**[Dennis]:** Could you repeat the question.

**[Derek Featherstone]:** The question was, you've heard about Dragon NaturallySpeaking. To kind of focus on that a little bit more, there's not a lot of info out there. What kind of resources are there? Is that good paraphrasing or not?

**[Attendee]:** Yes.

**[Derek Featherstone]:** There's not great resources out there, but what I would recommend you do, if you want to learn about Dragon, right now, it's $100. It is a piece of assistive technology that I would recommend that you go and try it out and learn about it and read through the documentation and learn about how it works. We write articles about it on our site, SimplyAccessible.com, so

But we just don't just write about Dragon, but we write about all the kind of disabilities we can and cover many types of disability, and there's lots of videos out there speaking in conferences and meet ups like this where I'm doing demos of Dragon. So you can certainly learn things there. 

The best part about building things that work for almost any assistive technology ... is make it simple. Use buttons. Use links.
Use straight up great quality HTML. And you can make things that you're building work very well, very easily, for a lot of assistive technology.

It's not simple as that, but in many ways it is as simple as that. So that clickable div, doesn't work for anybody that's just trying to use the keyboard. So using buttons and links that I can things hum. So think about that kind of stuff. As you're doing it. Because a lot of simple things you can do is, you don't really have to research. It's not like a core cut Dragon or anything like that. It's more, if we build it this way, it's going to be usable by the widest variety of people possible kind of thing. It really helps. 

If you have any other questions, feel free to get in touch. I'll put this up here too. Hang on a second before we finish. Just so you can get in touch. If you want to connect on Twitter, I'm @feather on Twitter. If you want to e-mail ... not me, because sometimes my Inboxes are like a black hole. Because certain reasons. So hello@simplyaccessible.com is a great way to get in touch and we often use the question that is come in as prompts to write an article about X. So if you have questions, we would love for you to ask them and we would often write about it.

So another question in the back?

**[Attendee]:** [Garbled]

**[Derek Featherstone]:** So to bring it together, ultimately the question from both of you is, how do you get people to go the extra edge or extra mile or whatever it is. Make it not anything extra. Our focus entirely is, we bake it in. So it's not seen as an optional thing. It's not like this thing that can be left. If we get to it, if we have time, great. Because guess what? As soon as it becomes a thing, if we have time to do it, we'll do it. There's never time to do it. Right?

If it's not baked in, you're kind of, like, we spend half of our time or at least half of our time not just helping teams fix things that are like websites, we actually spend a good chunk of our time, maybe three-quarters helping people fix their process, and fix their systems in the way that they work, and their mindset, so it's not ... never seen as an extra thing. It's actually just the way we do it. 

Kind of totally avoiding the question. But it's a big part of it is mindset. It's not an extra thing.  It's actually part of it. And we know lots of millennials that have disabilities. Loads of them. I don't know if you saw this, there's an article that came out not too long ago that younger generation in China right now, 75% of males between the age of 18 and 25, 75%. It's always been kind of like roughly 1/3 of the people. If you look at this room and we're probably geeky nerds that look at screens all day, we're probably slightly higher than say, 1/3 of people that need some kind of corrective eyewear. But in China right now, it's 18 to 25, there could be a different scenario, but 75% or more need glasses right now. So things are changing, right? There are things we can point to that say, for yourself now, but do it for your future self as well.

**[Attendee]:** [Garbled]

**[Derek Featherstone]:** Just to summarize that, a huge, huge part of this is education. Right? It has to be part of everything. And that makes it, you know, when we know what you're doing, it doesn't seem like a mountain. You know, much smaller chunks of work that needs to get done. So that education part of it is partial. It will surprise you, part of the reason that I'm here teaching and sharing things with you, because it helps bring the level up for everybody.

I used to be a high school teacher, and it's big part of what I do and it's a big part of what our mission is. We want to actually say this internally. Our mission is to go and make more believers. That this is important, that this matters. Currently, you don't get to work with us if you're not somebody that believes this is some of the most important work that anybody gets to do. 

And, so, our mission is to actually go up there and make more believers out of more people. Like, literally, that's it. If we can do that, then we know we're succeeding, because with that education level rises, we know how to do this. We can do this. All the teams that we work with, large and small, they get to a point where when they're working with us, it starts to click. It makes sense. And it becomes the way that they do things. When they have been doing it for long enough, you know, 6 months or a year or whatever it is, they don't need that checklist anymore. They need that list at the beginning because they don't know where to start. But that disappears and it goes away, because you build it into your practice.

You build things like pattern libraries that has accessibility built in. They have color palettes that are free vetted for color contrast so you have color combinations that work. You don't even have to test them out until the next time you rebrand. So that education is critical. And I mentioned this, I would be absolutely silly to not do this with such a captive audience here. If you're interested in the kinds of things that we do, and Dennis actually reminded me to do this before.

We need people.
SAteach.es/jobs
We're hiring testers and consultants.

Here's the cool thing.  We have a US company too. Patrick works for us and he works in Chicago. Elle works for us and she's in Louisville Kentucky and we have people in Vancouver, Nova Scotia, Philippines, Ottawa, Seattle. Hawaii. Hawaii! How cool is that? People work for us and the entire team is remote. We can talk about all that kind of stuff, too, afterwards. Elle, is this a comment or question?

**[Attendee]:** Garbled

**[Derek Featherstone]:** Yeah, this quote, all this stuff you've taught us, yes, make this more accessible. But really, fundamentally, this is just a better design, period. Four years ago, in this office, we were doing training, some workshops for Critical Mass designers and developers, and part management types, and they were working with us as partners for Humana. So we were working for Humana. Do you want to tell this part of the story? 

Elle worked for Humana. She ran the accessibility program at Humana and Critical Mass was hired as part of the team to do this big redesign. We were Simply Accessible hired to be part of the team. And this happened, Critical Mass, the lead designer, after a full day workshop with us, after looking at all these examples, she actually came up with this. And she said, all this stuff you've taught us, yes, you made it more accessible. But you've just made it better design.  Period. I was like, this moment where, I was like, oh, my God! They got it! It was like, mission accomplished! Because that was exactly what we believe in and we've seen time and time again. So this is pretty, kind of, fun to be able to be here and talk about it. It happened right here.

**[Attendee]:** I'll give you another one. That is, the more education we do, the more likely we'll put people like you out of business. Because everybody will get it.

**[Derek Featherstone]:** Yeah ... I have mix feelings about that.

**[Laughter]**

**[Derek Featherstone]** We actually say this.  A little insight into our work. We actually say with every client, our goal is that by the end of it, you don't need us anymore. Well, you still want to work with us because we're fun and stuff, but if things go well, you don't need us anymore. And we're good with that.

**[Attendee]:** [Garbled]

**[Derek Featherstone]:** I'll summarize again for the captioning. It was a magical time, definitely. And for the UX team to feel like it was something that, it's earned and created a need for innovation. And it wasn't something that was hampering people. It was like we can do better and we can do this. It sparked a lot of creativity in the solutions that we’ve created. And, so, it was a special time. We did put -- absolutely put the user first as a fundamental requirement. It was a requirement, and not just because Elle said so.

It was a requirement because there were regulations that say, but we did ... I kind of get goosebumps thinking about it. Because Elle straight up said, we're putting together this team, and it was, it was exactly that. A team that said, “good enough isn't enough.”  Period. And that was, it was awesome. It was awesome! It was pretty amazing. And now she works with us. Yeah.

**[Attendee]:** What are some requirements in the United States?

**[Attendee]:** If DOJ gets off their butts and release it.

**[Attendee]:** [Garbled]

**[Derek Featherstone]:** She's typing all of this up. I'll just summarize in text. Because the conversation in the back doesn't come through for the live captioning. So I was summarizing bunch of things but I got tired talking so I typed it instead.

Cool. You just want to have Bourbon or do you have any more questions? I'm not going to force anybody.  But we've got, we're here for a little bit longer. I'm happy to just go around and chat. I would love to talk with you. And thank you so much for being here.

**[Applause]**
