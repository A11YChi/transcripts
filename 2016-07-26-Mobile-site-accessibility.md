# Mobile site accessibility: the good, the bad and the ugly
## Gian Wild - Tuesday, July 26, 2016
[Source recording](https://www.youtube.com/watch?v=VTuioz4fzv4)

**[Dennis]** Our speaker is Gian Wild, I'm going to read from here, because I spent a good half hour researching and writing this, so... Gian Wild is an accessibility industry veteran, having started back in 1998. She spent six years with the W3C Web Content Accessibility Guidelines (WCAG) Working Group and other associated groups, contributing to the development of WCAG 2. Gian speaks at web and accessibility conferences throughout the world. Additionally, she has spoken at the United Nations on the importance of accessibility. She is presently CEO of AccessibilityOz based in Australia. Please give a warm Chicago welcome to Gian Wild.

**[Applause]**

11
00:01:02,360 --> 00:01:03,480
[Gian] Well thank you for having me.

12
00:01:03,480 --> 00:01:07,820
I'm very loud, can everyone hear me in the back?
Well, let me know if you can't hear me.

13
00:01:07,840 --> 00:01:16,020
We actually incorporated in the U.S. a year ago, a year and nine days ago,

14
00:01:16,040 --> 00:01:18,460
so we're actually a U.S. company as well.

15
00:01:18,480 --> 00:01:26,420
And, after that introduction I feel there's nothing left that I can actually do.

16
00:01:26,440 --> 00:01:34,680
But I have some great clients here in the U.S. and I'm really glad to be here in Chicago.

17
00:01:34,680 --> 00:01:37,160
And thanks to Dennis for organizing this.

18
00:01:37,360 --> 00:01:48,140
So if you want to have access to tonight's presentation, you can go to a11yoz.com/2016mobile

19
00:01:48,160 --> 00:01:56,400
and that has the presentation, you can actually look at it while I'm presenting if you want and take notes.

20
00:01:56,400 --> 00:02:00,500
Now unfortunately the system that I am using is not accessible to screen readers,

21
00:02:00,520 --> 00:02:05,280
but if you'd like a copy of this presentation, an accessible PowerPoint presentation

22
00:02:05,520 --> 00:02:10,680
just tweet me at @AccessibilityOz or come up and you can see me afterwards

23
00:02:10,680 --> 00:02:13,860
and I'll send you the accessible PowerPoint.

24
00:02:14,480 --> 00:02:22,900
That address again is a11yoz.com/2016mobile.

25
00:02:24,200 --> 00:02:30,300
This is my team in Australia about a year ago. We've probably doubled in size.

26
00:02:30,320 --> 00:02:36,400
When I started AccessibilityOz in 2011, I had a mission statement which was

27
00:02:36,400 --> 00:02:43,160
to make the world a more accessible place and also to actively hire people with disabilities.

28
00:02:43,160 --> 00:02:50,320
And I wanted to target a percentage of my staff to have, twenty percent of my staff to have disabilities.

29
00:02:50,320 --> 00:02:58,000
So at the moment we're actually at eighty percent. So we actively hire people with disabilities.

30
00:02:58,000 --> 00:03:03,300
We have two candidates and they have the same experiences, we hire the person with a disability.

31
00:03:03,320 --> 00:03:08,900
In some cases where we have a person without the adequate experience

32
00:03:08,920 --> 00:03:11,220
but they have a disability, we hire them anyway,

33
00:03:11,240 --> 00:03:18,120
We do really want to do what we preach.

34
00:03:19,720 --> 00:03:21,780
It's also something that we do with our products.

35
00:03:21,800 --> 00:03:25,680
We have three products; OzART, OzWiki and OzPlayer,

36
00:03:25,680 --> 00:03:30,660
and they're all fully accessible. We don't release anything unless it's fully accessible.

37
00:03:31,760 --> 00:03:37,520
So in terms of my staff, we've got people who use speech-to-text programs, on screen magnifiers,

38
00:03:37,560 --> 00:03:45,160
keyboard-only screen readers, we've got people who have Epilepsy, I get migraines,

39
00:03:45,160 --> 00:03:49,320
both of those can be triggered by flickering content on websites.

40
00:03:49,840 --> 00:03:52,760
And people with Fibromyalgia and Dyslexia,

41
00:03:52,760 --> 00:03:56,040
so we've got a whole range of different groups of people with disabilities.

42
00:03:57,360 --> 00:04:01,760
So the reason why I'm telling you all that is it's not just about vision impairments.

43
00:04:01,920 --> 00:04:05,800
A lot of people think that web accessibility is about vision impairments.

44
00:04:05,800 --> 00:04:10,920
They specifically say, IE8 and JAWs, and it's actually a lot bigger than that.

45
00:04:11,040 --> 00:04:16,820
So just because your site is screen reader accessible doesn't mean it's necessarily fully accessible.

46
00:04:17,760 --> 00:04:20,780
I terms of our services, we do everything.

47
00:04:21,320 --> 00:04:26,600
That's web accessibility or digital accessibility, and as I've said, we've got three products

48
00:04:26,840 --> 00:04:30,360
we were a reseller for BrowserAloud, I don't know why that is still there.

49
00:04:30,360 --> 00:04:36,080
OzPlayer, which is the fully accessible video player, which has just been purchased by Triple C Tech Center

50
00:04:36,160 --> 00:04:39,500
so all California community colleges now have
and use OzPlayer.

51
00:04:40,080 --> 00:04:44,440
OzART, our automated testing tool and OzWiki,

52
00:04:44,440 --> 00:04:48,360
our database of accessibility errors, screen shots, code and solutions.

53
00:04:48,800 --> 00:04:52,700
And if you want to give me your email address at the end of the session,

54
00:04:52,720 --> 00:04:55,400
I can actually give you one month's access to OzWiki.

55
00:04:55,400 --> 00:05:01,080
We've got over a thousand examples. A lot of the examples you'll see here today come from OzWiki.

56
00:05:02,080 --> 00:05:03,640
In terms of mobile ...

57
00:05:04,080 --> 00:05:09,020
there are a bunch of different accessibility features that people rely on when it comes to mobile.

58
00:05:09,320 --> 00:05:14,440
There are native screen readers like TalkBack on Android, Narrator on Windows,

59
00:05:14,440 --> 00:05:17,400
for those three people using Windows phones.

60
00:05:17,400 --> 00:05:18,820
[Laughter]

61
00:05:18,840 --> 00:05:20,600
[Gian Wild] VoiceOver of iOS.

62
00:05:20,600 --> 00:05:24,520
There's text-to-speech speech recognition, volume control,

63
00:05:24,520 --> 00:05:27,760
visual, auditory and vibrational notifications,

64
00:05:28,040 --> 00:05:31,900
haptic keyboard which vibrates when you change things, and zoom.

65
00:05:31,920 --> 00:05:35,600
So there's a whole range of different things
that people can do

66
00:05:35,600 --> 00:05:38,440
to make their web site more accessible 
on a mobile device.

67
00:05:39,920 --> 00:05:45,040
The system accessibility settings are things like font size, touch and hold delay,

68
00:05:45,040 --> 00:05:49,720
screen rotation, high contrast, assistive touch and mono audio.

69
00:05:50,280 --> 00:05:54,580
One of the best things you can do to test your mobile app or mobile site

70
00:05:54,600 --> 00:05:57,520
is to pinch zoom and see if you can use the site.

71
00:05:57,520 --> 00:06:01,700
The other thing is to turn auto landscape mode and see whether you can use it.

72
00:06:01,720 --> 00:06:06,240
You'd be surprised the number of apps that crash as soon as you move into landscape mode.

73
00:06:08,040 --> 00:06:13,500
Now, when it comes to web accessibility, everyone knows about the Web Content Accessibility Guidelines.

74
00:06:13,880 --> 00:06:19,040
But they don't specifically cover mobile sites.

75
00:06:19,040 --> 00:06:25,480
So, for example, WCAG 2 requires that everything be keyboard accessible.

76
00:06:25,480 --> 00:06:28,120
But it doesn't require that everything be 
mouse accessible.

77
00:06:28,640 --> 00:06:31,140
And it doesn't require that everything be touch accessible.

78
00:06:31,360 --> 00:06:35,920
So you could have a site that meets WCAG 2, but actually can't be used on a mobile device.

79
00:06:35,920 --> 00:06:40,920
So, the working group is addressing this at the moment,

80
00:06:40,920 --> 00:06:44,000
and they're talking about releasing a WCAG 2.1.

81
00:06:44,000 --> 00:06:47,460
It might be released in 2018.

82
00:06:47,480 --> 00:06:51,960
So obviously, we still need to build web sites and web apps between now and then.

83
00:06:51,960 --> 00:06:55,840
So we've come up with our own mobile methodology

84
00:06:55,840 --> 00:07:02,200
It's based on WCAG 2. It's also based on the BBC Mobile Accessibility Guidelines

85
00:07:02,200 --> 00:07:04,960
which are an absolutely excellent resource.

86
00:07:05,240 --> 00:07:08,780
Just be aware that the BBC wrote it for internal use

87
00:07:08,800 --> 00:07:14,920
and the BBC is obviously not a for-profit system, there's not stuff on ecommerce and things like that.

88
00:07:16,400 --> 00:07:18,400
So let's talk about Mobile usage.

89
00:07:18,600 --> 00:07:25,700
In 2014, people started spending more time on their mobile devices than than on desktops.

90
00:07:26,080 --> 00:07:30,080
So mobile is everywhere.

91
00:07:30,800 --> 00:07:38,260
WebAim does this great screen reader survey every year. And it peaked in January 2014

92
00:07:38,280 --> 00:07:43,940
the 82% of people who use screen readers, also use the screen readers on their mobile devices.

93
00:07:43,960 --> 00:07:49,740
It's gone down a little, but that's because they widened the number of people

94
00:07:49,760 --> 00:07:51,760
that accessed that particular survey.

95
00:07:51,840 --> 00:07:58,280
So, someone who is vision impaired, don't assume that they're just going to access your website on a desktop.

96
00:07:58,280 --> 00:08:05,820
In fact, we work with the National Federation of the Blind and they said to us,

97
00:08:05,840 --> 00:08:09,420
often we actually look at websites only on mobile.

98
00:08:09,440 --> 00:08:13,720
Because we don't need a big computer, we don't need a big screen, we can't see it.

99
00:08:13,720 --> 00:08:18,960
So we just plug in our little headphones into our mobile, and then when we get a mobile only site,

100
00:08:18,960 --> 00:08:24,780
and no way to drop that to a desktop site, we don't know whether we've seen stuff that might be on the desktop.

101
00:08:26,800 --> 00:08:32,160
So, this is the energy rating site that we worked on a couple years back

102
00:08:32,160 --> 00:08:36,100
and it did not have a responsive site.

103
00:08:36,120 --> 00:08:41,400
It was not friendly on the mobile. It looked exactly the same on the mobile as it did on the desktop,

104
00:08:41,400 --> 00:08:45,140
except much much smaller,
and it was impossible to use.

105
00:08:45,160 --> 00:08:51,600
But even so, nineteen percent of the people who visited that website, used a mobile or tablet to do so.

106
00:08:52,240 --> 00:08:57,960
So, when we redevelop a site and turn it into a responsive site, that jumped to thirty percent.

107
00:08:58,040 --> 00:09:04,800
So, even if the site is terrible terrible to use on a mobile, people are still going to use mobile to access.

108
00:09:06,720 --> 00:09:12,100
Compared to Consumer Affairs Victoria, that have always had a separate m dot site,

109
00:09:12,160 --> 00:09:16,900
and they were at thirty percent in January 2014
and they are still now.

110
00:09:18,320 --> 00:09:20,540
So let's talk about mobile-specific issues.

111
00:09:21,760 --> 00:09:27,400
So PDFs ... are probably one of the biggest problems with mobile cause you open a PDF

112
00:09:27,400 --> 00:09:33,020
and you wait ... and you wait ... and you wait ... and then you get something that looks like that.

113
00:09:33,040 --> 00:09:36,140
Most people who can't see it, it looks terrible.

114
00:09:36,160 --> 00:09:41,800
Its tiny text, it doesn't reflow, color contrast is bad,

115
00:09:41,800 --> 00:09:47,720
it's page two of a hundred and eight. Can you imaging scrolling a hundred and eight pages?

116
00:09:47,720 --> 00:09:55,200
And you can't search, might be an image, it's terrible. PDFs are terrible. I have a whole presentation about it.

117
00:09:56,400 --> 00:10:05,400
This is something like this. HTML. It resizes, you can pinch zoom, color contrast can be changed easily, etc.

118
00:10:06,720 --> 00:10:13,200
And then, even maybe a separate m dot site, so this is a responsive site actually.

119
00:10:13,200 --> 00:10:18,280
so you can see, much easier to use
than your standard PDF.

120
00:10:20,040 --> 00:10:26,580
Remember when it comes to mobile and PDFS, PDFS are much larger file size than HTML.

121
00:10:27,000 --> 00:10:32,200
You have a slow connection on a mobile, and so what that means is it takes longer for your users

122
00:10:32,200 --> 00:10:39,680
to download your content. It also increases their data usage. So, it equals up for customers.

123
00:10:41,560 --> 00:10:46,360
So, you should really consider being really friendly
to mobile,

124
00:10:46,360 --> 00:10:51,080
and so actually having something like a
separate m dot site.

125
00:10:51,160 --> 00:10:54,960
So this is the energy rating site before we looked at it

126
00:10:54,960 --> 00:10:58,760
and then nice big icons, easy to use, etc.

127
00:10:59,400 --> 00:11:03,380
Another example. Energy Rating is kind of like your Energy Star.

128
00:11:05,040 --> 00:11:09,600
Other issues we see are Autoplay.
Autoplay is incredibly inaccessible.

129
00:11:09,600 --> 00:11:14,300
It's one of the biggest accessibility failures of all time.

130
00:11:14,320 --> 00:11:17,800
There are four non-interference causes in WCAG 2

131
00:11:17,800 --> 00:11:21,760
that you absolutely must not fail.

132
00:11:22,040 --> 00:11:22,540
Autoplay is one of them.

133
00:11:22,540 --> 00:11:26,740
So this is actually Jamie Oliver's recipe mobile app.

134
00:11:27,200 --> 00:11:33,460
And when you open it for the first time, it takes you to your native mobile video player,

135
00:11:33,480 --> 00:11:35,480
and automatically plays the video.

136
00:11:35,640 --> 00:11:38,720
It doesn't have any captions, 
it doesn't have any audio descriptions,

137
00:11:39,080 --> 00:11:43,040
It doesn't have any way to easily know where you are or to go back.

138
00:11:43,480 --> 00:11:46,700
So this is a really really serious issue. Don't do this.

139
00:11:47,320 --> 00:11:50,600
The other thing you don't want to do is this movement.

140
00:11:50,640 --> 00:11:54,760
So, slideshows are really annoying on a desktop.

141
00:11:55,480 --> 00:12:00,700
If you're not sure about whether you should use a slideshow, look at shouldiuseacarousel.com.

142
00:12:02,680 --> 00:12:04,980
But its even more annoying on a mobile.

143
00:12:05,240 --> 00:12:11,620
Because, often if people provide pause buttons, they don't on mobile because they have less room.

144
00:12:11,640 --> 00:12:18,600
But on a mobile, it takes up a lot more space, compared to the space you have on a desktop.

145
00:12:18,800 --> 00:12:24,360
So, slideshows are incredibly problematic when it comes to mobile.

146
00:12:24,400 --> 00:12:26,400
So you must have a pause button.

147
00:12:26,400 --> 00:12:30,580
There are a whole bunch of things you need to do if you're going to have slideshows on mobile.

148
00:12:30,600 --> 00:12:33,320
And I do have an article that I have written about that.

149
00:12:33,320 --> 00:12:39,140
We also were commissioned to create
an accessible slideshow

150
00:12:39,160 --> 00:12:43,200
by the Department of Prime Minister and Cabinet in Australia,

151
00:12:43,200 --> 00:12:45,500
and they're released it under Creative Commons.

152
00:12:45,720 --> 00:12:53,860
It's a Drupal module and a WordPress Plugin if you are interested, feel free to contact us.

153
00:12:55,600 --> 00:13:01,360
Other issues are traps, and we see traps a lot more in mobile than we do on desktop.

154
00:13:01,360 --> 00:13:04,660
So, one of the big things is the on-screen keyboard trap,

155
00:13:04,680 --> 00:13:08,740
which is when the keyboard remains visible, no matter what you do.

156
00:13:09,440 --> 00:13:15,720
So, even if you are on a field, you need to have the ability to dismiss the keyboard, because the keyboard takes up

157
00:13:15,760 --> 00:13:18,260
almost half of the real estate of your mobile phone.

158
00:13:18,360 --> 00:13:23,920
So you need to be able to dismiss it, and look around at what you want and then re-open it.

159
00:13:24,160 --> 00:13:28,260
So this is an example of a mobile app where you cannot dismiss the keyboard.

160
00:13:28,880 --> 00:13:37,160
This is Trello, where you can't dismiss the keyboard, but you're not actually on a form or any kind of field,

161
00:13:37,160 --> 00:13:40,800
so that you can't even escape out of it.
It just shows up there.

162
00:13:40,800 --> 00:13:43,000
And as you can see, it takes up a whole lot of room.

163
00:13:44,200 --> 00:13:46,560
And theres this thing, we named it the hovertrap.

164
00:13:47,120 --> 00:13:52,220
This is where you have desktop-specific sites that are shown on mobile.

165
00:13:52,240 --> 00:13:57,360
And if you mouse over them on a desktop,  you get this beautiful zoomed in portion.

166
00:13:57,360 --> 00:13:59,640
So you see this a lot on clothing sites.

167
00:14:00,240 --> 00:14:08,240
What happens on a mobile is if you touch the item, it gives you that zoomed in portion on the right,

168
00:14:08,240 --> 00:14:09,940
but there's no way to close that.

169
00:14:10,200 --> 00:14:14,760
So, you can't actually get that image to ever disappear on a mobile.

170
00:14:15,120 --> 00:14:20,240
So we call it a trap because, like a keyboard trap, you have to close the browser and start again.

171
00:14:20,280 --> 00:14:22,280
So, it's very serious.

172
00:14:23,760 --> 00:14:27,520
We've also come across VoiceOver swipe traps.

173
00:14:27,640 --> 00:14:33,280
We've never had problems with VoiceOver until we started testing it on mobile.

174
00:14:33,280 --> 00:14:35,740
So, this is LinkedIn, this is its status update.

175
00:14:35,920 --> 00:14:41,480
Basically, you are stuck on the arrow. There's basically nothing on the page. Really.

176
00:14:41,480 --> 00:14:46,680
You can't dismiss the page, you can't access the keyboard, you can't link back.

177
00:14:46,680 --> 00:14:48,080
You cannot do anything.

178
00:14:48,080 --> 00:14:52,280
With VoiceOver, you're only option is to close the browser and start again.

179
00:14:53,080 --> 00:14:56,120
YouTube also has a VoiceOver swipe trap.

180
00:14:56,120 --> 00:14:57,860
Just slightly different.

181
00:14:57,880 --> 00:15:04,680
Basically, what happens is, you're stuck in a search bar, the rest of the content is grayed out,

182
00:15:04,800 --> 00:15:10,100
and if you are a visual user, you can tap on that content and it becomes the top layer.

183
00:15:11,240 --> 00:15:16,980
But if you are a VoiceOver user, you cannot get to that content at all. So you're stuck in the search bar.

184
00:15:21,280 --> 00:15:28,380
Just because I feel I should pick on all the social media networks, the Facebook Friends List,

185
00:15:28,400 --> 00:15:34,860
you can open the Facebook Friends List with VoiceOver, but you should be able to swipe to go backwards,

186
00:15:34,880 --> 00:15:39,020
and you can't. You're stuck in your Friends List.

187
00:15:41,640 --> 00:15:44,600
And this is a touch trap. This is impressive.

188
00:15:45,680 --> 00:15:51,660
So, you can't actually move the screen,
so you can't, you know, slide scroll.

189
00:15:52,520 --> 00:15:56,480
The only way to move the screen is to activate this little arrow at the bottom

190
00:15:56,480 --> 00:15:58,480
that doesn't meet color contrast requirements.

191
00:15:58,840 --> 00:16:03,700
And that throws you to the top of the page. So, we call that a touch trap.

192
00:16:05,640 --> 00:16:07,840
Mobile issues.

193
00:16:07,960 --> 00:16:11,020
Ok, so, Coles.

194
00:16:12,360 --> 00:16:19,960
I actually ran this presentation, and I have a couple of examples from Coles. Coles is like your Walgreens.

195
00:16:20,880 --> 00:16:23,200
And Coles is notoriously inaccessible.

196
00:16:23,280 --> 00:16:28,220
There are two major supermarket chains in Australia, and Coles is one of them.

197
00:16:28,720 --> 00:16:32,660
The day after I ran this presentation at the Future of Web Design in New York,

198
00:16:33,640 --> 00:16:37,820
Coles, there was a law suit started in Australia
against Coles

199
00:16:37,840 --> 00:16:40,760
for their site not being accessible to
vision impaired people.

200
00:16:41,600 --> 00:16:46,200
The problem with this app is that you have these buttons down on the bottom,

201
00:16:46,760 --> 00:16:50,200
and it says Lists, Specials, Product Finder,  More.

202
00:16:50,200 --> 00:16:53,160
And they're coded as buttons.
But they don't have any alternatives.

203
00:16:53,640 --> 00:16:57,160
So VoiceOver reads them as
button button button button.

204
00:16:59,640 --> 00:17:01,000
Access.

205
00:17:01,760 --> 00:17:05,820
So, you need to make sure that you specify your inputs correctly.

206
00:17:05,820 --> 00:17:11,000
So for some reason, Elance had decided they were going to create their own little drop-down,

207
00:17:11,000 --> 00:17:13,920
that doesn't follow any HTML rules whatsoever.

208
00:17:14,000 --> 00:17:17,460
So you can only choose 14, 15, 16, or 17,

209
00:17:17,600 --> 00:17:21,540
because it's recognized as a keyboard input field,

210
00:17:21,840 --> 00:17:26,900
but there's no ... there's actually a select
that you need to do.

211
00:17:26,920 --> 00:17:29,320
So if that had been coded as a select

212
00:17:29,320 --> 00:17:33,940
the mobile would have recognized it as such and would have shown it to you in a much friendly way.

213
00:17:35,880 --> 00:17:37,980
Text size is probably my biggest one.

214
00:17:38,640 --> 00:17:42,980
I actually can read very small text size, 
but this is ridiculous.

215
00:17:43,400 --> 00:17:45,400
This is the Etsy.

216
00:17:46,160 --> 00:17:51,760
And it looks like maybe four point.
And there's no way to increase the size.

217
00:17:53,040 --> 00:17:57,420
This ... is probably my favorite. No, actually Coles is.

218
00:17:57,920 --> 00:18:05,460
So this here is the app that you get when you fly from Australia to Los Angeles using Virgin Australia.

219
00:18:06,520 --> 00:18:10,720
And down at the bottom here, is ...
your longitude, your latitude,

220
00:18:10,720 --> 00:18:16,020
how many hours you've been flying, how long until you arrive, etc. etc.

221
00:18:16,040 --> 00:18:22,180
But this text is so small, that you cannot actually,
I can't read it on a mobile phone.

222
00:18:22,200 --> 00:18:24,400
And it doesn't allow pinch zoom.

223
00:18:24,400 --> 00:18:29,920
So, someone but this. Someone design it. Someone coded it.

224
00:18:29,920 --> 00:18:35,480
And at no point did they actually look at it on a phone, to determine it was unreadable.

225
00:18:38,680 --> 00:18:42,140
So, when you have text size, you need to make sure that

226
00:18:42,160 --> 00:18:46,140
if you're going to support the system settings on the phone, that they make sense.

227
00:18:46,160 --> 00:18:53,920
So, this here is the iPhone with the smallest text size. And this here is the iPhone with it's largest text size.

228
00:18:53,920 --> 00:18:57,060
So you can see that AccessibilityOz is basically cut off.

229
00:18:57,080 --> 00:19:03,100
So if you're going to support the system settings in your phone, make sure you test with those system settings.

230
00:19:04,240 --> 00:19:10,180
This is another example where basically the "Discover," "Cuisine," and "Open for" are cut off.

231
00:19:11,160 --> 00:19:19,420
And this is, you know, even Apple couldn't get it right because this is the part where you increase the text size.

232
00:19:19,440 --> 00:19:25,420
So on the lowest it says "Apps that support Dynamic Type will adjust to your preferred reading size below."

233
00:19:25,720 --> 00:19:30,180
And then when you put it on its largest, it goes "Apps that support Dy...",

234
00:19:31,040 --> 00:19:33,500
Because there's not enough room for it.

235
00:19:34,440 --> 00:19:37,320
They have actually fixed that particular error.

236
00:19:38,760 --> 00:19:44,800
Ok, so then you do see mobile apps that have large text.

237
00:19:46,240 --> 00:19:48,520
Or have a way to increase large text.

238
00:19:49,200 --> 00:19:51,480
So you can see that's not really large text.

239
00:19:51,480 --> 00:19:56,620
That's  moving from a size 8 font to maybe a size 10 font. That's not large text.

240
00:19:57,560 --> 00:20:03,960
In-app settings, so BBC news for example, doesn't support the system settings in an iPhone,

241
00:20:04,400 --> 00:20:08,540
but they have their own feature to increase text size.

242
00:20:08,920 --> 00:20:12,180
But if you look at it, that's not really particularly large.

243
00:20:12,280 --> 00:20:18,420
That's going once again form maybe a size 6 font to maybe a size 11 or 12 font.

244
00:20:20,080 --> 00:20:26,900
This is the ABC website. Once again small is very very small. Maybe 2 or 3 points.

245
00:20:26,920 --> 00:20:29,400
And large is maybe 12 or 14 points.

246
00:20:29,920 --> 00:20:35,320
But the important thing is that this is a small font and this is the large font.

247
00:20:35,440 --> 00:20:42,480
So, your titles and your who's written it and your captions are all the same size

248
00:20:42,480 --> 00:20:44,800
no matter what setting you selected.

249
00:20:44,800 --> 00:20:51,000
And you'd think, maybe the title would be, one of the most important things you wanted to make large.

250
00:20:52,840 --> 00:20:54,200
Color Contrast.

251
00:20:55,720 --> 00:20:58,740
Gray text on a white background is a bad idea.

252
00:21:00,160 --> 00:21:01,800
Hardly anyone can read it.

253
00:21:02,040 --> 00:21:06,520
We do user testing, people don't know ... everything about that search bar,

254
00:21:06,880 --> 00:21:12,920
it's gray text on a white background. The don't see it, they won't know where to put their search.

255
00:21:13,440 --> 00:21:18,040
Now this is Amazon. You know, basically this is the way that people are going to find things,

256
00:21:18,440 --> 00:21:20,440
and yet it's gray text on a white background.

257
00:21:21,880 --> 00:21:24,080
Gray text on a gray background.

258
00:21:24,080 --> 00:21:26,580
Search eBay, is also bad.

259
00:21:27,280 --> 00:21:34,920
But probably worse is LinkedIn, which is like a medium gray text on a light gray background.

260
00:21:34,920 --> 00:21:40,160
And this is just how close these people are to you in terms of your profile.

261
00:21:40,160 --> 00:21:45,040
So, Kare Romanski is a first degree, Jake Mitchell is a second degree,

262
00:21:45,040 --> 00:21:49,340
that's the kind of information that I, as a specialist might want to know.

263
00:21:49,360 --> 00:21:55,420
I might want to say, ok, I want to reach out to Steve Lee. No, well, I'm already a first level person.

264
00:21:55,440 --> 00:22:00,240
Well, if I can't tell because of the color contrast, then that is information I'm missing out on.

265
00:22:01,960 --> 00:22:03,960
Color alone is another problem.

266
00:22:04,460 --> 00:22:09,240
So, today's date, marked in blue
where everything else is black

267
00:22:09,240 --> 00:22:11,900
you're assuming that people don't have
color contrast issues.

268
00:22:12,360 --> 00:22:17,220
But it's also something that probably won't get read aloud to your screen reader users.

269
00:22:18,600 --> 00:22:24,440
So this is even worse because this will just be a little image

270
00:22:24,640 --> 00:22:27,580
and these will be colored table data cells.

271
00:22:27,600 --> 00:22:31,580
So that information is not going to be available to a screen reader at all.

272
00:22:34,720 --> 00:22:36,720
Maybe this is my favorite of the examples.

273
00:22:36,720 --> 00:22:38,720
So Kmart. Do you guys have Kmart?

274
00:22:39,000 --> 00:22:40,720
[Audience]: Yes

275
00:22:40,800 --> 00:22:44,440
[Gian]: So, this is the Kmart website,

276
00:22:45,600 --> 00:22:52,100
and this here is a link. You activate that link,
and you get an empty page.

277
00:22:52,800 --> 00:22:55,220
You get an empty page because it links to a Flash catalog.

278
00:22:56,520 --> 00:23:02,660
Flash is not supported on iOS devices, and hasn't been ... forever.

279
00:23:02,840 --> 00:23:09,600
So, they obviously never tested this. But not just that. In all Western countries,

280
00:23:09,920 --> 00:23:15,240
iOS devices are by far the most popular in mobile and tablet devices.

281
00:23:15,320 --> 00:23:21,060
So, at what point did anyone look at this?
And say "Oh, it's not even loading?"

282
00:23:22,320 --> 00:23:28,660
Zooming. Zooming is a big problem.
People zoom a lot on mobile or tablet.

283
00:23:28,960 --> 00:23:33,240
This is Airbnb. As you can see, it just overlaps and underlaps and looks terrible

284
00:23:33,960 --> 00:23:42,280
to the point where you can't even read some of the contents, to the point where you can read anything at all.

285
00:23:42,280 --> 00:23:47,060
So you say ok, fine. I know I'm on the mobile site,
I'll just go to the desktop site.

286
00:23:47,640 --> 00:23:50,860
And then, it loses all of your information.

287
00:23:51,960 --> 00:23:55,600
So you can imagine your searching for something, you found it and you just want to zoom in on something,

288
00:23:55,600 --> 00:23:59,840
it crashes. You go to the desktop site. You've lost all of your data.

289
00:24:03,000 --> 00:24:04,760
Functionality unclear.

290
00:24:06,280 --> 00:24:08,280
So is this one way or is it return?

291
00:24:11,960 --> 00:24:18,260
So, using color, alone, to convey information is problematic, but even if one was underlined

292
00:24:18,280 --> 00:24:22,200
and not underlined, its still a little bit unclear.

293
00:24:22,560 --> 00:24:28,820
Now, if it's going to be unclear for the general public, it's definitely going to be unclear for people with disabilities.

294
00:24:30,360 --> 00:24:35,120
This one, I can buy a warehouse trailing floral dress

295
00:24:35,520 --> 00:24:37,520
I can select from zero to dot dot dot.

296
00:24:38,280 --> 00:24:41,820
Now I'm not going to but this dress, because I don't know what it is that I am selecting.

297
00:24:43,920 --> 00:24:46,180
Ah, so, now we've got Commonwealth Bank.

298
00:24:46,400 --> 00:24:53,240
So, if you click on that, "Call Michael," it makes a phone call, uses your phone, very clever.

299
00:24:54,200 --> 00:24:59,580
So you think, Michael dot Dikeakos
at cba dot co dot dot dot

300
00:24:59,600 --> 00:25:02,440
because the email address is so long and
they can't fit it in,

301
00:25:02,440 --> 00:25:05,860
that maybe if you hit that, it would open your email ...

302
00:25:05,880 --> 00:25:07,820
... doesn't do that.

303
00:25:08,440 --> 00:25:13,720
These email addresses, that aren't displayed properly, are not active.

304
00:25:14,760 --> 00:25:16,260
Where as this is.

305
00:25:19,480 --> 00:25:22,600
Most people think that if you mark something as gray,

306
00:25:22,600 --> 00:25:24,600
it means that it is inactive.

307
00:25:24,600 --> 00:25:29,160
So, here we've got add a message, name, email, phone, postcade

308
00:25:29,680 --> 00:25:34,240
all in a light gray on a white background. 
Almost impossible to read.

309
00:25:34,240 --> 00:25:38,720
So they seem to be inactive. But they are actually active, if you tap on them.

310
00:25:39,600 --> 00:25:41,880
But, of course, VoiceOver can't catch them.

311
00:25:45,200 --> 00:25:50,740
It's also important to think about how people will use your systems.

312
00:25:51,440 --> 00:25:55,380
And that they might use them differently 
to what you expect.

313
00:25:55,960 --> 00:25:59,880
So YouTube for example, is a responsive website.

314
00:26:00,000 --> 00:26:05,960
So if you increase text size, it will eventually turn it into what you see on a mobile.

315
00:26:06,720 --> 00:26:11,420
Now, someone at YouTube has decided that, if you're on the mobile YouTube website,

316
00:26:11,440 --> 00:26:14,700
at no point are you ever going to want to upload a video.

317
00:26:15,440 --> 00:26:19,600
So, if you zoom in on the site as in Control Plus,

318
00:26:19,600 --> 00:26:23,540
you lose your upload button,
and your notifications button.

319
00:26:23,560 --> 00:26:27,260
So you cannot ... if you're zooming in,
you cannot upload a video to YouTube.

320
00:26:29,320 --> 00:26:31,660
This is Asana.

321
00:26:31,680 --> 00:26:35,260
Asana has this great featured called My Tasks.

322
00:26:35,320 --> 00:26:37,320
And this is how I get everything done.

323
00:26:37,360 --> 00:26:39,360
If it's not in My Tasks, it doesn't get done.

324
00:26:39,840 --> 00:26:44,420
Well that's great. Except for ... 
the mobile version doesn't have My Tasks.

325
00:26:44,920 --> 00:26:46,520
So how can I use it?

326
00:26:47,360 --> 00:26:48,940
So now we use Trello.

327
00:26:49,800 --> 00:26:52,080
This is Row in New York City.

328
00:26:52,680 --> 00:26:56,660
I put this example here because Future of Web Design put me up and we're in New York City.

329
00:26:57,320 --> 00:27:02,760
And this is the mobile version,
and this is the desktop version.

330
00:27:03,320 --> 00:27:05,460
So the mobile version has all your navigation,

331
00:27:06,040 --> 00:27:12,320
but it's got this big image about how do you create your New York City and it links off to

332
00:27:12,320 --> 00:27:16,600
how do you get access to Times Square or how do you visit MOMA and all of that kind of stuff.

333
00:27:17,160 --> 00:27:18,900
And none of that is on the mobile site.

334
00:27:19,360 --> 00:27:23,700
So you can image, you're looking at, where you're going to stay, and you click through,

335
00:27:23,720 --> 00:27:25,860
and "awe yeah, excellent, that's great."

336
00:27:25,880 --> 00:27:27,760
and you're on your way to New York,

337
00:27:27,760 --> 00:27:30,880
and you check the mobile site
to figure out where is it you want to go,

338
00:27:31,240 --> 00:27:33,240
and that information is not there.

339
00:27:34,960 --> 00:27:36,820
Pixelation on zoom.

340
00:27:41,920 --> 00:27:50,020
This is a mobile magazine, which you get for free if you fly with Virgin Australia on a local flight.

341
00:27:50,880 --> 00:27:57,040
They give you free access, assuming that you'll love the magazine so much that you will buy it.

342
00:27:58,320 --> 00:28:04,660
And yet, the books that it's promoting are so pixelated you can't even tell what the title is.

343
00:28:06,000 --> 00:28:13,500
This is another example about a Self-Worth Circle. And the only thing that is actually readable

344
00:28:13,760 --> 00:28:15,760
is the word "negative."

345
00:28:17,360 --> 00:28:21,180
Source order.
Source order is really important on mobile.

346
00:28:21,640 --> 00:28:26,460
So these are requirements on WCAG 2,
a lot of people aren't aware of them.

347
00:28:27,560 --> 00:28:32,720
So this is Lion King. Tickertech call, whatever your ticketing system is.

348
00:28:33,040 --> 00:28:36,780
And you think ok, so you select those things,
you hit Find Tickets.

349
00:28:36,960 --> 00:28:41,080
But, there's a whole bunch of information that's underneath that button.

350
00:28:42,240 --> 00:28:47,360
Not only color contrast, but especially the stuff about accessible tickets

351
00:28:47,360 --> 00:28:51,580
and how you have to go through a deeper process if you want an accessible ticket.

352
00:28:51,600 --> 00:28:56,140
But, you wouldn't think to scroll down, because it looks like a complete page,

353
00:28:56,160 --> 00:28:58,600
it looks like you reached the end of the page.

354
00:28:58,600 --> 00:29:02,140
So, be aware that no one is going to look past your submit buttons.

355
00:29:05,560 --> 00:29:10,160
To the point where, I was using this on my tablet, and you can see,

356
00:29:10,800 --> 00:29:15,920
you can see that there's options for room number, last name, continue button.

357
00:29:16,320 --> 00:29:18,320
Or you can have an access code and enter it here.

358
00:29:18,800 --> 00:29:23,060
So, I put in my room number, and I put in my last name, and I hit Continue,

359
00:29:23,160 --> 00:29:29,660
and it said you don't have access. I was like, no, but I do. So, I put in my room number and I put in my last name,

360
00:29:29,680 --> 00:29:37,260
and I hit continue. I said, but I do have an access code. And I couldn't believe I did not see,

361
00:29:37,280 --> 00:29:38,860
even though it was visible on the screen,

362
00:29:38,880 --> 00:29:42,620
because I was just concentrating on what was above the submit button.

363
00:29:43,000 --> 00:29:48,680
That's something I do, then it's going to be even more serious for, say for a screen reader user

364
00:29:48,680 --> 00:29:51,200
who takes much longer to go through a page.

365
00:29:51,320 --> 00:29:55,280
They're expecting the end to be a submit button, and that's where the end should be.

366
00:29:57,160 --> 00:30:04,900
This is another example, LastPass. I was purchasing Internet access on this Virgin Australia flight,

367
00:30:04,920 --> 00:30:07,900
no, it wasn't Virgin Australis, 
they don't have Internet on the flight.

368
00:30:08,680 --> 00:30:15,440
United. And I put in my email address and I put in my password, and I hit login.

369
00:30:16,440 --> 00:30:18,720
And it said "No network connectivity detected."

370
00:30:19,080 --> 00:30:22,740
I was like, I know it's on my phone, it shouldn't need network connectivity.

371
00:30:23,120 --> 00:30:28,000
What I had to do was select the option down below underneath the submit button Login Offline.

372
00:30:28,280 --> 00:30:33,980
Now, there are requirements for error suggestions and error descriptions in WCAG 2.

373
00:30:34,000 --> 00:30:36,640
In order for this to meet WCAG 2, you would say

374
00:30:36,640 --> 00:30:40,880
"No Network connectivity detected. Would you like to login offline?"

375
00:30:42,440 --> 00:30:43,920
It makes sense for people who don't ...

376
00:30:43,920 --> 00:30:49,420
... and I probably did this process three or four times before I realized that was there.

377
00:30:49,440 --> 00:30:51,440
And I could see it the whole time.

378
00:30:55,000 --> 00:30:56,400
Touch targets.

379
00:30:56,840 --> 00:31:03,780
So, this is Twitterific I think,

380
00:31:04,760 --> 00:31:10,080
and it's important that when you have an active element on a mobile, that it is a certain size.

381
00:31:10,480 --> 00:31:12,360
And these are not large enough.

382
00:31:12,560 --> 00:31:18,780
So, they're what, maybe, four pixels by four pixels, maybe eight pixels by eight pixels.

383
00:31:19,080 --> 00:31:24,500
The BBC has some great recommendations on size.

384
00:31:24,640 --> 00:31:30,680
But they are so small that you have to hit them several times before you actually have activated one.

385
00:31:31,440 --> 00:31:34,220
This is my favorite. This is the zoom of doom.

386
00:31:34,240 --> 00:31:35,600
This is a Cole's site.

387
00:31:36,400 --> 00:31:43,760
So this is basically a map that shows you where Coles is in Veepoon, which is a long way from anywhere

388
00:31:44,360 --> 00:31:50,400
But, if you scroll, swipe in the map area, it moves the map.

389
00:31:51,200 --> 00:31:58,080
If you want to move the page, you have to manage to select this small white area around the edge of the map

390
00:31:58,320 --> 00:31:59,880
in order to move the page.

391
00:32:01,400 --> 00:32:06,960
The other thing you have to do with touch targets is you need to make sure they're activated on removal of touch,

392
00:32:06,960 --> 00:32:08,300
not on touch.

393
00:32:08,680 --> 00:32:10,420
So, Coles again.

394
00:32:11,320 --> 00:32:19,200
So let's say I just want to scroll up this point. If I scroll, sorry, if I swipe, and I hit South Australia on that swipe,

395
00:32:19,240 --> 00:32:22,100
it will automatically jump to the South Australia stores,

396
00:32:22,120 --> 00:32:24,620
even though I might be using the swipe gesture.

397
00:32:25,160 --> 00:32:29,660
The other problem with this, is that every single Coles store in Australia

398
00:32:30,400 --> 00:32:34,380
is listed on one page, and there's no back to top.

399
00:32:35,360 --> 00:32:40,700
So there are thousands of stores listed here, and there is no way to get back to the top of the page

400
00:32:40,720 --> 00:32:44,480
to choose another state, unless you scroll. And it took me eight seconds.

401
00:32:48,200 --> 00:32:49,220
Spacing.

402
00:32:49,320 --> 00:32:55,400
Ok, so you really don't want to put your edit button right next to your Mark Complete button.

403
00:32:55,640 --> 00:32:59,580
Because they're opposite actions, and people accidentally click things

404
00:32:59,600 --> 00:33:03,740
that they shouldn't click on mobiles devices much more than they do on desktop.

405
00:33:05,320 --> 00:33:06,800
This is even worse.

406
00:33:06,800 --> 00:33:13,820
In order to get rid of this install Airbnb, to have to click this tiny little close button.

407
00:33:13,880 --> 00:33:15,880
It's about four pixels by four pixels.

408
00:33:16,360 --> 00:33:19,540
If you click anything else, it will install the app.

409
00:33:23,600 --> 00:33:25,220
Then there's things like just lack of testing,

410
00:33:25,240 --> 00:33:28,940
which probably covers a whole lot of things that I've talked about today.

411
00:33:28,960 --> 00:33:33,920
Best of YouTube. VoiceOver reads it as Best of YaToob.

412
00:33:37,040 --> 00:33:42,600
This is Target, which is ...
I think you guys have Target too.

413
00:33:43,200 --> 00:33:52,800
So if you activate this little image of ... game ... video games, it gives you this

414
00:33:53,000 --> 00:34:04,360
your search for 56626957 56626872 56626940 56626841 found four product results.

415
00:34:04,840 --> 00:34:06,840
Well actually, no.

416
00:34:08,120 --> 00:34:11,400
This is Coles. This is a mobile website.

417
00:34:11,940 --> 00:34:17,920
And, you know, you can't actually read the text at all, it's just squished.

418
00:34:18,280 --> 00:34:20,340
So no one looked at it. No one tested it.

419
00:34:22,200 --> 00:34:25,700
This is where one of my favorite dress shops are.

420
00:34:26,080 --> 00:34:30,520
Take me to the map, and it's taken me to the latitude and the longitude

421
00:34:31,240 --> 00:34:34,280
not the actual address.

422
00:34:36,920 --> 00:34:43,640
This is Kmart. So according to Kmart, Australia consists just of Western Australia,

423
00:34:44,120 --> 00:34:47,020
because the rest of it is off the screen.

424
00:34:48,680 --> 00:34:50,780
Same with Dish.com.

425
00:34:51,600 --> 00:34:55,760
We deliver to Sydney and ... well,
I guess you deliver to Sydney.

426
00:34:57,280 --> 00:35:01,200
Drupal, so once again, you have overlapping text,

427
00:35:01,720 --> 00:35:04,920
on a major iOS device, it's a problem.

428
00:35:05,640 --> 00:35:09,680
Spelling mistakes. So "10 cafe ustomers that are more annoying" ...

429
00:35:09,920 --> 00:35:14,300
they are going to really annoy people on mobile much more so than on desktop.

430
00:35:15,680 --> 00:35:19,880
Now this one is interesting. This happened about two years ago.

431
00:35:20,240 --> 00:35:24,940
All of a sudden, there was HTML code in all the Facebook headings.

432
00:35:25,480 --> 00:35:33,580
And it lasted, for some it lasted two hours. Crikey it was like this, Crikey is kind of like our alternative newspaper.

433
00:35:34,280 --> 00:35:36,000
It was like this for about two weeks.

434
00:35:36,320 --> 00:35:42,080
So the heading is span class equals qou end span why sacrifice yourself whistleblowers dot dot dot

435
00:35:42,680 --> 00:35:45,360
Now what happened? It's not like everyone got together one day and said

436
00:35:45,920 --> 00:35:48,540
"Let's put HTML code into our Facebook headings."

437
00:35:48,560 --> 00:35:52,060
It's that that's what was posted into Facebook, and Facebook changed something

438
00:35:52,400 --> 00:35:54,860
and then all of a sudden, that HTML code is showing up.

439
00:35:55,320 --> 00:35:58,800
Now, some people picked up on it quickly,
some people took two weeks.

440
00:36:01,920 --> 00:36:05,760
You don't want to post broken links.
People don't like broken links.

441
00:36:06,560 --> 00:36:09,600
And, this is ... we get to Los Angeles Airport

442
00:36:10,720 --> 00:36:15,400
Wi-Fi Internet Access. Were you disconnected?
Click here to reconnect.

443
00:36:15,480 --> 00:36:17,600
Time left twenty four hours zero minutes

444
00:36:17,760 --> 00:36:21,440
This page will redirect, so content doesn't really make sense to have here.

445
00:36:21,600 --> 00:36:23,140
[giggles]

446
00:36:23,200 --> 00:36:27,220
[Gian] And all of a sudden I don't want to give you my credit card information.

447
00:36:27,640 --> 00:36:29,480
You need to be careful with errors.

448
00:36:30,240 --> 00:36:36,060
Triplify.com description reference error can't find variable triplifymap file

449
00:36:36,080 --> 00:36:43,700
http www triplify dot com slash js slash display results dot js etc. etc.

450
00:36:44,720 --> 00:36:46,580
Give something meaningful to users.

451
00:36:48,400 --> 00:36:50,080
This is Green Apple Books.

452
00:36:50,080 --> 00:36:55,700
I'm ... I've got a library at home. I love real books. I can't read books on [garbled].

453
00:36:56,360 --> 00:36:58,880
This is the Green Apple Books mobile website.

454
00:36:59,320 --> 00:37:05,400
So not having an open day and half the map is off the page, half the information is off the page.

455
00:37:06,160 --> 00:37:09,960
The same with their events, on this specific mobile site.

456
00:37:10,320 --> 00:37:13,160
But if you went to their desktop site, it worked.

457
00:37:14,240 --> 00:37:17,240
So once again,
you need to make sure you test these things.

458
00:37:18,800 --> 00:37:20,440
This is Qantas.

459
00:37:20,440 --> 00:37:22,580
Because I don't want to pick just on Virgin Australia.

460
00:37:23,560 --> 00:37:26,880
So this is where you choose where you want to fly to, and from.

461
00:37:27,120 --> 00:37:29,000
Now Qantas flies everywhere.

462
00:37:29,720 --> 00:37:32,720
And so it says select city, and it starts at "A."

463
00:37:33,320 --> 00:37:36,900
Aberdeen ... Abidjan ... Accra ... Addis Ababa ...

464
00:37:37,520 --> 00:37:39,780
it took me twelve seconds to scroll down to Melbourne.

465
00:37:43,040 --> 00:37:46,780
Ok, so that's all the things you shouldn't do,
not all the things, some of the things,

466
00:37:46,800 --> 00:37:49,180
So I want to talk about correct implementations.

467
00:37:49,640 --> 00:37:51,940
This is Twitterific.

468
00:37:52,920 --> 00:37:58,580
So it is actually large text. But it also allows you to change the color.

469
00:37:59,000 --> 00:38:06,020
Now, it's interesting to note that people who have Dyslexia actually like to reduce color contrast

470
00:38:06,040 --> 00:38:10,180
so even though people with certain vision impairments like to increase color contrast,

471
00:38:10,200 --> 00:38:12,060
there are groups who want to do the opposite.

472
00:38:12,120 --> 00:38:15,940
So the ability to choose color contrast is quite important.

473
00:38:17,480 --> 00:38:21,500
So your iMessage actually supports large text size.

474
00:38:23,000 --> 00:38:24,560
And this is our website.

475
00:38:25,040 --> 00:38:29,600
So you can see in the main area we change the color contrast and things like that.

476
00:38:30,040 --> 00:38:32,040
Talks about outline etc. etc.,

477
00:38:32,240 --> 00:38:35,820
and can zoom in so much that you can see only two letters at a time

478
00:38:35,960 --> 00:38:39,700
and there will be some people that need to have that level of zoom.

479
00:38:41,680 --> 00:38:44,440
This is State Library New South Wales.

480
00:38:44,880 --> 00:38:49,120
So you've got this old photograph of people in Melbourne or Sydney.

481
00:38:49,440 --> 00:38:54,060
And you can zoom in and still get quite good quality information.

482
00:38:56,360 --> 00:39:02,500
Also, when it comes to desktop, you can move your mouse around, and see that

483
00:39:02,920 --> 00:39:05,560
it changes to indicate that something is active.

484
00:39:05,560 --> 00:39:12,240
You can't do that on a mobile, so you can't assume that people know when there's more functionality.

485
00:39:12,360 --> 00:39:18,560
So these people at Time have put this little tap text to indicate that you can tap on that

486
00:39:18,880 --> 00:39:20,880
and it gives you more information.

487
00:39:21,720 --> 00:39:25,000
Not quite sure of the point of this,
but it's still a good idea.

488
00:39:25,240 --> 00:39:28,900
This is The Guardian and it has that little arrow icon,

489
00:39:29,080 --> 00:39:33,960
and it takes you to what you would think would be a larger version the image but it's the same size.

490
00:39:34,120 --> 00:39:37,640
So I'm not quite sure why it did that, but at least it indicates that you can

491
00:39:38,120 --> 00:39:40,120
open that image separately.

492
00:39:42,120 --> 00:39:48,960
So this one has a "Done" option on its keyboard, it also has previous and next.

493
00:39:48,960 --> 00:39:52,980
So you can actually jump through your fields using mobile.

494
00:39:55,960 --> 00:39:57,500
And correct inputs.

495
00:39:57,680 --> 00:40:01,940
So, whoever coded that field, coded it as a telephone field

496
00:40:02,360 --> 00:40:05,800
and therefore the number keypad on mobile shows up.

497
00:40:07,960 --> 00:40:13,680
So this uses color and shape to indicate
what dates you selected.

498
00:40:14,360 --> 00:40:19,980
So you still would need to place some stuff behind make sure it gets read properly by the screen reader.

499
00:40:20,440 --> 00:40:23,520
But, by using changes in color and changes in shape,

500
00:40:23,520 --> 00:40:27,380
your covering people who have color contrast issues
as well.

501
00:40:29,080 --> 00:40:34,240
I mentioned the BBC Mobile accessibility guidelines. They're easy to find.

502
00:40:34,960 --> 00:40:40,740
There's also a whole bunch of OzWiki accessibility factsheets that are freely available,

503
00:40:40,760 --> 00:40:42,760
and Dennis has been tweeting them out all week.

504
00:40:43,440 --> 00:40:51,680
They're quite in-depth, especially the JavaScript one, is incredibly in-depth with demos and stuff you can use.

505
00:40:52,120 --> 00:40:55,380
And we also have this thing called OzWiki

506
00:40:55,400 --> 00:41:00,380
which a lot of these errors came from, and if you'd like access, come talk to me.

507
00:41:01,760 --> 00:41:09,280
As said, you can get this presentation on a11yoz.com/2016mobile

508
00:41:09,280 --> 00:41:11,480
and, any questions?

509
00:41:13,680 --> 00:41:14,260
[Gian]: Yes.

510
00:41:14,280 --> 00:41:19,180
[Attendee]: A common thing I see is when an app displays a message on the phone

511
00:41:19,200 --> 00:41:26,260
and it disappears from the screen. I'm running into that. And then I'm telling the developers

512
00:41:26,280 --> 00:41:31,060
ok, if your using a braille display, you won't be able to read it because the text isn't there anymore.

513
00:41:31,600 --> 00:41:38,040
[Gian]: Yes, so we saw that once or twice maybe five years ago.

514
00:41:38,360 --> 00:41:41,560
And in the last six months, it's just everywhere.

515
00:41:41,560 --> 00:41:47,820
Having errors disappears after a period of time is problematic.

516
00:41:47,840 --> 00:41:55,280
I think it's actually ... it has to do with the use of HTML5 form elements.

517
00:41:55,280 --> 00:42:00,040
Yeah, but it can be problematic. It's a very big issue.

518
00:42:00,560 --> 00:42:04,980
[Attendee]: I was dealing with it all day.

519
00:42:06,240 --> 00:42:07,760
[Gian]: Any other questions?

520
00:42:08,640 --> 00:42:12,440
[Attendee]: So you mentioned the ... unclear functionalities. I'm just curious,

521
00:42:12,440 --> 00:42:18,200
what would be the best approach to making sure each button or tab is active?

522
00:42:19,880 --> 00:42:26,760
Would it be just changing the color and the shape of the button? What is their task?

523
00:42:26,760 --> 00:42:33,280
[Gian]: So, the question is how do you,
for the people on the call,

524
00:42:33,280 --> 00:42:38,980
how do you indicate what's active and what's not, maybe on a tab or on the one way versus return.

525
00:42:39,680 --> 00:42:42,360
It depends on what you're using.

526
00:42:42,640 --> 00:42:46,640
Tabs is a little bit easier because there's a whole bunch of ARIA roles around tabs

527
00:42:46,640 --> 00:42:51,900
that will get read to screen readers.So you know that will get read properly to at least one group of people.

528
00:42:53,920 --> 00:43:03,120
There are things that you can do, like a little arrow, for the tab that you've got indicated,

529
00:43:03,120 --> 00:43:09,080
if you have it in blue with the little arrow that points down, I've seen that happen a few times.

530
00:43:10,520 --> 00:43:16,660
Also, repeating the content as headings. So if you have one way of return and then something that said one way,

531
00:43:16,660 --> 00:43:18,640
that's another way of doing it.

532
00:43:20,560 --> 00:43:26,820
Yeah. I'll see if I can ... there might be some examples in OzWiki. Let's me see ... I'll see if I can find them.

533
00:43:27,840 --> 00:43:37,780
[Attendee]: I think it was an autoplay feature, I think it was enlarge image feature you showed earlier

534
00:43:37,800 --> 00:43:42,160
in the slideshow. You were saying that one of the accessibility problems for that is that

535
00:43:42,160 --> 00:43:50,480
it would take up too much space. Would that take up too much data usage on a cell phone as well?

536
00:43:50,480 --> 00:43:55,140
[Gian]: I think you're probably talking about movement.

537
00:43:55,140 --> 00:43:58,660
So Facebook is the perfect example of this.

538
00:43:59,160 --> 00:44:03,960
The Autoplay video function on Facebook chews through data.

539
00:44:05,480 --> 00:44:10,340
First you've got movement that can't be stopped by the user, which is one of those non-interference clauses,

540
00:44:10,720 --> 00:44:15,240
but also it uses a whole lot of data,
a whole lot of bandwidth,

541
00:44:15,240 --> 00:44:18,040
so yeah definitly that would really be a problem.

542
00:44:19,360 --> 00:44:20,740
Any other questions?

543
00:44:21,120 --> 00:44:24,840
[Attendee]: With larger institutions in this country anyway,

544
00:44:24,840 --> 00:44:31,080
you tend to have the developers overseas. Primarily the Asian countries.

545
00:44:31,080 --> 00:44:37,520
As my function as a designer,
I'm never going to know all of this.

546
00:44:37,520 --> 00:44:43,840
What ... is there a wiki that you have that is specifically for designers to be aware of?

547
00:44:43,840 --> 00:44:47,060
Because, communicating with Asia is ...

548
00:44:47,520 --> 00:44:53,460
So, yeah. OzWiki is ...
OzWiki can definitely be used by designers,

549
00:44:53,460 --> 00:44:56,340
but it is definitely more aimed at developers.

550
00:45:01,080 --> 00:45:07,100
I have written a couple of articles about accessibility in the web development lifecycle,

551
00:45:07,100 --> 00:45:10,200
I talked a little bit about what to do with design.

552
00:45:10,520 --> 00:45:13,920
I do have a blog post on design as well.

553
00:45:13,920 --> 00:45:18,600
But yeah, so have a look at the resources section
of our website.

554
00:45:20,200 --> 00:45:25,620
[Attendee]: If there was one thing that you would say, or that mostly pops up,

555
00:45:25,640 --> 00:45:29,760
like I know know that everything that you do is important as far as accessibility,

556
00:45:29,760 --> 00:45:35,420
but is there one thing that stands out more, like even if you said if you do one thing,

557
00:45:35,440 --> 00:45:37,740
what would you say that would be?

558
00:45:38,000 --> 00:45:40,000
[Gian]: Make your site keyboard accessible.

559
00:45:41,680 --> 00:45:44,120
Because if your site is keyboard accessible, then

560
00:45:44,640 --> 00:45:48,840
at least, theoretically, all the features will be available to assistive technologies.

561
00:45:48,840 --> 00:45:52,060
They might not be read out properly, 
but at least they are all there.

562
00:45:53,000 --> 00:45:59,080
[Attendee]: You mentioned earlier that using HTML5 form elements would not be a good idea

563
00:45:59,080 --> 00:46:07,640
with regards to accessibility. Are there any other HTML elements or HTML5 tags?

564
00:46:08,080 --> 00:46:10,260
[Gian]: So, I'm glad that you said that.

565
00:46:10,280 --> 00:46:16,800
So, definitely use HTML5. HTML5 is fantastic.

566
00:46:16,800 --> 00:46:23,160
It has some problems, but you can't rely on HTML5 to meet WCAG 2 for you.

567
00:46:23,160 --> 00:46:29,180
So a lot of people for example ...
one of the requirements in WCAG 2 is that you need to

568
00:46:29,760 --> 00:46:33,820
indicate where your users have not completed a field.

569
00:46:34,440 --> 00:46:41,520
If you just rely on the required option in HTML5, then it will just pop up and then just disappear,

570
00:46:41,520 --> 00:46:43,900
that's probably what this guy has been dealing with.

571
00:46:44,320 --> 00:46:49,300
You can use HTML5,
and then use that required equals required,

572
00:46:49,320 --> 00:46:55,140
but then you also need to code in, you know,
this field is missing information.

573
00:46:55,160 --> 00:47:03,300
[Attendee]: But like, is there any tags within HTML5 that you wouldn't say like,

574
00:47:03,320 --> 00:47:09,280
wouldn't be like recommended as accessible, because I know that you where talking about the form element

575
00:47:09,280 --> 00:47:15,600
that like with the form tags, like HTML5, that would cause like accessibility problems.

576
00:47:16,080 --> 00:47:18,640
So, it's ...

577
00:47:24,000 --> 00:47:29,120
There is a factsheet on HTML5 that I've been told is out of date. So I haven't looked at it lately.

578
00:47:30,480 --> 00:47:35,640
One of the things that I disagree with HTML5 is the removal of the summary attribute in tables.

579
00:47:36,200 --> 00:47:43,880
But what I would say in general is anything that you can do in HTML5 that you can't do in HTML 4

580
00:47:44,200 --> 00:47:52,600
you need to code that in, separately, until the browsers have a better way of interpreting HTML5 elements.

581
00:47:55,280 --> 00:47:58,960
Placeholder is also another problem.
It's how people use it.

582
00:47:59,360 --> 00:48:04,160
So, a lot of people, instead of having a field label,
a visible field label,

583
00:48:04,160 --> 00:48:08,720
will put the field label as a placeholder using HTML5.

584
00:48:09,120 --> 00:48:12,900
That's not the technical way you should use it.
It's also incredibly inaccessible.

585
00:48:13,360 --> 00:48:17,600
So it's more how people are applying HTML5
than HTML5 itself.

586
00:48:20,040 --> 00:48:21,440
Any other questions?

587
00:48:22,200 --> 00:48:25,200
[Attendee]: I have a question about image size,
because you mentioned zooming in.

588
00:48:25,200 --> 00:48:32,040
So, but if you're actually trying to scale for devices, how do you go about that?

589
00:48:32,040 --> 00:48:37,420
Because you don't want too large of an image because it will use up data, versus the ability to zoom.

590
00:48:42,240 --> 00:48:48,240
[Gian]: You just have to be very careful with breakpoints. And you need to be ... you need to do a lot of testing.

591
00:48:51,920 --> 00:48:57,720
You should really, when you're designing a responsive site, design each breakpoint.

592
00:48:58,200 --> 00:49:05,380
So, design at the desktop size, design at the nine sixty by seven sixty eight or whatever,

593
00:49:05,400 --> 00:49:09,980
and know that's how your site is going to break
at those points.

594
00:49:10,320 --> 00:49:16,560
And that way you'll have a design that needs to be followed for certain sizes.

595
00:49:17,680 --> 00:49:23,140
[Attendee]: But I mean in terms of the data usage. Because you really don't want to put ...

596
00:49:23,160 --> 00:49:26,720
[Gian]: So I'm not technical, I'm not a developer ...

597
00:49:31,680 --> 00:49:33,640
... I don't know how that would work, actually.

598
00:49:34,320 --> 00:49:36,540
It could be something that you ...

599
00:49:38,280 --> 00:49:44,400
it depends on what people might ... like you might know what images that people zoom in on. On certain content.

600
00:49:45,960 --> 00:49:53,320
[Attendee]: There are new picture elements. I think the picture element is for more art direction.

601
00:49:53,320 --> 00:49:58,040
But the source that you can actually use on images,
on the image tag,

602
00:49:58,040 --> 00:50:02,540
will let you supply a different image
for different screen resolutions.

603
00:50:02,560 --> 00:50:09,520
I don't know if it detects what kind of bandwidth
your users are using,

604
00:50:09,520 --> 00:50:13,320
but at least it can detect what screen resolution
they are using.

605
00:50:15,040 --> 00:50:19,180
[Attendee]: Right, but if you want to zoom ...
so the thing is that zooming ...

606
00:50:19,200 --> 00:50:24,980
so you have a source that is set for a certain device width, it would serve up a smaller image.

607
00:50:30,960 --> 00:50:35,100
[Gian]: Good. Great.
I'm glad someone figured that one out.

608
00:50:53,360 --> 00:50:57,060
[Gian]: It also depends on the content
that is in the image.

609
00:50:57,080 --> 00:51:02,700
If it's an automated image of a couple having coffee, then people aren't likely to zoom in on it.

610
00:51:02,720 --> 00:51:10,220
If its your logo or mission statement, something like that, maybe that would inform the site.

611
00:51:14,640 --> 00:51:21,700
[Attendee]: Yeah, I was wondering, this is all most concerning mobile devices, phone, tablets,

612
00:51:21,720 --> 00:51:26,480
but there's now, around the corner,
the wearable devices too?

613
00:51:26,480 --> 00:51:27,060
[Gian]: Yep.

614
00:51:27,080 --> 00:51:32,860
[Attendee]: And do you have an opinion or vision on that? And how to deal with that?

615
00:51:32,880 --> 00:51:36,940
[Gian]: Yeah, if my job wasn't interesting before, it is going to be soon.

616
00:51:40,520 --> 00:51:45,140
Wearables are very interesting.

617
00:51:46,440 --> 00:51:51,880
They ... I think that people will have to accept that there are going to be some wearables that are not ...

618
00:51:52,680 --> 00:51:54,440
... going to be useful to them.

619
00:51:55,160 --> 00:52:02,980
So, for example, someone who's deaf might find a wrist, a smart watch

620
00:52:02,980 --> 00:52:07,560
very helpful, vibrates when you get an email,
vibrates when you get a call, that kind of stuff.

621
00:52:07,560 --> 00:52:09,920
But I think there's probably ...

622
00:52:11,240 --> 00:52:13,200
... just going to have to be an acceptance
that a smart watch

623
00:52:13,200 --> 00:52:16,420
is not necessarily going to be all that helpful
to a screen reader user.

624
00:52:17,440 --> 00:52:18,180
Yes please ...

625
00:52:18,480 --> 00:52:25,640
[Attendee]: Actually, you can use Apple Watch.
There are people who are working on,

626
00:52:26,240 --> 00:52:30,340
I know of one instance where a company in South Korea is working on a watch with a small

627
00:52:30,360 --> 00:52:37,100
braille display that pairs with your iPhone so your iPhone memorizes speech output with VoiceOver.

628
00:52:37,520 --> 00:52:43,780
[Gian]: Yeah, and I mean I see a lot of people with vision impairments just hang their braille display

629
00:52:43,800 --> 00:52:47,300
around their neck so it kind of operates in that way anyway.

630
00:52:47,840 --> 00:52:49,080
You wanted to say something?

631
00:52:49,080 --> 00:52:55,120
[Attendee]: I was just going to ask a question based off of what he was saying about wearable devices.

632
00:52:55,120 --> 00:52:59,780
I was wondering, can some wearable devices
be coded in HTML5

633
00:52:59,800 --> 00:53:03,240
or would it just depend on the wearable device?

634
00:53:03,240 --> 00:53:05,000
[Gian]: I think it would depend on the wearable device.

635
00:53:05,000 --> 00:53:13,400
I would expect that at some point there would be wearables that are HTML, that show websites.

636
00:53:13,400 --> 00:53:18,460
[Attendee]: Is there any country that you've noticed that is in the forefront,

637
00:53:18,480 --> 00:53:22,860
compared to others, with regards to accessibility?

638
00:53:22,880 --> 00:53:23,560
[Gian]: No.

639
00:53:23,560 --> 00:53:24,640
[Laughter]

640
00:53:24,640 --> 00:53:29,680
[Gian]: Look, Australia was really good
about five years ago,

641
00:53:29,680 --> 00:53:32,280
they released this thing called the National Transition Strategy

642
00:53:32,320 --> 00:53:38,560
which said basically if you don't meet your accessibility requirements, such as WCAG 2,

643
00:53:38,560 --> 00:53:42,800
we're going to turn your domain off. So, that was a pretty serious thing

644
00:53:42,800 --> 00:53:48,140
They never actually did that, and then people actually realized that they weren't going to do that,

645
00:53:48,160 --> 00:53:51,380
so people kind of gave up on accessibility.

646
00:53:52,400 --> 00:53:57,200
In a lot of ways, 
the U.S. understands accessibility a lot more,

647
00:53:57,200 --> 00:54:03,420
in terms of things like the need for automated accessibility testing tools,

648
00:54:03,440 --> 00:54:08,760
the need for a university developing policies and procedures, things like that.

649
00:54:08,800 --> 00:54:13,680
We're still at the stage in Australia, we meet with universities and say,

650
00:54:13,680 --> 00:54:16,640
"so let me explain what web accessibility is."

651
00:54:16,640 --> 00:54:23,400
So the U.S. is leading the way,
and one of the reasons is litigation.

652
00:54:25,120 --> 00:54:27,640
[Gian]: Yes ... what's your name, sorry?

653
00:54:27,680 --> 00:54:28,340
[Attendee]: Me?

654
00:54:28,360 --> 00:54:28,920
[Gian]: Yes.

655
00:54:28,920 --> 00:54:29,460
[Attendee]: Dan.

656
00:54:29,460 --> 00:54:31,440
[Gian]: Okay, Dan.

657
00:54:35,140 --> 00:54:39,980
[Attendee]: The problem in the U.S. is Congress will pass laws or there'll be executive orders,

658
00:54:40,320 --> 00:54:44,960
and then the Justice Department steps in and say we need to get public comment

659
00:54:44,960 --> 00:54:48,800
or we need to do rule making and
the things get delayed for years.

660
00:54:49,220 --> 00:54:54,280
[Gian]: Well, I think it was very interesting that the Department of Justice is sending out letters

661
00:54:54,480 --> 00:55:01,360
of accessibility compliance referencing WCAG 2, even though WCAG 2 is not on the law books.

662
00:55:02,080 --> 00:55:07,520
It's still Section 508, but in reality, you need to be following WCAG 2.

663
00:55:07,520 --> 00:55:11,120
Which, of course, is a problem because
it doesn't handle mobile very well

664
00:55:12,000 --> 00:55:18,460
[Attendee]: About making a business case for accessibility in a company,

665
00:55:18,480 --> 00:55:31,040
where does accessibility provided the biggest benefits? Outside of what we kind of know the obvious?

666
00:55:31,040 --> 00:55:38,620
With SEO or anything else we could push ...
you know it could help us out in this other

667
00:55:39,280 --> 00:55:43,680
[Gian]: So, definitely, Google rankings.

668
00:55:43,680 --> 00:55:49,920
So, not so much optimization, but if you have an accessible site,

669
00:55:49,920 --> 00:55:53,940
it's going to be able to be scanned better by Google.

670
00:55:54,640 --> 00:55:59,720
So, for example, and it's going to be
ranked higher by Google.

671
00:55:59,760 --> 00:56:07,560
So, sites that contain videos that have transcripts earn 16% more revenue

672
00:56:07,600 --> 00:56:11,000
than sites that have video without transcripts.

673
00:56:11,040 --> 00:56:15,020
That's basically because Google could search the transcript and rank them higher.

674
00:56:15,040 --> 00:56:17,120
Whereas Google cannot search a video.

675
00:56:17,920 --> 00:56:23,520
Completion of a video, like watching it to its end, doubles of that video has captions.

676
00:56:24,320 --> 00:56:32,360
One of the things the BBC found out was eighty percent of people who turn on captions,

677
00:56:32,400 --> 00:56:34,560
are not deaf or hard of hearing.

678
00:56:35,120 --> 00:56:37,000
They call it the Broadchurch effect.

679
00:56:37,440 --> 00:56:39,660
It's basically THL Broadchurch.

680
00:56:40,000 --> 00:56:43,520
The accent was so strong, half of England couldn't understand what they were saying.

681
00:56:44,000 --> 00:56:50,080
But it's also helping, like, I spent ten minutes looking at my Facebook page this afternoon.

682
00:56:50,080 --> 00:56:55,600
And I was in Starbucks, and I did want to play a video and I wasn't going to watch video unless it had captions.

683
00:56:56,400 --> 00:57:01,600
So, there's a whole lot of ... and also,
a page that has video,

684
00:57:01,600 --> 00:57:06,000
will be ranked much higher by Google than a page that does not have video.

685
00:57:06,160 --> 00:57:09,240
So, there's a whole bunch of things around that.

686
00:57:12,800 --> 00:57:20,640
[Attendee]: Do you have a good example of a site that gives users choice about their experience?

687
00:57:20,640 --> 00:57:27,820
For example, what kind of contrast they would like to have when visiting today?

688
00:57:28,640 --> 00:57:30,920
[Gian]: We worked on ...

689
00:57:30,960 --> 00:57:33,960
Anti-Discrimination Commission Queensland,

690
00:57:34,000 --> 00:57:40,440
and I believe they have options for color contrast
and text size.

691
00:57:50,400 --> 00:57:55,180
And they ... also won an Australian Web Award.

692
00:57:56,720 --> 00:58:00,320
[Attendee]: I'm working with a vendor and I'm trying to explain this concept,

693
00:58:00,320 --> 00:58:05,600
and they couldn't get the idea.
And I thought if I could just show them one.

694
00:58:08,500 --> 00:58:11,740
[Gian]: We did some work with ...

695
00:58:11,740 --> 00:58:17,040
... Griffith University in Queensland, and their corporate colors are red and white.

696
00:58:17,040 --> 00:58:24,940
And they decided that instead of just giving users the option to increase the color contrast,

697
00:58:24,960 --> 00:58:29,040
that they would give users the option to choose they're own color contrast,

698
00:58:29,040 --> 00:58:33,600
and they found that, I think it was something like eighty-two percent of people

699
00:58:33,600 --> 00:58:38,760
who used the color contrast feature, 
actually reduced color contrast.

700
00:58:39,760 --> 00:58:43,280
So ... I'm not sure this is going to work.

701
00:58:52,160 --> 00:58:57,700
So, at the top you've got your colors, so you can choose different colors,

702
00:58:57,700 --> 00:58:59,340
you've got text size,

703
00:59:00,320 --> 00:59:02,760
and you've also got BrowseAloud

704
00:59:02,760 --> 00:59:06,020
as I've mentioned, we're no longer a reseller,
but it is a great product.

705
00:59:06,600 --> 00:59:11,020
It allows you to basically, it's a screen reader, it's a screen magnifier,

706
00:59:12,440 --> 00:59:16,180
it changes color contrast, everything, so there's a whole lot of things it can do.

707
00:59:18,400 --> 00:59:21,880
[Attendee]: And that is accessed with the button in the upper right?

708
00:59:21,880 --> 00:59:25,040
[Gian]: Yeah, this thing. And you can pick it up, and it stays ...

709
00:59:25,040 --> 00:59:25,920
[Attendee]: And it's sticky?

710
00:59:26,360 --> 00:59:28,580
[Gian]: Yep, it's sticky.

711
00:59:35,440 --> 00:59:39,800
[Attendee]: So you're in fact creating almost a kind of white-label effect for every user.

712
00:59:41,480 --> 00:59:45,560
[Gian]: Yes, so this is the like, text version only.

713
00:59:48,360 --> 00:59:52,880
And then, um, my volume is off ...

714
00:59:55,800 --> 01:00:03,460
So it reads aloud and ... as soon as the ... 
I can't turn my volume on

715
01:00:04,120 --> 01:00:08,940
for some reason, but it is reading it aloud. And it's zooming at the top as well.

716
01:00:08,960 --> 01:00:13,080
So yeah, it's a lot of things that Browsealoud can do. It's aimed

717
01:00:14,040 --> 01:00:17,880
really at people with moderate vision impairment, so even though it has a screen reader,

718
01:00:17,880 --> 01:00:20,560
it's not for people who are completely blind.

719
01:00:20,800 --> 01:00:27,200
And it's also aimed at people with cognitive disabilities.

720
01:00:27,560 --> 01:00:33,380
So they've found that comprehension of a web page, they did a study, comprehension of a web page

721
01:00:33,400 --> 01:00:38,840
increased by eighteen percent when people used Browsealoud versus just reading a web page.

722
01:00:39,760 --> 01:00:43,940
And it's quite useful because you don't have to identify as a person with a disability

723
01:00:43,940 --> 01:00:47,780
and go off and find an assistive technology. If that button is on your web site,

724
01:00:47,780 --> 01:00:52,580
people might play with it and find that it helps them without having to go through that process.

725
01:00:52,760 --> 01:00:56,700
And it also is aimed at people with English
as a second language,

726
01:00:56,720 --> 01:00:59,940
so it can translate into a bunch of different languages as well.

727
01:01:01,360 --> 01:01:02,460
[Attendee]: What's it called?

728
01:01:02,480 --> 01:01:04,680
[Gian]: BrowseAloud.

729
01:01:07,080 --> 01:01:11,640
So yes, it's got a whole bunch of highlight things and ... I haven't checked the new one

730
01:01:11,640 --> 01:01:14,240
so I can't tell you all the things it can do.

731
01:01:14,960 --> 01:01:17,220
[Attendee]: Is that something that you have to pay for?

732
01:01:17,240 --> 01:01:18,420
[Gian]: Yes.

733
01:01:19,720 --> 01:01:23,800
If you want more information, feel free to contact me.

734
01:01:23,800 --> 01:01:28,440
Because we just implemented on the rudenman rights web site, the disability rights Washington,

735
01:01:28,440 --> 01:01:30,120
we just built them a website.

736
01:01:30,120 --> 01:01:33,100
So we can get you in contact with the right people.

737
01:01:35,660 --> 01:01:36,960
Any other questions?

738
01:01:37,160 --> 01:01:40,080
[Attendee]: Does that work as a plug-in then?

739
01:01:40,100 --> 01:01:44,060
[Gian]: It's basically JavaScript code, that sits on top of your web site.

740
01:01:47,520 --> 01:01:49,520
[Gian]: Any other questions?

741
01:01:50,780 --> 01:01:52,280
Well, thank you very much.

742
01:01:52,560 --> 01:01:59,440
[Applause]

