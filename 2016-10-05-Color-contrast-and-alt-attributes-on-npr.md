# Color contrast and alt attributes on npr.org (Lightning Talk)
## Todd Welstein - Wednesday, October 5, 2016
[Source recording](https://www.youtube.com/watch?v=s98z_ThsNC0)

**[Todd]:** Hi, I’m Todd Welstein. I work as a UI developer at NPR. The department that I’m in is called Digital Media, and it is responsible for NPR’s digital presence. It includes developers, QA people, dev ops, product owners, UX designers, product designers. We’re responsible for the website, npr.org, apps like NPR One, APIs that power website and the apps, and the internal content management system. And it’s a high traffic site. So for example, in September, there were 86 million page views and 40 million unique users. And my job as UI developer focuses on writing HTML, CSS and JavaScript.

This particular talk is going to be divided into two parts. The first part is color contrast. And it covers the basics of making adjustments for that. The second part of this related to alt text, specifically the null alt attribute value, and how that helps to reduce redundancy for screen reader users.

So contrast ratio refers to the relationship between foreground and background color. The Web Content Accessibility Guidelines for double A specifies a minimum ratio of four and a half for text and images of text. For large text, if text is over 18 points or 14 point bold, then the requirement gets lowered to 3.0. But this talk is going to focus on 4.5.

There are some other exceptions to this rule as well. For example, text that is part of a logo or a brand name also as no requirements. The ratios themselves range from 1 to 21, 1 being completely invisible, 21 being very visible. And in this particular example, I increased the font size so you can see it, but the first item that meets the 4.5 requirement is the third from the top.

So you might be wondering why did they choose 4.5 as the ratio? Well, according to the W3C, it is to account for the loss in contrast that results from moderately low visual acuity, congenital or acquired color deficiencies, or the loss of contrast sensitivity that typically accompanies aging. It goes on to say that this basically means someone with 20/40 vision. Someone with 20/40 vision is commonly thought of as having the acuity of someone who is about 80 years old.

However, in addition to helping users with permanent disabilities, permanent visual difficulties, the guidelines also help people with transient issues. So what’s a transient issue? Well, if you’re outside and you’re using your phone on a sunny day, there might be glare on the screen. Or if you’re viewing a presentation on a bad overhead projector, there also might be issues. So, this can help everybody.

There are many tools out there that can check color contrast. A few are listed here, but this talk is going to focus the last one, which is Google Accessibility Developer Tools, which is a Chrome extension you can get at the Chrome Web Store. So here is a typical story on npr.org. There is a large photo, a caption underneath and a photo credit. I took the photo and changed the caption color so that it no longer meets requirements. The ratio for the Chicago skyline is right now 2.32. And so now we can pretend that we’re going to use the Google Accessibility Developer tools to fix this. So once the extension is installed, you can open dev tools and go to the Audits pane where there will be a new option for Accessibility. And you run an audit and your presented with a list of findings.

So one list includes color contrast, which we’re looking at right now. And the photo caption is highlighted in red, so it’s a paragraph tag. If you right click that paragraph tag, you’re taken to the elements panel and, there’s also a new pane here too called Accessibility Properties, all the way on the right side. And you can see that the contrast is indeed 2.32.

And there’s other options there. So you can test out what double A or triple A will look like. If you click the icons directly next to those hex codes, you’ll see immediately in the browser what the new color looks like. And if you like it, you can copy the hex code and paste it into your CSS.

So, we pretend that we click on the double A icon, we get this. So the before version is on the left, the after version is on the right.
It’s a little difficult to see on the projector, but there’s a difference. And this is the process that we went through for the entire site. But it was a very manual process and there are many different templates for npr.org. There’s story pages, music homepage, music pages, podcast directory, and all of these templates have different permutations, because the content management system is very flexible. You can put different assets in different categories, different locations and configure them differently. So, we covered a big chunk of the site, but it’s still an ongoing process.

When you’re doing this, there’s going to be issues outside of your control, and also false-positives, depending on the tool that you use. Items outside of your control include ads from a third party server or embeds like video or any type of third party embed that has content that’s text. The Google Accessibility Developer Tools looks at those too and will give you warnings, it will flag them if they don’t meet contrast requirements. There’s not much you can do about that except for notify the originators of those ads or embeds about the problem.

False positives include … so there’s certain ways to hide text from sighted users while keeping it readable by screen readers. And depending on the CSS technique you use, if you deliberately want to hide text from sighted users, the Accessibility Developer Tools may still flag those items as being a problem. So for us, we’re seeing that a lot. And so you can either ignore them or try to figure out a different technique that the Developer Tools would ignore.

Also, as I mentioned, logos and branding-related text, they are exempt from contrast requirements, but they’ll still get flagged if you're using web fonts or just plain text.

That said, here are a few examples of before and after, from the site. Again, it may be a little bit difficult to see the difference on the projector, but on top is before, and on the bottom is after.

This is the homepage. We adjusted the blue color for the navigation links. This is the small breakpoints navigation and again the blue color has been altered. This is a larger breakpoint, top is before, bottom is after, it’s a little hard to see. This type of digital pattern is pretty common on the site. In this case, the tagline “Stories of Life in a Changing World” was … the difference is pretty obvious here.

Here is a music story page for small screen. Pretty much every element was adjusted. This is commonly on a story page, it’s a topic related to the topic of the story. And before is on the left and after is on the right. 

Here’s the audio player, when it’s not playing. The text for zoom listening now meets the requirements. This is from the podcast directory. The topic “business” was changed. And then lastly here’s the player, and this is again pretty hard to see, but the light blue background beneath the bottom portion of the player was made darker so that the timing information and the text in the center meet contrast requirements. Keep in mind if you are doing this, there may be other assets on the page that you need to change. Those icons above, the play icon, the rewind icon, the skip icon, are all SVGs, and so when we changed the blue of the player, we also had to change the SVG blue color to match the new shade of blue that we were using.

So those are a few examples, but after doing this, you may find that the color palette you are using in your CSS may grow. We already had a problem on the site where there were many several shades of colors, and it was hard to tell what was intentional and what was caused from using the eyedropper tool on the wrong part of a compressed palette. So after doing this, we ended up with 198 colors. Which is a lot, and some of them are very similar.

So very briefly, there are ways you can slim this down. There’s a tool called Parker, that will generate a list of all the different colors in your codebase. You can take that list and run it through a tool called CSS Colorguard, that will run that list through an algorithm to show you pairs of visually, semi-indistinguishable colors. But when you’re doing that, you have to be mindful that you’re not going to re-introduce color contrast issues. So we manually went and … trying to combine colors while making sure that there color contrast was above 4.5. Once we finished that, we ended up with 78 distinct colors, which still may seem like a lot, but the site is big and this takes into account everything.

The nice side effect of simplifying colors and organizing them is that you can programmatically create a color swatch guide for other developers and designers. This will hopefully allow people to choose combinations that have already been vetted and less likely to introduce contrast problems.

So that’s Part 1.

Part 2 is about the null alt attribute value.

So what is the null alt attribute value? So it looks like this. This is a very simplified img tag. The alt attribute value is equal to an empty string here. This is not the same thing as having no alt attribute value. So why would you want to do this? Well, alt text should typically not be redundant or provide the same information that is already on the page.

So going back to our example story here. There’s an image with a caption that says Chicago skyline. In the past, before we made any changes, the img tag was basically like this. It was the same text in the alt attribute as was already on the page as a caption. And screen readers will then just read the alt attribute, and directly after that, read the caption. So its a redundancy. I’ll play a screen recording of it, I’m not sure you’ll be able to hear it, but let’s see.

**[Screen reader]:** link Adam Frank Chicago Skyline image Chicago Skyline istockphoto

**[Todd]:** So if you could hear that, it read chicago skyline, and then again chicago skyline. As it read the alt text and then the caption. So we would use the null alt attribute value here, and then this is how VoiceOver will read the page.

**[Screen reader]:** link Adam Frank Chicago Skyline image credit istockphoto

**[Todd]**: So if you could hear that, it skipped over the image and just read the caption. You may have also heard these helper words. So we also added ARIA labels to the image credit and caption. The screen reader will read out image caption before it reads caption, and it’ll read out image credit before it read the credit. Also, we did that for the byline. I’ll play it one more time. Hopefully you can hear.

**[Screen reader]:** byline group link Adam Frank image caption  Chicago Skyline credit istockphoto

**[Todd]:** So those are from the ARIA labels. Now, editors can choose to inhibit the captions from showing on any image via a checkbox in the CMS. If they do that, then having the null alt attribute is not a good idea. So in that case, what was formerly the caption will then become the alt text again. And that sounds like this.

**[Screen reader]:** byline link Adam Frank Chicago Skyline image image credit istockphoto

**[Todd]:** So VoiceOver there read the alt text, because there was nothing else, there was no image caption, so we used alt text. Keep in mind that an image that is the only thing inside of a link, must never have the null alt attribute value. The functionality of the link should be mentioned in the alt text in addition to the content of the image. If you use a null alt attribute value, and an image is the only thing in a link, in VoiceOver, it won’t read anything helpful. 

Also, users that navigate via the tab key are going to hear this out if context. So if they tab to an image that just talks about … that has alt text that’s just about the image and not the link, you’re not going to hear anything relevant to where that link actually goes. It helps sighted users too, because if the image doesn’t load for whatever reason, then the alt text will be there telling them about the link.

So just to reiterate, if this image was the only thing in the link, even if Chicago Skyline was directly underneath it, you still need alt text, you can’t use the null attribute value. Because the alt text for the image should discuss the link as well as the image. So, if you’re like me and you worry a little bit about getting this perfectly right, this quote is really helpful for me. It says like many things in web accessibility, determining appropriate, equivalent, alt text is often a matter of personal interpretation, and there’s often not one super right answer. So this is really helpful to keep this in mind when you are doing this.

Lastly, some additional resources. There’s a link to the developer tools, a couple articles that were really helpful, contrast testing, there’s the mathematic formula to calculate the ratio if you’re interested in that, an article on alt text and on the bottom, I wrote an article on our tech blog, basically about what I just spoke about.

Also if you’re interested in what other people from the tech team are doing, check out npr.codes.

Thanks for listening.

**[Applause]**

**[Dennis]:** Any questions for Todd?

**[Attendee]:** So, what was the advantage of having a null alt tag versus not having any alt tag?

**[Todd]:** If there’s no alt tag at all, then, the screen reader … the question was … what’s the advantage of using null as an alt attribute value versus nothing, not even having an alt tag. If there’s no alt tag at all, then, the screen reader will likely read the file name of the image, which is like super unhelpful.

**[Dennis]:** Especially on a content management system.

**[Todd]:** Yes, very long, very long filenames.

**[Attendee]:** Yeah, I know you are on the UI/UX department at NPR Todd. I’m just curious, were there other areas of accessibility that NPR undertook in addition to the contrast issue?

**[Todd]:** Yeah, so we recently worked with ARIA landmarks and ARIA labels. I briefly touched on the labels. We added landmarks also. We have a skip to main content. For the player, we just launched a consistent player, an audio player. We added keyboard shortcuts for that. And a link to can get to via the tab key for getting help on keyboard shortcuts themselves. Those are a few that comes to mind right now. There’s other things too.

**[Attendee]:** That wasn’t under your task list for your department?

**[Todd]:** It was, it was, yeah.

**[Attendee]:** Do you have an accessible video player on your site?

**[Todd]:** So the question was about an accessible video player. I know we are adding support for video captions; I don’t know where that is yet, in terms of if it is available. But there was work done for that. It’s not a Flash player, so its viewable on mobile. So those are two things that come to mind.

**[Dennis]:** And just so you know, at United, we’re using Able Player, which is, I believe it’s open source. But if you just search on Able Player, you can find it. It can obviously just … bring in videos you have locally or from YouTube.

**[Attendee]:** So once you supplied your color palette, can you go into the whole process? In my experience, a lot of times the UI designers and the graphic visual designers, they get kind of territorial about changing colors. So, when you were going through the process, just some of the reactions from the visual designers and user designers. I would just … my background was in that space and I always thought once you simplified the color palette, it makes things a hell of a lot easier, from a creative development perspective. I was wondering if you could share some of the insights into some of the learnings and growing pains.

**[Todd]:** Yeah. Well, fortunately our visual designer Josh Osborne was very sympathetic to this, and so we would work over Slack or video calls, send screen shots back and forth, like hey, what do you think of this? Does this color look too different to you? And he was pretty willing to make changes, which really helped. Because, I know …

**[Attendee]:** Is there any way, because it was somewhat hard in the projection, to see, is there anyway to get our hands on the this presentation, so I …? Sometimes, they’re just so subtle and sometimes you just need to show an example to a visual designer, to say look, we’re not asking you to change everything, such a subtle difference. Or it really doesn’t change the integrity of the design, it just makes it more accessible. Is there any way we can get the deck?

**[Dennis]:** If you’re willing to share the deck out with attendees, we’ll get a link out to everyone.

**[Todd]:** Sure.

**[Dennis]:** I know I was going to ask for it for the video editing.

**[Todd]:** Yeah, I’ll send it to you.

**[Dennis]:** Cool. Any other questions?

Thank you very much, Todd.

**[Applause]**


