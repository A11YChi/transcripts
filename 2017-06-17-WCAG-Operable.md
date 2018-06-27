# WCAG 2.0 - Operable
## Dennis Deacon - Wednesday, June 21, 2017
[Source recording](https://www.youtube.com/watch?v=LzABv9dO4ao)

**[Dennis]:** This is tonight's topic.

So, we have four main principles or I'll just say guidelines within the principle of operable. Keyboard accessible, enough time,  seizures and navigable.

So the first is keyboard accessibility. Basically make all functionality on a web page available to the keyboard. Okay, so everyone thinks. okay well that happens by default, right? Well, hopefully, I'll prove that wrong.

There's two main things that are focusable by default. Links ... and that's only if they have the href attribute. I cannot tell you how many times I run across links that have "onclick" but no "href." You can't get to this via keyboard if you don't have "href." Form fields. Custom form fields, they're all the rage. I work for a major airline headquartered in Chicago, and we love to make radio buttons look like boxes. It's custom fields, okay. Whenever you make a custom field not using the default capabilities of that element so you have to bake it in and I hope to show that to you as an example here.

So, let's take the example of links. So you have this arrow graphic. This arrow graphic could be to a slideshow carousel, it could be to a linear type presentation. But here's the code for it. What about this code makes this not keyboard accessible? Anyone have any ideas? So there's two lines and actually let me read that out. By the way, two meetups ago, I was hugely impressed by Marcy Sutton, who basically provided alternative text for everything you saw on the screen. I was like, oh my gawd. I aspire to be like her. So the code here says bracket image onmousedown equals next page parenthesis, so a function. And then src equals image forward slash next dash arrow dot png and then alt equals go to next page. So, what about this is not accessible? Yes?

**[Indecipherable]**

There's no anchor tag, okay. But, wouldn't this take care of it? "href" is missing. So what will happen if the href is missing? You can't reach it. So if you're tabbing through, you can't actually reach this particular element. What else about it is makes it not keyboard accessible? Yes?

**[Attendee]:** If you're using a screen reader, the screen reader [indecipherable] like that.

**[Dennis]:** Ok, that is very helpful. Anything else? Anyone else have any insight into what makes this really bad? Going once ... going twice ... I'm sorry? It is not clickable via keyboard, exactly. So, to the point, there's no "href" so you can't actually reach it via keyboard. If you hit tab, you hit all the links and all the form fields, you would never reach this. So, we can do this, we can add onkeydown equals next page the same function. So now. at least the keyboard can act on it. It could trigger the event. But what's still wrong?

**[Attendee]:** Focus.

**[Dennis]:** Focus. You can't reach it via keyboard. Sort of the same problems, right? We can trigger the event if we could get there, right?

**[Attendee]:** [Indecipherable]

**[Dennis]:** Well, that's ... you have to be able to focus on it before you can actually trigger the event. So we could do this ... we can add a tabindex equals zero. Now you can reach it via keyboard. Now, therefore you could trigger the event, right? Well, actually no. Because, this is an image. If you're reaching it via screen reader, it's going to say image. Okay, what do I do with an image? I don't act on an image, so I'm going to be confused. So now we got to add role equals link so we could tell it, okay, not only can you reach it,this is a link and you can ... when you press the key down, you can trigger this function. That's a lot of work, isn't it? When actually, if you just did this ... which is a href equals next dash page dot html image src equals arrow dot PNG alt equals go to next page.

So you might be saying, "okay, but we're trying to do..." let's say if this was the form field, "but we're trying to do custom field, we're trying to do something different." That's fine. But realize, you're going to have to make sure that the event is triggered by keyboard. You going to have to make sure that you can reach it by keyboard, and you're going to have to make sure that the screen reader knows, assistive technology knows that this is a link. This could have been a div and it's the same thing. So there's quite a bit of baking that you have to do to make that work.

Next one is No Keyboard Trap. Now I'll be honest, you're going to have to work with me. We're trying to picture this scenario because, I spent two days trying to come up with something that I've seen in the wild and to be honest, I have not seen anything that ... I think this is something that maybe we would have seen five, ten years ago from bad JavaScript coders ... doing validation. So basically, if the keyboard focus can be moved to a component of the page using a keyboard interface, then focus can be moved away from that component using only a keyboard interface, and if it requires more than unmodified arrow or tab keys or other standard exit methods, the user is advised of the method for moving focus away.

So this is the example I came up with. So this is using form field validation. So if you think of it, there was a period of time where we would, you know, once you moved off of a form field, they would check the validation. If it doesn't match, it would show an error message, right? So let's go ahead and put in ... I'm going to put in user name. Let's see here  ... messing up here left and right. Okay, let's put in a key ... password here. And now we have sort of a poor man's CAPTCHA. Basically, it's a text CAPTCHA, what is two plus two? 

Okay, before I answer that form field, here's the scenario. You're working for a small business. They use this CAPTCHA because they were receiving a lot of spam. The web developer they used to have, they left, the site's been ignored for a year. You have another developer come in and they say we're starting to get spam. They figured this out, change it. So what does the developer do? Let's say before it said eight plus two. So it expects ten. They changed it, two plus two, but they forgot to change the actual validation. So now, I answer it properly. Ah, shoot. I'm on the wrong one. I apologize. I told you I'm going to mess myself up. Thank you very much. This again is why I have Seth here to watch me.

00:08:55.780 --> 00:09:00.360
So, let's try this, and thank goodness I don't have to type anymore. So what is two plus two? Remember, it used to be eight plus two. But now we changed it to two plus two. But we forgot to change the actual value in the JavaScript. So when I go to tab off ... Ah! I'm still typing in the wrong spot, hold on. This is a great example. I feel like I'm using a Microsoft product. Okay, so now when I tab, you see nothing's happening and the reason why is using onblur. If the onblur doesn't validate, it won't let me off. I'm trapped and I literally ... so you think okay, I can do shift-tab. I can't leave this form field. This is a keyboard trap.

We don't see many of them out in the wild anymore, but... I'm sorry? Phone numbers ...

**[Seth]:** When you have three fields with your phone number, there's a lot of instances where it pushes you to the next field, and you hit the Delete key and it pushes you ... that's an example that's commonly still used.

**[Dennis]:** Okay. Yes ...

**[Attendee]:** If you want to go to a site that has lots of traps, go to LinkedIn.

**[Dennis]:** Linkedin, oh my gawd.

**[Attendee]:** Go to the search function? You don't work for LinkedIn do you?

**[Dennis]:** I'll have to let Jennison know ...

**[Attendee]:** You go to the search function, it keeps all the things you've ever searched for, sometimes, in the virtual view with JAWs or NVDA, you will get stuck there.

**[Dennis]:** Oh my goodness.

**[Attendee]:** [Indecipherable]

**[Dennis]:** Wow. Well, so they are still out in the wild. I wish I would have contacted you when I was trying to do this research. I would have came up with a better example. Yes ... And actually, I'll tell you what, because I just thought of this. I can't ... many people can't hear you. I know the folks on the screen can hear you so ... without ripping everything out. There you go, thank you.

**[Attendee]:** [indecipherable] ... navigation exercises, I founded that, the hamburger menu, when it says collapsed ... sometimes when you go into it, you can't get out. And I don't know that's just my lack of experience yet. I'm still learning the shortcuts ... [Indecipherable]

**[Dennis]:** Yeah, exactly.

[Indecipherable]

**[Dennis]:** Oh yeah. I can't tell you how many people I said, "yes, you also have to include Escape." The last one under keyboard accessibility is actually a AAA, and once again WCAG is divided amongst A, AA, and AAA. The baseline standard tends to be AA. So this is a AAA. Typically you can get this maybe on a page, a few pages. Having a whole site be AAA complaint, very difficult, almost impossible. But in this case, no exception. Keyboard has to be able to do everything without requiring specific timings for individual keystrokes and such. So, let's see here ...

Okay, enough time.

00:13:04.340 --> 00:13:05.820
Ecommerce websites.

00:13:06.340 --> 00:13:08.000
You're trying to purchase something.

00:13:08.460 --> 00:13:12.600
You get called the way .. you know, the dog just knocked over the aquarium.

00:13:14.320 --> 00:13:16.320
The first thing I could think of, I'm sorry.

00:13:16.920 --> 00:13:21.540
I don't know why that visions in my head. Hopefully that's not happening at home right now.

00:13:22.420 --> 00:13:26.600
Basically, provide users enough time to read and use the content.

00:13:27.840 --> 00:13:35.420
So for just content, it could be, let's say if you have let's say a dynamic panel that's updating.

00:13:36.040 --> 00:13:39.340
If it's updating too fast and you can't read it...

00:13:39.560 --> 00:13:44.700
... I don't know about you, I'm one of the few people who actually looks at the credits at the end of movies.

00:13:45.160 --> 00:13:49.640
And you know, nowadays, they push the credits one third of the screen,

00:13:49.640 --> 00:13:53.900
and then they start the next movie and they're running this about 5 times as fast.

00:13:53.900 --> 00:13:57.080
It's like, "but wait who's the director of photography?"

00:13:58.660 --> 00:14:03.500
So basically, provide enough time. You could have this a lot on ecommerce websites.

00:14:05.220 --> 00:14:07.240
Let's say if you're trying to make a purchase.

00:14:08.600 --> 00:14:10.100
I'll get the hang of this yet.

00:14:10.660 --> 00:14:12.660
Let's say if you're trying to make a purchase.

00:14:13.140 --> 00:14:15.720
And, you have a session timeout.

00:14:16.220 --> 00:14:23.600
Ideally, you would provide a means for extending that timeout, so this way the user can continue.

00:14:24.160 --> 00:14:29.880
The problem is, what if you're getting pricing that's effective at that very moment?

00:14:29.880 --> 00:14:35.140
If the pricing changes, let's say you have an auction website, that pricing changes,

00:14:35.940 --> 00:14:38.300
well now that's no longer applicable.

00:14:38.300 --> 00:14:44.680
So this actually has guidance but it also has exceptions

00:14:44.680 --> 00:14:47.000
for when you do not need to follow this.

00:14:47.460 --> 00:14:50.620
So basically, you need to allow the user to turn off

00:14:51.900 --> 00:14:58.940
this time limit, adjust the time limit, or extend it.

00:15:00.180 --> 00:15:04.140
They should be told 20 seconds before the time limit expires.

00:15:04.580 --> 00:15:07.980
And then they should be allowed to extend it.

00:15:08.280 --> 00:15:09.520
It could be very well ...

00:15:09.520 --> 00:15:13.120
they can have communicated "press the spacebar"

00:15:13.120 --> 00:15:15.380
and the user can then extend their time

00:15:15.380 --> 00:15:17.380
by at least 10 times.

00:15:18.200 --> 00:15:20.280
Now as you can see, that might be very difficult.

00:15:20.280 --> 00:15:22.280
Let's say, on an e-commerce website.

00:15:23.000 --> 00:15:25.720
So for that, we have exceptions.

00:15:26.020 --> 00:15:33.360
Real time exceptions, time limit is a required part of the real time event for at for example an auction.

00:15:34.160 --> 00:15:36.780
And no alternative to the time limit is possible.

00:15:37.840 --> 00:15:43.540
Essential exception, the time limit is essential and extending it would invalidate the activity.

00:15:44.300 --> 00:15:47.480
Again, think like airline ...

00:15:47.900 --> 00:15:50.800
I was trying to avoid talking about us but ...

00:15:50.800 --> 00:15:55.540
yeah, you know, if I can fly to Buffalo for $25 ...

00:15:55.540 --> 00:15:57.540
... first off why am I flying to Buffalo?

00:15:58.000 --> 00:16:01.100
BUT, hey that's a great price!

00:16:01.860 --> 00:16:03.660
And then I hit timeout,

00:16:03.660 --> 00:16:07.740
I close that and now the fare is $189.

00:16:08.040 --> 00:16:09.740
So, you know, it happens.

00:16:10.040 --> 00:16:12.460
[Indecipherable]

00:16:12.640 --> 00:16:14.900
[Dennis]: Exactly, they're famous for timeouts.

00:16:15.420 --> 00:16:17.420
I don't know why I didn't think of them.

00:16:17.660 --> 00:16:20.420
And then there's a 20 hour exception.

00:16:20.420 --> 00:16:23.000
The time limit is longer than 20 hours.

00:16:24.120 --> 00:16:25.000
Go figure.

00:16:26.420 --> 00:16:29.520
So ... pause stop and hide.

00:16:29.880 --> 00:16:36.180
For moving, blinking, scrolling, or auto updating information all of the following are true;

00:16:37.420 --> 00:16:39.540
Moving, blinking, scrolling information

00:16:40.700 --> 00:16:43.820
that starts automatically, lasts more than 5 seconds

00:16:44.240 --> 00:16:47.460
and is presented in parallel with other content,

00:16:47.740 --> 00:16:51.040
there is a mechanism for the user to pause, stop,

00:16:51.960 --> 00:16:55.220
or hide it unless the movement blinking or scrolling

00:16:55.220 --> 00:16:57.840
is part of an activity that is essential.

00:17:00.240 --> 00:17:07.920
Can anyone give me an example of moving, blinking, scrolling content that starts up right away?

00:17:10.120 --> 00:17:12.120
Stock prices, okay.

00:17:13.720 --> 00:17:14.680
Carousels.

00:17:14.920 --> 00:17:19.080
[Attendee]: Temperature. Weather stuff.

00:17:19.420 --> 00:17:21.420
[Dennis]: Okay. Anything else?

00:17:22.360 --> 00:17:24.040
You know what's my biggest pet peeve?

00:17:25.200 --> 00:17:26.020
Facebook.

00:17:26.880 --> 00:17:27.640
[Laughter]

00:17:27.740 --> 00:17:28.500
[Dennis]: At work.

00:17:29.640 --> 00:17:31.200
You're scrolling down the page ...

00:17:32.140 --> 00:17:33.580
... and all of a sudden you get Rick Rolled

00:17:34.980 --> 00:17:37.380
Hold it, hold it, oh wait ... now Rick Rolled ...

00:17:37.980 --> 00:17:38.960
Oh shoot ...

00:17:41.880 --> 00:17:42.980
Isn't it awful ...

00:17:44.440 --> 00:17:46.440
I've been practicing this all ...

00:17:47.600 --> 00:17:48.380
Hold on ...

00:17:52.040 --> 00:17:52.840
[Sigh]

00:17:54.460 --> 00:17:55.240
[Dennis]: Waiting ...

00:17:56.180 --> 00:17:58.640
Of course, it doesn't happen like this on Facebook ... of course ...

00:18:01.980 --> 00:18:04.240
Waiting ... waiting ... you've just been Rick Rolled ...

00:18:07.900 --> 00:18:11.040
See Seth, wasn't it funny how, before anyone showed up,

00:18:11.500 --> 00:18:13.780
this was like, popping, like this ...

00:18:14.940 --> 00:18:17.820
And now, when you want Rick Ashley

00:18:19.180 --> 00:18:21.260
to be dancing and sing and does doesn't happen.

00:18:21.260 --> 00:18:24.020
So basically ... we can bypass that of course because ...

00:18:24.680 --> 00:18:28.140
... someone's going to be, of course, offended eventually here ...

00:18:29.280 --> 00:18:34.680
I'll show ... uhh ... raise your hands in favor of ...

00:18:34.680 --> 00:18:36.680
okay I didn't see any hands.

00:18:36.700 --> 00:18:38.000
[Laughter]

00:18:38.380 --> 00:18:42.160
So basically, for instance, video.

00:18:42.160 --> 00:18:43.820
So you have video backgrounds.

00:18:43.980 --> 00:18:48.600
How many of you run into a site with video background in the last week or so?

00:18:49.440 --> 00:18:51.000
[Attendee]: Just video or audio?

00:18:52.220 --> 00:18:54.940
[Dennis]: Video. It can be video and audio.

00:18:55.600 --> 00:19:01.360
So if you think of it, even if it's video, there's some people, who depending on ...

00:19:01.360 --> 00:19:08.460
I know I've seen video backgrounds where there's ever so slight movement and such,

00:19:08.960 --> 00:19:11.480
that can ... that can mess with people.

00:19:12.400 --> 00:19:16.360
So and they really should have a way of turning it off or stopping it.

00:19:16.540 --> 00:19:22.380
But to the point, to Rick Ashley ... you should be able to stop him.

00:19:23.440 --> 00:19:26.720
So obviously, with Facebook and Twitter and such,

00:19:27.000 --> 00:19:31.660
you have user settings to where you could, you know, change the default

00:19:31.660 --> 00:19:35.420
to where videos don't automatically play but in this case here we have

00:19:35.880 --> 00:19:39.140
an accessible media player called Able Player

00:19:39.960 --> 00:19:44.960
and then, now this is not a video background, but if you then wanted to see the video, you would merely ...

00:19:46.380 --> 00:19:50.400
click on the video and then once again ... this is hilarious to me.

00:19:50.440 --> 00:19:51.380
I'm sorry.

00:19:51.640 --> 00:19:54.960
It doesn't play, it just spins ... that's nice.

00:19:55.440 --> 00:19:56.800
That's ever so nice.

00:19:57.640 --> 00:19:59.680
Well anyways, you didn't want ... you didn't have to hear that.

00:19:59.680 --> 00:20:02.620
I'm just concerned about the next two videos that are later on.

00:20:03.360 --> 00:20:05.400
So here's another example.

00:20:05.400 --> 00:20:08.800
Now this happens to be the Twitter feed for this Meetup

00:20:09.160 --> 00:20:14.080
and these are live tweets that have been going out over the last hour or so.

00:20:15.880 --> 00:20:20.900
If you had a very active event, where you had a lot of updates,

00:20:21.900 --> 00:20:27.560
this content that is auto-updating over here would actually distract you from reading over here.

00:20:27.560 --> 00:20:31.880
So, ideally, you would have controls to stop that auto updating.

00:20:35.300 --> 00:20:38.340
Okay and then, again, for AAA for enough time,

00:20:38.660 --> 00:20:45.480
there would be no timing, you would not have a time limit on any part of the website.

00:20:45.480 --> 00:20:48.720
Again, I don't think that would be possible with e-commerce.

00:20:48.720 --> 00:20:51.140
I don't know what an alternative to that would be.

00:20:52.360 --> 00:20:56.980
No interruptions and re-authentication.

00:20:57.120 --> 00:21:00.060
When an authenticated session expires,

00:21:00.060 --> 00:21:03.620
an user can continue the activity without loss of data

00:21:03.960 --> 00:21:05.580
after re-authenticating.

00:21:06.340 --> 00:21:10.440
That's a great user experience, but how many sites do we have that actually do that?

00:21:11.620 --> 00:21:15.900
So I mean unless you're writing to cookies or some other means ...

00:21:17.760 --> 00:21:19.200
Okay, seizures.

00:21:19.400 --> 00:21:20.680
I'll be honest,

00:21:21.300 --> 00:21:24.420
for the longest time, I always talked about seizures and

00:21:25.580 --> 00:21:29.500
you might think, okay, what in the heck on a website could cause a seizure?

00:21:30.780 --> 00:21:35.480
I like this, that it says, do not design content in a way that is known to cause seizures.

00:21:36.080 --> 00:21:41.100
And the idea is the three flashes or below threshold which says

00:21:41.600 --> 00:21:48.120
web pages do not contain anything that flashes more than three times in any one second period

00:21:48.420 --> 00:21:53.240
or the flashes below the general flash and red flash thresholds.

00:21:54.960 --> 00:21:59.700
So basically, flashing content can actually cause someone to be sick.

00:21:59.700 --> 00:22:06.940
Now this is the first time in two plus years that I've been talking about accessibility

00:22:06.940 --> 00:22:10.080
that I'm actually going to show an example

00:22:10.080 --> 00:22:13.560
Now, this is about as serious as I'm going to get tonight.

00:22:14.360 --> 00:22:23.540
If you are impacted by flashing content and you can become sick, I'm going to ask you to close your eyes.

00:22:25.160 --> 00:22:32.260
Okay, I have a video here which, of course my luck will not play,

00:22:32.680 --> 00:22:37.600
but it's a video that actually at the very beginning has this exact same warning,

00:22:38.620 --> 00:22:43.600
and it's by a popular artist by the name of Kanye West.

00:22:45.140 --> 00:22:49.760
And ... I'll see, we'll see if this even plays here.

00:22:52.060 --> 00:22:53.460
Is the Wi-Fi wonky?

00:22:57.440 --> 00:22:59.440
Waiting for an available socket ...

00:23:01.880 --> 00:23:04.620
Let's see what happens and if not, we'll just bypass it.

00:23:04.980 --> 00:23:09.680
I can describe while this is going on, I can really describe what's happening.

00:23:19.360 --> 00:23:21.660
Wait while we change Wi-Fi networks ...

00:23:30.780 --> 00:23:33.860
I did not realize how many Wi-Fi networks we have here.

00:23:36.960 --> 00:23:38.960
And actually, I am not seeing this one.

00:23:49.960 --> 00:23:51.420
Yeah, I'm actually not seeing this one.

00:23:51.420 --> 00:23:52.480
So no worries.

00:23:52.480 --> 00:23:59.540
So basically, what the video shows, where the problem comes about is

00:23:59.540 --> 00:24:05.500
there's this ... it's a black and white video, a young girl, wintertime, she's walking down the street,

00:24:06.020 --> 00:24:12.060
every, you know, t's black and white, there's snow on the ground and she turns around, there's a ...

00:24:12.700 --> 00:24:15.140
it looks like a housing complex behind her,

00:24:16.040 --> 00:24:22.500
and all of a sudden, the picture changes from red and green tints on the screen,

00:24:23.060 --> 00:24:31.120
and then I think the first word is Kanye, but it's every graphic design variation of it

00:24:31.800 --> 00:24:35.060
flashing and changing like every half a second.

00:24:38.460 --> 00:24:43.760
I don't know ... I have to admit, Kanye West is not my cup of tea,

00:24:44.640 --> 00:24:50.120
but when I saw the video, I found it very interesting that they actually had to have a warning in front of it.

00:24:51.640 --> 00:24:58.440
So, other conditions, and this is ... as well a AAA.

00:24:58.680 --> 00:25:01.220
Three flashes, web pages don't contain anything

00:25:01.560 --> 00:25:05.880
that flashes more than three times in any one second period.

00:25:06.200 --> 00:25:13.520
There's actually a website, I want to say it's out of New York, I've seen it at other conferences.

00:25:13.520 --> 00:25:17.800
They show it, it's like the noisiest, busiest site you've ever seen.

00:25:18.180 --> 00:25:23.900
And I'd be willing to say if I could find it, they have flashing content and it's all to grab your attention.

00:25:24.320 --> 00:25:27.860
I'm sure they have tons of lawsuits for making people sick.

00:25:28.920 --> 00:25:36.820
Navigable. Provide ways to help users navigate find content and determine where they are.

00:25:37.940 --> 00:25:41.900
So bypass blocks. Who knows what Bypass Blocks are?

00:25:43.080 --> 00:25:44.060
Raise your hands.

00:25:45.340 --> 00:25:47.340
Anyone know what a skip link is?

00:25:49.200 --> 00:25:50.160
We've got a few more.

00:25:50.160 --> 00:25:57.180
Ok, so basically, on every page of a website that you probably deal with, you have global navigation.

00:25:58.480 --> 00:26:02.780
Let's say, if that global navigation exposes the mega menu.

00:26:04.040 --> 00:26:10.320
Imagine navigating each page on that website you had to read that mega menu.

00:26:10.900 --> 00:26:12.720
That could be really irritating, couldn't it?

00:26:13.180 --> 00:26:15.800
You probably only have to hear it the first time

00:26:16.200 --> 00:26:19.420
and then you least know how its organized and where everything is.

00:26:19.900 --> 00:26:21.320
So a skip link

00:26:22.260 --> 00:26:24.980
is literally just a

00:26:25.860 --> 00:26:27.860
typically, by default, it's hidden

00:26:28.920 --> 00:26:30.920
before the global navigation.

00:26:31.800 --> 00:26:35.340
And then it points to the the actual content.

00:26:35.340 --> 00:26:40.080
So in this case, we have anchor href pound sign content,

00:26:40.080 --> 00:26:42.080
so this would be content.

00:26:42.740 --> 00:26:44.240
Class visually hidden.

00:26:44.240 --> 00:26:47.060
Visually hidden is nearly a CSS class

00:26:47.580 --> 00:26:51.180
that keeps the content exactly where it is,

00:26:51.500 --> 00:26:54.820
but it hides it from presentation visually.

00:26:55.400 --> 00:27:00.160
Ok, and then it points to the actual content here.

00:27:00.440 --> 00:27:07.780
Some sites, when you tab and when this link gets focused it will actually display.

00:27:08.440 --> 00:27:10.440
Other sites just don't want it to display.

00:27:10.800 --> 00:27:13.640
There's nothing saying that it has to be displayed.

00:27:13.640 --> 00:27:15.500
I think it's a nice to have,

00:27:15.500 --> 00:27:21.000
because it's more than just people with visual impairments using screen readers

00:27:21.000 --> 00:27:21.960
who might need that.

00:27:22.240 --> 00:27:27.120
There's a lot of people who actually use screen readers who just have cognitive disabilities.

00:27:30.940 --> 00:27:31.980
Page Title.

00:27:33.280 --> 00:27:41.960
Guess how many pages on the Internet as of this morning have the page title of "untitled document?"

00:27:47.020 --> 00:27:48.600
It would seem that way...

00:27:49.020 --> 00:27:52.720
According to Google, twelve million, five hundred thousand pages.

00:27:53.660 --> 00:27:58.800
I don't know about you but untitled document is not all that descriptive.

00:27:58.800 --> 00:28:02.760
I can't think of a page that would benefit from that page title.

00:28:02.760 --> 00:28:06.340
So basically, provide a good descriptive page title.

00:28:06.340 --> 00:28:09.820
Now, for anyone here who also does SEO,

00:28:10.100 --> 00:28:15.380
"Hello." If you want to be found, then you probably have pretty good page titles.

00:28:17.460 --> 00:28:20.280
Obviously not untitled document or new page,

00:28:20.280 --> 00:28:23.080
good ones would be basically

00:28:23.080 --> 00:28:25.080
a description of the theme of the page.

00:28:25.940 --> 00:28:27.020
Create an account.

00:28:27.840 --> 00:28:29.140
Semantic structure.

00:28:29.560 --> 00:28:32.260
And then of course it could be the site name or whatever.

00:28:34.280 --> 00:28:35.340
Focus order.

00:28:35.340 --> 00:28:45.640
If a web page can be navigated sequentially and the navigation sequences affect meaning or operation,

00:28:45.640 --> 00:28:52.080
focusable components receive focus in an order that preserves the meaning and operability.

00:28:53.480 --> 00:28:56.020
Just so you know, WCAG is written this way.

00:28:57.280 --> 00:29:02.300
And after five o'clock, I cannot pronounce half of these words in sequence. So ...

00:29:05.020 --> 00:29:06.600
So, if you come to this web page,

00:29:06.600 --> 00:29:08.320
you have four form fields;

00:29:08.320 --> 00:29:11.260
first name, last name, email and phone.

00:29:11.260 --> 00:29:15.180
What order would you expect the focus order to be?

00:29:23.480 --> 00:29:28.200
So first name, last name, it sounds mixed whether it be email or phone.

00:29:30.120 --> 00:29:32.120
So let's see how that works out.

00:29:33.300 --> 00:29:34.760
So first name, right?

00:29:35.920 --> 00:29:38.800
Ah, oh ... phone ... that's not good.

00:29:38.900 --> 00:29:40.460
That's not what I expected.

00:29:41.040 --> 00:29:44.040
Last name ... doesn't seem right.

00:29:44.040 --> 00:29:44.760
Email ...

00:29:45.140 --> 00:29:46.640
The problem here ...

00:29:49.240 --> 00:29:51.240
... you find out all my email addresses here ...

00:29:52.460 --> 00:29:53.420
... there we go ...

00:29:53.540 --> 00:29:56.360
The problem here is that someone has used

00:29:57.200 --> 00:30:00.400
a tabindex attribute of a positive number.

00:30:02.820 --> 00:30:07.100
I have done this ... in 1998, I did this.

00:30:07.920 --> 00:30:12.260
I haven't done it since because whenever you use positive tabindex,

00:30:13.100 --> 00:30:16.540
you have to manually maintain that for the rest of your life.

00:30:17.660 --> 00:30:20.920
I don't know about you but I want to do as little work as possible.

00:30:20.920 --> 00:30:26.980
So if the business or the website owner decides that they want to add a field

00:30:26.980 --> 00:30:30.040
and they want to move this over here and put that over there,

00:30:30.320 --> 00:30:36.660
do you really want to go through all 137 form fields and change  the tabindex?

00:30:37.600 --> 00:30:42.500
No, never use a positive tabindex.

00:30:42.720 --> 00:30:46.140
Always use either zero ...

00:30:47.340 --> 00:30:48.820
having a tab index of zero

00:30:48.820 --> 00:30:54.340
and once again, this is only for elements that don't already get focus by default.

00:30:54.380 --> 00:30:59.000
So if it's not a link, if it's not a form field, then you would do this.

00:30:59.880 --> 00:31:02.620
Okay, tabindex equals zero

00:31:03.940 --> 00:31:08.340
puts it in the order in which it appears in the DOM, in the code order.

00:31:09.460 --> 00:31:11.620
Okay, so if you want something moved up,

00:31:11.620 --> 00:31:14.600
move the code for that up.

00:31:16.020 --> 00:31:20.160
If you have tabindex equals negative one

00:31:20.500 --> 00:31:21.320
it's ready .

00:31:21.320 --> 00:31:24.280
It's not focusable already,

00:31:24.640 --> 00:31:26.380
but when you have a script,

00:31:27.800 --> 00:31:30.260
you can then turn that on with the script,

00:31:30.260 --> 00:31:32.560
and then you can access it via the keyboard.

00:31:34.440 --> 00:31:38.080
Avoid using tabindex 1 plus

00:31:38.080 --> 00:31:40.080
Anything, any positive number.

00:31:40.300 --> 00:31:44.840
There's a article here that goes well deep into this

00:31:45.260 --> 00:31:49.660
excerpted from "Using the tabindex attribute" by Leonie Watson,

00:31:50.040 --> 00:31:52.920
who we saw the quote earlier in this presentation.

00:31:54.880 --> 00:31:56.120
Link purpose.

00:31:56.160 --> 00:31:58.420
I love this one. I'll tell you right now ...

00:32:00.000 --> 00:32:02.300
in anything that I touch and anything I do,

00:32:02.300 --> 00:32:05.180
I require Triple A on this.

00:32:05.300 --> 00:32:08.880
This is AA. You'll see why I say AAA.

00:32:09.260 --> 00:32:14.940
The purpose of each link can be determined from the link text alone or

00:32:14.940 --> 00:32:16.580
... here's where I have a problem ...

00:32:17.220 --> 00:32:22.120
from the link text together with its programmically determined link context

00:32:22.500 --> 00:32:27.580
except where the purpose of the link would be ambiguous to the users in general.

00:32:28.000 --> 00:32:31.120
So, basically, this allows for surrounding text

00:32:32.700 --> 00:32:35.120
to make that link text unique.

00:32:37.420 --> 00:32:39.140
Anyone who uses a screen reader,

00:32:40.100 --> 00:32:45.520
most folks who use a screen reader have the ability to look at all the links on a page.

00:32:46.180 --> 00:32:49.080
and those links are called out by the link text.

00:32:50.960 --> 00:32:56.280
Many sites that you visit, that list would be "learn more," "buy now," "book now."

00:32:58.900 --> 00:32:59.900
Things like that.

00:33:00.480 --> 00:33:01.940
Click here.

00:33:05.540 --> 00:33:07.540
Oh yeah, I'm shivering from that.

00:33:08.540 --> 00:33:13.240
So, definitely make your link text descriptive on its own.

00:33:13.240 --> 00:33:18.800
That is AAA. This is AA. Go the extra mile and do it right..

00:33:18.800 --> 00:33:21.260
So, I'm going to give you an example here ...

00:33:21.640 --> 00:33:25.700
...  to see the context for the link is not provided in one of the following ways ...

00:33:25.700 --> 00:33:29.260
in the same sentence, paragraph, list item, or table cells the link ...

00:33:30.180 --> 00:33:36.700
...  or in the preceding heading or via suitable ARIA properties such as aria-label or aria-labelledby,

00:33:36.920 --> 00:33:42.040
then the user will not be able to find out where the link is going with any ease.

00:33:42.320 --> 00:33:45.580
If the user must leave the link to search for the context,

00:33:45.580 --> 00:33:53.700
the context is not programmically determined link tech context and is and this is not considered accessible.

00:33:54.080 --> 00:33:56.540
I go the next route.

00:33:56.540 --> 00:33:59.280
So and this will give you an example of this.

00:33:59.280 --> 00:34:04.280
So on the screen, we have three add tiles, let's say.

00:34:04.280 --> 00:34:08.400
We have, some of them have headings, I guess all of them have headings.

00:34:08.880 --> 00:34:11.600
So we have one that says "Small Business Big Savings."

00:34:12.000 --> 00:34:17.160
And then the text is "Save up to 30% off base rates with Avis for Business."

00:34:17.800 --> 00:34:23.260
And it's difficult to see here, but the call-to-action button says "Enroll Today."

00:34:24.000 --> 00:34:28.000
We have another one for AARP ... "Welcome AARP Members."

00:34:28.300 --> 00:34:33.620
"Learn more about our exclusive offers and savings for AARP members."

00:34:34.600 --> 00:34:36.600
The link says "View Details."

00:34:37.800 --> 00:34:41.000
This last one, "SUV's as low as $29."

00:34:41.400 --> 00:34:42.940
"Maximize your drive."

00:34:43.520 --> 00:34:45.520
The link text, "Learn More."

00:34:46.560 --> 00:34:50.840
So again, screenreader users have a way to show a list of the links.

00:34:52.740 --> 00:34:54.940
So if you were to look at the list of links ...

00:34:56.060 --> 00:34:59.460
... and if you couldn't see those ads,

00:34:59.960 --> 00:35:02.800
what do you think the list of links would be?

00:35:05.660 --> 00:35:06.860
Enroll today.

00:35:08.380 --> 00:35:09.680
Enroll today for what?

00:35:12.400 --> 00:35:13.460
View Details

00:35:15.240 --> 00:35:16.720
Details of what?

00:35:17.920 --> 00:35:18.800
Learn more.

00:35:19.740 --> 00:35:20.820
About what?

00:35:21.400 --> 00:35:26.000
So, you see where that link text is very important and very valuable.

00:35:26.000 --> 00:35:30.300
Now, it doesn't mean that you have to ruin your designs.

00:35:31.000 --> 00:35:37.940
It doesn't mean that you have to turn into Wikipedia or Craigslist or you know really text-heavy.

00:35:39.380 --> 00:35:43.140
You could do things like adding, what we call screen reader text.

00:35:43.940 --> 00:35:46.160
So you can still have your link, your details,

00:35:47.020 --> 00:35:51.200
And then, you have a span with the class of visuallyhidden.

00:35:51.200 --> 00:35:55.660
Our CSS class that basically visually hides the text.

00:35:56.620 --> 00:35:59.720
And then you can have "about AARP membership"

00:36:00.660 --> 00:36:02.320
and then close span, close anchor.

00:36:02.320 --> 00:36:06.980
So a screen reader is going to see "View details about AARP membership."

00:36:08.320 --> 00:36:09.900
Isn't that much richer?

00:36:09.900 --> 00:36:16.180
Now yes, ideally, that would be there for both screen reader users and visually.

00:36:17.100 --> 00:36:19.100
But if you can't get buy off on that ...

00:36:19.820 --> 00:36:21.160
at least do this.

00:36:22.040 --> 00:36:24.140
Anyone here have a Wordpress site?

00:36:25.640 --> 00:36:26.520
Okay, we've got a few.

00:36:26.780 --> 00:36:29.820
You know the ... in a blog list,

00:36:29.820 --> 00:36:34.120
you got the headline, you got the excerpt and then you have, like, read more or whatever.

00:36:34.760 --> 00:36:36.980
There's now techniques where you can grab ...

00:36:37.760 --> 00:36:44.460
the article and just the through a screen reader text add it to the read more about

00:36:44.460 --> 00:36:46.460
and then the name of the article.

00:36:48.800 --> 00:36:49.760
Multiple Ways.

00:36:49.760 --> 00:36:54.300
More than one way is available to locate a web page within a set of web pages,

00:36:54.660 --> 00:36:57.280
except where the web pages is the result

00:36:57.880 --> 00:36:58.600
that doesn't

00:36:59.080 --> 00:37:04.120
oh, the web page singular, sorry, is the result of, or a step in, a process.

00:37:05.000 --> 00:37:08.880
This is my favorite site for multiple ways to get to information.

00:37:09.840 --> 00:37:11.840
This is Wikipedia.

00:37:12.540 --> 00:37:20.460
This is a Wikipedia page for the only Batman that matters by the way, Adam West.

00:37:20.620 --> 00:37:24.540
There's links here to everything that's on the page.

00:37:24.540 --> 00:37:31.020
There's links here to everywhere related content, relatable content.

00:37:31.440 --> 00:37:34.180
There's multiple ways to get to all this information.

00:37:34.380 --> 00:37:39.820
This, I view, is a fine example of multiple ways to get the content.

00:37:42.280 --> 00:37:43.240
Headings and Labels.

00:37:43.240 --> 00:37:46.100
Headings and labels describe topic or purpose.

00:37:48.200 --> 00:37:51.660
Ensure pages with groups of contents have headings.

00:37:53.740 --> 00:37:59.040
This is a little lenient on AA. It's more explicit in AAA.

00:37:59.520 --> 00:38:06.700
I think, where it makes sense, I think all pages with a lot of content should have that content chunked,

00:38:06.700 --> 00:38:09.820
and have headings for each of those groups of content.

00:38:10.400 --> 00:38:14.940
So in here, you have an h1, the page heading, of rental cars.

00:38:14.940 --> 00:38:16.780
h2 would be economy cars.

00:38:16.780 --> 00:38:18.900
Another h2 might be compact cars.

00:38:19.440 --> 00:38:22.780
Only one h1 to a page.

00:38:23.480 --> 00:38:29.120
I know HTML5 allows for multiple, especially if you have articles or sections, ...

00:38:30.400 --> 00:38:33.280
don't do that. That can actually confuse folks.

00:38:34.160 --> 00:38:41.920
Stick to one h1 per page and then have all the rest of the headings on a page be subheadings to that.

00:38:44.080 --> 00:38:44.940
Labels.

00:38:44.940 --> 00:38:50.860
The same thing. Provide a label for any interactive component that makes the components purpose clear.

00:38:51.200 --> 00:38:59.660
Here we have first name, and many screen readers are going to read that asterisk as star ... "first name star."

00:39:02.820 --> 00:39:07.180
I've always wanted to do this talk sounding like George Carlin.

00:39:07.420 --> 00:39:10.520
I haven't worked that one up yet. Talk to me next year.

00:39:13.760 --> 00:39:14.660
You can sit there

00:39:14.660 --> 00:39:17.760
and have the meaning of this star, required

00:39:17.760 --> 00:39:20.920
once again, screen reader text required,

00:39:20.920 --> 00:39:23.980
and then you can hide it from the screen reader

00:39:23.980 --> 00:39:25.020
with aria-hidden.

00:39:26.240 --> 00:39:32.420
You can ... I mean it's a little extra work,  but it makes for a much cleaner, richer experience for all.

00:39:33.640 --> 00:39:35.040
I really have to admit,

00:39:35.040 --> 00:39:37.200
I can't remember why I put this out there.

00:39:39.380 --> 00:39:40.640
It's about labels.

00:39:40.860 --> 00:39:44.240
I can't remember my point so I'm just going to have to bypass that one.

00:39:45.840 --> 00:39:46.820
Focus visible.

00:39:46.820 --> 00:39:50.880
Okay, raise your hands if you're primarily a designer.

00:39:52.660 --> 00:39:53.500
Don't be afraid ...

00:39:54.880 --> 00:39:56.400
Okay, we've got about three.

00:39:56.640 --> 00:40:02.900
How many of you have removed the focus indication around links and form fields?

00:40:06.340 --> 00:40:08.340
I need to talk to you afterwards.

00:40:09.780 --> 00:40:10.820
Don't do that.

00:40:13.380 --> 00:40:14.980
Here's why you shouldn't do it.

00:40:14.980 --> 00:40:27.640
If you go to the site outlinenone dot com, it'll explain all the reasons why you should not remove the outline

00:40:28.040 --> 00:40:30.040
to links and form fields.

00:40:32.780 --> 00:40:36.780
I'm going to pray that this last video will play.

00:40:37.080 --> 00:40:38.860
This is Marcy Sutton.

00:40:39.180 --> 00:40:44.140
This is really when I got started with accessibility and when I saw that being

00:40:44.660 --> 00:40:49.480
working with an airline website, I was blown away and I showed this to everyone I could.

00:40:50.880 --> 00:40:57.300
She does a screen reader demo here, trying to navigate the brand-new Virgin America web site

00:40:57.300 --> 00:41:02.580
that had just been redesigned, was getting a lot of press, it's so great so stylish

00:41:04.160 --> 00:41:08.060
and as you hopefully will see, completely inaccessible.

00:41:09.000 --> 00:41:14.300
[video - screen reader announcing]

00:41:14.300 --> 00:41:16.640
[video - Marcy Sutton]: "It's skipping before and after the calendar,

00:41:16.640 --> 00:41:20.060
and I can't figure out how I am going to book these dates."

00:41:20.600 --> 00:41:21.840
[Dennis]: Actually, I'm going to go ...

00:41:21.840 --> 00:41:27.360
I'm going to skip backwards again, because actually this went too far in advance.

00:41:27.920 --> 00:41:33.320
[video - screen reader announcing]: "Book link, tab"

00:41:33.320 --> 00:41:36.160
[video - Marcy Sutton]: "I don't see where I am on the screen. I can't really tell."

00:41:36.160 --> 00:41:37.620
[video - screen reader announcing]: "tab, tab, tab"

00:41:37.620 --> 00:41:39.460
[video - Marcy Sutton]: "I'm just tabbing.

00:41:39.460 --> 00:41:42.260
[video - screen reader announcing]: "sign out link tab"

00:41:42.900 --> 00:41:44.320
"san francisco link"

00:41:44.320 --> 00:41:45.640
[video - Marcy Sutton]: "Oh, ok, I see that"

00:41:45.640 --> 00:41:51.280
[video - screen reader announcing]: "tab, san francisco link"

00:41:51.960 --> 00:41:56.400
[video - Marcy Sutton]: "Ok, I guess I'm departing from somewhere. I don't now what I'm trying to book."

00:41:56.680 --> 00:42:00.640
[video - screen reader announcing]: "tab, los angeles ca ... link"

00:42:01.680 --> 00:42:04.800
[video - Marcy Sutton]: "Ok, I guess I'll just leave from los angeles, that's not very convenient."

00:42:04.800 --> 00:42:07.720
"I don't know how to use this website if I can't see it."

00:42:07.720 --> 00:42:09.720
[video - screen reader announcing]: "tab, tab, tab "

00:42:09.720 --> 00:42:12.280
[video - Marcy Sutton]: "Now, it just kicked me all the way back to the top, even though ..."

00:42:12.280 --> 00:42:13.880
[video - screen reader announcing]

00:42:14.060 --> 00:42:16.520
[video - Marcy Sutton]: "even though I should be on the screen. Oh ..."

00:42:16.520 --> 00:42:17.820
[video - screen reader announcing]

00:42:17.820 --> 00:42:20.140
[video - Marcy Sutton]: "There was an alert there, I don't know if you caught that,"

00:42:20.140 --> 00:42:22.740
"but, at the top of the screen, when something happened,"

00:42:22.740 --> 00:42:26.560
"I made a selection, and there was a big banner at the top, that said, 'hey, you made a selection."

00:42:27.140 --> 00:42:31.080
"But it didn't alert me. If I'm not a visual user, I have no idea that occurred."

00:42:32.780 --> 00:42:37.360
"So now, I''m further down on the page. This is part of the user experience that is very visual."

00:42:37.800 --> 00:42:40.080
"But I have no idea where I am in this purchase flow."

00:42:41.120 --> 00:42:44.260
[video - screen reader announcing]

00:42:44.260 --> 00:42:47.240
[video - Marcy Sutton]: "I don't see Fort Lauderdale ..."

00:42:48.020 --> 00:42:53.180
[video - screen reader announcing]: "new york tab san francisco tab all cities link tab"

00:42:53.580 --> 00:42:56.080
[video - Marcy Sutton]: "That's not what I'm trying to find. Frustrating."

00:42:56.700 --> 00:42:59.480
[video - screen reader announcing]

00:43:00.160 --> 00:43:03.040
[video - Marcy Sutton]: "Ok, I must be related to the numbers down below."

00:43:04.080 --> 00:43:14.020
[video - screen reader announcing]

00:43:14.020 --> 00:43:16.480
[video - Marcy Sutton]: "I still don't really know ..."

00:43:16.920 --> 00:43:21.460
[video - screen reader announcing]

00:43:21.460 --> 00:43:23.460
[video - Marcy Sutton]: "So, another alert, didn't hear it."

00:43:23.460 --> 00:43:26.400
[video - screen reader announcing]

00:43:26.400 --> 00:43:28.020
[video - Marcy Sutton]: "Now, I'm on the calendar selection."

00:43:28.020 --> 00:43:32.420
[video - screen reader announcing]

00:43:32.720 --> 00:43:35.360
[video - Marcy Sutton]: "I'm skipping, before and after the calendar,"

00:43:35.560 --> 00:43:39.180
"and I can't figure out how I am going to book these dates."

00:43:39.180 --> 00:43:41.180
"So, not only have I picked ... "

00:43:42.440 --> 00:43:44.440
[Dennis]: Oh, Gee, I've lost everything now.

00:43:48.180 --> 00:43:49.560
Hello...

00:43:55.420 --> 00:44:00.140
Isn't it great when you realize that you don't now how to use a computer?

00:44:04.640 --> 00:44:11.840
Ok, hold on ... I shall get us there ... we're actually not ... far to go now, as the saying goes.

00:44:13.840 --> 00:44:15.840
This is crazy. Ah, there we go. Good.

00:44:17.480 --> 00:44:19.060
One second.

00:44:25.020 --> 00:44:26.020
I don't now why I lost that.

00:44:26.020 --> 00:44:31.120
Normally, when I have these presentations, the screen just goes black, and I have no idea how to get it back.

00:44:31.420 --> 00:44:33.420
This time, I just lost my

00:44:34.460 --> 00:44:38.080
entire presentation, a whole browser.

00:44:39.640 --> 00:44:42.460
Ok, so, you've seen all that, you've done all that,

00:44:42.840 --> 00:44:44.980
let's get to where we were.

00:44:45.500 --> 00:44:48.880
So as you see, with the focus indication, you see how important

00:44:49.620 --> 00:44:57.620
if you don't have it, how ... you know ... you're not going to be able to safely navigate a web page

00:44:57.620 --> 00:45:01.740
unless you can see where you are, if you're using a keyboard.

00:45:02.300 --> 00:45:07.340
So ... I think I spoke almost slow enough.

00:45:07.340 --> 00:45:09.380
Okay, so here's a real example.

00:45:09.380 --> 00:45:12.420
So we have different focusable elements.

00:45:12.420 --> 00:45:19.240
We have link text, we have our infamous right arrow, a graphical button.

00:45:19.580 --> 00:45:22.360
We have a form field and we have sign up.

00:45:23.200 --> 00:45:31.180
Now if I'm tabbing, you can see that the focus indication is blatant.

00:45:31.180 --> 00:45:38.620
Now yes, I'll admit you probably will never make it this "contrasty" on a site that you're doing,

00:45:38.620 --> 00:45:43.180
but you want to be able to tell at any time where you are.

00:45:43.940 --> 00:45:48.320
What you want to be careful of is if you don't have ...

00:45:48.320 --> 00:45:50.540
like this is all nice, black background.

00:45:50.860 --> 00:45:55.980
Or on a typical website, you would have a white background and maybe you'd have black text and such.

00:45:57.260 --> 00:46:00.520
That's fine. But what if you have a colorful website?

00:46:01.780 --> 00:46:03.780
What's going to happen to your focus indication?

00:46:07.920 --> 00:46:09.920
There you go. Can you see it?

00:46:11.420 --> 00:46:12.460
How about now?

00:46:13.660 --> 00:46:15.300
I could do an eye chart thing right now.

00:46:15.580 --> 00:46:17.460
Better ... or worse?

00:46:20.840 --> 00:46:22.680
So, these are things ...

00:46:22.680 --> 00:46:26.420
so in this case ... you know last time we talked about color contrast,

00:46:26.420 --> 00:46:28.420
and we're primarily talking about text.

00:46:28.940 --> 00:46:30.340
Text communicates.

00:46:31.100 --> 00:46:34.360
In this case, focus indication communicates.

00:46:35.040 --> 00:46:39.420
So in this case, I would say you need to make sure you have proper color contrast.

00:46:40.600 --> 00:46:45.620
Okay, other items under this are location,

00:46:45.620 --> 00:46:48.540
information about the users location within the set of

00:46:48.860 --> 00:46:50.400
web pages is available.

00:46:51.640 --> 00:46:52.660
Breadcrumbs.

00:46:53.500 --> 00:46:55.440
You know where in the site that you are.

00:46:56.420 --> 00:46:58.500
Okay, link purpose.

00:46:58.500 --> 00:47:00.260
This is what I was talking about before.

00:47:00.260 --> 00:47:01.420
This is a AAA.

00:47:01.780 --> 00:47:03.900
I believe that the link purpose should be

00:47:03.900 --> 00:47:05.340
solely within the link text.

00:47:05.880 --> 00:47:07.480
That's me saying that.

00:47:07.720 --> 00:47:11.140
I believe in quality, so in this case,

00:47:11.880 --> 00:47:14.400
it's not required for AA compliance,

00:47:14.900 --> 00:47:17.520
but I would say here, go the extra mile.

00:47:17.520 --> 00:47:19.100
Your users will appreciate it.

00:47:20.720 --> 00:47:22.060
And then, section headings.

00:47:22.060 --> 00:47:24.520
Again, you know, just make sure

00:47:24.520 --> 00:47:26.400
if you have groups of content on your pages,

00:47:26.400 --> 00:47:27.920
make sure you have headings

00:47:27.920 --> 00:47:29.260
for each one of those groupings.

00:47:30.000 --> 00:47:32.400
Ok, WCAG 2.1 ...

00:47:32.580 --> 00:47:34.580
So, okay, go ahead, I'm sorry ...

00:47:35.380 --> 00:47:47.880
[Attendee]: [Indecipherable]

00:47:48.060 --> 00:47:50.600
[Dennis]: I don't know.

00:47:51.740 --> 00:47:53.420
There's actually a book called ...

00:47:54.440 --> 00:47:57.820
WCAG 2.0 Made Easy.

00:47:58.660 --> 00:48:00.500
And that's for a reason.

00:48:00.700 --> 00:48:02.840
It's actually, obviously,

00:48:03.540 --> 00:48:09.500
fewer pages than the hundred, I'm sorry, one thousand I think was ninety, pages of WCAG.

00:48:11.060 --> 00:48:15.200
To be honest, when you get to, you know, when you first read WCAG,

00:48:16.260 --> 00:48:20.000
when you read something like that, you're like, "okay, what are you talking about?"

00:48:20.920 --> 00:48:25.160
In WCAG , they typically have a link nearby that says, "Understanding."

00:48:25.940 --> 00:48:28.380
This particular, 2.4 Navigable.

00:48:28.780 --> 00:48:36.360
Read that. That's going to go into a lot of detail, but it's going to be slightly more everyday English.

00:48:41.220 --> 00:48:48.540
So again, with Operable, there's only one success criteria in 2.1 and that's Interruptions.

00:48:49.660 --> 00:48:55.360
So in 2.0, Interruptions is actually, I believe, a AAA.

00:48:56.140 --> 00:48:57.880
Here, they're saying AA.

00:48:57.880 --> 00:49:03.920
So if you want to be the baseline you have to have an easily available mechanism

00:49:03.920 --> 00:49:08.600
to postpone or suppress interruptions and changes in content

00:49:08.600 --> 00:49:13.280
unless they are initiated by the user or involve an emergency.

00:49:14.740 --> 00:49:19.240
I'll let you think about that for the next year or so,

00:49:19.240 --> 00:49:27.160
and the reason why I say a year or so is because WCAG 2.1 won't probably be fully supported for a few years.

00:49:27.680 --> 00:49:31.840
But, as you can imagine with something like this, it takes probably a few years of planning

00:49:31.840 --> 00:49:33.840
to think about how you're going to address this.

00:49:35.220 --> 00:49:36.740
So with that said,

00:49:37.820 --> 00:49:41.280
are there any questions on WCAG 2.0 Operable?

00:49:42.420 --> 00:49:47.700
Yes. Ah, hold on ... I gotta get you plugged in.

00:49:50.380 --> 00:49:54.840
[Attendee]: There's only one h1 per page even if it's HTML5.

00:49:55.640 --> 00:49:59.500
Here's the issue I'm facing and I'm not sure what to do about it.

00:50:00.340 --> 00:50:01.400
Iframes.

00:50:03.220 --> 00:50:14.300
When you bring a page into an iframe, the page that is being entered into will already have an h1.

00:50:14.720 --> 00:50:21.580
But the page that is brought in will have its own h1.

00:50:23.060 --> 00:50:30.100
[Dennis]: So will the host page's h1 and then the addition of the iframe pages h1 cause a problem?

00:50:30.100 --> 00:50:31.320
[Attendee]: That is the question.

00:50:31.320 --> 00:50:32.000
[Dennis]: No.

00:50:32.580 --> 00:50:33.520
[Attendee]: Yay!

00:50:33.520 --> 00:50:35.720
[Dennis]: I just made her happy!

00:50:35.720 --> 00:50:42.220
[Attendee]: You did! You cannot imagine the hundreds and thousands of pages you just saved the lives of.

00:50:44.960 --> 00:50:47.980
[Dennis]: Wow, I'm not going into work tomorrow. I feel special.

00:50:53.360 --> 00:50:57.160
I am not aware that that is an issue because

00:50:57.540 --> 00:51:00.300
that would just ...

00:51:05.000 --> 00:51:08.240
for lack of a better way to say it, that would be insane to require.

00:51:09.340 --> 00:51:10.880
I mean you can't. How are you gonna ...

00:51:11.320 --> 00:51:13.700
any paid ... that would mean that you can't use iframes.

00:51:14.920 --> 00:51:18.400
[Attendee]: So this my question, can you use an iframe and be accessible?

00:51:18.400 --> 00:51:19.920
[Dennis]: You can use an iframe,

00:51:19.920 --> 00:51:22.300
The only thing I'll say is, you can use an iframe,

00:51:22.300 --> 00:51:29.300
but make sure it has a title attribute that describes what the content in the iframe is.

00:51:29.680 --> 00:51:38.280
[Attendee]: We actually are currently implementing, I'll speak up, iframes from third-party providers,

00:51:38.280 --> 00:51:46.980
but those third-party provider, systems [indecipherable] ...  so we have a lot of included

00:51:47.620 --> 00:51:54.260
registration forms, ... forms, but their systems are accessible inherently.

00:51:55.120 --> 00:52:01.180
So when we include them as a iframe, the only thing we have to do, like Dennis said, is title the frame.

00:52:02.960 --> 00:52:09.860
[Attendee]: Thank you. The context is, I am a learning management system administrator.

00:52:10.260 --> 00:52:18.260
And our learning management system is coming up with a new mobile-friendly design

00:52:18.520 --> 00:52:25.180
where our content pages are brought into their ... as iframe.

00:52:25.320 --> 00:52:35.760
And I have to trust them, and I actually object to that, but they do have a general ... this is the page content.

00:52:36.080 --> 00:52:44.260
But, it's a learning management system, so it's not going to know.

00:52:44.600 --> 00:52:47.460
It has to be agnostic to the content, however ...

00:52:48.060 --> 00:52:55.700
it has access to the page title that we give it, so it uses that.

00:52:56.620 --> 00:53:02.980
So, they can do it, but what I didn't know is whether the screen readers would choke.

00:53:03.780 --> 00:53:05.680
[Dennis]: Yeah, no. They won't choke.

00:53:06.000 --> 00:53:09.920
I'm sorry, yes, you had a question?

00:53:10.240 --> 00:53:15.220
[Attendee]: There's all these systems that ... [indecipherable] ...

00:53:15.220 --> 00:53:20.080
like object embeds are probably what you are referring to? Those generally don't have problems.

00:53:20.780 --> 00:53:25.860
Again, it's the system that drives all that code, those things have to ...

00:53:25.860 --> 00:53:28.420
so like, take the old days, like the YouTube player.

00:53:29.240 --> 00:53:32.660
You'd use an object embed, and it would basically put it into a Flash player.

00:53:33.360 --> 00:53:37.300
Well, Flash itself isn't accessible, but the object embed is.

00:53:38.140 --> 00:53:41.580
So it's whatever is getting put into the page needs to be accessible.

00:53:41.580 --> 00:53:47.700
So, if I said my website is sethkane.com, which, doesn't exist, is accessible,

00:53:48.080 --> 00:53:53.940
but Dennis put an iframe on his website, and it was including my website,

00:53:54.380 --> 00:53:57.700
it would still be accessible, because mine is inherently accessible.

00:53:58.800 --> 00:54:06.140
So it's whatever renders into the DOM, the Document Object Model, as long as that is accessible,

00:54:06.560 --> 00:54:11.560
how its being delivered is irrelevant. That make sense?

00:54:12.060 --> 00:54:18.760
[Attendee]: [Indecipherable]

00:54:18.880 --> 00:54:26.960
[Attendee]: Well we also, say, like in our instance right now, we make decisions based on accessible-ready ...

00:54:27.620 --> 00:54:33.260
Like, if we're ... a booking appointment provider, for one of our clients,

00:54:33.260 --> 00:54:44.440
[Indecipherable]

00:54:45.600 --> 00:54:49.820
[Dennis]: And just so you know, on an eCommerce website like ours,

00:54:49.820 --> 00:54:51.920
we have third-party ads.

00:54:53.420 --> 00:55:01.080
None of them are displayed via iframe, but they are either displayed from Javascript or some other means,

00:55:01.460 --> 00:55:09.840
We require, since they are being presented on our domain, we require those to be AA compliant.

00:55:10.060 --> 00:55:13.060
Color contrast, alt text, everything.

00:55:14.240 --> 00:55:16.720
I'm sorry, you had a question?

00:55:16.720 --> 00:55:21.880
[Attendee]: Is there a reason people have to use iframes at all? They just reck havoc with the screen reader.

00:55:21.880 --> 00:55:27.060
[Indecipherable]

00:55:27.060 --> 00:55:31.020
... and I have to figure out a way to skip past the ad to go where the article continues.

00:55:31.020 --> 00:55:38.680
I know, JAWs has a ... I don't remember the command, but there is a mechanism in JAWs that you can say

00:55:39.040 --> 00:55:42.400
strip out all frames, and you can read the page, and it will just hide them.

00:55:43.720 --> 00:55:45.720
I don't think NVDA can do that ...

00:55:46.660 --> 00:55:51.820
... I don't know what Voiceover, if you could do it with that, but certainly can with JAWs, I hate frames.

00:55:52.820 --> 00:55:55.260
They are a hell for screen readers.

