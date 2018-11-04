# Accessibility into Automation
## Seth M Kane - Wednesday, October 5, 2016
[Source recording](https://www.youtube.com/watch?v=bep9xZX8eBQ)

**[Seth]:** ...the actual presentation, because mine is more of a hands on demo of accessibility and automation combined.

So, similar to what the other speakers spoke about using like Chrome tools, or various testing tools or auditing tools, one of the things that I’m going to demonstrate is, how to build that actually into your process like immediately rather than like a second step or something like that.

7
00:00:29,900 --> 00:00:35,660
So disclaimer. I’m going to show you about aXe, which is produced by Deque.

8
00:00:36,140 --> 00:00:39,460
I don’t work for them, I don’t get paid by them, I just like their product.

9
00:00:39,820 --> 00:00:45,460
And I actually saw the NPR … in your Chrome, you had aXe actually installed too.

10
00:00:45,460 --> 00:00:48,720
So, a lot of tools out there, there’s tons of them.

11
00:00:49,060 --> 00:00:52,800
This is just one of them that I found to be incredibly easy to use and useful.

12
00:00:54,160 --> 00:00:58,040
So a little bit about aXe, i.e. the Accessibility Engine.

13
00:00:58,340 --> 00:01:06,640
So Deque built this light weight JavaScript framework that is portable as is every testing framework out there.

14
00:01:06,960 --> 00:01:12,700
So if you’re in dev or have a dev team, you can build it into your unit testing,

15
00:01:12,700 --> 00:01:17,880
in your Selenium or your Cucumber or whatever, as more of an actual service.

16
00:01:18,120 --> 00:01:25,340
And then you can also, which is … there is a Chrome developer tool, which we saw in the NPR screen.

17
00:01:25,960 --> 00:01:29,520
And then I’m going to show you the fantom jazz implementation.

18
00:01:29,900 --> 00:01:34,020
But, this is a list of all the different tools that aXe Core,

19
00:01:34,020 --> 00:01:36,780
it’s what it is called, can be plugged right into it, really neat.

20
00:01:38,160 --> 00:01:40,080
And again, I’m not getting paid by them.

21
00:01:40,080 --> 00:01:42,840
So, here is just some links.

22
00:01:42,840 --> 00:01:47,840
I will disseminate this Powerpoint presentation and also the code that I am going to show you,

23
00:01:47,840 --> 00:01:50,480
in my Git repo which you can all access.

24
00:01:50,840 --> 00:01:52,120
I’ll get to that a little bit later.

25
00:01:52,120 --> 00:01:56,360
But basically, so aXe is core and there’s a link to their repo.

26
00:01:56,360 --> 00:02:01,300
And then they also have a very very extensive amount of API documentation.

27
00:02:01,540 --> 00:02:06,160
So if your developers are hooking it into various testing tools, they can look at it and other stuff.

28
00:02:06,520 --> 00:02:12,400
And then they also, what’s cool is, because it’s open source, they have a lot of other people building stuff

29
00:02:12,400 --> 00:02:19,380
on top of their core and that’s one of the things I’m actually going to show you. So one of the other projects.

30
00:02:20,100 --> 00:02:25,360
Before I get into the cool automation stuff, I’m going to show you the Chrome Developer Tools extension,

31
00:02:25,660 --> 00:02:33,040
which is very similar to the Chrome one. So I decided to do a little audit of the meetup.com site.

32
00:02:33,920 --> 00:02:37,600
And basically you push a little button, which I’ll show you on this screen,

33
00:02:37,840 --> 00:02:40,940
and it comes up with a whole list of error and so forth.

34
00:02:40,940 --> 00:02:48,460
So, what’s neat about this is not only does it show you the errors but it shows you the code that is erring out,

35
00:02:48,460 --> 00:02:53,240
it also shows you which compliance levels you may not be passing, so that’s in the top right hand corner.

36
00:02:53,440 --> 00:02:55,160
And then if you hit the inspect button,

37
00:02:55,160 --> 00:03:00,460
it will actually show you in the DOM which particular element isn’t passing.

38
00:03:00,740 --> 00:03:04,900
And then the one thing I actually really like, it links to the spec.

39
00:03:05,520 --> 00:03:11,080
So if you click more info, you can actually go to W3C right away and you can actually reference

40
00:03:11,240 --> 00:03:18,200
if you are or are not passing and so forth. I will caveat that they are continuously building this tool,

41
00:03:18,200 --> 00:03:24,520
so there are false positives and things like that. It is after the page renders when you use the Chrome tool,

42
00:03:24,760 --> 00:03:30,780
so if you basically, whatever you see on the page, and you hit analyze, is what gets rendered,

43
00:03:30,780 --> 00:03:36,380
so if there’s Ajax or anything like dynamic, it won’t analyze that stuff. It’s only whats in the DOM

44
00:03:36,380 --> 00:03:42,760
in that very moment in time. One of their bugs, which is a little silly, when you use it,

45
00:03:42,760 --> 00:03:46,820
it usually scrolls to the bottom of the page, because it wants to analyze the entire DOM.

46
00:03:46,820 --> 00:03:50,260
So one thing you’ll do is you’ll have to just scroll back up to actually see everything.

47
00:03:50,880 --> 00:03:52,000
But this kind of cool, right.

48
00:03:52,000 --> 00:04:00,960
So it tells you like, HTML basics too, right? Like, it’s not just accessibility, it’s, ID attribute values must be unique.

49
00:04:01,520 --> 00:04:08,140
That’s something that is HTML validation. But it affects accessibility because if you have more than one ID

50
00:04:08,140 --> 00:04:14,000
in your DOM that’s the same one, a screen reader won’t know what to reference, or it might repeat it again,

51
00:04:14,000 --> 00:04:17,000
or something like Dragon, you know if you’re trying to do something,

52
00:04:17,000 --> 00:04:19,840
it might actually not know which one if there are two of them.

53
00:04:19,840 --> 00:04:26,300
So, it’s not just an accessibility tool, it’s  also a basic, fundamental HTML auditing tool.

54
00:04:26,700 --> 00:04:36,820
So this is the Chrome plug-in, I will break out of here really quickly in the live.

55
00:04:37,020 --> 00:04:42,300
… let’s see if I can do this while looking over my shoulder … so if I inspect, I built a little mockup here

56
00:04:42,300 --> 00:04:48,200
which I’ll show you, and I hit aXe, and I hit analyze, it shows me that I have errors.

57
00:04:48,200 --> 00:04:52,940
It scrolled down like I mentioned before, I scroll back up and I can click on something like this and it will say

58
00:04:52,940 --> 00:04:58,680
here’s is my HTML, the home link, which is this guy, it doesn’t have enough color contrast,

59
00:04:58,680 --> 00:05:00,280
we heard that a couple of times, right?

60
00:05:01,240 --> 00:05:06,040
And then you can inspect it and what it will do it will actually show you in the DOM,

61
00:05:06,340 --> 00:05:10,600
this is where probably the Chrome tool could actually help out too, because you could run in Chrome

62
00:05:10,920 --> 00:05:12,920
and do some different examples and things like that.

63
00:05:13,280 --> 00:05:17,580
I didn’t know that it actually showed you different suggestions of changes, which is kind of cool.

64
00:05:18,060 --> 00:05:24,920
So that’s aXe. The one thing that is kind of annoying for me is like,

65
00:05:24,920 --> 00:05:30,780
I have to do this outside of my banging on the keyboard while I’m writing code, right?

66
00:05:31,200 --> 00:05:36,200
I have to go into the browser, I have to be on the page that I want to do, and I have to hit analyze

67
00:05:36,200 --> 00:05:41,260
and I have to review it and I have to make changes. So what aXe did is they built this plug-in,

68
00:05:41,260 --> 00:05:46,340
but if you build it into your testing software, it does it automatically.

69
00:05:46,860 --> 00:05:53,420
So let’s get out of here, unless someone wants to see another page being analyzed? I’ll just in to the cool stuff.

70
00:05:56,780 --> 00:05:58,740
So, let’s automate.

71
00:05:59,100 --> 00:06:02,740
So, I’m going to explain a little bit about

72
00:06:02,740 --> 00:06:06,300
how many developers are there in the room? Just so I have a frame of reference.

73
00:06:06,300 --> 00:06:07,480
Ok, so about half.

74
00:06:07,780 --> 00:06:14,560
Ok, does anybody use pre-compilers like Gulp, Grunt, you know, SASS, anything like that?

75
00:06:14,560 --> 00:06:15,160
LESS?

76
00:06:16,080 --> 00:06:19,920
Ok, so most of you will know exactly what I am talking about.

77
00:06:19,920 --> 00:06:22,520
The other people, I’ve kind of outlined it here a little bit.

78
00:06:22,720 --> 00:06:27,660
So Gulp is a JavaScript framework that allows you to compile and automate

79
00:06:27,660 --> 00:06:33,480
some of your development cycles. So like with CSS, which is a compiled code, there’s frameworks like LESS

80
00:06:33,480 --> 00:06:38,840
and SASS that are un-compiled, that will allow you to do a lot more flexibility and things like that.

81
00:06:38,840 --> 00:06:44,880
And Gulp is running all the time and doing a lot of magic as your actually banging on the keyboard.

82
00:06:45,180 --> 00:06:52,060
So I have Gulp as my primary compiler. Grunt is the other popular one. I think there’s a couple more.

83
00:06:52,060 --> 00:06:54,160
But Gulp is top notch, I like it.

84
00:06:54,520 --> 00:07:02,240
SASS. So, I’m using SASS as my CSS precompiled language, which allows me to do things like

85
00:07:02,240 --> 00:07:09,340
variables and mixins. So when you’re talking about color palettes and keeping things in check,

86
00:07:09,620 --> 00:07:15,800
you can right a variable called blue and every piece of CSS that’s referencing blue,

87
00:07:15,800 --> 00:07:18,200
you can change it to a different color if you wanted,

88
00:07:18,200 --> 00:07:23,020
without going back to all your CSS files and stuff like that. So it really kind of helps.

89
00:07:23,240 --> 00:07:29,160
Webpack is a JavaScript and debundler. So this is where we’re doing a lot of enterprise,

90
00:07:29,160 --> 00:07:36,480
big big big JavaScript structures. So we’re using Webpack to basically take a whole lot of

91
00:07:36,480 --> 00:07:42,220
JavaScript partials … so imagine like a CMS library, where you’ll have a component for a hero,

92
00:07:42,220 --> 00:07:49,760
and component for a carousel and a component for let’s say a modal, it bundles all of that code into one,

93
00:07:50,060 --> 00:07:52,820
but it does’t access the code unless you need it.

94
00:07:52,820 --> 00:08:01,100
So it’s one file to get cached, which is great for performance, but it’s really very powerful.

95
00:08:01,500 --> 00:08:06,600
If you’ve never used the next one, you need to do it. Browsersync, and I’ll demonstrate this.

96
00:08:06,600 --> 00:08:13,620
So Browsersync is a plug-in that runs in Gulp or Grunt, and what it does is it allows you to have as many

97
00:08:13,620 --> 00:08:19,420
Browsers open as you want, in as many locations as you want, and as you are coding,

98
00:08:19,420 --> 00:08:22,300
all of the browsers are refreshing while your actually coding.

99
00:08:22,620 --> 00:08:27,020
So one of the cool things is like I can have my iPhone simulator on the screen

100
00:08:27,240 --> 00:08:33,160
and my Windows IE and ... well I can't have that ... and my Chrome and my Firefox all at once

101
00:08:33,160 --> 00:08:37,680
and the minute I hit Save in my HTML editor, all of my browsers will refresh.

102
00:08:38,160 --> 00:08:42,260
So it let's me to actually see what's going on in various states and all of that kind of stuff.

103
00:08:42,500 --> 00:08:49,400
In addition, that if you have Browsersync running on an IP address that can be accessed from another computer,

104
00:08:49,400 --> 00:08:55,200
that other person looking at it will also see those changes. It's really really very powerful, very cool.

105
00:08:56,260 --> 00:09:00,620
So, the key to this automation is gulp-axe-webdriver.

106
00:09:00,620 --> 00:09:03,040
So I didn't write it. I found the plugin.

107
00:09:03,040 --> 00:09:05,920
Basically it is the gentleman that wrote

108
00:09:06,520 --> 00:09:12,260
a Gulp PhantomJS wrapper around aXe core.

109
00:09:12,260 --> 00:09:14,860
So what it does is, basically you run it,

110
00:09:15,140 --> 00:09:17,420
and it creates a PhantomJS, which is basically

111
00:09:17,420 --> 00:09:19,920
a visualess or headless browser.

112
00:09:20,480 --> 00:09:22,100
So it doesn't actually exist,

113
00:09:22,480 --> 00:09:24,680
but it actually acts as a real browser

114
00:09:24,900 --> 00:09:25,680
to do the tests.

115
00:09:25,680 --> 00:09:29,340
So just like I hit analyze in the Chrome Extension Tool,

116
00:09:29,580 --> 00:09:31,040
it essentially does the same thing

117
00:09:31,040 --> 00:09:32,520
and you just don't see what's happening.

118
00:09:32,880 --> 00:09:34,820
So it is behind the scenes.

119
00:09:35,040 --> 00:09:39,160
Ok, so here's just a kind of example of my Gulp build.

120
00:09:39,340 --> 00:09:42,240
So, I build the stylesheets, I build the HTML,

121
00:09:42,240 --> 00:09:47,280
I do a little cleaning, I do some linting, which is analyzing if my JavaScript is actually accurate.

122
00:09:47,280 --> 00:09:49,280
I don't know why it does that. But I'll switch back.

123
00:09:52,020 --> 00:09:55,180
I build all my JavaScript, I watch my environment,

124
00:09:55,180 --> 00:10:00,140
which is that Browsersync. I clean a little bit more JavaScript, it shows me what my environment is,

125
00:10:00,400 --> 00:10:02,520
and it does a little bit other stuff, and so forth.

126
00:10:03,260 --> 00:10:05,820
Then, I'm going to show you this in a live demonstration,

127
00:10:05,820 --> 00:10:12,240
but basically while I'm coding, if I have this window visible, you'll see that the minute I hit save,

128
00:10:12,240 --> 00:10:16,900
it says Hello, ok, I'm going to test the URL, it's found three accessibility violations,

129
00:10:17,060 --> 00:10:23,060
and it shows me the traversing of the object in the DOM, which is body, nav, row, column, blah blah blah,

130
00:10:23,060 --> 00:10:27,820
and it tells me that this element has a color contrast of 3.0, which we learned is too low.

131
00:10:28,560 --> 00:10:34,860
So this is actually being displayed to me live while I'm coding. I never actually have to look at my browser.

132
00:10:35,580 --> 00:10:39,640
So if you don't have two screens, or if you don't like looking at your other screen,

133
00:10:39,640 --> 00:10:44,080
you can actually just look at this while you're coding and it will show you all these errors and so forth.

134
00:10:45,980 --> 00:10:47,980
Cool right? Get it? Ok...

135
00:10:47,980 --> 00:10:53,500
So, let me sit down. Let me do some coding.

136
00:10:53,500 --> 00:10:56,500
I'm going to switch views so I can actually see this.

137
00:10:57,560 --> 00:10:59,560
I want to show you how this all works.

138
00:11:01,920 --> 00:11:07,060
Ok, so I built a really bad dummy HTML page for this.

139
00:11:07,320 --> 00:11:09,560
[Dennis]: Don't you find that to be hard to do?

140
00:11:09,560 --> 00:11:10,080
[Seth]: What?

141
00:11:10,660 --> 00:11:14,260
[Dennis]: To build a ... bad HTML page?

142
00:11:14,840 --> 00:11:20,500
[Seth]: It was easy by installing the Foundation Zurb framework, which is like Bootstrap.

143
00:11:20,500 --> 00:11:21,140
[Laughter]

144
00:11:21,140 --> 00:11:23,500
[Seth]: Ok, so I love Foundation, don't get me wrong.

145
00:11:24,100 --> 00:11:26,880
But, fundamentally, there's a whole lot going on that's wrong.

146
00:11:27,240 --> 00:11:30,880
But let me first stop my environment here quickly.

147
00:11:30,880 --> 00:11:33,460
So, I'll just clear it so you see what happens.

148
00:11:35,200 --> 00:11:38,800
So I basically, I have in my folder structure here

149
00:11:38,800 --> 00:11:40,800
I'll just quickly show you, if I can find it.

150
00:11:41,560 --> 00:11:43,400
When I'm talking about technically...

151
00:11:44,320 --> 00:11:47,300
And all of this is available for you to download.

152
00:11:47,300 --> 00:11:51,160
So I basically have, you know, my Gulp file, I'm using ES6

153
00:11:51,440 --> 00:11:53,620
all my Node modules, here's my source,

154
00:11:53,920 --> 00:11:58,360
and basically, this is essentially what becomes my web server. Ok, so enough about that. We don't care.

155
00:11:59,740 --> 00:12:05,820
But, when I run Gulp, and a special command that I give it, you'll see that it's now starting to

156
00:12:06,260 --> 00:12:11,420
do its magic, right. And hopefully it runs, right. Ok, good.

157
00:12:11,420 --> 00:12:16,300
And you'll see that automatically my browser opened up and refreshed. Like I didn't even have to do that.

158
00:12:16,480 --> 00:12:20,780
It magically did that. And if you noticed in the top right hand corner, which you'll see in a little bit,

159
00:12:21,020 --> 00:12:24,200
it said Browsersync and so forth and you'll see what I am talking about.

160
00:12:24,680 --> 00:12:27,120
So right now, this is more or less how I develop.

161
00:12:27,120 --> 00:12:33,200
I have the log, or the Gulp log on the left and I haver my browser on a different screen.

162
00:12:34,100 --> 00:12:36,940
But I'll pull this up. So this is my codebase.

163
00:12:37,220 --> 00:12:43,020
And it didn't test it on load because I would assume that I'm just going to like make a little change here.

164
00:12:43,020 --> 00:12:45,920
So I'm just going to delete one line and hit Save.

165
00:12:46,140 --> 00:12:48,620
And you'll see that over here, it did

166
00:12:50,280 --> 00:12:53,320
a localhost, so that's my web server,

167
00:12:53,320 --> 00:12:57,200
and here are all the errors, and I'm going to bang these out really really quickly.

168
00:12:57,200 --> 00:13:01,420
So a lot of them are color contrast, because of Foundation (again).

169
00:13:01,880 --> 00:13:06,360
And then there's a couple down here like, this image doesn't have an alt tag

170
00:13:06,360 --> 00:13:10,760
or an alternative text model. Because you don't have to use an alt tag,

171
00:13:10,960 --> 00:13:13,480
you could use ARIA, which you wouldn't, but you could.

172
00:13:13,740 --> 00:13:15,740
Ok, so it actually would reference that.

173
00:13:15,920 --> 00:13:18,380
And then I also have a little tiny form field in here

174
00:13:18,380 --> 00:13:19,700
that has no labels, right.

175
00:13:20,020 --> 00:13:24,340
So, right off the bat, I show you the page again so you can see it here

176
00:13:25,700 --> 00:13:28,020
over here just so you can see it refresh

177
00:13:28,440 --> 00:13:29,080
when I make a change.

178
00:13:29,080 --> 00:13:35,380
So I'm going to go into my SASS and I'm going to get rid of all of the Foundation stuff really quickly.

179
00:13:36,560 --> 00:13:41,900
So once I do this, I comment it out, I hit Save, you'll see immediately in my browser,

180
00:13:42,400 --> 00:13:49,320
refreshed, right? Ok, and if I move this over a little bit, you'll see that I have

181
00:13:50,180 --> 00:13:52,060
no more color contrast errors.

182
00:13:52,060 --> 00:13:53,160
So that's cool.

183
00:13:53,160 --> 00:13:57,480
So if I had a little bit more space, you could see this all in real time, right?

184
00:13:57,780 --> 00:14:01,720
So, while it doesn't look pretty, I'm not going to go redesign it, I just wanted to show you that

185
00:14:01,920 --> 00:14:02,920
you can do this.

186
00:14:03,220 --> 00:14:06,460
So now let's get rid of that image error.

187
00:14:06,460 --> 00:14:12,400
So I go look at my HTML file and I threw in an image in here some where.

188
00:14:15,900 --> 00:14:17,160
... do it the old fashioned way.

189
00:14:17,160 --> 00:14:20,560
So, here I took a picture of bacon, oh it's my logo, right?

190
00:14:20,940 --> 00:14:30,280
Ok, but even though that logo doesn't need an alt attribute to it, it still needs the actual attribute of null.

191
00:14:30,280 --> 00:14:34,380
We just learned that. So if I add alt equals blank,

192
00:14:35,660 --> 00:14:40,340
and you'll see, it just finished, and now I have one error left. Ok, fantastic, I'm working.

193
00:14:41,160 --> 00:14:45,300
Well, in the gaming, like you could do an audit afterwards

194
00:14:45,640 --> 00:14:49,860
think of if everyone one of your developers had a tool like this going at the same time

195
00:14:50,260 --> 00:14:55,920
you would reduce your HTML errors, you would reduce your accessibility errors like really fast

196
00:14:55,920 --> 00:14:57,760
because it's in your face.

197
00:14:57,760 --> 00:15:02,380
Now just to kind of give you the opposite end of the spectrum here, let's assume that I had ...

198
00:15:02,380 --> 00:15:04,380
well let's get rid of the accessibility errors first.

199
00:15:05,520 --> 00:15:10,860
So we come down to my little form down here, I think, I have a form, somewhere,  where is it ...

200
00:15:14,820 --> 00:15:16,820
... I put a lot of stuff in here ...

201
00:15:18,820 --> 00:15:20,180
Ok, so here's my form, right?

202
00:15:20,500 --> 00:15:22,980
So I'm going to add a label, because we need to have a label.

203
00:15:23,360 --> 00:15:26,680
So you could do it like this ... you know, input, right

204
00:15:27,460 --> 00:15:31,580
and then I'm going to wrap my label around here, because that's how I like doing it,

205
00:15:32,440 --> 00:15:33,260
I hit Save

206
00:15:33,900 --> 00:15:38,460
and, I have no accessibility violations, according to this page.

207
00:15:40,480 --> 00:15:44,620
Now, before I go on any further, I'm going to show you something really really cool ...

208
00:15:45,980 --> 00:15:54,020
So I built a configuration file for this, for aXe, and Gulp, ok?

209
00:15:54,460 --> 00:15:58,580
So what I've done, I've said here is my dev environment, which is traditionally what you do

210
00:15:58,840 --> 00:16:03,600
with Gulp, here's my, where my web server environment is, that's nothing unique.

211
00:16:04,360 --> 00:16:08,200
But what I did do, I created my own accessibility rules.

212
00:16:08,520 --> 00:16:10,920
All of these attributes in this object,

213
00:16:11,640 --> 00:16:13,380
are part of the aXe plugin.

214
00:16:13,640 --> 00:16:19,020
So for instance, like I built enable, or to disable, so if it was actually annoying me,

215
00:16:19,440 --> 00:16:25,200
that I was doing a lot of maybe pre-coding and all of these errors are flipping out at me,

216
00:16:25,500 --> 00:16:31,380
like I might turn it off, which I'll show you here, so if I undo all the good stuff I just did,

217
00:16:33,080 --> 00:16:36,200
you'll notice it doesn't actually audit my code, right?

218
00:16:36,460 --> 00:16:42,120
So you may want to turn that on, or maybe a gatekeeper, like a lead or a manager will turn that on or off

219
00:16:42,120 --> 00:16:45,460
depending upon the developer or what the point they are in stage

220
00:16:45,460 --> 00:16:48,380
so I added that ability in my Gulp file.

221
00:16:48,900 --> 00:16:54,500
Let me turn it back on, because I want to show you something, ok ... and then I

222
00:16:54,960 --> 00:16:58,720
Unfortunately you have to stop and start Gulp every time you make a change to the configuration.

223
00:17:01,300 --> 00:17:08,400
But one cool thing is that the aXe program and the web driver that this guy built,

224
00:17:09,220 --> 00:17:16,300
you're allowed to post in as many files or URLs as you want to be audited.

225
00:17:16,980 --> 00:17:21,620
So in my case, I'm building the site using partial HTML files.

226
00:17:21,840 --> 00:17:26,480
And one of the accessibility criterias is that everything audited needs to have an HTML tag

227
00:17:26,480 --> 00:17:29,060
and a body and a head and all of that kind of stuff.

228
00:17:29,440 --> 00:17:32,240
Well, if Im auditing individual files, which is just chunks,

229
00:17:34,280 --> 00:17:40,380
so instead of doing like auditing something like index.html,

230
00:17:40,900 --> 00:17:42,600
I actually pass in a URL.

231
00:17:43,760 --> 00:17:48,840
Now, you're saying "well what happens if I wanted to do a different page or more than one page?"

232
00:17:49,180 --> 00:17:52,400
They built it so you can just pass in as many URLs as you want.

233
00:17:52,720 --> 00:17:56,580
So I can add as many supplemental URLs as I wanted,

234
00:17:56,580 --> 00:18:01,800
and all of those will be test every time you make a change, regardless of what page that you are on.

235
00:18:02,080 --> 00:18:07,160
So if you were building a component in a CMS, that was on, say, five different pages,

236
00:18:07,760 --> 00:18:11,880
but maybe they had different treatments, or they had different styles or something like that,

237
00:18:12,080 --> 00:18:15,860
it will scan those, just like if you were to open five browsers

238
00:18:15,860 --> 00:18:19,940
and do it in Chrome or in the aXe developer tool.

239
00:18:20,140 --> 00:18:22,060
So, it's super super powerful.

240
00:18:22,360 --> 00:18:25,480
The other thing that it does, just natively, I didn't do any of this,

241
00:18:25,920 --> 00:18:29,860
you are allowed to include or exclude selectors.

242
00:18:30,100 --> 00:18:33,540
So I could do something like exclude the nav ...

243
00:18:34,760 --> 00:18:37,440
or include the nav, so I only want to scan the nav,

244
00:18:37,440 --> 00:18:39,580
because I'm working on it. Everything else is junk.

245
00:18:40,100 --> 00:18:41,600
Or visa versa.

246
00:18:42,180 --> 00:18:44,580
So you can pass in and out of these parameters.

247
00:18:44,840 --> 00:18:47,440
And in the documentation of the API by aXe,

248
00:18:47,780 --> 00:18:50,160
there are all of these special conditions and things like that.

249
00:18:50,380 --> 00:18:56,540
One of the things that the Phantomjs plugin doesn't do yet but aXe does is,

250
00:18:56,540 --> 00:18:59,780
you can tell it what priority level you want to check against.

251
00:18:59,900 --> 00:19:02,980
So, you could say like, I only want to check against Section 508.

252
00:19:02,980 --> 00:19:07,380
Or I only want to check against WCAG 2.0 level 2.

253
00:19:07,760 --> 00:19:11,020
Like you get to pick those things, and you can pass those things in as parameters.

254
00:19:11,240 --> 00:19:19,660
So it's really really really powerful and imagine like basically doing your site and instead of, you know,

255
00:19:21,740 --> 00:19:26,000
you can make changes, and now it should tell me look at all of these errors that I've got,

256
00:19:26,220 --> 00:19:28,320
and part of the job is to whittle them down.

257
00:19:28,700 --> 00:19:32,980
So, this automation is great for developers,

258
00:19:33,260 --> 00:19:40,020
but it can also be amazing for QA people, because they could pass in a whole site.

259
00:19:40,300 --> 00:19:44,640
15 thousand URLs essentially, and it can test out all of those.

260
00:19:44,840 --> 00:19:48,280
And you could have a log actually printed and all of that kind of stuff.

261
00:19:48,280 --> 00:19:51,020
So, there's a real real lot of powerful things.

262
00:19:51,600 --> 00:19:54,620
Since I mentioned it, I'm just going to show it to you here.

263
00:19:54,840 --> 00:19:57,280
So here's my web page again, I just wanted to just show you

264
00:19:57,920 --> 00:19:59,920
how this works with Browsersync ...

265
00:20:00,300 --> 00:20:01,340
so let me open up

266
00:20:02,460 --> 00:20:06,520
my iOS here ... I didn't plan to do this, but I'll do it anyway

267
00:20:06,700 --> 00:20:08,300
So here's my iOS simulator

268
00:20:08,780 --> 00:20:11,420
And if I open up this page,

269
00:20:11,560 --> 00:20:15,940
One of the cool things I did here, I put in this accordion, but it doesn't work until I click this bacon.

270
00:20:16,380 --> 00:20:19,320
See how I'm scrolling up and down and the actual page moves?

271
00:20:19,620 --> 00:20:26,540
And then if I click Select Bacon, which, I probably have a JavaScript, you'll see that turn light gray here,

272
00:20:26,940 --> 00:20:30,400
and if I click, I might have an error, but

273
00:20:30,620 --> 00:20:34,080
essentially, this is really neat, because now if I come over here and do it,

274
00:20:35,040 --> 00:20:38,520
I can actually do it, visa versa.

275
00:20:39,520 --> 00:20:46,660
Very powerful too. So between using Browsersync and Gulp and aXe plugin,

276
00:20:47,320 --> 00:20:52,700
all of my, let's call it first draft QA-ing, is being done while I'm coding.

277
00:20:53,380 --> 00:21:00,960
And Gulp also allows you to do things like JavaScript checking, so if you're a JavaScript developer,

278
00:21:00,960 --> 00:21:06,180
if I open up a JavaScript file here and I ... let's just change this guy,

279
00:21:06,440 --> 00:21:11,340
and let's say, I'm sure you've seen this a thousand times, someone leaves off a semicolon, right?

280
00:21:11,540 --> 00:21:14,140
Ok, well it says here, I've got an error.

281
00:21:14,320 --> 00:21:18,140
So there's all of these powerful tools that you can build into your compiler

282
00:21:18,300 --> 00:21:20,300
in addition to accessibility tools.

283
00:21:20,300 --> 00:21:28,400
And, I'm doing this on the fly, rather than going and actually using the same exact tool

284
00:21:29,960 --> 00:21:34,000
by inspecting and then by analyzing and then doing that.

285
00:21:34,000 --> 00:21:39,140
So, really really, exponentially helps the development process.

286
00:21:39,860 --> 00:21:44,720
And on that note ... I will say ... Questions.

287
00:21:44,720 --> 00:21:46,300
[Laughter]

288
00:21:46,300 --> 00:21:52,200
[Applause]

