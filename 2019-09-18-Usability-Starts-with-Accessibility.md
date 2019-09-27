ROUGH EDITED COPY

CDA
USABILITY STARTS WITH ACCESSIBILITY
SEPTEMBER 18, 2019
7:30 P.M. ET

REMOTE CART CAPTIONING PROVIDED BY:
ALTERNATIVE COMMUNICATION SERVICES, LLC
www.CaptionFamily.com

This is being provided in a rough-draft format. Communication Access Realtime Translation (CART) is provided in order to facilitate communication accessibility and may not be a totally verbatim record of the proceedings. 

 — —-

**PATRICK McSWEENY:** — sometimes the contrast is light this says light contrast and it's in gray instead of black. Sometimes fonts are not designed for readability the font I'm using here is Arial it was originally designed to save space on the screen rather than actually be readable yet still in 2019 people are using Arial or it's sibling Helvetica in their Websites for some weird reason. 

And I think the reason that me as someone with goods eyesight has trouble reading Websites sometimes is frankly accessibility is not a priority for a lot of web developers and designers. Some people don't know they should be making their Websites accessible. You know, for some people it's just honestly it's just something they are unaware of. Some people just don't care. You know they know it exists. But for whatever reason it's just not something that concerns them.

And then some people think, well, I would like to make my Website accessible but I just don't have the time or budget to do it and that's really unfortunate because it's not that hard if you know what you're doing. 

So real quickly just to go over the basics of human-computer interaction most of us interact with computers with input devices and output devices. So the input devices that most people are familiar with would be keyboard and then either a mouse or a trackpad or touchscreen or some combination of those. And then most of us use the output devices being a screen and speakers. 
So for able-bodied people this is all we know about how to use a computer. Like it doesn't occur to a lot of people that there might be other ways of interacting with a computer. 

And — but there are different disabilities that can affect someone's ability to interact with a computer. Some people have visual impairments. And this can run the gamut from just having poor eyesight to being completely blind. Some people have physical impairments for whatever reason they are not able to use a keyboard or mouse so they might need to rely on voice commands, for instance.

Cognitive impairments can be a challenge for some people. And then also auditory impairments so for people who have these disabilities using a screen and a keyboard might be — might not be an option for them. But this is not a possibility that a lot of developers and designers really consider. I think this leads to a vicious cycle so people who don't have disabilities tend — developers who don't have disabilities tend to develop for users who don't have disabilities.

And we — a lot of us take the typical workflow for interacting with computers for granted and this could lead to people with disabilities, they might get frustrated and give up. And then they might not use computers as much. And they would be less likely to become developers themselves. And then the cycle feeds into itself. Unfortunately. 

However, the good news is if you want to make your Websites accessible to people with disabilities you don't necessarily need to know the details of how screen readers work or how a voice command system would work. Because the browser on your user's computer already has an accessibility API built in. I'm going to build up the suspense for a second because what the accessibility API is might not be quite what you were expecting because it is HTML and CSS. So I think there's a common attitude among some developers that HTML and CSS is not real programming and I can get where they are coming from but I think developer HTML and CSS a lot of people take for granted all of the and useful for technologies and a lot of people never take the time to learn all of the different things you can do with them. Some people tend to look down upon it. There's a popular belief among developers that HTML was originally invented for displaying documents. technically that's not incorrect but you can also say computers were invented for solving math problems and that also would technically not be correct I think it's more accurate to say that HTML and CSS are designed to give you — allow — it gives you the building blocks for creating the user interface. Rather than having to build everything from scratch yourself. 

So HTTP HyperText Transfer Protocol this is the — this is for every single web application and also plays a role in a lot of mobile applications but a lot of people don't realize that HTTP and HTML were designed to be used together from their very beginning.

So if you're creating an HTML form on your Website, when someone fills out that form and hits the submit button, that — based on your form, the browser is going to be sending a rather complex HTTP request to the server and then the server will return information based on that. And this is the way it was always intended to be. So a lot of the people who like to you know say that HTML isn't real programming are the same ones who nerd out and knowing all of the different parts of the HTTP spec. And HTML, though, was designed for dynamic content user interaction from the very beginning. 

And some different ways that it's designed for these things HTML forms and links these actually provide ways for the user to give input to the Website. And then semantic HTML allows the browser to actually understand the content that it's being fed. 
So sometimes when I'm bored I'll use the inspector in my browser to examine the code of the Websites that I'm browsing when I'm browsing the web. To me it's quite evident that a lot of developers are simply unaware of what semantic HTML is and if they are they just don't care. 

But HTML, its original purpose was to organize the content in with your webpage. The reason this is important for accessibility is the — if you're using semantic HTML this will actually allow the browser to describe the text that's in your webpage to a screen reader. 

So just real basic example list elements like ul or ol, these — this can be a way of organizing the content. So if you have a list of items and you're using the ol or ul elements the screen reader will be able to understand that this is a list whereas if you wrap everything in divs the screen reader won't necessarily know there's a difference — they won't know these items are related or that they are the same thing. 

And then text elements, you know, we're all familiar with elements like the paragraph tag or the header tags the H1 H2 and so on. And these are some basic examples of how you can use HTML tags to describe the content in your page. And this is all stuff that's been around since the '90 so this is definitely not new. 

But HTML5 has opened up a lot of new ways to use semantic HTML to describe the content. So for instance, there's like the header tags and footer tags and then tags like article or aside and so on. 

So HTML5 has made HTML even more powerful in allowing you to describe the information that's contained within your web pages. 
But there's also a benefit to you as a developer to using semantic HTML. 

And it actually forces you to organize your content. So if you're just using divs and spans for everything in your webpage, this makes it a little too easy to just throw your content on the screen and not give it any thought as to how things should be organized or what the roles — different pieces of content are playing in your page. 

Whereas if you use semantic HTML, you actually have to think about, okay, is this a header or is it a paragraph? Is this a list or is it a — something else? 

So using semantic HTML gives you the power to better organize your content than you would be otherwise. 

So moving on to HTML forms. 

These are one of the most important ways that you can incorporate accessibility into your web pages. So input types, there's a lot of different input types in HTML forms. We're all text with like text and select tags and then — but the reason that it's important to use the different types is it allows different ways of — it gives the users different ways to interact with the computer if you're using your own custom tags, if you're trying to reinvent the wheel and come up with your own version of a select tag or your own version of a checkbox, the browser might not necessarily know what's going on there so they — the browser would not be able to describe that to a screen reader. 

And HTML5 has also introduced a lot of different types of form inputs. So for instance, you can have a date input which allows the browser to implement its own user interface for selecting a date. Or there's — if you use the color input type, it can actually allow the browser to bring up a color picker when you're using that. 

So once again, HTML5 has made forms even more powerful than they already were. 

Also, label tags, if — when you're putting out labels for all of your inputs, you need to make sure that you're using them properly in order for the browser to be able to understand which labels go to which inputs and then be able to convey that to someone who is using a screen reader or a different way of interacting with it. 

So label tags is something that a lot of us take for granted or might not give much thought to. But it's a really powerful way of adding accessibility to your forms while you're making them interactive. 

And fieldset and legend tags are some of the lesser known elements that get used in forms but this can make it easier to organize your forms and break them into different sections and let users know which inputs in your form are grouped together and also give you — give the users instructions. 

So the bottom line when it comes to HTML is, when used properly, it lays the foundation for accessibility. So CSS or Cascading Style Sheets. 

Probably one of the most important ways that you can use CSS to add accessibility is to use relative units when you're defining the font sizes. And I have a quick demo that I would like to show for this. 

So I coded a really simple HTML page and as you can see the fixed class is defined font size as 16 pixels and the relative class is defining font size as 1 m unit and m unit is the — in CSS is the approximate width of a character that's being displayed on the screen and over here you can see the fixed font size is a little bit smaller than the relative font size and the reason for that is that I set the font size for the browser at 18 pixels but you can take it even higher if you want so if you really wanted to you can set it to 32 pixels and as you can see the relative font size text has whereas the font size set using pixels remained the same. So if you are using pixels or other absolute units to set font sizes you're taking control out of the hands of the users and that's not something you want to do some people might need to increase the font sizes because they are not able to see well or in my case you're just lazy and you don't want to have to work more than you need to. 

Sorry. 

Okay. So yeah, as I was saying, if you use the m or rim is relative to the base font size that the browser is set to. If you're using these to set your font sizes, then users will be able to adjust the size — the text on your screen. And I mean, when you think about that, that's really pretty amazing. You know if you're printing words on a page, you're never going to be able to change the size of those words once they have been printed. But you can actually set up your webpage to make it so that everyone who uses it could be able to set the font size to whatever they want it to be. And it can be a challenge to get used to. But I think it's definitely worth it. 

And the benefit to you as a developer to using relative font sizes is that your code is cleaner. 

So just a real simple example, on the left, you can see — this is how you might use pixels to set font sizes for some of the different text elements. And then on the right this is how you might use m units. So on the left you can see all of the — you actually have to calculate the ratio yourself whereas on the right you can see very clearly H1 is going to be twice the size of a paragraph tag. And H2 is going to be 1.5 times the size so I think the code on the right is a lot easier to understand. And it would also be a lot easier to make adjustments to. So you don't have to every time you're changing a font size, you don't have to calculate how many pixels it should be and so on. 

And also if you're trying to make your Websites responsive, I think using relative font sizes makes it easier in that way so you're not constantly defining ten different font sizes for every type of element in your code. 

So some other CSS things you can do in order to enhance accessibility, as I alluded to earlier, don't give your text — don't make your text too small. And don't give it like contrast and I think some designers who do this are designing more for looking nice rather than actually trying to make it easy to read. 

So try to — you should always try to be prioritized readability for the text on your Website. 

And I think it's important to minimize the use of decorative fonts. So there's certain fonts that are made to look pretty but aren't really made to be readable. And I mean it's fine to use those once in a while. But it's not something you should be doing all the time. 

And also character spacing and character size are important. 

So — and the Arial text that I showed earlier, the characters are jammed together, which makes it hard to read. And you can do an entire presentation just about how to make text — how to choose fonts that are readable so if that's not a topic you're familiar with, I definitely suggest learning more about that. 

The reason that CSS was originally invented was to allow developers to extract the presentation logic from their HTML and then separate it out entirely into their style sheets. 

But when I'm looking at the underlying code of Websites, it's clear to me that a lot of developers still haven't gotten the memo, even though it's been about 20 something years since CSS came on the scene. 

So one thing that I see way too often is developers using VR tags in order to create spacing on the screen. VR tags were invented solely for putting line breaks in the text. Not for actually separating things apart. And this has been bad practice for a really long time yet people are still doing it. 

But in general, don't insert HTML into your — don't insert any HTML elements that don't actually serve a purpose of adding content. Don't insert elements purely for visual purposes. 

So if you're — for a person who is reading a webpage on a screen, if they don't really know the difference between how good the underlying HTML is or not, however, if there's a bunch of extra — did you have a question? Never mind. 

If there's a bunch of extra crud inside of your HTML, then that can definitely make it more strenuous on someone who is using a screen reader because then the screen reader would actually have to go through all of the extra elements that aren't actually there to add content. 

So if you want to learn more, a good place — probably the most authoritative source you can get would be from the World Wide Web Consortium. This is the standard study that will be official what's for HTML and CSS and all of that and they have an entire initiative dedicated to accessibility which you can find on their Website. 

And their documentation is very thorough and very exhaustive. However, it can be a little technical and dry. 

So another good resource would be the Mozilla Docs. The Mozilla foundation provides really excellent documentation for lots of different things for web development like HTML, CSS and JavaScript so it's definitely a good resource to use in general but they also have a lot of documentation about accessibility specifically. 

Typographic Web Design was a book written by Laura Fanz she gets into how to pick fonts that are readable and arrange text on the screen so it's readable it was definitely a big help to me when I read it so that would be another good resource. 

And you know just finally learn the fundamentals of HTML and CSS. As I've been saying, a lot of developers don't really give it the respect it deserves. And a lot of people just think, oh, I'll just, you know, learn it as I need to. Learn it as I go. You know, pick it up as I need to. And as a result a lot of people don't necessarily understand — they don't know what they are missing by not learning about it. So if you learn CSS and HTML fundamentals and really take them to heart, that will make you better at making your Websites be accessible. Even if that's not necessarily what you're focusing on itself. 

So that wraps up the presentation. 

Questions? Yeah. 

Oh, no.

**PATRICK McSWEENY:** Well, it's for the livestream. 

**Attendee:** Can you give some examples of the extra visual in HTML? 

**PATRICK McSWEENY:** Well like using break tags. Like I've seen a lot of web pages where someone will insert like a tag just to provide a line on the page or providing borders or providing spaces. Unless your HTML is wrapping a text or something or an image it doesn't need to be there you should be focusing on the HTML purely for content itself and you're not putting any presentation into it. No, not classes. But when you're inserting a tag into the HTML itself if the tag serves no purpose other than to add presentation, like you can put classes on your tags that's fine that's the way you're supposed to do it but put classes on the tags that are already there to just put tags in there for presentation purposes, if that makes sense. 

_(Off microphone)._

**PATRICK McSWEENY:** That's a good question. I don't know, to be honest. Is there anyone here who could speak on that? 
Okay. Sorry.
I would count on them not handling them. But in general screen readers will ignore stuff that's wrapped up in CSS and stuff like that. So just assume it's not going to be visible to a screen reader. Test it. You know, it's possible.

**PATRICK McSWEENY:** But I think that's the way it should be. Because like you should be using pseudo classes for stuff that's purely presentation like using pseudo classes can be a good way to take out content that's only there to be displayed that's not actually — would never actually be read outloud. 
Next question? 

>> Can you repeat the questions.

**PATRICK McSWEENY:** Sorry; I thought you were able to hear it through the microphone.

>> So when you're creating CSS, would it be better to create CSS externally for screen readers? Or would it be also a bad idea when you're creating CSS to do inline CSS? Because screen readers aren't able to read all of the CSS that's inline between an element? Or which method would be better for screen readers really in reading CSS? 

**PATRICK McSWEENY:** I mean, again I'm not an expert on how screen readers work — sorry to repeat the question the question is asking if it's better to use inline styles or to have your CSS in an external style sheet for screen readers. 
But I mean, I would think that screen readers would just ignore any inline CSS, or CSS that's in an external sheet. 
But I just think in terms of good web development practices it's always good to have it in an external style sheet whenever you can. 

>> I was just wondering if you could throw out like a couple of quick examples of (inaudible). 

**PATRICK McSWEENY:** Sure. Yeah, so the question is readable fonts that are built in. Verdana — so the fonts that you could — the web-safe fonts for — before the days of font face, probably the two best for that would be verdana and Georgia because those were two of the first fonts to be designed for computers where the No. 1 goal was readability. 
And then like some other common ones that you can get for free, like Droid sans and Droid serif is a good one. I'm kind of blanking on other examples. But in general for ones with better spacing that have well-defined goals, ascenders and descenders are very visible. But yeah, verdana and Georgia, those would be good ones to reference. 

>> Thank you. 

(Applause)

>> Feel free to indulge and eat more. 

* * * * *
Communication Access Realtime Translation (CART) is provided in order to facilitate communication accessibility. CART captioning and this realtime file may not be a totally verbatim record of the proceedings.
* * * *

