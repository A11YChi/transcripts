# Mobile site accessibility: the good, the bad and the ugly
## Gian Wild - Tuesday, July 26, 2016
[Source recording](https://www.youtube.com/watch?v=VTuioz4fzv4)

**[Dennis]:** Our speaker is Gian Wild, I'm going to read from here, because I spent a good half hour researching and writing this, so... Gian Wild is an accessibility industry veteran, having started back in 1998. She spent six years with the W3C Web Content Accessibility Guidelines (WCAG) Working Group and other associated groups, contributing to the development of WCAG 2. Gian speaks at web and accessibility conferences throughout the world. Additionally, she has spoken at the United Nations on the importance of accessibility. She is presently CEO of AccessibilityOz based in Australia. Please give a warm Chicago welcome to Gian Wild.

**[Applause]**

**[Gian]:** Well thank you for having me. I'm very loud, can everyone hear me in the back? Well, let me know if you can't hear me. We actually incorporated in the U.S. a year ago, a year and nine days ago, so we're actually a U.S. company as well. And, after that introduction I feel there's nothing left that I can actually do. But I have some great clients here in the U.S. and I'm really glad to be here in Chicago. And thanks to Dennis for organizing this.

So if you want to have access to tonight's presentation, you can go to a11yoz.com/2016mobile and that has the presentation, you can actually look at it while I'm presenting if you want and take notes.

Now unfortunately the system that I am using is not accessible to screen readers, but if you'd like a copy of this presentation, an accessible PowerPoint presentation just tweet me at @AccessibilityOz or come up and you can see me afterwards and I'll send you the accessible PowerPoint. That address again is a11yoz.com/2016mobile.

This is my team in Australia about a year ago. We've probably doubled in size. When I started AccessibilityOz in 2011, I had a mission statement which was to make the world a more accessible place and also to actively hire people with disabilities. And I wanted to target a percentage of my staff to have, twenty percent of my staff to have disabilities. So at the moment we're actually at eighty percent. So we actively hire people with disabilities.

We have two candidates and they have the same experiences, we hire the person with a disability. In some cases where we have a person without the adequate experience but they have a disability, we hire them anyway, We do really want to do what we preach.

It's also something that we do with our products. We have three products; OzART, OzWiki and OzPlayer, and they're all fully accessible. We don't release anything unless it's fully accessible. So in terms of my staff, we've got people who use speech-to-text programs, on screen magnifiers, keyboard-only screen readers, we've got people who have Epilepsy, I get migraines, both of those can be triggered by flickering content on websites. And people with Fibromyalgia and Dyslexia, so we've got a whole range of different groups of people with disabilities. 

So the reason why I'm telling you all that is it's not just about vision impairments. A lot of people think that web accessibility is about vision impairments. They specifically say, IE8 and JAWs, and it's actually a lot bigger than that. So just because your site is screen reader accessible doesn't mean it's necessarily fully accessible. In terms of our services, we do everything. That's web accessibility or digital accessibility, and as I've said, we've got three products. We were a reseller for BrowserAloud, I don't know why that is still there. OzPlayer, which is the fully accessible video player, which has just been purchased by Triple C Tech Center so all California community colleges now have and use OzPlayer. OzART, our automated testing tool and OzWiki, our database of accessibility errors, screen shots, code and solutions. And if you want to give me your email address at the end of the session, I can actually give you one month's access to OzWiki.

We've got over a thousand examples. A lot of the examples you'll see here today come from OzWiki. In terms of mobile ... there are a bunch of different accessibility features that people rely on when it comes to mobile. There are native screen readers like TalkBack on Android, Narrator on Windows, for those three people using Windows phones.

**[Laughter]**

**[Gian]:** VoiceOver of iOS. There's text-to-speech speech recognition, volume control, visual, auditory and vibrational notifications, haptic keyboard which vibrates when you change things, and zoom. So there's a whole range of different things
that people can do to make their web site more accessible on a mobile device. The system accessibility settings are things like font size, touch and hold delay, screen rotation, high contrast, assistive touch and mono audio.

One of the best things you can do to test your mobile app or mobile site is to pinch zoom and see if you can use the site. The other thing is to turn auto landscape mode and see whether you can use it. You'd be surprised the number of apps that crash as soon as you move into landscape mode. Now, when it comes to web accessibility, everyone knows about the Web Content Accessibility Guidelines. But they don't specifically cover mobile sites.

So, for example, WCAG 2 requires that everything be keyboard accessible. But it doesn't require that everything be mouse accessible. And it doesn't require that everything be touch accessible. So you could have a site that meets WCAG 2, but actually can't be used on a mobile device. So, the working group is addressing this at the moment, and they're talking about releasing a WCAG 2.1. It might be released in 2018.

So obviously, we still need to build web sites and web apps between now and then. So we've come up with our own mobile methodology. It's based on WCAG 2. It's also based on the BBC Mobile Accessibility Guidelines, which are an absolutely excellent resource. Just be aware that the BBC wrote it for internal use and the BBC is obviously not a for-profit system, there's not stuff on ecommerce and things like that.

So let's talk about Mobile usage. In 2014, people started spending more time on their mobile devices than than on desktops. So mobile is everywhere. WebAim does this great screen reader survey every year. And it peaked in January 2014 the 82% of people who use screen readers, also use the screen readers on their mobile devices. It's gone down a little, but that's because they widened the number of people that accessed that particular survey.

So, someone who is vision impaired, don't assume that they're just going to access your website on a desktop. In fact, we work with the National Federation of the Blind and they said to us, often we actually look at websites only on mobile. Because we don't need a big computer, we don't need a big screen, we can't see it. So we just plug in our little headphones into our mobile, and then when we get a mobile only site, and no way to drop that to a desktop site, we don't know whether we've seen stuff that might be on the desktop.

So, this is the energy rating site that we worked on a couple years back and it did not have a responsive site. It was not friendly on the mobile. It looked exactly the same on the mobile as it did on the desktop, except much much smaller, and it was impossible to use. But even so, nineteen percent of the people who visited that website, used a mobile or tablet to do so.

So, when we redevelop a site and turn it into a responsive site, that jumped to thirty percent. So, even if the site is terrible terrible to use on a mobile, people are still going to use mobile to access. Compared to Consumer Affairs Victoria, that have always had a separate m dot site, and they were at thirty percent in January 2014 and they are still now.

So let's talk about mobile-specific issues. So PDFs ... are probably one of the biggest problems with mobile cause you open a PDF and you wait ... and you wait ... and you wait ... and then you get something that looks like that. Most people who can't see it, it looks terrible. Its tiny text, it doesn't reflow, color contrast is bad, it's page two of a hundred and eight. Can you imaging scrolling a hundred and eight pages? And you can't search, might be an image, it's terrible. PDFs are terrible. I have a whole presentation about it.

This is something like this. HTML. It resizes, you can pinch zoom, color contrast can be changed easily, etc. And then, even maybe a separate m dot site, so this is a responsive site actually. So you can see, much easier to use than your standard PDF. Remember when it comes to mobile and PDFS, PDFS are much larger file size than HTML. You have a slow connection on a mobile, and so what that means is it takes longer for your users to download your content. It also increases their data usage. So, it equals up for customers. So, you should really consider being really friendly to mobile, and so actually having something like a separate m dot site.

So this is the energy rating site before we looked at it and then nice big icons, easy to use, etc. Another example. Energy Rating is kind of like your Energy Star. Other issues we see are Autoplay. Autoplay is incredibly inaccessible. It's one of the biggest accessibility failures of all time. There are four non-interference causes in WCAG 2 that you absolutely must not fail. Autoplay is one of them.

So this is actually Jamie Oliver's recipe mobile app. And when you open it for the first time, it takes you to your native mobile video player, and automatically plays the video. It doesn't have any captions, it doesn't have any audio descriptions, it doesn't have any way to easily know where you are or to go back. So this is a really really serious issue. Don't do this.

The other thing you don't want to do is this movement. So, slideshows are really annoying on a desktop. If you're not sure about whether you should use a slideshow, look at shouldiuseacarousel.com. But its even more annoying on a mobile. Because, often if people provide pause buttons, they don't on mobile because they have less room. But on a mobile, it takes up a lot more space, compared to the space you have on a desktop.

So, slideshows are incredibly problematic when it comes to mobile. So you must have a pause button. There are a whole bunch of things you need to do if you're going to have slideshows on mobile. And I do have an article that I have written about that. We also were commissioned to create an accessible slideshow by the Department of Prime Minister and Cabinet in Australia, and they're released it under Creative Commons.

It's a Drupal module and a WordPress Plugin if you are interested, feel free to contact us. Other issues are traps, and we see traps a lot more in mobile than we do on desktop. So, one of the big things is the on-screen keyboard trap, which is when the keyboard remains visible, no matter what you do. So, even if you are on a field, you need to have the ability to dismiss the keyboard, because the keyboard takes up almost half of the real estate of your mobile phone. So you need to be able to dismiss it, and look around at what you want and then re-open it. So this is an example of a mobile app where you cannot dismiss the keyboard.

This is Trello, where you can't dismiss the keyboard, but you're not actually on a form or any kind of field, so that you can't even escape out of it. It just shows up there. And as you can see, it takes up a whole lot of room. And there's this thing, we named it the hovertrap. This is where you have desktop-specific sites that are shown on mobile. And if you mouse over them on a desktop,  you get this beautiful zoomed in portion. So you see this a lot on clothing sites. What happens on a mobile is if you touch the item, it gives you that zoomed in portion on the right, but there's no way to close that. So, you can't actually get that image to ever disappear on a mobile.

So we call it a trap because, like a keyboard trap, you have to close the browser and start again. So, it's very serious. We've also come across VoiceOver swipe traps. We've never had problems with VoiceOver until we started testing it on mobile. So, this is LinkedIn, this is its status update. Basically, you are stuck on the arrow. There's basically nothing on the page. Really. You can't dismiss the page, you can't access the keyboard, you can't link back. You cannot do anything. With VoiceOver, you're only option is to close the browser and start again. 

YouTube also has a VoiceOver swipe trap. Just slightly different. Basically, what happens is, you're stuck in a search bar, the rest of the content is grayed out, and if you are a visual user, you can tap on that content and it becomes the top layer. But if you are a VoiceOver user, you cannot get to that content at all. So you're stuck in the search bar. Just because I feel I should pick on all the social media networks, the Facebook Friends List, you can open the Facebook Friends List with VoiceOver, but you should be able to swipe to go backwards, and you can't. You're stuck in your Friends List. And this is a touch trap. This is impressive. So, you can't actually move the screen, so you can't, you know, slide scroll. The only way to move the screen is to activate this little arrow at the bottom that doesn't meet color contrast requirements. And that throws you to the top of the page. So, we call that a touch trap. Mobile issues.

Ok, so, Coles. I actually ran this presentation, and I have a couple of examples from Coles. Coles is like your Walgreens. And Coles is notoriously inaccessible. There are two major supermarket chains in Australia, and Coles is one of them. The day after I ran this presentation at the Future of Web Design in New York, Coles, there was a law suit started in Australia against Coles for their site not being accessible to vision impaired people. The problem with this app is that you have these buttons down on the bottom, and it says Lists, Specials, Product Finder, More. And they're coded as buttons. But they don't have any alternatives. So VoiceOver reads them as button button button button. Access. So, you need to make sure that you specify your inputs correctly. 

So for some reason, Elance had decided they were going to create their own little drop-down, that doesn't follow any HTML rules whatsoever. So you can only choose 14, 15, 16, or 17, because it's recognized as a keyboard input field, but there's no ... there's actually a select that you need to do. So if that had been coded as a select the mobile would have recognized it as such and would have shown it to you in a much friendly way. Text size is probably my biggest one. I actually can read very small text size, but this is ridiculous.

This is the Etsy. And it looks like maybe four point. And there's no way to increase the size. This ... is probably my favorite. No, actually Coles is. So this here is the app that you get when you fly from Australia to Los Angeles using Virgin Australia. And down at the bottom here, is ... your longitude, your latitude, how many hours you've been flying, how long until you arrive, etc. etc. But this text is so small, that you cannot actually, I can't read it on a mobile phone. And it doesn't allow pinch zoom. So, someone built this. Someone design it. Someone coded it. And at no point did they actually look at it on a phone, to determine it was unreadable. So, when you have text size, you need to make sure that if you're going to support the system settings on the phone, that they make sense.

So, this here is the iPhone with the smallest text size. And this here is the iPhone with it's largest text size. So you can see that AccessibilityOz is basically cut off. So if you're going to support the system settings in your phone, make sure you test with those system settings.

This is another example where basically the "Discover," "Cuisine," and "Open for" are cut off. And this is, you know, even Apple couldn't get it right because this is the part where you increase the text size. So on the lowest it says "Apps that support Dynamic Type will adjust to your preferred reading size below." And then when you put it on its largest, it goes "Apps that support Dy...", because there's not enough room for it. They have actually fixed that particular error. 

Ok, so then you do see mobile apps that have large text. Or have a way to increase large text. So you can see that's not really large text. That's  moving from a size 8 font to maybe a size 10 font. That's not large text. In-app settings, so BBC news for example, doesn't support the system settings in an iPhone, but they have their own feature to increase text size. But if you look at it, that's not really particularly large. That's going once again form maybe a size 6 font to maybe a size 11 or 12 font.

This is the ABC website. Once again small is very very small. Maybe 2 or 3 points. And large is maybe 12 or 14 points. But the important thing is that this is a small font and this is the large font. So, your titles and your who's written it and your captions are all the same size no matter what setting you selected. And you'd think, maybe the title would be, one of the most important things you wanted to make large.

Color Contrast. Gray text on a white background is a bad idea. Hardly anyone can read it. We do user testing, people don't know ... everything about that search bar, it's gray text on a white background. They don't see it, they won't know where to put their search. Now this is Amazon. You know, basically this is the way that people are going to find things, and yet it's gray text on a white background. Gray text on a gray background. Search eBay, is also bad. 

But probably worse is LinkedIn, which is like a medium gray text on a light gray background. And this is just how close these people are to you in terms of your profile. So, Kare Romanski is a first degree, Jake Mitchell is a second degree, that's the kind of information that I, as a specialist might want to know. I might want to say, ok, I want to reach out to Steve Lee. No, well, I'm already a first level person. Well, if I can't tell because of the color contrast, then that is information I'm missing out on.

Color alone is another problem. So, today's date, marked in blue where everything else is black. You're assuming that people don't have
color contrast issues. But it's also something that probably won't get read aloud to your screen reader users. So this is even worse because this will just be a little image and these will be colored table data cells. So that information is not going to be available to a screen reader at all.

Maybe this is my favorite of the examples. So Kmart. Do you guys have Kmart?

**[Audience]:** Yes

**[Gian]:** So, this is the Kmart website, and this here is a link. You activate that link, and you get an empty page. You get an empty page because it links to a Flash catalog. Flash is not supported on iOS devices, and hasn't been ... forever. So, they obviously never tested this. But not just that. In all Western countries, iOS devices are by far the most popular in mobile and tablet devices. So, at what point did anyone look at this? And say "Oh, it's not even loading?"

Zooming. Zooming is a big problem. People zoom a lot on mobile or tablet. This is Airbnb. As you can see, it just overlaps and underlaps and looks terrible to the point where you can't even read some of the contents, to the point where you can read anything at all. So you say ok, fine. I know I'm on the mobile site, I'll just go to the desktop site. And then, it loses all of your information. So you can imagine your searching for something, you found it and you just want to zoom in on something, it crashes. You go to the desktop site. You've lost all of your data.

Functionality unclear. So is this one way or is it return? So, using color, alone, to convey information is problematic, but even if one was underlined and not underlined, its still a little bit unclear. Now, if it's going to be unclear for the general public, it's definitely going to be unclear for people with disabilities. This one, I can buy a warehouse trailing floral dress I can select from zero to dot dot dot. Now I'm not going to but this dress, because I don't know what it is that I am selecting.

Ah, so, now we've got Commonwealth Bank. So, if you click on that, "Call Michael," it makes a phone call, uses your phone, very clever. So you think, Michael dot Dikeakos at cba dot co dot dot dot because the email address is so long and they can't fit it in, that maybe if you hit that, it would open your email... doesn't do that. These email addresses, that aren't displayed properly, are not active. Whereas this is.

Most people think that if you mark something as gray, it means that it is inactive. So, here we've got add a message, name, email, phone, postcade all in a light gray on a white background. Almost impossible to read. So they seem to be inactive. But they are actually active, if you tap on them. But, of course, VoiceOver can't catch them. 

It's also important to think about how people will use your systems. And that they might use them differently to what you expect. So YouTube for example, is a responsive website. So if you increase text size, it will eventually turn it into what you see on a mobile. Now, someone at YouTube has decided that, if you're on the mobile YouTube website, at no point are you ever going to want to upload a video. So, if you zoom in on the site as in Control Plus, you lose your upload button, and your notifications button. So you cannot ... if you're zooming in, you cannot upload a video to YouTube.

This is Asana. Asana has this great featured called My Tasks. And this is how I get everything done. If it's not in My Tasks, it doesn't get done. Well that's great. Except for ... the mobile version doesn't have My Tasks. So how can I use it? So now we use Trello.

This is Row in New York City. I put this example here because Future of Web Design put me up and we're in New York City. And this is the mobile version, and this is the desktop version. So the mobile version has all your navigation, but it's got this big image about how do you create your New York City and it links off to how do you get access to Times Square or how do you visit MOMA and all of that kind of stuff. And none of that is on the mobile site. So you can image, you're looking at, where you're going to stay, and you click through, and "awe yeah, excellent, that's great." and you're on your way to New York, and you check the mobile site
to figure out where is it you want to go, and that information is not there.

Pixelation on zoom. This is a mobile magazine, which you get for free if you fly with Virgin Australia on a local flight. They give you free access, assuming that you'll love the magazine so much that you will buy it. And yet, the books that it's promoting are so pixelated you can't even tell what the title is. This is another example about a Self-Worth Circle. And the only thing that is actually readable is the word "negative."

Source order. Source order is really important on mobile. So these are requirements on WCAG 2, a lot of people aren't aware of them. So this is Lion King. Tickertech call, whatever your ticketing system is. And you think ok, so you select those things, you hit Find Tickets. But, there's a whole bunch of information that's underneath that button. Not only color contrast, but especially the stuff about accessible tickets and how you have to go through a deeper process if you want an accessible ticket. But, you wouldn't think to scroll down, because it looks like a complete page, it looks like you reached the end of the page. So, be aware that no one is going to look past your submit buttons. 

To the point where, I was using this on my tablet, and you can see, you can see that there's options for room number, last name, continue button. Or you can have an access code and enter it here. So, I put in my room number, and I put in my last name, and I hit Continue, and it said you don't have access. I was like, no, but I do. So, I put in my room number and I put in my last name, and I hit continue. I said, but I do have an access code. And I couldn't believe I did not see, even though it was visible on the screen, because I was just concentrating on what was above the submit button. That's something I do, then it's going to be even more serious for, say for a screen reader user who takes much longer to go through a page. They're expecting the end to be a submit button, and that's where the end should be.

This is another example, LastPass. I was purchasing Internet access on this Virgin Australia flight, no, it wasn't Virgin Australis, they don't have Internet on the flight. United. And I put in my email address and I put in my password, and I hit login. And it said "No network connectivity detected." I was like, I know it's on my phone, it shouldn't need network connectivity. What I had to do was select the option down below underneath the submit button Login Offline. Now, there are requirements for error suggestions and error descriptions in WCAG 2. In order for this to meet WCAG 2, you would say "No Network connectivity detected. Would you like to login offline?" It makes sense for people who don't ... and I probably did this process three or four times before I realized that was there. And I could see it the whole time.

Touch targets. So, this is Twitterific I think, and it's important that when you have an active element on a mobile, that it is a certain size. And these are not large enough. So, they're what, maybe, four pixels by four pixels, maybe eight pixels by eight pixels. The BBC has some great recommendations on size. But they are so small that you have to hit them several times before you actually have activated one.

This is my favorite. This is the zoom of doom. This is a Cole's site. So this is basically a map that shows you where Coles is in Veepoon, which is a long way from anywhere. But, if you scroll, swipe in the map area, it moves the map. If you want to move the page, you have to manage to select this small white area around the edge of the map in order to move the page. The other thing you have to do with touch targets is you need to make sure they're activated on removal of touch, not on touch.

So, Coles again. So let's say I just want to scroll up this point. If I scroll, sorry, if I swipe, and I hit South Australia on that swipe, it will automatically jump to the South Australia stores, even though I might be using the swipe gesture. The other problem with this, is that every single Coles store in Australia is listed on one page, and there's no back to top. So there are thousands of stores listed here, and there is no way to get back to the top of the page to choose another state, unless you scroll. And it took me eight seconds.

Spacing. Ok, so you really don't want to put your edit button right next to your Mark Complete button. Because they're opposite actions, and people accidentally click things that they shouldn't click on mobiles devices much more than they do on desktop. This is even worse. In order to get rid of this install Airbnb, to have to click this tiny little close button. It's about four pixels by four pixels. If you click anything else, it will install the app.

Then there's things like just lack of testing, which probably covers a whole lot of things that I've talked about today. Best of YouTube. VoiceOver reads it as Best of YaToob. This is Target, which is ... I think you guys have Target too. So if you activate this little image of ... game ... video games, it gives you this your search for 56626957 56626872 56626940 56626841 found four product results. Well actually, no.

This is Coles. This is a mobile website. And, you know, you can't actually read the text at all, it's just squished. So no one looked at it. No one tested it. This is where one of my favorite dress shops are. Take me to the map, and it's taken me to the latitude and the longitude, not the actual address.

This is Kmart. So according to Kmart, Australia consists just of Western Australia, because the rest of it is off the screen. Same with Dish.com. We deliver to Sydney and ... well, I guess you deliver to Sydney. 

Drupal, so once again, you have overlapping text, on a major iOS device, it's a problem.

Spelling mistakes. So "10 cafe ustomers that are more annoying" ... they are going to really annoy people on mobile much more so than on desktop. Now this one is interesting. This happened about two years ago. All of a sudden, there was HTML code in all the Facebook headings. And it lasted, for some it lasted two hours. Crikey it was like this, Crikey is kind of like our alternative newspaper. It was like this for about two weeks. So the heading is span class equals qou end span why sacrifice yourself whistleblowers dot dot dot. Now what happened? It's not like everyone got together one day and said "Let's put HTML code into our Facebook headings." It's that that's what was posted into Facebook, and Facebook changed something and then all of a sudden, that HTML code is showing up. Now, some people picked up on it quickly, some people took two weeks. You don't want to post broken links. People don't like broken links.

And, this is ... we get to Los Angeles Airport Wi-Fi Internet Access. Were you disconnected? Click here to reconnect. Time left twenty four hours zero minutes This page will redirect, so content doesn't really make sense to have here.

**[giggles]**

**[Gian]:** And all of a sudden I don't want to give you my credit card information. You need to be careful with errors.

Triplify.com description reference error can't find variable triplifymap file http www triplify dot com slash js slash display results dot js etc. etc. Give something meaningful to users.

This is Green Apple Books. I'm ... I've got a library at home. I love real books. I can't read books on [garbled]. This is the Green Apple Books mobile website. So not having an open day and half the map is off the page, half the information is off the page. The same with their events, on this specific mobile site. But if you went to their desktop site, it worked. So once again, you need to make sure you test these things.

This is Qantas. Because I don't want to pick just on Virgin Australia. So this is where you choose where you want to fly to, and from. Now Qantas flies everywhere. And so it says select city, and it starts at "A." Aberdeen ... Abidjan ... Accra ... Addis Ababa ... it took me twelve seconds to scroll down to Melbourne. Ok, so that's all the things you shouldn't do, not all the things, some of the things,

So I want to talk about correct implementations. This is Twitterific. So it is actually large text. But it also allows you to change the color. Now, it's interesting to note that people who have Dyslexia actually like to reduce color contrast so even though people with certain vision impairments like to increase color contrast, there are groups who want to do the opposite. So the ability to choose color contrast is quite important. So your iMessage actually supports large text size.

And this is our website. So you can see in the main area we change the color contrast and things like that. Talks about outline etc. etc., and can zoom in so much that you can see only two letters at a time and there will be some people that need to have that level of zoom.

This is State Library New South Wales. So you've got this old photograph of people in Melbourne or Sydney. And you can zoom in and still get quite good quality information. Also, when it comes to desktop, you can move your mouse around, and see that it changes to indicate that something is active. You can't do that on a mobile, so you can't assume that people know when there's more functionality. So these people at Time have put this little tap text to indicate that you can tap on that and it gives you more information. Not quite sure of the point of this, but it's still a good idea.

This is The Guardian and it has that little arrow icon, and it takes you to what you would think would be a larger version the image but it's the same size. So I'm not quite sure why it did that, but at least it indicates that you can open that image separately. So this one has a "Done" option on its keyboard, it also has previous and next. So you can actually jump through your fields using mobile. And correct inputs. So, whoever coded that field, coded it as a telephone field and therefore the number keypad on mobile shows up.

So this uses color and shape to indicate what dates you selected. So you still would need to place some stuff behind make sure it gets read properly by the screen reader. But, by using changes in color and changes in shape, your covering people who have color contrast issues as well.

I mentioned the BBC Mobile accessibility guidelines. They're easy to find. There's also a whole bunch of OzWiki accessibility factsheets that are freely available, and Dennis has been tweeting them out all week. They're quite in-depth, especially the JavaScript one, is incredibly in-depth with demos and stuff you can use. And we also have this thing called OzWiki which a lot of these errors came from, and if you'd like access, come talk to me.

As said, you can get this presentation on a11yoz.com/2016mobile and, any questions?

**[Gian]:** Yes.

**[Attendee]:** A common thing I see is when an app displays a message on the phone and it disappears from the screen. I'm running into that. And then I'm telling the developers, ok, if your using a braille display, you won't be able to read it because the text isn't there anymore.

**[Gian]:** Yes, so we saw that once or twice maybe five years ago. And in the last six months, it's just everywhere. Having errors disappears after a period of time is problematic. I think it's actually ... it has to do with the use of HTML5 form elements. Yeah, but it can be problematic. It's a very big issue.

**[Attendee]:** I was dealing with it all day.

**[Gian]:** Any other questions?

**[Attendee]:** So you mentioned the ... unclear functionalities. I'm just curious, what would be the best approach to making sure each button or tab is active? Would it be just changing the color and the shape of the button? What is their task?

**[Gian]:** So, the question is how do you, for the people on the call, how do you indicate what's active and what's not, maybe on a tab or on the one way versus return. It depends on what you're using. Tabs is a little bit easier because there's a whole bunch of ARIA roles around tabs that will get read to screen readers.So you know that will get read properly to at least one group of people. There are things that you can do, like a little arrow, for the tab that you've got indicated, if you have it in blue with the little arrow that points down, I've seen that happen a few times. Also, repeating the content as headings. So if you have one way of return and then something that said one way, that's another way of doing it. Yeah. I'll see if I can ... there might be some examples in OzWiki. Let's me see ... I'll see if I can find them.

**[Attendee]:** I think it was an autoplay feature, I think it was enlarge image feature you showed earlier in the slideshow. You were saying that one of the accessibility problems for that is that it would take up too much space. Would that take up too much data usage on a cell phone as well?

**[Gian]:** I think you're probably talking about movement. So Facebook is the perfect example of this. The Autoplay video function on Facebook chews through data. First you've got movement that can't be stopped by the user, which is one of those non-interference clauses, but also it uses a whole lot of data, a whole lot of bandwidth, so yeah definitly that would really be a problem.

Any other questions?

**[Attendee]:** With larger institutions in this country anyway, you tend to have the developers overseas. Primarily the Asian countries. As my function as a designer, I'm never going to know all of this. What ... is there a wiki that you have that is specifically for designers to be aware of? Because, communicating with Asia is ...

So, yeah. OzWiki is ... OzWiki can definitely be used by designers, but it is definitely more aimed at developers. I have written a couple of articles about accessibility in the web development lifecycle, I talked a little bit about what to do with design. I do have a blog post on design as well. But yeah, so have a look at the resources section of our website.

**[Attendee]:** If there was one thing that you would say, or that mostly pops up, like I know know that everything that you do is important as far as accessibility, but is there one thing that stands out more, like even if you said if you do one thing, what would you say that would be?

**[Gian]:** Make your site keyboard accessible. Because if your site is keyboard accessible, then at least, theoretically, all the features will be available to assistive technologies. They might not be read out properly, but at least they are all there.

**[Attendee]:** You mentioned earlier that using HTML5 form elements would not be a good idea with regards to accessibility. Are there any other HTML elements or HTML5 tags?

**[Gian]:** So, I'm glad that you said that. So, definitely use HTML5. HTML5 is fantastic. It has some problems, but you can't rely on HTML5 to meet WCAG 2 for you. So a lot of people for example ... one of the requirements in WCAG 2 is that you need to indicate where your users have not completed a field. If you just rely on the required option in HTML5, then it will just pop up and then just disappear, that's probably what this guy has been dealing with. You can use HTML5, and then use that required equals required, but then you also need to code in, you know, this field is missing information.

**[Attendee]:** But like, is there any tags within HTML5 that you wouldn't say like, wouldn't be like recommended as accessible, because I know that you where talking about the form element that like with the form tags, like HTML5, that would cause like accessibility problems. 

**[Gian]** So, it's ... There is a factsheet on HTML5 that I've been told is out of date. So I haven't looked at it lately. One of the things that I disagree with HTML5 is the removal of the summary attribute in tables. But what I would say in general is anything that you can do in HTML5 that you can't do in HTML 4 you need to code that in, separately, until the browsers have a better way of interpreting HTML5 elements. 

Placeholder is also another problem. It's how people use it. So, a lot of people, instead of having a field label, a visible field label, will put the field label as a placeholder using HTML5. That's not the technical way you should use it. It's also incredibly inaccessible. So it's more how people are applying HTML5 than HTML5 itself. Any other questions?

**[Attendee]:** I have a question about image size, because you mentioned zooming in. So, but if you're actually trying to scale for devices, how do you go about that? Because you don't want too large of an image because it will use up data, versus the ability to zoom. 

**[Gian]:** You just have to be very careful with breakpoints. And you need to be ... you need to do a lot of testing. You should really, when you're designing a responsive site, design each breakpoint. So, design at the desktop size, design at the nine sixty by seven sixty eight or whatever, and know that's how your site is going to break at those points. And that way you'll have a design that needs to be followed for certain sizes.

**[Attendee]:** But I mean in terms of the data usage. Because you really don't want to put ...

**[Gian]:** So I'm not technical, I'm not a developer... I don't know how that would work, actually. It could be something that you ... it depends on what people might ... like you might know what images that people zoom in on. On certain content.

**[Attendee]:** There are new picture elements. I think the picture element is for more art direction. But the source that you can actually use on images, on the image tag, will let you supply a different image for different screen resolutions. I don't know if it detects what kind of bandwidth your users are using, but at least it can detect what screen resolution they are using.

**[Attendee]:** Right, but if you want to zoom ... so the thing is that zooming ... so you have a source that is set for a certain device width, it would serve up a smaller image.

**[Gian]:** Good. Great. I'm glad someone figured that one out.

It also depends on the content that is in the image. If it's an automated image of a couple having coffee, then people aren't likely to zoom in on it. If its your logo or mission statement, something like that, maybe that would inform the site.

**[Attendee]:** Yeah, I was wondering, this is all most concerning mobile devices, phone, tablets, but there's now, around the corner,
the wearable devices too?

**[Gian]:** Yep.

**[Attendee]:** And do you have an opinion or vision on that? And how to deal with that?

**[Gian]:** Yeah, if my job wasn't interesting before, it is going to be soon. Wearables are very interesting. They ... I think that people will have to accept that there are going to be some wearables that are not ... going to be useful to them. So, for example, someone who's deaf might find a wrist, a smart watch very helpful, vibrates when you get an email, vibrates when you get a call, that kind of stuff. But I think there's probably... just going to have to be an acceptance that a smart watch is not necessarily going to be all that helpful to a screen reader user.

Yes please ...

**[Attendee]:** Actually, you can use Apple Watch. There are people who are working on, I know of one instance where a company in South Korea is working on a watch with a small braille display that pairs with your iPhone so your iPhone memorizes speech output with VoiceOver.

**[Gian]:** Yeah, and I mean I see a lot of people with vision impairments just hang their braille display around their neck so it kind of operates in that way anyway. You wanted to say something?

**[Attendee]:** I was just going to ask a question based off of what he was saying about wearable devices. I was wondering, can some wearable devices be coded in HTML5 or would it just depend on the wearable device?

**[Gian]:** I think it would depend on the wearable device. I would expect that at some point there would be wearables that are HTML, that show websites.

**[Attendee]:** Is there any country that you've noticed that is in the forefront, compared to others, with regards to accessibility?

**[Gian]:** No.

**[Laughter]**

**[Gian]:** Look, Australia was really good about five years ago, they released this thing called the National Transition Strategy which said basically if you don't meet your accessibility requirements, such as WCAG 2, we're going to turn your domain off. So, that was a pretty serious thing. They never actually did that, and then people actually realized that they weren't going to do that, so people kind of gave up on accessibility. In a lot of ways, the U.S. understands accessibility a lot more, in terms of things like the need for automated accessibility testing tools, the need for a university developing policies and procedures, things like that. We're still at the stage in Australia, we meet with universities and say, "so let me explain what web accessibility is." So the U.S. is leading the way, and one of the reasons is litigation.

**[Gian]:** Yes ... what's your name, sorry?

**[Attendee]:** Me?

**[Gian]:** Yes.

**[Attendee]:** Dan.

**[Gian]:** Okay, Dan.

**[Attendee]:** The problem in the U.S. is Congress will pass laws or there'll be executive orders, and then the Justice Department steps in and say we need to get public comment or we need to do rule making and the things get delayed for years.

**[Gian]:** Well, I think it was very interesting that the Department of Justice is sending out letters of accessibility compliance referencing WCAG 2, even though WCAG 2 is not on the law books. It's still Section 508, but in reality, you need to be following WCAG 2. Which, of course, is a problem because it doesn't handle mobile very well

**[Attendee]:** About making a business case for accessibility in a company, where does accessibility provided the biggest benefits? Outside of what we kind of know the obvious? With SEO or anything else we could push ... you know it could help us out in this other

**[Gian]:** So, definitely, Google rankings. So, not so much optimization, but if you have an accessible site, it's going to be able to be scanned better by Google. So, for example, and it's going to be ranked higher by Google. So, sites that contain videos that have transcripts earn 16% more revenue than sites that have video without transcripts. That's basically because Google could search the transcript and rank them higher. Whereas Google cannot search a video. Completion of a video, like watching it to its end, doubles of that video has captions. One of the things the BBC found out was eighty percent of people who turn on captions, are not deaf or hard of hearing. They call it the Broadchurch effect. It's basically THL Broadchurch. The accent was so strong, half of England couldn't understand what they were saying. But it's also helping, like, I spent ten minutes looking at my Facebook page this afternoon. And I was in Starbucks, and I did want to play a video and I wasn't going to watch video unless it had captions. So, there's a whole lot of ... and also, a page that has video, will be ranked much higher by Google than a page that does not have video. So, there's a whole bunch of things around that.

**[Attendee]:** Do you have a good example of a site that gives users choice about their experience? For example, what kind of contrast they would like to have when visiting today?

**[Gian]:** We worked on ... Anti-Discrimination Commission Queensland, and I believe they have options for color contrast and text size. And they ... also won an Australian Web Award.

**[Attendee]:** I'm working with a vendor and I'm trying to explain this concept, and they couldn't get the idea. And I thought if I could just show them one.

**[Gian]:** We did some work with... Griffith University in Queensland, and their corporate colors are red and white. And they decided that instead of just giving users the option to increase the color contrast, that they would give users the option to choose they're own color contrast, and they found that, I think it was something like eighty-two percent of people who used the color contrast feature, actually reduced color contrast. So ... I'm not sure this is going to work. So, at the top you've got your colors, so you can choose different colors, you've got text size, and you've also got BrowseAloud. As I've mentioned, we're no longer a reseller, but it is a great product. It allows you to basically, it's a screen reader, it's a screen magnifier, it changes color contrast, everything, so there's a whole lot of things it can do.

**[Attendee]:** And that is accessed with the button in the upper right?

**[Gian]:** Yeah, this thing. And you can pick it up, and it stays ...

**[Attendee]:** And it's sticky?

**[Gian]:** Yep, it's sticky.

**[Attendee]:** So you're in fact creating almost a kind of white-label effect for every user.

**[Gian]:** Yes, so this is the like, text version only. And then, um, my volume is off ... So it reads aloud and ... as soon as the ... 
I can't turn my volume on for some reason, but it is reading it aloud. And it's zooming at the top as well. So yeah, it's a lot of things that Browsealoud can do. It's aimed really at people with moderate vision impairment, so even though it has a screen reader, it's not for people who are completely blind. And it's also aimed at people with cognitive disabilities. So they've found that comprehension of a web page, they did a study, comprehension of a web page increased by eighteen percent when people used Browsealoud versus just reading a web page. And it's quite useful because you don't have to identify as a person with a disability and go off and find an assistive technology. If that button is on your web site, people might play with it and find that it helps them without having to go through that process. And it also is aimed at people with English as a second language, so it can translate into a bunch of different languages as well.

**[Attendee]:** What's it called?

**[Gian]:** BrowseAloud. So yes, it's got a whole bunch of highlight things and ... I haven't checked the new one so I can't tell you all the things it can do.

**[Attendee]:** Is that something that you have to pay for?

**[Gian]:** Yes. If you want more information, feel free to contact me. Because we just implemented on the rudenman rights web site, the disability rights Washington, we just built them a website. So we can get you in contact with the right people. Any other questions?

**[Attendee]:** Does that work as a plug-in then?

**[Gian]:** It's basically JavaScript code, that sits on top of your web site.

**[Gian]:** Any other questions? Well, thank you very much.

**[Applause]**

