**Fen Slattery:** Okay dokey. We also want to encourage you to take a look at two specific hashtags. This is a meetup not only about accessibility but also inclusive design, so we are very passionate about — sorry, there is a train going by the house. 

One second. I should have closed the window so you wouldn't hear it. We want to really encourage you to take a look at two hashtags that specifically center disabled black voices, those are #DisabledBlackTalk and #DisabledBlackLivesMatter on Twitter. You should definitely take a listen and amplify those voices with the platform you have. 

And now to the main event. [Makes trumpet fanfare!] 

I am going to read you this lovely intro about Kathleen and then I will let Kathleen take it away. 

So Kathleen pronoun she/her is a full stack engineer with a design background. In other words, she really enjoys the front of the front end, digging in to new technologies and talking about accessibility, React component libraries, design systems and inclusive documentation. 

She is also a color module specification editor for the W3C design tokens community group. And when not coding, designing or speaking about things, which is a lot already, Kathleen is the best Lanterne Rouge cyclocrosser you will ever meet. 
Kathleen, you sound really cool, I am excited to hear your talk. And we also have your Twitter on here too if you're live tweeting along, you can tag Kathleen. Kathleen's Twitter account is @resource11. 
 
That's resource one one and that's all I have. Kathleen. I think you're good to take it away.
 
**Kathleen McMahon:** Wonderful. Now I will share my screen. And we're going to share the screen and then start the presentation. Here we go. I have to hide you all in my thumbnails or I can't stay on my notes and stay on track. 
 
Going back, previous slide, there. Take two. Welcome every one, my name is Kathleen, my pronouns are she and her. With a tickle in my throat tonight, bear with me. I am here today to show you how accessibility-flavored React components can make your design system delicious. 

Before we begin, let's get some details out of the way. I know that there's a slide deck posted in the A11yChi [chat] for the SpeakerDeck URL, but if you also need a copy where you have speaker notes and I also have some links to resources, I have also a copy here for anyone that needs that type of documentation at https://noti.st/resource11/cb2h86
 
I will also share that link at the end of the presentation and on Twitter after the meetup. 
 
Whew! That was a mouthful. 
 
You can follow me @resource11 on Twitter, Instagram and GitHub. 

Now that we have an outline, gotten those details out of the way, wow it has been a long day, let's talk about what we will be covering today. 
 
Oh, yes, there is an agenda. Who doesn't have one? 

We will talk about why accessibility first, design systems, they are cookbook, design systems and React. We will also talk about icons, buttons, inputs and sneak in a little talk about disclosure widget patterns and wrap up with some documentation tips. 
 
Before we begin, let's review who I am, a little bit of a better introduction. I am a principal engineer at CarGurus and I race bikes very badly. Mostly you will see me in costume, racing two laps to your six at the back of the pack on a single speed. Mostly. Unless something happens, like perhaps a pandemic kicking in of doors then your racing season is postponed. 

So, while I am an engineer and super slow bike ricer, I am also a dev dinosaur and I find it fascinating to see how far we have come in terms of the tools we have had for computing and software and storage, reference materials, and browsers. Our browser choices were minimal back then. Netscape anyone? Our stack, though, has stood the test of time — HTML, CSS and JavaScript.
 
Fast forward to now, an industry is moving at a really fast pace. And it can feel overwhelming to keep up much less find the place where you can thrive, especially if you have both designing and engineer skills. And especially if you love that fundamental stack. But fear not, dinosaurs are always the hotness. 

Those old school HTML, CSS, and JavaScript skills are highly valuable and transferable no matter which framework or library you happen to use. And those skills will give you an edge in the industry where the `<div>` has become the reluctant king. So before working at car gurus, I was the tech lead for the O'Reilly Media design system team. I learned a lot about streamlining component libraries during my time there. If you have ever worked on design system, you know there are a lot of things to consider. And great design systems combine two key factors: User experience and the end user experience. 
 
However, like herding cats, creating a great design system can be tough with so many moving parts. If you happen to be rebooting a design system from a previous version, you will have to choose what to tackle first. If your design system team is small, you will have to be very strategic. For example, if you have any business logic in your components, 
your first priority should be to extract those out and build within accessibility in mind. Fix your colors, fix your components, then reboot your docks. You may ask, why accessibility first? 

Well, our users have varied needs, and because so often accessibility is what is handled last. And that sends a poor message to our users. If you have read the WebAIM Million report, the results are depressing. With the amount of errors found on pages - 97.8%, unlabeled - 59%, and 60.1% of unnecessary ARIA attributes added to the page. We are making the web worse in the name of good intentions. 

While we have things like the Web Content Accessibility Guidelines to follow, which really sets a really low bar to pass, we have been missing the mark in the industry when it comes to making sure all of our users can use our apps. 

Imagine, though, if you had accessibility baked in to some commonly used components, a design system is the perfect place for this. I would like to say your design system is a cookbook, and cookbooks have a personality. My mom is a serious fan of cooking and lately I have been digging into her cookbooks she has collected over the years to read how recipes have evolved over time. If you happen to take a look at some of the cookbooks published in the 1940s through the 60s and look past those outdated views on women, you will find some
interesting recipes, questionable food combinations that include Jell-O with shellfish, yum, but also an impressive level of detail paid to the structure of every single part of the cooking process. There is even a section on table settings and entertaining. This is very similar to how a design system works. Now, what does that have to do with React? There is always some debate on how using a JavaScript library creating inaccessible apps. 

Yet, if you look at the React documentation, React states that they fully support building accessible by using standard HTML and CSS techniques. They don't say that, but I am shoving it in there. A better way to think of it as a kitchen utensil, it is not the only utensil in your kitchen. You are the cook. In my opinion it is up to the developer to understand those HTML, CSS and JavaScript and accessibility best practices to be able to leverage a utensil correctly. And that includes React.

That said, if your developers are unsure how to start building inclusive apps, empower them with your design system. Build some features in to your component to help them along.

Then you can start celebrating when your coworkers make those apps accessible without you having to ask for it. Now, components, they are your tried and true recipes. And 
WCAG is your reference material. Creating a component is like following a recipe. First, you start off with high quality ingredients, that's your semantic HTML. You mix in your seasonings, just a touch of ARIA attributes, follow the directions, your documentation; and provide helpful hints as best practices. Let's take those principles and apply them to some components. 
 
Starting with icons, icons can be either informative or decorative. Informative icons need to be paired with descriptive text to be perceivable by screen readers. Decorative icons need to be be hidden from screen readers because they don't add enough significant value to your app to be announced. But wait, icons can be interpreted in so many different ways. True. For example, you may say the heart symbol used to favorite something in an app, other apps may use a star, this leaves way too much up to interpretation by the user. Ideally you should be pairing any icons you use that are informative with visible text. This way users will have a clear context on the purpose of that icon. Of course there is a big but here, because — well, a big but in here, sorry, I am about to pun, and I refuse punning about butts, but getting icons paired with visible text also depends on the buy in you get from your team and the organization for particular icon usage in your designs. And it depends on whether you can get a design approved that uses a label paired with an icon like this. This is the ideal scenario. 

But in general terms, there is more than one way to create an accessible icon. Two of the most recent ways are SVGs and icon fonts. At O'Reilly, we initially used SVG icons in a design system combined into a spreadsheet, yet we ran in to some problems when we started testing. We discovered a bug when testing in Safari on the High Sierra operating system where voice over would announce every single one of those 100 or so icons in that spreadsheet. It made me sad, like Natalie crying in the corner. 

So, we had to think fast to find a different solution, remember, small team. So, icon fonts to the rescue, we converted all of our icons into a font set for the time being and choose to revisit the SVG icons later since that High Sierra bug has now been fixed. Let's go over an example of how to make a component using HTML and the icon font technique. So this is what you will typically see as an icon font in the wild but it is not accessible. This is an accessible pattern. Let's break it down. 

The span containing our icon font has been sprinkled with a pinch of `AIRA-hidden = "true"` to hide the icon font from our screen readers. The second span contains the descriptive name for our icon and has a `"visuallyHidden"` class added to it. This removes the visual presentation of that text yet keeps that text available for screen readers. 

In the wrapping span, we use a CSS class to convert the span's native `display` property from `inline` to `inline-block`   This allows us to support margin and padding customization on all four sides of the element. Notice that we are using spans, all the way down for all of these elements. This is done on purpose for when we pair this component with a button.
 
Now, before we refactor this pattern into React syntax or JSX syntax, let's consider whether this icon is informative or decorative. If it is informative, we keep the markup as it is because informative icons should announce. 

If our icon is decorative, we would add this ARIA hidden attribute to the wrapping span and set it to true to ensure the entire group is not announced by a screen reader. 

Now that we have an accessible icon pattern, let's pop this into a functional component in React and and convert to JSX. You are going to change that class to class name, convert that true string to a boolean value and self-close that 
empty span and voila now this is a static icon component in syntax. Let's make this component more flexible though. And expand that syntax to support incoming props like `iconHidden`, `iconName`, `iconTitle`, and add some guardrails. 

It is important to create guardrails for your components so you can always be sure that your developers are using the accessibility features that you have mixed in. 

For our icon component we have added three guardrails. 

The first is set up a check if the icon name, the dev passes in to our component exists in our icon library. If that icon does not exist in our library, the component does not render in the app. 

The second guardrail we have set here is to ensure 
if the developer doesn't pass in descriptive text to that icon title prop, the icon's default name will always be exposed to screen readers as fallback.

The last guardrail is the icon hidden prop. This one ensures that if the developer passes in `iconHidden ? true` here, the containing span will render in the DOM with a hidden attribute attached. If no `iconHidden` prop is passed in, the `aria-hidden` attribute isn't attached to the wrapping span at all.

This way we are guaranteeing that the icon will read out to screen readers no matter what, unless the developer specifies purposely otherwise by passing in that `iconHidden` value. This `true` or no pattern works very well with HTML attributes that only need to be added if the value exists to support screen readers that are modern screen readers and, I believe, older 
screen readers. ARIA is one of those attributes.  

You may still be saying what about SVGs? What if I haven't rolled my own icon set? Well, there are great options out there to do this with SVGs as well. 

For example, Font Awesome is still a great option. In fact, Font Awesome now has an official React component that you can use. And it has been built with accessibility in mind. Hooray. It is pretty straightforward to use this component, and it adds the right properties for you under the hood by default. 

There is a slight bug if you want to use this component as a standalone informative icon though. Say you want the icon to announce as a beverage in this case. And you pass in an 
`ariaLabel` prop to the font awesome icon component. Yes, that ARIA label will render; however, because the SVG element already has an `aira-hidden` attribute attached on that SVG 
element, that `aria-label` will do nothing here.

However, you can get around this by using the icon component we built and swapping out the span that used the CSS class that attached our icon font and swap in that Font Awesome component instead. Then you can leverage that `visuallyHidden` span to make sure your icon is informative.
 
Moving on to buttons. Buttons perform an action on the page. 
Buttons should look and act like a button, not a link. Don't get me started on that. [laughs]

Buttons will get screen reader for free. It is amazing. Our high quality ingredient here is the button element. We will sprinkle an `aria-label` prop here, well, attribute, to support instances where we have multiple buttons with the same name on the page to give context to screen reader users. Like those times when you have 10 more 'Read more' buttons on page, with this label you know it allows you to read more about dinosaurs. Also, notice it is important when you're using an `aria-label` in this way to match the first words of the `aira-label` with the words in the button text to support voice recognition software. 
 
If your app needs to support localization, Adrian Roselli wrote a great article with a different pattern that uses the ARIA described by attribute. That article will be shared in the resources. 
 
This is an accessible button in JSX. If we want to support button text with icons, we mix in our icon component and we wrap the button context in a span for positioning. Note here we are using inline level elements inside the button children. We should not be nesting things like other buttons, other links or other controls inside a button's children. That is not valid HTML. Also, this is why we had those spans. Remember those spans? Because spans are in line elements, we are cool here. Same thing with if someone — remember a `div`? If a `div` has no semantics? `div` renders implicitly as a block level, this is why `span` instead of `div` belong in a button. 
 
This JSX is popped into a component - into the components
render method - and we add some props here. We are going to add the `onClick` handler to support whatever function the developer wants to pass in, and we are going to add some disabled button support using that true or null pattern. 

The one guardrail we add here will ensure that if no icon name is passed in, no icon will render in this button. 

Inputs. Input need labels and error messages because labeled inputs give all users more context. And no, placeholders are not labels. Avoid using placeholders instead of labels because they will lose context of where they are. Placeholders hard to style across browsers. (Thank you, Eric Bailey.) And placeholders are not auto translated. 
 
We built our input components to minimize horizontal scrolling and we stacked our labels above the input — we stack our input labels above the input and the error messages below the input to support screen reader. To support screen magnification users.

Also you can place the error message right below the label for 
even better discoverability if you want. There is an article by Adam Silver that talks about that. He has great articles about forms. 
 
Now this is an accessible input pattern. It is a bit hard to 
read, so let's zoom in. We start with our high quality ingredients and pair our labels and error messages to the input. In JSX, we associate our label with the input by pairing the `label htmlFor` prop with the inputs ID value. We are going to mix in some key ARIA spices for validation. `aria-invalid`, `aria-required` and pair that `aria-describedby` value with the error text ID values. 

We will also add an `aira-live = "polite"` attribute to the error message span to make sure that errors are announced to screen readers immediately at a convenient stopping point.

To make this component even more flexible, we are going to add mix in some disabled attribute support and some synthetic event support like `onChange` and `onKeyPress` handlers to capture keyboard actions. We are using that true or null handling pattern here as well.
 
Add your guardrails. If your `div` does not pass in 
a label, the whole input will not render. Neither will the icon. This will help guide the developer to follow best practices when implementing a component, especially an input. And this will become second nature when a developer is creating any type of input, they will know to pair input with a label. So it is a great muscle memory to establish. 
 
Same goes for error handling. If the developer does not pass in both the invalid prop and the error message to the component, the error message will not render.

Fancy and new. A disclosure widget is an interactive pattern that uses a button to control the accessibility of a vision content. This pattern is great because of that flexibility and because it is keyboard and mouse operable and its base functionality is very similar for more than one type of interactive component. 

Some common patterns are nav menus, toggle tips and settings disclosures. Other types of widget patterns are custom select menus and autocompletes, which will not be talking about those today because in addition to needing enter spacebar and escape key functionality, those two patterns. Also, needs up/down arrow keys and home/end key support, and you know, autocomplete. Also, needs to be paired with an input.
 
One important thing to note. A tool tip is not a toggle tip. 
Those interactions are completely different. A tool tip's interactivity revolves around hovering over the tool tip and focusing with a keyboard. This can be problematic for any sort of touch device that doesn't support hoverer like a mouse or eye tracker. 

Also anyone using a screen magnifier may accidentally dismiss a tooltip by moving their field of view and hovering away. 

And in my resources, Sarah M. Higley, she is the person to 
watch and listen to about tooltips. She has a lot of opinions and good patterns. 

The three primary interactions we will focus on here are the space bar and enter key functionality, which comes natively when you use a button to open disclosure, and the escape key and also handle mouse clicks. 
 
For special cases, like a search menu that toggles into view when you press the button you can actually send focus to the 
first item in the open container with the pattern. 

I am going show you. Let's take a look at a disclosure widget pattern in CodeSandbox, so I will open up the browser. And I have this CodeSandbox to share later and I am going to hide the floating meeting controls. (Yes, thank you.) Okay, so here is the disclosure widget pattern, so you are, you have things 
for React that you're importing React, some hooks for use creating refs, states and effects. Basically, some life cycle hooks. And we're also importing using a button in here. We are going to pair a button down here. 

I am going to show you just what returns. Basically, you have a wrapper div and a button and a div here that is a container for whatever you're going to pass into this disclosure widget. If I click on something with my mouse, this pattern opens and closes. And here if I hit the tab key and space bar, look, keyboard functionality. How amazing. I can also do the same thing with the entered key. Amazing. And if I hit the escape key  

I will keep those tools apparently. Thanks. That is the beauty of Zoom. Zoom sometimes hijacks your key commands. I will see if it works. Yes! So as long as I keep these tools up here, I can use my window. If I expose my disclosure widget and hit escape, the widget closes and the focus stays back to the button that opens the widget. Pretty cool. To make this pattern, we have a button that is grabbing a bunch of ... (Hello Otis. Go over here. Over here. Over here. Good boy.) [Laughs] Otis entered the building. Okay. So over here 
we have a bunch of attributes that we want for the button the ARIA attributes we have is `ariaExpanded` to control whether the button is opened or closed if `ariaExpanded` is true. The container will be open. Also we have this `ariaHasPopup` attribute to let this button know that it is attached to this div. 
 
I also have a ref to have a reference for this button to this div and this extra class is a way that you can override classes, using css modules into this button so we can style this as we see fit, passing in whatever icon we want into our button component, whether we want to have an icon only button — we can pass in an `onClick` handler and basically toggle the 
button open and also do other things if we want and we can pass in what if we want to have a large or small or medium button, which is great. 

And in this div, this shows the children only if it is 
open. So this is controlled by some state up here, so right here, we have establishing our state, making some refs.

So, we can talk to our button and we have some handlers. We can't have handler for if the button has toggled this open and someone has pressed either the escape key. It has pressed the escape key. We are going to close the button and send focus right back to this button.

This function will toggle the button open and close and we will basically toggle the state to true or false. This `clickOutsideHandler`, and by the way, this pattern is based off of inspired by Marcy Sutton's Frontend Masters course on 
Accessibility in Javascript. She has a great pattern for this that I took and expanded to make it more of a flexible component, versus a one-off. She has really great techniques you should look at.
 
We also have this function here. A `clickOutsideHandler`. If you happen to have this disclosure widget open and you click outside, it will close it for you and it removes. And it removes focus, which is great. And it also resets the state for you so it is a really nice pattern, like to reset your state.

We also have some event listeners from mouse up and key and key up to listen for that `clickOutsideHandler` and we also have a function here that if we say that the first item is going to need focus - if we pass that into our component -
we can focus to set focus to that item. And also, we have some cleanup functions and here, also a function, to when you unmount the component to remove any event listeners. 

Now, so this is the general pattern — what we can do though in our app we have that disclosure widget and we have it here so we're passing in that that widget. We also have three other widgets that use this as a basis. For example, let me hide this one. Make sure everything is working.

I will show you the toggle tip. Making sure everything wraps, is in the toggle tip pattern, I am inside the div, I am inside just the widget here. I pass whatever I want and style it as a want and it is fantastic, because what I can do is over here everything is good.
 
If I — first I will show you all three at once. This uses the 
disclosure widget under the hood. I want to keep this nice and big so everybody can see it. Look at this. Mouse, keyboard, glorious. 

The next one I will show you is this one here, the settings 
disclosure. What if you have things like a menu where you want to toggle some settings. For here we have the widget and we put on an unorder list and I map an unorder list with buttons in there. With this pattern — I will use my keyboard. Click to open. Look, you can select your grape and then if you hit escape it goes back to the button that opened it, another nice pattern. 
 
The last pattern I want to show you is a search widget pattern. What this one does is, I am passing a form that has an input and a button, a search input and a button that will make this particular pattern. And notice how it went to that search input. That is because we passed in here `inputRef = {firstItemRef}`. Just by doing that here and here, here, basically creating a ref at the end of your function. Declare your function, make it a ref, set it to null, pass it in to your widget, and also pass it in to your input and what is great is when you open it, that is fantastic and you hit escape and now you have over here. (Agh. Way too many things.) What is really great about this now is I have a pattern that will close the previous one, open this, and just do things. Basically expand it for many uses. So that is pretty cool. Back to the presentation. 

Documentation — those massive design systems out there have some drool-worthy patterns for us to dream about. If your team small, show the examples of the many ways a component can be used is a good first step. When we were rebooting our docks, we used Gatsby for our style guide to leverage the power of MDX because MDX was pretty new and Storybook was pretty new. We also used Storybook to document our component playground.

We also deployed static instances of our docks using Zeit's Now product, which has now been renamed Vercel. And Now has ruined all my 'now' puns about the software. I can't call it later anymore. 
 
Moving on. I want to touch on Storybook for a moment. Storybook is a fantastic way to sandbox your components in isolation and play with UI logic without the complexity of business logic. And now Storybook supports MDX as well, which is fantastic. You can use it for a one stop shop. The accessibility is a must for Storybook. That add on uses the ax core engine under the hood and does a quick audit of your 
components, identifies the errors, tells you how serious they are and gives you steps to fix them before you start your manual accessibility process. 
 
When documenting your components, you should add helpful hints to help your developers to know how to choose how to use your components. For example, how to make an informative icon or decorative icon. Be sure to add props tables for your components to your components, so your developers know which 
prop does what and whether it's required. Add those component "do's and don'ts" as well. Those are essential because it is so possible to make accessible components and use them inaccessible. Dedicated page to accessibility resources and add all of those links you have curated. The WCAG success criteria is intense to parse. Make it more straightforward for your design system users to learn how to build with accessibility in mind and how — show them how to implement common accessibilities by adding this to your documentation. 
 
So to wrap up our users are diverse, your design system is a 
cookbook, cookbooks have accessibility, components are your tried and trued recipes. WCAG is your reference material and document, document, document it all. And remember, dinosaurs are always the hotness. Thank you. 
 
Santina Croniser: Thank you, Kathleen. That was so amazing, everybody has been saying in the chat it is a wonderful and inform TIFR and we have folks from YouTube as well that have enjoyed this. We appreciate your knowledge in bringing all of this information about design systems specifically as it 
pertains to React. Thank you. 
 
Just to remind folks, please ask questions. It is so very 
thorough that I didn't see any questions along the way, but if folks just want to through the questions in chat or certainly at this point you can unmute yourself and ask questions, we would love to hear from you now. 
 
**Attendee:** I have a question. So Kathleen, could you expand a little bit more on the consequences of not following the true or null pattern? Maybe a more specific example would be taking the case of ARIA hidden versus ARIA expanded? 
 
**Kathleen:** Yes. ARIA hidden, ideally if you had ARIA hidden you would want to have — all right. So if you want to hide something, you would put in `aria-hidden = "true"`, right, that would hide the wrap. Anything that is a child of that, it would hide the wrapping span of any of the children inside there. I remember some conversations with, I believe, 
Scott O'Hara where he mentioned that there were some old screen readers that if you happened to — I used to do ARIA equals true or false. He was mentioning some old screen readers, if you even had a value in the ARIA hidden attribute attached to your element in the DOM, it would still hide things. Those attributes where it should be like `aria-hidden = "true"`, or ARIA input check, it should be just added on to the element or not at all so you don't confuse any of the older assistive technology that will behave unexpectedly. With ARIA expanded, because ARIA expanded is a true or false thing, because that would not identify for true or null pattern. But you wouldn't want to add — you want to make sure that particular ARIA expanded attribute is not added to your button unless you are using it as part of something with a disclosure pattern. You don't want to attach it unless it is the purpose of that. You can add the ARIA added attribute and have three, true, false, null, and attach it to null. 
 
**Attendee:** Yes, that makes sense. Thank you. 
 
**Santina:** You also have a question in the chat. There is a lot of growing in the space. What is the best way to learn the fundamentals?
 
**Kathleen:** One is A11yProject.com, and that has been a great resource over the years. It has just undergone a redesign with Eric Bailey, Tatiana Mac, and a whole bunch of seriously talented people. I have a whole bunch of links on my resources in my deck that I can share. 

Let me add this — noti.st/resource11. In there I will share later the full URL which will have my presentation with all of the links. I learn a lot by following lot of people. Deque is a good place to learn about some tips. The Paciello Group. Knowbility. FableLabs is a place for, like, real testing with, you know, user testing with real users with disabilities that will give you the best feedback you will ever get because you're getting read feedback. 

Smashing magazine does, you know, some good articles. Someone named Eric Bailey tends to write a lot, I tend to bookmark a lot of his stuff. Marcy Sutton is another big name to follow. Scott O'Hara. I don't know how to pronounce her last name, I-R-E-A-D-E-A-D-E. (Agh. I don't.) It is very long name. Very good articles. 

Look at my resources. Another person has been talking about EJ Mason. He has interesting talks, perspectives, I would learn from him. 
 
There are more that I'm not thinking of now. Carrie Fisher. I could go on. Lainey Feingold. Every one that spoke at Accessibility Toronto last week. All of them. Let's see. I think Jen Luker will talk a bit about React. 

I see another question, span for loading your icons, if there are down side to using an image oh element to display your icon. So what I did there was we took our SVG icons and we ran it through a tool and converted each of the icons in to a font set. Those were being loaded as fonts. We had like the wrap around span which was wrapping around — well, the first span that contained the CSS would attach the font and then the second span would be that descriptive icon. In terms of images for when you were using the SVG pattern React font awesome icon, I believe that SVG had a roll of image in there and that was following some particular SVG best practices. There is an article by Carrie Fisher I put in my resources of all the different ways she has tested SVGs, different patterns. She has a whole grid on how each of the techniques announce in various screen readers. If you are making an SVG and using a roll image you would have to do other things to make it either announce or not. 
 
**Santina:** Thank you for answering that. It looks like we're getting a more intimate group, so feel free to take yourself off mute if you have additional questions. 
 
**Kathleen:** I will nerd out and do a little more. You probably didn't see it when I was talking. I had this behind me, the lighting scenes that would change every 15 minutes. You probably missed all of that so I will change one more of them. We will go back to fall foliage. 
 
**Santina:** What kind of lighting system is it? 
 
**Kathleen:** Hue lighting, and probably because I have it not connected to the right WiFi. I have been having a great time just playing. It entertains me. Now we will try it. 
 
**Santina:** That looks like a new toy I need to have. 
 
**Kathleen:** Yes, I had to play with some lighting. 
 
**Santina:** Conner has a specific question, but is worried about monopolizing your time. And Eric wants to know if you have a blog. Please respond to those. 
 
**Kathleen:** So the quick question is do I have a blog, yes, KathleenMcMahon.dev, right now has about 9-10 posts on how I did the 100 days of Gatsby and talked about MDX. I also did a post on there, cross posted, which was on 24 Accessibility, and also on my blog post about how CSS, fonts and relative units — how they're still a big deal. Like please don't use pixels for fonts and why.

Connor, what is your question? 
 
**Connor:** I was wondering if you can go in more detail about the behavior of input errors, particularly related to the ARIA live polite behavior. If you have a form that fails on submission with multiple errors, will it read out all of the errors or just the first one? 
 
**Kathleen:** This is the ARIA live that we put on that span that contained the message, that created a live region. If there were any errors in each of the inputs, like first, ideally you have them paired with each input where you group with a section. Well, there are two ways. You can have input above and below the errors, so they show up but also have them in a separate region all in one bucket and put a live region for that one area that contains all the errors and have an `aria-live = "polite"` on that one bucket and it will announce all of them when you try to submit it fails. The minute it shows up, they will announce so it is up to you when you want those to show up. 
 
Connor: So if I had a form that had two inputs, first name/last name and I just click 'Submit' right away, and they had individual errors beneath each one of them, would both of those get read by a screen reader? 
 
**Kathleen:** Yes, if you put the ARIA live announcement on your input component message. That is one way. Another way you can do it is not have an ARIA live and have a separate area in your form that collects all the errors, like a copy of all the errors in one region. And it will announce what ARIA live will do is announce the changes in that region. So whenever there is new text, there will be — it will be announced. I think ARIA is true for that, it will listen for changes for new text. 
 
Now I know why my other cat isn't meowing because I closed him in the bedroom. Poor kitty. Oh Otis is up there, that was the one walking in front of me during the whole presentation. 
He is very content. 

**Santina:** We have about three minutes left. Thank you for coming. If you have one quick question we can squeeze in the last couple of minutes, we are happy to do that. Otherwise certainly we appreciate you spending time with us today and we would love for you to come back to our next meetup, I believe, Nick, confirm, I believe one next month, is that correct? 

We are working on what that subject will be and working on 
announcing it so you can look for that shortly on the meetup page. Otherwise thank you. 
 
**Kathleen:** Thank you every one. 
 
**Nick:** Thank you Kathleen. 
 
**Kathleen:** Thank you for having me. This was fun. 
 
**Santina:** It was a great presentation, we appreciate it.