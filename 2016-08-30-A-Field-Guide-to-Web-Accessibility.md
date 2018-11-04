# A Field Guide to Web Accessibility with Derek Featherstone
## Derek Featherstone - Tuesday, August 30, 2016
[Source recording](https://www.youtube.com/watch?v=gf_BrfCZT7c)

**[Dennis]:** I'm very, very excited to introduce Derek Featherstone. He is a former Ironman tri-athlete, 
and a current Star Wars fanboy. You notice I saw the Ottawa meetup ... He's also been a web professional since 1999 an internationally known speaker, teacher and authority on accessibility and web design. He leads the team at Simply Accessible based in Ottawa Canada. He always puts the user first and strives to make the web a better place by designing experiences that are easy to use for everyone, including people with disabilities. Derek's ideal accessible experience is to combine engaging, rich content, with brilliant design, and technical development excellence. Please give a warm Chicago welcome to Derek Featherstone.

**[Applause]**

**[Derek Featherstone]:** I'm sweating a lot right now, with that introduction. I feel a little bit of pressure, but I think we'll sort it out.

15
00:01:25,100 --> 00:01:28,460
This is a field guide to web accessibility.

16
00:01:28,460 --> 00:01:34,340
And the idea behind this is that this is a collection of things we've learned

17
00:01:35,220 --> 00:01:38,180
by actually working with people with different disabilities.

18
00:01:38,580 --> 00:01:42,160
On real things, and not just things we learned out of books

19
00:01:42,160 --> 00:01:46,300
or reading things that people said, these are the guidelines and this is how it should be.

20
00:01:46,880 --> 00:01:52,580
These are things that we learned doing actual testing with real people.

21
00:01:53,500 --> 00:01:55,260
As opposed to fake people.

22
00:01:55,260 --> 00:01:58,780
It's when you test with fake people ... is well ...

23
00:01:58,960 --> 00:02:01,380
We're talking about sitting there ...

24
00:02:01,380 --> 00:02:03,780
... one of the thing we do at Simply Accessible,

25
00:02:03,780 --> 00:02:09,540
we kind of drew the line in the sand about two and a half years ago, and we said,

26
00:02:10,000 --> 00:02:12,360
we don't really engage in projects

27
00:02:12,360 --> 00:02:17,740
where there's no actual usability testing with people that actually have disabilities.

28
00:02:17,740 --> 00:02:21,900
And we drew that line basically, because to us,

29
00:02:22,460 --> 00:02:26,780
that's kind of the ultimate test of whether or not something works.

30
00:02:27,100 --> 00:02:37,060
For us, the checklist, WCAG guidelines, the things we say we need to do from an accessibility perspective,

31
00:02:37,060 --> 00:02:39,640
that needs to be the starting point.  Not the end point.

32
00:02:39,640 --> 00:02:43,860
The true end point is really, yes, it meets all these technical requirements,

33
00:02:43,860 --> 00:02:48,820
but can it really be used by somebody that has different types of disabilities?

34
00:02:48,820 --> 00:02:52,900
Because if they can't, what was the point of it in the first place, right?

35
00:02:53,500 --> 00:03:03,420
So this is a collection of stories and things that they kind of share those kind of concepts and situations with you.

36
00:03:03,420 --> 00:03:09,280
I'm really interested in this, because this is, you know, lots of people here,

37
00:03:10,360 --> 00:03:15,740
and I'm really interested in knowing how many people are web geeks and not web geeks.

38
00:03:15,740 --> 00:03:21,720
Some people come to these kind of meet ups and they're just interested in what we're talking about.

39
00:03:23,240 --> 00:03:27,380
So hands up and say "I" if you're a developer,
like a web developer?

40
00:03:28,300 --> 00:03:29,660
[Multiple voices]: "I"

41
00:03:29,660 --> 00:03:35,940
[Derek Featherstone]: There wasn't enough "I's" there.  Hands up and say "I" if you're a developer.

42
00:03:36,220 --> 00:03:37,560
[Multiple voices]: "I"

43
00:03:37,560 --> 00:03:42,060
[Derek Featherstone]: That was better. Hands up 
and say "I" if you're a designer.

44
00:03:42,400 --> 00:03:44,000
[Multiple voices]: "I"

45
00:03:44,000 --> 00:03:45,560
[Derek Featherstone]: You guys are way less enthusiastic.

46
00:03:45,560 --> 00:03:47,560
[Laughter]

47
00:03:47,560 --> 00:03:52,160
[Derek Featherstone]: And then anybody like hands up and say "I"

48
00:03:52,160 --> 00:03:55,580
if you're a project manager or product owner type thing?

49
00:03:55,820 --> 00:03:56,900
[Multiple voices]: "I"

50
00:03:56,900 --> 00:03:59,260
[Derek Featherstone]: Good chunk of numbers there.  That's excellent.

51
00:03:59,980 --> 00:04:04,360
And then anybody, hands up and say if you're like a QA type of person?

52
00:04:05,120 --> 00:04:05,800
[Multiple voices]: "I"

53
00:04:06,080 --> 00:04:11,220
[Derek Featherstone]: There's a couple.  That's good.  See you in the corner.  Excellent.

54
00:04:11,220 --> 00:04:13,660
I don't know why you're in the corner but that's okay.

55
00:04:15,360 --> 00:04:21,340
And rest of you, how many people are like a hybrid of what you do, like whole a lot of everything.

56
00:04:21,340 --> 00:04:22,480
So hands up and "I" for that.

57
00:04:22,480 --> 00:04:23,580
[Multiple voices]: "I"

58
00:04:23,580 --> 00:04:25,580
[Derek Featherstone]: Probably most and the rest of you.

59
00:04:25,580 --> 00:04:32,540
Did I not cover anybody?  Is there somebody I did not cover?  I want everybody to feel represented here.

60
00:04:34,080 --> 00:04:34,920
[Attendee]: User experience

61
00:04:34,920 --> 00:04:42,400
[Derek Featherstone]: I consider that part of the design. UX. Anybody hardcore UX-ers?

62
00:04:42,400 --> 00:04:47,820
Hands up say "I".  How come you guys are not saying aye?  Say "I".

63
00:04:47,820 --> 00:04:49,380
[Multiple voices]: "I"

64
00:04:49,380 --> 00:04:55,180
[Derek Featherstone]:  There are 4 people are like, fair enough.  Fair enough.

65
00:04:56,760 --> 00:05:03,340
Did anybody just are here and doesn't snow anything about the web at all.  Oh, networking, that could be fun?

66
00:05:03,340 --> 00:05:04,700
[Laughter]

67
00:05:04,900 --> 00:05:07,100
Okay.  That's fine too.

68
00:05:07,100 --> 00:05:11,560
It's good to kind of hear what kind of representation we have.

69
00:05:11,560 --> 00:05:16,320
I'm really interested in dynamics and where everybody fits.

70
00:05:16,640 --> 00:05:21,320
But hopefully, there's things in here that are useful for everybody.

71
00:05:22,520 --> 00:05:29,520
I want to start off with this.  This is a tap from a hotel in London that I stayed at, London in UK.

72
00:05:29,980 --> 00:05:34,460
Not London, Ontario, which I'm from Ottawa, Canada. 
We have our own London.

73
00:05:35,440 --> 00:05:36,560
It's not quite the same but....

74
00:05:37,300 --> 00:05:45,040
This is a tap from that hotel where I had a hot water tap on the left, and a hot water tap on the right.

75
00:05:45,900 --> 00:05:48,140
And I don't know what to do.

76
00:05:48,140 --> 00:05:51,560
So I decided I'm not showering that day.

77
00:05:51,680 --> 00:05:52,720
[Laughter]

78
00:05:52,720 --> 00:05:53,840
[Derek Featherstone]: It's not going to happen.

79
00:05:54,340 --> 00:05:57,640
This doesn't work for me of these two hot water taps are confusing.

80
00:05:57,640 --> 00:06:03,900
Until I see this sign that tells me that the left tap operates the shower and the right  tap operates the bath.

81
00:06:05,660 --> 00:06:08,200
Now I know if I'm going to burn my head or feet at least.

82
00:06:10,180 --> 00:06:13,500
The problem with this interface is that the tap is exactly where you expect it to be

83
00:06:13,500 --> 00:06:18,340
but the instructions on how to operate it are about six feet away on the side wall.

84
00:06:19,340 --> 00:06:22,380
You can all instinctively look at this and say well this just doesn't make sense.

85
00:06:22,380 --> 00:06:26,200
Those instructions need to kind of be somewhere in the line of sight

86
00:06:26,200 --> 00:06:30,320
when you're looking at the tap, those instructions should be in the vicinity.

87
00:06:30,600 --> 00:06:33,460
From a design perspective, we call that proximity.

88
00:06:33,880 --> 00:06:37,120
We want to take these closely related items and we want to group them together.

89
00:06:37,840 --> 00:06:42,320
So we're going to do a little experiment here.
Very straightforward.

90
00:06:43,960 --> 00:06:47,160
I like you to all take your,
provided you can see the screen,

91
00:06:47,160 --> 00:06:51,060
I'd love for you to take your left hand or right hand,
either one.

92
00:06:51,060 --> 00:06:52,660
If you do both, it's not going to work.

93
00:06:52,660 --> 00:06:57,620
So take your left hand or your right hand, hold it up and make a fist like you're holding on to a straw.

94
00:06:58,620 --> 00:07:02,780
What you're going to do is you're going to look through the straw.

95
00:07:04,040 --> 00:07:06,360
You don't actually have a straw.
Pretend you do.

96
00:07:06,360 --> 00:07:08,520
You're going to look through the straw at the screen.

97
00:07:08,520 --> 00:07:10,140
What you're going to need to do is two things.

98
00:07:10,140 --> 00:07:17,680
One is orient yourself to the interface, and two is go through the process of filling out the form.

99
00:07:17,680 --> 00:07:21,460
So I just told you what's on the interface. 
It's a form, that you need to fill out.

100
00:07:21,880 --> 00:07:22,760
Does that make sense?

101
00:07:22,760 --> 00:07:24,420
You're holding the straw, we're going to do a test run.

102
00:07:24,820 --> 00:07:28,500
Hold up your straw.  You need to actually like put it right up against your eye.

103
00:07:29,340 --> 00:07:31,340
And then you need to close the other eye.

104
00:07:32,580 --> 00:07:34,580
Okay.  Or cover it with your hand.

105
00:07:34,980 --> 00:07:37,520
So what we're doing here is limiting
how much you can see.

106
00:07:37,520 --> 00:07:40,800
Now, some of you are holding on
to a garden hose right now.

107
00:07:41,160 --> 00:07:45,340
You need to make it like a straw.  
Like a tiny cocktail straw.

108
00:07:45,720 --> 00:07:47,040
So that's what you're going to do.

109
00:07:48,260 --> 00:07:54,440
I'm about to reveal the interface.  Are you ready or this?  Straw's up and the way you go!

110
00:07:56,800 --> 00:08:01,740
While you do that, I'm going to take a photo.

111
00:08:01,740 --> 00:08:03,740
[Laughter]   [Taking photo]

112
00:08:22,040 --> 00:08:24,160
[Derek Featherstone: Some of you are still 
filling in the form.

113
00:08:24,160 --> 00:08:28,920
Some of you are done. Some of you are like, I'm out. Can't do this.

114
00:08:31,320 --> 00:08:36,160
So what we have on this form, 
we have four clusters of information

115
00:08:36,160 --> 00:08:41,840
and the clusters are two questions on the left-hand side and two sets of answers on the right-hand side

116
00:08:41,840 --> 00:08:48,000
and then two more questions on the left-hand side and two more sets of answers on the far right-hand side.

117
00:08:48,000 --> 00:08:50,840
and then we have our Quit button, our Previous button and our Next button.

118
00:08:51,120 --> 00:08:53,380
This is a very straightforward form, and, yet,

119
00:08:55,360 --> 00:08:59,540
this was coded perfectly and it worked very well for somebody that was using a screen reader.

120
00:09:00,400 --> 00:09:07,400
And it was ... the developers that built it said to me, like,
this is coded perfectly. This is accessible.

121
00:09:08,120 --> 00:09:12,500
And then we went and actually tested with people that had low vision, that weren't using screen readers.

122
00:09:12,500 --> 00:09:14,500
It failed miserably.

123
00:09:14,960 --> 00:09:18,700
And those who were looking through the straw 
might actually understand a little bit about why.

124
00:09:18,700 --> 00:09:21,580
What motion did you have to go through 
to fill in that form?

125
00:09:24,160 --> 00:09:27,060
Left right, left right, left right, left right.

126
00:09:27,060 --> 00:09:29,400
Because of the way that this form is designed,

127
00:09:29,400 --> 00:09:35,620
where we have these questions on the left, and the answers way over on the right,

128
00:09:35,620 --> 00:09:38,820
what ends up happening is 
we're creating a situation like this.

129
00:09:39,220 --> 00:09:42,920
When somebody has low vision,
they have a limited view of the screen.

130
00:09:43,620 --> 00:09:47,100
So this is roughly 250% magnification.

131
00:09:47,700 --> 00:09:54,200
Somebody that needs 200% magnification is going to see roughly one quarter of the screen at any given time.

132
00:09:54,720 --> 00:10:01,400
If they need 300% magnification, 
they will see 1/9th screen at any given time.

133
00:10:01,400 --> 00:10:05,380
400% would be 1/16th of the screen that they will be looking at.

134
00:10:05,700 --> 00:10:08,060
And so it's very easy to lose that context.

135
00:10:08,420 --> 00:10:13,700
If you take a look here when we're magnified and we're zoomed in and you're looking at the questions,

136
00:10:14,180 --> 00:10:15,700
you really just see the questions.

137
00:10:16,080 --> 00:10:24,220
When you scroll over to the far right to get to those answers, those questions you saw are now kind of like,

138
00:10:24,460 --> 00:10:25,720
out of sight, out of mind.

139
00:10:26,740 --> 00:10:31,020
Same thing as the tap and the instructions for the tap being six feet away from each other.

140
00:10:31,860 --> 00:10:33,640
It's exactly the same thing.

141
00:10:34,000 --> 00:10:40,460
So what we need to do in interface design is take those closely related items and group them together.

142
00:10:40,880 --> 00:10:45,120
There's really good reasons. 
We create visual relationships when we do that.

143
00:10:45,460 --> 00:10:53,160
We can create programmatic relationships all day long in code for screen reader users

144
00:10:53,160 --> 00:10:55,280
and Dragon NaturallySpeaking users.

145
00:10:55,500 --> 00:11:00,040
But the visual relationships are quite important for people with low vision.

146
00:11:00,040 --> 00:11:03,480
The proximity of things
become even more important to them.

147
00:11:03,480 --> 00:11:05,480
Almost more important than the programmatic side.

148
00:11:06,560 --> 00:11:10,320
So we're at this point here, where we've started on the left and we see the questions

149
00:11:10,320 --> 00:11:13,200
and gone over to the right to answer that first question.

150
00:11:13,540 --> 00:11:16,660
We go back over to the left to hit the next question.

151
00:11:17,700 --> 00:11:18,960
Right for the answer.

152
00:11:19,580 --> 00:11:20,740
Left for the question.

153
00:11:21,260 --> 00:11:22,380
Right for the answer.

154
00:11:22,700 --> 00:11:23,740
Left for the question.

155
00:11:24,260 --> 00:11:25,300
Right for the answer.

156
00:11:25,960 --> 00:11:27,200
What's your next move?

157
00:11:28,220 --> 00:11:32,380
Left for the question.  And it's not a question, but it's quit.

158
00:11:33,120 --> 00:11:37,880
It's a call to action that is kind of the 
least desirable call to action.

159
00:11:38,360 --> 00:11:43,160
And yet, we led them right there by that pattern of use we created.

160
00:11:43,800 --> 00:11:49,900
We also have things, and this is not unique to people with low vision,

161
00:11:49,900 --> 00:11:52,780
but there's a certain muscle memory that you've created.

162
00:11:53,220 --> 00:11:56,180
You probably felt it and you knew exactly 
how far to scroll over

163
00:11:56,180 --> 00:11:58,180
every time when you were looking through the straw.

164
00:11:59,120 --> 00:12:04,480
The place where those answers were, when we get our second least favorite call to action,

165
00:12:04,480 --> 00:12:06,480
the previous action.

166
00:12:06,780 --> 00:12:08,780
There's whole a lot of thing wrapped up into this.

167
00:12:08,780 --> 00:12:13,880
We've created a pattern of use.
We have created the wrong chunks of information.

168
00:12:14,260 --> 00:12:18,500
And if you take a look at these three buttons, the quit, the previous and the next,

169
00:12:19,100 --> 00:12:22,960
from a design perspective, we say they have essentially the same visual weight.

170
00:12:23,900 --> 00:12:27,640
They're all the same shape. They're all roughly the same size and same color.

171
00:12:28,000 --> 00:12:30,000
All the same other characteristics.

172
00:12:30,000 --> 00:12:33,820
The only thing that's different about them is the text and the characters that are on them.

173
00:12:35,200 --> 00:12:38,700
So when we take a look at all 3 of these,

174
00:12:39,380 --> 00:12:41,700
these different factors, this design actually ends up kind of failing miserably.

175
00:12:42,420 --> 00:12:46,640
Failing miserably for someone with low vision.

176
00:12:47,940 --> 00:12:50,400
We have these kind of the wrong chunks, right?

177
00:12:50,400 --> 00:12:53,400
Question, question, answer, answer.
Question, question, answer, answer.

178
00:12:54,280 --> 00:12:56,520
That's like all kinds of wrong.

179
00:12:58,000 --> 00:13:02,840
What we want to do is we want to take this and fix all 3 of those things at once

180
00:13:02,840 --> 00:13:07,340
and make this something that works a little bit better for someone with low vision.

181
00:13:07,660 --> 00:13:11,720
And we're not really just saying every form should be designed like this.

182
00:13:12,500 --> 00:13:14,420
But ...

183
00:13:14,420 --> 00:13:17,500
... well, actually we are. 
Every form should be designed like this.

184
00:13:17,600 --> 00:13:22,980
We want to create things that work well, that have the right groupings,

185
00:13:22,980 --> 00:13:27,780
that have a really straightforward flow if it can,
and have obvious calls to action.

186
00:13:27,780 --> 00:13:31,220
So we want to take this interface, and maybe turn it,

187
00:13:31,220 --> 00:13:32,940
and this is not the only design,

188
00:13:32,940 --> 00:13:35,220
but this is the one that works reasonably well.

189
00:13:35,740 --> 00:13:39,220
The same interface and we design it
so it's in a vertical stack.

190
00:13:39,780 --> 00:13:41,960
So instead of having multiple columns,

191
00:13:42,700 --> 00:13:48,980
we actually make things flow in a vertical stack such that we create the right groupings,

192
00:13:48,980 --> 00:13:51,220
and we go directly down to the call to action.

193
00:13:51,220 --> 00:13:56,160
So now, if you bring your straws up and fill out this form, compare the  experience.

194
00:13:56,160 --> 00:14:00,760
So go ahead. Straws up. And fill out this form.

195
00:14:05,440 --> 00:14:08,800
You should immediately recognize the difference.

196
00:14:09,400 --> 00:14:13,100
You probably will never completely eliminate
left to right scrolling.

197
00:14:13,100 --> 00:14:15,100
That's not necessarily the goal.

198
00:14:15,100 --> 00:14:18,720
But the idea is, like,
if this second question was really long,

199
00:14:19,200 --> 00:14:22,600
you might have to scroll some. 
You won't necessarily eliminate that.

200
00:14:23,080 --> 00:14:28,700
We were looking at magnification that was at like 250%.

201
00:14:28,700 --> 00:14:31,120
Somebody might be looking at it at 500%.

202
00:14:31,820 --> 00:14:34,140
But what we do by creating this vertical stack is

203
00:14:34,140 --> 00:14:41,060
we minimize the effort that's required to have, to fill out that form by somebody that has low vision.

204
00:14:41,740 --> 00:14:43,180
We've got the right groupings.

205
00:14:43,180 --> 00:14:45,180
Instead of question, question, answer, answer,

206
00:14:46,260 --> 00:14:50,140
we've got question and answer, question and answer, question and answer, question and answer.

207
00:14:51,140 --> 00:14:54,820
You also see what we've done with the calls to action. Right?

208
00:14:54,820 --> 00:14:58,000
they're now distinct. 
They're not all exactly the same shape.

209
00:14:58,520 --> 00:15:02,820
For someone with low vision, those shapes might look like the same blob, right?

210
00:15:02,820 --> 00:15:05,680
Whereas, here, we made it like this is a really definite,

211
00:15:05,680 --> 00:15:08,380
this is our primary call to action
that we want people to take.

212
00:15:08,740 --> 00:15:12,840
Then the other ones, they look different and they have different characteristics in the interface.

213
00:15:14,040 --> 00:15:16,040
So all of that should make sense to you.

214
00:15:16,040 --> 00:15:20,280
When we look at this even magnified and we Zoom into that roughly 250%,

215
00:15:20,960 --> 00:15:22,040
you can see what happens.

216
00:15:22,040 --> 00:15:26,300
That pattern of use is no longer left right, left right.
It's straight down.

217
00:15:26,960 --> 00:15:33,860
The thing I love about this is that that design also works well for a mobile device.

218
00:15:35,120 --> 00:15:39,660
Multicolumn layouts on a mobile device for somebody that can see the screen are a total pain.

219
00:15:40,280 --> 00:15:44,900
When you have your form label to the left 
and you have the field on the right-hand side,

220
00:15:45,380 --> 00:15:48,460
I don't know about you,
but I hate this when I tap into a form field,

221
00:15:48,900 --> 00:15:51,080
and suddenly, the label is gone, right?

222
00:15:51,080 --> 00:15:53,740
It's off the screen. I can't see it.

223
00:15:54,280 --> 00:16:00,460
When I move to the next field, if I hit the next,
either I tap the field directly or if I use,

224
00:16:00,460 --> 00:16:04,400
there's usually a next field thing to go to the next field.

225
00:16:04,860 --> 00:16:07,740
Those don't zoom back out to let you see
what the field is.

226
00:16:08,880 --> 00:16:14,520
This single vertical stack is actually really good for people that are on a mobile device as well.

227
00:16:14,980 --> 00:16:19,880
So I love this kind of idea of creating these little things that we can do.

228
00:16:19,880 --> 00:16:21,880
And I want you to use that straw test.

229
00:16:22,460 --> 00:16:30,240
We use that straw test at Simply Accessible
to test wireframes, to test mockups, to test live designs.

230
00:16:30,240 --> 00:16:36,160
And that's all to try to make things better before we test with people with real low vision.

231
00:16:36,960 --> 00:16:41,600
All we're doing is simulating some of the effects of having low vision by limiting that field of view.

232
00:16:43,080 --> 00:16:44,200
Make sense?

233
00:16:44,200 --> 00:16:50,500
Like use it. Every design you ever create, try it
and see the impact that it has.

234
00:16:50,880 --> 00:16:54,120
I'm not saying you're going to make radical changes
to your design,

235
00:16:54,120 --> 00:16:56,520
but you will find things that seem out of place.

236
00:16:57,380 --> 00:16:59,420
Go through flows.  Go through tasks.

237
00:16:59,420 --> 00:17:04,920
Like ... go and purchase Cubs Pirates tickets
for tomorrow night.

238
00:17:06,040 --> 00:17:07,300
That's a great example.

239
00:17:07,300 --> 00:17:12,000
Go through that flow and what kind of things do you find that are out of place?

240
00:17:13,000 --> 00:17:22,100
When we think of accessibility, we like to categorize and we say there's more or 5 major types of disabilities.

241
00:17:22,100 --> 00:17:28,260
We're talking about people with visual impairment, hearing impairment, mobility, cognitive impairments,

242
00:17:28,260 --> 00:17:33,440
you know, and even speech related impairments.

243
00:17:34,160 --> 00:17:39,060
We like to put categories and put people inboxes and it's really not that simple.

244
00:17:39,540 --> 00:17:43,900
And I really mean this.
We like to put things in  boxes all the time.

245
00:17:43,900 --> 00:17:50,180
As an example, these are my two sons.  And I have put them in  boxes many times.

246
00:17:50,180 --> 00:17:51,920
Because it's lots of fun.

247
00:17:51,920 --> 00:17:57,040
This is our first son, he's 18 months here, 18 months old.  Now he's 12.

248
00:17:57,040 --> 00:18:00,700
I tried to get him to come tonight with me. 
He's here in Chicago with me.

249
00:18:00,700 --> 00:18:05,860
And he's like, you're going to show that photo of me in a box again, aren't you?

250
00:18:05,860 --> 00:18:07,860
I said yes. He said forget it, I'm not coming.

251
00:18:07,860 --> 00:18:12,160
And this is my other son who is now 3.

252
00:18:12,900 --> 00:18:15,700
This first son loves being in this box.

253
00:18:16,380 --> 00:18:19,320
I'm going to put my other son in a box too 
and see how happy he is.

254
00:18:19,320 --> 00:18:21,320
He wasn't nearly as happy.

255
00:18:21,320 --> 00:18:26,040
But we like to put things in the boxes and we do that in the accessibility world all the time.

256
00:18:27,180 --> 00:18:30,300
The reality is accessibility can be very, very messy.

257
00:18:32,740 --> 00:18:38,880
The real world, like real world kind of this is why
this is in this field guide.

258
00:18:38,880 --> 00:18:44,380
We all want to believe that everybody stays
up-to-date with their technology,

259
00:18:44,380 --> 00:18:50,180
including people with disabilities and these are quotes from actual studies that we did.

260
00:18:50,180 --> 00:18:51,940
"I should probably upgrade Jaws,

261
00:18:51,940 --> 00:18:55,900
but I going to have to manually move all my settings and macros and I just don't want to do it."

262
00:18:57,940 --> 00:19:02,120
Like that's reality. 
This is a person that instead of being on Jaws 17,

263
00:19:02,120 --> 00:19:05,540
which is the latest and greatest and in the fall we'll probably see Jaws 18.

264
00:19:06,200 --> 00:19:11,580
This was a person on Jaws 13
which was effectively from 5 years ago.

265
00:19:13,140 --> 00:19:14,820
And we keep saying all these things.

266
00:19:14,820 --> 00:19:19,980
You know, I don't know if you guys knows this, but we're nerds and the rest of the world is not.

267
00:19:23,120 --> 00:19:25,560
Not that they never do, but they're slower to upgrade.

268
00:19:25,560 --> 00:19:29,760
They might choose not to. They're not as technically inclined as we are.

269
00:19:30,180 --> 00:19:32,100
[Attendee]: And Jaws makes you pay for it.

270
00:19:32,100 --> 00:19:36,020
[Derek Featherstone]: And Freedom Scientific, they make you pay.

271
00:19:37,200 --> 00:19:41,100
And this is another one.  What is this?

272
00:19:41,100 --> 00:19:48,120
"I've been using Dragon 10 for a while and it works

273
00:19:48,120 --> 00:19:50,120
so why do I have to spend the money 
when I don't have to?

274
00:19:51,680 --> 00:19:58,720
We're about to hit Dragon 15, it's coming out in September. Dragon 10 is from not quite five years ago.

275
00:19:58,720 --> 00:19:59,940
It works.

276
00:20:01,320 --> 00:20:02,560
Why would I update?

277
00:20:04,300 --> 00:20:08,320
That starts to get messy, especially when people are saying things, like we try to say it.

278
00:20:08,320 --> 00:20:10,320
I want to be just on this browser.

279
00:20:10,320 --> 00:20:14,200
We support these browsers and what assistive technology do we support?

280
00:20:14,200 --> 00:20:16,200
If we even have that conversation.

281
00:20:16,580 --> 00:20:23,040
Everybody wants to say, we even say when we're doing a lot of testing, current version minus 2.

282
00:20:24,140 --> 00:20:27,920
Well, current version minus 2
wouldn't have caught either of these different scenarios

283
00:20:27,920 --> 00:20:33,420
and these were people that showed up
in actual testing for us.

284
00:20:33,420 --> 00:20:37,980
If so it's kind of like that reality check that not everybody is like us.

285
00:20:37,980 --> 00:20:41,820
Even though we want to believe that everybody is.
It just doesn't happen.

286
00:20:43,440 --> 00:20:46,960
How many people never heard a screen reader
at full pace before?

287
00:20:46,960 --> 00:20:48,180
Hands up and say "I."

288
00:20:49,560 --> 00:20:51,560
You might not know what a screen reader is.

289
00:20:51,560 --> 00:20:59,220
But this is basically somebody that is blind might use a screen reader to read the screen for them.

290
00:20:59,880 --> 00:21:02,880
And from a captioning perspective,
this isn't going to work at all.

291
00:21:02,880 --> 00:21:05,660
Because this is just a very fast video.

292
00:21:07,460 --> 00:21:12,380
But this is actual footage from the user test that we did.

293
00:21:12,860 --> 00:21:19,200
And this person, this was how fast they had their screen reader going, pretty much all the time.

294
00:21:19,200 --> 00:21:20,500
So here we go.

295
00:21:22,800 --> 00:21:42,340
[Video Clip] [Indiscernible speech]
[Screen reader reading very fast]

296
00:21:43,620 --> 00:21:47,740
This is somebody that's going through
the remote desktop software that they were using

297
00:21:47,740 --> 00:21:50,880
so they're looking for specific pieces of information.

298
00:21:51,520 --> 00:21:54,600
They're not sitting there listening to a webpage that fast

299
00:21:55,200 --> 00:21:58,280
to get at that content.
They might slow that down to go through a form.

300
00:21:58,720 --> 00:22:01,820
But they had a very specific task they were trying to complete there.

301
00:22:01,820 --> 00:22:07,100
Which was let's log-in and allow people to access remote desktop.

302
00:22:08,120 --> 00:22:12,660
For that activity was completely fine.  Right?

303
00:22:12,660 --> 00:22:13,720
For them.

304
00:22:13,720 --> 00:22:15,720
Not everybody listens to it that fast.

305
00:22:16,040 --> 00:22:18,040
But that's an actual recording.

306
00:22:18,280 --> 00:22:22,000
We didn't go in there and speed this up with the magic of computer or anything.

307
00:22:22,000 --> 00:22:24,000
That was actually how fast it was.

308
00:22:25,880 --> 00:22:31,440
How easy do you think it might be to miss something when things are going that fast?

309
00:22:32,200 --> 00:22:34,200
An error message comes up.

310
00:22:34,800 --> 00:22:37,220
This is the thing that's bugging me a lot lately.

311
00:22:37,220 --> 00:22:41,460
My webpages are giving me alert notifications when I'm typing.

312
00:22:42,100 --> 00:22:46,060
And that notification suddenly takes the focus 
and I dismiss it

313
00:22:46,060 --> 00:22:48,300
because I was typing something
and I don't know what it said.

314
00:22:48,780 --> 00:22:53,480
Really easy to miss. Maybe that's just me, 
but that happens all the time.

315
00:22:53,480 --> 00:22:56,140
We dismiss notifications if we're in the middle of typing something,

316
00:22:56,600 --> 00:22:59,700
and we don't know what it was,
but we feel like we've done our job.

317
00:22:59,700 --> 00:23:01,280
We've given them a notice.

318
00:23:01,280 --> 00:23:10,580
And they just, they actually, they didn't actually “notice the notice”… that's just a bad joke.

319
00:23:10,580 --> 00:23:12,580
[Laughter]

320
00:23:14,020 --> 00:23:17,080
[Derek Featherstone]: It's really easy to miss something when the screen reader is going that fast.

321
00:23:17,460 --> 00:23:21,640
And we tend to say, well, that's their problem.

322
00:23:21,640 --> 00:23:27,440
But actually, we have to kind of get passed that and say, well, what can we do about that?

323
00:23:27,860 --> 00:23:30,940
There are things we can actually, that we can actually change.

324
00:23:32,880 --> 00:23:37,140
When we talk about the real world of accessibility being messy, I love this example as well.

325
00:23:38,160 --> 00:23:41,000
Most people have talked about, and really, you can't answer this.

326
00:23:41,660 --> 00:23:43,360
You're not allowed to answer this.

327
00:23:43,660 --> 00:23:46,020
When we say something about like the autism spectrum.

328
00:23:46,840 --> 00:23:51,540
People that are talking about people that are autistic or not autistic.

329
00:23:51,540 --> 00:23:57,320
We talk about the autistic spectrum.  Just draw for me, you know,

330
00:23:57,320 --> 00:24:03,160
in the sky here, draw for me what a spectrum looks like when you think about the autism spectrum.

331
00:24:06,900 --> 00:24:11,540
So I'm seeing some people doing this putting their arms out wide.

332
00:24:11,540 --> 00:24:14,500
Some people are drawing a line.  I don't know what this was.

333
00:24:14,500 --> 00:24:17,580
Somebody putting their hand up and down.  I don't know what that is.

334
00:24:17,580 --> 00:24:24,780
But we'll go with it.  That's totally fine.  I saw one person do like a O and circley thing.

335
00:24:28,540 --> 00:24:30,920
It was like this.  It was almost like jazz hands happening.

336
00:24:30,920 --> 00:24:36,840
Don't where you're getting to, but this brilliant cartoon,

337
00:24:36,840 --> 00:24:47,260
that person that is autistic created to express how she feels about things and there was this cartoon,

338
00:24:47,260 --> 00:24:55,100
there's links to this out there. And I will tweet this out for the full version of the cartoon.

339
00:24:55,360 --> 00:25:00,460
She says here when people think of this word, they think of the autism spectrum like this.

340
00:25:00,460 --> 00:25:05,740
And it's that linear spectrum, where on the left hand side, we've got not autistic

341
00:25:05,740 --> 00:25:07,740
and on the right-hand side, you've got very autistic.

342
00:25:08,680 --> 00:25:14,820
And we have this mental model that some people have autism fits somewhere on there.

343
00:25:15,220 --> 00:25:18,960
And then, you know, because we think we can judge that kind of thing,

344
00:25:18,960 --> 00:25:22,780
we can see, or I can look at somebody 
and say they have autism.

345
00:25:23,940 --> 00:25:25,700
And it's totally not like that.

346
00:25:25,940 --> 00:25:31,260
But because of this idea that somebody is either not autistic or very autistic,

347
00:25:31,260 --> 00:25:33,960
or somewhere in between,
and that constitutes a spectrum.

348
00:25:35,160 --> 00:25:41,900
She was finding that people were constantly pushing her into situations that she was completely uncomfortable

349
00:25:41,900 --> 00:25:45,280
with simply because she didn't look autistic.

350
00:25:46,500 --> 00:25:49,580
And, so, she created this to kind of talk about that.

351
00:25:49,580 --> 00:25:59,240
And I love this, because her depiction in this next slide of what the spectrum actually means to her is brilliant.

352
00:25:59,500 --> 00:26:02,740
The truth is though, someone who is neural diverse in some areas of the brain

353
00:26:02,740 --> 00:26:07,340
will also be no different to the average person in other areas of the brain.

354
00:26:07,600 --> 00:26:13,600
So she took this and literally made like a circular spectrum that has the color of the rainbows,

355
00:26:13,600 --> 00:26:20,100
but it's kind of like different levels of saturation and different color values.

356
00:26:20,460 --> 00:26:23,520
And she says, so the autistic spectrum looks
more like this and

357
00:26:23,520 --> 00:26:29,720
she has 5 aspects of kind of neural diversity or brain function that she mapped on to this.

358
00:26:29,720 --> 00:26:32,020
There's many more than that, but she took these 5.

359
00:26:32,340 --> 00:26:36,700
Language skills, motor skills, perception,  
executive function and sensory filter.

360
00:26:37,980 --> 00:26:44,460
So, executive function is that part of the brain that regulates, like, you shouldn't say that right now.

361
00:26:44,460 --> 00:26:48,700
Or you should say this right now.
Or reading social situations.

362
00:26:48,700 --> 00:26:52,600
Your executive function is that part of your brain that regulates all of that.

363
00:26:53,620 --> 00:26:56,020
So she figures this is where she is.

364
00:26:56,280 --> 00:26:59,900
Her language skills are very advanced.  
Much better than average.

365
00:27:00,160 --> 00:27:03,780
But her sensory filter is much, much lower than average.

366
00:27:04,100 --> 00:27:06,340
Her executive function is roughly average.

367
00:27:06,340 --> 00:27:09,280
Her perception skills, much better than average.

368
00:27:09,280 --> 00:27:12,060
And her motor skills are much less than average.

369
00:27:12,660 --> 00:27:17,580
So for her, she's created this kind of profile of these 5 particular characteristics.

370
00:27:17,580 --> 00:27:23,700
They're not "the" five characteristics that we would have for people with autism.

371
00:27:23,700 --> 00:27:27,740
They're just five that seemed like really convenient ones that people can easily understand.

372
00:27:28,880 --> 00:27:33,460
And I love this model.  Because it's really not about you're either this or that.

373
00:27:34,080 --> 00:27:37,060
It's complicated.  It's messy.  Right?

374
00:27:37,060 --> 00:27:39,060
And I think about the same thing for vision.

375
00:27:39,060 --> 00:27:43,020
I have a friend with Stargardt syndrome.

376
00:27:43,020 --> 00:27:46,200
Which means he only has peripheral vision.

377
00:27:46,980 --> 00:27:50,740
He has no central vision,
but he has some peripheral vision.

378
00:27:51,120 --> 00:27:55,460
So if you think of applying this spectrum model
to vision,

379
00:27:55,980 --> 00:28:02,380
you might think of peripheral vision as one of the characteristics,  central vision as another characteristics.

380
00:28:02,380 --> 00:28:07,740
The ability to perceive color.
The ability to have stereo vision.

381
00:28:07,740 --> 00:28:11,620
Some people can only see with one eye, 
therefore, they're ... wow.

382
00:28:13,500 --> 00:28:18,940
You're blurry right now.  Wait a second.  I'll switch.

383
00:28:20,820 --> 00:28:27,780
Stereo vision, you need to be able to see with both eyes and see 3 dimensions and have that depth of perception

384
00:28:27,780 --> 00:28:31,900
and depth of perception might be another factor
that we take into account here.

385
00:28:31,900 --> 00:28:37,660
There's lots of different things that might make up somebody's visual profile.

386
00:28:38,300 --> 00:28:47,560
We can apply that to many different types of,
different types of disabilities or characteristics.

387
00:28:48,720 --> 00:28:50,960
So things do continue to get messy.

388
00:28:52,920 --> 00:28:59,460
This is a little bit of a concept of the viewport.

389
00:28:59,460 --> 00:29:02,160
And I'll explain more what that means later.

390
00:29:03,560 --> 00:29:07,200
It goes along with us putting people in boxes.

391
00:29:07,640 --> 00:29:12,800
The view port is part of your browser
that shows the webpage.

392
00:29:13,200 --> 00:29:15,120
I'm going to share this with you.

393
00:29:15,120 --> 00:29:22,320
This is my father-in-law's desktop computer.
A screenshot of his computer.

394
00:29:22,320 --> 00:29:24,500
And he passed away last summer.

395
00:29:25,440 --> 00:29:33,060
But when we were there, probably about … I don't know, 6 months to 9 months before he passed away,

396
00:29:33,060 --> 00:29:37,740
we were looking at this computer
and I see things on here that scare me.

397
00:29:37,740 --> 00:29:40,300
And I don't really understand it.

398
00:29:40,300 --> 00:29:44,140
But I see here that he's got a new brief case icon.

399
00:29:44,140 --> 00:29:47,060
And then he's got a copy of a new brief case icon.

400
00:29:47,060 --> 00:29:50,140
He's got a copy 2 of the brief case icon.

401
00:29:50,140 --> 00:29:53,400
And he's also got a shortcut to a new brief case icon.

402
00:29:53,780 --> 00:29:55,520
He's got all of these things on his desktop.

403
00:29:55,520 --> 00:29:57,760
And I'm like .. Dude, what's going on here?

404
00:29:57,760 --> 00:29:59,360
Like I don't understand.

405
00:30:01,660 --> 00:30:03,760
And I'm looking at other things
and other things scare me.

406
00:30:03,760 --> 00:30:08,480
He's got two copies of Apache on his desktop. Don't understand why.

407
00:30:08,480 --> 00:30:16,060
Shortcut to games. Shortcuts to Seahaven. 
And Seahaven 2. And Seahaven 3.

408
00:30:16,060 --> 00:30:19,940
And I'm looking at this and trying to understand it. 
And I don't get it.

409
00:30:20,840 --> 00:30:22,840
Now, we'll talk about that in a moment.

410
00:30:24,100 --> 00:30:27,520
Can you tell what resolution that screen is
just by looking at it?

411
00:30:27,520 --> 00:30:30,060
[Attendee guesses shouted out]

412
00:30:30,460 --> 00:30:36,820
[Derek Featherstone]: 800 by 600. Some people said 640 by 480. What size?

413
00:30:37,960 --> 00:30:39,960
Some of you don't know what 640 by 480 is.

414
00:30:39,960 --> 00:30:41,600
[Laughter]

415
00:30:41,600 --> 00:30:43,840
[Derek Featherstone]: That's totally good if you are actually in that place.

416
00:30:46,460 --> 00:30:48,460
What size monitor do you think it's on?

417
00:30:48,460 --> 00:30:50,460
[Attendee guesses]

418
00:30:50,460 --> 00:30:56,760
[Derek Featherstone]: Who said that? 
You've been to my presentation before?

419
00:30:57,200 --> 00:30:59,200
27 inch monitor.

420
00:30:59,200 --> 00:31:03,160
At 832 by 623.

421
00:31:03,160 --> 00:31:07,740
I don't know why it's 832 by 623, but ...

422
00:31:08,740 --> 00:31:15,220
all those icons, all of those icons, the multiple copies,

423
00:31:15,220 --> 00:31:18,200
I start to realize
as I watch him working on the computer

424
00:31:18,980 --> 00:31:25,340
not only does he have low vision, and has this setting where he's at 832 by 624 in a 27 inch monitor

425
00:31:25,960 --> 00:31:29,080
but he also has some dexterity issues 
because he's pushing 90.

426
00:31:30,440 --> 00:31:33,380
And when he tries to double-click, when he's holding down the mouse,

427
00:31:33,860 --> 00:31:42,520
he tries to double-click with his left finger and his middle finger ends up tapping on the right-click as well.

428
00:31:42,860 --> 00:31:49,240
So he's double-clicking and dragging it at the same time accidentally moving by 10 pixels.

429
00:31:49,540 --> 00:31:53,680
And he's dragging right-clicking and letting go
and it's creating shortcuts and doing all this stuff.

430
00:31:54,300 --> 00:32:00,000
So he's not just somebody that has low vision.

431
00:32:00,000 --> 00:32:03,380
He's not just somebody with mobility
and dexterity issues.

432
00:32:03,380 --> 00:32:05,760
He's got both of those things going on at the same time.

433
00:32:06,220 --> 00:32:08,660
He was also ... and you can imagine how this would be.

434
00:32:09,900 --> 00:32:11,900
He's also deaf in his left ear.

435
00:32:12,260 --> 00:32:13,480
He didn't drive anymore.

436
00:32:13,480 --> 00:32:19,360
His wife actually drove so she was in the driver seat
and she's deaf in the right ear.

437
00:32:19,360 --> 00:32:23,300
And he was in the passenger seat
and he's deaf in the left ear.

438
00:32:24,080 --> 00:32:28,420
And you can imagine what driving with them might have been like.

439
00:32:29,080 --> 00:32:33,400
They couldn't hear each other.
So they were like, you know, yelling.

440
00:32:33,400 --> 00:32:37,580
And it just escalated and... wow!

441
00:32:37,580 --> 00:32:44,700
So, we think about putting people in boxes and we think about this person is blind or this person has low vision.

442
00:32:45,520 --> 00:32:48,280
And it's so not that simple.

443
00:32:48,880 --> 00:32:54,280
People are going to have multiple things that impacts how they work on a computer in multiple ways.

444
00:32:55,040 --> 00:32:58,280
We cannot ... I'm going to get to the view port here.

445
00:32:58,280 --> 00:33:03,600
We cannot make assumptions about the  device that somebody is on based on their view port.

446
00:33:04,220 --> 00:33:06,580
Now, he was at 832 by 624.

447
00:33:08,240 --> 00:33:14,760
If we were creating a responsive design for him, what size or what version of the site would he probably get?

448
00:33:16,440 --> 00:33:23,880
He would probably get the tablet type rendering.
And he's not on the tablet.

449
00:33:24,940 --> 00:33:28,020
But we make assumptions all the time about the size and the view port somebody has

450
00:33:28,020 --> 00:33:31,780
and what device they're on.
And it's so not that simple, right?

451
00:33:31,780 --> 00:33:38,160
View port is not a proxy for anything.
All it tells you is what's the visible size of this Window?

452
00:33:38,780 --> 00:33:43,540
And things are changing, you know,
changing all the time.

453
00:33:44,840 --> 00:33:46,200
IOS 9.

454
00:33:47,240 --> 00:33:54,920
We now have on iPads and iPad Pros.
We have split screen capability, right?

455
00:33:56,380 --> 00:34:02,860
Something goes into a half screen, you've got a browser on there, maybe that's now getting a mobile view.

456
00:34:02,860 --> 00:34:07,560
You can even split it two-thirds, 1/3, three quarter on an iPad Pro.

457
00:34:08,120 --> 00:34:15,680
So it's a tablet, but maybe it's getting a mobile view port in that doc kind of stripped down on the side.

458
00:34:16,240 --> 00:34:19,100
Viewpoint isn't a proxy for anything.
We can't make assumptions about it.

459
00:34:19,520 --> 00:34:22,540
And that's becoming more and more prevalent to us.

460
00:34:22,540 --> 00:34:29,580
We were doing a series of usability tests
right before Christmas.

461
00:34:30,220 --> 00:34:36,000
And we found 3 out of 8 screen reader users.

462
00:34:36,000 --> 00:34:37,420
And I want to think about this.

463
00:34:37,420 --> 00:34:38,820
3 out of 8.

464
00:34:39,460 --> 00:34:41,020
That's close to 50%.

465
00:34:42,180 --> 00:34:46,420
3 out of 8 screen reader users were on computers
where they didn't have a monitor attached.

466
00:34:47,760 --> 00:34:51,120
We call it "headless browsing."

467
00:34:52,220 --> 00:34:57,980
They are working in a scenario where they don't have anybody that they live with.

468
00:34:57,980 --> 00:34:59,680
They don't need a monitor, right?

469
00:34:59,680 --> 00:35:04,040
They're using JAWS or VoiceOver or whatever it is.
And they don't need a monitor.

470
00:35:05,780 --> 00:35:11,660
So they're browsing in it, and it sounds weird every time I say it, they're browsing in a headless situation.

471
00:35:14,540 --> 00:35:15,980
And their screens look like this.

472
00:35:15,980 --> 00:35:19,260
This is our capture of their remote desktop.

473
00:35:19,560 --> 00:35:23,980
One of the things we find really interesting on Windows is when there's no monitor attached,

474
00:35:23,980 --> 00:35:27,720
instead of the screen being, because there's a virtual screen there, right?

475
00:35:27,720 --> 00:35:31,040
There's a virtual desktop even though it's not being displayed on the monitor.

476
00:35:32,840 --> 00:35:35,460
Not landscape, but it's portrait every time.

477
00:35:36,400 --> 00:35:38,080
That is some pretty significant impact.

478
00:35:38,080 --> 00:35:43,420
This is a browser that's maximized
on that portrait screen

479
00:35:43,420 --> 00:35:46,600
and you can see this big honking sidebar 
on the left-hand side.

480
00:35:46,600 --> 00:35:50,380
It's their favorite sidebar they didn't know it was open.

481
00:35:50,980 --> 00:35:58,760
But the visible portion, they're in a tablet layout.  Because of responsive design.

482
00:35:58,760 --> 00:36:00,300
Responsive design is fantastic.

483
00:36:00,620 --> 00:36:05,140
But we have to keep in mind this responsive design
or tablet layout

484
00:36:05,140 --> 00:36:09,400
is something somebody is now
using their keyboard to go through.

485
00:36:09,880 --> 00:36:13,720
They're not necessarily on a tablet.
We have to do more testing.

486
00:36:13,720 --> 00:36:22,120
This is another one where, you know, their browser
was actually half the width of the screen.

487
00:36:22,860 --> 00:36:27,480
This is real. Like we're not making this stuff up. This is real scenarios.

488
00:36:27,480 --> 00:36:33,280
The last one, we had to go in, this Window was I think 150 pixels by 150 pixels.

489
00:36:34,040 --> 00:36:39,540
We had to go in and make it a little bigger so we could actually ... as we were doing the remote session,

490
00:36:39,960 --> 00:36:44,960
we actually had to go in and resize it so we can even see what was going on and what they were interacting with.

491
00:36:46,880 --> 00:36:52,640
So this stuff is not, like, these assumptions that
we make about view port.

492
00:36:52,640 --> 00:36:58,100
That somebody is on mobile view and therefore using touch. It doesn't hold true.

493
00:36:58,620 --> 00:37:06,360
We need to do more. We have to test our mobile and tablet layouts and those breakpoints with the keyboard.

494
00:37:06,860 --> 00:37:07,840
We have to.

495
00:37:12,280 --> 00:37:14,920
Disability is often a usability amplifier.

496
00:37:14,920 --> 00:37:19,140
And I am a big believer this happens in both in a positive direction and negative direction.

497
00:37:20,300 --> 00:37:25,740
We have done lots of work with people,
people with disabilities and people without

498
00:37:25,740 --> 00:37:28,000
doing usability testing on the same product,

499
00:37:28,000 --> 00:37:34,100
same user tasks and we found time and time again
that people with disabilities

500
00:37:34,680 --> 00:37:38,180
find the same usability problems
as people without disabilities,

501
00:37:38,180 --> 00:37:41,040
but they find them faster
and they're much more pronounced.

502
00:37:41,040 --> 00:37:46,840
They're very much easier to see and kind of isolate in the interface

503
00:37:48,040 --> 00:37:51,480
than they would be for somebody that
doesn't have a disability.

504
00:37:52,040 --> 00:37:54,360
Somebody that doesn't have a disability
might just brush something off,

505
00:37:54,360 --> 00:37:58,000
and even though it slows them down by 2 seconds, 
they kind of move on.

506
00:37:59,040 --> 00:38:04,740
Somebody with a disability, that 2 second road block actually might become a 2 minute road block,

507
00:38:04,740 --> 00:38:08,840
or a 10 minute road block.
It really depends on what it is.

508
00:38:09,640 --> 00:38:17,220
We also see that making things better for somebody with a disability improves it for everyone.

509
00:38:17,220 --> 00:38:19,040
But maybe not to the same extent.

510
00:38:19,360 --> 00:38:24,600
So if I make a usability enhancement for me and it might help me get through something twice as fast,

511
00:38:25,580 --> 00:38:30,840
that same enhancement might help somebody that has a disability get through it ten times as fast.

512
00:38:31,960 --> 00:38:36,720
So we look at this and we see that disability
is often a usability amplifier.

513
00:38:37,660 --> 00:38:38,800
We do this all the time.

514
00:38:39,140 --> 00:38:42,240
All this stuff that you've taught us,
yes, it makes it more accessible.

515
00:38:42,700 --> 00:38:46,000
But really, fundamentally, this is just a better design.  Period.

516
00:38:46,000 --> 00:38:47,660
I'm a big believer in this.

517
00:38:47,660 --> 00:38:55,340
If we create things that work better for these extreme levels of ability, we're making things better for everyone.

518
00:38:56,720 --> 00:39:01,920
You may have seen this stuff.  This is ... what is this?

519
00:39:02,600 --> 00:39:05,000
It's part of like Fast Company, the magazine?

520
00:39:05,000 --> 00:39:09,900
This is a design related publication.  And this is from February 2006.

521
00:39:10,240 --> 00:39:13,940
Microsoft's radical bet on a new type of design thinking.

522
00:39:14,760 --> 00:39:17,020
Microsoft ... Microsoft is doing this.

523
00:39:17,280 --> 00:39:18,040
Google is doing this.

524
00:39:18,040 --> 00:39:22,640
Everybody is doing the things that we have been saying for 10-15 years now.

525
00:39:23,480 --> 00:39:25,760
They're doing it and making a huge splash with it.

526
00:39:25,760 --> 00:39:32,260
Anybody here work at Microsoft or Google? 
Okay, good. Cool.

527
00:39:33,200 --> 00:39:36,920
But this was a big article about this radical new way
of thinking.

528
00:39:36,920 --> 00:39:42,080
And Google is like, how designing for disabled people giving Google an edge!

529
00:39:43,600 --> 00:39:47,080
People are like, big companies are
waking up to this now.

530
00:39:47,400 --> 00:39:49,920
This was in May of 2016.

531
00:39:50,500 --> 00:39:58,120
There's a lot of people that have been talking about this since like January 2001. Right?

532
00:39:58,120 --> 00:40:03,240
This has been going on for awfully long time and now people are waking up to it.

533
00:40:03,740 --> 00:40:09,600
It's actually kind of fantastic but at the same time, I wish we had gotten to this point much, much sooner.

534
00:40:09,600 --> 00:40:16,840
But the fact that Google is talking about this and Microsoft is, that's a big boom for us.

535
00:40:19,700 --> 00:40:27,780
So couple of more examples and then we'll talk about some other things here.

536
00:40:31,380 --> 00:40:38,340
When we talk about designing for these extremes,
I want you to think of this.

537
00:40:38,340 --> 00:40:45,840
This is an example I use very often and what we did with this straw test is to limit our view of the screens.

538
00:40:45,840 --> 00:40:50,100
So that's really kind of an extreme that we're expressing for that design.

539
00:40:53,140 --> 00:40:55,520
They're a pain.

540
00:40:57,240 --> 00:41:03,660
And if you were to try and work with this data table in a magnified scenario,

541
00:41:03,660 --> 00:41:08,980
because you have low vision, you might be faced with something like this.

542
00:41:08,980 --> 00:41:16,300
And your ability can be the entire scope of the table is kind of severely,

543
00:41:16,300 --> 00:41:20,640
you know, hampered by the fact you have that screen.

544
00:41:20,640 --> 00:41:27,780
There's visual relationships that are created in data tables that maybe as low vision you're not going to see.

545
00:41:28,420 --> 00:41:33,840
But we can code this table of data so it works reasonably well for a screen reader user.

546
00:41:35,020 --> 00:41:38,160
But for someone with low vision,
this might be really difficult.

547
00:41:38,160 --> 00:41:44,340
So we're zoomed in at this level, it's maybe 400%, and I'm on this table cell where it has a number 10 in it,

548
00:41:44,340 --> 00:41:54,100
but it's a lot of work for me as a magnifier user to figure out what it's about and come back down

549
00:41:54,100 --> 00:41:58,420
and then to go over to the left to figure out what those two pieces of data were.

550
00:41:58,420 --> 00:42:01,480
Whereas, when I can see the entire thing,

551
00:42:01,480 --> 00:42:10,520
I can see here that this number 10 is Jupiter,
and it's hours in the day for that planet.

552
00:42:10,520 --> 00:42:13,940
I can see that readily.
Because I can see the whole table.

553
00:42:14,620 --> 00:42:16,620
But if I can't see that whole table,

554
00:42:17,580 --> 00:42:22,840
it becomes really much more difficult to do any comparison or data mining or whatever it is.

555
00:42:23,120 --> 00:42:25,120
So we start to play around with ideas like this.

556
00:42:26,100 --> 00:42:34,800
And that is functionality so that when you're magnified, you can actually pull those roads and column headers in

557
00:42:34,800 --> 00:42:36,800
so you can actually get that context.

558
00:42:37,180 --> 00:42:38,960
So I'll zoom it back out, so you can see that

559
00:42:38,960 --> 00:42:44,800
here's the entire table and as I click on a particular cell
or hover over a cell,

560
00:42:44,800 --> 00:42:49,560
we get this little call to action to bring the row 
and column headers in,

561
00:42:49,560 --> 00:42:54,420
so that somebody that uses a magnifier has limited use the screen.

562
00:42:55,660 --> 00:42:56,900
We can pull those things in.

563
00:42:57,880 --> 00:43:00,560
It's some simple CSS and simple JavaScript.

564
00:43:01,680 --> 00:43:06,700
And I swear to you, and as I'm looking around the room and people nodding, oh,

565
00:43:08,200 --> 00:43:12,320
almost everybody that I showed this too says,
I want that.

566
00:43:12,320 --> 00:43:14,320
And I can see the screen just fine.

567
00:43:14,320 --> 00:43:19,400
Because we get stuck with dealing with tables like this that are pages and pages and pages long.

568
00:43:19,400 --> 00:43:22,040
I mean, that's just poor design for everybody.

569
00:43:22,740 --> 00:43:24,740
But the impact of that poor design

570
00:43:25,640 --> 00:43:28,200
is going to be more pronounced on people
with different types of disabilities.

571
00:43:28,680 --> 00:43:32,340
So you know, what would this actually look like?
Or how would that work here?

572
00:43:32,820 --> 00:43:34,720
That might actually be even more important.

573
00:43:34,720 --> 00:43:39,400
If we can, we always love to break up these big massive long tables into smaller chunks.

574
00:43:39,400 --> 00:43:41,580
Into smaller tables if we can.

575
00:43:42,100 --> 00:43:43,440
But we can't always do that.

576
00:43:43,440 --> 00:43:46,580
So why don't we have a set of tools
that allow us to do this.

577
00:43:47,360 --> 00:43:54,780
If you want to see an example of it, examples dot Simply Accessible dot com forward slash cell dash headers.

578
00:43:55,240 --> 00:44:00,980
There's variations on it as well that we've create
that are slightly different.

579
00:44:00,980 --> 00:44:10,180
So we have a version where you could actually click and instead of bringing in one row header,

580
00:44:10,180 --> 00:44:16,260
you can actually bring in that entire,
that entire column to bring that over.

581
00:44:17,060 --> 00:44:19,140
Or bring in that entire header row.

582
00:44:19,140 --> 00:44:25,480
So if you were magnified, you have the ability to kind of traverse the road or column much easier.

583
00:44:28,840 --> 00:44:33,920
Now this was something that we kind of conceptualized and prototyped and put together quickly.

584
00:44:33,920 --> 00:44:39,240
It's not something I would say go out and take that code and put it on your tables and you're done.

585
00:44:39,720 --> 00:44:44,600
You would need to do work to do this, but almost everybody I showed this to says,

586
00:44:45,820 --> 00:44:48,520
because we deal with tons of financial data, right?

587
00:44:48,520 --> 00:44:53,700
Or we deal with annual reports.  And we want to have that ability to do stuff like this.

588
00:44:55,000 --> 00:45:00,060
So this is the kind of thing that you can do 
when you start

589
00:45:02,700 --> 00:45:06,980
really think about what it means
to have a limited view of the screen,

590
00:45:06,980 --> 00:45:11,200
and what impact that has on people with low vision.

591
00:45:12,780 --> 00:45:14,600
I'm going to share one more with you here.

592
00:45:14,600 --> 00:45:19,320
And this is a story about my dad.

593
00:45:21,980 --> 00:45:23,980
I want to ...

594
00:45:26,120 --> 00:45:29,180
I want people to design for extreme emotions as well.

595
00:45:31,580 --> 00:45:40,100
Several years ago, my parents, it's like a complicated story.  So I'll tell it in a straightforward way as I can.

596
00:45:40,560 --> 00:45:48,140
So my father is like, he's now ...
 I don't remember how old he is.

597
00:45:48,140 --> 00:45:49,840
He's older than I am.

598
00:45:49,840 --> 00:45:51,020
[Laughter]

599
00:45:51,020 --> 00:45:55,360
[Derek Featherstone]: This is him and me together.
He's the one with the sideburns.

600
00:45:56,400 --> 00:46:00,160
And you can tell it's the '70s
because this lamp the corner

601
00:46:00,820 --> 00:46:04,900
with that weird pattern
and the spiral around the central.

602
00:46:05,540 --> 00:46:11,420
People would pay tons of dollar for a lamp like that right now and they would call it retro.

603
00:46:11,420 --> 00:46:13,420
I wish we still had it.

604
00:46:13,420 --> 00:46:17,300
But my dad was a big burly dude.

605
00:46:17,920 --> 00:46:21,980
And there's a lot of things that have happened over time.

606
00:46:21,980 --> 00:46:26,320
And now he's older.  And he's had a lot of things that happened.

607
00:46:26,320 --> 00:46:33,720
He had prostate cancer.  And, so, he had a lot of treatment, he had hormone treatment.

608
00:46:33,720 --> 00:46:43,080
And he said, he's told me before, I'm very emotional about stuff now that he didn't use to ...

609
00:46:43,660 --> 00:46:49,100
Or he would say, maybe this is a little stereotypical
and he was my dad

610
00:46:49,100 --> 00:46:54,300
and he was brought up in that age where boys don't cry, right?

611
00:46:54,300 --> 00:46:57,200
And, so, he's my dad.  So of course he doesn't cry.

612
00:46:57,720 --> 00:47:02,920
But he cries.  Emotionally,
he was being set off by certain things.

613
00:47:03,300 --> 00:47:09,560
He actually was at the point where he was in a very, very extreme emotional state.

614
00:47:09,560 --> 00:47:14,780
Because he was away on a cruise with my mom,
and I had to call them,

615
00:47:14,780 --> 00:47:18,360
because his mom, my grandmother,
had just passed away.

616
00:47:19,600 --> 00:47:27,400
I was trying to get them to book tickets to come back, because they needed to fly back off the cruise.

617
00:47:27,400 --> 00:47:34,700
And, so, he was ready to book the tickets,
I ended up doing it with his credit card.

618
00:47:34,700 --> 00:47:37,960
Because he didn't want to do it.
And I started to try to unpack why?

619
00:47:37,960 --> 00:47:39,960
And I said you guys should sign up.

620
00:47:39,960 --> 00:47:45,000
We're Canadian, so Air Canada is our main airline.

621
00:47:45,000 --> 00:47:48,800
We have two airlines. That sounds really small.

622
00:47:49,280 --> 00:47:55,760
But Air Canada and West Canada our national airline and we can pretty much fly everywhere in the country.

623
00:47:56,320 --> 00:48:02,300
And you know, let's sign you up for Aeroplan,
which is our frequent flyer program for Air Canada.

624
00:48:02,840 --> 00:48:04,420
And he didn't want to do it.

625
00:48:05,380 --> 00:48:07,960
He's like, I don't want to do it. I'm digging into why.

626
00:48:08,520 --> 00:48:13,900
I'm worried about how he bought an MP3 player.
I won't say who it was from.

627
00:48:15,780 --> 00:48:19,500
But he went to register it online.

628
00:48:19,500 --> 00:48:20,500
Register for the warranty.

629
00:48:20,500 --> 00:48:26,980
My dad is the one of about 3 people in the world that actually go online and register warranty for things.

630
00:48:27,420 --> 00:48:33,800
And, so, he did that. And he was telling me about this form that he tried to fill in for the warranty.

631
00:48:33,800 --> 00:48:37,920
He said, I got through it all and I put the information in that I thought was right.

632
00:48:38,820 --> 00:48:41,900
And I thought everything was good.

633
00:48:41,900 --> 00:48:45,400
And I hit the submit button on it.

634
00:48:45,400 --> 00:48:46,340
And it came back.

635
00:48:46,340 --> 00:48:47,820
And it was basically a sea of red.

636
00:48:48,680 --> 00:48:50,940
And I'm like, what do you mean?

637
00:48:51,600 --> 00:48:56,820
And he said there's errors everywhere. And I froze. 
I didn't know what to do anymore.

638
00:48:57,500 --> 00:49:00,380
And I said, What would have made it better?

639
00:49:00,960 --> 00:49:04,920
He said, well, 
I really felt if they knew all the errors were there,

640
00:49:04,920 --> 00:49:11,400
why wouldn't they tell me before I submitted the form ... he wouldn’t really say that.

641
00:49:11,400 --> 00:49:13,400
Before I hit the button on the form.

642
00:49:13,960 --> 00:49:16,220
Why didn't they tell me that before?

643
00:49:16,220 --> 00:49:20,160
Now it's like overwhelming.  It was too much.

644
00:49:21,640 --> 00:49:30,220
And he just, he lost every bit of confidence he had after this transaction.  He wouldn't go back.

645
00:49:30,220 --> 00:49:35,800
And he wouldn't book those flights himself. He wouldn't sign up for Aeroplan, the loyalty program himself.

646
00:49:36,560 --> 00:49:43,080
He said when he did this, getting through these error messages, he felt like an idiot.

647
00:49:43,080 --> 00:49:49,680
Like, he's like, this is not a valid e-mail format.
This is how he's seeing them.

648
00:49:50,000 --> 00:49:53,780
Password doesn't contain a special character. Neither does this one. [Sigh]

649
00:49:55,360 --> 00:49:56,640
How can you not know your name?

650
00:49:56,640 --> 00:49:58,880
This is how he's feeling.

651
00:49:59,840 --> 00:50:01,240
This data is not formatted correctly.

652
00:50:01,240 --> 00:50:02,300
Come on.

653
00:50:03,760 --> 00:50:05,840
I bet you won't even get this right.

654
00:50:06,860 --> 00:50:08,040
Yep.  I was right.

655
00:50:08,040 --> 00:50:09,400
Seriously. Are you stupid?

656
00:50:09,920 --> 00:50:11,340
I can't wait for this to end.

657
00:50:11,680 --> 00:50:13,220
You're really not that smart.

658
00:50:13,660 --> 00:50:15,340
Odds are pretty slim on this one.

659
00:50:16,100 --> 00:50:17,620
Why do you use computers?

660
00:50:18,440 --> 00:50:24,240
This is what he was feeling. Not quite in those words
but that's what he felt the webpages were doing to him.

661
00:50:25,000 --> 00:50:29,540
This is my dad who doesn't cry,
and webpages made my dad cry.

662
00:50:31,640 --> 00:50:34,000
They’ve made you cry probably for different reasons.

663
00:50:34,840 --> 00:50:38,460
But they made him cry too.
And I was like, totally shocked about this.

664
00:50:38,460 --> 00:50:48,280
And he went to fix this for 2 hours before he actually successfully got the form to go through.

665
00:50:49,280 --> 00:50:58,240
Because he was overthinking at this point.
Error message, error message, fix that.

666
00:50:58,800 --> 00:51:00,440
And he couldn't get it done.

667
00:51:01,060 --> 00:51:06,700
And my dad was like, my dad was from Canada.
He didn't use computers.

668
00:51:07,420 --> 00:51:08,700
He's a mechanic.

669
00:51:09,100 --> 00:51:16,120
And now that he's retired, it's hard.
And we kind of forget that.

670
00:51:17,000 --> 00:51:19,000
There are a lot of new people out there.

671
00:51:21,580 --> 00:51:24,620
So I want us to kind of think about all of these things.

672
00:51:24,620 --> 00:51:28,760
I want us to think about the extremes
that people have to deal with.

673
00:51:30,940 --> 00:51:34,180
There's all scenarios,
everything I've shared here today,

674
00:51:34,180 --> 00:51:39,660
they're scenarios that you would kind of question it
and say, oh, that can't possibly have happened.

675
00:51:39,660 --> 00:51:43,040
Oh, that's like a one in whatever chance, right?

676
00:51:43,040 --> 00:51:49,240
Yeah, maybe my dad is a edge case.
Or maybe your dad or mom too.

677
00:51:50,340 --> 00:51:53,880
The problem is,
I like thinking about it this way.

678
00:51:55,680 --> 00:51:57,680
We say a lot of things in life.

679
00:51:57,680 --> 00:52:02,660
And as a teacher, I've said this,
to help one person, right?

680
00:52:02,660 --> 00:52:06,120
We're all excited.
We give that so much weight.

681
00:52:06,620 --> 00:52:12,180
If I can have helped just one person and made a difference, then we're really ecstatic about that.

682
00:52:12,680 --> 00:52:17,720
And when we think about that one person 
that we actually created a barrier for,

683
00:52:17,720 --> 00:52:19,720
we don't give it nearly that much weight.

684
00:52:20,040 --> 00:52:23,400
But we're like doing the opposite.
Like "Oh, its just one person."

685
00:52:24,180 --> 00:52:32,760
So it's really, really something that we've kind of embraced all of these different scenarios,

686
00:52:32,760 --> 00:52:37,300
things that seemed like edge cases in many ways seems like the norm.

687
00:52:38,120 --> 00:52:42,160
The people out there that we're designing for and building for are so not like us.

688
00:52:42,500 --> 00:52:43,780
They really aren't.

689
00:52:43,780 --> 00:52:45,780
We need to really keep that in mind.

690
00:52:46,240 --> 00:52:51,700
And the whole idea here is that
accessibility really is messy.

691
00:52:51,700 --> 00:52:58,800
These are things that ... you'll never see this stuff in a guideline, encapsulated all in a guideline.

692
00:52:59,300 --> 00:53:00,840
Do this, do this, do this.

693
00:53:01,680 --> 00:53:04,320
The real world, it's much more messy than that.

694
00:53:04,880 --> 00:53:06,640
I want you to be thinking about these things,

695
00:53:06,640 --> 00:53:09,600
like putting these extremes onto design problems
and then solving them.

696
00:53:10,840 --> 00:53:18,300
What I want you ... you know, a lot of people that are new to accessibility go into it and they say things like this.

697
00:53:19,460 --> 00:53:21,460
There's only so much I can do.

698
00:53:22,180 --> 00:53:25,340
Scratch out the “only” word.

699
00:53:26,660 --> 00:53:29,000
And just go with there's so much I can do.

700
00:53:29,000 --> 00:53:35,520
There's so many little things that you can do that make a huge difference for people with disabilities

701
00:53:35,520 --> 00:53:37,520
and how they use the web.

702
00:53:38,280 --> 00:53:41,160
I would love it if you would just go for it.

703
00:53:41,160 --> 00:53:43,160
I know. Some of you are doing this already.

704
00:53:43,160 --> 00:53:45,780
But I want you to think about some of the things that we talked about here

705
00:53:45,780 --> 00:53:49,340
as challenges that you haven't thought about before.

706
00:53:49,340 --> 00:53:51,160
Things you want to investigate more.

707
00:53:51,160 --> 00:53:53,160
How can you bring some of these things into your work?

708
00:53:54,680 --> 00:54:00,700
Doing the straw test on your wireframes and on your mockups, to look for those opportunities out there.

709
00:54:02,440 --> 00:54:06,880
And I want you to think about all of them.

710
00:54:06,880 --> 00:54:12,680
I know I have successfully almost spoken
until exactly 7:30.

711
00:54:14,120 --> 00:54:16,480
Which means I can't answer any questions at all.

712
00:54:16,480 --> 00:54:17,380
[Laughter]

713
00:54:17,380 --> 00:54:18,340
[Derek Featherstone]: Totally good.

714
00:54:18,780 --> 00:54:27,300
I am happy to kind of have really minimal discussion.  Keep your questions to two words or less.

715
00:54:27,300 --> 00:54:29,200
[Laughter]

716
00:54:29,200 --> 00:54:33,240
[Derek Featherstone]: But I'd love to talk.
And how long are we here?

717
00:54:33,240 --> 00:54:37,200
[Dennis Deacon]: We have until 8, but, you know ... 
give or take.

718
00:54:37,200 --> 00:54:40,280
[Derek Featherstone]: 8:03?

719
00:54:40,280 --> 00:54:42,280
[Dennis Deacon]: We'll go for it.

720
00:54:43,420 --> 00:54:46,580
[Derek Featherstone]: I would love to, if you want to ask questions, I'm happy to do that.

721
00:54:46,580 --> 00:54:52,900
And we can do it at this forum?  So I'm happy to take a few questions now and just hang.

722
00:54:52,900 --> 00:54:54,300
Question, go ahead sir.

723
00:54:54,300 --> 00:55:03,840
[Attendee]: First of all, thank you.  I hear what you're saying having done adaptive tech work.

724
00:55:05,020 --> 00:55:09,100
At a help desk, where I had somebody ones that said push the Windows keys. And they said what's that?

725
00:55:09,100 --> 00:55:11,100
You do have the extremes out the there.

726
00:55:11,100 --> 00:55:22,460
But I wanted to ask you, I do QA testing.  But I'm totally blind.  So my main focus is the screen reader.

727
00:55:22,460 --> 00:55:29,980
Are there things that I can do to maybe try to hit a few of these extremes a little bit more carefully?

728
00:55:29,980 --> 00:55:41,460
Things I should be listening for in that?  It's really tough to cover all the basis.  I feel like I can cover more.

729
00:55:41,460 --> 00:55:45,400
[Derek Featherstone]: I know, do you use an iPad by any chance?

730
00:55:45,400 --> 00:55:46,140
[Attendee]: I do, yes.

731
00:55:46,140 --> 00:55:54,100
[Derek Featherstone]: One of the things that I love about the iPad and touchscreen, iOS touchscreen device.

732
00:55:55,560 --> 00:55:56,820
You have explore by touch.

733
00:55:56,820 --> 00:56:02,380
So even yourself, even though you're completely blind, you can explore by touch over the entire interface.

734
00:56:03,120 --> 00:56:07,340
By dragging your finger around, I don't know if you use it by touch very much.

735
00:56:08,160 --> 00:56:11,680
But that can easily show you
some of these layout problems.

736
00:56:11,680 --> 00:56:16,940
And one of the layout problems that we often see happens for people with low vision,

737
00:56:16,940 --> 00:56:20,580
I would look for very clearly ... change that.

738
00:56:20,580 --> 00:56:28,520
I would listen for on VoiceOver things like forms or content that appears to be in multiple columns.

739
00:56:29,140 --> 00:56:32,120
Multiple columns for someone with low vision
can be a huge deal.

740
00:56:32,720 --> 00:56:37,420
The form button ... we see form buttons all the time

741
00:56:37,420 --> 00:56:41,700
that are down on the bottom left corner,
bottom right corner of the interface,

742
00:56:42,040 --> 00:56:46,920
and they're like, always in the bottom right corner which seems really predictable and stuff.

743
00:56:47,400 --> 00:56:52,620
But for someone that has low vision, if there's like massive amount of white space there,

744
00:56:52,620 --> 00:56:56,160
that button that's on the bottom right corner
might not be noticeable.

745
00:56:56,620 --> 00:57:01,820
You can, you know, it's obviously, there's a lot of more exploration that you can do there

746
00:57:01,820 --> 00:57:03,820
or you would need to do.

747
00:57:05,300 --> 00:57:12,920
One of the things that is a huge issue is like mismatched ALT text.

748
00:57:13,920 --> 00:57:21,080
And when the ALT text on an image says one thing, but the actual text that's visible on it says another thing.

749
00:57:21,080 --> 00:57:26,900
It's creates issues for people that use Dragon NaturallySpeaking. Not that they can't get around it,

750
00:57:26,900 --> 00:57:32,500
but if this ... let me see what I'm trying to find.

751
00:57:32,500 --> 00:57:34,080
[Attendee]: That one I have caught.

752
00:57:34,080 --> 00:57:34,600
[Derek Featherstone]: Good.

753
00:57:34,600 --> 00:57:37,340
Mismatched ALT text can be really difficult.

754
00:57:37,340 --> 00:57:46,820
I'll show this desktop again.  Pretend this desktop is a webpage.  It's just a desktop.

755
00:57:47,840 --> 00:57:50,160
This is a link to Apache.

756
00:57:51,440 --> 00:57:56,860
Just assume for a second, that this was an image
and the image says Apache on it.

757
00:57:56,860 --> 00:58:00,860
But beneath the hood the ALT text was OpenOffice.

758
00:58:02,060 --> 00:58:08,500
If I'm looking at that screen, and I'm using voice recognition software, I'm going to say click "Apache."

759
00:58:10,320 --> 00:58:12,940
But if the ALT text underneath says Open Office,

760
00:58:15,360 --> 00:58:17,240
That's mismatched ALT text is actually ...

761
00:58:17,240 --> 00:58:22,100
Everybody thinks about ALT text as being like ... this is critical for people with visual impairment.

762
00:58:23,460 --> 00:58:25,940
Just as critical for people that use Dragon NaturallySpeaking.

763
00:58:26,280 --> 00:58:28,660
Particularly when things are images that are active.

764
00:58:30,300 --> 00:58:33,760
So if you're catching that, that's a huge boom.

765
00:58:35,900 --> 00:58:43,260
The last one that I'll give you, and you're probably coming across this as a screen reader user

766
00:58:43,260 --> 00:58:46,700
Things that look clickable, but aren't actually clickable.

767
00:58:47,440 --> 00:58:52,160
You can't tab to it. Or it's clickable, but it's a clickable div. It's not a button or a link.

768
00:58:53,540 --> 00:58:56,280
For someone that's using Dragon NaturallySpeaking,

769
00:58:57,200 --> 00:59:00,480
like there's ways around it,
but that really slows them down,

770
00:59:01,480 --> 00:59:05,440
to click on these things that aren't
natively focusable or clickable.

771
00:59:05,440 --> 00:59:09,360
So those, know that you're not just
finding them for yourself,

772
00:59:09,360 --> 00:59:14,440
but you're finding them for every
Dragon user out there as well.

773
00:59:14,980 --> 00:59:19,660
I'd love to talk with you more about that stuff because I love to put more thought into

774
00:59:19,660 --> 00:59:24,720
other things that you could find pretty readily.

775
00:59:24,720 --> 00:59:27,380
So, let's talk more about that.
What's your name?

776
00:59:27,380 --> 00:59:33,640
[Attendee]: Ray Campbell. I am a QA with United Airlines. I work with Dennis. Don't hold that against me.

777
00:59:33,640 --> 00:59:36,900
[Derek Featherstone]: I wouldn't think of it.

778
00:59:38,500 --> 00:59:40,500
Question in the back.

779
00:59:40,500 --> 00:59:51,420
[Attendee]: Text-to-speech, or speech-to-text in Dragon is from people that are focusing in on different aspects

780
00:59:51,420 --> 00:59:54,520
of accessibility and they find that to be the most challenging right now.

781
00:59:54,520 --> 00:59:58,300
[Indecipherable]

782
00:59:58,300 --> 01:00:00,300
And I'm trying to learn more about that.

783
01:00:00,300 --> 01:00:02,300
[Dennis]: Could you repeat the question.

784
01:00:02,300 --> 01:00:07,760
[Derek Featherstone]: The question was, you've heard about Dragon NaturallySpeaking.

785
01:00:08,800 --> 01:00:13,780
To kind of focus on that a little bit more, there's not a lot of info out there.  What kind of resources are there?

786
01:00:13,780 --> 01:00:16,080
Is that good paraphrasing or not?

787
01:00:16,080 --> 01:00:18,080
[Attendee]: Yes.

788
01:00:20,460 --> 01:00:24,340
[Derek Featherstone]: There's not great resources out there, but what I would recommend you do,

789
01:00:24,340 --> 01:00:29,140
if you want to learn about Dragon, right now, it's $100.

790
01:00:31,840 --> 01:00:36,800
It is a piece of assistive technology that I would recommend that you go and try it out

791
01:00:36,800 --> 01:00:40,660
and learn about it and read through the documentation and learn about how it works.

792
01:00:40,660 --> 01:00:44,660
We write articles about it on our site, SimplyAccessible.com, so

793
01:00:44,660 --> 01:00:46,820
But we just don't just write about Dragon,

794
01:00:46,820 --> 01:00:54,340
but we write about all the kind of disabilities we can
and cover many types of disability,

795
01:00:54,340 --> 01:01:00,580
and there's lots of videos out there speaking in conferences and meet ups like this

796
01:01:00,580 --> 01:01:05,980
where I'm doing demos of Dragon.
So you can certainly learn things there.

797
01:01:06,520 --> 01:01:11,680
The best part about building things that work for almost any assistive technology ...

798
01:01:13,260 --> 01:01:14,980
is make it simple.

799
01:01:15,900 --> 01:01:21,120
Use buttons. Use links.
Use straight up great quality HTML.

800
01:01:21,120 --> 01:01:28,080
And you can make things that you're building work very well, very easily, for a lot of assistive technology.

801
01:01:28,080 --> 01:01:31,960
It's not simple as that,
but in many ways it is as simple as that.

802
01:01:31,960 --> 01:01:37,820
So that clickable div, doesn't work for anybody that's just trying to use the keyboard.

803
01:01:39,080 --> 01:01:46,620
So using buttons and links that I can things hum.
So think about that kind of stuff.

804
01:01:46,620 --> 01:01:52,440
As you're doing it. Because a lot of simple things you can do is, you don't really have to research.

805
01:01:52,440 --> 01:01:54,440
It's not like a core cut Dragon or anything like that.

806
01:01:54,440 --> 01:02:01,200
It's more, if we build it this way, it's going to be usable by the widest variety of people possible kind of thing.

807
01:02:03,380 --> 01:02:04,460
It really helps.

808
01:02:04,460 --> 01:02:07,040
If you have any other questions, feel free to get in touch.

809
01:02:07,040 --> 01:02:11,060
I'll put this up here too.
Hang on a second before we finish.

810
01:02:13,000 --> 01:02:14,660
Just so you can get in touch.

811
01:02:14,660 --> 01:02:16,660
If you want to connect on Twitter,
I'm @feather on Twitter.

812
01:02:17,120 --> 01:02:23,320
If you want to e-mail ... not me, because sometimes my Inboxes are like a black hole.

813
01:02:23,320 --> 01:02:29,740
Because certain reasons.
So hello@simplyaccessible.com

814
01:02:29,740 --> 01:02:35,060
is a great way to get in touch and we often use the question that is come in

815
01:02:36,940 --> 01:02:39,680
as prompts to write an article about X.

816
01:02:39,680 --> 01:02:44,240
So if you have questions, we would love for you to ask them and we would often write about it.

817
01:02:44,240 --> 01:02:46,240
So another question in the back?

818
01:02:47,340 --> 01:04:19,260
[Attendee]: [Garbled]

819
01:04:19,260 --> 01:04:23,180
[Derek Featherstone]: So to bring it together, ultimately the question from both of you is,

820
01:04:23,180 --> 01:04:27,400
how do you get people to go the extra edge or extra mile or whatever it is.

821
01:04:30,320 --> 01:04:32,160
Make it not anything extra.

822
01:04:32,540 --> 01:04:36,660
Our focus entirely is, we bake it in.

823
01:04:36,660 --> 01:04:38,660
So it's not seen as an optional thing.

824
01:04:38,660 --> 01:04:40,660
It's not like this thing that can be left.

825
01:04:41,980 --> 01:04:44,540
If we get to it, if we have time, great.

826
01:04:45,360 --> 01:04:49,720
Because guess what? As soon as it becomes a thing, if we have time to do it, we'll do it.

827
01:04:50,500 --> 01:04:52,820
There's never time to do it. Right?

828
01:04:53,440 --> 01:04:57,440
If it's not baked in, you're kind of, like,

829
01:04:57,440 --> 01:05:07,220
we spend half of our time or at least half of our time not just helping teams fix things that are like websites,

830
01:05:07,220 --> 01:05:13,480
we actually spend a good chunk of our time, maybe three-quarters helping people fix their process,

831
01:05:14,460 --> 01:05:22,220
and fix their systems in the way that they work, and their mindset, so it's not ... never seen as an extra thing.

832
01:05:22,220 --> 01:05:24,660
It's actually just the way we do it.

833
01:05:25,580 --> 01:05:27,580
Kind of totally avoiding the question.

834
01:05:27,980 --> 01:05:30,800
But it's a big part of it is mindset.

835
01:05:31,260 --> 01:05:34,460
It's not an extra thing.  It's actually part of it.

836
01:05:34,460 --> 01:05:40,220
And we know lots of millennials that have disabilities. Loads of them.

837
01:05:40,220 --> 01:05:45,460
I don't know if you saw this, there's an article that came out not too long ago

838
01:05:45,460 --> 01:05:58,160
that younger generation in China right now, 75% of males between the age of 18 and 25, 75%.

839
01:05:58,160 --> 01:06:01,960
It's always been kind of like roughly 1/3 of the people.

840
01:06:01,960 --> 01:06:07,100
If you look at this room and we're probably geeky nerds that look at screens all day,

841
01:06:08,280 --> 01:06:13,040
we're probably slightly higher than say, 1/3 of people that need some kind of corrective eyewear.

842
01:06:13,040 --> 01:06:18,340
But in China right now, it's 18 to 25, there could be a different scenario,

843
01:06:18,340 --> 01:06:21,680
but 75% or more need glasses right now.

844
01:06:21,680 --> 01:06:23,680
So things are changing, right?

845
01:06:23,680 --> 01:06:31,260
There are things we can point to that say, for yourself now, but do it for your future self as well.

846
01:06:31,260 --> 01:08:05,220
[Attendee]: [Garbled]

847
01:08:05,220 --> 01:08:12,620
[Derek Featherstone]: Just to summarize that, a huge, huge part of this is education.  Right?

848
01:08:12,620 --> 01:08:14,620
It has to be part of everything.

849
01:08:14,620 --> 01:08:20,560
And that makes it, you know, when we know what you're doing, it doesn't seem like a mountain.

850
01:08:20,560 --> 01:08:25,300
You know, much smaller chunks of work that needs to get done.

851
01:08:26,700 --> 01:08:30,660
So that education part of it is partial.
It will surprise you,

852
01:08:30,660 --> 01:08:34,260
part of the reason that I'm here teaching and sharing things with you,

853
01:08:34,260 --> 01:08:37,360
because it helps bring the level up for everybody.

854
01:08:37,360 --> 01:08:44,420
I used to be a high school teacher, and it's big part of what I do and it's a big part of what our mission is.

855
01:08:44,980 --> 01:08:47,820
We want to actually say this internally.

856
01:08:47,820 --> 01:08:50,260
Our mission is to go and make more believers.

857
01:08:50,880 --> 01:08:54,280
That this is important, that this matters.

858
01:08:55,500 --> 01:09:00,600
Currently, you don't get to work with us if you're not somebody that believes this is

859
01:09:00,600 --> 01:09:04,460
some of the most important work
that anybody gets to do.

860
01:09:06,140 --> 01:09:11,020
And, so, our mission is to actually go up there and make more believers out of more people.

861
01:09:12,440 --> 01:09:14,440
Like, literally, that's it.

862
01:09:15,400 --> 01:09:20,920
If we can do that, then we know we're succeeding, because with that education level rises,

863
01:09:22,640 --> 01:09:27,140
we know how to do this. We can do this.

864
01:09:27,140 --> 01:09:32,880
All the teams that we work with, large and small, they get to a point where when they're working with us,

865
01:09:32,880 --> 01:09:39,060
it starts to click.  It makes sense.  And it becomes the way that they do things.

866
01:09:39,540 --> 01:09:43,760
When they have been doing it for long enough, you know, 6 months or a year or whatever it is,

867
01:09:43,760 --> 01:09:45,760
they don't need that checklist anymore.

868
01:09:46,980 --> 01:09:49,740
They need that list at the beginning because they don't know where to start.

869
01:09:51,460 --> 01:09:55,040
But that disappears and it goes away, because you build it into your practice.

870
01:09:55,040 --> 01:09:58,600
You build things like pattern libraries that has accessibility built in.

871
01:10:00,480 --> 01:10:07,020
They have color palettes that are free vetted for color contrast so you have color combinations that work.

872
01:10:07,760 --> 01:10:11,340
You don't even have to test them out until the next time you rebrand.

873
01:10:13,900 --> 01:10:16,320
So that education is critical.

874
01:10:16,320 --> 01:10:22,400
And I mentioned this, I would be absolutely silly to not do this with such a captive audience here.

875
01:10:22,400 --> 01:10:29,320
If you're interested in the kinds of things that we do, and Dennis actually reminded me to do this before.

876
01:10:29,320 --> 01:10:31,840
We need people.

877
01:10:31,840 --> 01:10:40,840
SAteach.es/jobs

878
01:10:41,260 --> 01:10:43,440
We're hiring testers and consultants.

879
01:10:43,440 --> 01:10:48,160
Here's the cool thing.  We have a US company too.

880
01:10:48,900 --> 01:10:55,940
Patrick works for us and he works in Chicago.

881
01:10:55,940 --> 01:10:57,940
Elle works for us and she's in Louisville Kentucky

882
01:10:57,940 --> 01:11:08,660
and we have people in Vancouver, Nova Scotia, Philippines, Ottawa, Seattle. Hawaii.

883
01:11:08,660 --> 01:11:11,080
Hawaii! How cool is that?

884
01:11:11,080 --> 01:11:15,320
People work for us and the entire team is remote.

885
01:11:16,120 --> 01:11:19,860
We can talk about all that kind of stuff, too, afterwards.

886
01:11:19,860 --> 01:11:22,320
Elle, is this a comment or question?

887
01:11:22,320 --> 01:11:42,500
[Attendee]: Garbled

888
01:11:42,500 --> 01:11:46,740
[Derek Featherstone]: Yeah, this quote, all this stuff you've taught us, yes, make this more accessible.

889
01:11:46,740 --> 01:11:50,420
But really, fundamentally, this is just a better design, period.

890
01:11:51,180 --> 01:11:57,040
Four years ago, in this office, we were doing training, some workshops

891
01:11:57,040 --> 01:12:03,060
for Critical Mass designers and developers, and part management types,

892
01:12:03,060 --> 01:12:09,660
and they were working with us as partners for Humana.

893
01:12:09,660 --> 01:12:14,020
So we were working for Humana.  Do you want to tell this part of the story?

894
01:12:15,580 --> 01:12:19,320
Elle worked for Humana. She ran the accessibility program at Humana

895
01:12:19,740 --> 01:12:24,660
and Critical Mass was hired as part of the team to do this big redesign.

896
01:12:26,100 --> 01:12:30,240
We were Simply Accessible hired to be part of the team.

897
01:12:30,840 --> 01:12:34,980
And this happened, Critical Mass, the lead designer,

898
01:12:35,440 --> 01:12:41,120
after a full day workshop with us, after looking at all these examples, she actually came up with this.

899
01:12:41,120 --> 01:12:45,460
And she said, all this stuff you've taught us, yes, you made it more accessible.

900
01:12:45,460 --> 01:12:48,540
But you've just made it better design.  Period.

901
01:12:48,540 --> 01:12:56,380
I was like, this moment where, I was like, oh, my God! They got it!

902
01:12:56,620 --> 01:12:59,760
It was like, mission accomplished!

903
01:12:59,760 --> 01:13:03,820
Because that was exactly what we believe in and we've seen time and time again.

904
01:13:04,180 --> 01:13:10,820
So this is pretty, kind of, fun to be able to be here and talk about it. It happened right here.

905
01:13:10,820 --> 01:13:12,820
[Attendee]: I'll give you another one.

906
01:13:12,820 --> 01:13:21,000
That is, the more education we do, the more likely we'll put people like you out of business.

907
01:13:21,000 --> 01:13:22,740
Because everybody will get it.

908
01:13:22,740 --> 01:13:27,000
[Derek Featherstone]: Yeah ... 
I have mix feelings about that.

909
01:13:27,000 --> 01:13:28,760
[Laughter]

910
01:13:28,760 --> 01:13:37,580
We actually say this.  A little insight into our work.

911
01:13:37,580 --> 01:13:43,420
We actually say with every client, our goal is that by the end of it, you don't need us anymore.

912
01:13:45,200 --> 01:13:49,640
Well, you still want to work with us because
we're fun and stuff,

913
01:13:49,640 --> 01:13:57,500
but if things go well, you don't need us anymore.  And we're good with that.

914
01:13:57,500 --> 01:15:03,380
[Attendee]: [Garbled]

915
01:15:03,380 --> 01:15:11,000
[Derek Featherstone]: I'll summarize again for the captioning.  It was a magical time, definitely.

916
01:15:11,000 --> 01:15:23,020
And for the UX team to feel like it was something that, it's earned and created a need for innovation.

917
01:15:23,020 --> 01:15:29,800
And it wasn't something that was hampering people.  It was like we can do better and we can do this.

918
01:15:30,280 --> 01:15:35,520
It sparked a lot of creativity in the solutions that we’ve created.

919
01:15:36,700 --> 01:15:43,660
And, so, it was a special time.  We did put -- absolutely put the user first as a fundamental requirement.

920
01:15:43,660 --> 01:15:47,940
It was a requirement, and not just because Elle said so.

921
01:15:47,940 --> 01:15:51,800
It was a requirement because there were regulations that say,

922
01:15:52,480 --> 01:15:57,220
but we did ... I kind of get goosebumps thinking about it.

923
01:15:57,220 --> 01:16:09,100
Because Elle straight up said, we're putting together this team, and it was, it was exactly that.

924
01:16:09,100 --> 01:16:14,920
A team that said, “good enough isn't enough.”  Period.

925
01:16:15,700 --> 01:16:17,960
And that was, it was awesome.

926
01:16:18,720 --> 01:16:24,480
It was awesome! It was pretty amazing. 
And now she works with us.  Yeah.

927
01:16:24,480 --> 01:16:27,340
[Attendee]: What are some requirements in the United States?

928
01:16:27,340 --> 01:16:30,300
[Attendee]: If DOJ gets off their butts and release it.

929
01:16:30,300 --> 01:19:13,400
[Attendee]: [Garbled]

930
01:19:13,400 --> 01:19:16,160
[Derek Featherstone]: She's typing all of this up.

931
01:19:29,020 --> 01:19:34,120
I'll just summarize in text. Because the conversation in the back doesn't come through for the live captioning.

932
01:19:34,580 --> 01:19:40,600
So I was summarizing bunch of things but I got tired talking so I typed it instead.

933
01:19:42,860 --> 01:19:47,380
Cool. You just want to have Bourbon or do you have any more questions?

934
01:19:49,920 --> 01:19:55,900
I'm not going to force anybody.  But we've got, we're here for a little bit longer.

935
01:19:55,900 --> 01:20:00,220
I'm happy to just go around and chat. 
I would love to talk with you.

936
01:20:00,220 --> 01:20:03,880
And thank you so much for being here.

937
01:20:03,880 --> 01:20:11,200
[Applause]

