# Accessibility 101
##  with Margie Chubin & Girl Develop It (GDI) Chicago - Tuesday, October 2, 2018
[View recording](https://www.youtube.com/watch?v=-tH8QpIdU_E)

[Narration]: The Chicago Digital Accessibility and Inclusive Design Meetup presents Accessibility 101 with Margie Chubin.

[Margie Chubin]: So as Dennis said, this Accessibility 101. I've been coming to this meetup for a couple of months, so I'm a little bit new to the field, too. But I've been studying accessibility for like a couple years. As Dennis said, use that hash tag, it's really awesome. Definitely follow what he's doing on Twitter, because he's always tweeting out really great links too. And then, I also posted my slides at bit.ly/Margie-A11Y101

So as I said, my name is Margie, my pronouns are she her hers, I forgot my button, I do have one. I'm a Software Engineer at Sprout Social. I like cooking, traveling, eating food and also eating food while traveling. So here's a good picture of me eating food in Rome. I was really happy about that.

So my Twitter handle is @MargarineMargie Fun fact, somebody asked me if that was what my name was short for, and I said "nope that's a substitute for butter."

[Laughter]

So that's how I came about a couple of years ago.

19
00:01:26,680 --> 00:01:33,020
So as I said, my slides are posted online. We can share that link, so you can look over it my content later,

20
00:01:33,020 --> 00:01:34,340
click on my links.

21
00:01:35,160 --> 00:01:41,580
So as Dennis also said, this is a promo for the Web Accessibility Class that I am featuring on Saturday.

22
00:01:41,580 --> 00:01:44,560
I'm really excited to get really deep into a lot of these topics,

23
00:01:45,200 --> 00:01:48,560
but today we are just going to do an overview and it will be really fun.

24
00:01:51,120 --> 00:01:56,760
So our goals for today, we are going to learn about different types of disabilities,

25
00:01:56,760 --> 00:01:58,760
maybe the challenges that they face,

26
00:01:59,360 --> 00:02:01,360
how we measure accessibility,

27
00:02:01,900 --> 00:02:07,940
and then how designing and developing with accessibility in mind will improve the web for everyone

28
00:02:09,380 --> 00:02:11,760
So why accessibility? Why you guys here?

29
00:02:11,760 --> 00:02:12,620
I don't know.

30
00:02:14,220 --> 00:02:16,240
So here's my definition for today,

31
00:02:16,240 --> 00:02:22,020
that web accessibility is making our products as usable by as many people as possible,

32
00:02:22,440 --> 00:02:24,860
including users with disabilities.

33
00:02:25,780 --> 00:02:30,140
So we want to ... we know that it's not perfect right now,

34
00:02:30,140 --> 00:02:34,760
but we want to intentionally include everyone especially users disabilities,

35
00:02:35,140 --> 00:02:38,840
and we want to fix it because we know it can be fixed.

36
00:02:39,780 --> 00:02:41,980
So let's go over "a one one y."

37
00:02:41,980 --> 00:02:43,980
What is that, I've seen that everywhere.

38
00:02:44,180 --> 00:02:46,220
I found this picture here.

39
00:02:46,420 --> 00:02:50,200
It shows how there are 11 letters between the "a" and the "y,"

40
00:02:50,740 --> 00:02:55,400
and that's where we got accessibility ... "a,"  11 letters, and then "y."

41
00:02:59,800 --> 00:03:03,940
So we're here because we can't assume anything about our users.

42
00:03:03,940 --> 00:03:08,700
If you work in product at all, you know that your users don't look like you.

43
00:03:09,060 --> 00:03:12,500
They don't have the same abilities, they're not in the same context,

44
00:03:12,880 --> 00:03:16,940
they might not be using a keyboard or a mouse or a modern web browser.

45
00:03:16,940 --> 00:03:22,500
Maybe they're on IE11 and maybe they're not even on a desktop computer.

46
00:03:22,500 --> 00:03:23,860
Maybe it's on their mobile device.

47
00:03:24,260 --> 00:03:28,600
So there's a lot of things that we can't assume, this is why we do user research,

48
00:03:28,600 --> 00:03:32,700
user testing, we test what we put out to see if people are actually using it.

49
00:03:34,300 --> 00:03:37,500
So we have to think about users with disabilities in the same way.

50
00:03:37,500 --> 00:03:42,860
So some of our users might have disabilities and they shouldn't have to out themselves,

51
00:03:42,860 --> 00:03:47,820
They shouldn't have to say, "I have a disability and your website it's not useful for me."

52
00:03:48,580 --> 00:03:50,540
They should just be able to use your website.

53
00:03:50,540 --> 00:03:54,560
You shouldn't say you can't come in the building because I don't have a ramp for you.

54
00:03:54,560 --> 00:03:56,980
You should just let everyone in your building.

55
00:03:57,680 --> 00:04:00,280
So yeah ...

56
00:04:01,200 --> 00:04:05,320
So I've got the social model of disability up on the slides here,

57
00:04:06,200 --> 00:04:11,580
and it is that disability is a mismatch between an individual and the environment

58
00:04:12,040 --> 00:04:18,060
and this is in contrast to the old medical model, which is that people need to be fixed.

59
00:04:20,120 --> 00:04:26,940
So we're not saying, you are deaf, you need to go fix yourself, or it's your fault that your a dog person.

60
00:04:27,300 --> 00:04:33,240
You're deaf, so here is a space where you can also be included by providing captions.

61
00:04:34,640 --> 00:04:41,060
So we're here because the web has barriers to some people, and we want to fix that.

62
00:04:41,060 --> 00:04:44,220
We want to make sure everyone can come in our buildings.

63
00:04:44,820 --> 00:04:46,900
So we all experience disabilities, sometimes.

64
00:04:48,280 --> 00:04:50,800
So we're going to talk about temporary disabilities.

65
00:04:50,800 --> 00:04:57,060
In what way have you experienced a temporary disability in the past few weeks?

66
00:04:58,420 --> 00:05:04,560
There's some examples to the right, such as you temporarily broke your arm,

67
00:05:04,760 --> 00:05:08,360
or you have an ear infection and you can't hear.

68
00:05:08,360 --> 00:05:13,100
I'm getting over being sick because the weather keeps changing, so my hearing's a little down.

69
00:05:14,880 --> 00:05:19,720
Maybe there's a bartender shaking something right next to you and you can't hear what your friends trying to say.

70
00:05:20,000 --> 00:05:24,000
So temporarily, we're all disabled, all the time, and

71
00:05:25,020 --> 00:05:29,900
that gives us a little bit of empathy, but it can't really like give us the full experience of disabilities.

72
00:05:30,300 --> 00:05:36,480
But it's so important to think about that anybody can be disabled at any time and

73
00:05:37,380 --> 00:05:39,880
we'll just think about that as we go through

74
00:05:40,260 --> 00:05:42,260
with talking about disabilities.

75
00:05:43,280 --> 00:05:47,240
And then, the other thing we obviously have to mention is inclusive design.

76
00:05:47,480 --> 00:05:51,500
So this is where we all benefit when things are designed more inclusively.

77
00:05:51,820 --> 00:05:56,980
Better design, making things more simple, that's going to benefit everyone, not just users with disabilities.

78
00:05:57,580 --> 00:06:04,080
An example that a friend in this room mentioned to me the other day was the crosswalk buttons

79
00:06:04,540 --> 00:06:06,760
that make noise when it's time to cross the street.

80
00:06:07,100 --> 00:06:11,440
So you can see the sign that says, like the person or don't walk,

81
00:06:13,240 --> 00:06:17,760
but if you have low vision and you want to cross the street, you'll hit the button and it will say

82
00:06:17,980 --> 00:06:20,320
time to cross, walk sign on,

83
00:06:20,820 --> 00:06:23,520
so just make a noise depending on what city you're in.

84
00:06:24,020 --> 00:06:27,100
And it would also benefit you if you're on your phone and you weren't paying attention.

85
00:06:28,060 --> 00:06:32,640
So fixing accessibility problems, making sure things are available on multiple formats,

86
00:06:32,640 --> 00:06:37,300
that's just gonna fix a lot of usability problems and fix things for everyone.

87
00:06:40,000 --> 00:06:42,480
So here's the main topic of the day.

88
00:06:42,480 --> 00:06:46,760
The web was not built for everyone, but we can do something about it.

89
00:06:47,180 --> 00:06:54,480
So I want to talk about why it's not built for everyone, what are the challenges we're facing with it

90
00:06:54,620 --> 00:06:56,740
and then what also we can do about it.

91
00:06:58,740 --> 00:07:00,940
So whose job is accessibility?

92
00:07:01,620 --> 00:07:03,180
Thinking emoji

93
00:07:04,180 --> 00:07:05,900
So we're gonna do a roll call.

94
00:07:06,700 --> 00:07:09,540
So raise your hand if you are a designer.

95
00:07:10,880 --> 00:07:13,040
Alright, so looks like maybe half of you.

96
00:07:13,520 --> 00:07:16,180
Raise your hand if you are a developer.

97
00:07:17,400 --> 00:07:21,920
It looks like about the other half, but I'm guessing there's a few of you that are not.

98
00:07:22,300 --> 00:07:25,480
Anyone here project or product manager?

99
00:07:27,020 --> 00:07:28,100
Nobody.

100
00:07:28,880 --> 00:07:29,780
QA?

101
00:07:30,860 --> 00:07:33,260
Anything else today, I'm not sure and I want to be inclusive.

102
00:07:35,060 --> 00:07:36,120
Nope?

103
00:07:36,340 --> 00:07:40,900
Where you going out your self, that's fine, cool, not all of you are, but guess what ...

104
00:07:41,200 --> 00:07:45,000
accessibility is everybody's job and responsibility.

105
00:07:45,820 --> 00:07:49,480
So, did anyone have anything else to say to that?

106
00:07:49,480 --> 00:07:54,620
Oh yeah, so we're just here to talk about how we can build accessibility into every step of the process,

107
00:07:55,000 --> 00:07:57,000
to improve the web for everyone.

108
00:07:57,680 --> 00:08:01,700
So first we can't do that without talking about what are the types of disabilities.

109
00:08:01,700 --> 00:08:03,500
So I have emojis next to them.

110
00:08:03,900 --> 00:08:09,100
I like emojis. So sorry. There's gonna be a lot of them, if you don't like them.

111
00:08:09,760 --> 00:08:15,720
[Indecipherable] accessibility according to people with disabilities. There's a Twitter thread, someone said,

112
00:08:16,000 --> 00:08:21,500
if you have a disability, what is the most frustrating thing about the web to you and why?

113
00:08:21,980 --> 00:08:26,940
So that's just a really interesting thread and someone wrote something up about it. Click that on your own time.

114
00:08:30,200 --> 00:08:33,120
So the other thing I have to mention

115
00:08:33,580 --> 00:08:37,960
sorry, I want to mention all of these things up front, so I don't accidentally forget to define them later.

116
00:08:38,440 --> 00:08:46,940
Assistive technology, this is technology that is physical, or is software that helps you just accomplish your task.

117
00:08:47,500 --> 00:08:53,980
So users with disabilities are often going to use assistive technologies to access content on the web

118
00:08:54,300 --> 00:08:57,780
and we have to think about that when we're designing and developing your content.

119
00:08:58,180 --> 00:09:05,920
And then ... accessing physical situations, you might use a wheelchair or a hearing aid or two,

120
00:09:06,160 --> 00:09:12,380
accessing the web or devices you might use a screen reader or an alternative input method,

121
00:09:12,580 --> 00:09:14,580
the mouse or even a keyboard.

122
00:09:15,520 --> 00:09:21,540
But a screen reader is a piece of software that's gonna convey what's on the screen to a user,

123
00:09:21,540 --> 00:09:23,540
usually in the form of reading it out.

124
00:09:26,360 --> 00:09:28,560
So the first one is hearing disabilities

125
00:09:28,560 --> 00:09:34,220
and this is going to range from users who are completely deaf to users that are hard of hearing.

126
00:09:34,580 --> 00:09:39,240
and then the range of hearing within the hard-of-hearing is gonna go from pretty severe

127
00:09:39,240 --> 00:09:43,060
to just a little bit of hearing loss and this is going to include

128
00:09:43,520 --> 00:09:50,620
people that have been deaf since they were born to elderly folks who are losing their hearing

129
00:09:50,620 --> 00:09:53,200
with maybe your parents are already starting to lose their hearing.

130
00:09:53,840 --> 00:10:00,140
It's affecting a lot of people, so we know that audio should not be the only form of information, ever.

131
00:10:00,520 --> 00:10:03,540
So we want to provide captions and transcripts,

132
00:10:04,240 --> 00:10:08,380
and then also, this is from two years ago or something,

133
00:10:08,860 --> 00:10:12,000
but 85% of Facebook videos are watched without sound

134
00:10:12,300 --> 00:10:16,620
and most of us are scrolling through Facebook on the train and don't have our headphones in,

135
00:10:17,000 --> 00:10:19,160
don't care what the sound is anyways.

136
00:10:19,520 --> 00:10:22,860
So a lot of them are without sound, so it's really important that it has captions,

137
00:10:22,860 --> 00:10:24,860
otherwise you're gonna lose everyone.

138
00:10:28,900 --> 00:10:31,300
So next one is visual disabilities.

139
00:10:31,300 --> 00:10:38,100
And, this again is also a range of people who have completely lost their sight, they're legally blind,

140
00:10:38,100 --> 00:10:42,820
people with low vision and people who are color blind are also included in this.

141
00:10:43,680 --> 00:10:47,280
So some of them wear glasses or contacts, but some of them don't.

142
00:10:47,280 --> 00:10:53,520
Some of them can't correct their vision, and many of them use screen readers or magnification software.

143
00:10:55,020 --> 00:11:00,120
Here's a little chart about color blind people and it is why I hate pie charts.

144
00:11:00,380 --> 00:11:06,160
The the whole circle is gray and on the legend says because I'm color blind.

145
00:11:07,140 --> 00:11:10,020
And pie charts are just not great graphs to begin with,

146
00:11:10,020 --> 00:11:13,500
so and that if you're not going to use color contrast within that,

147
00:11:13,500 --> 00:11:16,140
then it's just going to look like that to some people.

148
00:11:16,140 --> 00:11:18,140
No data is conveyed.

149
00:11:19,340 --> 00:11:23,520
So colorblind users or people who have low vision,

150
00:11:23,980 --> 00:11:26,400
they're going to rely on other cues for information.

151
00:11:27,280 --> 00:11:30,720
So you don't ever want to use color alone to convey information.

152
00:11:31,280 --> 00:11:32,680
So more on that later.

153
00:11:33,400 --> 00:11:37,660
So what are some other things we can do for users with visual disabilities.

154
00:11:38,980 --> 00:11:42,520
The content should be legible when zoom to 200%.

155
00:11:42,880 --> 00:11:45,200
Some users are going to be magnifying their screen.

156
00:11:45,200 --> 00:11:49,340
I know, even on my phone, I have my text a little bit magnified

157
00:11:49,340 --> 00:11:52,800
and I'm pretty young and don't have bad vision at all.

158
00:11:53,180 --> 00:11:56,300
But this has to do with responsive design.

159
00:11:56,560 --> 00:12:01,060
Basically, if you zoom in, it's kind of the same as making your screen smaller.

160
00:12:01,420 --> 00:12:07,280
So the contents should all flow and stay ... to stay in the right place.

161
00:12:07,280 --> 00:12:10,980
And you shouldn't have to scroll horizontally in order to see the rest of the content.

162
00:12:12,440 --> 00:12:15,500
So responsive design we know that's good design.

163
00:12:15,500 --> 00:12:21,040
So if we make our designs responsive, then it should work for a user who is zooming in,

164
00:12:21,540 --> 00:12:23,960
even to the extreme of 400%.

165
00:12:25,480 --> 00:12:30,100
So the next thing that I'm going to talk about, a couple of times within this presentation,

166
00:12:30,100 --> 00:12:33,640
is that, the page should be accessible using just the keyboard.

167
00:12:34,800 --> 00:12:40,700
This is because screen readers and using the keyboard without a mouse,

168
00:12:40,700 --> 00:12:43,060
you can't see the mouse pointer where it is.

169
00:12:43,540 --> 00:12:50,180
It's going to be using just the page, so it needs to be able to go through the page just using the keyboard.

170
00:12:51,680 --> 00:12:55,780
You'd be surprised how many pages you can't just use the keyboard for.

171
00:12:57,240 --> 00:13:01,040
And, of course, I'm going to talk about that later, that's something that bothers me.

172
00:13:01,040 --> 00:13:09,080
The next thing, sufficient color contrast and this is for users with low vision and also color blind users.

173
00:13:09,740 --> 00:13:16,500
They need like contrasts like white text on a grey background, for example.

174
00:13:16,900 --> 00:13:23,000
Otherwise, they just won't be able to focus on that content, they won't be able to see what you're doing.

175
00:13:23,260 --> 00:13:29,720
So there's really easy ways to track your contrast, such as the aXe Chrome extension, a really great tool,

176
00:13:30,060 --> 00:13:33,840
or WebAIM has a contrast checker that I like to use.

177
00:13:34,580 --> 00:13:40,840
Also another thing that I write about that made me kind of angry a few years ago was

178
00:13:40,840 --> 00:13:46,000
pop-ups and I was like, yeah, pop-ups are annoying but they're worse for the blind.

179
00:13:46,000 --> 00:13:49,680
Can you imagine, you can't see the screen and something pops up

180
00:13:49,680 --> 00:13:52,200
and there's no consistent way to close it.

181
00:13:52,200 --> 00:13:56,000
The X is on the left or right, maybe you can press escape to close it.

182
00:13:56,280 --> 00:13:58,180
You don't know, so they're inconsistent.

183
00:13:58,180 --> 00:14:03,000
So we want then to handle those correctly if we're going to use them, or not use them.

184
00:14:05,180 --> 00:14:10,080
So the next disability we're going to talk about is physical disabilities.

185
00:14:10,600 --> 00:14:16,740
These are folks who have limited movement, muscle control, or fine motor skills.

186
00:14:17,100 --> 00:14:23,220
Using a mouse often requires a great deal of motor skills, so they're most likely not using a mouse.

187
00:14:23,220 --> 00:14:28,760
So this is where you want to make sure that your content is available to the keyboard

188
00:14:28,760 --> 00:14:32,180
or other alternative input methods.

189
00:14:33,080 --> 00:14:40,080
And what can we do for them, the keyboard thing, the web page should be accessible using the keyboard.

190
00:14:40,440 --> 00:14:43,880
We don't want to use complicated motions, such as clicking and dragging.

191
00:14:43,880 --> 00:14:50,340
We want to find alternatives to that or just provide alternatives, like for file dropping,

192
00:14:50,340 --> 00:14:55,220
normally you can use the actual file picker, but you can also click and drag,

193
00:14:55,220 --> 00:14:57,920
and I think that's probably a good alternative.

194
00:14:58,620 --> 00:15:01,540
And then also we want to make navigation easier.

195
00:15:01,860 --> 00:15:07,060
Usually, web pages have a lot of content to go through, the navigations are complicated.

196
00:15:07,520 --> 00:15:10,380
But we have this thing called a skip to main content link,

197
00:15:10,860 --> 00:15:16,080
which will allow a user to skip over the navigation and get right to the content.

198
00:15:16,820 --> 00:15:18,660
I have an example here.

199
00:15:18,660 --> 00:15:22,400
This is Facebook, with all my personal stuff removed.

200
00:15:24,240 --> 00:15:26,720
So basically, when you tap into Facebook,

201
00:15:27,100 --> 00:15:30,320
the first thing on the page is going to be the top bar,

202
00:15:30,720 --> 00:15:36,880
and it says jump to, sections of this page, other pages on Facebook,

203
00:15:36,880 --> 00:15:41,640
Accessibility Help, and you can jump to a part of the page,

204
00:15:41,640 --> 00:15:44,940
and this is a very extreme, like well thought out example.

205
00:15:45,320 --> 00:15:50,540
Most pages would probably just have like a skip to main content, just let you go to the main content.

206
00:15:51,040 --> 00:15:54,440
But this allows you to go to like anything. It's really cool.

207
00:15:54,440 --> 00:15:55,940
I recommend playing around with it.

208
00:16:03,860 --> 00:16:07,160
It's really hard not to click more than one ...

209
00:16:08,100 --> 00:16:11,280
... sorry for the previews of the next slide.

210
00:16:12,800 --> 00:16:16,560
So the final disability we're going to talk about is cognitive disabilities.

211
00:16:16,560 --> 00:16:23,500
In my opinion, the hearing one was the easiest, because all we need to do is provide captions or transcripts,

212
00:16:23,500 --> 00:16:26,900
and this one is the hardest. This is the least visual.

213
00:16:26,900 --> 00:16:32,420
You don't know by looking at someone what their processing is like, or how they think at all.

214
00:16:33,060 --> 00:16:40,780
So these are users with difficulty with learning, memory, attention, problem solving, and comprehension.

215
00:16:41,220 --> 00:16:49,560
Could be Autism, or this could be like Dyslexia, this could be just a very wide variety of things.

216
00:16:49,560 --> 00:16:52,420
This could be you're getting old and you're very forgetful.

217
00:16:54,220 --> 00:16:57,680
So some of them really use screen readers and other assistive technologies,

218
00:16:57,800 --> 00:17:02,060
but it's probably gonna be just normal users trying to use your site.

219
00:17:02,420 --> 00:17:05,080
I know they're gonna get frustrated a lot more easily.

220
00:17:06,120 --> 00:17:09,980
So they're gonna benefit from a simpler user experience, and then ...

221
00:17:10,700 --> 00:17:15,020
also just less text and avoiding timed elements, like

222
00:17:15,940 --> 00:17:17,800
this is gonna expire in five minutes.

223
00:17:17,900 --> 00:17:20,800
That's really scary. It might take me a really long time to fill out this form.

224
00:17:21,540 --> 00:17:22,980
And then, flashing elements.

225
00:17:22,980 --> 00:17:24,900
We don't want to do that. That's just scary.

226
00:17:24,900 --> 00:17:29,660
We don't ... I think we're done with text flying across the screen.

227
00:17:29,980 --> 00:17:32,280
I think we're just done with that.

228
00:17:33,180 --> 00:17:37,620
And then also forms. We want to make sure we have really descriptive instructions

229
00:17:38,040 --> 00:17:40,660
and good form errors, that tell you what you need to fix,

230
00:17:40,660 --> 00:17:45,020
so you're not just trying to review your form for ten minutes, trying to figure out the website.

231
00:17:47,140 --> 00:17:49,400
So great, we talked about disabilities.

232
00:17:49,400 --> 00:17:54,380
So the next section, the next thing we're going to talk about is how do we know if something is compliant,

233
00:17:54,780 --> 00:17:58,800
and there's got to be something I can do, some boxes I can check off,

234
00:17:59,020 --> 00:18:03,420
so what I know if I'm compliant. So let's try and talk about that a little bit.

235
00:18:04,240 --> 00:18:07,160
So this is the Web Content Accessibility Guidelines.

236
00:18:07,160 --> 00:18:09,160
This is the standard for measuring ...

237
00:18:09,940 --> 00:18:12,700
like what is accessible, is your content accessible?

238
00:18:13,380 --> 00:18:19,480
We're measuring it against these four categories that all have like kind of guidelines within them,

239
00:18:19,480 --> 00:18:25,660
They have a lot of information about how something is accessible, what fails this.

240
00:18:25,980 --> 00:18:32,340
I recommend looking at it, but also not, because it's a lot to look at, especially for a beginner.

241
00:18:32,340 --> 00:18:36,320
It's just a huge wall of text with a ton of stuff, very comprehensive.

242
00:18:39,220 --> 00:18:46,080
So the four categories that we had in there are Perceivable, Operable, Understandable and Robust.

243
00:18:46,880 --> 00:18:50,860
And they're going to deal with the different ways that we use technology.

244
00:18:51,240 --> 00:18:53,700
So Perceivable ... can it be perceived?

245
00:18:54,120 --> 00:18:56,680
And notice it doesn't say, can it be seen.

246
00:18:57,100 --> 00:19:02,820
Because perceived is not necessarily seen and it's not necessarily heard. It could even be felt.

247
00:19:02,880 --> 00:19:05,120
So, can it be perceived.

248
00:19:05,500 --> 00:19:07,720
Operable. Can it be used?

249
00:19:08,180 --> 00:19:14,160
Can it be comfortably, like, not just something that someone could use if they figured it out,

250
00:19:14,160 --> 00:19:17,080
over a couple hours, could they use it comfortably?

251
00:19:17,720 --> 00:19:23,540
Understandable. Could it be understood? Like, is it intuitive?

252
00:19:24,020 --> 00:19:25,860
Do you know what to do when you look at it?

253
00:19:25,860 --> 00:19:29,700
Or is it just a huge wall of text that doesn't tell you anything.

254
00:19:30,680 --> 00:19:35,220
And then Robust is the last one and that is, does it support assistive technology,

255
00:19:35,580 --> 00:19:40,260
if at all? A strong arm next to it. It should be strong and be able to handle

256
00:19:40,260 --> 00:19:43,800
whatever assistive technology someone is using.

257
00:19:44,960 --> 00:19:47,760
So Perceivable is the first category.

258
00:19:48,600 --> 00:19:51,460
Put eyes, ears, and a little pointer for touch.

259
00:19:52,520 --> 00:19:57,780
So users can perceive the content and the information is available multiple formats.

260
00:19:57,920 --> 00:20:00,260
So there are multiple formats is the key here.

261
00:20:00,560 --> 00:20:05,180
People learn in different ways, people prefer their content in different ways.

262
00:20:05,880 --> 00:20:13,340
So that doesn't just apply to people with disabilities, sometimes they don't want to listen to a full podcast,

263
00:20:13,340 --> 00:20:15,340
they just want to scan the transcript.

264
00:20:15,660 --> 00:20:22,160
There's just many times when you, when one format isn't working for you

265
00:20:22,160 --> 00:20:24,160
and you're like happy that there is another format.

266
00:20:24,540 --> 00:20:28,180
So this has to do with text alternatives for images.

267
00:20:28,340 --> 00:20:30,960
This is about captions, too.

268
00:20:31,260 --> 00:20:34,640
Colors isn't the only thing being used to convey information,

269
00:20:34,640 --> 00:20:37,680
and that the color contrast is enough for low-sighted users.

270
00:20:37,920 --> 00:20:39,840
So literally, it is, can it be seen?

271
00:20:40,380 --> 00:20:44,160
And the contrast that is recommended is the four point five to one.

272
00:20:44,840 --> 00:20:50,400
So you just want to keep playing with your colors, or use a tool that will tell you

273
00:20:50,880 --> 00:20:59,180
if your colors are the right contrast, or might even recommend a color to use that is the right contrast.

274
00:20:59,520 --> 00:21:01,320
I've seen a tool like that.

275
00:21:02,620 --> 00:21:05,660
So, I have a slide here about text alternatives

276
00:21:06,340 --> 00:21:11,460
and this is as easy as an image tag, this is HTML.

277
00:21:11,460 --> 00:21:18,600
If people don't know HTML, I'll try to talk about it as much as I can, explain what I'm talking about.

278
00:21:18,600 --> 00:21:24,140
But basically, it just requires a source for the image, the SRC, and the alt tag.

279
00:21:25,360 --> 00:21:28,520
And the alt tag should just be a description of the image.

280
00:21:28,520 --> 00:21:31,240
This is not supposed to be the image, next to it.

281
00:21:31,240 --> 00:21:36,580
It is supposed to be cat, sticking out its tongue image, show you can picture that.

282
00:21:36,860 --> 00:21:40,440
So basically, non-decorative images should have text alternatives

283
00:21:40,980 --> 00:21:48,320
and you want to use the empty value for the alt tag to let the screenreader to skip over an image

284
00:21:48,620 --> 00:21:51,660
if it is not, or if it is decorative.

285
00:21:52,300 --> 00:21:54,540
If the image is important, you need a description.

286
00:21:54,540 --> 00:21:58,500
If it's not important, tell the screen reader don't try to read it.

287
00:21:59,180 --> 00:22:03,260
So, I have a caption on the right that I'm sure you guys have read by now, if you can see.

288
00:22:03,820 --> 00:22:11,000
It's two guys and four cats in the picture and one of the guys seems to be doing something to the cats,

289
00:22:11,000 --> 00:22:12,320
like putting something on them.

290
00:22:12,820 --> 00:22:14,440
So the first guy says

291
00:22:15,340 --> 00:22:17,340
"Oh, Hi; I'm here from the internet"

292
00:22:17,580 --> 00:22:18,780
and the second guy says,

293
00:22:18,780 --> 00:22:19,720
"What are you doing?"

294
00:22:20,140 --> 00:22:21,480
And the first guy says,

295
00:22:21,660 --> 00:22:23,660
"Gluing captions to your cats."

296
00:22:23,660 --> 00:22:28,320
So this is probably like what a few of us want to do.

297
00:22:28,320 --> 00:22:34,320
Like we see images without alt text and we're like, "can't we just glue captions onto here?"

298
00:22:34,460 --> 00:22:36,020
Which it would not be that hard.

299
00:22:36,400 --> 00:22:40,660
So this is from xkcd. Funny comics.

300
00:22:41,680 --> 00:22:43,740
So the next one we have, Operable.

301
00:22:44,460 --> 00:22:49,960
And this is where we want to be able to navigate and use the page with the mouse, but also the keyboard.

302
00:22:50,980 --> 00:22:57,020
So it should be available using the keyboard only, but this also is about just usability in general,

303
00:22:57,480 --> 00:23:01,860
We want to not trap our users anywhere; if they get into a menu or something,

304
00:23:01,860 --> 00:23:04,020
they should be able to get out pretty easily.

305
00:23:04,780 --> 00:23:10,840
Imagine you go into a menu expecting just to see what's there and you just can never get out of there.

306
00:23:11,340 --> 00:23:16,280
And then we want our logical focus order, so that it's usable, we know where we are at all times,

307
00:23:16,940 --> 00:23:21,300
and we can navigate our pages correctly.

308
00:23:22,500 --> 00:23:27,820
So our next one, the third category, we're going to talk about understandable.

309
00:23:29,440 --> 00:23:34,220
This is that users should be able to understand the interface and its information.

310
00:23:34,820 --> 00:23:37,740
So our interfaces should be predictable

311
00:23:38,240 --> 00:23:41,740
and the navigation should also be consistent on every page.

312
00:23:42,580 --> 00:23:45,220
And then more about forms.

313
00:23:45,220 --> 00:23:49,080
Forms should have labels, instructions and errors.

314
00:23:49,420 --> 00:23:54,880
So you should be able to see a form, know exactly what to do, it should be labeled, have instructions,

315
00:23:54,980 --> 00:23:59,740
and then if you mess up, it should tell you what to fix and how to fix it.

316
00:24:01,940 --> 00:24:03,120
And then Robust.

317
00:24:03,520 --> 00:24:06,160
This means that it supports user agents.

318
00:24:06,160 --> 00:24:10,840
So actually not just assistive technology, we want to make sure it supports the browser as well.

319
00:24:11,540 --> 00:24:13,880
So this just means writing good code.

320
00:24:13,880 --> 00:24:18,540
So the half of you that are developers in here, this is really not that hard.

321
00:24:18,940 --> 00:24:21,140
So we'll talk a little bit about that.

322
00:24:21,140 --> 00:24:23,720
There's this thing called semantic HTML,

323
00:24:24,160 --> 00:24:29,440
So we have HTML, the code that builds the websites, and renders things to the page.

324
00:24:29,440 --> 00:24:34,540
But we have semantic HTML, which means that we're using elements that have meaning,

325
00:24:35,540 --> 00:24:37,680
and we know what those are going to do.

326
00:24:37,680 --> 00:24:44,500
Like we can trust that when we want to put a button on the page and we say, like, when we write button,

327
00:24:44,860 --> 00:24:46,120
so that's going to be a button.

328
00:24:46,400 --> 00:24:48,400
And that's going to be handled correctly.

329
00:24:48,780 --> 00:24:53,260
So a little more on that. Lately I think I can talk about semantic HTML for a while.

330
00:24:53,760 --> 00:24:57,200
Definitely going to cover that in the class.

331
00:24:58,040 --> 00:25:01,220
And then, I know I just told you all the stuff about compliance,

332
00:25:01,440 --> 00:25:04,600
but compliance doesn't mean your product is usable.

333
00:25:05,260 --> 00:25:09,380
Just because you've checked off a bunch of boxes, you still need to test it out.

334
00:25:09,780 --> 00:25:18,280
Just because I write all the code perfectly, which I wouldn't, I'm human, doesn't mean it's actually usable.

335
00:25:18,340 --> 00:25:25,240
Unless we do research, at my company with users who have disabilities, and prove that it actually works

336
00:25:25,240 --> 00:25:26,300
and that it's useful.

337
00:25:27,260 --> 00:25:31,140
So you need to listen to your users, no matter what, that's definitely the goal.

338
00:25:31,980 --> 00:25:35,460
Also, with the guidelines, they're not fixed or comprehensive.

339
00:25:37,340 --> 00:25:43,440
We've been talking mostly about WCAG, the Web Content Accessibility Guidelines 2.0,

340
00:25:43,440 --> 00:25:49,020
but 2.1 just came out, and you just know they're going to keep putting the guidelines out.

341
00:25:49,020 --> 00:25:52,480
So if you think about actual user needs and usability,

342
00:25:53,160 --> 00:25:58,620
then you're much more likely to set your up set yourself up for success in the future,

343
00:25:59,020 --> 00:26:05,580
because you're thinking ahead, and the usability problem ... they're going to become the usability standards later.

344
00:26:07,280 --> 00:26:15,240
So, here's an example of ... I provided a ramp for a staircase, but it doesn't look very usable.

345
00:26:15,720 --> 00:26:22,660
It is stairs, there's like three sets of stairs going up and then there's a ramp going alongside it on the side.

346
00:26:23,020 --> 00:26:29,460
But it kind of looks like an amusement ride and not a ramp that I don't think anyone would want to use.

347
00:26:29,460 --> 00:26:32,960
Like anyone with the baby or just how funny is that.

348
00:26:32,960 --> 00:26:37,880
So definitely it looks terrifying, is what I wrote.

349
00:26:38,720 --> 00:26:40,900
But they put a ramp there, right?

350
00:26:41,160 --> 00:26:44,880
So yeah.

351
00:26:45,160 --> 00:26:47,160
So what can we do?

352
00:26:48,980 --> 00:26:49,920
Good question.

353
00:26:50,280 --> 00:26:54,440
So a few tips for designing more accessible products.

354
00:26:54,860 --> 00:26:59,020
So I've mentioned a few of these, but here it is, in a slide.

355
00:27:00,420 --> 00:27:03,620
We want to use colors that have sufficient color contrast.

356
00:27:04,320 --> 00:27:06,480
You don't want to use color alone to convey meaning,

357
00:27:06,820 --> 00:27:14,460
and this means that you should ... you can use color to convey the meaning. but also put some text in there.

358
00:27:14,840 --> 00:27:18,340
Say a username is required,

359
00:27:18,840 --> 00:27:22,400
or username has to have this character in it.

360
00:27:22,640 --> 00:27:24,500
Not just a red box around it.

361
00:27:24,960 --> 00:27:30,600
And then you also want ... you can use an icon, maybe, like you just want to give other visual clues,

362
00:27:30,600 --> 00:27:34,540
even if you're explaining it to the screenreader, explain it to visual users, too.

363
00:27:35,400 --> 00:27:39,700
So designing better forms ... just ... can't state that enough.

364
00:27:39,700 --> 00:27:41,620
The error states should be good.

365
00:27:41,620 --> 00:27:47,660
Don't use placeholders as the label ... you start to type and then you forget, what does this want, anyways.

366
00:27:49,340 --> 00:27:55,760
Just not a good label ... you can use placeholders, but just don't use them as the only labels in there.

367
00:27:56,800 --> 00:28:01,300
So a couple more tips for designing more accessible products,

368
00:28:01,300 --> 00:28:03,460
because they fit on the other slide.

369
00:28:03,880 --> 00:28:07,220
So you want to write clear and concise copy.

370
00:28:07,220 --> 00:28:11,420
This means descriptive links and call-to-action buttons.

371
00:28:12,000 --> 00:28:18,320
We all like to see stuff like, read more, click here, those are not very useful.

372
00:28:18,640 --> 00:28:22,580
Like where this is taking me, learn more about what?

373
00:28:23,060 --> 00:28:27,140
So if you're only looking at the links through the buttons, they should make sense so it should say,

374
00:28:27,720 --> 00:28:31,900
sign up for a free trial, learn more about the iPhone 10.

375
00:28:32,600 --> 00:28:34,540
Those are way more useful for everyone.

376
00:28:35,560 --> 00:28:38,440
So you want to write copy for text alternatives.

377
00:28:38,440 --> 00:28:44,680
If you're a designer, like you should say, here's the image I designed for you or the image that I want with it.

378
00:28:45,360 --> 00:28:48,780
But you should also say, this is not an important image,

379
00:28:48,780 --> 00:28:54,960
or just the description of this image is, three friends holding hands.

380
00:28:55,720 --> 00:29:03,100
That's useful, and then also, I think it'd be awesome as my designer put expected keyboard navigation

381
00:29:03,100 --> 00:29:04,380
in the design.

382
00:29:05,000 --> 00:29:09,060
Told me ... it should not only told me how it works when you click it,

383
00:29:09,060 --> 00:29:11,360
but also what the keyboard should do with it.

384
00:29:12,460 --> 00:29:19,140
So I guess that the image here is a click here and with no context.

385
00:29:20,840 --> 00:29:24,020
So a few tips for developing more accessible products.

386
00:29:26,080 --> 00:29:31,680
So the entire page should be useful with the keyboard and semantic HTML is actually going to help with that.

387
00:29:32,240 --> 00:29:35,720
I know we should give images text alternatives.

388
00:29:36,120 --> 00:29:38,780
So some more semantic HTML here.

389
00:29:40,520 --> 00:29:45,360
Well first of all, a quick HTML lesson for anyone who doesn't know HTML the room,

390
00:29:45,800 --> 00:29:52,920
We use div elements, it's just d-i-v, to mean a division or a section.

391
00:29:52,920 --> 00:29:59,720
We use them as containers and we could use some [indecipherable] to apply some styles on top of it.

392
00:30:00,620 --> 00:30:01,680
But we shouldn't.

393
00:30:03,820 --> 00:30:08,800
They are often used improperly they should be used for containers or moving things around or ...

394
00:30:09,040 --> 00:30:14,120
layouts, but they should not be used for actual elements, especially buttons.

395
00:30:14,720 --> 00:30:20,600
So this is definitely something I see a lot. I'm going to show you some examples in a minute, too.

396
00:30:23,920 --> 00:30:27,580
So yes, we want to use HTML elements that have meaning ...

397
00:30:28,140 --> 00:30:33,380
so that the browser knows what it is and so that assistive technologies can announce them properly.

398
00:30:34,260 --> 00:30:37,460
So it's going to be more accessible just to every device.

399
00:30:38,300 --> 00:30:41,940
And so, we have button tags, so we should use them.

400
00:30:42,900 --> 00:30:46,360
Screen readers can announce all the elements like I said,

401
00:30:46,840 --> 00:30:52,840
and you can also list things by headings, by links, you can navigate between sections more easily.

402
00:30:53,240 --> 00:30:58,380
And if we, as developers, label the elements, and use the right elements,

403
00:30:58,740 --> 00:31:02,720
then it'll be a lot easier for everyone to navigate the website.

404
00:31:03,260 --> 00:31:04,820
So I have a demo ...

405
00:31:06,640 --> 00:31:09,960
We shouldn't do live demos. Live demos are bad I'm gonna do one.

406
00:31:10,500 --> 00:31:12,740
Not to live, I've coded most of it.

407
00:31:12,880 --> 00:31:18,180
But this demo is going to show some bad semantic HTML and how we can make it better.

408
00:31:18,580 --> 00:31:25,660
And for examples and they're all examples of code that I've seen, either in the wild on random websites

409
00:31:25,940 --> 00:31:27,760
or in my code base at work.

410
00:31:28,420 --> 00:31:33,740
And so we're gonna look at them. Did this in Codepen.

411
00:31:34,400 --> 00:31:38,200
So hopefully you all can see ... what is going on.

412
00:31:38,200 --> 00:31:43,980
I'm not sure if the live stream will be able to see this, I'll just talk about as best I can what is going on.

413
00:31:44,460 --> 00:31:52,700
The theme is for the code we're not very high contrast, but basically we have four buttons here

414
00:31:53,720 --> 00:31:55,640
And they all look the same, right?

415
00:31:55,640 --> 00:31:56,980
Or at least pretend they do.

416
00:31:58,540 --> 00:32:03,420
Messes with the padding and stuff too much but we have four buttons here,

417
00:32:03,420 --> 00:32:08,820
and I'm just gonna go through them and test this website, test my buttons,

418
00:32:09,480 --> 00:32:17,840
as if we were looking for like accessibility here, or just what is going on with these buttons.

419
00:32:17,840 --> 00:32:23,640
So, I'm going to click on each button

420
00:32:24,220 --> 00:32:27,580
and all I have it doing is saying which button was clicked.

421
00:32:27,580 --> 00:32:33,920
It's just reading the text of the button and displaying it and saying it was clicked on the right.

422
00:32:33,920 --> 00:32:35,300
Really fun demo.

423
00:32:35,480 --> 00:32:37,700
So button 1, I clicked it.

424
00:32:37,960 --> 00:32:39,920
Button 2, I clicked it.

425
00:32:39,920 --> 00:32:41,080
This is the boring part.

426
00:32:41,220 --> 00:32:44,580
Button 3, clicked,  button 4, clicked.

427
00:32:44,960 --> 00:32:47,320
So it work with the keyboard, that's great.

428
00:32:47,820 --> 00:32:56,220
Most of us in here would be fine with that, great, ship it, put it in the code base, put it in production, this is fun.

429
00:32:56,680 --> 00:32:59,120
But what about the keyboard?

430
00:33:00,000 --> 00:33:06,560
So I wrote a reset button, that you probably can't see my reset button, but don't worry about it

431
00:33:06,560 --> 00:33:10,660
I just want to, you know, the reset it sometimes, just to restart my demo.

432
00:33:11,040 --> 00:33:17,660
So we're gonna try ... just gonna click up here move the tabbing focus up there,

433
00:33:17,660 --> 00:33:23,100
and then I'm going to tab and hopefully be able to click on all these buttons with the keyboard.

434
00:33:23,700 --> 00:33:26,140
So I'm going to try to tab to the first one

435
00:33:26,900 --> 00:33:34,600
and let's see, what is the first one. I hit enter to activate it and it says button one was clicked.

436
00:33:35,380 --> 00:33:37,620
So let's see what is under the hood.

437
00:33:40,000 --> 00:33:43,040
So I have button one here and ...

438
00:33:43,040 --> 00:33:48,240
I was expecting a button, because it's coded like a button, it doesn't take me anywhere,

439
00:33:48,640 --> 00:33:50,340
but actually it's a link.

440
00:33:50,340 --> 00:33:55,600
So we have an anchor tag here, which is an a with the href

441
00:33:56,380 --> 00:34:01,240
attribute and the href attribute is javascript:void 0,

442
00:34:01,240 --> 00:34:07,680
which is basically, cancel out any navigation that this would have done, and then there's an onclick on this.

443
00:34:08,060 --> 00:34:12,140
That says that will actually do the clicking.

444
00:34:12,140 --> 00:34:18,100
I wrote a function over here that just sets button to say button is clicked.

445
00:34:18,900 --> 00:34:22,440
But, this is the link under the hood and it's just a cancelled out link.

446
00:34:22,440 --> 00:34:26,420
So this is one of the red flags that this should have been a button.

447
00:34:26,660 --> 00:34:30,200
Because you have to cancel out the href, the navigation.

448
00:34:30,460 --> 00:34:32,200
I actually see this all the time,

449
00:34:33,040 --> 00:34:36,100
mostly when you think you want a link,

450
00:34:36,940 --> 00:34:41,880
but it's actually going to do something like bring something up, or like just do something on the page,

451
00:34:42,300 --> 00:34:45,440
and your designer gave you a link, so you're like great, I'll make it a link.

452
00:34:46,340 --> 00:34:52,000
But really, even so you should make it a button and not worry about what it looks like.

453
00:34:52,260 --> 00:34:54,380
In the first pass and then in the second pass,

454
00:34:54,800 --> 00:34:59,160
remove all the styling and make it look like whatever links look like in your application.

455
00:35:00,180 --> 00:35:03,080
So let's try the second one.

456
00:35:04,640 --> 00:35:05,980
We'll reset.

457
00:35:08,220 --> 00:35:14,380
So I'm going to try and tab to my second button,  button one ... where's my button two?

458
00:35:14,380 --> 00:35:16,380
I wonder why I can't focus on it.

459
00:35:18,160 --> 00:35:19,980
Let's see what it is under the hood.

460
00:35:20,120 --> 00:35:21,440
So it was clickable, right?

461
00:35:21,440 --> 00:35:25,380
So it was a button. Most people would say, yeah.

462
00:35:27,000 --> 00:35:28,800
It's not. It's a div.

463
00:35:28,940 --> 00:35:32,280
So remember I mentioned the div? You can use this pretty much for anything,

464
00:35:32,740 --> 00:35:34,620
But should we have used it here?

465
00:35:35,060 --> 00:35:36,120
Not really.

466
00:35:36,120 --> 00:35:40,680
I will explain like how you could have used it here, but we'll get to that in a moment.

467
00:35:41,260 --> 00:35:44,840
But basically, I gave it a role of button, so that's a button, right?

468
00:35:45,300 --> 00:35:46,180
Ah, no.

469
00:35:46,180 --> 00:35:51,460
So the role button, that's ARIA, which we'll talk about also in a couple minutes.

470
00:35:52,200 --> 00:35:55,000
What that is, why that's there ...

471
00:35:55,920 --> 00:35:59,480
but basically that's saying like, I now exist as a button.

472
00:36:00,060 --> 00:36:03,620
But it's not saying, do anything to make it work like a button.

473
00:36:04,060 --> 00:36:07,940
It's just saying, announce it like the screen reader will hit it and say button.

474
00:36:08,620 --> 00:36:12,520
Button two,  or button two, button, however it's going to announce it.

475
00:36:13,240 --> 00:36:19,800
But, so it has an onclick but it doesn't handle the keypress and it also doesn't handle tabbing, right?

476
00:36:20,140 --> 00:36:26,680
I couldn't even get over to it, even if it could handle a keypress, I couldn't even get to it with my keyboard.

477
00:36:27,440 --> 00:36:31,240
So I'm guilty of this, everyone's guilty of this.

478
00:36:31,240 --> 00:36:36,740
We all are like, well, I don't want it to look like an actual button, I just want something that's clickable.

479
00:36:38,400 --> 00:36:42,320
I found a great example that I did 10 months ago and I was like, wow this was me,

480
00:36:42,320 --> 00:36:48,600
and I didn't even handle, you can't talk to it, you can't click on it, you can't like tab to it

481
00:36:48,600 --> 00:36:54,220
and you can't press a button to click on it, but you can click on it just fine and it works all just fine.

482
00:36:54,220 --> 00:36:55,540
So it passed everything.

483
00:36:55,760 --> 00:36:58,040
Like, Wow, [indecipherable].

484
00:36:58,840 --> 00:37:00,980
So, let's look at the next button.

485
00:37:00,980 --> 00:37:03,120
So I see we were able to tab to it.

486
00:37:03,860 --> 00:37:06,720
And let's try hitting Enter.

487
00:37:07,400 --> 00:37:08,480
Just while we're here.

488
00:37:09,120 --> 00:37:13,980
So that wouldn't work. So let's see what happened there. Is this one button?

489
00:37:15,480 --> 00:37:18,520
And the answer is no, still not a button.

490
00:37:18,940 --> 00:37:27,080
But it did handle tabbing to it. So, this is the tabindex zero, puts it in the tabbing order.

491
00:37:27,720 --> 00:37:32,000
So, they stuffed it in the tabbing order already like buttons and links,

492
00:37:32,640 --> 00:37:35,240
but there's stuff that's not, like divs, or text.

493
00:37:36,000 --> 00:37:38,060
So this puts it in the tabbing order.

494
00:37:38,900 --> 00:37:43,740
And then we handled that onclick and then we handled the onkeypress.

495
00:37:44,380 --> 00:37:47,380
So we can look at the onkeypress,

496
00:37:49,140 --> 00:37:54,220
which is the button press function, now we've moved to the right,

497
00:37:56,440 --> 00:38:00,680
and basically we're taking in that click event, the button click,

498
00:38:01,280 --> 00:38:04,000
we're checking to see what button was pressed.

499
00:38:04,520 --> 00:38:13,360
What key was pressed and I checked for the Space bar or the Enter key or Enter or Space bar 13 and 32

500
00:38:13,360 --> 00:38:17,300
and then I basically just called my button click function with that.

501
00:38:17,960 --> 00:38:23,200
So a lot of extra code. Let's see if we can make this any simpler.

502
00:38:24,080 --> 00:38:27,460
So, let's tab over to the fourth button.

503
00:38:27,880 --> 00:38:35,960
1 ... 2 doesn't really exist according to the keyboard, 3 & 4 ... we'll try clicking on it,

504
00:38:36,120 --> 00:38:37,300
and that one worked.

505
00:38:37,300 --> 00:38:40,760
So let's see if we finally made a button.

506
00:38:41,820 --> 00:38:47,440
And this one required a little bit of extra styling and that's what I did is good for.

507
00:38:48,060 --> 00:38:54,680
And have a div around my button but the real thing is the button with just an onclick,

508
00:38:55,340 --> 00:38:59,180
add to class for some styling and it has button four.

509
00:39:00,100 --> 00:39:05,640
That didn't require an extra function, that didn't require tabindex, that didn't require handling the keypress,

510
00:39:06,180 --> 00:39:08,780
and it's just a lot easier. Like, all I type is button.

511
00:39:09,380 --> 00:39:17,440
So, it's amazing like how many times they find stuff with all the other examples that I showed in the code base,

512
00:39:17,440 --> 00:39:24,840
and I'm really trying to just explain that there's ways that we could just write really simple code, write better code,

513
00:39:25,680 --> 00:39:29,080
that'll fix it and we won't up to handle additional things.

514
00:39:29,660 --> 00:39:33,160
So even if you have something really complicated, as long as it's clickable,

515
00:39:33,440 --> 00:39:38,040
most of the time, you can use a button and just take away the styling, worry about that later,

516
00:39:38,040 --> 00:39:42,760
handle anything else later, but it should just work a lot better.

517
00:39:43,560 --> 00:39:48,060
So that was my demo. I think that went well. I hope you thought so.

518
00:39:49,060 --> 00:39:51,520
And good news, we still have more slides.

519
00:39:51,880 --> 00:39:59,880
So now we're going to talk a little bit about ARIA, which means Accessible Rich  Internet Application.

520
00:40:00,560 --> 00:40:07,800
And this defines how custom widgets should be handled, so anything that is not a button or a navigation,

521
00:40:07,800 --> 00:40:13,660
or just a simple things that we used to have the early days of the web,

522
00:40:13,660 --> 00:40:20,620
now we have complicated menus and menu buttons and just all sorts of widgets that are happening,

523
00:40:20,900 --> 00:40:23,500
because we want to do cooler things with the web.

524
00:40:24,080 --> 00:40:27,420
But, how should the web handle that?  We're still try to figure that out.

525
00:40:27,940 --> 00:40:31,860
It's not exactly consistent and we're working on it,

526
00:40:32,080 --> 00:40:39,900
But ARIA is trying to solve that problem by saying, you can describe what your component does

527
00:40:39,900 --> 00:40:48,860
to the screen reader, to your users, by using these additional attributes like aria-label or role,

528
00:40:49,780 --> 00:40:54,020
and then you should use, you can use ARIA to supplement HTML.

529
00:40:54,120 --> 00:40:57,780
So first you want to write great HTML, then you want to style it.

530
00:40:57,780 --> 00:41:03,100
Then, you want to make it all work, and then you want to describe it using ARIA.

531
00:41:04,400 --> 00:41:08,440
But no ARIA is better than bad ARIA.

532
00:41:08,440 --> 00:41:14,640
And this is directly out of the ARIA Authoring Practices, literally in the documentation.

533
00:41:15,080 --> 00:41:16,900
Like, don't use it if you don't understand it.

534
00:41:16,900 --> 00:41:18,980
And I've seen a lot of bad ARIA.

535
00:41:19,520 --> 00:41:23,520
So I can't stress this enough. That's why it's on its own slide.

536
00:41:23,980 --> 00:41:28,920
Definitely look at trying to use it, but it is not something that you just play with,

537
00:41:28,920 --> 00:41:31,300
it's not something to just tack on to anything.

538
00:41:31,840 --> 00:41:37,380
Because, using it wrong is just worse than not using it at all.

539
00:41:38,060 --> 00:41:41,240
Because here you're telling your user what you can expect from something.

540
00:41:41,240 --> 00:41:45,160
So if you say this is a button, and it's not, then it's not a button.

541
00:41:45,840 --> 00:41:49,080
And that's just confusing, that would frustrate any of us.

542
00:41:51,040 --> 00:41:53,600
So ... let that sink in.

543
00:41:54,900 --> 00:41:56,040
[Laugh]

544
00:41:59,600 --> 00:42:01,600
And, we've got some takeaways here.

545
00:42:02,820 --> 00:42:06,200
Hopefully a lot but just a couple on a summary slide.

546
00:42:06,980 --> 00:42:10,860
We want to provide content in alternative formats.

547
00:42:10,920 --> 00:42:16,560
Text is good, because it can be converted to audio, it could be read, it can be made bigger,

548
00:42:16,860 --> 00:42:18,860
it's a good alternative.

549
00:42:19,880 --> 00:42:23,680
We want to make sure that pages work with just the keyboard,

550
00:42:25,720 --> 00:42:31,320
and you should definitely go home and try this on some of the websites that you use frequently.

551
00:42:31,680 --> 00:42:39,260
Definitely try Facebook, that's a fun one, but try like some stores that you buy from or Amazon

552
00:42:39,260 --> 00:42:40,920
or just just anything.

553
00:42:40,920 --> 00:42:44,340
Just start tabbing around and see what they've handled, see what they haven't.

554
00:42:44,980 --> 00:42:52,720
Look at Apple, some places are doing it very well and some places are doing it very poorly.

555
00:42:52,780 --> 00:42:54,820
And we're working on it.

556
00:42:55,760 --> 00:42:57,260
Try it at your own company.

557
00:42:58,840 --> 00:43:00,340
Tell people about it.

558
00:43:02,360 --> 00:43:05,820
So interfaces should be predictable and easy to use.

559
00:43:06,580 --> 00:43:08,540
Definitely frustrating when they are not.

560
00:43:08,980 --> 00:43:12,040
Even more frustrating to users with disabilities,

561
00:43:13,080 --> 00:43:17,820
and then we just know that designing for different abilities benefits everyone.

562
00:43:18,180 --> 00:43:22,300
It benefits ourselves. After you've gone through like a whole long workshop,

563
00:43:22,300 --> 00:43:26,680
you're probably going to find out that the design was just better after ...

564
00:43:27,560 --> 00:43:32,660
than when you started, because it's just gonna force you to think more simply,

565
00:43:33,280 --> 00:43:34,640
just break things down.

566
00:43:34,640 --> 00:43:42,180
Sometimes, it's just not about adding more code on, it's not about just tacking more accessibility features on,

567
00:43:42,180 --> 00:43:47,580
or aria-labels or just putting more JavaScript in there.

568
00:43:47,580 --> 00:43:50,580
Sometimes it's about just breaking it down and making it simpler.

569
00:43:50,960 --> 00:43:54,600
There's some pages in the application that I work on that are so complicated

570
00:43:54,600 --> 00:43:56,600
that I don't even know how we would fix them.

571
00:43:56,980 --> 00:44:01,480
So, I think we're just gonna probably try to redesign them and come back to it.

572
00:44:02,000 --> 00:44:08,140
So it's not about just fixing everything, 'cause that's way harder, but it's about trying to do it from the beginning.

573
00:44:11,660 --> 00:44:17,420
I have a resources slide, so this is assuming that you go to my slides and click on these.

574
00:44:17,900 --> 00:44:23,400
Just a couple of articles that I found interesting, couple of resources.

575
00:44:23,960 --> 00:44:28,000
Definitely follow @a11ychi on Twitter.

576
00:44:28,340 --> 00:44:34,440
Dennis queues up so much content and there's content several times a day sometimes.

577
00:44:34,440 --> 00:44:42,560
He's always talking about what else is going on, just really cool articles, great resource.

578
00:44:43,540 --> 00:44:47,340
And then, that's my last slide.

579
00:44:47,600 --> 00:44:53,840
Thank you for coming. You can follow me on Twitter, find my slides, sorry, now you can clap.

580
00:44:53,840 --> 00:45:00,580
[Applause]

581
00:45:03,620 --> 00:45:07,760
[Dennis]: So I thank you for ... sure yeah, please ...

582
00:45:08,680 --> 00:45:11,700
[Arelia]: Hi everyone, I'm Arelia, I'm a software engineer with Sprout Social.

583
00:45:11,700 --> 00:45:15,860
I am one of the Chapter Organizers of Girl Develop It, along with Brittany, over here.

584
00:45:16,100 --> 00:45:18,980
Who has not been to Girl Develop It before?

585
00:45:20,160 --> 00:45:22,160
Alright, would love to see you at our events.

586
00:45:22,160 --> 00:45:28,360
So, Girl Develop It is a non-profit organization. We provide affordable and judgement-free opportunities

587
00:45:28,360 --> 00:45:31,500
for women who are interested in working in web and software development.

588
00:45:32,080 --> 00:45:37,320
And although our events and classes are geared towards women, we are open to everyone of all genders.

589
00:45:37,800 --> 00:45:42,260
One of the ways we provide affordable and judgement-free classes is

590
00:45:42,260 --> 00:45:45,840
by bringing in instructors who are working in the field.

591
00:45:46,380 --> 00:45:53,020
We also have ample teacher assistants at each class. We hope you will feel comfortable asking questions,

592
00:45:53,020 --> 00:45:56,080
answer all of your questions so you will feel well supported.

593
00:45:56,540 --> 00:45:59,620
We also have a Code of Conduct that is listed on each event,

594
00:45:59,620 --> 00:46:04,920
and we encourage participants to come to the chapter or organizer onsite

595
00:46:05,260 --> 00:46:07,260
for any violations to the code of conduct.

596
00:46:07,760 --> 00:46:31,240
[Indecipherable]

597
00:46:31,520 --> 00:46:36,660
[Applause]

598
00:46:36,800 --> 00:46:38,440
[Dennis]: Thank you for coming.

599
00:46:38,440 --> 00:46:43,040
If you have any questions for Margie, please come on up. Thanks.

600
00:46:43,040 --> 00:46:46,160
[Applause]

601
00:46:47,340 --> 00:46:54,620
Thanks to our presenter, Margie Chubin. Follow her on Twitter at @MargarineMargie

602
00:46:55,740 --> 00:46:58,760
Also thanks to Girl Develop It Chicago.

603
00:46:59,320 --> 00:47:12,400
Join them at meetup.com/Girl-Develop-It-Chicago-IL

604
00:47:14,540 --> 00:47:17,560
Thanks to our venue sponsor, Redshelf.

605
00:47:17,800 --> 00:47:21,620
Visit them online at redshelf.com.

606
00:47:27,420 --> 00:47:33,800
Live captions provided by ACS, Alternative Communication Services.

607
00:47:34,180 --> 00:47:38,260
Visit them online at acscaptions.com

608
00:47:42,480 --> 00:47:47,140
Live captions sponsored by McDonald's. We're lovin' it!

609
00:47:53,780 --> 00:47:59,980
This has been a production of the Chicago Digital Accessibility & Inclusive Design Meetup.

610
00:48:01,100 --> 00:48:09,020
Visit us online at meetup.com/a11ychi

611
00:48:10,240 --> 00:48:17,900
Follow us on Twitter at twitter.com/a11ychi

612
00:48:18,940 --> 00:48:26,580
Follow us on Facebook at facebook.com/a11ychi

613
00:48:27,680 --> 00:48:33,000
Watch recordings of past meetups on YouTube, on our YouTube channel

614
00:48:33,240 --> 00:48:42,420
youtube.com/c/ChicagoDigitalAccessibilityInclusiveDesign

615
00:48:42,800 --> 00:48:44,920
Make sure you subscribe today!

616
00:48:46,100 --> 00:48:54,340
Copyright 2018 Chicago Digital Accessibility & Inclusive Design Meetup. All rights reserved.

