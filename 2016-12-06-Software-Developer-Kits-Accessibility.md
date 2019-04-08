# Software Developer Kits & Accessibility
## Thomas Logan - Tuesday, December 6, 2016
[Source recording](https://www.youtube.com/watch?v=Csh3G2bdBMk)

**[Thomas]:** Thank you. Hello, everyone.

**[Applause]**

**[Thomas]:** That video made me a bit emotional, too. I hadn't actually seen that video yet, but I had known that Apple started their keynote this year with a sequence of videos. And it was, you know, really exciting to me to see, you know, the CEO of the world's most powerful corporation, the richest corporation, starting off their presentation talking about accessibility. It does really speak to the fact that we are at a time where change is happening.

I started working accessibility in 2001. I was a computer science student in North Carolina, Chapel Hill. So Michael Jordan here in Chicago. I'm a big fan.

So I started in computer science, and I worked with a blind student in the classics department. He was working with ancient world maps which are inherently visual. And so that was my first exposure to thinking about accessibility as someone new to computer science. Like, wow, this is actually something where with technology we can make information accessible to someone else. So my project at that time was how do we make a map explored through touch and sound. That's what got me interested, you know, in this whole world of accessibility.

Right after that I actually got a job at Microsoft. So speaking tonight about accessibility software development kits, it's kind of close to me because it's kind of full circle for me. That's really the first corporate job I had in accessibility is working on a software development kit. I worked on Microsoft UI automation which is a way to make software applications accessible on the Windows platform.

And, you know, it's funny for me just to go back in time and look at me coming out of college, really just I've only worked with this one student that was in the computer science department, learned from the experience of that project. And then there I was working on a software development kit at that time one of the largest companies really to understand what are the things that need to be in a software development kit for accessibility.

So tonight, you know, it's really ... I'm kind of highlighting a lot of the different things that I've seen in the current software development kits. It's coming from both the point of view of let's look at what's really interesting and great in each one of these kits but also sort of a bit of let's look at the big picture of why does each software development kit need to have each of these unique things.

You know, I'm kind of coming from a viewpoint now working as long as I have in this field that we really do better working collaboratively and working together. So part of my viewpoint even talking about these kits is how can we sort of bring these together, like why do we need to think of making application accessible on Android as something, you know, kind of very different from making it accessible on iOS or on Microsoft.

So a couple of other things. I'm @techthomas on Twitter. I'm not as prolific as Dennis on Twitter but I try to be. I have a company called Equal Entry. My whole career is working on making technology accessible. Right as I say that, my Chrome crashes. That's a different kind of accessibility.

So tonight I'm a big person.  I do a lot of presentations, so I'm very much into what are my three key takeaways. I'm going to start with them and end with them.

My first key takeaway is I think accessibility software development kits should strive for more consistency between implementations. I think it's not doing a service to accessibility to have these concepts that are all in theory exactly the same concepts be expressed different ways on each platform. You know, I'm someone that's, like, looking at virtual reality now as, like, okay, my partner actually works on a virtual reality platform. I don't want virtual reality to be something that we're waiting like five years after people start working in these new experiences to make it accessible. I'm already thinking from that viewpoint, like, let's learn from everything that's been done already in the software development kits. And as new technologies continue to come out, try to make these things more consistent.

Second is I think accessibility software developer kits, when we make them, we should have at least one real example demonstration of how to properly use the functionality in it. I've worked with the W3C. I've worked on the Accessible Rich Internet Specification. I've read a lot of the specifications. Frequently, you know, for me I'm always thinking, wow, we always document these API calls, things developers should do. We don't exactly explain end-to-end how it would work. Like, the video that we watched at the very beginning tonight, it's very powerful. You know, we're seeing things happening. I guess that was Final Cut Pro, or iMovie. It was Final Cut Pro. Right, it's very interesting if you can connect the experience of what did the developer do in the Apple SDK to make that functionality work for using the head switch that allowed that movie to be created. 

A lot of times when we look at the documentation for the developer kits, they don't actually connect the experience end-to-end. So that's something that I'm very passionate about. That's a lot of the work that I do at Equal Entry. I do a lot of work with SSB Bart Group. Erica Zelmanowicz is here from them. I have worked a lot on creating these demonstration videos. Here's what actually happens if you implement the work. I think that's something software development kits should do more of. Looking at what Apple already showed, that can be a followup. Ok, so how did that actually work? What needed to happen to make Final Cut Pro work that way so she could create that awesome video?

And then, lastly, I think software development kits need to demonstrate more accessibility implementations throughout. So, you know, worked in this field a long time. Building up a sample as someone that doesn't work for Apple or work for Google, you know, I really or anyone working in this field, we only have so much time to build sample code to show people how to make something to be accessible. It's much better and what I have been trying to do more lately is look at what's already been shipped by Google or Apple or Microsoft and say, well how do we implement your accessibility API in the samples that you're teaching developers how to use?

So what I will be demonstrating today ... most of them have one sample. At least each SDK will have an accessibility sample that shows you here's how we implement our API. But unfortunately all the rest of the samples which could have implemented the API and have been further evidence for developers of how to implement accessibility, they're just missing that work. So if I was a developer learning from a different part of the SDK and I download that sample, I'm like, grabbing something and starting from something that doesn't have accessibility built into it.

So my point of view is we should be advocating or if we're working in a place where we can make that change, let's put more accessibility implementations into every developer sample we put out because a lot of developers work by cutting and pasting, at least I work that way. And so that's something that, you know, if people are cutting and pasting accessible solutions, now they already have those attributes in their code. They already know that kind of needs to be there. If it's not in the sample code they're cutting and pasting from, there's no real push for them to add that in. They have to actually go that extra step and download the accessibility SDK.

Those are my three main points. The rest of my presentation today is really a whole bunch of demos which is dangerous so we'll see how far.

**[Attendee]:** It's brave.

**[Thomas]:** It's brave. We'll see how far each of those goes. We'll basically start with Apple. I think it's great we started with the Apple presentation. I really think Apple has just done so much to demonstrate, you know, really going above and beyond. The one that I usually show that was in that video is using the camera and actually hearing that someone's face is in the view finder. You know, that's not something legally required from Section 508 or WCAG 2.0 or the jargon if you work in the accessibility industry we see. There's no mandate to add that to a consumer product.

But Apple doing that, you know, it's such a powerful thing. Who doesn't want to take a photo of their family or share that on social media. It's a really good example. It's cool to see that in there. I do think Apple has done a lot to really go beyond and do more. I think that's what all companies should be doing. It's definitely paid off for Apple with the loyalty of consumers really flocking to their platform.

All right.  So let's start  ... actually, I forgot. The first thing that I'm talking about, this is just one example. I could have picked a million different examples of APIs. But let's start with the most basic.

Images need to have a text alternative. If you started in the very earliest days of Web 1.0, the image tag had alt attribute and we would tell developers that every image needs to have an alt attribute and you need to fill that out. It's 2016. You can still find and scan most websites where that's not being done perfectly correctly. You know, you look at that, that's HTML. We're calling that concept that an image needs a text alternative an alt attribute.

These are three more examples just to show you how dramatically different APIs refer to that same base concept. Like, we're saying let's give a description, let's give a label to something that's not text on the page. Microsoft has a property called UI automation or has a platform called UI automation and their property is called the name property field. So if you are working on Windows and you're building an application that needs to provide a text alternative for an image, you would need to go into your code and set AutomationElement.NameProperty equals the description of the image.

If you are on Android and you are building an Android mobile application, Android has called this exact same content a content description. Android has a whole bunch of well meaning and well written information of how to add a content description to an image that's put on an Android phone. Conceptually, it's exactly the same thing. We're giving a text description of an image. But, you know, from a thought process or for a developer, we're making this harder. 

It's the exact same thing that needs to be done for accessibility. But because we call it something dramatically different, we don't really let people transfer that knowledge as easily between platforms. And the longer you work in technology, the more you cycle through these platforms. You just sort of start getting frustrated, why do I need to relearn some of these concepts. And now accessibility is a base concept. Android has a lot of great information. So just calling out this page, pretty well built out, lots of different information of how to properly add the content description.

And then the last one is iOS. They call their property the accessibility label. So this would be if I'm building an iOS application and I put an image in iOS application. I would need to go and look and set accessibility label to provide that information. Now, if I was hosting a Web view inside of my iOS application, I might need to set aria-label because I'm building a Rich Internet Application. Maybe that's a little bit closer, accessibility label and aria label. But on Android and that means you were setting content description and you are setting aria-label, all the exact same concept. I just picked that as one.

We could go into a million other properties, setting roles, states, values. These are all part of Web Content Accessibility Guidelines. They are all expressed usually differently on each platform. So just multiply this one property times all the things we want developers to do correctly. You can see we're adding a lot of complexity.

I think that's my first key takeaway. If we could get, you know, as a group to either, one, work more collaboratively you know, it's very hard to work from consensus. I have only worked for a year with the W3C because I realized getting consensus is very difficult. I do think that's something we should advocate for as a group of people working in technology. The more consensus there is on these concepts, the easier it will be for someone to implement them. And I think about property like a border or a margin or an outline, those properties are pretty much referred very similarly across technology platforms. It's more when we get into things that have, like accessibility that hasn't had as much of a pattern practice to it. All right. So that's the first point.

All right. So then the next one is now I'm just going to look at three platforms just with the time we have, try to do a bunch of demos, but show you what is currently available and hopefully teach you some neat things that are on each platform.

The first one for Apple, we'll start with Apple. They have a whole portal page for the developers. It's an accessibility portal page. We can read about accessibility on iOS. We can see lots of different areas. It's very nicely designed. We can go to captioning and audio descriptions, how to use voiceover. And then we have a bunch of developer resources that they link to. And so they do a great job of all of the videos from their different annual conferences for developers that they did a topic on accessibility are available, at least going back to 2012.

So if you are interested, just from this development link, you can already watch some pretty high quality multimedia content of Apple developers or product managers teaching you how to do accessibility correctly. You can also go into the UI accessibility protocol which this is the main way that we implement accessibility in an Apple iPhone/iOS application. So, again, this is pretty well documented.

One of the concepts that I call out is that we could go and read about these different properties, and each one has a pretty good written description but not necessarily that end-to-end visual description I was talking about. Like, I think it would be cool that somewhere in one of these properties, the functionality that we saw in the Final Cut video, it would actually say, for example, if you want to understand how this trait or this property works in practice, like, this is how it worked in Final Cut.

So I'm going to click on traits just to call this one out as a place to look. These are a bunch of different traits that you can set in their accessibility API. And maybe some of them we read and we say, okay, I know what that should sound like when assistive technologies interact with it. Like UI accessibility trait selected, okay, yeah, if I have a selection state in my application, I want to express that an element is selected and probably voiceover on that screen reader reads it, it will read out to the user that element is selected.

But there's other ones like UI accessibility trait updates frequently. Like, I read this one and it says, okay, this element updates very frequently. If the label or value too often to send update notifications include this trait when you want an assistive application to avoid handling continual notifications and instead poll for changes when it needs updated information.

For example, you might use this trait to characterize the readout of a stopwatch. So, okay, you could use the timer stopwatch app on the iOS platform. But I still don't really know what's the correct behavior. Like, what does voiceover do now that I have set that property? Does it just read every minute, it polls it and reads it out? It's kind of hard to know exactly if I did start using this in my own application what it supposed to do. I think that's the barrier we have in a lot of APIs, is we don't actually explain the other side of it. We tell developers to set these traits.

But what is the assistive technology supposed to do with that information when they consume it? I know we can't prescribe and set every single case of how they should use it. But I think something more representative of an end-to-end sample, that it really shows well with the stopwatch voiceover does this. That would really help illustrate the principle more. So that's the UI accessibility traits.

I do call out here the two really good examples that Apple has built for developers. There's Custom Content Accessibility, and then HelloGoodbye. I'm going to try to hook up my iPhone now to show you guys HelloGoodbye. This is just another example where it's more just taking the documentation further. Maybe some of us in the room, you may have never seen this example. But you would actually benefit from knowing what are the things it shows me how to implement.

So right now the Apple expectation is that we download the SDK. We can download the sample code, load it into X code, build it on our phone. But hopefully what I will be able to show is just demonstrate what it's trying to show you that's good for accessibility.

Here's a free tip if you run ... if you have an Apple platform. You can actually turn on Quicktime, select your iPhone, and that's a really cheap and free way to display what you're iPhone is displaying to a room or for a presentation.

So on this I have downloaded HelloGoodbye. And so one of the things that HelloGoodbye was implemented, so it was like, I think I like this, it's a pretty, fully built out sample. One of the other points I said is, If I was building a sample for iOS to teach you accessibility concepts, maybe mine wouldn't look quite as nice, wouldn't be as quite realistic.

They are trying to build like a Tinder clone, or an OkCupid clone, you know, online dating. They took a pretty realistic app that lots of developers are trying to build, and they put accessibility implementations into it. So some of the things that it does is on the ... on your profile page showing you how ...

**[Voiceover Screen Reader]:** 37 adjustable

**[Thomas]:** So on this one, it is showing you how to use  using the adjustable trait. So adjustable trait is for a slider or something that can have a number go up and down. This is showing, okay, I'm setting how old I am by actually doing the slide up, slide down.

**[Voiceover Screen Reader]:** 38, 39, 40, 41, 42, 40, 38

**[Thomas]:** I don't know if I want to tell you guys how old I am. But um, we will ... this is an example of, all right, slider is not something that's always really clearly understood how do you make that accessible. A lot of apps that don't follow this pattern, they're not accessible. Like, they don't actually have the slide up and down to adjust it. So for a screenreader, they don't have a way to get to that and navigate it. In this sample, that was one of the ideas to build accessibility.

**[Voiceover Screen Reader]:** HelloGoodbye.  Hello.  Matches.  HelloGoodbye.  Back button.  Matches. Slide up to say hello.  Slide down to say goodbye.

**[Thomas]:** This one is showing actually visually displaying instructions of it's like the swipe right or swipe left from Tinder I think. But this is swipe up and swipe down, Hello and Goodbye.

**[Voiceover Screen Reader]:** Profile photo. Image.

**[Attendee]:** How did you navigate to that?

**[Thomas]:** So this one, with Voiceover, it's swipe right to go to the next element, swipe left to go to the previous element. What this example was showing is we have a somewhat rich UI. You know, it's not as rich as what we see in the apps, but it shows we have a label for the photo. We can move sequentially through the content.

**[Voiceover Screen Reader]:** Travel.

**[Thomas]:** And this one is actually  oh. You know, one way that people frequently make mistakes with accessibility is it might read age, hobbies, then 32, then cooking bubble tea with friends, travel. That's hard to understand. So this was to show the proper implementation that it actually reads age, and it reads 32. It reads hobbies, and then it reads cooking bubbles. A lot of those things you have to learn going through the sample code and building it out.

But having that also illustrated in the SDK, you know, where people don't have to go and download and build it, maybe a product manager or program manager or designer just wants to know the right behavior of these traits. They've already built this example. Right now it's kind of a little bit walled off that you have to download, build it, and play around with it to illustrate these.

**[Voiceover Screen Reader]:** Voiceover off.

**[Thomas]:** The other things that are interesting with this sample, so I think these are exciting sort of features that are coming and they're enabled on mobile platforms. But developers do have a way to detect if people are running different accessibility features on the iPhone. So this sample let's you see, for example, if I select bold text, this is actually going to reboot my phone a little bit. But when you use bold text on your phone, it makes applications that support that have a stronger contrast. It's easier to see.

So this application, it might be a little hard to see without seeing it side by side. But it actually swaps out a bold font when the user sets that. So without that setting on, it's a little lower contrast. And maybe for some designers or design scenarios you don't want to have a bold font. But this app is showing that you can actually have two different presentations. You can detect if a user has that bold setting set on their phone. And then you can re-render the application that way.

The only one I was going to call out here because I kind of react to this one quite a bit is animation, is becoming more back on trend and putting into interfaces. And so there is ... I have that actually set on right now. But you can reduce the motion of the user interface. So this app actually illustrates how to use or properly detect, reduce motion.

This application, if I turn off "reduce motion," again, a little hard to see without doing this side by side. But, you know, when we're dismissing people that we either, you know, like them or don't like them, this animation happens much faster when reduced motion is turned off. So for someone who actually has maybe a type of disability where motion is either distracting or could be a vestibular disorder, this app shows you if you can set that setting, you can actually decrease the animation and make it slower, make it less jarring.

So that is basically that was an app that they built, right, that was really good. Like, that's the one that they tell people let's go build an accessible app. Let's implement it.

So now this is me kind of calling out Apple a little bit, that you go and get a different app from their SDK. They build an app for displaying a periodic table of elements. And they build that app more to train developers how to ... oh, let's see. You know, it's showing you a model view controller. We're having, you know, how to do configuring and responding selections in a tab bar, displaying information in a table view, using navigation controllers. There's, like, a whole bunch of things they're teaching you how to do in their accessibility ... sorry, in their API.

The problem is they are not actually implementing accessibility in the sample. So if the developer hadn't downloaded that HelloGoodbye sample but they were interested in learning these concepts from the element sample, it doesn't have that implemented. So I'm just going to show that.

So I made two. So I have fixed one, and this is the default one that comes in the API. So the default one, some of the critiques of what's being taught here is that this application when we spin it around and when we view information about the periodic table of the elements, the contrast of the text. So depending on the ones that we select, the contrast for, like, the link to view the hyperlink out there, it's not very good. So, you know, we could say, well, that's not the point of showing this sample. But it is if we want people to always be building accessible apps, even just having, you know, a sample that lots of people are learning from that doesn't illustrate that concept is problematic. 

Another one is if I turn on Voiceover ...

**[Voiceover Screen Reader]:** Button. Tag button. Button. Wikipedia.

**[Thomas]:** I'm going to swipe left and right.

**[Voiceover Screen Reader]:** Button. Tag button. Button. Wikipedia.

**[Thomas]:** So on this screen all we hear is back button, button, and view at Wikipedia. So the actual information, the information about the atomic weight, what element is being displayed, none of that information is exposed in this sample. So again, if I was building a card view, you could put anything into maybe you're like.

**[Voiceover Screen Reader]:** Alert accessibility.

**[Thomas]:** When I saw it, I'm like this is kind of a slick animation to turn the card over. But if someone just took this card, added their own information into it, it's already built not implementing accessibility. So I'm just going to show, because we don't have time to go fully into all of these.

This was one where... turn off the contrast here ... So darken colors, if you didn't know, darken colors is how we set a high contrast theme on the iPhone. Kind of another point, most platforms call that high contrast theme. High contrast is somewhere in the language. In the language of iPhone, it's actually called darken colors.

It really does potentially give the same possibility for a developer to say if someone has darken colors on, I'm going to present a high contrast theme. That's really taking a leap of understanding of accessibility to really get there that this is what that means. I'm going to turn that one off just for right now.

**[Voiceover Screen Reader]:** Voice over off.  A11Y The elements. Back button. Americium. Atomic weight. 243. State.  Artificial. 7. Discover. 1944 A.D.

**[Thomas]:** So in this concept, I'm showing you... that's... actually a sorry. To really nail down giving a live presentation and having a screenreader talking...

**[Laughter]**

**[Thomas]:** It's quite a juxtaposition. One of the things I'm trying to illustrate that's in every API is you don't ever want each one of these pieces of text to be, like, separate, navigable elements.

One of the basic principals is trying to group together information. All the APIs will have documentation explaining that concept. I saw this one as a perfect example as there's really no benefit, at least in this scenario making one swipe right go to the period, one swipe right go to the group, one swipe right go to discover. We can group that information together and make it just one hit target or one selection state.

So, again, it's just looking at all the different samples that Apple has built, that was sort of my thought process when I had to work on how do I show people in my trainings to make an accessible app rather than build my own app. I took the Apple SDK for the periodic table of elements and just added those techniques in. But that's something I am planning to report back to Apple, hopefully incorporate. I would really like more and more samples to have those illustrative points.

All right. So now I'll go off of Apple, switching to Android. Let's talk about some good things in Android. First, you know, Android has very complete accessibility SDK. One of the things that I think is the most interesting with Android is they have actually... they have a bunch of different ways to view and interpret the information. But on their developer screen, they actually have... way more documentation, step by step, of things that you should do.

And then they even have a course that they've built that's like a step-by-step course for people to follow on at home. So rather than only having a video or only having a SDK, they have an iterative sample where you follow along and you build out the sample as you go. So you download it. You make these changes. And then you keep working with it and they tell you if you're doing things right or wrong. So I do think, you know, documentation, if anyone here in the room does work on the documentation team, that's something that I think Android and Google is probably doing the most for trying to document more interactive code samples.

They've also done a lot of video trainings. So on Udacity which is also something that Google works a lot with, Google has a really extensive Web accessibility course that's available for free. And that's something that, you know, I think really supports the work that they have been doing on Android. So here's the app, sorry, the training. So you can see they have 13 different modules.

This is the codelabs.developer.Google. And this is basic Android accessibility. You can really step through this at your own pace. And again, it has all of the different types of steps that you would expect from an accessibility training. They tell you how to download the code. You start off working in Android Studio. There are steps for enabling Talkback. They have done a lot on that side to make it more than just download a SDK sample. I think those are all good things to applaud.

All right. So the basic accessibility ... all right. I'm going to try something here to switch to the other ... So on the Android, at least I don't know if something as fast as using Quicktime, to display your phone, so I use a paid client called Reflector. Reflector needs you to be on the same WiFi network to work. We'll see if they will work. We got it. All right. Well, just to keep it moving because this is live, I did record this prior to coming. That's another pro tip.  It's always good to record it before you go.

**[Attendee]:** Finding it...

**[Thomas]:** Right, finding it. It should be in something labeled. Accessibility Chicago. Have a good label. And this is ... basically I think the thing I want to call out that I thought was a little bit of a negative here is that so Android sample that you download from their SDK, if you compare that to what Apple did, this isn't a real app. This is probably more what I think I traditionally in accessibility samples where, of course, there's value in teaching us the techniques. But it's not as illustrative for a developer end-to-end especially if you look at, again, going back to the fist video that was shown.

You really see the impact, like, why did I implement accessibility? Like, that person was now able to edit a video and this is how it all connects. I mean, it's nothing wrong with building a sample like this. It's just not as exciting or illustrative of why accessibility is important. So you step through and you set different information that's available in the API. But you can't actually really see end-to-end why that was important because it's not a real application.

And then the last thing that I'll call out that's just another ding to me for Android is that, you know, there are a lot of conventions that have been built up for accessibility APIs. And one of the most important ones, I think, is that accessible labels or accessible names, they need to get associated with controls. And that's something that in the documentation at least for how you set up, like, this custom dial, they're just using the label "custom view."

You also know this is Talkback showing what it's reading. It doesn't actually associate the label with the dials. So from even just in the accessibility sample, it doesn't really follow the conventions of what would normally be in an accessibility sample. And part of my question is that might be because the people don't work in a large enough group of comparing work across different platforms.

There might be other reasons why that's implemented that way in Android. It's not explained and for someone who works in accessibility quite a lot, it's a noticeable difference in the way their API doesn't have the ability to do that versus the other APIs. And I will say another thing that I think is really good  and this is funny because now I don't have to actually have the screenreader reading out, but seeing "discard" buttons, the Android has a way to display what the speech synthesizer is speaking in its view.

Voiceover running on iOS does not. If you are working collaborative with a developer and want to show them a bug, it's much easier having this visual display. This one is trying to show us it's stuttering saying discard button button. A screenreader just needs to hear discard button. I can actually take a screen shot, you know, using Android's Talkback because it does have the visual display. And if I'm working with someone, a developer, to show them the problem, it's easier to communicate the problem on this platform because we have that visual display of what the screenreader is speaking.

**[Dennis]:** Time check. We have about five more minutes.

**[Thomas]:** Perfect. So why not transition to Microsoft? Save the best or worst for last, depending on your opinions of each of these companies. So Microsoft, again, doing a great job on accessibility. You know, I started when I did start working accessibility, I was really excited to work for Microsoft because they actually had an accessibility team.

So if you go back to 2002 when I graduated, it was not something like it is today where people had these accessibility groups so you could go and work in. So for a long time, Microsoft has been committed to working on accessibility and making progress there. So just want to show that they also have a developer portal. 

So all of the three main, you know, technology platform companies that I see, they all have these developer portals for accessibility. Microsoft's is also more heavily focused on video training, video illustrations of how to do things. And they similarly have sample code that you can download, different things that you can do to play around with accessibility. I will just call out the example I showed of Apple having SDK samples that aren't accessible. That applies for Google and Microsoft too.

The majority of the samples don't have accessibility built into them. Unless you go to their developer accessibility portal and download the accessibility sample, you don't learn the techniques. The thing I wanted to demonstrate and I learned this very recently, how many people have used Microsoft Edge in the room? One, two, three, four. A smaller percentage.

What's Microsoft trying to shift to for their new browser, for their new Web experience? So one of the things, I will just do parallels quickly. But Edge has a cool future for viewing the accessibility tree. And I guess I just wanted to make sure I showed at least one good thing from each of these three companies. And this is pretty cool.

Like, the accessibility tree has always been, you know, if you work in accessibility, visualizing the accessibility tree, making sure accessible elements that there's not too many in the tree. That's always a part of all the different platforms. But they don't make it easy to see the tree.

In Microsoft Edge, you can actually pull up the developer tools. And the accessibility tree is available from this accessibility icon. That will let you navigate through the tree of elements and see the different elements that are in the trees. I can see that there's hyperlinks in my presentation. I can see that there are headings in my presentation. I can see there's an element marked description which is what  because we have the highlighting, we can see that Microsoft Edge maps the block, quote, element to a description element in UI automation.

So this is something very important. This is really talking about Web accessibility. I was talking about mobile accessibility before. But if you look at Safari running on the Mac or you look at Google Chrome running on Mac or Windows, they don't have an easy way to visualize this tree. You have to download other tools. I think this is great Microsoft building that into the browser. It's making it more present for developers that need to do this work. Like, why make someone download another tool to do accessibility?

So let's look at that as a great example that hopefully gets emulated in the other browsers because if you have done a lot of work on developing accessibility, the tree is, like, a very important concept on any platform for making it accessible.

So to wrap up, go back to my ... Well, I don't need to.  But I will use them from memory. The three points I was talking about here that we need to have a more robust set of developer examples for accessibility. Ideally, every developer sample in a SDK has accessibility built in. We should have more implementations for anything we put into an accessibility SDK. We should show how it works end-to-end. So we should make it really clear what the benefits are. Why is a developer doing that, and what's it supposed to look like with assistive technology. And, lastly, we should have more consistent naming. We should not make it confusing that, you know, we're giving a text alternative for an image having totally different names on each platform. That's more difficult.

Those are my three points. I would like to wrap up. Thank you for the attention and then have some Q&A here at the end just for a few minutes. Thank you.

**[Applause]**

**[Dennis]:** What I will do as people have questions, I will actually hand you the mic. Anyone have any questions?

**[Attendee]:** I was surprised ... first of all, thank you very much for your presentation. I was surprised to find or to know that Microsoft even did accessibility for so long. Why is it that Apple seems to be the winner of accessible platform?

**[Thomas]:** Well, one thing that I do think is very interesting at least I can share from the Microsoft experience I had was that if we look at just the screenreader perspective, so people with vision impairments, Narrator, the screenreader that's built into the Windows platform had never been advertised by Microsoft as a screenreader replacement.

And so I think that's been a big difficulty for them, that they're now, you know, addressing because Apple does build in a screenreader that works fully, you know, really you can't install other screen readers on the iPhone, for example. So Apple was able to get that to work much more consistently. I mean, that's one simple example. 

I think that's something Microsoft still needs to continue working on, is that Narrator which is the screenreader they ship on their platform, needs to be a full-featured screenreader. It should be able to be able to fully implement it. That's one. And I think it's really just taking on mobile. I think it's really just the end-to-end, makes interfaces simpler, easier to use. I look at the accessibility SDK from Microsoft. It's got a lot more options in it, but it was trying to support a lot more functionality that's available on the desktop.

And so mobile I think you could still say Apple is not necessarily as great on the desktop for accessibility as Microsoft is. But on mobile, Apple did so much more. And, also, to ding Microsoft on the Windows phone, that shipped without accessibility. That's a huge embarrassment. That's not ... no new technology should ship without an accessibility implementation. And so Apple is shown with the watch and the TV that we are really committed. I think they have really, I think, won that argument that no one should be releasing products that don't have accessibility built in. So other companies should follow and do that.

**[Attendee]:** You talked about other things where you are working with UI controls and things like that. How would you say for Open GL for a game, are there ways you can still utilize the operating system's built-in features?

**[Thomas]:** I think that's a good question. That's a little bit where I was going with talking about the virtual reality stuff. You know, unfortunately there's not like these primitives or elements. I mean, if I look at Unity in building an application in that interface, they do have the elements and objects we could add properties on.

I think in OpenGL we would have to almost build that structure yourself. I don't think there is the higher level tree or, like, set of elements you can add those objects on to. I mean, that's something I don't actually know a ton about the OpenGL development space. But there should be. I mean, that's the point. Like, any developer environment, so I had just pick on Unity because that's the one I'm most familiar with, there should be a way in Unity to set accessibility attributes and add that information.

It shouldn't all be on developers to build the underlying backend. I do think that's most of the way games have been made accessible in the past, is that people build up just like a structure that maps to the game and almost like it's hidden behind the game. And they have had to basically just rebuild the whole interface from scratch.

**[Dennis]:** We have time for one more question, if there is one more.

**[Attendee]:** If we're talking about preaching the Apple accessibility, what do you think needs to be done? Developers usually think of accessibility as something rather second rate. [Indiscernible]

**[Thomas]:** Lots of different ideas. I guess one idea that I think is a community, making sure that we either file bugs or add on to bugs that have been filed, I mean, I know that a lot of companies, they have people that work for a company. But if people aren't presenting it as a problem or logging things as a problem, then they don't have anything to go to their executive team or management team to say, hey, this is a problem.

So definitely one is that I think if you are working in the capacity where you find bugs, like you log them on to people that are responsible. I think the other one is just making sure that if you are building components, UI libraries, that if you really make your library very accessible, advertise that. Make the community know. Like, let Accessibility Chicago, Accessibility New York know.

As Dennis mentioned, I do the New York Meetup. There's meetups like this all over the US and now the world. I think as a grass-roots community, really evangelizing the things that do accessibility well and using them on our own projects, that's one way we can strengthen them and support them.

**[Dennis]:** Thank you very much.

**[Thomas]:** Thank you.

**[Applause]**

