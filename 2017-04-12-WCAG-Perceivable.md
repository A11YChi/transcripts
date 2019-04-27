# WCAG 2.0 - Perceivable
## Dennis Deacon - Wednesday, April 12, 2017
[Source recording](https://www.youtube.com/watch?v=t4PY8mnShm4&t=12s)

**[Dennis]:** So tonight, we're talking about Perceivable: WCAG 2.0 for designers and developers. This is the URL for this presentation. It's there, live now. And you can always go back there after this event. This URL will also be on the final slide, so if you don't get to write it all down now, you can write it down then.

I originally had scheduled this to cover all of WCAG in one event.

**[Laughter]**

**[Dennis]:** Oh my goodness, I don't know how I am going to get this into one hour. So the way I foresee this is ... and we'll get into it more as we get into some of the slides, but WCAG is like the World Book encyclopedia or Wikipedia it's huge and there's no way that you're ever going to know everything but as long as you get the high level details and you know where everything is, you can always refer to it.

So hopefully what you'll do is walk away today having a better understanding at least with regards to Perceivable, the first principle. What's involved, what's covered, and then you'll be able to go out and do some further research on your own.

So tonight's agenda ...what is WCAG, the first principal, which is Perceivable, and within there we have text alternatives for non-text content, alternative for time-based media, does anyone know what time-based media would be?

**[Attendee]:** Video

**[Dennis]:** Video

**[Attendee]:** Carousels

**[Dennis]:** Awww...

**[Laughter]**

**[Dennis]:** Seth, show this man the door.

**[Laughter]**

**[Dennis]:** No, just kidding. No, that would not be a time-based ... but I can see how you would think that though, so, I'm not going to totally discredit that.

**[Attendee]:** [mumbled]

**[Dennis]:** That's an interesting ... no ... that's covered by WCAG, but not in Perceivable. So just so you know, we are going to touch upon that. I could tell you stories about time out sessions, oh my goodness, but that's not included as part of time-based media.

Okay, flexible content, contrast of content, the other principles will be covering we're hopefully going to cover operable which is very ... more heavily around developers as well as UX. We hope to have that scheduled for June.

Understandable probably this fall, maybe September. And then Robust. Robust has one item, and I wouldn't ask you all to come out just for one item, so what we'll do for that is will cover Robust, and then we'll summarize what we've you know covered with all these other sessions.

So, how will this be presented ... WCAG is very dry. If you read it you're going to all asleep and I'm just tell you right now it's very text heavy, very text-based. So, and there's a lot of bullets so don't fear the bullets I know you're in Chicago but don't fear the bullets. There's going to be plenty of code examples, plenty of design examples, and plenty of tools and resources in this presentation.

And of course plenty of my tacky jokes ...

[Video of Human League's "Human" plays]

**[Dennis]:** Because I'm human of course, so...

64
00:04:07,860 --> 00:04:10,340
So what is WCAG 2.0?

65
00:04:12,040 --> 00:04:13,960
This is the official definition.

66
00:04:15,180 --> 00:04:21,380
It's a definition of how to make web content more accessible to people with a wide range of disabilities,

67
00:04:21,380 --> 00:04:28,840
including visual, auditory, physical, speech, cognitive, language, learning and neurological.

68
00:04:30,660 --> 00:04:32,660
That's the whole mouthful.

69
00:04:34,420 --> 00:04:37,420
It's made up of four principles

70
00:04:37,420 --> 00:04:40,620
which tonight you're here for Perceivable, but there's also

71
00:04:40,620 --> 00:04:42,620
Operable, Understandable and Robust.

72
00:04:44,120 --> 00:04:46,980
The Guidelines, which support those principles

73
00:04:46,980 --> 00:04:52,720
which there's 12 of them, those are the basic goals that you should work towards.

74
00:04:53,180 --> 00:04:56,440
The Success Criteria which there's sixty one of them ...

75
00:04:56,440 --> 00:05:00,300
as you can see this is multiplying as we go deeper and deeper.

76
00:05:00,540 --> 00:05:05,520
but there's three levels of conformance for the success criteria.

77
00:05:05,520 --> 00:05:08,120
So I just want to stop and talk a little bit about that.

78
00:05:09,020 --> 00:05:13,580
If you think of it, if you have a website, and you add alt text,

79
00:05:14,000 --> 00:05:16,000
your site is now more accessible.

80
00:05:16,220 --> 00:05:20,640
Is it totally accessible? No, but it's more accessible to a degree.

81
00:05:20,640 --> 00:05:27,700
So think of these conformance levels, A, AA and AAA as levels of accessibility.

82
00:05:28,680 --> 00:05:37,520
Level A is very basic. I mean literally alt text, color contrast, things like that.

83
00:05:39,520 --> 00:05:47,740
Section 508, before it was refreshed was closer to Level A than anything else.

84
00:05:47,740 --> 00:05:53,260
It has been refreshed now to be more compliant with Level AA.

85
00:05:53,580 --> 00:05:59,860
AA conformance is actually the world standard now for accessibility.

86
00:06:01,500 --> 00:06:07,400
The airlines in the United States are mandated to be WCAG 2 AA compliant.

87
00:06:08,000 --> 00:06:16,580
Most businesses like your financial institutions, your higher ed institutions,

88
00:06:16,580 --> 00:06:19,600
they need to be Level AA compliant.

89
00:06:20,020 --> 00:06:22,460
Triple A ... good luck with that.

90
00:06:23,400 --> 00:06:24,480
When you see some ...

91
00:06:24,480 --> 00:06:28,200
and so what we're going to do tonight is I'm going to cover A and AA.

92
00:06:28,200 --> 00:06:30,200
I'm going to breeze through AAA,

93
00:06:30,840 --> 00:06:34,640
making probably snide remarks as I go along.

94
00:06:34,640 --> 00:06:36,640
Because some of them are just ...

95
00:06:38,200 --> 00:06:40,740
they're not ridiculous, but they're ...

96
00:06:40,740 --> 00:06:43,760
when you think about your work, they're almost impossible.

97
00:06:43,760 --> 00:06:48,300
You might be able to do a few on a page but site-wide forget about it.

98
00:06:49,220 --> 00:06:54,540
And then techniques. There's 383 techniques to be accessible.

99
00:06:55,600 --> 00:06:58,900
So as you can imagine now with all that information

100
00:06:58,900 --> 00:07:01,680
WCAG 2 can be overwhelming.

101
00:07:01,680 --> 00:07:04,620
I mean if you printed WCAG out

102
00:07:04,620 --> 00:07:06,620
and you can, I don't advise it

103
00:07:06,620 --> 00:07:09,500
we need all the trees we can have...

104
00:07:09,500 --> 00:07:13,140
WCAG itself is 36 pages,

105
00:07:14,040 --> 00:07:20,160
how to meet accessibility, how to meet WCAG is 44 pages ... additional.

106
00:07:21,240 --> 00:07:26,860
Understanding WCAG, this separate section, is 230 pages.

107
00:07:28,080 --> 00:07:34,040
Techniques and failures to meet WCAG is 780 pages.

108
00:07:34,040 --> 00:07:36,960
That's a total of 1090 pages,

109
00:07:37,880 --> 00:07:39,140
printed pages,

110
00:07:39,140 --> 00:07:41,400
that you need to learn by Friday.

111
00:07:42,500 --> 00:07:44,220
Yeah that's not going to happen, trust me.

112
00:07:44,220 --> 00:07:50,120
So again ... in tonight's session, you're going to learn on a high level what's involved,

113
00:07:50,120 --> 00:07:53,200
and then you're going to be able to take away some of those learnings,

114
00:07:53,200 --> 00:07:57,700
as well as being able to delve further and as you go through your work.

115
00:07:59,440 --> 00:08:02,540
Yes there's a WCAG 2.1, believe it or not.

116
00:08:02,540 --> 00:08:05,460
It just came out February 28 of this year.

117
00:08:06,660 --> 00:08:11,880
It's not a new version, it just adds to 2.0.

118
00:08:13,760 --> 00:08:17,160
It basically focuses on three different areas:

119
00:08:17,500 --> 00:08:19,760
users with low vision

120
00:08:20,600 --> 00:08:23,860
users with cognitive or learning disabilities,

121
00:08:23,860 --> 00:08:26,600
and accessibility of mobile devices.

122
00:08:26,600 --> 00:08:29,680
WCAG 2.0 came out in 2008.

123
00:08:30,620 --> 00:08:33,520
Smartphones were just starting to catch on.

124
00:08:34,360 --> 00:08:38,980
So WCAG 2 really doesn't cover mobile ... at all.

125
00:08:38,980 --> 00:08:41,120
We've had to adapt it, you know.

126
00:08:41,120 --> 00:08:43,480
Think about how does this apply to mobile.

127
00:08:43,980 --> 00:08:49,300
So WCAG 2.1 tries to start addressing some of those items.

128
00:08:50,320 --> 00:08:53,940
We're going to cover this at a very high level.

129
00:08:53,940 --> 00:08:57,840
We're not going to go too deep, because many of these things are brand new,

130
00:08:58,340 --> 00:09:00,600
most of them are just proposed.

131
00:09:00,900 --> 00:09:04,220
When you see some of them, you'll say well how are we going to do that?

132
00:09:04,220 --> 00:09:11,180
So realize that while this is just come out, you know, think about a year or two before it starts to gain steam

133
00:09:11,180 --> 00:09:14,060
in that you'll actually start applying this.

134
00:09:15,700 --> 00:09:18,440
So WCAG 2.0 in baby steps.

135
00:09:19,280 --> 00:09:21,820
First of all we have the four principles as stated,

136
00:09:21,820 --> 00:09:26,440
we have Perception, Operable, Understanding and Robust.

137
00:09:26,740 --> 00:09:32,220
If you ever need to remember what the principals are, they spell out POUR.

138
00:09:34,300 --> 00:09:38,120
This is something that's been drilled into my head and, to be honest,

139
00:09:38,120 --> 00:09:44,640
I've never ... I mean it helps, I mean, "U" okay, what's "U"? Usable? No that's not it.

140
00:09:45,800 --> 00:09:49,180
Typically "U" and "R" are the ones I can't remember.

141
00:09:49,960 --> 00:09:52,440
But you know, Perception and Operable I can sort of get.

142
00:09:52,440 --> 00:09:57,460
But we're going to be covering just Perception in this particular event.

143
00:09:58,140 --> 00:09:59,580
So Perception...

144
00:10:01,240 --> 00:10:03,360
information and user interface components

145
00:10:03,360 --> 00:10:05,360
must be presentable to users

146
00:10:05,360 --> 00:10:07,360
in ways that they can perceive.

147
00:10:07,360 --> 00:10:10,040
So what are, what is perception?

148
00:10:10,040 --> 00:10:12,040
What are ... you know ...

149
00:10:13,300 --> 00:10:18,380
what are the things that you would think applied to something being perceived?

150
00:10:18,860 --> 00:10:19,740
Anyone?

151
00:10:22,300 --> 00:10:24,300
[Attendee] Based on the sense...

152
00:10:24,300 --> 00:10:27,220
[Dennis] Ok, so the senses

153
00:10:28,340 --> 00:10:30,800
You must have seen my slides, so ... [laughter]

154
00:10:30,800 --> 00:10:32,800
You were looking at them on the phone, I know...

155
00:10:33,380 --> 00:10:36,060
So sight ... vision ... yes.

156
00:10:37,060 --> 00:10:38,760
Hearing ... auditory.

157
00:10:38,760 --> 00:10:41,120
Ok, so if you're watching a video,

158
00:10:41,780 --> 00:10:44,980
if you can't hear, you got to have those captions or else

159
00:10:46,040 --> 00:10:48,260
now you do to see someone flailing their arms

160
00:10:48,260 --> 00:10:50,260
and you have no idea why.

161
00:10:50,980 --> 00:10:51,560
Touch.

162
00:10:52,100 --> 00:10:53,500
So here's an interesting thing.

163
00:10:53,500 --> 00:10:55,240
You think well we don't have ... how you know ...

164
00:10:55,240 --> 00:10:59,860
I understand touchscreen but how does touch play ... enter into this?

165
00:11:00,300 --> 00:11:04,560
Many blind people, true, exactly ...

166
00:11:04,560 --> 00:11:10,480
Many blind people use what's called a Refreshable Braille keyboard.

167
00:11:10,960 --> 00:11:12,960
So basically what happens is ...

168
00:11:13,420 --> 00:11:17,480
As they refresh the screen, that ... you know they're blind so they don't use a monitor,

169
00:11:17,940 --> 00:11:19,940
they feel the content ...

170
00:11:20,720 --> 00:11:24,340
as you know Braille is a bunch of dots, raised dots

171
00:11:24,780 --> 00:11:30,840
and these raised dots refresh as he or she navigates the page.

172
00:11:30,840 --> 00:11:35,640
They feel it and then they'll you know they'll do whatever data entry they need to do

173
00:11:35,640 --> 00:11:39,420
and then ... they'll read some more by reading the keyboard.

174
00:11:40,060 --> 00:11:45,980
By the way those things are like fifteen hundred dollars ... on sale. It's ridiculous.

175
00:11:47,360 --> 00:11:52,020
Smell ... we don't have smell-o-vision on digital ... yet,

176
00:11:52,020 --> 00:11:54,020
and we don't have taste.

177
00:11:54,020 --> 00:11:59,940
So these three senses are key to the digital landscape.

178
00:11:59,940 --> 00:12:10,300
So in Perception the guidelines are, text alternatives, time-based media, adaptable and distinguishable.

179
00:12:10,940 --> 00:12:12,940
So text alternatives ...

180
00:12:13,700 --> 00:12:17,220
Provide text alternatives for any non-text content.

181
00:12:19,160 --> 00:12:22,380
Can anyone name non-text content?

182
00:12:23,400 --> 00:12:25,400
[Attendee] ... photos ... videos ...

183
00:12:26,840 --> 00:12:28,620
[Dennis] Photos, videos ... ok ...

184
00:12:30,300 --> 00:12:31,220
... clipart ...

185
00:12:32,580 --> 00:12:36,060
... there's going to be a lot of cats tonight, ok,  just so you know.

186
00:12:37,500 --> 00:12:41,220
Even animated ones, I apologize right now.

187
00:12:41,520 --> 00:12:46,840
And they're jaggy, they got the jaggy, so if you're looking for high-quality clipart forget about it,

188
00:12:46,840 --> 00:12:48,420
you came to the wrong place.

189
00:12:49,300 --> 00:12:50,960
Photos, to your point.

190
00:12:52,320 --> 00:12:56,060
Charts ... imagine what's the alt text for a chart.

191
00:12:58,540 --> 00:13:00,840
Audio ... audio players.

192
00:13:02,020 --> 00:13:03,700
There's my guy ...

193
00:13:06,540 --> 00:13:07,740
... super jaggies.

194
00:13:09,360 --> 00:13:12,620
Video, such as the giraffe.

195
00:13:14,260 --> 00:13:15,580
And maps.

196
00:13:15,580 --> 00:13:21,280
At United Airlines, one of our infamous ones are the terminal maps.

197
00:13:22,240 --> 00:13:27,800
We countered that by putting an invisible table on the page with the same information.

198
00:13:28,880 --> 00:13:30,080
It works.

199
00:13:31,420 --> 00:13:32,540
So techniques.

200
00:13:32,540 --> 00:13:38,480
On a high level, images that communicate information must provide a text alternative.

201
00:13:40,100 --> 00:13:45,860
Images that are for design purposes only do not need to provide a text alternative.

202
00:13:46,980 --> 00:13:52,800
So there's two methods of implementing images on the web ... primary methods.

203
00:13:52,800 --> 00:13:56,180
I only say that because Seth will probably say, "what about that," you know,

204
00:13:57,200 --> 00:13:58,680
hadn't thought about that.

205
00:13:58,680 --> 00:14:01,920
But you have inline images you have background images.

206
00:14:03,540 --> 00:14:05,540
Okay so inline images.

207
00:14:06,800 --> 00:14:09,280
Inline images for all you non-coders

208
00:14:10,480 --> 00:14:15,520
are images where the code references that image directly on the page, directly in the code.

209
00:14:17,080 --> 00:14:24,480
You have an image tag, you can also have an SVG tag which is gaining prominence nowadays.

210
00:14:25,580 --> 00:14:27,580
So the inline image tag.

211
00:14:28,840 --> 00:14:35,220
All inline image instances must provide an alt attribute. And I'm going to hammer this ...

212
00:14:35,700 --> 00:14:41,100
Every inline image must have an alt attribute.

213
00:14:41,760 --> 00:14:45,500
The value of that attribute depends on the image's context.

214
00:14:46,360 --> 00:14:49,040
Ok, so if you sweep your sites ...

215
00:14:49,960 --> 00:14:55,320
if you have images, inline images that don't have an alt attribute, add it.

216
00:14:56,100 --> 00:14:58,300
We'll worry about the value in a little bit.

217
00:15:00,400 --> 00:15:04,620
So here's an image without alt attribute.

218
00:15:05,040 --> 00:15:06,320
You have a cat here.

219
00:15:07,300 --> 00:15:11,280
Here's our code for it, just the reference to the cat image.

220
00:15:11,920 --> 00:15:19,060
So a screen reader is going to read graphic I M G / cat dot j p g.

221
00:15:20,600 --> 00:15:25,760
Well, thankfully here, the filename gives some sense of what this image might be.

222
00:15:25,760 --> 00:15:27,260
But that's not always the case.

223
00:15:27,260 --> 00:15:37,140
We've seen ... we've all seen image names that are 256 characters in cryptic code from a CMS.

224
00:15:38,100 --> 00:15:44,880
So don't do this because this really frustrates screen reader users.

225
00:15:45,540 --> 00:15:49,440
Okay, here's an example of an image with alternative text.

226
00:15:52,320 --> 00:15:56,860
Here's the alt attribute, there's the value, a cat looking out the window.

227
00:15:58,560 --> 00:16:02,840
A screen reader would read ... graphic a cat looking out the window.

228
00:16:03,680 --> 00:16:05,180
Very self-explanatory.

229
00:16:05,180 --> 00:16:09,280
Fairly easy to do. This is the low-hanging fruit of all accessibility.

230
00:16:09,280 --> 00:16:15,960
If you do this, you have already reached first base rounding towards second.

231
00:16:17,300 --> 00:16:19,760
Hopefully you're all into baseball like I am.

232
00:16:20,920 --> 00:16:25,080
Here's an example of an image with no alternative text description.

233
00:16:25,080 --> 00:16:31,800
It's basically design. There's no ... it's not communicating anything in this instance.

234
00:16:32,840 --> 00:16:35,980
Alt ... quote quote. It's empty value.

235
00:16:36,300 --> 00:16:38,540
What happens when the screen reader reaches that?

236
00:16:39,400 --> 00:16:41,080
It'll just skip over the image.

237
00:16:42,280 --> 00:16:44,320
That's exactly what we wanted to do.

238
00:16:44,320 --> 00:16:48,040
It's not ... it's there just for ... flair.

239
00:16:48,040 --> 00:16:50,740
Just for, you know, to enhance something.

240
00:16:50,740 --> 00:16:53,660
But it's not communicating anything uniquely.

241
00:16:54,700 --> 00:16:56,740
Okay, inline SVG.

242
00:16:57,240 --> 00:17:05,060
Two ways of implementing it. Either referencing it as an image and the image tag, or else in line SVG.

243
00:17:06,120 --> 00:17:11,020
So again, just like an inline image, just alt "Cat."

244
00:17:13,220 --> 00:17:19,080
Now if you have inline SVG, you got to figure out how to describe it.

245
00:17:19,080 --> 00:17:23,240
Because it doesn't actually have an alt attribute.

246
00:17:24,100 --> 00:17:26,520
So in this case we use aria-labeledby.

247
00:17:26,520 --> 00:17:31,900
ARIA is one of the hottest things for developers to use

248
00:17:32,720 --> 00:17:33,620
... overuse ...

249
00:17:33,620 --> 00:17:38,160
I just got ... again, it always happens, got out of the meeting today,

250
00:17:38,160 --> 00:17:42,380
someone recreated a table with divs,

251
00:17:43,880 --> 00:17:47,600
used ARIA every which way to make it, "yeah but look at the table!"

252
00:17:47,600 --> 00:17:49,180
Like it's not a table.

253
00:17:49,180 --> 00:17:51,180
There's no table tag.

254
00:17:52,060 --> 00:18:01,740
So in this case, you would have your SVG aria-labeledby the ID that actually contains the title

255
00:18:01,740 --> 00:18:05,640
and you do this because there's different ways to actually access this information.

256
00:18:06,080 --> 00:18:11,040
So it may seem a little bit duplicative but it's really not.

257
00:18:11,040 --> 00:18:13,040
It's really necessary at least today.

258
00:18:15,360 --> 00:18:17,360
CSS background images.

259
00:18:18,280 --> 00:18:20,620
So typically when you have a background image

260
00:18:22,180 --> 00:18:27,680
it's not communicating anything that needs to be communicated to assistive technology,

261
00:18:27,680 --> 00:18:29,120
like a screen reader.

262
00:18:30,040 --> 00:18:33,460
Okay, it doesn't offer any ...

263
00:18:34,280 --> 00:18:42,480
the background CSS, the background property for CSS does not offer any type of alternative text.

264
00:18:43,240 --> 00:18:51,920
So again you would just put imagery that is for more design not communicating information.

265
00:18:54,080 --> 00:18:59,720
As a remediation exercise which we did find ourselves doing at United,

266
00:19:00,220 --> 00:19:06,200
you can add either screen reader text or an aria-label on the container

267
00:19:06,200 --> 00:19:09,880
where that background image is and that will work.

268
00:19:11,820 --> 00:19:16,160
Who here knows what screen ... when i say screen reader text what screen reader text is?

269
00:19:16,620 --> 00:19:17,780
Raise your hand ...

270
00:19:18,880 --> 00:19:21,040
Ok, very few ...

271
00:19:21,040 --> 00:19:30,140
So screen reader text is text that's on the page, that's visibly hidden but available for assistive technology.

272
00:19:30,140 --> 00:19:34,760
And its really ... it's all using CSS to do this.

273
00:19:35,540 --> 00:19:43,580
So you might have something like this, you know, we have the i tag used for icons and imagery

274
00:19:43,580 --> 00:19:45,580
left and right on the web today.

275
00:19:46,940 --> 00:19:54,440
Within there you'd put a span with a class of visuallyhidden and let's say if it's the check mark,

276
00:19:55,080 --> 00:19:59,060
well nothing there says that it's that it means included,

277
00:19:59,540 --> 00:20:05,480
but here you can put the visually hidden text in there, it won't display, you'll still display your check mark,

278
00:20:05,980 --> 00:20:11,740
but it will be communicated to the assistive technology that this means included.

279
00:20:12,880 --> 00:20:20,240
This is a typical CSS code for this type of information it's really just taking it,

280
00:20:20,240 --> 00:20:28,160
putting it in line and you know, making it 1 pixel x 1 pixel and clipping it and doing all the various tricks

281
00:20:28,160 --> 00:20:30,760
to ensure that it's not displayed visually.

282
00:20:33,360 --> 00:20:34,980
aria-label

283
00:20:34,980 --> 00:20:37,940
So, again, if you got your container, you've got your background image,

284
00:20:37,940 --> 00:20:46,320
if you have to communicate something you can use
aria-label to provide that type of information.

285
00:20:48,080 --> 00:20:55,920
So now we learned how, let's talk about when when you would use alt text.

286
00:20:56,320 --> 00:20:58,780
This is a great resource by the W3C.

287
00:20:58,780 --> 00:21:03,160
Basically it is a decision tree. You go through these questions to ask yourself,

288
00:21:03,160 --> 00:21:08,240
in this context, does this make sense to add alt text or not?

289
00:21:09,780 --> 00:21:15,020
Let's see here, does this image contain text?

290
00:21:15,020 --> 00:21:24,240
So if the image contains text, you're going to want to add the text that's in that image.

291
00:21:24,240 --> 00:21:26,080
So think about advertisements.

292
00:21:26,080 --> 00:21:28,460
You've got an ad banner.

293
00:21:29,160 --> 00:21:36,520
Our website famously ... Earn Fifty Thousand Miles when you get a MileagePlus Award card.

294
00:21:38,700 --> 00:21:42,420
You would want to put this in the alt text for that particular image.

295
00:21:45,300 --> 00:21:47,300
[humming]

296
00:21:48,500 --> 00:21:53,960
So in this case, if you have an image and the text is duplicated nearby,

297
00:21:53,960 --> 00:21:58,160
you can go ahead and leave that alt attribute as empty.

298
00:22:00,220 --> 00:22:02,840
If the text is there just for visual effect ...

299
00:22:02,840 --> 00:22:04,840
let's say if you have ...

300
00:22:06,800 --> 00:22:08,940
I'm trying to think of the case ... a scenario like this.

301
00:22:08,940 --> 00:22:12,120
If you had a ... the word win ...

302
00:22:12,760 --> 00:22:16,820
... and it was in a weird perspective ...

303
00:22:16,820 --> 00:22:19,320
... it was on a flag, let's say.

304
00:22:19,320 --> 00:22:25,180
Maybe that's the case where you would not need to put alt text on that.

305
00:22:25,180 --> 00:22:28,160
It just really depends on your situation.

306
00:22:30,640 --> 00:22:38,560
Not present anywhere else, then you would go ahead and add the text that's on the image as your alt text.

307
00:22:39,500 --> 00:22:45,500
Is the image used in the link or button and would it be
 hard or impossible to understand

308
00:22:45,500 --> 00:22:48,860
what the link where the button does if the image wasn't there?

309
00:22:50,620 --> 00:22:52,540
No, you just continue on.

310
00:22:52,540 --> 00:22:59,360
Yes, use the alt attribute to communicate the destination of the link or action taken.

311
00:22:59,780 --> 00:23:03,700
So, again, going back to the idea of advertisements,

312
00:23:03,700 --> 00:23:10,100
maybe it's the case we say advertisement by Chase or advertisement by Hertz.

313
00:23:12,280 --> 00:23:16,620
Does the image contribute meaning to the current page or context?

314
00:23:16,620 --> 00:23:19,060
No, you just continue on to the next.

315
00:23:19,460 --> 00:23:22,440
Yes, and it's a simple graphic or photograph,

316
00:23:22,440 --> 00:23:29,020
use a brief description of the image in a way that conveys that meaning in the alt attribute.

317
00:23:29,800 --> 00:23:35,520
If yes, and it's a graph or a complex piece of information,

318
00:23:35,520 --> 00:23:38,480
include the information somewhere else on the page.

319
00:23:38,480 --> 00:23:43,560
The scenario gave a little while ago ... the airport terminal maps,

320
00:23:44,180 --> 00:23:50,600
we have the information elsewhere on the page. It's hidden visually but it's there for the screen readers.

321
00:23:52,180 --> 00:23:56,780
and it shows content that is redundant to a real ... to real text nearby

322
00:23:57,300 --> 00:24:00,820
go ahead and use an empty alt attribute.

323
00:24:02,420 --> 00:24:06,200
Is the image purely decorative or not intended for the user?

324
00:24:07,880 --> 00:24:09,600
Use an empty alt attribute.

325
00:24:11,480 --> 00:24:14,440
Is the images use not listed or is unclear?

326
00:24:14,440 --> 00:24:21,780
I'll be honest ... alt text I thought was going to be the stupid easy part of accessibility.

327
00:24:21,780 --> 00:24:24,740
I've been doing accessibility for about three years.

328
00:24:25,220 --> 00:24:30,480
Alt text is actually quite hard if you're trying ... if you're striving for quality.

329
00:24:31,060 --> 00:24:35,480
To know the scenarios where you should have alt text...

330
00:24:35,480 --> 00:24:41,520
it's not as clear-cut as you may think, at least on an e-commerce website.

331
00:24:42,180 --> 00:24:47,900
It takes practice and doing it over and over until you start realizing certain patterns.

332
00:24:48,920 --> 00:25:00,540
There's exceptions to the alternative text criteria and that is for certain other instances of images.

333
00:25:00,540 --> 00:25:04,540
So for instance, and we don't do this as often as we used to, but let's say

334
00:25:04,540 --> 00:25:08,160
if you have an image used as a submit button,

335
00:25:08,160 --> 00:25:12,800
then obviously there's a way to provide alternative text for that.

336
00:25:13,380 --> 00:25:14,500
Time-based

337
00:25:15,680 --> 00:25:18,820
This is sort of covered in Guideline 1.2.

338
00:25:18,820 --> 00:25:24,640
But basically, you would provide alternative text that describes what is this,

339
00:25:24,640 --> 00:25:29,280
what it like in this case it's an audio player what is this audio going to be?

340
00:25:29,760 --> 00:25:33,440
What is this about? Is that a podcast? Is it a song?

341
00:25:35,200 --> 00:25:36,860
A test.

342
00:25:37,320 --> 00:25:38,960
I've had to deal with this recently.

343
00:25:38,960 --> 00:25:42,100
It's very difficult because a lot of times

344
00:25:42,660 --> 00:25:49,620
if it's a test, you can't put the alt text as straightforward as you may think

345
00:25:49,620 --> 00:25:51,620
because you might be giving away the answer.

346
00:25:53,440 --> 00:25:57,900
So this is actually quite a difficult one to deal with.

347
00:25:58,620 --> 00:26:00,040
Sensory.

348
00:26:00,760 --> 00:26:02,720
You know if that ...

349
00:26:03,480 --> 00:26:06,680
... to be honest this one I haven't quite figured out yet.

350
00:26:06,680 --> 00:26:10,880
Because to me, images are very very visual.

351
00:26:10,880 --> 00:26:16,340
So I'm trying to think of the other instances, the other sensories that might apply to this.

352
00:26:17,120 --> 00:26:18,340
CAPTCHA

353
00:26:19,800 --> 00:26:21,680
Captcha is nothing but evil.

354
00:26:24,500 --> 00:26:26,500
Google is trying ...

355
00:26:26,500 --> 00:26:29,680
Now all you have to do is hit that check box.

356
00:26:30,240 --> 00:26:31,660
Because it's watching you.

357
00:26:31,660 --> 00:26:33,900
So there's good and bad in that.

358
00:26:34,180 --> 00:26:39,100
But, if you think of it, for someone with visual disabilities,

359
00:26:39,600 --> 00:26:46,740
having lines and you know on the the apartment number on a brick wall of the building

360
00:26:46,740 --> 00:26:52,200
and you're supposed to identify what it is ... it's very difficult, very difficult.

361
00:26:53,240 --> 00:26:55,760
Decoration, Formatting, Invisible.

362
00:26:55,760 --> 00:26:59,880
You know, in this case you just just forget about it.

363
00:26:59,880 --> 00:27:01,880
You know, it's just alt null.

364
00:27:01,880 --> 00:27:03,880
You don't have to provide alternatives for that.

365
00:27:05,520 --> 00:27:07,960
Ok, any questions on alt text?

366
00:27:10,160 --> 00:27:12,480
Everyone ... are you all still here?

367
00:27:13,580 --> 00:27:15,320
Okay, are you all ... okay, yes?

368
00:27:15,900 --> 00:27:27,180
[Attendee] So alt text is the alt attribute ... [Indecipherable] ...

369
00:27:27,180 --> 00:27:28,960
[Dennis] It's typically a text string.

370
00:27:28,960 --> 00:27:33,660
You would not use it in the case of referencing text elsewhere.

371
00:27:33,660 --> 00:27:37,040
There is a ... longdesc,

372
00:27:38,000 --> 00:27:42,740
that is supposed to reference another page that has the longer description.

373
00:27:43,840 --> 00:27:47,160
You know except for museums that have artwork and such,

374
00:27:47,160 --> 00:27:52,460
I cannot think of another, you know, scenario where that might come into play.

375
00:27:52,460 --> 00:27:53,340
Yes Seth ...

376
00:27:53,340 --> 00:28:12,540
[Indecipherable]

377
00:28:12,540 --> 00:28:16,660
[Dennis] Trying to throw the microphone ...

378
00:28:18,220 --> 00:28:23,600
So ... let me try to restate that for everyone ...

379
00:28:23,600 --> 00:28:29,300
Alt ... alternative should not be confused with alt text.

380
00:28:29,900 --> 00:28:31,900
There is a difference.

381
00:28:36,320 --> 00:28:42,500
[Seth] So for instance, you could have a paragraph of text, describing an image.

382
00:28:42,500 --> 00:28:46,140
But that would be the text alternative to the image.

383
00:28:46,140 --> 00:28:51,180
You don't have to use alt tag, or an attribute for the image.

384
00:28:51,680 --> 00:28:59,440
Whereas if you have a graph or a chart or SVG, you can create a text alternative in different ways

385
00:28:59,440 --> 00:29:02,280
and accomplish the same criteria.

386
00:29:04,680 --> 00:29:09,480
[Attendee] So, if you accomplish it in the body copy somehow, like you describe what the image is,

387
00:29:09,480 --> 00:29:11,980
or what the graph is for, or what your map is for,

388
00:29:11,980 --> 00:29:15,800
then you don't necessarily have to accommodate it in the actual alt.

389
00:29:16,340 --> 00:29:24,160
[Seth] It could be like a caption or it could be like ... there's a lot of gray area but, more or less.

390
00:29:24,500 --> 00:29:30,640
A lot of people get confused with the word text alternative with alt text.

391
00:29:30,640 --> 00:29:32,640
[Dennis} Agreed.

392
00:29:33,020 --> 00:29:35,260
Another place you know I said terminal maps,

393
00:29:35,260 --> 00:29:37,940
another place where we see this is infographics.

394
00:29:38,560 --> 00:29:41,480
Unless you can turn that into HTML,

395
00:29:41,920 --> 00:29:47,560
you've got to have that same content in a text format somewhere else on the page.

396
00:29:47,560 --> 00:29:58,480
[Attendee] [Indecipherable]

397
00:29:58,480 --> 00:30:01,180
[Dennis] Yeah, that's ... oh god yes, that's very complex.

398
00:30:01,460 --> 00:30:08,800
I'm going to keep moving here only because you guys don't know how much more I got here.

399
00:30:08,960 --> 00:30:10,000
Time-based media.

400
00:30:10,000 --> 00:30:12,900
I'm actually going to fly through the bullets ...

401
00:30:12,900 --> 00:30:14,900
... hold your applause please.

402
00:30:14,900 --> 00:30:16,900
I want to get to the examples

403
00:30:16,900 --> 00:30:19,400
which I actually think that some of the examples are pretty cool

404
00:30:19,400 --> 00:30:21,400
so that's why I want to get to that so ...

405
00:30:21,400 --> 00:30:25,400
So success criteria for time-based media.

406
00:30:25,940 --> 00:30:29,300
You got audio only and video only pre-recorded.

407
00:30:29,300 --> 00:30:31,300
This gets really detailed.

408
00:30:31,300 --> 00:30:33,300
Captions pre-recorded.

409
00:30:34,400 --> 00:30:38,660
Audio description or media alternative pre-recorded.

410
00:30:39,320 --> 00:30:42,220
Captions live, like this event tonight.

411
00:30:43,580 --> 00:30:45,580
Audio description pre-recorded.

412
00:30:47,120 --> 00:30:48,940
Sign language pre-recorded.

413
00:30:48,940 --> 00:30:50,940
I have an example of that; it's pretty cool.

414
00:30:52,160 --> 00:30:53,960
Extended audio description.

415
00:30:53,960 --> 00:30:56,940
I had to look that up, because I didn't understand.

416
00:30:57,200 --> 00:31:01,160
But when I saw the example that I included in this presentation,

417
00:31:01,160 --> 00:31:03,960
I thought, Whoa, I didn't even know anyone did it

418
00:31:04,260 --> 00:31:08,220
It's an example video that explains it, but I don't ...

419
00:31:08,220 --> 00:31:12,240
do you know if they there's a lot of usage of that?

420
00:31:12,500 --> 00:31:15,900
Where they actually stop the video and get the description in

421
00:31:15,900 --> 00:31:37,420
[Attendee] The most widely, disseminated version of that ... [Indecipherable]

422
00:31:37,420 --> 00:31:38,540
[Dennis] Okay, yeah.

423
00:31:38,540 --> 00:31:40,540
I'm going to show an example of that...

424
00:31:40,540 --> 00:31:44,280
I just looked at the time ... boy ... I gotta speed up here.

425
00:31:44,280 --> 00:31:48,480
So I am going to start flying through this, to get to the examples,

426
00:31:48,480 --> 00:31:51,000
to get to the to the good stuff here.

427
00:31:51,000 --> 00:31:53,540
So Media Alternative Pre-recorded.

428
00:31:53,820 --> 00:31:55,820
Audio-only live.

429
00:31:56,920 --> 00:32:00,520
So, Audio-only and Video-only prerecorded.

430
00:32:00,520 --> 00:32:05,540
Except when ... mind you, I had to reread this stuff three or four times to think

431
00:32:05,540 --> 00:32:08,760
wait I misunderstood what this really meant.

432
00:32:08,760 --> 00:32:14,720
Except for when the audio or video is clearly labeled media alternative for text.

433
00:32:15,800 --> 00:32:21,660
Pre-recorded audio-only, an alternative for the time-based media is provided

434
00:32:21,660 --> 00:32:26,620
that presents equivalent information for pre-recorded audio-only content.

435
00:32:27,700 --> 00:32:32,140
Podcast, interview, things like that.

436
00:32:32,740 --> 00:32:34,880
Pre-recorded video only.

437
00:32:35,060 --> 00:32:38,040
So think of this, a video only ... um ...

438
00:32:38,660 --> 00:32:42,860
a time-lapse camera, a cam or there's no sound.

439
00:32:44,560 --> 00:32:49,280
Either an alternative for the time-based media or an audio track is provided

440
00:32:49,280 --> 00:32:54,220
that presents equivalent information for pre-recorded video only content.

441
00:32:57,460 --> 00:33:04,060
That actually was an eye opener because I had made some assumptions that actually were not accurate.

442
00:33:04,440 --> 00:33:05,080
Captions

443
00:33:05,080 --> 00:33:10,780
Captions are provided for all pre-recorded audio content and synchronized media.

444
00:33:11,300 --> 00:33:13,720
I want you to pay attention to ...

445
00:33:14,900 --> 00:33:16,540
...  why do I keep doing that ...

446
00:33:17,940 --> 00:33:21,500
There we go. I'm pressing a button here that's causing that I'm not sure why.

447
00:33:23,160 --> 00:33:29,100
I want you to pay attention to the level ... the level of accessibility.

448
00:33:29,100 --> 00:33:32,320
So this is single A, okay. So this is basic.

449
00:33:32,320 --> 00:33:37,260
Captions are provided for all pre-recorded audio content and synchronized media.

450
00:33:37,260 --> 00:33:39,260
YouTube. YouTube videos.

451
00:33:42,540 --> 00:33:46,080
Audio description or media alternative pre-recorded.

452
00:33:46,520 --> 00:33:51,420
An alternative for time-based media or audio description of the pre-recorded video content

453
00:33:51,420 --> 00:33:54,560
is provided for synchronized media.

454
00:33:55,880 --> 00:33:57,880
Captions live. Like this tonight.

455
00:33:58,560 --> 00:34:04,420
Captions are provided for all live audio content in synchronized media.

456
00:34:05,980 --> 00:34:07,700
Audio description pre-recorded.

457
00:34:07,700 --> 00:34:12,740
Audio description is provided for all pre-recorded video content in synchronized media.

458
00:34:13,080 --> 00:34:19,440
How many of you have ever watched movies let's say on Netflix or something and turned on audio description?

459
00:34:20,680 --> 00:34:21,680
Isn't it cool?

460
00:34:22,660 --> 00:34:27,900
I actually also get into, you know, watching the caption versions of things.

461
00:34:28,140 --> 00:34:31,500
Until my wife tells me to stop because she can't stand it.

462
00:34:31,500 --> 00:34:38,260
She actually, okay, my wife was supposed to be here, to help out, she didn't.

463
00:34:38,820 --> 00:34:45,460
Just so you know she has turned on captions using comic sans.

464
00:34:46,800 --> 00:34:50,260
I think it's keep me from using captions.

465
00:34:50,260 --> 00:34:52,260
Sign language pre-recorded.

466
00:34:52,260 --> 00:34:58,780
Sign language interpretation is provided for all pre-recorded audio content and synchronized media.

467
00:34:58,960 --> 00:35:00,960
Notice it's level AAA.

468
00:35:01,740 --> 00:35:04,320
I actually have an example of that, it's pretty cool.

469
00:35:04,800 --> 00:35:07,520
Extended audio description pre-recorded.

470
00:35:07,960 --> 00:35:14,620
Pauses in foreground audio are insufficient to allow audio descriptions to convey the sense of the video,

471
00:35:14,940 --> 00:35:21,580
extended audio descriptions is provided for all pre-recorded video content and synchronized media.

472
00:35:21,580 --> 00:35:23,580
This is also Triple A.

473
00:35:24,600 --> 00:35:26,980
Media alternatives pre-recorded.

474
00:35:26,980 --> 00:35:28,980
I'm going to start flying through these because...

475
00:35:30,280 --> 00:35:33,920
you know they get so ... so complex here

476
00:35:33,920 --> 00:35:40,580
Alternative ... for all pre-record synchronized media and for all pre-recorded video only media.

477
00:35:41,220 --> 00:35:42,560
Audio only live.

478
00:35:43,340 --> 00:35:45,340
Live concert, radio concert, I guess.

479
00:35:46,020 --> 00:35:48,600
Okay, here's where we have some demos.

480
00:35:48,600 --> 00:35:56,260
So, for those of you who have attended past meetups, you've heard me mention this accessible player

481
00:35:56,260 --> 00:35:57,440
called Able Player.

482
00:35:57,880 --> 00:36:01,920
These are a couple of demos of Able Player in action.

483
00:36:01,920 --> 00:36:07,980
So this is an audio file with a transcript.

484
00:36:09,200 --> 00:36:15,660
So for those who are hard of hearing or can't hear, this is their way to obtain the information.

485
00:36:16,560 --> 00:36:19,580
[♪♪ Music ♪♪]

486
00:36:19,580 --> 00:36:20,780
[Dennis] Watch the transcript.

487
00:36:20,780 --> 00:36:25,000
[♪♪ Music ♪♪]

488
00:36:25,000 --> 00:36:32,460
[♪♪ A male signing to music, lyrics indecipherable ♪♪]

489
00:36:32,720 --> 00:36:36,060
[Dennis] Trust me you're not missing anything.

490
00:36:36,060 --> 00:36:45,080
As you see that the the transcript highlights the lyrics that are being sung at the present time.

491
00:36:45,640 --> 00:36:49,000
What else... we have video transcript.

492
00:36:49,000 --> 00:36:55,780
This is similar, but what this looks like ...

493
00:36:56,500 --> 00:37:03,980
[♪♪ Music ♪♪]

494
00:37:03,980 --> 00:37:08,460
[♪♪ Narration over music ♪♪]

495
00:37:08,460 --> 00:37:14,180
[Dennis] So not only do you have the caption here, you have the text highlighted and transcript.

496
00:37:14,460 --> 00:37:17,020
You might wonder why you need both?

497
00:37:17,580 --> 00:37:23,360
Well, the captions are not accessible by a screen reader or a refreshable Braille keyboard.

498
00:37:24,140 --> 00:37:28,620
So this would provide additional coverage for people who need that.

499
00:37:31,220 --> 00:37:33,780
Okay this is one of my favorites.

500
00:37:33,780 --> 00:37:36,120
So this is video with sign language.

501
00:37:36,120 --> 00:37:40,920
As you remember, this is a Triple A compliance item.

502
00:37:41,740 --> 00:37:49,360
[♪♪ Music ♪♪]

503
00:37:49,360 --> 00:38:00,520
[♪♪ Narration over music ♪♪]

504
00:38:00,520 --> 00:38:04,780
[Dennis] So as you can imagine, most people understand text

505
00:38:05,760 --> 00:38:09,100
but there's some people who are more comfortable with sign language

506
00:38:09,100 --> 00:38:14,360
or maybe there's instances where someone's only comfortable with sign language.

507
00:38:14,900 --> 00:38:17,320
This allows them to gain that information.

508
00:38:18,580 --> 00:38:25,440
[Attendee]: Dennis, the highlighting of the transcript, was covered up by the ....

509
00:38:25,440 --> 00:38:31,580
[Dennis]: Actually, no, I actually, for that example I should have turned off the transcripts as not to confuse things.

510
00:38:31,580 --> 00:38:36,160
But yeah, if this were a full-size page, you could actually drag and drop

511
00:38:36,160 --> 00:38:43,000
the transcript over here, the sign language over here so not in this constrained view.

512
00:38:43,000 --> 00:38:46,620
But yeah, you could have both of those options running.

513
00:38:47,300 --> 00:38:51,260
So this is an example of Extended Audio Description.

514
00:38:53,940 --> 00:38:56,780
Oh, ok, didn't know it was going to do that ...

515
00:39:01,460 --> 00:39:04,820
... and we're live folks ...

516
00:39:06,760 --> 00:39:08,760
... try this again ...

517
00:39:12,100 --> 00:39:20,440
[Audio Description of paused video]

518
00:39:20,440 --> 00:39:22,440
[Audio from video]

519
00:39:22,440 --> 00:39:28,380
[Audio Description of paused video]

520
00:39:28,380 --> 00:39:35,300
[Audio from video]

521
00:39:35,300 --> 00:39:40,680
[Audio Description of paused video]

522
00:39:41,800 --> 00:39:52,300
[Audio from video]

523
00:39:52,820 --> 00:39:57,160
[Dennis] So, this is the first time I had ever experienced extended audio description,

524
00:39:57,160 --> 00:40:01,360
preparing for this presentation. I just thought that there was like so cool.

525
00:40:03,200 --> 00:40:05,900
[Audio Description of paused video]

526
00:40:05,940 --> 00:40:07,940
[Dennis] ... ok, stop ...

527
00:40:09,800 --> 00:40:13,920
Any questions about time-based media?

528
00:40:16,220 --> 00:40:18,220
Going once, going twice, yes?

529
00:40:18,220 --> 00:40:23,640
[Attendee]  So, for people who are deaf ... so, for the sign language aspect of it,

530
00:40:23,640 --> 00:40:27,700
is that prerecorded? Or is that, I would assume ...

531
00:40:27,700 --> 00:40:30,060
[Dennis] It's a video.

532
00:40:30,060 --> 00:40:35,360
And to the point, if you reread those different criteria,

533
00:40:36,220 --> 00:40:43,900
they ... so basing in this case, the recording of the sign language does not need a text alternative

534
00:40:43,900 --> 00:40:50,480
because it itself is an alternative to another instance of media.

535
00:40:51,340 --> 00:40:55,040
So ... [laughing]

536
00:40:55,040 --> 00:41:01,700
It's funny, preparing this series, I looked at it as a way to dig deeper into WCAG

537
00:41:01,700 --> 00:41:07,440
and you know each one of these principles I could just spend ... it could be my full-time job,

538
00:41:07,440 --> 00:41:11,760
just digging in and learning more about these things, so ... but anyways...

539
00:41:12,780 --> 00:41:19,100
Oh god, literally have 17 minutes to finish so this is going to be fun.

540
00:41:19,100 --> 00:41:20,280
Adaptable.

541
00:41:20,280 --> 00:41:23,720
Creating content that can be presented in different ways.

542
00:41:25,100 --> 00:41:26,840
So the success criteria...

543
00:41:26,840 --> 00:41:28,840
Info and relationships,

544
00:41:29,580 --> 00:41:32,840
Meaningful Sequence and Sensory Characteristics.

545
00:41:32,840 --> 00:41:34,380
Info and Relationships,

546
00:41:34,380 --> 00:41:40,380
what's the first thing you think about when you think Info and Relationships with regards to webpages?

547
00:41:41,520 --> 00:41:42,320
Anyone?

548
00:41:43,700 --> 00:41:48,440
Headings? Okay that's that's good. What else?

549
00:41:50,640 --> 00:41:51,500
Bless you.

550
00:41:51,980 --> 00:41:53,340
[Attendee] Taxonomy?

551
00:41:59,540 --> 00:42:00,460
[Dennis] Possibly.

552
00:42:00,460 --> 00:42:03,780
I was thinking ... stretch ... stretch ...

553
00:42:04,760 --> 00:42:07,940
Possibly, in certain ways ... maybe we'll be able to touch on that.

554
00:42:07,940 --> 00:42:08,780
Anything else?

555
00:42:08,780 --> 00:42:13,140
[Attendee] [Indecipherable]

556
00:42:13,140 --> 00:42:17,860
[Dennis] Ah ... yes and no.

557
00:42:17,860 --> 00:42:20,680
For me, I always call it semantics.

558
00:42:21,460 --> 00:42:29,620
Ok, so Information structure relationships conveyed through presentation that can be programma ... uh

559
00:42:29,620 --> 00:42:30,820
It's late, folks ...

560
00:42:30,860 --> 00:42:37,580
programma ... thank you, I think I'm just going to point to you, because that word comes up several times here.

561
00:42:37,580 --> 00:42:41,240
Determined or are available in text.

562
00:42:42,060 --> 00:42:44,060
So, think of it this way ...

563
00:42:44,060 --> 00:42:46,060
... oh, stop that ...

564
00:42:46,060 --> 00:42:50,740
Semantic, web standards based HTML

565
00:42:50,960 --> 00:42:55,640
And there, in the slides, there's actually a great link to a great article on this.

566
00:42:56,160 --> 00:43:00,160
Basically what this means is ... coding semantically.

567
00:43:01,300 --> 00:43:10,780
So, if we want a heading we don't just say font size 24 pixels of blue you know,

568
00:43:10,780 --> 00:43:11,980
we don't do that.

569
00:43:11,980 --> 00:43:15,000
We give it an H1 or we give it an H2.

570
00:43:15,000 --> 00:43:17,600
We call it what it is.

571
00:43:17,600 --> 00:43:21,240
[Attendee] [Indecipherable]

572
00:43:23,060 --> 00:43:29,520
I would say using markup ... it's the separation between the markup and styles.

573
00:43:29,520 --> 00:43:32,560
[Attendees] [Indecipherable]

574
00:43:32,560 --> 00:43:34,000
[Dennis] Yes, definitely.

575
00:43:34,400 --> 00:43:37,420
[Attendees] [Indecipherable]

576
00:43:37,420 --> 00:43:41,600
[Dennis] Sections, Articles, all in HTML5, yeah ...

577
00:43:41,600 --> 00:43:43,600
[Attendees] [Indecipherable]

578
00:43:43,600 --> 00:43:45,600
[Dennis] And so, Techniques.

579
00:43:45,600 --> 00:43:46,920
And again, I'll just ...

580
00:43:46,920 --> 00:43:52,140
because most of you are going to be familiar with this you just might not realize how its applied here

581
00:43:53,300 --> 00:43:58,180
Use paragraphs, or use the P tag for paragraphs.

582
00:43:58,180 --> 00:44:02,980
Don't use break tags, which are actually all over our site.

583
00:44:03,640 --> 00:44:12,340
Use list tags instead of ... break  break break ... you know, putting a dash because it looks good.

584
00:44:13,880 --> 00:44:17,260
Don't use a table for layout. Use it for tabular data.

585
00:44:17,940 --> 00:44:21,460
If you're going to use data tables, have a caption.

586
00:44:21,460 --> 00:44:31,000
Put in table heading cells and use the scope attribute to determine what that heading is applied to.

587
00:44:32,580 --> 00:44:35,820
Use ... oh here we go, another can of worms.

588
00:44:35,820 --> 00:44:40,140
Use the "a" tag for links with an href.

589
00:44:40,140 --> 00:44:46,240
Did you know that if you have an "a" tag that doesn't have a href, it's not focusable?

590
00:44:51,060 --> 00:44:53,240
"a" tag should be used for navigation.

591
00:44:54,060 --> 00:45:00,480
It can run a script in addition to, but that should not be the primary function of the link.

592
00:45:01,880 --> 00:45:07,040
Use button tags to trigger actions and scripts.

593
00:45:08,180 --> 00:45:12,560
Don't use non-semantic elements such as divs or spans for links or buttons.

594
00:45:13,100 --> 00:45:20,960
There's a plethora of articles out there about that. Just do a Google search on links versus buttons.

595
00:45:20,960 --> 00:45:25,940
And in fact, Marcy Sutton has an article on that, that is quite good.

596
00:45:25,940 --> 00:45:31,600
However now, with this said, think about custom controls.

597
00:45:33,180 --> 00:45:45,420
We're actually using non-semantic markup to perform the same functionality as links and buttons.

598
00:45:45,420 --> 00:45:48,600
So the key is, you know it can work.

599
00:45:48,600 --> 00:45:51,560
I mean, I can go to a visit a website and this functions.

600
00:45:51,560 --> 00:45:55,060
I click on this button it performs an action.

601
00:45:55,060 --> 00:45:57,060
When I look at the code, it's a div.

602
00:45:57,620 --> 00:45:58,720
How did they do that?

603
00:45:58,720 --> 00:46:02,180
They had to bake it all in. It's a lot of extra work.

604
00:46:02,900 --> 00:46:04,600
Sometimes it's necessary.

605
00:46:04,600 --> 00:46:11,880
If you're using frameworks like Angular and Ember and such, there's likely a reason why you need to do that.

606
00:46:12,740 --> 00:46:18,020
However, whenever possible, try to use the holistic tags that we have.

607
00:46:19,880 --> 00:46:25,260
So for instance, here's an anchor a tag with a href.

608
00:46:25,980 --> 00:46:27,860
This "continue" link here.

609
00:46:27,860 --> 00:46:31,060
Screen reader reads "link continue,"

610
00:46:31,500 --> 00:46:34,000
and they can interact with it using the Enter key.

611
00:46:35,220 --> 00:46:37,220
The Continue button is a button.

612
00:46:38,200 --> 00:46:40,580
Screen reader reads it as "button continue."

613
00:46:41,440 --> 00:46:44,360
The user knows that they can press the spacebar

614
00:46:44,360 --> 00:46:46,360
to interact with it.

615
00:46:47,160 --> 00:46:49,160
What happens here when we use a div?

616
00:46:50,360 --> 00:46:52,360
Screen reader says "continue."

617
00:46:53,720 --> 00:46:57,080
It's not focusable, you can't interact with it,

618
00:46:57,720 --> 00:47:00,280
because the screen reader user doesn't know what to do,

619
00:47:00,280 --> 00:47:03,620
It's not focusable, there's no role stating what it is.

620
00:47:04,160 --> 00:47:06,160
You'd have to bake all that in.

621
00:47:06,900 --> 00:47:08,300
It's a lot of extra work.

622
00:47:08,300 --> 00:47:11,920
I'm not saying it's not ... that you should never do it,

623
00:47:11,920 --> 00:47:15,340
but always think, do I have to do this?

624
00:47:16,400 --> 00:47:19,840
That's the link to the article that I just mentioned.

625
00:47:20,560 --> 00:47:22,280
Meaningful Sequence.

626
00:47:22,880 --> 00:47:27,900
I literally was having meetings at work on this today.

627
00:47:29,040 --> 00:47:32,680
So if you were to code this,

628
00:47:33,460 --> 00:47:35,040
how would you code this?

629
00:47:35,040 --> 00:47:37,640
What would you expect the navigation of this to be?

630
00:47:39,960 --> 00:47:41,060
Anyone?

631
00:47:41,060 --> 00:47:44,620
[Attendee] [Indecipherable]

632
00:47:44,620 --> 00:47:49,360
[Dennis] So Package 1, then the content. Package 2, then the content.

633
00:47:50,920 --> 00:47:54,760
Today, it's Package one, Package two.

634
00:47:56,060 --> 00:48:03,040
List with two items. Free room upgrade. A list item, late check-out.

635
00:48:04,100 --> 00:48:06,860
But what is this apply to, package one or  package two?

636
00:48:06,860 --> 00:48:13,500
Because it's coded like that, they're actually not related to one another.

637
00:48:13,500 --> 00:48:15,500
That's where the relationships come in.

638
00:48:16,320 --> 00:48:19,880
Okay, done the correct way, looks the same,

639
00:48:19,880 --> 00:48:27,540
but it's coded to where you have the heading and then you have the information immediately after it.

640
00:48:29,160 --> 00:48:31,160
Sensory characteristics.

641
00:48:32,180 --> 00:48:39,620
Ah, imagine you're blind and your screen reader says click the submit button on the left.

642
00:48:42,380 --> 00:48:45,140
Where are you going to go if your screen reader user?

643
00:48:46,820 --> 00:48:47,940
Before?

644
00:48:49,040 --> 00:48:50,120
Possibly.

645
00:48:51,340 --> 00:48:52,900
So, that's confusing.

646
00:48:53,180 --> 00:48:58,380
Okay here's one of the first 2.1, WCAG 2.1 items we have...

647
00:48:58,380 --> 00:48:59,880
Support personalization.

648
00:49:00,680 --> 00:49:07,480
So once again, the items that are in amber or orange, these are still being discussed.

649
00:49:07,480 --> 00:49:09,480
So there's nothing to do here.

650
00:49:10,100 --> 00:49:17,980
Basically, it's providing programmatically ...  help me out ... thank you.

651
00:49:17,980 --> 00:49:24,180
... determinable content so that personalization is available.

652
00:49:24,600 --> 00:49:28,000
So it can be determined that this is personalization.

653
00:49:28,000 --> 00:49:32,440
As you could think of it, we don't have any tags that say this is personalization.

654
00:49:32,720 --> 00:49:36,700
We don't have any ARIA that says that this is personalization.

655
00:49:37,560 --> 00:49:38,680
Distinguishable.

656
00:49:39,840 --> 00:49:46,180
Make it easier for users to see and hear content including separating foreground from background.

657
00:49:47,600 --> 00:49:49,600
... Let's see ... ok we're doing pretty good ...

658
00:49:50,580 --> 00:49:55,980
So this is going to be dealing a lot with contrast, but it's not just color.

659
00:49:56,820 --> 00:49:58,000
Use of color.

660
00:49:58,380 --> 00:49:59,600
Audio control.

661
00:49:59,600 --> 00:50:01,600
Contrast minimum.

662
00:50:02,200 --> 00:50:03,800
Resize text.

663
00:50:04,840 --> 00:50:06,160
Images of text.

664
00:50:07,260 --> 00:50:09,020
Contrast enhanced.

665
00:50:09,680 --> 00:50:11,680
Low or no background audio.

666
00:50:12,420 --> 00:50:13,820
Visual presentation.

667
00:50:13,820 --> 00:50:16,340
Images of text no exception

668
00:50:16,340 --> 00:50:18,500
As you can imagine, that's a Triple A item.

669
00:50:20,040 --> 00:50:22,820
New criteria ... linearization

670
00:50:23,980 --> 00:50:25,520
Resizing content.

671
00:50:25,520 --> 00:50:27,520
Graphics contrast.

672
00:50:28,460 --> 00:50:29,180
Printing.

673
00:50:29,940 --> 00:50:34,640
Can you imagine having to make sure that when you print a page, it's accessible?

674
00:50:35,720 --> 00:50:37,000
Haven't thought of that yet.

675
00:50:38,040 --> 00:50:40,520
User interface component contrast.

676
00:50:41,440 --> 00:50:44,480
Think about how many forms controls you have.

677
00:50:45,420 --> 00:50:46,660
Let's say form fields.

678
00:50:46,660 --> 00:50:49,980
You know we just love to put the lightest shade of grey

679
00:50:49,980 --> 00:50:51,360
around that form field.

680
00:50:52,040 --> 00:50:55,000
Or maybe none ... you know I've seen that.

681
00:50:56,140 --> 00:50:58,780
That would hit upon that.

682
00:50:59,860 --> 00:51:01,040
Adapting text.

683
00:51:02,000 --> 00:51:03,800
Popup interference.

684
00:51:04,220 --> 00:51:07,200
Oh you can imagine that's amber, people are like,

685
00:51:07,200 --> 00:51:07,960
okay what does that mean?

686
00:51:09,180 --> 00:51:10,480
Use of color, okay.

687
00:51:11,080 --> 00:51:17,600
Colors not use as the only visual means of conveying information, indicating in action,

688
00:51:17,600 --> 00:51:22,340
prompting a response or distinguishing a visual element.

689
00:51:23,080 --> 00:51:28,000
How many times, not recently, how many times have we said click the green button?

690
00:51:31,280 --> 00:51:33,280
This is a basic item, Level A.

691
00:51:34,860 --> 00:51:37,120
Okay, here's where I get to have a little fun.

692
00:51:39,300 --> 00:51:44,720
So what is the links ... what are the links on this particular page?

693
00:51:47,240 --> 00:51:49,260
The text in blue? Okay.

694
00:51:50,080 --> 00:51:59,960
Now, let's just say that you have a form of colorblindness to where you can't see blue.

695
00:52:01,280 --> 00:52:03,280
What's the link text?

696
00:52:08,920 --> 00:52:09,960
It's an issue.

697
00:52:09,960 --> 00:52:16,200
So this is simulated using a Chrome plugin called No Coffee Vision simulator.

698
00:52:16,200 --> 00:52:18,200
It's actually ... it's ...

699
00:52:23,740 --> 00:52:31,560
So the ... obviously the alternative to just using color alone would be to use underlines,

700
00:52:31,560 --> 00:52:33,560
which of course we all hate.

701
00:52:34,540 --> 00:52:43,360
But it's the basis of the web from nineteen ninety two, three ... what ... yeah ... something like that.

702
00:52:43,360 --> 00:52:45,360
Here's another one.

703
00:52:47,380 --> 00:52:50,960
So what are the ... what's the regular rate and what's the member rate?

704
00:52:51,520 --> 00:52:54,260
It's very clear. It's all based on color.

705
00:52:54,960 --> 00:52:56,960
If we use the same premise,

706
00:53:00,900 --> 00:53:02,000
which is which?

707
00:53:04,000 --> 00:53:08,380
Again using the No Coffee Vision simulator.

708
00:53:13,120 --> 00:53:14,260
Audio Control

709
00:53:14,260 --> 00:53:17,420
I had really tried to get a good example of this,

710
00:53:17,420 --> 00:53:20,940
but I gave up. I have to admit.

711
00:53:21,380 --> 00:53:26,840
But basically, you know, and we don't have this as often now thank God,

712
00:53:27,100 --> 00:53:29,340
I literally run into this about once a year now.

713
00:53:29,800 --> 00:53:33,060
But how many times have we gone to a website ... let's say you go to ...

714
00:53:34,340 --> 00:53:37,280
beaches resort website,

715
00:53:37,840 --> 00:53:41,480
and they would have, what's that song ...

716
00:53:41,480 --> 00:53:43,820
[Dennis's bad impression of Bill Medley singing] I had the time of my life ...

717
00:53:43,820 --> 00:53:47,740
I think that was there running song for a while there,

718
00:53:48,720 --> 00:53:50,280
and there's no way to turn it off.

719
00:53:51,140 --> 00:53:52,420
Okay, really?

720
00:53:52,760 --> 00:53:54,760
That could be very irritating, especially at work.

721
00:53:55,420 --> 00:53:59,420
Now everyone knows, "they're on the beaches website."

722
00:54:00,160 --> 00:54:02,160
Contrast minimum.

723
00:54:03,800 --> 00:54:07,300
I'm not a numbers person, so I literally have to read up.

724
00:54:07,300 --> 00:54:10,420
I depend on tools when it comes to color contrast.

725
00:54:12,640 --> 00:54:14,280
So basically, as a minimum,

726
00:54:14,960 --> 00:54:17,460
color contrast, foreground to background.

727
00:54:17,460 --> 00:54:20,560
So think of it, text and to the background,

728
00:54:20,560 --> 00:54:26,680
you must have a color of contrast ratio of 4.5:1.

729
00:54:27,840 --> 00:54:30,200
Okay, to be Level AA compliant.

730
00:54:31,320 --> 00:54:34,860
There are nuances for large text.

731
00:54:34,860 --> 00:54:37,700
Large-scale text and images of large scale text

732
00:54:37,700 --> 00:54:41,620
have a color contrast ratio of at least 3:1.

733
00:54:43,100 --> 00:54:44,440
Incidental text.

734
00:54:44,440 --> 00:54:47,720
Text or images of texts that are part of an inactive ...

735
00:54:47,720 --> 00:54:49,720
okay I'm just going to forget about that ...

736
00:54:49,720 --> 00:54:51,760
... it's that's getting too detailed.

737
00:54:51,760 --> 00:54:54,300
Logotypes. So this is interest we always have

738
00:54:54,300 --> 00:54:56,620
a lot of people ask about well what about logos,

739
00:54:57,320 --> 00:55:01,940
if it's part of a logo, it is exempt from color contrast.

740
00:55:02,460 --> 00:55:03,900
Okay, I would say though,

741
00:55:03,900 --> 00:55:05,900
wouldn't you want your logo to pop?

742
00:55:06,400 --> 00:55:08,400
I always tell folks.

743
00:55:08,400 --> 00:55:10,900
Here's a perfect example.

744
00:55:10,900 --> 00:55:15,520
So this is using what we call normal sized text.

745
00:55:15,520 --> 00:55:19,160
This is a ...  WCAG uses points ...

746
00:55:20,160 --> 00:55:22,580
can anyone show me a point on this screen?

747
00:55:24,640 --> 00:55:25,960
Go ahead, I'll wait...

748
00:55:25,960 --> 00:55:27,340
... ok, I won't.

749
00:55:27,340 --> 00:55:29,340
There are no points. There's pixels ...

750
00:55:30,280 --> 00:55:32,720
And nowadays, we use ems and percentages.

751
00:55:33,340 --> 00:55:38,980
I've actually submitted feedback to have WCAG change from points to pixels.

752
00:55:39,740 --> 00:55:44,260
Because all that does is makes me have to go and perform the conversion.

753
00:55:45,040 --> 00:55:46,740
That doesn't make any sense.

754
00:55:49,480 --> 00:55:57,400
Text is less than 18 points or 24 pixels if not bold and less than 14 points 18 pixels if bold.

755
00:55:58,100 --> 00:56:06,780
So basically with these various shades of blue both of these paths the non bold version fails both failed.

756
00:56:08,020 --> 00:56:11,080
Okay now you might ask well how do you know that offhand?

757
00:56:11,080 --> 00:56:18,800
So I do have ... I do have an analyzer let's see if I can do this without messing everything up.

758
00:56:20,120 --> 00:56:22,960
Ah let's see here get past the Kardashians ...

759
00:56:26,320 --> 00:56:34,460
So this is the tool that actually I was told about called the WCAG color ... the contrast checker.

760
00:56:34,460 --> 00:56:41,840
So basically it puts a side panel here and you just use the eyedropper to select the foreground and background.

761
00:56:43,400 --> 00:56:48,380
If you can imagine trying to get white out of this you know it's a little bit difficult,

762
00:56:48,380 --> 00:56:53,560
but as you see here that combination passes for Level AA.

763
00:56:53,960 --> 00:56:55,520
Actually passes for AAA.

764
00:56:55,760 --> 00:57:01,520
If we change the background to this lighter one, you notice that now at this size it fails

765
00:57:02,580 --> 00:57:07,760
and then obviously for the even lighter version it all fails.

766
00:57:07,760 --> 00:57:16,000
Okay if we go to the larger version, this is larger text, same sort of thing,

767
00:57:17,080 --> 00:57:19,080
we perform the test,

768
00:57:20,920 --> 00:57:23,880
It passes, it passes, it fails.

769
00:57:27,360 --> 00:57:32,880
United.com uses a fairly popular font called Open Sans.

770
00:57:32,880 --> 00:57:35,420
How many people use Open Sans in your work?

771
00:57:36,120 --> 00:57:38,120
Raise your hands ... okay ...

772
00:57:38,120 --> 00:57:40,120
So decent representation.

773
00:57:40,120 --> 00:57:46,440
The lighter or thinner the typeface is, the more likely you're going to be out of compliance.

774
00:57:46,440 --> 00:57:48,440
And it's more of a perceptional thing.

775
00:57:48,440 --> 00:57:53,320
You know you might say this background and this foreground, it actually matches,

776
00:57:53,680 --> 00:57:58,120
but because of the thinness, I can't tell you how many times have to get up really close to say

777
00:57:58,500 --> 00:58:00,880
I don't know. I just don't know.

778
00:58:02,380 --> 00:58:04,720
[Attendee] You've got like one minute.

779
00:58:04,720 --> 00:58:05,860
[Dennis] [sigh] Oh boy.

780
00:58:06,220 --> 00:58:08,220
Thanks for the time check. I appreciate that.

781
00:58:10,200 --> 00:58:11,520
Same thing here,  ads.

782
00:58:11,520 --> 00:58:15,420
I know these two duplicate, I forgot to get the third one.

783
00:58:15,620 --> 00:58:16,500
These all fail.

784
00:58:18,240 --> 00:58:20,160
Here's one of my favorites.

785
00:58:20,160 --> 00:58:25,580
When you place text over the image, technically this fails.

786
00:58:25,580 --> 00:58:28,740
And the reason why is, yes, I can read "Superb Getaway,"

787
00:58:29,540 --> 00:58:32,360
but I can't ... this is failing right there.

788
00:58:32,840 --> 00:58:38,080
Okay, now, there is a technique to improve things so you can just put an overlay,

789
00:58:39,240 --> 00:58:43,440
which is fine, but you know what's one thing that a lot of people forget whenever you use

790
00:58:43,440 --> 00:58:45,860
in this case, this is the background image,

791
00:58:47,100 --> 00:58:49,420
what happens if the images are turned off?

792
00:58:53,940 --> 00:58:56,380
You get a white box. I mean, the text is there.

793
00:58:57,960 --> 00:59:01,440
So always, if you using a background image, always use a background color.

794
00:59:03,460 --> 00:59:04,300
Resizing text.

795
00:59:04,300 --> 00:59:07,220
I'm not going to demo this, but basically in Firefox,

796
00:59:07,220 --> 00:59:12,360
so you know nowadays, we just zoom and everything sizes nicely.

797
00:59:12,880 --> 00:59:15,160
In Firefox you can zoom just the text.

798
00:59:16,200 --> 00:59:22,240
What happens is now this text overlays this and now you're failing 1.4.4.

799
00:59:22,240 --> 00:59:22,760
Yes?

800
00:59:23,600 --> 00:59:24,860
Did you have a question?

801
00:59:25,060 --> 00:59:25,700
Okay.

802
00:59:29,200 --> 00:59:30,160
Images of text.

803
00:59:30,660 --> 00:59:31,900
Don't use images of text.

804
00:59:32,400 --> 00:59:37,620
We've got these font APIs left and right so don't use that.

805
00:59:38,600 --> 00:59:40,600
Contrast enhanced.

806
00:59:42,500 --> 00:59:44,840
All the AAA stuff, I'm just going to blow right past this.

807
00:59:45,080 --> 00:59:47,340
You definitely can check this out.

808
00:59:47,340 --> 00:59:52,220
If you have audio, make sure that the foreground audio, if someone speaking,

809
00:59:52,660 --> 00:59:57,460
don't have traffic with blowing horns, blowing, you know, that'll be difficult.

810
00:59:59,860 --> 01:00:01,380
Visual presentation.

811
01:00:01,380 --> 01:00:02,140
AAA

812
01:00:02,140 --> 01:00:04,140
I'm just going to go past this...

813
01:00:04,140 --> 01:00:06,140
Images of text no exception.

814
01:00:06,140 --> 01:00:08,140
Here's the 2.1, thanks.

815
01:00:08,520 --> 01:00:18,960
Firefox has a setting to where you can linearize the page so this way it's just it's almost like an e-reader.

816
01:00:18,960 --> 01:00:23,620
It just takes all the layout out and just linearizes the entire page.

817
01:00:24,760 --> 01:00:28,540
This is actually a proposed item and this is going to be basic,

818
01:00:28,860 --> 01:00:31,920
which means your page must be able to be linearized.

819
01:00:32,640 --> 01:00:37,080
Resizing content. This is actually one that is fairly approved.

820
01:00:37,960 --> 01:00:45,780
Normally, the WCAG 2 specification say you need to be able to zoom text by 200%.

821
01:00:47,040 --> 01:00:51,120
I've done user testing where people zoom by 500%.

822
01:00:51,800 --> 01:00:56,440
So this is actually getting closer to meeting users needs.

823
01:00:57,240 --> 01:00:59,280
Graphics contrast.

824
01:01:00,180 --> 01:01:03,340
If you have a graphic that has foreground and background

825
01:01:03,720 --> 01:01:09,320
and there are things being communicated that's not text this is where this would fall to play.

826
01:01:10,940 --> 01:01:13,300
Lots of details here.

827
01:01:13,300 --> 01:01:14,060
Printing.

828
01:01:16,160 --> 01:01:22,220
It has to be resized, so if you resize the screen, the text that you print must also be resized.

829
01:01:22,560 --> 01:01:23,560
Think about that.

830
01:01:24,720 --> 01:01:30,160
Changes reflected ... if you make changes to the page, you have the ability to make changes to the page,

831
01:01:30,160 --> 01:01:32,820
that printout must reflect those changes.

832
01:01:34,960 --> 01:01:38,280
This one is just ... a ton of stuff.

833
01:01:39,640 --> 01:01:41,640
Adapting text.

834
01:01:44,980 --> 01:01:46,540
I can't wait to see some of these ...

835
01:01:46,540 --> 01:01:47,900
Pop-up interface.

836
01:01:48,820 --> 01:01:56,540
So tool. Tools that I did not cover in the ... earlier in this presentation.

837
01:01:56,540 --> 01:02:01,140
The WAVE browser extension both for Chrome and Firefox.

838
01:02:01,720 --> 01:02:08,340
They stopped developing the one for Firefox because Firefox made some changes that basically made it,

839
01:02:09,200 --> 01:02:15,860
you know, impossible to maintain. Firefox then made changes that now allow them to continue development.

840
01:02:16,160 --> 01:02:19,300
The WAVE browser extension is one of your baseline tools.

841
01:02:19,620 --> 01:02:23,480
You turn it on, it will show you many of the errors.

842
01:02:23,480 --> 01:02:30,840
Now, any of these automated tools are only going to catch on average 30% of errors.

843
01:02:30,840 --> 01:02:36,380
Okay just so you know and as you begin to use it you'll see things that it's missing.

844
01:02:37,980 --> 01:02:42,980
There's also the aXe tool, which is a free browser tool.

845
01:02:42,980 --> 01:02:45,540
Once again, you run this on a particular page.

846
01:02:45,920 --> 01:02:51,540
There's also aXe Core, which I know Seth has presented on during our lightning talks.

847
01:02:51,900 --> 01:02:58,660
And this can basically, as you're developing, it's checking, it's checking, it's checking, so it's a wonderful tool.

848
01:02:58,660 --> 01:03:05,260
And actually, Marcy Sutton, who's presenting next month, is one of the key contributors to that product.

