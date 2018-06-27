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

Okay, enough time. Ecommerce websites. You're trying to purchase something. You get called the way .. you know, the dog just knocked over the aquarium. The first thing I could think of, I'm sorry. I don't know why that visions in my head. Hopefully that's not happening at home right now. Basically, provide users enough time to read and use the content.

So for just content, it could be, let's say if you have let's say a dynamic panel that's updating. If it's updating too fast and you can't read it ... I don't know about you, I'm one of the few people who actually looks at the credits at the end of movies. And you know, nowadays, they push the credits one third of the screen, and then they start the next movie and they're running this about 5 times as fast. It's like, "but wait who's the director of photography?" So basically, provide enough time. You could have this a lot on ecommerce websites. Let's say if you're trying to make a purchase. I'll get the hang of this yet. Let's say if you're trying to make a purchase. And, you have a session timeout. Ideally, you would provide a means for extending that timeout, so this way the user can continue. The problem is, what if you're getting pricing that's effective at that very moment? If the pricing changes, let's say you have an auction website, that pricing changes, well now that's no longer applicable. So this actually has guidance but it also has exceptions for when you do not need to follow this. So basically, you need to allow the user to turn off this time limit, adjust the time limit, or extend it. They should be told 20 seconds before the time limit expires. And then they should be allowed to extend it. It could be very well ... they can have communicated "press the spacebar" and the user can then extend their time by at least 10 times. Now as you can see, that might be very difficult.

Let's say, on an e-commerce website. So for that, we have exceptions. Real time exceptions, time limit is a required part of the real time event for at for example an auction. And no alternative to the time limit is possible. Essential exception, the time limit is essential and extending it would invalidate the activity. Again, think like airline ... I was trying to avoid talking about us but ... yeah, you know, if I can fly to Buffalo for $25 ... first off why am I flying to Buffalo? BUT, hey that's a great price! And then I hit timeout, I close that and now the fare is $189. So, you know, it happens.

[Indecipherable]

**[Dennis]:** Exactly, they're famous for timeouts. I don't know why I didn't think of them. And then there's a 20 hour exception. The time limit is longer than 20 hours. Go figure.

So ... pause stop and hide. For moving, blinking, scrolling, or auto updating information all of the following are true; Moving, blinking, scrolling information that starts automatically, lasts more than 5 seconds and is presented in parallel with other content, there is a mechanism for the user to pause, stop, or hide it unless the movement blinking or scrolling is part of an activity that is essential. Can anyone give me an example of moving, blinking, scrolling content that starts up right away? Stock prices, okay. Carousels.

**[Attendee]:** Temperature. Weather stuff.

**[Dennis]:** Okay. Anything else? You know what's my biggest pet peeve? Facebook.

[Laughter]

**[Dennis]:** At work. You're scrolling down the page ... and all of a sudden you get Rick Rolled. Hold it, hold it, oh wait ... now Rick Rolled ... Oh shoot ... Isn't it awful ... I've been practicing this all ... Hold on ... [Sigh] Waiting ... Of course, it doesn't happen like this on Facebook ... of course ... Waiting ... waiting ... you've just been Rick Rolled ... See Seth, wasn't it funny how, before anyone showed up, this was like, popping, like this ... And now, when you want Rick Ashley to be dancing and sing and does doesn't happen.

So basically ... we can bypass that of course because ... someone's going to be, of course, offended eventually here ... I'll show ... uhh ... raise your hands in favor of ... okay I didn't see any hands.

[Laughter]

So basically, for instance, video. So you have video backgrounds. How many of you run into a site with video background in the last week or so?

[Attendee]: Just video or audio?

[Dennis]: Video. It can be video and audio. So if you think of it, even if it's video, there's some people, who depending on ... I know I've seen video backgrounds where there's ever so slight movement and such, that can ... that can mess with people. So and they really should have a way of turning it off or stopping it. But to the point, to Rick Ashley ... you should be able to stop him. So obviously, with Facebook and Twitter and such, you have user settings to where you could, you know, change the default to where videos don't automatically play but in this case here we have an accessible media player called Able Player and then, now this is not a video background, but if you then wanted to see the video, you would merely ... click on the video and then once again ... this is hilarious to me. I'm sorry. It doesn't play, it just spins ... that's nice. That's ever so nice. Well anyways, you didn't want ... you didn't have to hear that. I'm just concerned about the next two videos that are later on. 

So here's another example. Now this happens to be the Twitter feed for this Meetup and these are live tweets that have been going out over the last hour or so. If you had a very active event, where you had a lot of updates, this content that is auto-updating over here would actually distract you from reading over here. So, ideally, you would have controls to stop that auto updating. Okay and then, again, for AAA for enough time, there would be no timing, you would not have a time limit on any part of the website. Again, I don't think that would be possible with e-commerce. I don't know what an alternative to that would be. No interruptions and re-authentication. When an authenticated session expires, an user can continue the activity without loss of data after re-authenticating. That's a great user experience, but how many sites do we have that actually do that? So I mean unless you're writing to cookies or some other means ...

Okay, seizures. I'll be honest, for the longest time, I always talked about seizures and you might think, okay, what in the heck on a website could cause a seizure? I like this, that it says, do not design content in a way that is known to cause seizures. And the idea is the three flashes or below threshold which says web pages do not contain anything that flashes more than three times in any one second period or the flashes below the general flash and red flash thresholds. So basically, flashing content can actually cause someone to be sick. Now this is the first time in two plus years that I've been talking about accessibility that I'm actually going to show an example. Now, this is about as serious as I'm going to get tonight. If you are impacted by flashing content and you can become sick, I'm going to ask you to close your eyes. Okay, I have a video here which, of course my luck will not play, but it's a video that actually at the very beginning has this exact same warning, and it's by a popular artist by the name of Kanye West. And ... I'll see, we'll see if this even plays here. Is the Wi-Fi wonky? Waiting for an available socket ... Let's see what happens and if not, we'll just bypass it. I can describe while this is going on, I can really describe what's happening. Wait while we change Wi-Fi networks ... I did not realize how many Wi-Fi networks we have here. And actually, I am not seeing this one. Yeah, I'm actually not seeing this one. So no worries.

So basically, what the video shows, where the problem comes about is there's this ... it's a black and white video, a young girl, wintertime, she's walking down the street, every, you know, t's black and white, there's snow on the ground and she turns around, there's a ... it looks like a housing complex behind her, and all of a sudden, the picture changes from red and green tints on the screen, and then I think the first word is Kanye, but it's every graphic design variation of it flashing and changing like every half a second. I don't know ... I have to admit, Kanye West is not my cup of tea, but when I saw the video, I found it very interesting that they actually had to have a warning in front of it. 

So, other conditions, and this is ... as well a AAA. Three flashes, web pages don't contain anything that flashes more than three times in any one second period. There's actually a website, I want to say it's out of New York, I've seen it at other conferences. They show it, it's like the noisiest, busiest site you've ever seen. And I'd be willing to say if I could find it, they have flashing content and it's all to grab your attention. I'm sure they have tons of lawsuits for making people sick.

Navigable. Provide ways to help users navigate find content and determine where they are.

So bypass blocks. Who knows what Bypass Blocks are? Raise your hands. Anyone know what a skip link is? We've got a few more. Ok, so basically, on every page of a website that you probably deal with, you have global navigation. Let's say, if that global navigation exposes the mega menu. Imagine navigating each page on that website you had to read that mega menu. That could be really irritating, couldn't it? You probably only have to hear it the first time and then you least know how its organized and where everything is.

So a skip link is literally just a typically, by default, it's hidden before the global navigation. And then it points to the the actual content. So in this case, we have anchor href pound sign content, so this would be content. Class visually hidden. Visually hidden is nearly a CSS class that keeps the content exactly where it is, but it hides it from presentation visually. Ok, and then it points to the actual content here. Some sites, when you tab and when this link gets focused it will actually display. Other sites just don't want it to display. There's nothing saying that it has to be displayed. I think it's a nice to have, because it's more than just people with visual impairments using screen readers who might need that. There's a lot of people who actually use screen readers who just have cognitive disabilities.

Page Title.

Guess how many pages on the Internet as of this morning have the page title of "untitled document?" It would seem that way... According to Google, twelve million, five hundred thousand pages. I don't know about you but untitled document is not all that descriptive. I can't think of a page that would benefit from that page title. So basically, provide a good descriptive page title.

Now, for anyone here who also does SEO, "Hello." If you want to be found, then you probably have pretty good page titles. Obviously not untitled document or new page, good ones would be basically a description of the theme of the page. Create an account. Semantic structure. And then of course it could be the site name or whatever.

Focus order.

If a web page can be navigated sequentially and the navigation sequences affect meaning or operation, focusable components receive focus in an order that preserves the meaning and operability. Just so you know, WCAG is written this way. And after five o'clock, I cannot pronounce half of these words in sequence. So ... So, if you come to this web page, you have four form fields; first name, last name, email and phone. What order would you expect the focus order to be? So first name, last name, it sounds mixed whether it be email or phone. So let's see how that works out. So first name, right? Ah, oh ... phone ... that's not good. That's not what I expected. Last name ... doesn't seem right. Email ... The problem here  ... you find out all my email addresses here ... there we go ... The problem here is that someone has used a tabindex attribute of a positive number. I have done this ... in 1998, I did this. I haven't done it since because whenever you use positive tabindex, you have to manually maintain that for the rest of your life. I don't know about you but I want to do as little work as possible. So if the business or the website owner decides that they want to add a field and they want to move this over here and put that over there, do you really want to go through all 137 form fields and change  the tabindex? No, never use a positive tabindex. Always use either zero ... having a tab index of zero and once again, this is only for elements that don't already get focus by default. So if it's not a link, if it's not a form field, then you would do this. Okay, tabindex equals zero puts it in the order in which it appears in the DOM, in the code order. Okay, so if you want something moved up, move the code for that up. If you have tabindex equals negative one it's ready. It's not focusable already, but when you have a script, you can then turn that on with the script, and then you can access it via the keyboard. Avoid using tabindex 1 plus Anything, any positive number. There's an article here that goes well deep into this excerpted from "Using the tabindex attribute" by Leonie Watson, who we saw the quote earlier in this presentation.

Link purpose.

I love this one. I'll tell you right now ... in anything that I touch and anything I do, I require Triple A on this. This is AA. You'll see why I say AAA. The purpose of each link can be determined from the link text alone or ... here's where I have a problem ... from the link text together with its programmically determined link context except where the purpose of the link would be ambiguous to the users in general. So, basically, this allows for surrounding text to make that link text unique. Anyone who uses a screen reader, most folks who use a screen reader have the ability to look at all the links on a page, and those links are called out by the link text. Many sites that you visit, that list would be "learn more," "buy now," "book now." Things like that. Click here. Oh yeah, I'm shivering from that. So, definitely make your link text descriptive on its own. That is AAA. This is AA. Go the extra mile and do it right.

So, I'm going to give you an example here ... to see the context for the link is not provided in one of the following ways ... in the same sentence, paragraph, list item, or table cells the link ...  or in the preceding heading or via suitable ARIA properties such as aria-label or aria-labelledby, then the user will not be able to find out where the link is going with any ease. If the user must leave the link to search for the context, the context is not programmically determined link tech context and is and this is not considered accessible. I go the next route. So and this will give you an example of this. So on the screen, we have three add tiles, let's say. We have, some of them have headings, I guess all of them have headings. So we have one that says "Small Business Big Savings." And then the text is "Save up to 30% off base rates with Avis for Business." And it's difficult to see here, but the call-to-action button says "Enroll Today." We have another one for AARP ... "Welcome AARP Members." "Learn more about our exclusive offers and savings for AARP members." The link says "View Details." This last one, "SUV's as low as $29." "Maximize your drive." The link text, "Learn More."

So again, screenreader users have a way to show a list of the links. So if you were to look at the list of links ... and if you couldn't see those ads, what do you think the list of links would be? Enroll today. Enroll today for what? View Details Details of what? Learn more. About what? So, you see where that link text is very important and very valuable. Now, it doesn't mean that you have to ruin your designs. It doesn't mean that you have to turn into Wikipedia or Craigslist or you know really text-heavy. You could do things like adding, what we call screen reader text. So you can still have your link, your details, And then, you have a span with the class of visuallyhidden. Our CSS class that basically visually hides the text. And then you can have "about AARP membership" and then close span, close anchor. So a screen reader is going to see "View details about AARP membership." Isn't that much richer? Now yes, ideally, that would be there for both screen reader users and visually. But if you can't get buy off on that ... at least do this.

Anyone here have a Wordpress site? Okay, we've got a few. You know the ... in a blog list, you got the headline, you got the excerpt and then you have, like, read more or whatever. There's now techniques where you can grab ... the article and just the through a screen reader text add it to the read more about and then the name of the article.

Multiple Ways.

More than one way is available to locate a web page within a set of web pages, except where the web pages is the result that doesn't oh, the web page singular, sorry, is the result of, or a step in, a process. This is my favorite site for multiple ways to get to information. This is Wikipedia. This is a Wikipedia page for the only Batman that matters by the way, Adam West. There's links here to everything that's on the page. There's links here to everywhere related content, relatable content. There's multiple ways to get to all this information. This, I view, is a fine example of multiple ways to get the content.

Headings and Labels.

Headings and labels describe topic or purpose. Ensure pages with groups of contents have headings. This is a little lenient on AA. It's more explicit in AAA. I think, where it makes sense, I think all pages with a lot of content should have that content chunked, and have headings for each of those groups of content. So in here, you have an h1, the page heading, of rental cars. h2 would be economy cars. Another h2 might be compact cars. Only one h1 to a page. I know HTML5 allows for multiple, don't do that. That can actually confuse folks. Stick to one h1 per page and then have all the rest of the headings on a page be subheadings to that. Labels. The same thing. Provide a label for any interactive component that makes the components purpose clear. Here we have first name, and many screen readers are going to read that asterisk as star ... "first name star." I've always wanted to do this talk sounding like George Carlin.I haven't worked that one up yet. Talk to me next year. You can sit there and have the meaning of this star, required once again, screen reader text required, and then you can hide it from the screen reader with aria-hidden. You can ... I mean it's a little extra work,  but it makes for a much cleaner, richer experience for all. I really have to admit, I can't remember why I put this out there. It's about labels. I can't remember my point so I'm just going to have to bypass that one.

Focus visible.

Okay, raise your hands if you're primarily a designer. Don't be afraid ... Okay, we've got about three. How many of you have removed the focus indication around links and form fields? I need to talk to you afterwards.

Don't do that.

Here's why you shouldn't do it. If you go to the site outlinenone dot com, it'll explain all the reasons why you should not remove the outline to links and form fields. I'm going to pray that this last video will play. This is Marcy Sutton. This is really when I got started with accessibility and when I saw that being working with an airline website, I was blown away and I showed this to everyone I could. She does a screen reader demo here, trying to navigate the brand-new Virgin America web site
that had just been redesigned, was getting a lot of press, it's so great so stylish and as you hopefully will see, completely inaccessible.

[video - screen reader announcing]

**[video - Marcy Sutton]:** "It's skipping before and after the calendar, and I can't figure out how I am going to book these dates."

**[Dennis]:** Actually, I'm going to go ... I'm going to skip backwards again, because actually this went too far in advance.

[video - screen reader announcing]: "Book link, tab"

**[video - Marcy Sutton]:** "I don't see where I am on the screen. I can't really tell."

[video - screen reader announcing]: "tab, tab, tab"

**[video - Marcy Sutton]:** "I'm just tabbing."

[video - screen reader announcing]: "sign out link tab san francisco link"

**[video - Marcy Sutton]:** "Oh, ok, I see that"

[video - screen reader announcing]: "tab, san francisco link"

**[video - Marcy Sutton]:** "Ok, I guess I'm departing from somewhere. I don't now what I'm trying to book."

[video - screen reader announcing]: "tab, los angeles ca ... link"

**[video - Marcy Sutton]:** "Ok, I guess I'll just leave from los angeles, that's not very convenient. I don't know how to use this website if I can't see it."

[video - screen reader announcing]: "tab, tab, tab "

**[video - Marcy Sutton]:** "Now, it just kicked me all the way back to the top, even though ..."

[video - screen reader announcing]

**[video - Marcy Sutton]:** "even though I should be on the screen. Oh ..."

[video - screen reader announcing]

**[video - Marcy Sutton]:** "There was an alert there, I don't know if you caught that, but, at the top of the screen, when something happened, I made a selection, and there was a big banner at the top, that said, 'hey, you made a selection. But it didn't alert me. If I'm not a visual user, I have no idea that occurred. So now, I''m further down on the page. This is part of the user experience that is very visual. But I have no idea where I am in this purchase flow."

[video - screen reader announcing]

**[video - Marcy Sutton]:** "I don't see Fort Lauderdale ..."

[video - screen reader announcing]: "new york tab san francisco tab all cities link tab"

**[video - Marcy Sutton]:** "That's not what I'm trying to find. Frustrating."

[video - screen reader announcing]

**[video - Marcy Sutton]:** "Ok, I must be related to the numbers down below."

[video - screen reader announcing]

**[video - Marcy Sutton]:** "I still don't really know ..."

[video - screen reader announcing]

**[video - Marcy Sutton]:** "So, another alert, didn't hear it."

[video - screen reader announcing]

**[video - Marcy Sutton]:** "Now, I'm on the calendar selection."

[video - screen reader announcing]

**[video - Marcy Sutton]:** "I'm skipping, before and after the calendar, and I can't figure out how I am going to book these dates. So, not only have I picked ... "

**[Dennis]:** Oh, Gee, I've lost everything now. Hello ... Isn't it great when you realize that you don't now how to use a computer? Ok, hold on ... I shall get us there ... we're actually not ... far to go now, as the saying goes. This is crazy. Ah, there we go. Good. One second. I don't now why I lost that. Normally, when I have these presentations, the screen just goes black, and I have no idea how to get it back. This time, I just lost my entire presentation, a whole browser. Ok, so, you've seen all that, you've done all that, let's get to where we were.

So as you see, with the focus indication, you see how important if you don't have it, how ... you know ... you're not going to be able to safely navigate a web page unless you can see where you are, if you're using a keyboard. So ... I think I spoke almost slow enough. Okay, so here's a real example. So we have different focusable elements. We have link text, we have our infamous right arrow, a graphical button. We have a form field and we have sign up. Now if I'm tabbing, you can see that the focus indication is blatant. Now yes, I'll admit you probably will never make it this "contrasty" on a site that you're doing, but you want to be able to tell at any time where you are. What you want to be careful of is if you don't have ... like this is all nice, black background. Or on a typical website, you would have a white background and maybe you'd have black text and such. That's fine. But what if you have a colorful website? What's going to happen to your focus indication? There you go. Can you see it? How about now? I could do an eye chart thing right now. Better ... or worse?

So, these are things ... so in this case ... you know last time we talked about color contrast, and we're primarily talking about text.

Text communicates.

In this case, focus indication communicates. So in this case, I would say you need to make sure you have proper color contrast. Okay, other items under this are location, information about the users location within the set of web pages is available.

Breadcrumbs.

You know where in the site that you are.

Okay, link purpose. This is what I was talking about before. This is a AAA. I believe that the link purpose should be solely within the link text. That's me saying that. I believe in quality, so in this case, it's not required for AA compliance, but I would say here, go the extra mile. Your users will appreciate it. And then, section headings.

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

