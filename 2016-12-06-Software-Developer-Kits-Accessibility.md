# Software Developer Kits & Accessibility
## Thomas Logan - Tuesday, December 6, 2016
[Source recording](https://www.youtube.com/watch?v=Csh3G2bdBMk)

**[Thomas]:** Thank you. Hello, everyone.

**[Applause]**

**[Thomas]:** That video made me a bit emotional, too. I hadn't actually seen that video yet, but I had known that Apple started their keynote this year with a sequence of videos. And it was, you know, really exciting to me to see, you know, the CEO of the world's most powerful corporation, the richest corporation, starting off their presentation talking about accessibility. It does really speak to the fact that we are at a time where change is happening.

I started working accessibility in 2001. I was a computer science student in North Carolina, Chapel Hill. So Michael Jordan here in Chicago. I'm a big fan.

13
00:01:11,780 --> 00:01:16,900
So I started in computer science, and I worked with a blind student in the classics department.

14
00:01:17,300 --> 00:01:21,500
He was working with ancient world maps which are inherently visual.

15
00:01:21,980 --> 00:01:28,100
And so that was my first exposure to thinking about accessibility as someone new to computer science.

16
00:01:28,100 --> 00:01:30,200
Like, wow, this is actually something where

17
00:01:30,600 --> 00:01:34,480
with technology we can make information accessible to someone else.

18
00:01:34,700 --> 00:01:40,560
So my project at that time was how do we make a map explored through touch and sound.

19
00:01:40,920 --> 00:01:45,600
That's what got me interested, you know, in this whole world of accessibility.

20
00:01:45,600 --> 00:01:50,040
Right after that I actually got a job at Microsoft.

21
00:01:50,200 --> 00:01:54,380
So speaking tonight about accessibility software development kits,

22
00:01:55,000 --> 00:01:57,900
it's kind of close to me because it's kind of full circle for me.

23
00:01:57,900 --> 00:02:04,120
That's really the first corporate job I had in accessibility is working on a software development kit.

24
00:02:04,580 --> 00:02:07,560
I worked on Microsoft UI automation

25
00:02:08,020 --> 00:02:12,980
which is a way to make software applications accessible on the Windows platform.

26
00:02:13,580 --> 00:02:17,760
And, you know, it's funny for me just to go back in time and look at me coming out of college,

27
00:02:18,520 --> 00:02:25,080
really just I've only worked with this one student that was in the computer science department,

28
00:02:25,080 --> 00:02:27,620
learned from the experience of that project.

29
00:02:27,620 --> 00:02:31,980
And then there I was working on a software development kit at that time

30
00:02:31,980 --> 00:02:35,180
one of the largest companies really to understand

31
00:02:35,180 --> 00:02:40,260
what are the things that need to be in a software development kit for accessibility.

32
00:02:40,260 --> 00:02:42,260
So tonight, you know, it's really ...

33
00:02:42,760 --> 00:02:48,320
I'm kind of highlighting a lot of the different things that I've seen in the current software development kits.

34
00:02:48,900 --> 00:02:52,940
It's coming from both the point of view of let's look at what's really interesting and great

35
00:02:53,400 --> 00:02:56,220
in each one of these kits but also sort of a bit of

36
00:02:56,680 --> 00:03:00,320
let's look at the big picture of why does each software development kit

37
00:03:00,700 --> 00:03:02,700
need to have each of these unique things.

38
00:03:02,700 --> 00:03:04,700
You know, I'm kind of coming from a viewpoint now

39
00:03:04,700 --> 00:03:12,220
working as long as I have in this field that we really do better working collaboratively and working together.

40
00:03:12,220 --> 00:03:17,660
So part of my viewpoint even talking about these kits is how can we sort of bring these together,

41
00:03:17,660 --> 00:03:22,960
like why do we need to think of making application accessible on Android as something,

42
00:03:23,560 --> 00:03:28,780
you know, kind of very different from making it accessible on iOS or on Microsoft.

43
00:03:29,820 --> 00:03:30,980
So a couple of other things.

44
00:03:30,980 --> 00:03:32,420
I'm @techthomas on Twitter.

45
00:03:32,860 --> 00:03:36,300
I'm not's prolific as Dennis on Twitter but I try to be.

46
00:03:36,620 --> 00:03:39,980
I have a company called Equal Entry.

47
00:03:39,980 --> 00:03:46,440
My whole career is working on making technology accessible.

48
00:03:53,760 --> 00:03:57,180
Right as I say that, my Chrome crashes.

49
00:03:57,680 --> 00:03:59,680
That's a different kind of accessibility.

50
00:04:01,320 --> 00:04:08,480
So tonight  I'm a big person.  I do a lot of presentations, so I'm very much into what are my three key takeaways.

51
00:04:08,480 --> 00:04:10,800
I'm going to start with them and end with them.

52
00:04:10,800 --> 00:04:13,220
My first key takeaway is

53
00:04:13,220 --> 00:04:19,700
I think accessibility software development kits should strive for more consistency between implementations.

54
00:04:19,700 --> 00:04:26,900
I think it's not doing a service to accessibility to have these concepts that are all in theory

55
00:04:26,900 --> 00:04:31,160
exactly the same concepts be expressed different ways on each platform.

56
00:04:31,160 --> 00:04:34,980
You know, I'm someone that's, like, looking at virtual reality now as, like,

57
00:04:34,980 --> 00:04:39,180
okay, my partner actually works on a virtual reality platform.

58
00:04:39,180 --> 00:04:42,760
I don't want virtual reality to be something that we're waiting like

59
00:04:42,760 --> 00:04:48,220
five years after people start working in these new experiences to make it accessible.

60
00:04:48,220 --> 00:04:51,280
I'm already thinking from that viewpoint, like,

61
00:04:51,280 --> 00:04:55,400
let's learn from everything that's been done already in the software development kits.

62
00:04:55,400 --> 00:05:01,040
And as new technologies continue to come out, try to make these things more consistent.

63
00:05:01,740 --> 00:05:06,840
Second is I think accessibility software developer kits, when we make them,

64
00:05:06,840 --> 00:05:13,860
we should have at least one real example demonstration of how to properly use the functionality in it.

65
00:05:14,120 --> 00:05:20,280
I've worked with the W3C.  I've worked on the Accessible Rich Internet Specification.

66
00:05:20,280 --> 00:05:22,880
I've read a lot of the specifications.

67
00:05:23,660 --> 00:05:26,160
Frequently, you know, for me I'm always thinking,

68
00:05:26,160 --> 00:05:30,260
wow, we always document these API calls, things developers should do.

69
00:05:30,540 --> 00:05:33,340
We don't exactly explain end-to-end how it would work.

70
00:05:33,340 --> 00:05:37,200
Like, the video that we watched at the very beginning tonight, it's very powerful.

71
00:05:37,200 --> 00:05:39,200
You know, we're seeing things happening.

72
00:05:39,540 --> 00:05:42,540
I guess that was Final Cut Pro, or iMovie.

73
00:05:42,540 --> 00:05:43,460
It was Final Cut Pro.

74
00:05:43,460 --> 00:05:47,480
Right, it's very interesting if you can connect the experience of

75
00:05:47,480 --> 00:05:50,680
what did the developer do in the Apple SDK

76
00:05:50,680 --> 00:05:57,200
to make that functionality work for using the head switch that allowed that movie to be created.

77
00:05:57,200 --> 00:06:01,260
A lot of times when we look at the documentation for the developer kits,

78
00:06:01,260 --> 00:06:03,920
they don't actually connect the experience end-to-end.

79
00:06:04,320 --> 00:06:06,760
So that's something that I'm very passionate about.

80
00:06:06,760 --> 00:06:09,240
That's a lot of the work that I do at Equal Entry.

81
00:06:09,240 --> 00:06:11,420
I do a lot of work with SSB Bart Group.

82
00:06:11,860 --> 00:06:13,860
Erica Zelmanowicz is here from them.

83
00:06:14,360 --> 00:06:17,180
I have worked a lot on creating these demonstration videos.

84
00:06:17,180 --> 00:06:21,300
Here's what actually happens if you implement the work.

85
00:06:21,300 --> 00:06:24,440
I think that's something software development kits should do more of.

86
00:06:25,160 --> 00:06:29,660
Looking at what Apple already showed, that can be a followup.

87
00:06:29,660 --> 00:06:31,980
Ok, so how did that actually work?

88
00:06:31,980 --> 00:06:38,120
What needed to happen to make Final Cut Pro work that way so she could create that awesome video?

89
00:06:39,160 --> 00:06:40,280
And then, lastly,

90
00:06:40,280 --> 00:06:45,080
I think software development kits need to demonstrate more accessibility implementations throughout.

91
00:06:45,360 --> 00:06:48,560
So, you know, worked in this field a long time.

92
00:06:48,560 --> 00:06:52,980
Building up a sample as someone that doesn't work for Apple or work for Google,

93
00:06:52,980 --> 00:06:59,000
you know, I really or anyone working in this field, we only have so much time to build sample code

94
00:06:59,000 --> 00:07:02,180
to show people how to make something to be accessible.

95
00:07:02,580 --> 00:07:05,240
It's much better and what I have been trying to do more lately is

96
00:07:05,240 --> 00:07:09,140
look at what's already been shipped by Google or Apple or Microsoft and say,

97
00:07:10,020 --> 00:07:15,560
well how do we implement your accessibility API in the samples that you're teaching developers how to use?

98
00:07:15,980 --> 00:07:19,240
So what I will be demonstrating today ... most of them have one sample.

99
00:07:19,240 --> 00:07:25,660
At least each SDK will have an accessibility sample that shows you here's how we implement our API.

100
00:07:26,200 --> 00:07:29,740
But unfortunately all the rest of the samples which could have implemented the API

101
00:07:29,740 --> 00:07:34,980
and have been further evidence for developers of how to implement accessibility, they're just missing that work.

102
00:07:35,640 --> 00:07:41,160
So if I was a developer learning from a different part of the SDK and I download that sample,

103
00:07:41,640 --> 00:07:46,400
I'm like, grabbing something and starting from something that doesn't have accessibility built into it.

104
00:07:46,660 --> 00:07:47,660
So my point of view is

105
00:07:47,660 --> 00:07:52,880
we should be advocating or if we're working in a place where we can make that change,

106
00:07:52,880 --> 00:07:57,300
let's put more accessibility implementations into every developer sample we put out

107
00:07:57,300 --> 00:08:01,700
because a lot of developers work by cutting and pasting, at least I work that way.

108
00:08:02,140 --> 00:08:06,660
And so that's something that, you know, if people are cutting and pasting accessible solutions,

109
00:08:06,660 --> 00:08:09,660
now they already have those attributes in their code.

110
00:08:09,660 --> 00:08:12,060
They already know that kind of needs to be there.

111
00:08:12,560 --> 00:08:17,860
If it's not in the sample code they're cutting and pasting from, there's no real push for them to add that in.

112
00:08:17,860 --> 00:08:21,880
They have to actually go that extra step and download the accessibility SDK.

113
00:08:22,540 --> 00:08:24,100
Those are my three main points.

114
00:08:24,100 --> 00:08:29,520
The rest of my presentation today is really a whole bunch of demos which

115
00:08:30,800 --> 00:08:34,060
is dangerous so we'll see how far.

116
00:08:34,280 --> 00:08:34,900
[Attendee]: It's brave.

117
00:08:34,900 --> 00:08:39,260
[Thomas]: It's brave. We'll see how far each of those goes.

118
00:08:45,960 --> 00:08:47,640
We'll basically start with Apple.

119
00:08:47,640 --> 00:08:51,480
I think it's great we started with the Apple presentation.

120
00:08:51,480 --> 00:08:58,520
I really think Apple has just done so much to demonstrate, you know, really going above and beyond.

121
00:08:58,520 --> 00:09:00,880
The one that I usually show that was in that video

122
00:09:00,880 --> 00:09:07,040
is using the camera and actually hearing that someone's face is in the view finder.

123
00:09:07,040 --> 00:09:12,740
You know, that's not something legally required from Section 508 or WCAG 2.0

124
00:09:12,740 --> 00:09:16,940
or the jargon if you work in the accessibility industry we see.

125
00:09:16,940 --> 00:09:20,960
There's no mandate to add that to a consumer product.

126
00:09:20,960 --> 00:09:23,940
But Apple doing that, you know, it's such a powerful thing.

127
00:09:23,940 --> 00:09:28,200
Who doesn't want to take a photo of their family or share that on social media.

128
00:09:28,900 --> 00:09:32,200
It's a really good example.  It's cool to see that in there.

129
00:09:32,660 --> 00:09:37,040
I do think Apple has done a lot to really go beyond and do more.

130
00:09:37,040 --> 00:09:39,780
I think that's what all companies should be doing.

131
00:09:39,780 --> 00:09:46,340
It's definitely paid off for Apple with the loyalty of consumers really flocking to their platform.

132
00:09:47,320 --> 00:09:49,680
All right.  So let's start  ... actually, I forgot.

133
00:09:49,680 --> 00:09:52,700
The first thing that I'm talking about, this is just one example.

134
00:09:52,700 --> 00:09:55,820
I could have picked a million different examples of APIs.

135
00:09:55,820 --> 00:09:58,720
But let's start with the most basic.

136
00:10:00,040 --> 00:10:02,680
Images need to have a text alternative.

137
00:10:03,260 --> 00:10:09,880
If you started in the very earliest days of Web 1.0, the image tag had alt attribute

138
00:10:09,880 --> 00:10:16,420
and we would tell developers that every image needs to have an alt attribute and you need to fill that out.

139
00:10:16,680 --> 00:10:18,140
It's 2016.

140
00:10:18,140 --> 00:10:24,140
You can still find and scan most websites where that's not being done perfectly correctly.

141
00:10:24,140 --> 00:10:26,700
You know, you look at that, that's HTML.

142
00:10:26,700 --> 00:10:32,980
We're calling that concept that an image needs a text alternative an alt attribute.

143
00:10:33,660 --> 00:10:36,440
These are three more examples just to show you

144
00:10:36,440 --> 00:10:41,000
how dramatically different APIs refer to that same base concept.

145
00:10:41,000 --> 00:10:43,960
Like, we're saying let's give a description,

146
00:10:43,960 --> 00:10:47,000
let's give a label to something that's not text on the page.

147
00:10:48,200 --> 00:10:55,040
Microsoft has a property called UI automation or has a platform called UI automation

148
00:10:55,680 --> 00:10:58,100
and their property is called the name property field.

149
00:10:58,480 --> 00:11:00,480
So if you are working on Windows

150
00:11:00,480 --> 00:11:05,140
and you're building an application that needs to provide a text alternative for an image,

151
00:11:05,800 --> 00:11:07,600
you would need to go into your code and set

152
00:11:07,600 --> 00:11:12,780
AutomationElement.NameProperty equals the description of the image.

153
00:11:14,900 --> 00:11:21,160
If you are on Android and you are building an Android mobile application,

154
00:11:21,160 --> 00:11:25,580
Android has called this exact same content a content description.

155
00:11:26,080 --> 00:11:32,660
Android has a whole bunch of well meaning and well written information of how to add a content description

156
00:11:32,660 --> 00:11:36,280
to an image that's put on an Android phone.

157
00:11:36,740 --> 00:11:38,540
Conceptually, it's exactly the same thing.

158
00:11:38,540 --> 00:11:41,360
We're giving a text description of an image.

159
00:11:41,360 --> 00:11:45,900
But, you know, from a thought process or for a developer, we're making this harder.

160
00:11:45,900 --> 00:11:48,980
It's the exact same thing that needs to be done for accessibility.

161
00:11:49,620 --> 00:11:52,040
But because we call it something dramatically different,

162
00:11:52,560 --> 00:11:57,440
we don't really let people transfer that knowledge as easily between platforms.

163
00:11:57,440 --> 00:12:02,660
And the longer you work in technology, the more you cycle through these platforms.

164
00:12:02,660 --> 00:12:07,320
You just sort of start getting frustrated, why do I need to relearn some of these concepts.

165
00:12:07,320 --> 00:12:09,840
And now accessibility is a base concept.

166
00:12:11,000 --> 00:12:13,000
Android has a lot of great information.

167
00:12:13,000 --> 00:12:16,160
So just calling out this page, pretty well built out,

168
00:12:16,160 --> 00:12:21,800
lots of different information of how to properly add the content description.

169
00:12:22,800 --> 00:12:24,440
And then the last one is iOS.

170
00:12:24,440 --> 00:12:27,300
They call their property the accessibility label.

171
00:12:27,860 --> 00:12:34,240
So this would be if I'm building an iOS application and I put an image in iOS application.

172
00:12:34,240 --> 00:12:39,460
I would need to go and look and set accessibility label to provide that information.

173
00:12:40,180 --> 00:12:45,460
Now, if I was hosting a Web view inside of my iOS application,

174
00:12:45,900 --> 00:12:51,980
I might need to set aria-label because I'm building a Rich Internet Application.

175
00:12:52,760 --> 00:12:56,920
Maybe that's a little bit closer, accessibility label and aria label.

176
00:12:57,220 --> 00:13:00,300
But on Android and that means you were setting content description

177
00:13:00,300 --> 00:13:05,300
and you are setting aria-label, all the exact same concept.

178
00:13:06,180 --> 00:13:07,700
I just picked that as one.

179
00:13:07,700 --> 00:13:12,420
We could go into a million other properties, setting roles, states, values.

180
00:13:12,420 --> 00:13:16,520
These are all part of Web Content Accessibility Guidelines.

181
00:13:16,520 --> 00:13:20,420
They are all expressed usually differently on each platform.

182
00:13:20,420 --> 00:13:26,060
So just multiply this one property times all the things we want developers to do correctly.

183
00:13:26,760 --> 00:13:28,760
You can see we're adding a lot of complexity.

184
00:13:29,060 --> 00:13:31,360
I think that's my first key takeaway.

185
00:13:31,360 --> 00:13:37,460
If we could get, you know, as a group to either, one, work more collaboratively

186
00:13:37,460 --> 00:13:39,800
you know, it's very hard to work from consensus.

187
00:13:39,800 --> 00:13:45,960
I have only worked for a year with the W3C because I realized getting consensus is very difficult.

188
00:13:46,480 --> 00:13:51,980
I do think that's something we should advocate for as a group of people working in technology.

189
00:13:51,980 --> 00:13:59,020
The more consensus there is on these concepts, the easier it will be for someone to implement them.

190
00:13:59,240 --> 00:14:04,260
And I think about property like a border or a margin or an outline,

191
00:14:04,260 --> 00:14:09,460
those properties are pretty much referred very similarly across technology platforms.

192
00:14:09,460 --> 00:14:11,980
It's more when we get into things that have,

193
00:14:12,440 --> 00:14:17,200
like accessibility that hasn't had as much of a pattern practice to it.

194
00:14:18,740 --> 00:14:20,220
All right.  So that's the first point.

195
00:14:26,520 --> 00:14:27,020
All right.

196
00:14:27,020 --> 00:14:31,820
So then the next one is now I'm just going to look at three platforms just with the time we have,

197
00:14:31,820 --> 00:14:35,960
try to do a bunch of demos, but show you what is currently available

198
00:14:35,960 --> 00:14:40,260
and hopefully teach you some neat things that are on each platform.

199
00:14:40,680 --> 00:14:44,020
The first one for Apple, we'll start with Apple.

200
00:14:45,600 --> 00:14:48,720
They have a whole portal page for the developers.

201
00:14:48,720 --> 00:14:50,720
It's an accessibility portal page.

202
00:14:51,140 --> 00:14:53,760
We can read about accessibility on iOS.

203
00:14:55,820 --> 00:14:58,840
We can see lots of different areas.

204
00:14:58,840 --> 00:15:00,340
It's very nicely designed.

205
00:15:00,340 --> 00:15:05,040
We can go to captioning and audio descriptions, how to use voiceover.

206
00:15:05,600 --> 00:15:09,520
And then we have a bunch of developer resources that they link to.

207
00:15:09,520 --> 00:15:15,840
And so they do a great job of all of the videos from their different annual conferences for developers

208
00:15:15,840 --> 00:15:21,720
that they did a topic on accessibility are available, at least going back to 2012.

209
00:15:21,720 --> 00:15:25,740
So if you are interested, just from this development link,

210
00:15:27,000 --> 00:15:32,060
you can already watch some pretty high quality multimedia content of Apple developers

211
00:15:32,060 --> 00:15:37,380
or product managers teaching you how to do accessibility correctly.

212
00:15:38,180 --> 00:15:43,940
You can also go into the UI accessibility protocol

213
00:15:43,940 --> 00:15:52,440
which this is the main way that we implement accessibility in an Apple iPhone/iOS application.

214
00:15:52,440 --> 00:15:55,740
So, again, this is pretty well documented.

215
00:15:55,740 --> 00:16:02,380
One of the concepts that I call out is that we could go and read about these different properties,

216
00:16:02,380 --> 00:16:05,840
and each one has a pretty good written description

217
00:16:05,840 --> 00:16:09,980
but not necessarily that end-to-end visual description I was talking about.

218
00:16:09,980 --> 00:16:14,240
Like, I think it would be cool that somewhere in one of these properties,

219
00:16:14,240 --> 00:16:20,260
the functionality that we saw in the Final Cut video, it would actually say, for example,

220
00:16:20,260 --> 00:16:26,700
if you want to understand how this trait or this property works in practice, like, this is how it worked in Final Cut.

221
00:16:27,320 --> 00:16:34,520
So I'm going to click on traits just to call this one out as a place to look.

222
00:16:35,960 --> 00:16:40,620
These are a bunch of different traits that you can set in their accessibility API.

223
00:16:40,620 --> 00:16:42,980
And maybe some of them we read and we say,

224
00:16:42,980 --> 00:16:47,340
okay, I know what that should sound like when assistive technologies interact with it.

225
00:16:47,340 --> 00:16:55,280
Like UI accessibility trait selected, okay, yeah, if I have a selection state in my application,

226
00:16:55,280 --> 00:17:01,820
I want to express that an element is selected and probably voiceover on that screen reader reads it,

227
00:17:01,820 --> 00:17:04,420
it will read out to the user that element is selected.

228
00:17:05,280 --> 00:17:11,660
But there's other ones like UI accessibility trait updates frequently.

229
00:17:11,660 --> 00:17:18,360
Like, I read this one and it says, okay, this element updates very frequently.

230
00:17:18,820 --> 00:17:24,060
If the label or value too often to send update notifications include this trait

231
00:17:24,480 --> 00:17:28,800
when you want an assistive application to avoid handling continual notifications

232
00:17:28,800 --> 00:17:33,080
and instead poll for changes when it needs updated information.

233
00:17:33,660 --> 00:17:37,360
For example, you might use this trait to characterize the readout of a stopwatch.

234
00:17:37,680 --> 00:17:43,580
So, okay, you could use the timer stopwatch app on the iOS platform.

235
00:17:43,580 --> 00:17:46,320
But I still don't really know what's the correct behavior.

236
00:17:46,320 --> 00:17:50,000
Like, what does voiceover do now that I have set that property?

237
00:17:50,000 --> 00:17:53,880
Does it just read every minute, it polls it and reads it out?

238
00:17:53,880 --> 00:17:59,520
It's kind of hard to know exactly if I did start using this in my own application what it supposed to do.

239
00:18:00,020 --> 00:18:05,740
I think that's the barrier we have in a lot of APIs, is we don't actually explain the other side of it.

240
00:18:05,740 --> 00:18:07,740
We tell developers to set these traits.

241
00:18:08,440 --> 00:18:14,120
But what is the assistive technology supposed to do with that information when they consume it?

242
00:18:14,120 --> 00:18:19,120
I know we can't prescribe and set every single case of how they should use it.

243
00:18:19,120 --> 00:18:22,900
But I think something more representative of an end-to-end sample,

244
00:18:23,460 --> 00:18:27,800
that it really shows well with the stopwatch voiceover does this.

245
00:18:28,040 --> 00:18:31,040
That would really help illustrate the principle more.

246
00:18:33,820 --> 00:18:36,200
So that's the UI accessibility traits.

247
00:18:36,200 --> 00:18:41,620
I do call out here the two really good examples that Apple has built for developers.

248
00:18:41,620 --> 00:18:46,660
There's Custom Content Accessibility, and then HelloGoodbye.

249
00:18:47,420 --> 00:18:51,860
I'm going to try to hook up my iPhone now to show you guys HelloGoodbye.

250
00:18:53,460 --> 00:18:59,600
This is just another example where it's more just taking the documentation further.

251
00:18:59,900 --> 00:19:04,240
Maybe some of us in the room, you may have never seen this example.

252
00:19:04,240 --> 00:19:09,720
But you would actually benefit from knowing what are the things it shows me how to implement.

253
00:19:10,140 --> 00:19:15,220
So right now the Apple expectation is that we download the SDK.

254
00:19:15,620 --> 00:19:20,900
We can download the sample code, load it into X code, build it on our phone.

255
00:19:21,260 --> 00:19:25,800
But hopefully what I will be able to show is just demonstrate what it's trying to show you

256
00:19:26,300 --> 00:19:28,300
that's good for accessibility.

257
00:19:31,040 --> 00:19:37,800
Here's a free tip if you run ... if you have an Apple platform.

258
00:19:37,800 --> 00:19:42,880
You can actually turn on Quicktime, select your iPhone,

259
00:19:43,400 --> 00:19:50,340
and that's a really cheap and free way to display what you're iPhone is displaying

260
00:19:50,340 --> 00:19:52,340
to a room or for a presentation.

261
00:19:53,440 --> 00:19:59,160
So on this I have downloaded HelloGoodbye.

262
00:19:59,440 --> 00:20:04,080
And so one of the things that HelloGoodbye was implemented, so it was like,

263
00:20:04,080 --> 00:20:07,780
I think I like this, it's a pretty, fully built out sample.

264
00:20:07,980 --> 00:20:14,260
One of the other points I said is, If I was building a sample for iOS to teach you accessibility concepts,

265
00:20:14,860 --> 00:20:18,920
maybe mine wouldn't look quite as nice, wouldn't be as quite realistic.

266
00:20:18,920 --> 00:20:24,360
They are trying to build like a Tinder clone, or an OkCupid clone, you know, online dating.

267
00:20:24,360 --> 00:20:29,400
They took a pretty realistic app that lots of developers are trying to build,

268
00:20:29,400 --> 00:20:33,300
and they put accessibility implementations into it.

269
00:20:36,920 --> 00:20:47,280
So some of the things that it does is on the ... on your profile page showing you how ...

270
00:21:02,140 --> 00:21:04,140
[Voiceover Screen Reader]: 37 adjustable

271
00:21:04,820 --> 00:21:10,700
[Thomas]: So on this one, it is showing you how to use  using the adjustable trait.

272
00:21:10,700 --> 00:21:16,560
So adjustable trait is for a slider or something that can have a number go up and down.

273
00:21:16,560 --> 00:21:23,160
This is showing, okay, I'm setting how old I am by actually doing the slide up, slide down.

274
00:21:23,160 --> 00:21:30,600
[Voiceover Screen Reader]: 38, 39, 40, 41, 42, 40, 38

275
00:21:30,600 --> 00:21:32,760
[Thomas]: I don't know if I want to tell you guys how old I am.

276
00:21:32,760 --> 00:21:36,520
But um, we will ... this is an example of, all right,

277
00:21:36,520 --> 00:21:41,400
slider is not something that's always really clearly understood how do you make that accessible.

278
00:21:41,400 --> 00:21:45,620
A lot of apps that don't follow this pattern, they're not accessible.

279
00:21:45,620 --> 00:21:48,620
Like, they don't actually have the slide up and down to adjust it.

280
00:21:49,120 --> 00:21:52,580
So for a screenreader, they don't have a way to get to that and navigate it.

281
00:21:52,580 --> 00:21:57,600
In this sample, that was one of the ideas to build accessibility.

282
00:21:57,600 --> 00:22:05,580
[Voiceover Screen Reader]: HelloGoodbye.  Hello.  Matches.  HelloGoodbye.  Back button.  Matches.

283
00:22:05,580 --> 00:22:08,960
Slide up to say hello.  Slide down to say goodbye.

284
00:22:09,480 --> 00:22:13,260
[Thomas]: This one is showing actually visually displaying instructions of

285
00:22:13,260 --> 00:22:17,360
it's like the swipe right or swipe left from Tinder I think.

286
00:22:17,360 --> 00:22:20,160
But this is swipe up and swipe down, Hello and Goodbye.

287
00:22:21,860 --> 00:22:26,940
[Voiceover Screen Reader]: Profile photo. Image.

288
00:22:29,340 --> 00:22:31,260
[Attendee]: How did you navigate to that?

289
00:22:31,260 --> 00:22:33,520
[Thomas]: So this one, with Voiceover,

290
00:22:33,520 --> 00:22:38,040
it's swipe right to go to the next element, swipe left to go to the previous element.

291
00:22:38,040 --> 00:22:43,540
What this example was showing is we have a somewhat rich UI.

292
00:22:43,540 --> 00:22:48,740
You know, it's not as rich as what we see in the apps, but it shows we have a label for the photo.

293
00:22:49,400 --> 00:22:52,760
We can move sequentially through the content.

294
00:22:53,600 --> 00:22:55,600
[Voiceover Screen Reader]: Travel.

295
00:22:56,680 --> 00:22:59,260
[Thomas]: And this one is actually  oh.

296
00:23:02,220 --> 00:23:06,160
You know, one way that people frequently make mistakes with accessibility is it might read

297
00:23:06,160 --> 00:23:11,080
age, hobbies, then 32, then cooking bubble tea with friends, travel.

298
00:23:11,080 --> 00:23:12,600
That's hard to understand.

299
00:23:12,600 --> 00:23:18,780
So this was to show the proper implementation that it actually reads age, and it reads 32.

300
00:23:18,780 --> 00:23:21,560
It reads hobbies, and then it reads cooking bubbles.

301
00:23:21,840 --> 00:23:26,900
A lot of those things you have to learn going through the sample code and building it out.

302
00:23:27,500 --> 00:23:33,920
But having that also illustrated in the SDK, you know, where people don't have to go and download and build it,

303
00:23:33,920 --> 00:23:38,340
maybe a product manager or program manager or designer just wants to know

304
00:23:38,680 --> 00:23:40,280
the right behavior of these traits.

305
00:23:40,520 --> 00:23:42,120
They've already built this example.

306
00:23:42,120 --> 00:23:45,440
Right now it's kind of a little bit walled off that you have to download,

307
00:23:45,940 --> 00:23:49,280
build it, and play around with it to illustrate these.

308
00:23:55,260 --> 00:23:57,260
[Voiceover Screen Reader]: Voiceover off.

309
00:23:58,220 --> 00:24:00,600
[Thomas]: The other things that are interesting with this sample,

310
00:24:00,600 --> 00:24:07,200
so I think these are exciting sort of features that are coming and they're enabled on mobile platforms.

311
00:24:07,200 --> 00:24:13,620
But developers do have a way to detect if people are running different accessibility features on the iPhone.

312
00:24:14,280 --> 00:24:23,880
So this sample let's you see, for example, if I select bold text, this is actually going to reboot my phone a little bit.

313
00:24:24,440 --> 00:24:31,240
But when you use bold text on your phone, it makes applications that support that have a stronger contrast.

314
00:24:31,240 --> 00:24:32,740
It's easier to see.

315
00:24:38,580 --> 00:24:43,000
So this application, it might be a little hard to see without seeing it side by side.

316
00:24:43,000 --> 00:24:47,880
But it actually swaps out a bold font when the user sets that.

317
00:24:47,880 --> 00:24:50,740
So without that setting on, it's a little lower contrast.

318
00:24:50,740 --> 00:24:55,900
And maybe for some designers or design scenarios you don't want to have a bold font.

319
00:24:56,360 --> 00:25:00,020
But this app is showing that you can actually have two different presentations.

320
00:25:00,020 --> 00:25:04,100
You can detect if a user has that bold setting set on their phone.

321
00:25:04,540 --> 00:25:07,680
And then you can re-render the application that way.

322
00:25:09,120 --> 00:25:17,780
The only one I was going to call out here because I kind of react to this one quite a bit is animation,

323
00:25:17,780 --> 00:25:22,000
is becoming more back on trend and putting into interfaces.

324
00:25:22,000 --> 00:25:25,600
And so there is ... I have that actually set on right now.

325
00:25:25,600 --> 00:25:28,820
But you can reduce the motion of the user interface.

326
00:25:28,820 --> 00:25:35,020
So this app actually illustrates how to use or properly detect, reduce motion.

327
00:25:35,020 --> 00:25:42,840
This application, if I turn off "reduce motion," again, a little hard to see without doing this side by side.

328
00:25:43,200 --> 00:25:49,420
But, you know, when we're dismissing people that we either, you know, like them or don't like them,

329
00:25:49,420 --> 00:25:54,440
this animation happens much faster when reduced motion is turned off.

330
00:25:54,440 --> 00:26:00,980
So for someone who actually has maybe a type of disability where motion is either distracting

331
00:26:00,980 --> 00:26:07,060
or could be a vestibular disorder, this app shows you if you can set that setting, you can actually

332
00:26:07,520 --> 00:26:12,800
decrease the animation and make it slower, make it less jarring.

333
00:26:24,840 --> 00:26:31,520
So that is basically that was an app that they built, right, that was really good.

334
00:26:31,520 --> 00:26:35,660
Like, that's the one that they tell people let's go build an accessible app.

335
00:26:35,660 --> 00:26:37,060
Let's implement it.

336
00:26:37,060 --> 00:26:43,500
So now this is me kind of calling out Apple a little bit, that you go and get a different app from their SDK.

337
00:26:43,500 --> 00:26:49,360
They build an app for displaying a periodic table of elements.

338
00:26:50,120 --> 00:26:54,200
And they build that app more to train developers how to ... oh, let's see.

339
00:26:58,900 --> 00:27:01,300
You know, it's showing you a model view controller.

340
00:27:01,300 --> 00:27:06,860
We're having, you know, how to do configuring and responding selections in a tab bar,

341
00:27:06,860 --> 00:27:11,820
displaying information in a table view, using navigation controllers.

342
00:27:11,820 --> 00:27:16,920
There's, like, a whole bunch of things they're teaching you how to do in their accessibility ... sorry, in their API.

343
00:27:17,400 --> 00:27:21,540
The problem is they are not actually implementing accessibility in the sample.

344
00:27:21,540 --> 00:27:26,600
So if the developer hadn't downloaded that HelloGoodbye sample but they were interested

345
00:27:26,600 --> 00:27:32,100
in learning these concepts from the element sample, it doesn't have that implemented.

346
00:27:33,040 --> 00:27:35,040
So I'm just going to show that.

347
00:27:48,020 --> 00:27:55,240
So I made two. So I have fixed one, and this is the default one that comes in the API.

348
00:27:55,240 --> 00:28:03,900
So the default one, some of the critiques of what's being taught here is that this application when we

349
00:28:03,900 --> 00:28:10,100
spin it around and when we view information about the periodic table of the elements, the contrast of the text.

350
00:28:10,680 --> 00:28:16,120
So depending on the ones that we select, the contrast for, like, the link

351
00:28:16,120 --> 00:28:19,960
to view the hyperlink out there, it's not very good.

352
00:28:19,960 --> 00:28:24,120
So, you know, we could say, well, that's not the point of showing this sample.

353
00:28:24,120 --> 00:28:30,700
But it is if we want people to always be building accessible apps, even just having, you know,

354
00:28:31,100 --> 00:28:37,180
a sample that lots of people are learning from that doesn't illustrate that concept is problematic.

355
00:28:37,480 --> 00:28:40,280
Another one is if I turn on Voiceover ...

356
00:28:48,280 --> 00:28:49,660
[Voiceover Screen Reader]: Button. Tag button. Button. Wikipedia.

357
00:28:49,820 --> 00:28:52,500
[Thomas]: I'm going to swipe left and right.

358
00:28:53,040 --> 00:28:58,940
[Voiceover Screen Reader]: Button. Tag button. Button. Wikipedia.

359
00:28:58,940 --> 00:29:05,360
[Thomas]: So on this screen all we hear is back button, button, and view at Wikipedia.

360
00:29:05,360 --> 00:29:11,360
So the actual information, the information about the atomic weight, what element is being displayed,

361
00:29:11,620 --> 00:29:14,460
none of that information is exposed in this sample.

362
00:29:14,460 --> 00:29:19,380
So again, if I was building a card view, you could put anything into maybe you're like.

363
00:29:21,120 --> 00:29:22,340
[Voiceover Screen Reader]: Alert accessibility.

364
00:29:22,340 --> 00:29:27,320
[Thomas]: When I saw it, I'm like this is kind of a slick animation to turn the card over.

365
00:29:27,320 --> 00:29:31,140
But if someone just took this card, added their own information into it,

366
00:29:31,640 --> 00:29:35,380
it's already built not implementing accessibility.

367
00:29:35,940 --> 00:29:39,920
So I'm just going to show, because we don't have time to go fully into all of these.

368
00:29:41,980 --> 00:29:43,980
This was one where ...

369
00:29:50,280 --> 00:29:52,280
... turn off the contrast here ...

370
00:29:55,020 --> 00:30:01,460
So darken colors, if you didn't know, darken colors is how we set a high contrast theme on the iPhone.

371
00:30:01,460 --> 00:30:06,020
Kind of another point, most platforms call that high contrast theme.

372
00:30:06,680 --> 00:30:08,980
High contrast is somewhere in the language.

373
00:30:08,980 --> 00:30:13,200
In the language of iPhone, it's actually called darken colors.

374
00:30:13,200 --> 00:30:19,900
It really does potentially give the same possibility for a developer to say if someone has darken colors on,

375
00:30:20,380 --> 00:30:22,380
I'm going to present a high contrast theme.

376
00:30:22,780 --> 00:30:28,040
That's really taking a leap of understanding of accessibility to really get there that

377
00:30:28,040 --> 00:30:30,040
this is what that means.

378
00:30:31,180 --> 00:30:33,180
I'm going to turn that one off just for right now.

379
00:30:43,240 --> 00:30:47,180
[Voiceover Screen Reader]: Voice over off.  A11Y The elements. Back button.

380
00:30:47,180 --> 00:30:58,520
Americium. Atomic weight. 243. State.  Artificial. 7. Discover. 1944 A.D.

381
00:30:58,520 --> 00:31:07,580
[Thomas]: So in this concept, I'm showing you ... that's ... actually a sorry.

382
00:31:11,420 --> 00:31:15,800
To really nail down giving a live presentation and having a screenreader talking ...

383
00:31:15,800 --> 00:31:16,860
[Laughter]

384
00:31:16,860 --> 00:31:18,860
[Thomas]: it's quite a juxtaposition.

385
00:31:18,860 --> 00:31:26,300
One of the things I'm trying to illustrate that's in every API is you don't ever want each one of these pieces

386
00:31:26,300 --> 00:31:29,520
of text to be, like, separate, navigable elements.

387
00:31:29,520 --> 00:31:34,480
One of the basic principals is trying to group together information.

388
00:31:34,480 --> 00:31:39,540
All the APIs will have documentation explaining that concept.

389
00:31:39,740 --> 00:31:45,720
I saw this one as a perfect example as there's really no benefit, at least in this scenario

390
00:31:45,720 --> 00:31:53,780
making one swipe right go to the period, one swipe right go to the group, one swipe right go to discover.

391
00:31:53,780 --> 00:32:00,240
We can group that information together and make it just one hit target or one selection state.

392
00:32:00,920 --> 00:32:05,300
So, again, it's just looking at all the different samples that Apple has built,

393
00:32:05,880 --> 00:32:10,540
that was sort of my thought process when I had to work on how do I show people in my trainings

394
00:32:10,540 --> 00:32:13,820
to make an accessible app rather than build my own app.

395
00:32:14,240 --> 00:32:20,720
I took the Apple SDK for the periodic table of elements and just added those techniques in.

396
00:32:21,000 --> 00:32:25,940
But that's something I am planning to report back to Apple, hopefully incorporate.

397
00:32:25,940 --> 00:32:31,660
I would really like more and more samples to have those illustrative points.

398
00:32:40,400 --> 00:32:43,940
All right. So now I'll go off of Apple, switching to Android.

399
00:32:44,580 --> 00:32:47,060
Let's talk about some good things in Android.

400
00:32:51,500 --> 00:32:56,440
First, you know, Android has very complete accessibility SDK.

401
00:32:56,440 --> 00:33:02,060
One of the things that I think is the most interesting with Android is

402
00:33:02,060 --> 00:33:04,060
they have actually ...

403
00:33:21,480 --> 00:33:25,940
... they have a bunch of different ways to view and interpret the information.

404
00:33:25,940 --> 00:33:30,360
But on their developer screen, they actually have ...

405
00:33:32,820 --> 00:33:36,960
... way more documentation, step by step, of things that you should do.

406
00:33:36,960 --> 00:33:41,580
And then they even have a course that they've built that's like a step-by-step course

407
00:33:41,580 --> 00:33:43,580
for people to follow on at home.

408
00:33:43,580 --> 00:33:47,300
So rather than only having a video or only having a SDK,

409
00:33:47,300 --> 00:33:53,820
they have an iterative sample where you follow along and you build out the sample as you go.

410
00:33:53,820 --> 00:33:55,380
So you download it.

411
00:33:55,680 --> 00:33:56,920
You make these changes.

412
00:33:56,920 --> 00:34:01,240
And then you keep working with it and they tell you if you're doing things right or wrong.

413
00:34:01,460 --> 00:34:07,500
So I do think, you know, documentation, if anyone here in the room does work on the documentation team,

414
00:34:07,500 --> 00:34:11,520
that's something that I think Android and Google is probably doing the most

415
00:34:11,520 --> 00:34:17,320
for trying to document more interactive code samples.

416
00:34:17,820 --> 00:34:22,460
They've also done a lot of video trainings.

417
00:34:22,460 --> 00:34:26,640
So on Udacity which is also something that Google works a lot with,

418
00:34:26,640 --> 00:34:31,720
Google has a really extensive Web accessibility course that's available for free.

419
00:34:31,720 --> 00:34:38,040
And that's something that, you know, I think really supports the work that they have been doing on Android.

420
00:34:38,040 --> 00:34:42,340
So here's the app, sorry, the training.

421
00:34:42,640 --> 00:34:45,800
So you can see they have 13 different modules.

422
00:34:45,800 --> 00:34:49,580
This is the codelabs.developer.Google.

423
00:34:49,580 --> 00:34:52,080
And this is basic Android accessibility.

424
00:34:53,000 --> 00:34:55,600
You can really step through this at your own pace.

425
00:34:55,600 --> 00:35:03,920
And again, it has all of the different types of steps that you would expect from an accessibility training.

426
00:35:03,920 --> 00:35:05,920
They tell you how to download the code.

427
00:35:06,240 --> 00:35:08,480
You start off working in Android Studio.

428
00:35:09,020 --> 00:35:11,060
There are steps for enabling Talkback.

429
00:35:11,060 --> 00:35:16,520
They have done a lot on that side to make it more than just download a SDK sample.

430
00:35:16,520 --> 00:35:20,460
I think those are all good things to applaud.

431
00:35:28,520 --> 00:35:34,040
All right. So the basic accessibility ... all right. I'm going to try something here to switch to the other ...

432
00:36:00,640 --> 00:36:07,420
So on the Android, at least I don't know if something as fast as using Quicktime, to display your phone,

433
00:36:07,420 --> 00:36:12,120
so I use a paid client called Reflector.

434
00:36:12,920 --> 00:36:18,360
Reflector needs you to be on the same WiFi network to work.

435
00:36:18,680 --> 00:36:20,140
We'll see if they will work.

436
00:36:24,200 --> 00:36:26,560
We got it. All right.

437
00:36:38,180 --> 00:36:45,180
Well, just to keep it moving because this is live, I did record this prior to coming.

438
00:36:45,180 --> 00:36:51,680
That's another pro tip.  It's always good to record it before you go.

439
00:36:52,600 --> 00:36:54,860
[Attendee]: Finding it...

440
00:36:54,860 --> 00:37:01,860
[Thomas]: Right, finding it. It should be in something labeled. Accessibility Chicago. Have a good label.

441
00:37:02,280 --> 00:37:04,280
And this is ...

442
00:37:06,440 --> 00:37:12,260
basically I think the thing I want to call out that I thought was a little bit of a negative here is that

443
00:37:12,260 --> 00:37:19,940
so Android sample that you download from their SDK, if you compare that to what Apple did, this isn't a real app.

444
00:37:19,940 --> 00:37:25,000
This is probably more what I think I traditionally in accessibility samples where, of course,

445
00:37:25,000 --> 00:37:28,040
there's value in teaching us the techniques.

446
00:37:28,040 --> 00:37:34,320
But it's not as illustrative for a developer end-to-end especially if you look at,

447
00:37:34,320 --> 00:37:36,780
again, going back to the fist video that was shown.

448
00:37:36,780 --> 00:37:40,000
You really see the impact, like, why did I implement accessibility?

449
00:37:40,000 --> 00:37:44,600
Like, that person was now able to edit a video and this is how it all connects.

450
00:37:45,460 --> 00:37:48,220
I mean, it's nothing wrong with building a sample like this.

451
00:37:48,220 --> 00:37:52,820
It's just not as exciting or illustrative of why accessibility is important.

452
00:37:52,820 --> 00:37:59,540
So you step through and you set different information that's available in the API.

453
00:38:00,580 --> 00:38:06,980
But you can't actually really see end-to-end why that was important because it's not a real application.

454
00:38:09,760 --> 00:38:16,640
And then the last thing that I'll call out that's just another ding to me for Android is that, you know,

455
00:38:16,640 --> 00:38:21,000
there are a lot of conventions that have been built up for accessibility APIs.

456
00:38:21,000 --> 00:38:23,560
And one of the most important ones, I think,

457
00:38:23,560 --> 00:38:31,080
is that accessible labels or accessible names, they need to get associated with controls.

458
00:38:31,080 --> 00:38:36,300
And that's something that in the documentation at least for how you set up,

459
00:38:36,820 --> 00:38:40,900
like, this custom dial, they're just using the label "custom view."

460
00:38:40,900 --> 00:38:45,280
You also know this is Talkback showing what it's reading.

461
00:38:45,540 --> 00:38:49,580
It doesn't actually associate the label with the dials.

462
00:38:49,580 --> 00:38:53,020
So from even just in the accessibility sample,

463
00:38:53,020 --> 00:38:58,960
it doesn't really follow the conventions of what would normally be in an accessibility sample.

464
00:38:58,960 --> 00:39:02,200
And part of my question is that might be because

465
00:39:03,240 --> 00:39:07,920
the people don't work in a large enough group of comparing work across different platforms.

466
00:39:07,920 --> 00:39:12,720
There might be other reasons why that's implemented that way in Android.

467
00:39:12,720 --> 00:39:17,360
It's not explained and for someone who works in accessibility quite a lot,

468
00:39:17,360 --> 00:39:24,680
it's a noticeable difference in the way their API doesn't have the ability to do that versus the other APIs.

469
00:39:30,020 --> 00:39:37,340
And I will say another thing that I think is really good  and this is funny because

470
00:39:37,340 --> 00:39:44,060
now I don't have to actually have the screenreader reading out, but seeing "discard" buttons,

471
00:39:44,060 --> 00:39:50,480
the Android has a way to display what the speech synthesizer is speaking in its view.

472
00:39:50,920 --> 00:39:53,540
Voiceover running on iOS does not.

473
00:39:54,340 --> 00:39:58,460
If you are working collaborative with a developer and want to show them a bug,

474
00:39:58,820 --> 00:40:01,480
it's much easier having this visual display.

475
00:40:01,480 --> 00:40:06,860
This one is trying to show us it's stuttering saying discard button button.

476
00:40:06,860 --> 00:40:10,220
A screenreader just needs to hear discard button.

477
00:40:10,880 --> 00:40:14,480
I can actually take a screen shot, you know, using Android's Talkback

478
00:40:14,480 --> 00:40:17,360
because it does have the visual display.

479
00:40:17,360 --> 00:40:21,040
And if I'm working with someone, a developer, to show them the problem,

480
00:40:21,040 --> 00:40:24,700
it's easier to communicate the problem on this platform

481
00:40:24,700 --> 00:40:28,340
because we have that visual display of what the screenreader is speaking.

482
00:40:38,500 --> 00:40:41,700
[Dennis]: Time check. We have about five more minutes.

483
00:40:41,700 --> 00:40:42,540
[Thomas]: Perfect.

484
00:40:42,540 --> 00:40:45,020
So why not transition to Microsoft?

485
00:40:46,340 --> 00:40:51,260
Save the best or worst for last, depending on your opinions of each of these companies.

486
00:40:51,760 --> 00:40:57,880
So Microsoft, again, doing a great job on accessibility.

487
00:40:57,880 --> 00:41:01,520
You know, I started when I did start working accessibility,

488
00:41:01,520 --> 00:41:06,800
I was really excited to work for Microsoft because they actually had an accessibility team.

489
00:41:07,320 --> 00:41:12,700
So if you go back to 2002 when I graduated, it was not something like it is today

490
00:41:12,700 --> 00:41:16,840
where people had these accessibility groups so you could go and work in.

491
00:41:16,840 --> 00:41:25,100
So for a long time, Microsoft has been committed to working on accessibility and making progress there.

492
00:41:26,080 --> 00:41:30,300
So just want to show that they also have a developer portal.

493
00:41:30,300 --> 00:41:35,440
So all of the three main, you know, technology platform companies that I see,

494
00:41:35,440 --> 00:41:39,380
they all have these developer portals for accessibility.

495
00:41:39,840 --> 00:41:46,780
Microsoft's is also more heavily focused on video training, video illustrations of how to do things.

496
00:41:46,780 --> 00:41:50,200
And they similarly have sample code that you can download,

497
00:41:52,120 --> 00:41:55,720
different things that you can do to play around with accessibility.

498
00:41:55,720 --> 00:42:01,920
I will just call out the example I showed of Apple having SDK samples that aren't accessible.

499
00:42:02,380 --> 00:42:04,380
That applies for Google and Microsoft too.

500
00:42:04,380 --> 00:42:08,380
The majority of the samples don't have accessibility built into them.

501
00:42:08,380 --> 00:42:13,620
Unless you go to their developer accessibility portal and download the accessibility sample,

502
00:42:13,620 --> 00:42:15,620
you don't learn the techniques.

503
00:42:16,660 --> 00:42:20,920
The thing I wanted to demonstrate and I learned this very recently,

504
00:42:21,600 --> 00:42:24,540
how many people have used Microsoft Edge in the room?

505
00:42:25,740 --> 00:42:27,300
One, two, three, four.

506
00:42:27,440 --> 00:42:29,240
A smaller percentage.

507
00:42:29,240 --> 00:42:37,740
What's Microsoft trying to shift to for their new browser, for their new Web experience?

508
00:42:38,020 --> 00:42:41,960
So one of the things, I will just do parallels quickly.

509
00:42:42,340 --> 00:42:47,920
But Edge has a cool future for viewing the accessibility tree.

510
00:42:51,140 --> 00:42:57,140
And I guess I just wanted to make sure I showed at least one good thing from each of these three companies.

511
00:42:57,580 --> 00:42:59,400
And this is pretty cool.

512
00:42:59,400 --> 00:43:04,060
Like, the accessibility tree has always been, you know, if you work in accessibility,

513
00:43:04,060 --> 00:43:11,580
visualizing the accessibility tree, making sure accessible elements that there's not too many in the tree.

514
00:43:11,580 --> 00:43:14,080
That's always a part of all the different platforms.

515
00:43:14,260 --> 00:43:17,240
But they don't make it easy to see the tree.

516
00:43:17,240 --> 00:43:22,800
In Microsoft Edge, you can actually pull up the developer tools.

517
00:43:22,800 --> 00:43:27,840
And the accessibility tree is available from this accessibility icon.

518
00:43:29,160 --> 00:43:36,080
That will let you navigate through the tree of elements and see the different elements that are in the trees.

519
00:43:36,080 --> 00:43:40,440
I can see that there's hyperlinks in my presentation.

520
00:43:40,440 --> 00:43:44,220
I can see that there are headings in my presentation.

521
00:43:44,800 --> 00:43:50,700
I can see there's an element marked description which is what  because we have the highlighting,

522
00:43:51,080 --> 00:44:00,180
we can see that Microsoft Edge maps the block, quote, element to a description element in UI automation.

523
00:44:01,080 --> 00:44:02,760
So this is something very important.

524
00:44:02,760 --> 00:44:04,400
This is really talking about Web accessibility.

525
00:44:04,400 --> 00:44:06,760
I was talking about mobile accessibility before.

526
00:44:06,760 --> 00:44:13,500
But if you look at Safari running on the Mac or you look at Google Chrome running on Mac or Windows,

527
00:44:13,500 --> 00:44:16,660
they don't have an easy way to visualize this tree.

528
00:44:16,660 --> 00:44:18,820
You have to download other tools.

529
00:44:18,820 --> 00:44:23,740
I think this is great Microsoft building that into the browser.

530
00:44:23,740 --> 00:44:27,240
It's making it more present for developers that need to do this work.

531
00:44:27,240 --> 00:44:31,240
Like, why make someone download another tool to do accessibility?

532
00:44:31,240 --> 00:44:36,640
So let's look at that as a great example that hopefully gets emulated in the other browsers

533
00:44:36,640 --> 00:44:42,040
because if you have done a lot of work on developing accessibility, the tree is,

534
00:44:42,040 --> 00:44:47,120
like, a very important concept on any platform for making it accessible.

535
00:44:49,000 --> 00:44:51,840
So to wrap up, go back to my ...

536
00:45:02,240 --> 00:45:05,260
Well, I don't need to.  But I will use them from memory.

537
00:45:05,260 --> 00:45:09,120
The three points I was talking about here that we need

538
00:45:09,120 --> 00:45:14,800
to have a more robust set of developer examples for accessibility.

539
00:45:14,800 --> 00:45:21,320
Ideally, every developer sample in a SDK has accessibility built in.

540
00:45:22,400 --> 00:45:28,200
We should have more implementations for anything we put into an accessibility SDK.

541
00:45:28,800 --> 00:45:30,800
We should show how it works end-to-end.

542
00:45:30,800 --> 00:45:33,200
So we should make it really clear what the benefits are.

543
00:45:33,200 --> 00:45:38,780
Why is a developer doing that, and what's it supposed to look like with assistive technology.

544
00:45:39,180 --> 00:45:41,860
And, lastly, we should have more consistent naming.

545
00:45:41,860 --> 00:45:44,540
We should not make it confusing that, you know,

546
00:45:44,540 --> 00:45:49,500
we're giving a text alternative for an image having totally different names on each platform.

547
00:45:50,000 --> 00:45:51,620
That's more difficult.

548
00:45:51,620 --> 00:45:53,620
Those are my three points.

549
00:45:53,620 --> 00:45:54,900
I would like to wrap up.

550
00:45:54,900 --> 00:46:00,020
Thank you for the attention and then have some Q&A here at the end just for a few minutes.

551
00:46:00,020 --> 00:46:00,920
Thank you.

552
00:46:00,920 --> 00:46:04,220
[Applause]

553
00:46:04,220 --> 00:46:07,240
[Dennis]: What I will do as people have questions, I will actually hand you the mic.

554
00:46:07,240 --> 00:46:09,700
Anyone have any questions?

555
00:46:15,020 --> 00:46:18,620
[Attendee]: I was surprised ... first of all, thank you very much for your presentation.

556
00:46:19,480 --> 00:46:24,800
I was surprised to find or to know that Microsoft even did accessibility for so long.

557
00:46:25,540 --> 00:46:32,380
Why is it that Apple seems to be the winner of accessible platform?

558
00:46:33,460 --> 00:46:38,340
[Thomas]: Well, one thing that I do think is very interesting at least I can share

559
00:46:38,340 --> 00:46:45,000
from the Microsoft experience I had was that if we look at just the screenreader perspective,

560
00:46:45,000 --> 00:46:52,440
so people with vision impairments, Narrator, the screenreader that's built into the Windows platform

561
00:46:52,940 --> 00:46:58,880
had never been advertised by Microsoft as a screenreader replacement.

562
00:46:58,880 --> 00:47:03,480
And so I think that's been a big difficulty for them, that they're now, you know,

563
00:47:03,480 --> 00:47:08,080
addressing because Apple does build in a screenreader that works fully, you know,

564
00:47:08,080 --> 00:47:11,820
really you can't install other screen readers on the iPhone, for example.

565
00:47:11,820 --> 00:47:16,240
So Apple was able to get that to work much more consistently.

566
00:47:16,240 --> 00:47:22,300
I mean, that's one simple example.  I think that's something Microsoft still needs to continue working on,

567
00:47:22,300 --> 00:47:27,720
is that Narrator which is the screenreader they ship on their platform, needs to be a full-featured screenreader.

568
00:47:27,720 --> 00:47:30,140
It should be able to be able to fully implement it.

569
00:47:30,140 --> 00:47:31,240
That's one.

570
00:47:31,240 --> 00:47:35,860
And I think it's really just taking on mobile.

571
00:47:35,860 --> 00:47:41,360
I think it's really just the end-to-end, makes interfaces simpler, easier to use.

572
00:47:41,360 --> 00:47:46,000
I look at the accessibility SDK from Microsoft.

573
00:47:46,000 --> 00:47:48,000
It's got a lot more options in it,

574
00:47:48,000 --> 00:47:52,960
but it was trying to support a lot more functionality that's available on the desktop.

575
00:47:52,960 --> 00:47:58,380
And so mobile I think you could still say Apple is not necessarily as great on the desktop for accessibility

576
00:47:58,380 --> 00:48:02,760
as Microsoft is. But on mobile, Apple did so much more.

577
00:48:03,560 --> 00:48:07,580
And, also, to ding Microsoft on the Windows phone, that shipped without accessibility.

578
00:48:07,580 --> 00:48:09,080
That's a huge embarrassment.

579
00:48:09,080 --> 00:48:15,620
That's not ... no new technology should ship without an accessibility implementation.

580
00:48:15,620 --> 00:48:19,600
And so Apple is shown with the watch and the TV that we are really committed.

581
00:48:19,600 --> 00:48:24,920
I think they have really, I think, won that argument that no one should be releasing products

582
00:48:24,920 --> 00:48:26,760
that don't have accessibility built in.

583
00:48:26,760 --> 00:48:29,020
So other companies should follow and do that.

584
00:48:37,160 --> 00:48:41,340
[Attendee]: You talked about other things where you are working with UI controls and things like that.

585
00:48:41,340 --> 00:48:44,900
How would you say for Open GL for a game,

586
00:48:44,900 --> 00:48:49,400
are there ways you can still utilize the operating system's built-in features?

587
00:48:50,380 --> 00:48:51,740
[Thomas]: I think that's a good question.

588
00:48:51,740 --> 00:48:57,920
That's a little bit where I was going with talking about the virtual reality stuff.

589
00:48:58,700 --> 00:49:01,880
You know, unfortunately there's not like these primitives or elements.

590
00:49:01,880 --> 00:49:06,000
I mean, if I look at Unity in building an application in that interface,

591
00:49:06,000 --> 00:49:10,800
they do have the elements and objects we could add properties on.

592
00:49:10,800 --> 00:49:16,160
I think in OpenGL we would have to almost build that structure yourself.

593
00:49:16,160 --> 00:49:22,760
I don't think there is the higher level tree or, like, set of elements you can add those objects on to.

594
00:49:23,560 --> 00:49:27,940
I mean, that's something I don't actually know a ton about the OpenGL development space.

595
00:49:27,940 --> 00:49:30,700
But there should be. I mean, that's the point.

596
00:49:30,700 --> 00:49:35,920
Like, any developer environment, so I had just pick on Unity because that's the one I'm most familiar with,

597
00:49:36,520 --> 00:49:41,540
there should be a way in Unity to set accessibility attributes and add that information.

598
00:49:41,540 --> 00:49:46,980
It shouldn't all be on developers to build the underlying backend.

599
00:49:47,240 --> 00:49:50,880
I do think that's most of the way games have been made accessible in the past,

600
00:49:50,880 --> 00:49:56,900
is that people build up just like a structure that maps to the game and almost like it's hidden behind the game.

601
00:49:56,900 --> 00:50:02,220
And they have had to basically just rebuild the whole interface from scratch.

602
00:50:04,580 --> 00:50:09,100
[Dennis]: We have time for one more question, if there is one more.

603
00:50:14,100 --> 00:50:22,200
[Attendee]: If we're talking about preaching the Apple accessibility, what do you think needs to be done?

604
00:50:23,880 --> 00:50:34,120
Developers usually think of accessibility as something rather second rate. [Indiscernible]

605
00:50:34,480 --> 00:50:36,520
[Thomas]: Lots of different ideas.

606
00:50:36,520 --> 00:50:43,660
I guess one idea that I think is a community, making sure that we either file bugs

607
00:50:43,660 --> 00:50:49,380
or add on to bugs that have been filed, I mean, I know that a lot of companies,

608
00:50:49,380 --> 00:50:52,360
they have people that work for a company.

609
00:50:52,360 --> 00:50:57,120
But if people aren't presenting it as a problem or logging things as a problem,

610
00:50:57,120 --> 00:51:02,580
then they don't have anything to go to their executive team or management team to say, hey, this is a problem.

611
00:51:02,580 --> 00:51:07,700
So definitely one is that I think if you are working in the capacity where you find bugs,

612
00:51:07,700 --> 00:51:11,740
like you log them on to people that are responsible.

613
00:51:12,280 --> 00:51:18,640
I think the other one is just making sure that if you are building components, UI libraries,

614
00:51:18,640 --> 00:51:24,000
that if you really make your library very accessible, advertise that.

615
00:51:24,000 --> 00:51:29,060
Make the community know. Like, let Accessibility Chicago, Accessibility New York know.

616
00:51:29,060 --> 00:51:35,220
As Dennis mentioned, I do the New York Meetup. There's meetups like this all over the US and now the world.

617
00:51:35,680 --> 00:51:41,140
I think as a grass-roots community, really evangelizing the things that do accessibility well

618
00:51:41,140 --> 00:51:47,020
and using them on our own projects, that's one way we can strengthen them and support them.

619
00:51:49,480 --> 00:51:50,580
[Dennis]: Thank you very much.

620
00:51:50,580 --> 00:51:51,280
[Thomas]: Thank you.

621
00:51:51,280 --> 00:51:56,400
[Applause]

