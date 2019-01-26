# Designing Accessible Sign Up Forms
## Presenter: Michellanne Li  - Tuesday, December 11, 2018
[Source recording](https://youtu.be/ac1jkylPdPI)

**[Michellanne]:** Alright, hey y'all, my name is Michellanne Li and tonight I'm going to be talking to you about designing accessible signup forms.

Alright, so I know it's late, it's the last talk of the night and it's cold and dark outside. So y'all might be wondering, who is this chick I have to listen to for the next 15 minutes? I'm a designer, a developer, and an Accessibility Crusader. There's a ... inserted myself into a scene from Monty Python and the Holy Grail.

This is my husband. He lost his right leg in a motorcycle accident, so he wears a prosthetic. And accessibility is something that we always factor in when making travel plans. We were recently looking to plan a trip with some friends who have children. So I visited a travel website that specializes in kid-friendly property rentals. It's aimed at families and it has global destinations so we can assume global audience. Here's their homepage. It's really fun, it's really colorful, and it's been featured in some cool lifestyle blogs. However once I tried to sign up to create an account so I could book a rental, I started to notice some really glaring accessibility issues and I thought it would be an interesting design exercise to reimagine their user flow.

Now to be clear, this company has no idea who I am, they did not pay me to do this. But I really believe that by focusing on common design patterns and making them really accessible, we can have an outsized impact on users with disabilities.

Alright, so let's take a look at what's not accessible about this site, starting with the home page. So, for starters, none of the links have a focus state. And it would be really great if there was a skip to main link for users who are tabbing through the site, so they could skip over the navigation when they need to.

Alright, so to create an account you click on this sign up link in the main navigation and you get this window pops up and at the top of the window, there's a link to sign up with Facebook, then we have a form to sign up with email, and below that, if you already have an account, there's a link to login. So, let's say you already have an account. If you're tabbing through the site, you have to tab through this entire form to get to that login link. And the contrast is way too low, I could barely read it with my glasses on. Also, I just want to note the text on the right and all caps, those are labels, but the text on the left is placeholder text, which means that it disappears when users start typing. So, let's say someone starts typing their password and maybe they have a cognitive disability. Maybe they're just distracted, you know, and they forget that it's supposed to be seven or more characters. So let's say they enter like a six character password. 

So they are then taken to this page that has, again, a link to sign it with Facebook and a header one that says oops, and then there's the errors listed below that and the related input in which the error was made was highlighted. So this Facebook signup has a really odd placement. A screen reader would read that, you know, first It's first on the page and it's not that important in the hierarchy. It is nice that this header one makes it really clear what the intent of the page is. When you get to this page, you know that something went wrong and I like that errors are listed at the top of the page. However, it would be really nice if the errors linked to the related inputs, especially if this was a very long form and you would have to do a lot of scrolling or searching to find where you made the mistake. And the error text contrast is way too low. This is red on pink. It's very difficult to read.

Alright, so let's say you get this form corrected, you submit it. You are then taken back to the homepage and there's this blue bar at the top of the page that has a link to encourage you to update your details. And at this point, it's really not clear whether you've successfully signed up. This blue bar is easy to overlook. I honestly overlooked it when I was signing up and the text contrast within this blue bar is too low.

So this is kind of like that metaphor you sometimes hear in the accessibility community of taking someone out on a date and leaving them in a field, we don't know how we got here or where to go next.

Alright, so let's take a look at the redesign. Alright, so we're going to start, let's assume that you've clicked the sign up link and in the main navigation what happens next, this window pops up, this window has only three options. So we've got a sign up with Facebook and sign up with email and login. So having only three options means that you only have to tab a maximum of three times now in order to get to the option that meets your need. You're no longer tabbing through entire forms as in the original website.

Want to note a couple things in the code. So, these icons within the buttons is Facebook and email icon, these have an aria-hidden attribute because they're purely decorative. And this "X" icon is an SVG at the top right of the pop-up it has a title attribute as well as some hidden text to make sure that assistive technology understands that you click that in order to close the window. The purpose is really evident for users who wouldn't see it and understand that that's what the X means.

Alright, so you click on sign up with email, you're taken to this page next, create an account, there's a form that you can fill out and let's just walk through this form and the changes that I made in order to make it more accessible. So first off, all the form elements have a focus state, this first field is in its focus state. It's highlighted in yellow, there's ... it's hard to see in this presenter, but there's a bit of a drop shadow on it, the fields a bit lighter, all of these form fields have labels now, I styled them within the form field, so they sort of look like placeholder text, but as you can see with the first field, when you click into it, the label moves above the text that you're typing. So you can still see it as you go.

Required fields have asterisks. So you can visually see they're required, but in the markup, there's also a required attribute and visually hidden text. Just again, making sure that assistive technologies understand the things that are being presented visually. Alright, so if we move down to the password fields, third from the top, there is a little link, that's a show, on the right, and you can click that to reveal the password. So this is great for users with cognitive disabilities, users with maybe some mobility issues, who are having trouble entering their password as intended, or people who are just, you know, busy. I think we've all forgotten our password.

Moving down from there, there's a request that you verify your birthday, in order to prove that you're 18 years old or older. So, this wasn't part of the original form but I was doing some competitive analysis looking to see what other similar services are doing and it's a common thing to ask people to verify their age. You could certainly do some A/B testing to see if it's better to have them check a box to verify etc., but I thought it would be interesting to explore this particular design pattern of entering your birthday.

So, you know that that got me thinking about date inputs and, you know, my first instinct was to say, okay, people can just type out the date of their birthday. But, you know, date formats are not universal and people are often miss labels that tell them how to input information. Just to give you an example, my husband grew up in Europe. He likes to use European date formats, day, month, year. And I grew up in Texas, so I always say month, day, year. And for this reason, I have forgotten his birthday just like so many times.

**[Laughter]**

**[Michellanne]:**  He does not love that ... also anniversaries, it's awful. Anyway, um ...

So, I wanted to have the users select the month, the day, and the year. And even if you know they were kind of half paying attention and just hit the drop-down arrow for the select, they would still see amongst the options, you know that there are months listed or days ... or the days that are in a typical calendar month, etc. So that would help them understand how to input the information as intended. And then finally with a checkbox at the bottom. One more thing I want to note is that all of these form elements meet WCAG 2.1 contrast requirements. This is not specified by Section 508, which is currently tied to WCAG 2.0, but I think it's a really great new addition to WCAG 2.1, because it says that for non-text content that's really essential to understanding the meaning of the page, you want to meet minimum contrast requirements, so it's really visible and easy to see.

Alright, so let's say you're entering content, you're entering your information and you know, how can we tell users that they've made a mistake? And also how can we validate that, you know, they've correctly inputted input information? I didn't love the pattern of, you know, filling out a whole form and then submitting it and then having to go back and check through errors, I think that's a lot of cognitive load. So I reimagined this using dynamic validation to provide immediate feedback as you're filling out the form. So what this would look like is, when you enter the information correctly, a green check appears next to that field. And if you've entered it incorrectly, a red X appears. And what you'd probably want to do is have some kind of aural alerts to notify assistive technologies that some new information is appearing on the page.

These icons are really ... they're large. They're ... you can, they're very visible, they meet contrast requirements and even though they're red and green, which would not be great for users with red-green color blindness, you don't want to be relying on color alone to convey information, they're distinct enough from one another that you know it's very clear which is which. And also, we have the error messages appearing right next to the fields and questions, So you can get immediate feedback right there that helps you understand how to correct the error. You're not searching for where the field is and you've got the errors on the top. 

Alright, so let's say you get this all corrected, everything's great, you submit it and then you're taken to the success confirmation page. And it says success at the top. So you know that you have signed up for this service. There's also some, you know, suggestions that you could update your profile or start browsing homes. So again, we're not leaving our dates out in a field, they don't know where to go, we got them home, on time, within curfew and gave them our phone number.

**[Laughter]**

**[Michellanne]:** Alright, so I just want to note that all of these considerations follow best practices, but you absolutely want to be testing your work with users with disabilities. That is the best way to validate if it is truly accessible. And I have a question slide, but feel free to reach out to me. I'd love to hear from any y'all.

**[Applause]**

Thanks to our speaker, Michellanne Li.

Live captions provided by ACS, Alternative Communication Services.

Visit them online at acscaptions.com.

Live captions sponsored by McDonald's. We're lovin' it.

This has been a production of the Chicago Digital Accessibility and Inclusive Design Meetup. Visit us online at meetup.com/a11ychi Follow us on Twitter at twitter.com/a11ychi Follow us on Facebook at facebook.com/a11ychi. Subscribe to our YouTube channel to view recordings of previous meetup events at youtube.com/c/ChicagoDigitalAccessibilityInclusiveDesign

Copyright 2018. All Rights Reserved.

