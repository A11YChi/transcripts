# Automating Peace of Mind with Accessibility Testing & CI
## Marcy Sutton - Wednesday, May 3, 2017
[Source recording](https://www.youtube.com/watch?v=9x-MRZEEONE)

**[Dennis]:** Please give a warm, Chicago welcome to Marcy Sutton.

**[Applause]**

**[Marcy]** Hello, everyone. Should we check this microphone? This one's for the captions, right?

**[Dennis]** That's for the stream and the captions.

**[Marcy]** For everyone on there. Okay well I guess I'll just talk loud enough so this mic picks me up. Hi everyone. I'm super excited to be here.

8
00:00:36,400 --> 00:00:40,600
I'm going to talk to you about the technical side of accessibility.

9
00:00:40,880 --> 00:00:45,120
So a bit of a fair warning, that I'm a developer so this will be really technical.

10
00:00:45,440 --> 00:00:48,640
But if there's anything that you need extra explanation on,

11
00:00:48,840 --> 00:00:52,920
we're going to do Q&A at the end so I'm happy to answer any questions that you have.

12
00:00:54,540 --> 00:00:58,820
My name is Marcy Sutton as Dennis mentioned. You can find me on Twitter at @MarcySutton.

13
00:00:59,780 --> 00:01:05,520
I work at Deque Systems as a senior front-end engineer, so I work on browser extensions,

14
00:01:05,520 --> 00:01:12,640
APIs for developers to test for accessibility so that we're helping developers figure it out on their own

15
00:01:12,640 --> 00:01:15,720
so that you can become self-sustaining at accessibility

16
00:01:15,720 --> 00:01:20,180
and really catch those easy bugs that we shouldn't make those mistakes over and over.

17
00:01:21,020 --> 00:01:28,360
My slides can be found online at bit.ly/a11y-and-ci

18
00:01:29,120 --> 00:01:30,620
and they're on github too.

19
00:01:32,560 --> 00:01:36,480
So a bit of a background about me, at Deque, I work on the aXe core team.

20
00:01:36,480 --> 00:01:43,000
And I'll tell you all about that a little bit later in the talk and I have stickers if anybody wants some aXecore stickers.

21
00:01:43,080 --> 00:01:45,280
since we have heard now that everyone loves stickers.

22
00:01:46,420 --> 00:01:52,780
I have a course on accessibility on egghead.io where I demo how to do some technical topics,

23
00:01:52,780 --> 00:01:58,140
really general accessibility things, since egghead had no  accessibility content at all,

24
00:01:58,520 --> 00:02:03,680
they convinced me to start contributing some videos and I add to it as time goes on,

25
00:02:03,680 --> 00:02:06,000
typically not during conference season.

26
00:02:06,400 --> 00:02:07,600
We have a question already?

27
00:02:07,600 --> 00:02:08,380
[Attendee] Is it free?

28
00:02:08,380 --> 00:02:09,580
Yes, it is free.

29
00:02:10,680 --> 00:02:14,180
Free videos and they're short, I think under 15 minutes.

30
00:02:14,180 --> 00:02:18,160
It's really hard to jam that much content into a short video.

31
00:02:18,880 --> 00:02:23,000
I, in a past, have co-led the Seattle chapter of Girl Develop It,

32
00:02:23,000 --> 00:02:26,980
which is a non-profit encouraging adult women in software

33
00:02:27,740 --> 00:02:33,440
I've since moved to Bellingham Washington, so I don't run the Seattle chapter of Girl Develop It anymore.

34
00:02:34,240 --> 00:02:36,220
I actually need to update this slide because

35
00:02:36,220 --> 00:02:41,020
I do run the Seattle Accessibility Meetup as of about two months ago.

36
00:02:41,540 --> 00:02:45,520
So we're hosting a Global Accessibility Awareness Day event there

37
00:02:45,520 --> 00:02:49,280
and it'll be interesting to see what we end up doing.

38
00:02:49,280 --> 00:02:51,280
I'm definitely going to take some inspiration from this meetup,

39
00:02:52,000 --> 00:02:54,580
since you seem to have great content going all the time.

40
00:02:56,180 --> 00:02:57,560
I used to work with the Angular team.

41
00:02:57,560 --> 00:03:03,700
I worked on Angular material UI framework for almost a year and I still contribute comments

42
00:03:03,700 --> 00:03:08,700
on component specs to the teams at Google give them feedback on their websites,

43
00:03:08,700 --> 00:03:11,280
which need a little bit of help to be honest.

44
00:03:11,280 --> 00:03:12,300
[Laughter]

45
00:03:12,300 --> 00:03:19,580
But I am very heavy on the JavaScript side and providing talks and blog posts and things

46
00:03:19,580 --> 00:03:22,920
on client rendered accessibility and JavaScript stuff.

47
00:03:25,740 --> 00:03:29,060
A little plug for my blog called Accessibility Wins.

48
00:03:29,060 --> 00:03:35,360
It's a11ywins.tumblr.com and if you've got something that you're really proud of I would love to hear about it.

49
00:03:35,360 --> 00:03:39,060
So you could submit it to me and I will write glowingly about it.

50
00:03:39,980 --> 00:03:45,380
It's really hard to find wins out there, so I try to put a positive spin on accessibility.

51
00:03:46,000 --> 00:03:49,620
Sometimes it's not perfect, and I'll talk about that in a post,

52
00:03:49,620 --> 00:03:54,460
but I try not to let perfection preventing me from highlighting the wins,

53
00:03:54,460 --> 00:03:56,840
because we need to celebrate what's going right.

54
00:03:57,220 --> 00:03:59,700
So I'd love to hear if you have something that you're proud of.

55
00:04:02,280 --> 00:04:08,420
Okay, so, this talk originated from experience I had working at a digital agency,

56
00:04:08,420 --> 00:04:11,240
where we didn't do any software testing at all.

57
00:04:11,660 --> 00:04:14,180
And I remember sitting at my desk with my colleague going,

58
00:04:14,700 --> 00:04:20,220
I keep experiencing really painful deployments of websites that we've worked on

59
00:04:20,740 --> 00:04:26,220
where I broke something and QA'd like maybe I broke something on a page I wasn't thinking about

60
00:04:26,220 --> 00:04:30,640
because I didn't know I'd reused a component or something and QA didn't know to test it and

61
00:04:31,200 --> 00:04:35,680
everybody looks bad in that scenario and I knew there had to be a better way.

62
00:04:36,480 --> 00:04:41,480
I thought this ... I'd heard of this thing called software testing and I leaned over my colleague and said

63
00:04:41,960 --> 00:04:43,500
do we do any software testing?

64
00:04:43,500 --> 00:04:44,460
And he said, "Nah ...

65
00:04:46,000 --> 00:04:46,560
we don't."

66
00:04:46,560 --> 00:04:47,060
[Laughter]

67
00:04:47,060 --> 00:04:48,280
I went, "oh."

68
00:04:48,520 --> 00:04:52,400
Okay, well, I guess if I want to learn that I need to pursue that in my career.

69
00:04:52,400 --> 00:04:57,120
And so I found another job working at a company called Substantial.

70
00:04:57,120 --> 00:05:00,480
And they were really pragmatic about their software development.

71
00:05:00,480 --> 00:05:02,480
I learned how to write software tests.

72
00:05:02,920 --> 00:05:06,820
I ended up working on the Angular team after that and that was very heavy with software tests.

73
00:05:07,700 --> 00:05:11,320
And I grew to love that as a practice because it was all about software quality.

74
00:05:11,900 --> 00:05:15,160
And as time went on, I learned that I could work accessibility into that as well.

75
00:05:15,160 --> 00:05:16,640
So I'm going to tell you about that.

76
00:05:18,400 --> 00:05:21,220
So imagine this scenario. You just shipped a redesign you know,

77
00:05:21,220 --> 00:05:25,220
you flip the switch on your brand-new gorgeous website and all of a sudden,

78
00:05:25,220 --> 00:05:27,840
if you haven't addressed accessibility at all,

79
00:05:28,320 --> 00:05:32,500
you could be making your website unusable to 15% of users just like that.

80
00:05:33,340 --> 00:05:37,180
Because you didn't test it for accessibility and I think I'm preaching to the choir here.

81
00:05:37,180 --> 00:05:40,080
Obviously we all care about accessibility enough to be here.

82
00:05:40,360 --> 00:05:45,980
But we probably all have experienced this where you see teams who aren't doing accessibility,

83
00:05:45,980 --> 00:05:51,140
and, that fast, you could push code out to you know a new production server

84
00:05:51,140 --> 00:05:53,120
and all of a sudden people can't use it.

85
00:05:53,700 --> 00:05:56,800
Or maybe it regresses and that's a really common scenario.

86
00:06:00,320 --> 00:06:03,140
Pretty familiar everyone here, what is web accessibility?

87
00:06:03,140 --> 00:06:08,280
To me, it means that people with disabilities can interact with the web and contribute to the web.

88
00:06:08,840 --> 00:06:12,420
And so I keep this in here when I'm talking to really technical audiences

89
00:06:12,420 --> 00:06:14,780
who don't know anything about accessibility.

90
00:06:14,940 --> 00:06:16,980
If we start from with software testing,

91
00:06:17,440 --> 00:06:21,280
it's a really great way to kind of open that door to this world of accessibility

92
00:06:21,280 --> 00:06:24,720
and talk about how we can make these things work together.

93
00:06:27,060 --> 00:06:28,560
So with testing,

94
00:06:28,560 --> 00:06:31,160
if you don't have any test coverage at all,

95
00:06:31,160 --> 00:06:34,320
you could be one bad deployment away from failure.

96
00:06:34,500 --> 00:06:36,000
Like I said, you could flip the switch,

97
00:06:36,000 --> 00:06:38,000
all of a sudden your site is unusable.

98
00:06:38,240 --> 00:06:40,240
And I have a really amazing animated gif

99
00:06:40,240 --> 00:06:42,440
of a car trying to merge into traffic

100
00:06:43,100 --> 00:06:44,900
and it just ... it goes really horribly.

101
00:06:45,200 --> 00:06:48,140
And so that's kind of what I think about with a bad deployment.

102
00:06:48,560 --> 00:06:50,280
So we want to protect ourselves from that.

103
00:06:50,280 --> 00:06:54,280
We want to have some test coverage to help mitigate this ahead of time,

104
00:06:54,720 --> 00:06:59,700
so that we're not having to go and tell our leadership team we broke it without realizing it.

105
00:07:02,340 --> 00:07:05,860
So software testing, as I learned over time, it's really a winning strategy,

106
00:07:05,860 --> 00:07:10,480
but not only for software quality in general but also for web accessibility.

107
00:07:10,480 --> 00:07:15,380
And it made me think of Kramer's coffee table book of coffee tables from Seinfeld.

108
00:07:15,380 --> 00:07:16,240
[Laughter]

109
00:07:16,240 --> 00:07:18,060
Because it's kind of a meta concept.

110
00:07:18,280 --> 00:07:22,840
You've got your code and then you write tests the assert that your code does what you want,

111
00:07:23,480 --> 00:07:28,660
And so it's the sort of this meta concept and makes me one watch more episodes of Seinfeld.

112
00:07:31,180 --> 00:07:34,540
So today we'll talk about software quality and how it applies to accessibility.

113
00:07:34,540 --> 00:07:40,580
Because that's a great way to really try and break through to people who are not caring about accessibility.

114
00:07:40,580 --> 00:07:44,260
If you make it a quality issue, not only that it's about people,

115
00:07:44,260 --> 00:07:50,420
but if you have quality issues, sometimes that's a way to get people to perk up a little bit and start listening.

116
00:07:52,160 --> 00:07:54,320
We'll talk about Continuous Integration and CI.

117
00:07:54,320 --> 00:07:59,800
What is that? I'll tell you what that is and how I see that fitting into the accessibility development practice.

118
00:08:01,640 --> 00:08:04,000
We'll talk about what we can automate for accessibility.

119
00:08:04,000 --> 00:08:08,080
Because we can't automate everything. Some of it requires a human to actually test it.

120
00:08:09,520 --> 00:08:15,180
And really, the overarching thing in all of my talks and all my stuff is that we can use technology for good.

121
00:08:15,680 --> 00:08:18,640
And I think we're all probably all on board with that here at this Meetup.

122
00:08:21,340 --> 00:08:24,800
So getting into some of the different types of software testing.

123
00:08:24,800 --> 00:08:27,780
For me, it's all about validating code and covering yourself.

124
00:08:28,140 --> 00:08:32,920
You know covering your butt from getting this code pushed out there without any tests.

125
00:08:33,320 --> 00:08:39,300
So there's functional testing and that includes unit testing, integration testing, system testing,

126
00:08:39,300 --> 00:08:44,800
acceptance testing, and depending on how your company, you know, what level of testing you go to,

127
00:08:45,080 --> 00:08:47,680
these fall under functional testing.

128
00:08:49,000 --> 00:08:51,120
There's non-functional testing, which can include

129
00:08:51,120 --> 00:08:53,220
performance, security, usability,

130
00:08:53,220 --> 00:08:55,940
which does get back closer to accessibility,

131
00:08:55,940 --> 00:08:58,420
and compatibility with lots of platforms.

132
00:09:00,800 --> 00:09:03,340
But the cool step to me is all the accessibility testing

133
00:09:03,340 --> 00:09:09,800
And we can automate things like HTML and ARIA validation to make sure that we using tags correctly.

134
00:09:10,280 --> 00:09:13,180
We didn't make up ARIA roles because I've seen that happen.

135
00:09:13,180 --> 00:09:14,340
Make up attributes.

136
00:09:14,340 --> 00:09:17,480
What do you mean there's a set number of roles?

137
00:09:17,480 --> 00:09:19,480
I thought I could just make those up.

138
00:09:20,000 --> 00:09:22,080
We can automate checking for form labels,

139
00:09:22,080 --> 00:09:26,340
color contrast, accessible names for icon buttons for example.

140
00:09:26,840 --> 00:09:29,740
We can automate testing of focus management.

141
00:09:29,740 --> 00:09:33,080
In applications, specifying a language and  more.

142
00:09:33,540 --> 00:09:37,780
And I have a link to our repository for aXe-core here in my slides

143
00:09:37,780 --> 00:09:40,580
of all of the rules that we actually test against.

144
00:09:41,760 --> 00:09:46,020
And then on the manual testing side, because we can't automate absolutely everything.

145
00:09:46,020 --> 00:09:48,660
We can't really automate focus order.

146
00:09:48,660 --> 00:09:51,540
Maybe in your own app you could, but from our ...

147
00:09:51,940 --> 00:09:54,820
from the aXe-core API level, we can't really determine that.

148
00:09:55,900 --> 00:10:01,140
We can't automate the quality of your text alternatives quite yet.

149
00:10:01,140 --> 00:10:03,140
Maybe with computer vision we can get there,

150
00:10:03,140 --> 00:10:07,840
but right for right now I can't automate whether your alt text is the right  person,

151
00:10:08,920 --> 00:10:11,540
or really if the quality of your alt text is good.

152
00:10:11,540 --> 00:10:18,720
I can tell you if you forgot it, if it's missing, but the quality of those text alternatives is more of a manual process.

153
00:10:19,820 --> 00:10:24,720
Screen reader testing ... we can't programmatically fire up a screen reader, have it do what we want, yet.

154
00:10:24,920 --> 00:10:26,080
I'm hoping that changes.

155
00:10:26,620 --> 00:10:28,420
There's more with keyboard support.

156
00:10:29,040 --> 00:10:32,680
Like if it's not operable at all, we can't really automate.

157
00:10:33,180 --> 00:10:35,980
You know it's like if you don't know what you don't know, we can't really automate that.

158
00:10:36,740 --> 00:10:40,900
Contrast of text over images and gradients is challenging,

159
00:10:40,900 --> 00:10:42,900
and error identification

160
00:10:43,580 --> 00:10:48,780
In my slides, I have a link on the Deque blog about our manual accessibility testing approach

161
00:10:48,780 --> 00:10:52,380
and I use that to kind of give myself a gut check about,

162
00:10:52,380 --> 00:10:54,460
okay well, what can we automate, what can't we.

163
00:10:54,460 --> 00:10:57,900
So if you want to read more about that you can find that in my slides.

164
00:11:00,840 --> 00:11:05,320
But really, technical accessibility like we do it for the people.

165
00:11:05,660 --> 00:11:06,940
It's really about the people.

166
00:11:06,940 --> 00:11:08,940
So as much as I harp on, you know,

167
00:11:08,940 --> 00:11:09,740
development, yay!

168
00:11:09,740 --> 00:11:10,980
Technical stuff, yay!

169
00:11:10,980 --> 00:11:15,000
We do this so that people can actually use these websites.

170
00:11:15,000 --> 00:11:18,480
So we want to keep ... keep that in mind. Obviously I think we all know that.

171
00:11:18,820 --> 00:11:24,700
But visual disabilities, hearing disabilities, motor and cognitive

172
00:11:24,700 --> 00:11:29,800
and I have some more background from the WebAIM site, which I just love all of their resources.

173
00:11:30,020 --> 00:11:31,860
If you want to read more about those...

174
00:11:34,300 --> 00:11:36,020
And it's important to check your work.

175
00:11:36,020 --> 00:11:42,480
WCAG, the Web Content Accessibility Guidelines is a really great set of, exactly that, guidelines,

176
00:11:42,480 --> 00:11:46,500
to help you figure out how to tell if something is actually accessible.

177
00:11:46,500 --> 00:11:49,900
The version 2.1 is currently being worked on.

178
00:11:49,900 --> 00:11:55,580
There's some new success criteria for mobile and low vision folks,

179
00:11:55,580 --> 00:11:59,200
and you can actually provide feedback on those right now.

180
00:11:59,200 --> 00:12:00,460
So that's pretty cool.

181
00:12:00,900 --> 00:12:04,580
And I think when I first got into accessibility, I kind of went Aahhh...

182
00:12:05,320 --> 00:12:09,560
I don't understand this and I went for just making it operable and usable,

183
00:12:09,860 --> 00:12:12,500
using focus management and off screen text and stuff,

184
00:12:12,900 --> 00:12:14,900
and not so much ARIA.

185
00:12:14,900 --> 00:12:18,760
But as I've learned about it more, I see this is a really great resource

186
00:12:18,760 --> 00:12:22,180
for validating whether something is actually accessible.

187
00:12:22,180 --> 00:12:28,460
There's so much expertise has been put into WCAG that it's really valuable to go and reference.

188
00:12:29,820 --> 00:12:32,520
And it's also really important to automated testing.

189
00:12:32,940 --> 00:12:37,220
And I bring this up because in our tooling, you know, a lot of times this is what we're checking against.

190
00:12:40,100 --> 00:12:41,800
So why "geek out" over this?

191
00:12:41,800 --> 00:12:47,020
Well to me, it's all about making the best quality software that works for people,

192
00:12:47,020 --> 00:12:52,740
And my animated gif right now is, I think it's I don't know if that's from The Office...

193
00:12:53,480 --> 00:12:57,100
The guy's just like dancing in the elevator and that's what geeking out is to me.

194
00:12:57,100 --> 00:12:59,880
Is when you're just so excited that this is so cool.

195
00:12:59,880 --> 00:13:02,920
I think software development and accessibility go together

196
00:13:02,920 --> 00:13:07,680
and it produces this amazing result so I geeked out over it I hope you do too.

197
00:13:10,100 --> 00:13:11,320
What can we automate?

198
00:13:12,020 --> 00:13:17,600
We can only catch roughly 30 to 50 percent of accessibility issues, and that depends on your rule set.

199
00:13:18,120 --> 00:13:21,920
So if you're in another country, maybe you're not using WCAG.

200
00:13:22,080 --> 00:13:25,380
It really varies what rule set are we actually testing against.

201
00:13:25,380 --> 00:13:30,380
But it's that smaller set of you know 30 to 50 percent.

202
00:13:31,640 --> 00:13:36,160
And some really interesting work that's happening in this space is the Auto WCAG Community Group,

203
00:13:36,160 --> 00:13:40,860
and the Accessibility Conformance Testing Task Force at the W3C.

204
00:13:41,820 --> 00:13:44,520
They're actually working to standardize some of these automated tests

205
00:13:44,940 --> 00:13:50,240
and my colleague, Wilco Fiers, I work with him on the aXe-Core team, he's in both of these groups

206
00:13:51,200 --> 00:13:56,760
So it's really cool to see us moving towards a standard for this so that every accessibility checker

207
00:13:56,760 --> 00:13:58,760
isn't reinventing the wheel.

208
00:13:59,160 --> 00:14:02,300
So if you want to learn more about the standard side of automated testing,

209
00:14:02,540 --> 00:14:06,160
I would recommend those two groups, Auto-WCAG and the ACT Taskforce.

210
00:14:06,960 --> 00:14:09,960
And you can participate in those groups too, which is really cool.

211
00:14:12,220 --> 00:14:18,180
But it's worth reminding, just to say it yet again, that automated testing is no substitute for manual testing,

212
00:14:18,180 --> 00:14:20,180
and getting real user feedback.

213
00:14:20,960 --> 00:14:26,000
Just because it's technically compliant doesn't mean it's usable and user-friendly.

214
00:14:26,240 --> 00:14:28,600
So we want to make sure that we're doing that.

215
00:14:28,940 --> 00:14:34,220
The automated tests are the great first step so that we're not wasting human effort

216
00:14:34,440 --> 00:14:40,840
with these low-hanging fruit things, like missing alt text and I mean the really basic things that we can automate.

217
00:14:41,100 --> 00:14:45,440
We want to catch those with automated tooling to free up the more complex tasks

218
00:14:45,440 --> 00:14:49,880
for our staff who will be doing manual testing and usability testing.

219
00:14:52,600 --> 00:14:58,040
Okay, so let's dive into some technical talking about what can we actually write in our tests.

220
00:14:59,120 --> 00:15:04,400
So in accessibility unit tests, they're really great for component specific behavior.

221
00:15:04,400 --> 00:15:11,160
So, if you're writing a component that is a menu or a icon button or something that's reusable,

222
00:15:11,400 --> 00:15:16,160
you would want to write some tests for that component that are isolated to just that component,

223
00:15:16,540 --> 00:15:20,120
So it doesn't reach out to the network, it doesn't pull in other components,

224
00:15:20,120 --> 00:15:22,120
it's just this one unit.

225
00:15:23,000 --> 00:15:25,000
And that's general in software development

226
00:15:26,180 --> 00:15:31,560
You'd probably also want to test for anything in that component that handles focus or interactions.

227
00:15:31,560 --> 00:15:38,760
So the kind of the inputs into that component that would make it do certain things like take focus,

228
00:15:39,960 --> 00:15:45,180
change the state of it internally like if it has if it's a custom component and it has some ARIA in it

229
00:15:45,180 --> 00:15:50,000
you would want to validate and attest that those values change when you expect,

230
00:15:50,000 --> 00:15:51,500
so you'd write that into a test.

231
00:15:52,400 --> 00:15:56,800
Maybe you could write a unit test for something like a text alternative if it was an icon button.

232
00:15:57,480 --> 00:16:03,540
And these ... I learned these, this set of tasks as being more unit tests

233
00:16:03,540 --> 00:16:06,260
when I worked on the Angular Material UI framework.

234
00:16:07,020 --> 00:16:11,780
So in those components, you're creating ... creating components that

235
00:16:11,780 --> 00:16:16,180
when the developer uses that component, they might supply alt text

236
00:16:16,180 --> 00:16:19,180
in whatever you've decided is part of your API.

237
00:16:19,180 --> 00:16:25,580
So that way we would want to test that when the developer puts in text for an icon button for example

238
00:16:25,580 --> 00:16:29,820
or a form control or something, we want to make sure that it ends up in the right place

239
00:16:29,820 --> 00:16:32,260
to expose text to a screen reader.

240
00:16:32,660 --> 00:16:37,320
And that's just one example, but you would write a unit test that's sort of limited to just this unit.

241
00:16:39,840 --> 00:16:43,100
Here's an example of a unit test I took this from David Clark.

242
00:16:43,100 --> 00:16:47,680
He has put out some really great ARIA or sorry, React components

243
00:16:48,140 --> 00:16:51,340
and he's got this menu button that you can find on Github.

244
00:16:51,860 --> 00:16:57,820
It's the React ARIA Menu Button and he's got a unit test that tests his focus manager.

245
00:16:58,040 --> 00:17:03,960
So rather than, the way that he set up his test was actually to test that his focus manager had been called,

246
00:17:03,960 --> 00:17:08,360
because that gets triggered by the user's keyboard focus going through a page.

247
00:17:09,320 --> 00:17:13,980
So he sets up this menu by setting the menu to be open to start.

248
00:17:14,640 --> 00:17:20,080
And then what we're asserting is that if that it's open that our focus manager is being called

249
00:17:20,080 --> 00:17:22,220
to send focus into the menu when it opens.

250
00:17:23,080 --> 00:17:25,800
So this is one example of how you might test for focus.

251
00:17:26,280 --> 00:17:31,760
But it sort of depends on this higher level API that he's created called the Focus Manager.

252
00:17:32,320 --> 00:17:34,780
So if you want to learn more about how he set up his component,

253
00:17:34,780 --> 00:17:37,420
I would definitely recommend checking out his repository.

254
00:17:40,300 --> 00:17:42,400
On the flip side, so let's unit test.

255
00:17:43,220 --> 00:17:46,740
You might consider writing integration or end-to-end tests as well.

256
00:17:47,640 --> 00:17:49,780
They're really great for real-world browser testing.

257
00:17:49,780 --> 00:17:54,460
So in the unit tests we're often running those in a headless browser like Phantom.js

258
00:17:54,460 --> 00:17:57,440
or Karma Chrome Launcher or something like that.

259
00:17:57,680 --> 00:18:02,160
And what that does is ... in a headless environment,

260
00:18:02,500 --> 00:18:06,840
we aren't actually opening up a browser, we're running it on the command line, kind of in memory

261
00:18:07,060 --> 00:18:15,240
and that works pretty well. But if you're really getting into things like the actual focus of an element,

262
00:18:15,240 --> 00:18:18,200
you might run into some edge cases with your tooling.

263
00:18:18,640 --> 00:18:22,780
And so we recommend that if you're having issues with your unit tests,

264
00:18:22,780 --> 00:18:25,680
just write an integration test with Selenium Webdriver.

265
00:18:26,780 --> 00:18:32,080
And what that will do is open a real browser instance on your machine, you're driving it with code.

266
00:18:32,480 --> 00:18:37,080
So we'll open up a real browser and you can specify which one. I'll show you an example in a minute.

267
00:18:37,400 --> 00:18:41,020
But then you're actually testing it in a real browser like a user would.

268
00:18:41,920 --> 00:18:43,100
That's super valuable.

269
00:18:43,100 --> 00:18:48,400
It's a little bit slower so that's why some people don't like Selenium, but it's really reliable.

270
00:18:48,940 --> 00:18:52,360
So I would highly recommend it for real-world browser testing.

271
00:18:53,760 --> 00:18:57,500
These types of tests are also really great for document or page level rules.

272
00:18:57,500 --> 00:19:03,020
So if you're testing the title of the page or the language of the document.

273
00:19:03,020 --> 00:19:09,640
So that's not really a component unit test, that's probably more of an integration test for this overall page.

274
00:19:10,740 --> 00:19:16,360
And furthermore, if you had multiple widgets like maybe you have focus management going between widgets,

275
00:19:16,360 --> 00:19:20,040
you would want to write an integration test where they're both on the same page.

276
00:19:20,800 --> 00:19:22,800
So that's a case where ...

277
00:19:23,100 --> 00:19:25,240
you would be reaching outside of your single units.

278
00:19:25,240 --> 00:19:29,920
So to test things together you would want to have an integration test.

279
00:19:31,440 --> 00:19:36,480
We can use this environment in the real browser to test color contrast a lot more reliably.

280
00:19:36,480 --> 00:19:41,400
We need CSS to be there, we need the browser layout to happen,

281
00:19:41,720 --> 00:19:46,260
and we need real DOM APIs to actually test for color.

282
00:19:47,260 --> 00:19:52,480
And then lastly, I've seen integration or end-to-end tests with Webdriver be used, because

283
00:19:53,180 --> 00:19:56,160
the site might be written with a JavaScript framework like Angular,

284
00:19:56,860 --> 00:20:03,320
and that framework may not have all the tools you need to write unit tests for keyboard support for example.

285
00:20:03,980 --> 00:20:07,880
And my example, I grabbed from the Angular Material 2 Dialogue.

286
00:20:08,520 --> 00:20:10,960
They ... when Angular 2 came out,

287
00:20:11,320 --> 00:20:15,040
they hadn't set up all of the necessary tooling for unit tests.

288
00:20:15,980 --> 00:20:19,200
So they ended up writing their accessibility tests in Protractor,

289
00:20:19,200 --> 00:20:23,040
which is the Angular layer over Selenium webdriver.

290
00:20:23,600 --> 00:20:29,120
So this dialog example is on Github in the Angular Material 2 Library.

291
00:20:29,620 --> 00:20:31,140
It's written in Typescript

292
00:20:32,460 --> 00:20:37,160
and so this is an example of just their general tests for their dialog.

293
00:20:37,380 --> 00:20:41,220
They've put accessibility tests in with everything else, which is how it should be.

294
00:20:41,560 --> 00:20:44,040
When we're testing for our code we should just ...

295
00:20:44,800 --> 00:20:47,140
... add the accessibility stuff to our regular tests.

296
00:20:47,140 --> 00:20:49,140
It shouldn't be this add-on special thing.

297
00:20:49,440 --> 00:20:53,560
Just write the tests in there, because it's a core feature to be able to use the keyboard.

298
00:20:54,300 --> 00:20:55,840
So this dialog ...

299
00:20:56,260 --> 00:21:00,500
... they pull in a number of resources to actually be able to test this code.

300
00:21:01,360 --> 00:21:05,600
And then they go and get this dialog demo, because it's actually open in a browser.

301
00:21:06,300 --> 00:21:09,660
They assert in one test that it ... the dialog should open.

302
00:21:10,540 --> 00:21:14,120
They assert that you should be able to close it by clicking on the backdrop.

303
00:21:14,540 --> 00:21:16,260
So these are features of this dialog.

304
00:21:17,160 --> 00:21:19,940
They have it and, this I would consider an accessibility test.

305
00:21:19,940 --> 00:21:22,240
it should close by pressing the Escape key.

306
00:21:23,060 --> 00:21:27,300
So you can see like if you're testing the clicking, you should be testing the keyboard at the same time.

307
00:21:27,860 --> 00:21:32,500
This is a great example of how accessibility tests just go right in with all of the other tests.

308
00:21:34,180 --> 00:21:37,160
They have a test that it should close by pressing the Escape key

309
00:21:37,160 --> 00:21:39,540
when the first tab-able element has lost focus

310
00:21:40,120 --> 00:21:43,020
So if you end up ...

311
00:21:43,640 --> 00:21:48,820
I know, using a skip link or somehow this menu loses focus they don't want it to get stuck open.

312
00:21:49,220 --> 00:21:51,160
I guess it's a dialog not a menu.

313
00:21:51,160 --> 00:21:55,600
But they want to make sure that it doesn't just get stuck open if your focus is somewhere else.

314
00:21:55,600 --> 00:21:57,600
So they have a test for that case.

315
00:21:58,320 --> 00:22:02,880
And there's all different scenarios depending on how your component is supposed to function,

316
00:22:03,580 --> 00:22:07,600
you can both document that in your tests, and prevent regressions,

317
00:22:07,600 --> 00:22:12,380
so if someone breaks it, unknowingly, they've broken the tests as well.

318
00:22:12,380 --> 00:22:15,360
So it's really important to have this test coverage.

319
00:22:17,900 --> 00:22:21,500
So to sort of illustrate the value of tests,

320
00:22:21,500 --> 00:22:24,140
I have a couple of animated gifts from Twitter.

321
00:22:24,440 --> 00:22:27,480
One from Sarah Dresner saying but unit tests are passing.

322
00:22:29,440 --> 00:22:31,080
[Laughter]

323
00:22:31,080 --> 00:22:35,780
So she's holding an umbrella or whoever's gif this is, and they opened the umbrella,

324
00:22:35,780 --> 00:22:38,840
and the top just goes shooting off of the handle.

325
00:22:39,460 --> 00:22:43,160
Because they probably tested each part of it but they didn't test it all together.

326
00:22:44,000 --> 00:22:48,080
So it's a good metaphor for your unit tests, like you might test every little part,

327
00:22:48,560 --> 00:22:51,680
but if you don't test it and integrated together,

328
00:22:52,160 --> 00:22:54,160
your umbrella might fall apart.

329
00:22:55,920 --> 00:22:57,960
Another example from Twitter.

330
00:22:57,960 --> 00:23:01,520
It's kind of been going around lately with these funny animated gifs were test.

331
00:23:01,520 --> 00:23:07,040
So this one from Nick Vasily says 2 unit tests, 0 integration tests.

332
00:23:08,820 --> 00:23:15,740
So he's drying his hands in the restroom, he goes to put his paper towel in the garbage can,

333
00:23:15,740 --> 00:23:20,180
and there's a fan right over it and they just ... the towels blow right out of the garbage can.

334
00:23:21,060 --> 00:23:26,800
Because, again, they probably didn't test things together, like when they assembled this bathroom,

335
00:23:26,800 --> 00:23:28,800
there was a fan over the garbage can.

336
00:23:29,280 --> 00:23:34,540
So this is a really good way to think about testing and why you actually need to do both kinds of tests

337
00:23:36,260 --> 00:23:42,300
So you really want a combination of tests to catch a variety of bugs, both unit tests and integration tests.

338
00:23:42,740 --> 00:23:48,480
Unit tests are really nice because they're fast, they give you test coverage for a discrete unit.

339
00:23:48,480 --> 00:23:54,340
So if you say you package up your menu component and let other people use it,

340
00:23:54,460 --> 00:23:56,760
your unit tests would be really essential for that.

341
00:23:57,420 --> 00:24:01,840
But if you're using it in your real project you need to make sure that everything's working together.

342
00:24:02,680 --> 00:24:05,800
So it's important to have a variety of these types of tests.

343
00:24:08,380 --> 00:24:14,040
So those are tests for the features on your website or your application, that are specific to you,

344
00:24:14,360 --> 00:24:17,400
and how your design works, how your website is set up.

345
00:24:17,640 --> 00:24:21,400
So you want to have custom tests for your application.

346
00:24:22,060 --> 00:24:28,820
That way, you know, if it is documenting how that particular feature or page is supposed to work,

347
00:24:28,940 --> 00:24:34,160
and it provides a contract for your team members so that things don't just start breaking.

348
00:24:34,860 --> 00:24:39,000
But there's some tests that would really benefit from pulling in an API.

349
00:24:39,000 --> 00:24:42,780
An accessibility Testing API, and there are multiple of them.

350
00:24:42,780 --> 00:24:45,140
I work on one which is aXe-Core,

351
00:24:45,480 --> 00:24:50,600
but API's like this are really valuable because you can save yourself from writing some of this boilerplate

352
00:24:50,600 --> 00:24:54,680
that is, gets you in the weeds, that you frankly don't have time for,

353
00:24:54,680 --> 00:24:58,720
if you're not specializing in that you just need to get your tests in and get up and running.

354
00:24:58,720 --> 00:25:03,200
So an API can help you with accessible name calculation,

355
00:25:03,800 --> 00:25:11,400
so you know, icon buttons, form labels, things like that where the way that that label is exposed and calculated

356
00:25:11,900 --> 00:25:13,680
is pretty needy gritty to be honest.

357
00:25:13,680 --> 00:25:18,420
Like though the way that those rules are applied takes a lot of insider knowledge.

358
00:25:18,680 --> 00:25:22,920
And so it would be nice to just not have to worry about that and have an API test that for you.

359
00:25:23,300 --> 00:25:25,420
So you're not having to write that test yourself.

360
00:25:26,460 --> 00:25:29,160
It could help you with incorrect ARIA usage.

361
00:25:29,160 --> 00:25:35,640
Like say you're using one ARIA widget role and you don't have all of the other required child roles.

362
00:25:35,640 --> 00:25:42,060
Or maybe you spell and attribute wrong or something like that, it's nice to have an API test that for you.

363
00:25:42,060 --> 00:25:46,200
And then the API is keeping up to date with any changes with ARIA spec,

364
00:25:46,940 --> 00:25:49,600
like those kind of insider things of like well ...

365
00:25:49,840 --> 00:25:53,840
we filed a bug with Apple four years ago and they've never fixed it so ...

366
00:25:54,560 --> 00:25:56,380
they having the API ...

367
00:25:56,760 --> 00:26:01,380
test against the real world scenarios is also really useful, so you don't have to keep track of all of that.

368
00:26:02,700 --> 00:26:06,220
It can help with color contrast, which is really expensive calculation.

369
00:26:06,220 --> 00:26:12,480
It takes a lot of checking styles, computed styles in the browser,

370
00:26:12,480 --> 00:26:15,420
and so it's nice to not have to worry about that because it's pretty complicated.

371
00:26:16,540 --> 00:26:20,240
Testing tables, whether they're data tables or layout tables.

372
00:26:20,840 --> 00:26:22,840
It's nice to not have to write that boilerplate.

373
00:26:23,580 --> 00:26:25,580
Things like viewport and zooming problems.

374
00:26:25,840 --> 00:26:31,580
So that again you're letting an API handle some of this more complicated stuff for you.

375
00:26:31,600 --> 00:26:35,480
And you can focus on the tests that are specific to your application.

376
00:26:38,540 --> 00:26:41,320
So that my preferred API, because I'm obviously biased,

377
00:26:41,320 --> 00:26:44,560
I went to work on aXe because I was using it everyday anyway,

378
00:26:45,180 --> 00:26:48,000
and it's ended up being a really enlightening experience,

379
00:26:48,000 --> 00:26:51,100
learning from people who know accessibility inside and out.

380
00:26:51,100 --> 00:26:53,340
And that is packed into aXe-core.

381
00:26:53,800 --> 00:26:56,780
So you can find aXe-core on NPM,

382
00:26:57,640 --> 00:26:59,020
and you can get it on Github.

383
00:26:59,020 --> 00:27:02,800
We just released the newest version, 2.2.0 this last week,

384
00:27:03,080 --> 00:27:06,740
and we love getting feedback on Github; if you find an issue with it,

385
00:27:07,240 --> 00:27:13,360
if you want to submit a pull request, we love getting feedback from people and out in the world.

386
00:27:15,120 --> 00:27:21,560
So aXe-core, its github.com/dequelabs/axe-core

387
00:27:21,560 --> 00:27:22,880
and it's a x e.

388
00:27:23,180 --> 00:27:25,980
So aXe-core is an open source JavaScript library.

389
00:27:26,820 --> 00:27:30,020
It doesn't require a network and it doesn't require an API key.

390
00:27:30,400 --> 00:27:35,000
And so you could be on an airplane with no internet and use this to test stuff locally on your machine,

391
00:27:35,000 --> 00:27:36,400
which i think is really cool.

392
00:27:37,280 --> 00:27:40,340
You can configure it completely. You can turn rules on and off.

393
00:27:40,960 --> 00:27:44,040
Rules are made up of multiple checks, that are reusable.

394
00:27:44,040 --> 00:27:46,680
So you could configure down to the check level if you wanted.

395
00:27:47,720 --> 00:27:50,200
We really aim for no false positives.

396
00:27:51,100 --> 00:27:54,300
That means that we're only trying to flag things that are legitimate issues,

397
00:27:54,300 --> 00:27:56,520
because if you have so many issues that you're like,

398
00:27:56,520 --> 00:27:58,520
Oh that's not a real issue,

399
00:27:58,520 --> 00:28:00,520
you're going to start to ignore it after a while.

400
00:28:01,100 --> 00:28:03,300
And we really try to keep up on that.

401
00:28:03,300 --> 00:28:08,180
It's hard to anticipate absolutely every use case so that's why we're really open on Github,

402
00:28:08,180 --> 00:28:11,400
and we love getting issues if you find a false positive,

403
00:28:11,760 --> 00:28:13,200
let us know, so we can fix it.

404
00:28:13,580 --> 00:28:19,620
And that's one of the benefits of being open source, is that we can all pull this effort together.

405
00:28:19,620 --> 00:28:22,260
so that we're trying to make it as solid as we can.

406
00:28:22,920 --> 00:28:27,320
And that in turn goes back to that Auto WCAG and ACT Taskforce stuff.

407
00:28:27,320 --> 00:28:29,020
It's not just aXe-core.

408
00:28:29,360 --> 00:28:31,200
This is helping web standards as well.

409
00:28:31,560 --> 00:28:35,120
So I really appreciate that movement to make it standards-based.

410
00:28:38,220 --> 00:28:41,240
So if we look at a unit test with aXe-core,

411
00:28:41,240 --> 00:28:44,920
the idea of it, when you pull in this API is that it will ...

412
00:28:44,920 --> 00:28:48,440
you run the API and then it returns a result object to you,

413
00:28:48,440 --> 00:28:50,760
and you expect that it has no violations.

414
00:28:51,420 --> 00:28:54,140
So aXe-core ... and we'll look at what it returns in a second,

415
00:28:54,540 --> 00:28:59,500
But it returns a JSON object that has an array of passes,

416
00:28:59,500 --> 00:29:02,340
An array of violations and an array of ...

417
00:29:02,340 --> 00:29:04,800
I think there's incomplete and inapplicable .

418
00:29:05,040 --> 00:29:10,720
But the passes in the violations are really the sort of pass/fail for your test that you want to key into.

419
00:29:12,100 --> 00:29:14,320
So in my little unit test example here,

420
00:29:14,320 --> 00:29:16,440
I pull in aXe-core using require.

421
00:29:16,440 --> 00:29:19,020
You could use import if you're using ES6.

422
00:29:19,020 --> 00:29:22,900
There's multiple ways to pull this in once you've installed it from NPM.

423
00:29:24,400 --> 00:29:28,480
I'm going to describe this custom component and then say with Jasmine,

424
00:29:28,480 --> 00:29:31,200
it should have no accessibility violations.

425
00:29:31,820 --> 00:29:33,880
You pass the test a callback function.

426
00:29:33,880 --> 00:29:39,460
We include this asynchronous done argument, so that way, when we're done with aXe-core,

427
00:29:39,460 --> 00:29:41,680
we can tell Jasmine that our test is done.

428
00:29:41,680 --> 00:29:44,160
Otherwise, it'll just timeout and scream at you.

429
00:29:45,360 --> 00:29:50,060
Inside of our test, you can setup any number of options. I'm just passing an empty object.

430
00:29:51,000 --> 00:29:53,020
But then we can say axe.run,

431
00:29:53,020 --> 00:29:58,340
path of either a selector or an element reference. It's pretty flexible in what you can pass to it,

432
00:29:58,340 --> 00:29:59,960
It defaults to the document.

433
00:30:00,960 --> 00:30:02,960
We pass that options or an empty object,

434
00:30:03,340 --> 00:30:04,740
and then a callback function.

435
00:30:05,140 --> 00:30:08,140
And axe.run, which is one of our newer API methods,

436
00:30:08,380 --> 00:30:11,120
it added this ability to bubble up errors.

437
00:30:11,820 --> 00:30:14,660
Which was different. We had to add that support in there.

438
00:30:14,660 --> 00:30:16,660
So if aXe encounters a problem ...

439
00:30:17,280 --> 00:30:22,060
it would kind of just fail silently before, with our other API method of aXe.a11ycheck.

440
00:30:22,640 --> 00:30:27,500
So this callback function, you pass it two parameters; an error and the results.

441
00:30:28,100 --> 00:30:32,500
And if there's an error, it'll pass that back to you. Otherwise you just get this results.

442
00:30:33,520 --> 00:30:38,580
So then in this callback function, we can expect result.violations.length to be zero.

443
00:30:39,480 --> 00:30:41,200
And that's really all you have to do.

444
00:30:41,200 --> 00:30:43,820
Because you're expecting that it's going to return something to you

445
00:30:43,820 --> 00:30:45,420
and if it returns violations,

446
00:30:45,760 --> 00:30:47,160
[buzzer sound]

447
00:30:47,160 --> 00:30:50,700
and you have to go fix them and you can kind of iterate on that until it passes.

448
00:30:51,120 --> 00:30:53,300
And then you can call this done callback,

449
00:30:53,720 --> 00:30:57,960
and that's how you could expect accessibility violations with this API.

450
00:31:01,660 --> 00:31:05,640
So another example of this, an integration test with another tool.

451
00:31:05,640 --> 00:31:08,560
So aXe-core is just the JavaScript engine

452
00:31:08,560 --> 00:31:13,820
that powers both our browser extensions and the JavaScript library itself.

453
00:31:14,420 --> 00:31:16,720
We have another tool called axe-webdriverjs,

454
00:31:16,720 --> 00:31:20,300
that instead of using the the headless phantom browser,

455
00:31:20,980 --> 00:31:24,680
we're using Selenium webdriver to programmatically open a real browser instance

456
00:31:24,680 --> 00:31:26,680
and I'll show you how that works in a minute.

457
00:31:27,400 --> 00:31:33,080
But in this test example, we pull in AxeBuilder by saying require axe-webdriverjs,

458
00:31:33,780 --> 00:31:38,240
We pull in Selenium Webdriver and cache that in a variable called WebDriver.

459
00:31:38,860 --> 00:31:43,320
And then we set it up by saying var driver equals webdriver.builder,

460
00:31:43,780 --> 00:31:45,780
and then we can specify which browser.

461
00:31:46,080 --> 00:31:51,200
I'm specifying Chrome ... you could say Firefox, Safari depending on if you're on a Mac,

462
00:31:51,200 --> 00:31:53,200
or Edge if you're on a Windows machine.

463
00:31:53,500 --> 00:31:55,740
And that depends on having the ...

464
00:31:56,080 --> 00:32:00,380
there's a driver that you have to download and put it somewhere on your path on your machine.

465
00:32:01,040 --> 00:32:04,320
And if you have questions about that part let me know.

466
00:32:04,620 --> 00:32:09,280
I think we document it on the axe-webdriverjs repository on Github.

467
00:32:10,600 --> 00:32:14,260
It can be a little tricky, but once you know like which folders are on your path,

468
00:32:14,260 --> 00:32:16,920
you can just go put the drivers there when you download them.

469
00:32:17,260 --> 00:32:19,680
I will warn you that Chrome is the most reliable.

470
00:32:20,460 --> 00:32:23,040
Firefox has been really unpredictable lately.

471
00:32:24,100 --> 00:32:25,380
So once we've set up webdriver,

472
00:32:25,380 --> 00:32:31,920
we can say driver.get and point it at a URL either a local host URL running on our own machine,

473
00:32:32,200 --> 00:32:35,740
or it could be out on the internet somewhere on a fully qualified URL

474
00:32:36,520 --> 00:32:41,160
that returns a promise, so we can say that this driver.get and then

475
00:32:41,640 --> 00:32:44,800
we pass a callback function, and we can call axe-builder now.

476
00:32:45,160 --> 00:32:47,480
So we've let Selenium go out and get this resource,

477
00:32:47,780 --> 00:32:50,780
it returns the promise, now we can run axe-builder on it.

478
00:32:51,520 --> 00:32:54,080
So axe-builder, we pass it the driver variable

479
00:32:54,080 --> 00:32:56,080
and say axe-builder dot analyze,

480
00:32:56,760 --> 00:32:58,000
and in this callback function,

481
00:32:58,000 --> 00:33:01,160
it's really similar to our last test that we saw.

482
00:33:01,160 --> 00:33:04,380
it passes back the exact same results object.

483
00:33:05,040 --> 00:33:10,060
So once we have that results object, we can expect results dot violations dot lengths to be 0.

484
00:33:10,780 --> 00:33:12,800
And you can name that parameter whatever you want.

485
00:33:12,800 --> 00:33:16,600
It was result in the last test its results plural in this test.

486
00:33:16,600 --> 00:33:19,320
It's whatever you call it, really.

487
00:33:19,320 --> 00:33:22,460
But the structure that it passes back is the same.

488
00:33:24,680 --> 00:33:27,480
So let's run this test locally. I'm going to run the webdriver version.

489
00:33:27,920 --> 00:33:33,460
So I have a command prompt in my browser which is not available on my slides,

490
00:33:33,460 --> 00:33:35,660
because that would be a big security hole.

491
00:33:35,920 --> 00:33:39,320
But locally I have it running in my slides, so I can just say

492
00:33:39,320 --> 00:33:41,600
npm space test

493
00:33:42,480 --> 00:33:45,380
npm test running in this directory,

494
00:33:45,820 --> 00:33:49,160
you can see it exited out of my slides and opened a real browser.

495
00:33:49,560 --> 00:33:54,540
I'm running this Mars commuter web site that we use, it's atrocious for accessibility.

496
00:33:55,240 --> 00:33:56,840
It's really great test example.

497
00:33:57,580 --> 00:34:02,540
So it opened that browser instance, I went back to my slides and in the command prompt now

498
00:34:02,540 --> 00:34:06,760
we can see that it expected there to be zero violations, but there were ten.

499
00:34:07,820 --> 00:34:09,140
So that's a problem.

500
00:34:09,300 --> 00:34:11,540
But that's what you would really ... that's how it really work.

501
00:34:11,540 --> 00:34:14,700
if you were running this for the first time as you would get these violations,

502
00:34:15,060 --> 00:34:17,060
and then go and figure out what failed.

503
00:34:18,720 --> 00:34:22,340
So the output that axe-core gives you is a JSON object.

504
00:34:22,620 --> 00:34:28,000
And in my test, if I logged out results at violations

505
00:34:28,000 --> 00:34:30,000
I can look at just what failed.

506
00:34:30,460 --> 00:34:33,880
So just the violations and it gives us back this structure.

507
00:34:34,260 --> 00:34:36,960
So I'm going to do a quick search here for a description,

508
00:34:37,660 --> 00:34:39,940
and there's quite a few of them.

509
00:34:40,980 --> 00:34:43,240
Things like buttons needing discernible text,

510
00:34:43,960 --> 00:34:48,680
and it gives you a help URL, so you could go and learn more about how to fix it if you needed remediation help.

511
00:34:49,340 --> 00:34:53,040
It'll tell you which elements were the problem so you can go and find those.

512
00:34:53,400 --> 00:34:58,040
And these are ... this is the same details that we use for our Chrome and Firefox extensions.

513
00:34:58,040 --> 00:35:00,040
But it's programmatic, it's an API.

514
00:35:01,560 --> 00:35:04,520
The Mars commuter site has issues with color contrast,

515
00:35:04,520 --> 00:35:07,780
and it'll tell you what the contrast ratio was.

516
00:35:08,060 --> 00:35:11,980
So 4.49 is so close to passing.

517
00:35:12,420 --> 00:35:14,880
Four point five to one is what it should be.

518
00:35:14,880 --> 00:35:18,340
But four point four nine is not passing, technically.

519
00:35:19,460 --> 00:35:22,460
So you can just bump that color up a little bit or maybe the font size.

520
00:35:22,660 --> 00:35:26,560
We do take font size and boldness into account when we calculate that.

521
00:35:27,800 --> 00:35:31,600
That site had issues with ID attributes not being unique,

522
00:35:32,420 --> 00:35:34,540
iframes not having a title attribute,

523
00:35:35,800 --> 00:35:39,580
the HTML document element not having a Lang attribute,

524
00:35:40,860 --> 00:35:43,160
images missing alt text and so on.

525
00:35:43,160 --> 00:35:47,240
So it'll give you all of these tips of how to fix these really easy things that

526
00:35:47,760 --> 00:35:51,520
hopefully we can just knock out and then focus on the more complex issues.

527
00:35:54,780 --> 00:36:00,060
And I should add, if you want to see everything that's part of this aXe API on Github,

528
00:36:00,060 --> 00:36:04,520
we have our API documentation and that's dequelabs slash axecore.

529
00:36:07,480 --> 00:36:10,300
So to talk about continuous integration,

530
00:36:10,900 --> 00:36:14,020
we had to cover software testing, because otherwise what would you be testing against.

531
00:36:14,520 --> 00:36:17,580
So I like to talk about that first, just so that we know

532
00:36:17,760 --> 00:36:21,000
this really important part of continuous integration is ...

533
00:36:21,680 --> 00:36:24,800
before you can actually do continuous integration you need some into test.

534
00:36:25,700 --> 00:36:30,440
But this idea is that, you have code and it has tests,

535
00:36:30,840 --> 00:36:35,960
and if you're going to push that code out to another server, you want it to run your tests automatically.

536
00:36:36,540 --> 00:36:40,280
So that if there was something about that environment that you didn't expect and your tests don't pass,

537
00:36:40,880 --> 00:36:42,880
you could have it automatically tell you.

538
00:36:43,080 --> 00:36:47,300
You could have it light up somebody's desk with a red light and be like "Ha, Ha, they broke the build."

539
00:36:48,080 --> 00:36:50,500
You could do that with continuous integration.

540
00:36:51,140 --> 00:36:54,180
You could have a drone fly over to them and squirt them with a water gun ... I don't know.

541
00:36:54,220 --> 00:36:55,260
[laughter]

542
00:36:55,260 --> 00:37:00,860
So continuous integration is this idea of pushing code out to a server, having it automatically run your tests,

543
00:37:00,860 --> 00:37:02,860
and then report back to you the status.

544
00:37:03,540 --> 00:37:08,440
And there's a great article from Carnegie Mellon on continuous integration and DevOps.

545
00:37:09,820 --> 00:37:13,600
There's tools that I'm going to tell you about that have made this really easy for us as front-end developers,

546
00:37:13,980 --> 00:37:16,160
and people who aren't DevOps people,

547
00:37:16,280 --> 00:37:19,360
to learn about how we can actually make this happen.

548
00:37:19,360 --> 00:37:23,680
how can we run these tests automatically, without having to become DevOps experts.

549
00:37:25,160 --> 00:37:26,740
So there's quite a few solutions for this.

550
00:37:26,740 --> 00:37:31,380
There's circle CI and Travis CI and then there's Jenkins.

551
00:37:31,380 --> 00:37:35,620
And there's probably more, but these are the really popular ones, at least from the front-end land.

552
00:37:36,220 --> 00:37:38,600
I'm going to focus on circle and Travis,

553
00:37:39,260 --> 00:37:42,320
because honestly, Jenkins is like a can of worms

554
00:37:42,960 --> 00:37:49,000
and has been really challenging, especially if you have multiple code repositories that you need to build together.

555
00:37:49,000 --> 00:37:51,000
we just found having a heck of a time with Jenkins.

556
00:37:51,480 --> 00:37:54,460
So if you're a Jenkins master, props to you.

557
00:37:54,460 --> 00:37:55,560
[laughter]

558
00:37:55,560 --> 00:37:59,900
We're going to focus on the hosted ones, because that's really the difference between circle and Travis,

559
00:37:59,900 --> 00:38:01,900
they are hosted solutions that are free.

560
00:38:02,640 --> 00:38:05,000
Jenkins is something that you can easily set up.

561
00:38:05,340 --> 00:38:09,140
There's great tutorials on setting up Jenkins and that part was easy.

562
00:38:09,520 --> 00:38:14,240
But actually getting it to trigger at the right time I found was really difficult.

563
00:38:16,420 --> 00:38:21,240
So here's a real-world scenario of how continuous integration might be beneficial to you

564
00:38:21,620 --> 00:38:26,080
if you have a Github repository like we do for axe-core and axe-webdriver.js,

565
00:38:26,780 --> 00:38:28,340
when someone contributes code,

566
00:38:28,840 --> 00:38:34,000
Travis ... I think we've since moved a circle but when someone commits the pull request,

567
00:38:34,000 --> 00:38:36,000
our tests automatically run.

568
00:38:36,000 --> 00:38:38,800
And so if their code that they're submitting breaks our tests,

569
00:38:39,160 --> 00:38:40,400
they know, we know,

570
00:38:40,760 --> 00:38:46,260
we don't submit their ... we don't push their code into our, you know, bigger repository until the tests are passing.

571
00:38:47,200 --> 00:38:50,880
That's how you can protect yourself from breaking everything all the time.

572
00:38:51,260 --> 00:38:57,020
And so, this is a really simple example that I find this is easier to wrap my head around,

573
00:38:57,020 --> 00:38:59,880
you know, you're participating in open source code,

574
00:39:00,060 --> 00:39:02,060
you want to make sure that their tests are passing,

575
00:39:02,060 --> 00:39:06,700
it's the same process if you were deploying a new website out to a server somewhere.

576
00:39:07,580 --> 00:39:12,120
But this is where you might find it in the real world all the time, is on Github.

577
00:39:13,180 --> 00:39:16,680
So we can have our test run if we commit a new branch,

578
00:39:17,040 --> 00:39:19,460
if someone submits a pull request,

579
00:39:20,000 --> 00:39:23,040
we can run it in all kinds of different scenarios.

580
00:39:23,940 --> 00:39:29,140
Some other tools we have here on Github, we have an automatic contributor License Agreement.

581
00:39:29,960 --> 00:39:36,800
If somebody has signed our document to say they're ok with submitting code a repository,

582
00:39:36,800 --> 00:39:44,960
and then we have this sneak security check - so we can check for any vulnerabilities in any dependencies and things like that.

583
00:39:44,960 --> 00:39:49,440
So there's all kinds of tools and integrations that you could put into a Github repo,

584
00:39:49,800 --> 00:39:52,780
and this CI fits in really nicely.

585
00:39:55,360 --> 00:39:58,080
So hosted continuous integration in a nutshell.

586
00:39:58,400 --> 00:40:02,100
You would write your code and write some tests, because you need the test to begin with.

587
00:40:02,100 --> 00:40:05,340
We covered some really great ways to write tests for accessibility.

588
00:40:06,200 --> 00:40:10,800
You have to add the integration to a Git repo, so either on Github or on fitbucket,

589
00:40:11,240 --> 00:40:15,800
and these are the processes that, at least from the front-end, this is how it normally works.

590
00:40:16,620 --> 00:40:21,020
Then you go over to that ... either your if your using circle or Travis,

591
00:40:21,020 --> 00:40:23,220
and I'll show you what this looks like in a minute.

592
00:40:23,700 --> 00:40:28,860
They actually have to go off to that site and enable builds for your project, so it's sort of a two-step process.

593
00:40:29,400 --> 00:40:32,620
And then you either push code or you can manually trigger build

594
00:40:32,620 --> 00:40:37,300
and that's how you can get this ... these tests to run on the hosted CI services.

595
00:40:39,060 --> 00:40:42,620
They ... CI, both circle and Travis have default settings.

596
00:40:43,240 --> 00:40:48,880
They have certain languages already running, like node or PHP and things like that.

597
00:40:49,340 --> 00:40:53,320
But if you need a specific version that's newer than what they provide to you ...

598
00:40:53,920 --> 00:40:57,120
we use a lot of newer JavaScript features in our tests,

599
00:40:57,580 --> 00:41:02,920
and so the default version of node.js is too old for ours, so we have to override it.

600
00:41:03,420 --> 00:41:05,700
So I have a circle dot yml file

601
00:41:05,700 --> 00:41:09,880
is how you would override circles default node install.

602
00:41:10,620 --> 00:41:15,020
And then on their documentation, that you can find on circle CI  dot com,

603
00:41:15,640 --> 00:41:18,660
their configuration has all these different things that you can do.

604
00:41:18,920 --> 00:41:22,880
You could have it deploy your code to production after your test pass if you want.

605
00:41:23,180 --> 00:41:24,520
You could pick which branch ...

606
00:41:25,100 --> 00:41:28,460
There's all kinds of different scenarios that you could use in CI,

607
00:41:28,460 --> 00:41:31,040
but from the most basic standpoint,

608
00:41:31,880 --> 00:41:34,780
all we really needed was to upgrade the node version.

609
00:41:36,600 --> 00:41:38,000
Travis is really similar.

610
00:41:38,000 --> 00:41:40,420
Instead of circle dot yml, it's Travis dot yml.

611
00:41:40,660 --> 00:41:45,300
And their API is slightly different, so I spent a lot of time on these docs

612
00:41:45,560 --> 00:41:51,860
figuring out how to craft these files and takes a couple tries. I fail a lot but it works eventually.

613
00:41:52,680 --> 00:41:56,260
So this is a really similar document that shows how to upgrade Node,

614
00:41:56,260 --> 00:42:00,000
and if you were going to deploy your code, how you might do that.

615
00:42:02,940 --> 00:42:05,220
So how to CI help for accessibility?

616
00:42:05,440 --> 00:42:09,080
It really helps you test are more platforms that you don't have physically in front of you.

617
00:42:09,340 --> 00:42:11,920
If I'm a Mac user and I want to run it against ...

618
00:42:12,880 --> 00:42:18,840
Edge or some Linux version or maybe mobile devices using soft labs or something like that,

619
00:42:19,140 --> 00:42:21,860
it really expands your reach to these other platforms

620
00:42:22,100 --> 00:42:24,920
that can be really useful if you're writing accessibility tests.

621
00:42:26,340 --> 00:42:27,740
You can prevent regressions.

622
00:42:28,020 --> 00:42:32,360
So if you have accessibility test coverage and a teammate breaks it,

623
00:42:32,360 --> 00:42:33,580
and doesn't realize it,

624
00:42:34,140 --> 00:42:38,340
you can prevent that code from getting pushed out to the world because they broke the build.

625
00:42:38,480 --> 00:42:39,880
So that's really valuable.

626
00:42:40,200 --> 00:42:42,020
Because not everyone is an expert

627
00:42:42,740 --> 00:42:46,480
and so if you have some test coverage that people on your team have written,

628
00:42:46,480 --> 00:42:48,240
and then you have other team members come in,

629
00:42:48,480 --> 00:42:53,400
it really helps document how that's supposed to work in your actual tests.

630
00:42:54,160 --> 00:42:58,000
And then from a really basic level, it encourages test coverage at all,

631
00:42:58,000 --> 00:43:02,200
because you can kind of gamify it and say we want these things to turn green,

632
00:43:02,200 --> 00:43:07,140
we wanted to pass and we want to protect ourselves from pushing broken code for accessibility.

633
00:43:09,720 --> 00:43:15,280
So here's an example ... I'll walk you through how to set up CI testing for a Github repo that I have.

634
00:43:15,280 --> 00:43:17,280
It's called axe-jasmine-unit.

635
00:43:17,600 --> 00:43:21,300
It's just a little demo of how to use axe-core and Jasmine together.

636
00:43:21,960 --> 00:43:26,380
So I already had this repo and I knew that it had some sort of simple tests in it,

637
00:43:27,980 --> 00:43:33,260
That project ... if I open it in my text editor, it has a package.json file

638
00:43:33,740 --> 00:43:35,840
and in that file I have some scripts.

639
00:43:36,300 --> 00:43:38,640
So I can say npm build or npm test

640
00:43:39,020 --> 00:43:40,400
and then tell it what to do.

641
00:43:40,500 --> 00:43:43,780
And so my npm test command runs grunt Jasmine.

642
00:43:44,360 --> 00:43:48,960
So I have grunt, the JavaScript task runner and then it pulls in Jasmine,

643
00:43:48,960 --> 00:43:54,420
the grunt contrib Jasmine module I guess I installed in it from NPM

644
00:43:55,200 --> 00:43:59,520
and I have a single task because this is a really simple demo it's just showing how to test,

645
00:44:00,040 --> 00:44:07,660
so i init Grunt with Jasmine and in the test object I point it at a source file of axe-core.

646
00:44:08,220 --> 00:44:10,520
I'm just pulling acts directly from the Node modules.

647
00:44:10,880 --> 00:44:14,760
So it's Node module slash axe-core slash axe dot js

648
00:44:15,500 --> 00:44:20,060
and that will tell Jasmine about this JavaScript file so it will inject it into this test environment

649
00:44:20,060 --> 00:44:23,340
and then we have access to that in the global namespace.

650
00:44:24,820 --> 00:44:27,660
For the options in Jasmine, I tell it where my tests live.

651
00:44:28,320 --> 00:44:31,580
So you could put them in any folder, but I have them in a spec directory

652
00:44:32,060 --> 00:44:36,360
and then using wildcards I can just say hey run any file in this folder.

653
00:44:36,940 --> 00:44:40,300
And so it'll just automatically pick up any files that you add in this task.

654
00:44:40,780 --> 00:44:43,820
And you could use Mocha, that would be another test framework.

655
00:44:44,120 --> 00:44:47,760
It's really just this was an example that I had using Jasmine.

656
00:44:49,500 --> 00:44:55,500
So in the test itself, I described axe, because that's what we're testing in this example.

657
00:44:55,800 --> 00:44:58,880
I am including a fixture dynamically.

658
00:44:59,100 --> 00:45:02,680
So how you include the code that you're actually testing can vary.

659
00:45:03,320 --> 00:45:06,080
You might have a component that you would instantiate with Javascript.

660
00:45:06,520 --> 00:45:10,000
You might load something ... there's all different scenarios,

661
00:45:10,480 --> 00:45:17,500
the quick and dirtiest way, then I could just isolate my test was to put some strings of HTML.

662
00:45:18,100 --> 00:45:22,520
So I have a button, that's the cool, it's a taco button, it's the coolest button ever because it delivers tacos,

663
00:45:24,000 --> 00:45:29,700
And then, I have a broken fieldset so I have a fieldset with an input but no label.

664
00:45:30,120 --> 00:45:32,960
So I know that's broken and I expect it to be broken.

665
00:45:33,240 --> 00:45:34,780
So my two tests here ...

666
00:45:35,540 --> 00:45:39,340
... assert that axe should report that good HTML is good

667
00:45:40,240 --> 00:45:46,120
by ... I pull in just using document dot getElementById

668
00:45:46,300 --> 00:45:50,960
So in this environment I can use browser DOM APIs, which is really cool.

669
00:45:51,840 --> 00:45:54,580
So I can go and grab that taco button by its ID.

670
00:45:54,960 --> 00:45:56,420
I can say axe dot run,

671
00:45:56,420 --> 00:45:59,380
pass it a reference to this particular part of the fixture,

672
00:46:00,120 --> 00:46:04,500
and then I can tell axe to do its thing with that same call that we used before.

673
00:46:04,500 --> 00:46:08,820
And when it passes back the results object, I expect that it has no violations.

674
00:46:10,060 --> 00:46:12,760
In the second test, I expect that there's a violation.

675
00:46:12,760 --> 00:46:19,060
So the test passes even though it has broken HTML in it, which is kind of a mind game.

676
00:46:19,360 --> 00:46:21,960
But the idea is that I have these two examples

677
00:46:22,240 --> 00:46:27,500
and they're checking the quality of this HTML against axe-core.

678
00:46:28,580 --> 00:46:30,580
So I had these two passing tests ...

679
00:46:31,160 --> 00:46:34,240
and to hook up CI for this, on Github,

680
00:46:34,580 --> 00:46:38,860
as long as you have access and permissions to the settings tab of the repository,

681
00:46:38,860 --> 00:46:40,860
t's kind of a minor detail,

682
00:46:40,860 --> 00:46:47,440
you can go into settings under integrations and services there's this little drop-down that says add service.

683
00:46:48,260 --> 00:46:52,340
And there's a ton of stuff in here, but it's both Circle and Travis are options.

684
00:46:52,960 --> 00:46:54,620
So you can go and set up circle.

685
00:46:56,020 --> 00:47:02,020
It gives you this little screen that says add Circle CI and you can leave the domain blank and just hit add service.

686
00:47:02,400 --> 00:47:03,300
It's really easy.

687
00:47:04,380 --> 00:47:08,700
And then, once it's there you can go back to your settings tab and see which integrations you have.

688
00:47:08,700 --> 00:47:14,020
That's where you might have other things like the sneak security thing or our little CLA checker.

689
00:47:14,520 --> 00:47:17,640
So any integrations for that repo would be listed in the settings.

690
00:47:19,740 --> 00:47:21,740
So then I go over to Circle CI's website,

691
00:47:22,340 --> 00:47:25,620
to make sure that I actually have this binding set up.

692
00:47:25,620 --> 00:47:27,620
So the repo has given permission

693
00:47:27,880 --> 00:47:30,820
now we have to go over to Circle and tell it about this repo.

694
00:47:31,100 --> 00:47:33,100
And so I go in all my projects,

695
00:47:33,520 --> 00:47:37,960
I'm showing it has both Github and bitbucket, because we use both a Deque,

696
00:47:38,720 --> 00:47:43,360
But I can go into my own Github account and find any projects,

697
00:47:43,360 --> 00:47:49,780
and go make this association between the Github repository and Circle so that they're their friends now,

698
00:47:50,480 --> 00:47:55,460
And rather than push code the first time I ran this I just hit build project,

699
00:47:56,580 --> 00:48:01,480
And it would go and run the tests right then otherwise I would have had to push updated code to get him to run.

700
00:48:01,480 --> 00:48:07,020
But that'll happen the next time I push code but I wanted to just run this right away, so I hit build project.

701
00:48:07,760 --> 00:48:10,620
And they could really use some better color contrast on their site.

702
00:48:13,400 --> 00:48:19,440
Once I've got that, once I've built this project, I can see that it says success and it has this you know green.

703
00:48:20,700 --> 00:48:23,700
An example in the real world of where you might have a bunch of tests,

704
00:48:23,700 --> 00:48:26,120
you might have a bunch of passes and a bunch of failures,

705
00:48:26,900 --> 00:48:33,420
we had to get our configuration set up correctly, so Circle ... this is a circle example...

706
00:48:33,420 --> 00:48:35,420
it was failing for a little while.

707
00:48:35,860 --> 00:48:37,860
And so if you have it failing,

708
00:48:38,140 --> 00:48:42,720
it's like, I feel so drawn to fix it, need to fix it, it's broken.

709
00:48:43,000 --> 00:48:46,300
So it's that it's a good reminder of the health of your code.

710
00:48:46,300 --> 00:48:48,900
Like, is it passing? Is it failing? Who broke it?

711
00:48:49,440 --> 00:48:50,900
And it will tell you who broke it.

712
00:48:51,420 --> 00:48:52,740
So Dylan broke it.

713
00:48:52,740 --> 00:48:54,640
[laughter]

714
00:48:54,640 --> 00:48:56,080
I broke it too. We all break it.

715
00:48:56,080 --> 00:48:58,260
It's fun, you fix it. That's part of the process.

716
00:48:58,860 --> 00:49:02,200
But that's how you hook up a Github repository to CI.

717
00:49:02,660 --> 00:49:03,820
And then when it runs ...

718
00:49:04,100 --> 00:49:08,540
you know, anytime we push code or if someone pushes a pull request,  it will automatically run all of our tests.

719
00:49:09,300 --> 00:49:11,940
But you have to have tests to begin with it's kind of a big caveat.

720
00:49:14,400 --> 00:49:15,360
So there's some gotchas.

721
00:49:15,660 --> 00:49:20,520
This was just some things that really caught me off guard.

722
00:49:20,520 --> 00:49:22,740
Things that hopefully will help you.

723
00:49:23,000 --> 00:49:24,520
And I have a Gif of ...

724
00:49:25,760 --> 00:49:27,760
... gosh ... I'm blanking on what show that is.

725
00:49:29,660 --> 00:49:31,380
it's Parks and Rec. I knew it was Leslie Knope.

726
00:49:31,380 --> 00:49:32,520
She's sort of like ...

727
00:49:33,120 --> 00:49:35,280
a bigger figure to me than just a TV character.

728
00:49:35,280 --> 00:49:36,740
Like Leslie Knope is amazing.

729
00:49:36,740 --> 00:49:42,640
But there's an episode where they get her good and it's got a big red stamp over face saying Gotcha!

730
00:49:44,800 --> 00:49:45,300
Gotcha!

731
00:49:45,300 --> 00:49:46,720
Okay so if you see this ...

732
00:49:47,160 --> 00:49:50,820
I have a little bit of code from my test running locally,

733
00:49:51,060 --> 00:49:56,340
or actually, no, this was ... I could reproduce it locally if I had the same scenario.

734
00:49:56,660 --> 00:49:58,660
So this I saw on Circle.

735
00:49:59,560 --> 00:50:01,740
My tests were failing, I go to look at why,

736
00:50:02,240 --> 00:50:09,480
And it says it's running our parallel browser tests and it says loading tests webdriver.js tasks error.

737
00:50:10,080 --> 00:50:12,760
Syntax error unexpected token dot dot dot.

738
00:50:14,340 --> 00:50:16,060
Took me a while to figure out what that one was.

739
00:50:16,320 --> 00:50:22,480
So, turns out, we use ES6 features and including the new spread syntax,

740
00:50:23,660 --> 00:50:28,380
So that's the new feature in JavaScript that depends on the version of node.js that you are running.

741
00:50:29,000 --> 00:50:33,400
And as I mentioned, the version that Circle and Travis installs by default is really old.

742
00:50:34,460 --> 00:50:39,000
So if you're using newer JavaScript features and you see this unexpected token dot dot dot ...

743
00:50:39,400 --> 00:50:41,740
you need to go and tell it to use a newer version of Node.

744
00:50:43,080 --> 00:50:44,620
And that's happened to me multiple times,

745
00:50:44,620 --> 00:50:48,680
so I thought it was worthy of telling you about so you don't have the same problem.

746
00:50:49,800 --> 00:50:53,900
So yeah, just upgrade the Node version in those config files that's how we upgrade it

747
00:50:54,120 --> 00:50:57,160
and then you can use features like ES6 in your tests

748
00:50:58,400 --> 00:51:02,300
So in our tests, we're not as worried about compiling to old versions of JavaScript,

749
00:51:02,640 --> 00:51:03,620
because they're tests.

750
00:51:03,960 --> 00:51:06,400
Whereas in your code that you're shipping the users,

751
00:51:06,400 --> 00:51:10,760
you probably want to transpile it back to ECMAScript five and stuff like that.

752
00:51:12,060 --> 00:51:14,060
And test though ... we can get fancy.

753
00:51:15,000 --> 00:51:15,720
So here's another one.

754
00:51:15,720 --> 00:51:19,140
If you see this, you should try and reproduce your test locally.

755
00:51:19,140 --> 00:51:24,360
So figure out if you can you know run your test locally like I did in my slides, how we had the command prompt,

756
00:51:24,900 --> 00:51:28,420
and ideally, you can reproduce it there.

757
00:51:28,700 --> 00:51:35,500
If you can't and here's an example of what I found was our color contrast sticky header test

758
00:51:35,920 --> 00:51:38,560
was saying type error undefined is not an object.

759
00:51:39,220 --> 00:51:41,200
It was trying to evaluate what the reason was

760
00:51:41,200 --> 00:51:44,900
that we couldn't tell like that your color contrast was passing or failing.

761
00:51:45,400 --> 00:51:49,920
And further down in the test that's failing it says uncaught.

762
00:51:51,260 --> 00:51:56,840
So there's an uncaught exception in the code, but only on CI it wasn't happening locally.

763
00:51:57,740 --> 00:51:59,120
So how do you get around that?

764
00:51:59,120 --> 00:52:00,700
That was kind of a tricky one.

765
00:52:00,700 --> 00:52:02,700
So I add logging ... [laughing]

766
00:52:03,720 --> 00:52:08,580
... like how I started with programming back in ActionScript Flash days was trace all the things.

767
00:52:09,020 --> 00:52:11,020
So in our Mocha test ...

768
00:52:11,740 --> 00:52:15,120
... the mocha grunt task that we were using

769
00:52:15,120 --> 00:52:17,120
had this option to log errors.

770
00:52:17,120 --> 00:52:19,120
So if I change that to log errors true...

771
00:52:20,340 --> 00:52:23,120
... CI might start actually reporting what failed.

772
00:52:23,120 --> 00:52:25,520
Otherwise, they try to suppress them by default.

773
00:52:26,260 --> 00:52:28,580
And if that isn't an option, maybe you're not using Mocha

774
00:52:28,580 --> 00:52:31,840
or your test framework is just really quiet about what failed

775
00:52:31,840 --> 00:52:34,260
or like what error actually occurred,

776
00:52:34,960 --> 00:52:39,400
you can wrap that new code, whatever code ... if you figured out where it's failing,

777
00:52:39,740 --> 00:52:42,100
you can wrap it in a try-catch in JavaScript.

778
00:52:42,100 --> 00:52:44,100
So you put the code in the try block,

779
00:52:44,940 --> 00:52:49,080
And then if it fails in the catch, you just console.log the error.

780
00:52:50,160 --> 00:52:53,300
And that is really hacky, but it works.

781
00:52:53,840 --> 00:52:57,980
So that's how you can figure out what failed and then have it report back to you.

782
00:52:57,980 --> 00:53:02,380
And that without fail is like my number one debugging tip for CI.

783
00:53:02,720 --> 00:53:05,300
Because otherwise, it's just a black box and you have no idea ...

784
00:53:06,000 --> 00:53:09,620
like why was that datum dot reason object undefined there?

785
00:53:10,420 --> 00:53:11,340
I have no idea.

786
00:53:11,340 --> 00:53:16,980
But I was able to debug it and add some more checks and conditionals to say hey if this is broken,

787
00:53:17,980 --> 00:53:22,700
don't die, just move on with your life or here's a default value or whatever.

788
00:53:22,960 --> 00:53:28,440
So if you are having trouble debugging, the try/catch is totally worth checking out.

789
00:53:31,180 --> 00:53:33,800
And if you have all the stuff set up you can do really funny things

790
00:53:33,800 --> 00:53:39,440
like I mentioned with you know lighting up someone's desk or having a drone go over and surprise them.

791
00:53:39,760 --> 00:53:42,080
I wrote on Twitter I was trying to find

792
00:53:42,680 --> 00:53:46,600
I knew the Angular team in the Google office had a big monitor of their build status

793
00:53:46,600 --> 00:53:49,360
and I happen to be there one time when I broke Angular.

794
00:53:50,280 --> 00:53:52,460
It was amazing and horrifying,

795
00:53:52,920 --> 00:53:56,600
but I didn't have a picture of it I'm like, "oh, I don't know take a picture of it."

796
00:53:57,320 --> 00:54:01,180
Somebody else had a cool monitor where anyone who broke the build they would say wanted

797
00:54:01,860 --> 00:54:03,080
for crimes against Babel.

798
00:54:03,800 --> 00:54:07,560
and have a made-up reward and would say how long the build has been broken.

799
00:54:07,560 --> 00:54:08,560
I think this is kind of old.

800
00:54:08,560 --> 00:54:10,120
It says 2014.

801
00:54:10,600 --> 00:54:14,720
But it's a really funny way to kind of gamify fixing your code,

802
00:54:15,420 --> 00:54:19,040
especially if you have accessibility tests, like you could, depending on what failed,

803
00:54:19,040 --> 00:54:21,840
you could probably get really fancy with your build monitor.

804
00:54:23,360 --> 00:54:28,560
Makes it a collaborative effort and you know not such a nightmare it could be sort of a funny experience,

805
00:54:28,560 --> 00:54:30,560
like "haha, we broke the build let's go fix it."

806
00:54:31,600 --> 00:54:35,880
So that was one example of tracking who broke it that you could do if you had CI hooked up.

807
00:54:38,520 --> 00:54:43,400
So your end-all goal is to both write software tests and then get them passing.

808
00:54:43,660 --> 00:54:47,980
Because there's just super satisfying to feel like your code is covered.

809
00:54:48,720 --> 00:54:52,460
So that you're not pushing code out there and just going well I hope it doesn't break.

810
00:54:53,300 --> 00:54:54,580
Because I've done that where ...

811
00:54:55,200 --> 00:54:59,020
I didn't realize that I was breaking something on another page.

812
00:54:59,020 --> 00:55:01,960
Like it happens, we're human, we make mistakes.

813
00:55:02,220 --> 00:55:05,000
But if we have test coverage that way we know about it.

814
00:55:05,240 --> 00:55:08,920
Maybe it fails a build and it doesn't push the code to production

815
00:55:09,300 --> 00:55:14,140
Whew ... you're like another day to fix it and you're not spending you know all night trying to fix it

816
00:55:14,140 --> 00:55:16,320
because it's broken out in production.

817
00:55:17,100 --> 00:55:21,960
These are really pragmatic ways that we can get more accurate and more professional

818
00:55:21,960 --> 00:55:26,020
about how we push code to new environments including for accessibility features.

819
00:55:28,080 --> 00:55:31,840
You can be, yes, like Kip from Napoleon Dynamite.

820
00:55:32,180 --> 00:55:35,560
Because anytime a test pass I still go "yes!" every time.

821
00:55:36,440 --> 00:55:37,460
Never fails.

822
00:55:38,760 --> 00:55:43,560
So to recap, we can automate about 30 to 50 percent of accessibility issues.

823
00:55:43,560 --> 00:55:46,980
I wish it was more, but that's the real world, that's how it works.

824
00:55:47,400 --> 00:55:52,200
But the benefit of automating those issues is that it frees us up from having to

825
00:55:52,960 --> 00:55:56,380
spend our human time debugging things that we can catch with computers.

826
00:55:56,880 --> 00:55:59,440
So I think it's really valuable to have that practice.

827
00:56:00,600 --> 00:56:05,040
You want to write a mix of unit and integration tests, so that you're catching a variety of bugs,

828
00:56:05,260 --> 00:56:10,460
so that you have really solid features that you're contributing but you don't have those bathroom issues,

829
00:56:10,460 --> 00:56:12,940
where the paper towels we're blowing everywhere

830
00:56:13,340 --> 00:56:15,220
because we didn't test it integrated.

831
00:56:16,520 --> 00:56:19,860
You can expand your platform coverage using continuous integration,

832
00:56:19,860 --> 00:56:24,140
so that you can run your tests in environments that maybe you don't have physically in front of you.

833
00:56:25,220 --> 00:56:26,660
You want to watch out for gotchas,

834
00:56:27,120 --> 00:56:30,740
because that's sort of the real-world application of this

835
00:56:30,740 --> 00:56:36,680
is that when you're actually trying to debug while your test failed, that logging might really save you.

836
00:56:37,640 --> 00:56:41,280
But don't forget about manual accessibility testing and usability testing.

837
00:56:41,500 --> 00:56:45,720
Because we're only, scratching the surface here with what we can automate.

838
00:56:46,080 --> 00:56:49,860
So we want to make sure that things are actually good experiences for our users.

839
00:56:52,620 --> 00:56:56,500
So with that, I think we could do some Q&A. Thanks everyone!

840
00:56:56,500 --> 00:57:01,840
[Applause]

