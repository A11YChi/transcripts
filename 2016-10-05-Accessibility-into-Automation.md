# Accessibility into Automation
## Seth M Kane - Wednesday, October 5, 2016
[Source recording](https://www.youtube.com/watch?v=bep9xZX8eBQ)

**[Seth]:** ...the actual presentation, because mine is more of a hands on demo of accessibility and automation combined.

So, similar to what the other speakers spoke about using like Chrome tools, or various testing tools or auditing tools, one of the things that I’m going to demonstrate is, how to build that actually into your process like immediately rather than like a second step or something like that.

So disclaimer. I’m going to show you about aXe, which is produced by Deque. I don’t work for them, I don’t get paid by them, I just like their product. And I actually saw the NPR … in your Chrome, you had aXe actually installed too. So, a lot of tools out there, there’s tons of them.

This is just one of them that I found to be incredibly easy to use and useful. So a little bit about aXe, i.e. the Accessibility Engine. So Deque built this light weight JavaScript framework that is portable as is every testing framework out there. So if you’re in dev or have a dev team, you can build it into your unit testing, in your Selenium or your Cucumber or whatever, as more of an actual service. And then you can also, which is … there is a Chrome developer tool, which we saw in the NPR screen. And then I’m going to show you the fantom jazz implementation.

But, this is a list of all the different tools that aXe Core, it’s what it is called, can be plugged right into it, really neat. And again, I’m not getting paid by them. So, here is just some links. I will disseminate this Powerpoint presentation and also the code that I am going to show you, in my Git repo which you can all access. I’ll get to that a little bit later.

But basically, so aXe is core and there’s a link to their repo. And then they also have a very very extensive amount of API documentation. So if your developers are hooking it into various testing tools, they can look at it and other stuff. And then they also, what’s cool is, because it’s open source, they have a lot of other people building stuff on top of their core and that’s one of the things I’m actually going to show you. So one of the other projects.

Before I get into the cool automation stuff, I’m going to show you the Chrome Developer Tools extension, which is very similar to the Chrome one. So I decided to do a little audit of the meetup.com site. And basically you push a little button, which I’ll show you on this screen, and it comes up with a whole list of error and so forth.

So, what’s neat about this is not only does it show you the errors but it shows you the code that is erring out, it also shows you which compliance levels you may not be passing, so that’s in the top right hand corner. And then if you hit the inspect button, it will actually show you in the DOM which particular element isn’t passing. 

And then the one thing I actually really like, it links to the spec. So if you click more info, you can actually go to W3C right away and you can actually reference if you are or are not passing and so forth. I will caveat that they are continuously building this tool, so there are false positives and things like that. It is after the page renders when you use the Chrome tool, so if you basically, whatever you see on the page, and you hit analyze, is what gets rendered, so if there’s Ajax or anything like dynamic, it won’t analyze that stuff. It’s only whats in the DOM in that very moment in time. One of their bugs, which is a little silly, when you use it, it usually scrolls to the bottom of the page, because it wants to analyze the entire DOM.

So one thing you’ll do is you’ll have to just scroll back up to actually see everything. But this kind of cool, right. So it tells you like, HTML basics too, right? Like, it’s not just accessibility, it’s, ID attribute values must be unique. That’s something that is HTML validation. But it affects accessibility because if you have more than one ID in your DOM that’s the same one, a screen reader won’t know what to reference, or it might repeat it again, or something like Dragon, you know if you’re trying to do something, it might actually not know which one if there are two of them. So, it’s not just an accessibility tool, it’s also a basic, fundamental HTML auditing tool.

So this is the Chrome plug-in, I will break out of here really quickly in the live. … let’s see if I can do this while looking over my shoulder … so if I inspect, I built a little mockup here which I’ll show you, and I hit aXe, and I hit analyze, it shows me that I have errors. It scrolled down like I mentioned before, I scroll back up and I can click on something like this and it will say here’s is my HTML, the home link, which is this guy, it doesn’t have enough color contrast, we heard that a couple of times, right?

And then you can inspect it and what it will do it will actually show you in the DOM, this is where probably the Chrome tool could actually help out too, because you could run in Chrome and do some different examples and things like that. I didn’t know that it actually showed you different suggestions of changes, which is kind of cool.

So that’s aXe. The one thing that is kind of annoying for me is like, I have to do this outside of my banging on the keyboard while I’m writing code, right? I have to go into the browser, I have to be on the page that I want to do, and I have to hit analyze and I have to review it and I have to make changes. So what aXe did is they built this plug-in, but if you build it into your testing software, it does it automatically. So let’s get out of here, unless someone wants to see another page being analyzed? I’ll just in to the cool stuff.

So, let’s automate. So, I’m going to explain a little bit about... How many developers are there in the room? Just so I have a frame of reference. Ok, so about half. Ok, does anybody use pre-compilers like Gulp, Grunt, you know, SASS, anything like that? LESS? Ok, so most of you will know exactly what I am talking about.  The other people, I’ve kind of outlined it here a little bit.

So Gulp is a JavaScript framework that allows you to compile and automate some of your development cycles. So like with CSS, which is a compiled code, there’s frameworks like LESS and SASS that are un-compiled, that will allow you to do a lot more flexibility and things like that. And Gulp is running all the time and doing a lot of magic as your actually banging on the keyboard. So I have Gulp as my primary compiler. Grunt is the other popular one. I think there’s a couple more. But Gulp is top notch, I like it.

SASS. So, I’m using SASS as my CSS precompiled language, which allows me to do things like variables and mixins. So when you’re talking about color palettes and keeping things in check, you can right a variable called blue and every piece of CSS that’s referencing blue, you can change it to a different color if you wanted, without going back to all your CSS files and stuff like that. So it really kind of helps.

Webpack is a JavaScript and debundler. So this is where we’re doing a lot of enterprise, big big big JavaScript structures. So we’re using Webpack to basically take a whole lot of JavaScript partials … so imagine like a CMS library, where you’ll have a component for a hero, and component for a carousel and a component for let’s say a modal, it bundles all of that code into one, but it does’t access the code unless you need it. So it’s one file to get cached, which is great for performance, but it’s really very powerful.

If you’ve never used the next one, you need to do it. Browsersync, and I’ll demonstrate this. So Browsersync is a plug-in that runs in Gulp or Grunt, and what it does is it allows you to have as many Browsers open as you want, in as many locations as you want, and as you are coding, all of the browsers are refreshing while your actually coding. So one of the cool things is like I can have my iPhone simulator on the screen and my Windows IE and ... well I can't have that ... and my Chrome and my Firefox all at once and the minute I hit Save in my HTML editor, all of my browsers will refresh. So it let's me to actually see what's going on in various states and all of that kind of stuff. 

In addition, that if you have Browsersync running on an IP address that can be accessed from another computer, that other person looking at it will also see those changes. It's really really very powerful, very cool. So, the key to this automation is gulp-axe-webdriver. So I didn't write it. I found the plugin. Basically it is the gentleman that wrote a Gulp PhantomJS wrapper around aXe core. So what it does is, basically you run it, and it creates a PhantomJS, which is basically a visualess or headless browser. So it doesn't actually exist, but it actually acts as a real browser to do the tests. So just like I hit analyze in the Chrome Extension Tool, it essentially does the same thing and you just don't see what's happening. So it is behind the scenes.

Ok, so here's just a kind of example of my Gulp build. So, I build the stylesheets, I build the HTML, I do a little cleaning, I do some linting, which is analyzing if my JavaScript is actually accurate. I don't know why it does that. But I'll switch back.

I build all my JavaScript, I watch my environment, which is that Browsersync. I clean a little bit more JavaScript, it shows me what my environment is, and it does a little bit other stuff, and so forth.

Then, I'm going to show you this in a live demonstration, but basically while I'm coding, if I have this window visible, you'll see that the minute I hit save, it says Hello, ok, I'm going to test the URL, it's found three accessibility violations, and it shows me the traversing of the object in the DOM, which is body, nav, row, column, blah blah blah, and it tells me that this element has a color contrast of 3.0, which we learned is too low.

So this is actually being displayed to me live while I'm coding. I never actually have to look at my browser. So if you don't have two screens, or if you don't like looking at your other screen, you can actually just look at this while you're coding and it will show you all these errors and so forth. Cool right? Get it? Ok...

So, let me sit down. Let me do some coding. I'm going to switch views so I can actually see this. I want to show you how this all works. Ok, so I built a really bad dummy HTML page for this.

**[Dennis]:** Don't you find that to be hard to do?

**[Seth]:** What?

**[Dennis]:** To build a ... bad HTML page?

**[Seth]:** It was easy by installing the Foundation Zurb framework, which is like Bootstrap.

**[Laughter]**

**[Seth]:** Ok, so I love Foundation, don't get me wrong. But, fundamentally, there's a whole lot going on that's wrong. But let me first stop my environment here quickly. So, I'll just clear it so you see what happens. So I basically, I have in my folder structure here I'll just quickly show you, if I can find it. When I'm talking about technically... And all of this is available for you to download.

So I basically have, you know, my Gulp file, I'm using ES6 all my Node modules, here's my source, and basically, this is essentially what becomes my web server. Ok, so enough about that. We don't care. But, when I run Gulp, and a special command that I give it, you'll see that it's now starting to do its magic, right. And hopefully it runs, right. Ok, good.

And you'll see that automatically my browser opened up and refreshed. Like I didn't even have to do that. It magically did that. And if you noticed in the top right hand corner, which you'll see in a little bit, it said Browsersync and so forth and you'll see what I am talking about.

So right now, this is more or less how I develop. I have the log, or the Gulp log on the left and I haver my browser on a different screen. But I'll pull this up. So this is my codebase. And it didn't test it on load because I would assume that I'm just going to like make a little change here.

So I'm just going to delete one line and hit Save. And you'll see that over here, it did a localhost, so that's my web server, and here are all the errors, and I'm going to bang these out really really quickly.

So a lot of them are color contrast, because of Foundation (again). And then there's a couple down here like, this image doesn't have an alt tag or an alternative text model. Because you don't have to use an alt tag, you could use ARIA, which you wouldn't, but you could. Ok, so it actually would reference that.

And then I also have a little tiny form field in here that has no labels, right. So, right off the bat, I show you the page again so you can see it here over here just so you can see it refresh when I make a change.

So I'm going to go into my SASS and I'm going to get rid of all of the Foundation stuff really quickly. So once I do this, I comment it out, I hit Save, you'll see immediately in my browser, refreshed, right? Ok, and if I move this over a little bit, you'll see that I have no more color contrast errors. So that's cool.

So if I had a little bit more space, you could see this all in real time, right? So, while it doesn't look pretty, I'm not going to go redesign it, I just wanted to show you that you can do this.

So now let's get rid of that image error. So I go look at my HTML file and I threw in an image in here some where. ... do it the old fashioned way.

So, here I took a picture of bacon, oh it's my logo, right? Ok, but even though that logo doesn't need an alt attribute to it, it still needs the actual attribute of null. We just learned that. So if I add alt equals blank, and you'll see, it just finished, and now I have one error left. Ok, fantastic, I'm working.

Well, in the gaming, like you could do an audit afterwards think of if everyone one of your developers had a tool like this going at the same time you would reduce your HTML errors, you would reduce your accessibility errors like really fast because it's in your face.

Now just to kind of give you the opposite end of the spectrum here, let's assume that I had ... well let's get rid of the accessibility errors first. So we come down to my little form down here, I think, I have a form, somewhere,  where is it ...

... I put a lot of stuff in here ...

Ok, so here's my form, right? So I'm going to add a label, because we need to have a label. So you could do it like this ... you know, input, right and then I'm going to wrap my label around here, because that's how I like doing it, I hit Save and, I have no accessibility violations, according to this page.

Now, before I go on any further, I'm going to show you something really really cool ... So I built a configuration file for this, for aXe, and Gulp, ok? So what I've done, I've said here is my dev environment, which is traditionally what you do with Gulp, here's my, where my web server environment is, that's nothing unique.

But what I did do, I created my own accessibility rules. All of these attributes in this object, are part of the aXe plugin.

So for instance, like I built enable, or to disable, so if it was actually annoying me, that I was doing a lot of maybe pre-coding and all of these errors are flipping out at me, like I might turn it off, which I'll show you here, so if I undo all the good stuff I just did, you'll notice it doesn't actually audit my code, right?

So you may want to turn that on, or maybe a gatekeeper, like a lead or a manager will turn that on or off depending upon the developer or what the point they are in stage so I added that ability in my Gulp file.

Let me turn it back on, because I want to show you something, ok ... and then I... 

Unfortunately you have to stop and start Gulp every time you make a change to the configuration. But one cool thing is that the aXe program and the web driver that this guy built, you're allowed to post in as many files or URLs as you want to be audited.

So in my case, I'm building the site using partial HTML files. And one of the accessibility criterias is that everything audited needs to have an HTML tag and a body and a head and all of that kind of stuff. Well, if Im auditing individual files, which is just chunks, so instead of doing like auditing something like index.html, I actually pass in a URL.

Now, you're saying "well what happens if I wanted to do a different page or more than one page?" They built it so you can just pass in as many URLs as you want. So I can add as many supplemental URLs as I wanted, and all of those will be test every time you make a change, regardless of what page that you are on.

So if you were building a component in a CMS, that was on, say, five different pages, but maybe they had different treatments, or they had different styles or something like that, it will scan those, just like if you were to open five browsers and do it in Chrome or in the aXe developer tool. So, it's super super powerful.

The other thing that it does, just natively, I didn't do any of this, you are allowed to include or exclude selectors. So I could do something like exclude the nav ... or include the nav, so I only want to scan the nav, because I'm working on it. Everything else is junk. Or visa versa. So you can pass in and out of these parameters. And in the documentation of the API by aXe, there are all of these special conditions and things like that.

One of the things that the Phantomjs plugin doesn't do yet but aXe does is, you can tell it what priority level you want to check against. So, you could say like, I only want to check against Section 508. Or I only want to check against WCAG 2.0 level 2. Like you get to pick those things, and you can pass those things in as parameters. So it's really really really powerful and imagine like basically doing your site and instead of, you know, you can make changes, and now it should tell me look at all of these errors that I've got, and part of the job is to whittle them down.

So, this automation is great for developers, but it can also be amazing for QA people, because they could pass in a whole site. 15 thousand URLs essentially, and it can test out all of those. And you could have a log actually printed and all of that kind of stuff.

So, there's a real real lot of powerful things. Since I mentioned it, I'm just going to show it to you here.

So here's my web page again, I just wanted to just show you how this works with Browsersync ... so let me open up my iOS here ... I didn't plan to do this, but I'll do it anyway. So here's my iOS simulator and if I open up this page, one of the cool things I did here, I put in this accordion, but it doesn't work until I click this bacon.

See how I'm scrolling up and down and the actual page moves? And then if I click Select Bacon, which, I probably have a JavaScript, you'll see that turn light gray here, and if I click, I might have an error, but essentially, this is really neat, because now if I come over here and do it, I can actually do it, visa versa.

Very powerful too. So between using Browsersync and Gulp and aXe plugin, all of my, let's call it first draft QA-ing, is being done while I'm coding. And Gulp also allows you to do things like JavaScript checking, so if you're a JavaScript developer, if I open up a JavaScript file here and I ... let's just change this guy, and let's say, I'm sure you've seen this a thousand times, someone leaves off a semicolon, right?

Ok, well it says here, I've got an error. So there's all of these powerful tools that you can build into your compiler in addition to accessibility tools. And, I'm doing this on the fly, rather than going and actually using the same exact tool by inspecting and then by analyzing and then doing that. So, really really, exponentially helps the development process.

And on that note ... I will say ... Questions.

**[Laughter]**

**[Applause]**
