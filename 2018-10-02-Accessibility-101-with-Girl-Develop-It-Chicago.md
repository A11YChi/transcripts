# Accessibility 101
##  with Margie Chubin & Girl Develop It (GDI) Chicago - Tuesday, October 2, 2018
**[View recording]**(https://www.youtube.com/watch?v=-tH8QpIdU_E)

**[Narration]:** The Chicago Digital Accessibility and Inclusive Design Meetup presents Accessibility 101 with Margie Chubin.

**[Margie Chubin]:** So as Dennis said, this Accessibility 101. I've been coming to this meetup for a couple of months, so I'm a little bit new to the field, too. But I've been studying accessibility for like a couple years. As Dennis said, use that hash tag, it's really awesome. Definitely follow what he's doing on Twitter, because he's always tweeting out really great links too. And then, I also posted my slides at bit.ly/Margie-A11Y101

So as I said, my name is Margie, my pronouns are she her hers, I forgot my button, I do have one. I'm a Software Engineer at Sprout Social. I like cooking, traveling, eating food and also eating food while traveling. So here's a good picture of me eating food in Rome. I was really happy about that.

So my Twitter handle is @MargarineMargie. Fun fact, somebody asked me if that was what my name was short for, and I said "nope that's a substitute for butter."

**[Laughter]**

**[Margie]:** So that's how I came about a couple of years ago. So as I said, my slides are posted online. We can share that link, so you can look over it my content later, click on my links.

So as Dennis also said, this is a promo for the Web Accessibility Class that I am featuring on Saturday. I'm really excited to get really deep into a lot of these topics, but today we are just going to do an overview and it will be really fun.

So our goals for today, we are going to learn about different types of disabilities, maybe the challenges that they face, how we measure accessibility, and then how designing and developing with accessibility in mind will improve the web for everyone

So why accessibility? Why you guys here? I don't know.

So here's my definition for today, that web accessibility is making our products as usable by as many people as possible, including users with disabilities. So we want to ... we know that it's not perfect right now, but we want to intentionally include everyone especially users disabilities, and we want to fix it because we know it can be fixed.

So let's go over "a one one y." What is that, I've seen that everywhere. I found this picture here. It shows how there are 11 letters between the "a" and the "y," and that's where we got accessibility ... "a,"  11 letters, and then "y."

So we're here because we can't assume anything about our users. If you work in product at all, you know that your users don't look like you. They don't have the same abilities, they're not in the same context, they might not be using a keyboard or a mouse or a modern web browser. Maybe they're on IE11 and maybe they're not even on a desktop computer. Maybe it's on their mobile device.

So there's a lot of things that we can't assume, this is why we do user research, user testing, we test what we put out to see if people are actually using it. So we have to think about users with disabilities in the same way. So some of our users might have disabilities and they shouldn't have to out themselves,

They shouldn't have to say, "I have a disability and your website it's not useful for me." They should just be able to use your website. You shouldn't say you can't come in the building because I don't have a ramp for you. You should just let everyone in your building.

So yeah ... So I've got the social model of disability up on the slides here, and it is that disability is a mismatch between an individual and the environment and this is in contrast to the old medical model, which is that people need to be fixed. So we're not saying, you are deaf, you need to go fix yourself, or it's your fault that your a dog person. You're deaf, so here is a space where you can also be included by providing captions.

So we're here because the web has barriers to some people, and we want to fix that. We want to make sure everyone can come in our buildings. So we all experience disabilities, sometimes. So we're going to talk about temporary disabilities. In what way have you experienced a temporary disability in the past few weeks? There's some examples to the right, such as you temporarily broke your arm, or you have an ear infection and you can't hear. I'm getting over being sick because the weather keeps changing, so my hearing's a little down. Maybe there's a bartender shaking something right next to you and you can't hear what your friends trying to say.

So temporarily, we're all disabled, all the time, and that gives us a little bit of empathy, but it can't really like give us the full experience of disabilities. But it's so important to think about that anybody can be disabled at any time and we'll just think about that as we go through with talking about disabilities.

And then, the other thing we obviously have to mention is inclusive design. So this is where we all benefit when things are designed more inclusively. Better design, making things more simple, that's going to benefit everyone, not just users with disabilities. An example that a friend in this room mentioned to me the other day was the crosswalk buttons that make noise when it's time to cross the street. So you can see the sign that says, like the person or don't walk, but if you have low vision and you want to cross the street, you'll hit the button and it will say time to cross, walk sign on, so just make a noise depending on what city you're in. And it would also benefit you if you're on your phone and you weren't paying attention.

So fixing accessibility problems, making sure things are available on multiple formats, that's just gonna fix a lot of usability problems and fix things for everyone. So here's the main topic of the day. 

The web was not built for everyone, but we can do something about it. So I want to talk about why it's not built for everyone, what are the challenges we're facing with it and then what also we can do about it.

So whose job is accessibility? Thinking emoji. So we're gonna do a roll call. So raise your hand if you are a designer. Alright, so looks like maybe half of you. Raise your hand if you are a developer. It looks like about the other half, but I'm guessing there's a few of you that are not. Anyone here project or product manager? Nobody. QA? Anything else today, I'm not sure and I want to be inclusive. Nope?

Where you going out your self, that's fine, cool, not all of you are, but guess what ... accessibility is everybody's job and responsibility. So, did anyone have anything else to say to that? Oh yeah, so we're just here to talk about how we can build accessibility into every step of the process, to improve the web for everyone.

So first we can't do that without talking about what are the types of disabilities. So I have emojis next to them. I like emojis. So sorry. There's gonna be a lot of them, if you don't like them. [Indecipherable] accessibility according to people with disabilities. 

There's a Twitter thread, someone said, if you have a disability, what is the most frustrating thing about the web to you and why? So that's just a really interesting thread and someone wrote something up about it. Click that on your own time.

So the other thing I have to mention, sorry, I want to mention all of these things up front, so I don't accidentally forget to define them later. Assistive technology, this is technology that is physical, or is software that helps you just accomplish your task. So users with disabilities are often going to use assistive technologies to access content on the web and we have to think about that when we're designing and developing your content. 

And then ... accessing physical situations, you might use a wheelchair or a hearing aid or two, accessing the web or devices you might use a screen reader or an alternative input method, the mouse or even a keyboard. But a screen reader is a piece of software that's gonna convey what's on the screen to a user, usually in the form of reading it out.

So the first one is hearing disabilities and this is going to range from users who are completely deaf to users that are hard of hearing. And then the range of hearing within the hard-of-hearing is gonna go from pretty severe to just a little bit of hearing loss and this is going to include people that have been deaf since they were born to elderly folks who are losing their hearing with maybe your parents are already starting to lose their hearing.

It's affecting a lot of people, so we know that audio should not be the only form of information, ever. So we want to provide captions and transcripts, and then also, this is from two years ago or something, but 85% of Facebook videos are watched without sound and most of us are scrolling through Facebook on the train and don't have our headphones in, don't care what the sound is anyways. So a lot of them are without sound, so it's really important that it has captions, otherwise you're gonna lose everyone.

So next one is visual disabilities. And, this again is also a range of people who have completely lost their sight, they're legally blind, people with low vision and people who are color blind are also included in this. So some of them wear glasses or contacts, but some of them don't. Some of them can't correct their vision, and many of them use screen readers or magnification software. 

Here's a little chart about color blind people and it is why I hate pie charts. The the whole circle is gray and on the legend says because I'm color blind. And pie charts are just not great graphs to begin with, so and that if you're not going to use color contrast within that, then it's just going to look like that to some people. No data is conveyed. So colorblind users or people who have low vision, they're going to rely on other cues for information. So you don't ever want to use color alone to convey information. So more on that later.

So what are some other things we can do for users with visual disabilities. The content should be legible when zoom to 200%. Some users are going to be magnifying their screen. I know, even on my phone, I have my text a little bit magnified and I'm pretty young and don't have bad vision at all. But this has to do with responsive design.

Basically, if you zoom in, it's kind of the same as making your screen smaller. So the contents should all flow and stay ... to stay in the right place. And you shouldn't have to scroll horizontally in order to see the rest of the content. So responsive design we know that's good design. So if we make our designs responsive, then it should work for a user who is zooming in, even to the extreme of 400%.

So the next thing that I'm going to talk about, a couple of times within this presentation, is that, the page should be accessible using just the keyboard. This is because screen readers and using the keyboard without a mouse, you can't see the mouse pointer where it is. It's going to be using just the page, so it needs to be able to go through the page just using the keyboard. You'd be surprised how many pages you can't just use the keyboard for. And, of course, I'm going to talk about that later, that's something that bothers me.

The next thing, sufficient color contrast and this is for users with low vision and also color blind users. They need like contrasts like white text on a grey background, for example. Otherwise, they just won't be able to focus on that content, they won't be able to see what you're doing. So there's really easy ways to track your contrast, such as the aXe Chrome extension, a really great tool, or WebAIM has a contrast checker that I like to use.

Also another thing that I write about that made me kind of angry a few years ago was pop-ups and I was like, yeah, pop-ups are annoying but they're worse for the blind. Can you imagine, you can't see the screen and something pops up and there's no consistent way to close it. The X is on the left or right, maybe you can press escape to close it. You don't know, so they're inconsistent. So we want then to handle those correctly if we're going to use them, or not use them.

So the next disability we're going to talk about is physical disabilities. These are folks who have limited movement, muscle control, or fine motor skills. Using a mouse often requires a great deal of motor skills, so they're most likely not using a mouse. So this is where you want to make sure that your content is available to the keyboard or other alternative input methods. And what can we do for them, the keyboard thing, the web page should be accessible using the keyboard. We don't want to use complicated motions, such as clicking and dragging. We want to find alternatives to that or just provide alternatives, like for file dropping, normally you can use the actual file picker, but you can also click and drag, and I think that's probably a good alternative.

And then also we want to make navigation easier. Usually, web pages have a lot of content to go through, the navigations are complicated. But we have this thing called a skip to main content link, which will allow a user to skip over the navigation and get right to the content. I have an example here. This is Facebook, with all my personal stuff removed. So basically, when you tap into Facebook, the first thing on the page is going to be the top bar, and it says jump to, sections of this page, other pages on Facebook, Accessibility Help, and you can jump to a part of the page, and this is a very extreme, like well thought out example.

Most pages would probably just have like a skip to main content, just let you go to the main content. But this allows you to go to like anything. It's really cool. I recommend playing around with it. It's really hard not to click more than one... sorry for the previews of the next slide.

So the final disability we're going to talk about is cognitive disabilities. In my opinion, the hearing one was the easiest, because all we need to do is provide captions or transcripts, and this one is the hardest. This is the least visual. You don't know by looking at someone what their processing is like, or how they think at all. So these are users with difficulty with learning, memory, attention, problem solving, and comprehension. Could be Autism, or this could be like Dyslexia, this could be just a very wide variety of things. This could be you're getting old and you're very forgetful. So some of them really use screen readers and other assistive technologies, but it's probably gonna be just normal users trying to use your site.

I know they're gonna get frustrated a lot more easily. So they're gonna benefit from a simpler user experience, and then... also just less text and avoiding timed elements, like this is gonna expire in five minutes. That's really scary. It might take me a really long time to fill out this form. And then, flashing elements. We don't want to do that. That's just scary. We don't ... I think we're done with text flying across the screen. I think we're just done with that.

And then also forms. We want to make sure we have really descriptive instructions and good form errors, that tell you what you need to fix, so you're not just trying to review your form for ten minutes, trying to figure out the website.

So great, we talked about disabilities.

So the next section, the next thing we're going to talk about is how do we know if something is compliant, and there's got to be something I can do, some boxes I can check off, so what I know if I'm compliant. So let's try and talk about that a little bit. So this is the Web Content Accessibility Guidelines. This is the standard for measuring ... like what is accessible, is your content accessible?

We're measuring it against these four categories that all have like kind of guidelines within them, They have a lot of information about how something is accessible, what fails this. I recommend looking at it, but also not, because it's a lot to look at, especially for a beginner. It's just a huge wall of text with a ton of stuff, very comprehensive.

So the four categories that we had in there are Perceivable, Operable, Understandable and Robust. And they're going to deal with the different ways that we use technology.

So Perceivable ... can it be perceived? And notice it doesn't say, can it be seen. Because perceived is not necessarily seen and it's not necessarily heard. It could even be felt. So, can it be perceived.

Operable. Can it be used? Can it be comfortably, like, not just something that someone could use if they figured it out, over a couple hours, could they use it comfortably?

Understandable. Could it be understood? Like, is it intuitive? Do you know what to do when you look at it? Or is it just a huge wall of text that doesn't tell you anything.

And then Robust is the last one and that is, does it support assistive technology, if at all? A strong arm next to it. It should be strong and be able to handle whatever assistive technology someone is using.

So Perceivable is the first category. Put eyes, ears, and a little pointer for touch. So users can perceive the content and the information is available multiple formats. So there are multiple formats is the key here. People learn in different ways, people prefer their content in different ways. So that doesn't just apply to people with disabilities, sometimes they don't want to listen to a full podcast, they just want to scan the transcript.

There's just many times when you, when one format isn't working for you and you're like happy that there is another format. So this has to do with text alternatives for images. This is about captions, too. Colors isn't the only thing being used to convey information, and that the color contrast is enough for low-sighted users. So literally, it is, can it be seen? And the contrast that is recommended is the four point five to one.

So you just want to keep playing with your colors, or use a tool that will tell you if your colors are the right contrast, or might even recommend a color to use that is the right contrast. I've seen a tool like that. So, I have a slide here about text alternatives and this is as easy as an image tag, this is HTML.

If people don't know HTML, I'll try to talk about it as much as I can, explain what I'm talking about. But basically, it just requires a source for the image, the SRC, and the alt tag. And the alt tag should just be a description of the image. This is not supposed to be the image, next to it. It is supposed to be cat, sticking out its tongue image, show you can picture that. So basically, non-decorative images should have text alternatives and you want to use the empty value for the alt tag to let the screenreader to skip over an image if it is not, or if it is decorative. If the image is important, you need a description. If it's not important, tell the screen reader don't try to read it. 

So, I have a caption on the right that I'm sure you guys have read by now, if you can see. It's two guys and four cats in the picture and one of the guys seems to be doing something to the cats, like putting something on them. So the first guy says "Oh, Hi; I'm here from the internet" and the second guy says, "What are you doing?" And the first guy says, "Gluing captions to your cats."

So this is probably like what a few of us want to do. Like we see images without alt text and we're like, "can't we just glue captions onto here?" Which it would not be that hard. So this is from xkcd. Funny comics.

So the next one we have, Operable. And this is where we want to be able to navigate and use the page with the mouse, but also the keyboard. So it should be available using the keyboard only, but this also is about just usability in general, We want to not trap our users anywhere; if they get into a menu or something, they should be able to get out pretty easily. Imagine you go into a menu expecting just to see what's there and you just can never get out of there. And then we want our logical focus order, so that it's usable, we know where we are at all times, and we can navigate our pages correctly.

So our next one, the third category, we're going to talk about understandable. This is that users should be able to understand the interface and its information. So our interfaces should be predictable and the navigation should also be consistent on every page. 

And then more about forms. Forms should have labels, instructions and errors. So you should be able to see a form, know exactly what to do, it should be labeled, have instructions, and then if you mess up, it should tell you what to fix and how to fix it.

And then Robust. This means that it supports user agents. So actually not just assistive technology, we want to make sure it supports the browser as well. So this just means writing good code. So the half of you that are developers in here, this is really not that hard. So we'll talk a little bit about that.

There's this thing called semantic HTML, So we have HTML, the code that builds the websites, and renders things to the page. But we have semantic HTML, which means that we're using elements that have meaning, and we know what those are going to do. Like we can trust that when we want to put a button on the page and we say, like, when we write button, so that's going to be a button. And that's going to be handled correctly.

So a little more on that. Lately I think I can talk about semantic HTML for a while. Definitely going to cover that in the class. And then, I know I just told you all the stuff about compliance, but compliance doesn't mean your product is usable. Just because you've checked off a bunch of boxes, you still need to test it out. Just because I write all the code perfectly, which I wouldn't, I'm human, doesn't mean it's actually usable.

Unless we do research, at my company with users who have disabilities, and prove that it actually works and that it's useful. So you need to listen to your users, no matter what, that's definitely the goal. Also, with the guidelines, they're not fixed or comprehensive. We've been talking mostly about WCAG, the Web Content Accessibility Guidelines 2.0, but 2.1 just came out, and you just know they're going to keep putting the guidelines out. So if you think about actual user needs and usability, then you're much more likely to set your up set yourself up for success in the future, because you're thinking ahead, and the usability problem ... they're going to become the usability standards later.

So, here's an example of ... I provided a ramp for a staircase, but it doesn't look very usable. It is stairs, there's like three sets of stairs going up and then there's a ramp going alongside it on the side. But it kind of looks like an amusement ride and not a ramp that I don't think anyone would want to use. Like anyone with the baby or just how funny is that. So definitely it looks terrifying, is what I wrote. But they put a ramp there, right? So yeah.

So what can we do? Good question. So a few tips for designing more accessible products. So I've mentioned a few of these, but here it is, in a slide.

We want to use colors that have sufficient color contrast.
You don't want to use color alone to convey meaning, and this means that you should ... you can use color to convey the meaning. but also put some text in there. Say a username is required, or username has to have this character in it. Not just a red box around it. And then you also want ... you can use an icon, maybe, like you just want to give other visual clues, even if you're explaining it to the screenreader, explain it to visual users, too.

So designing better forms ... just ... can't state that enough. The error states should be good. Don't use placeholders as the label ... you start to type and then you forget, what does this want, anyways. Just not a good label ... you can use placeholders, but just don't use them as the only labels in there. 

So a couple more tips for designing more accessible products, because they fit on the other slide. So you want to write clear and concise copy. This means descriptive links and call-to-action buttons. We all like to see stuff like, read more, click here, those are not very useful. Like where this is taking me, learn more about what? So if you're only looking at the links through the buttons, they should make sense so it should say, sign up for a free trial, learn more about the iPhone 10. Those are way more useful for everyone.

So you want to write copy for text alternatives. If you're a designer, like you should say, here's the image I designed for you or the image that I want with it. But you should also say, this is not an important image, or just the description of this image is, three friends holding hands. 

That's useful, and then also, I think it'd be awesome as my designer put expected keyboard navigation in the design. Told me ... it should not only told me how it works when you click it, but also what the keyboard should do with it. So I guess that the image here is a click here and with no context.

So a few tips for developing more accessible products. So the entire page should be useful with the keyboard and semantic HTML is actually going to help with that. I know we should give images text alternatives. So some more semantic HTML here. Well first of all, a quick HTML lesson for anyone who doesn't know HTML the room, We use div elements, it's just d-i-v, to mean a division or a section. We use them as containers and we could use some [indecipherable] to apply some styles on top of it. But we shouldn't.

They are often used improperly they should be used for containers or moving things around or ... layouts, but they should not be used for actual elements, especially buttons. So this is definitely something I see a lot. I'm going to show you some examples in a minute, too. So yes, we want to use HTML elements that have meaning ... so that the browser knows what it is and so that assistive technologies can announce them properly. So it's going to be more accessible just to every device. And so, we have button tags, so we should use them.

Screen readers can announce all the elements like I said, and you can also list things by headings, by links, you can navigate between sections more easily. And if we, as developers, label the elements, and use the right elements, then it'll be a lot easier for everyone to navigate the website.

So I have a demo ... We shouldn't do live demos. Live demos are bad I'm gonna do one. Not to live, I've coded most of it. But this demo is going to show some bad semantic HTML and how we can make it better. And for examples and they're all examples of code that I've seen, either in the wild on random websites or in my code base at work. And so we're gonna look at them. Did this in Codepen. So hopefully you all can see ... what is going on. I'm not sure if the live stream will be able to see this, I'll just talk about as best I can what is going on.

The theme is for the code we're not very high contrast, but basically we have four buttons here And they all look the same, right? Or at least pretend they do. Messes with the padding and stuff too much but we have four buttons here, and I'm just gonna go through them and test this website, test my buttons, as if we were looking for like accessibility here, or just what is going on with these buttons. So, I'm going to click on each button and all I have it doing is saying which button was clicked. It's just reading the text of the button and displaying it and saying it was clicked on the right.

Really fun demo. So button 1, I clicked it. Button 2, I clicked it. This is the boring part. Button 3, clicked,  button 4, clicked. So it work with the keyboard, that's great. Most of us in here would be fine with that, great, ship it, put it in the code base, put it in production, this is fun.

But what about the keyboard? So I wrote a reset button, that you probably can't see my reset button, but don't worry about it I just want to, you know, the reset it sometimes, just to restart my demo. So we're gonna try ... just gonna click up here move the tabbing focus up there, and then I'm going to tab and hopefully be able to click on all these buttons with the keyboard. So I'm going to try to tab to the first one and let's see, what is the first one. I hit enter to activate it and it says button one was clicked.

So let's see what is under the hood. So I have button one here and ... I was expecting a button, because it's coded like a button, it doesn't take me anywhere, but actually it's a link. So we have an anchor tag here, which is an a with the href attribute and the href attribute is javascript:void 0, which is basically, cancel out any navigation that this would have done, and then there's an onclick on this.

That says that will actually do the clicking. I wrote a function over here that just sets button to say button is clicked. But, this is the link under the hood and it's just a cancelled out link. So this is one of the red flags that this should have been a button. Because you have to cancel out the href, the navigation.

I actually see this all the time, mostly when you think you want a link, but it's actually going to do something like bring something up, or like just do something on the page, and your designer gave you a link, so you're like great, I'll make it a link. But really, even so you should make it a button and not worry about what it looks like. In the first pass and then in the second pass, remove all the styling and make it look like whatever links look like in your application.

So let's try the second one. We'll reset. So I'm going to try and tab to my second button,  button one ... where's my button two? I wonder why I can't focus on it. Let's see what it is under the hood. So it was clickable, right? So it was a button. Most people would say, yeah. It's not. It's a div.

So remember I mentioned the div? You can use this pretty much for anything, But should we have used it here? Not really. I will explain like how you could have used it here, but we'll get to that in a moment. But basically, I gave it a role of button, so that's a button, right? Ah, no. So the role button, that's ARIA, which we'll talk about also in a couple minutes. What that is, why that's there ... but basically that's saying like, I now exist as a button. But it's not saying, do anything to make it work like a button. It's just saying, announce it like the screen reader will hit it and say button.

Button two,  or button two, button, however it's going to announce it. But, so it has an onclick but it doesn't handle the keypress and it also doesn't handle tabbing, right? I couldn't even get over to it, even if it could handle a keypress, I couldn't even get to it with my keyboard. So I'm guilty of this, everyone's guilty of this.

We all are like, well, I don't want it to look like an actual button, I just want something that's clickable. I found a great example that I did 10 months ago and I was like, wow this was me, and I didn't even handle, you can't talk to it, you can't click on it, you can't like tab to it and you can't press a button to click on it, but you can click on it just fine and it works all just fine. So it passed everything. Like, Wow, [indecipherable].

So, let's look at the next button. So I see we were able to tab to it. And let's try hitting Enter. Just while we're here. So that wouldn't work. So let's see what happened there. Is this one button? And the answer is no, still not a button. But it did handle tabbing to it. So, this is the tabindex zero, puts it in the tabbing order. So, they stuffed it in the tabbing order already like buttons and links, but there's stuff that's not, like divs, or text. So this puts it in the tabbing order.

And then we handled that onclick and then we handled the onkeypress. So we can look at the onkeypress, which is the button press function, now we've moved to the right, and basically we're taking in that click event, the button click, we're checking to see what button was pressed. What key was pressed and I checked for the Space bar or the Enter key or Enter or Space bar 13 and 32 and then I basically just called my button click function with that. So a lot of extra code. Let's see if we can make this any simpler.

So, let's tab over to the fourth button. 1 ... 2 doesn't really exist according to the keyboard, 3 & 4 ... we'll try clicking on it, and that one worked. So let's see if we finally made a button. And this one required a little bit of extra styling and that's what I did is good for. And have a div around my button but the real thing is the button with just an onclick, add to class for some styling and it has button four. That didn't require an extra function, that didn't require tabindex, that didn't require handling the keypress, and it's just a lot easier. Like, all I type is button.

So, it's amazing like how many times they find stuff with all the other examples that I showed in the code base, and I'm really trying to just explain that there's ways that we could just write really simple code, write better code, that'll fix it and we won't up to handle additional things. So even if you have something really complicated, as long as it's clickable, most of the time, you can use a button and just take away the styling, worry about that later, handle anything else later, but it should just work a lot better.

So that was my demo. I think that went well. I hope you thought so. And good news, we still have more slides.

So now we're going to talk a little bit about ARIA, which means Accessible Rich Internet Application. And this defines how custom widgets should be handled, so anything that is not a button or a navigation, or just a simple things that we used to have the early days of the web, now we have complicated menus and menu buttons and just all sorts of widgets that are happening, because we want to do cooler things with the web.

But, how should the web handle that?  We're still try to figure that out. It's not exactly consistent and we're working on it, But ARIA is trying to solve that problem by saying, you can describe what your component does to the screen reader, to your users, by using these additional attributes like aria-label or role, and then you should use, you can use ARIA to supplement HTML.

So first you want to write great HTML, then you want to style it. Then, you want to make it all work, and then you want to describe it using ARIA. But no ARIA is better than bad ARIA. And this is directly out of the ARIA Authoring Practices, literally in the documentation. Like, don't use it if you don't understand it. And I've seen a lot of bad ARIA. So I can't stress this enough. That's why it's on its own slide.

Definitely look at trying to use it, but it is not something that you just play with, it's not something to just tack on to anything. Because, using it wrong is just worse than not using it at all. Because here you're telling your user what you can expect from something. So if you say this is a button, and it's not, then it's not a button. And that's just confusing, that would frustrate any of us.

So ... let that sink in. [Laugh] And, we've got some takeaways here. Hopefully a lot but just a couple on a summary slide.

We want to provide content in alternative formats. Text is good, because it can be converted to audio, it could be read, it can be made bigger, it's a good alternative.

We want to make sure that pages work with just the keyboard, and you should definitely go home and try this on some of the websites that you use frequently. Definitely try Facebook, that's a fun one, but try like some stores that you buy from or Amazon or just just anything. Just start tabbing around and see what they've handled, see what they haven't. Look at Apple, some places are doing it very well and some places are doing it very poorly. And we're working on it. Try it at your own company. Tell people about it.

So interfaces should be predictable and easy to use. Definitely frustrating when they are not. Even more frustrating to users with disabilities, and then we just know that designing for different abilities benefits everyone. It benefits ourselves. After you've gone through like a whole long workshop, you're probably going to find out that the design was just better after ... than when you started, because it's just gonna force you to think more simply, just break things down. Sometimes, it's just not about adding more code on, it's not about just tacking more accessibility features on, or aria-labels or just putting more JavaScript in there. 

Sometimes it's about just breaking it down and making it simpler. There's some pages in the application that I work on that are so complicated that I don't even know how we would fix them. So, I think we're just gonna probably try to redesign them and come back to it. So it's not about just fixing everything, 'cause that's way harder, but it's about trying to do it from the beginning. 

I have a resources slide, so this is assuming that you go to my slides and click on these. Just a couple of articles that I found interesting, couple of resources. Definitely follow @a11ychi on Twitter. Dennis queues up so much content and there's content several times a day sometimes. He's always talking about what else is going on, just really cool articles, great resource.

And then, that's my last slide. Thank you for coming. You can follow me on Twitter, find my slides, sorry, now you can clap.

**[Applause]**

**[Dennis]:** So I thank you for ... sure yeah, please ...

**[Arelia]:** Hi everyone, I'm Arelia, I'm a software engineer with Sprout Social. I am one of the Chapter Organizers of Girl Develop It, along with Brittany, over here. Who has not been to Girl Develop It before? Alright, would love to see you at our events.

So, Girl Develop It is a non-profit organization. We provide affordable and judgement-free opportunities for women who are interested in working in web and software development. And although our events and classes are geared towards women, we are open to everyone of all genders. One of the ways we provide affordable and judgement-free classes is by bringing in instructors who are working in the field. We also have ample teacher assistants at each class. We hope you will feel comfortable asking questions, answer all of your questions so you will feel well supported.

We also have a Code of Conduct that is listed on each event, and we encourage participants to come to the chapter or organizer onsite for any violations to the code of conduct. [Indecipherable]

**[Applause]**

**[Dennis]:** Thank you for coming. If you have any questions for Margie, please come on up. Thanks.

**[Applause]**

Thanks to our presenter, Margie Chubin. Follow her on Twitter at @MargarineMargie 
Also thanks to Girl Develop It Chicago. Join them at meetup.com/Girl-Develop-It-Chicago-IL
Thanks to our venue sponsor, Redshelf. Visit them online at redshelf.com.
Live captions provided by ACS, Alternative Communication Services. Visit them online at acscaptions.com
Live captions sponsored by McDonald's. We're lovin' it!
This has been a production of the Chicago Digital Accessibility & Inclusive Design Meetup. 
Visit us online at meetup.com/a11ychi
Follow us on Twitter at twitter.com/a11ychi
Follow us on Facebook at facebook.com/a11ychi
Watch recordings of past meetups on YouTube, on our YouTube channel youtube.com/c/ChicagoDigitalAccessibilityInclusiveDesign
Make sure you subscribe today!

Copyright 2018 Chicago Digital Accessibility & Inclusive Design Meetup. All rights reserved.

