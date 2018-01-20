# Standards, Design Patterns, ARIA and more 
## Seth M Kane - Wednesday, March 16, 2016
[Source recording](https://www.youtube.com/watch?v=jh5X64XMQYk)

1
00:00:01,420 --> 00:00:07,260
[Dennis] And we're live. And with that, I shall turn it over to Seth and his presentation.

2
00:00:07,260 --> 00:00:12,780
[Seth] So, again, my name is Seth Kane, technology lead at Critical Mass

3
00:00:12,780 --> 00:00:18,280
I'm going to be talking about standards, design patterns and ARIA, and a little bit more

4
00:00:18,280 --> 00:00:23,180
Just to give you a little preface to what this is going to be about

5
00:00:23,180 --> 00:00:31,100
because I'm very technical, it's not going to be about that. I want this presentation to be engaging,

6
00:00:31,100 --> 00:00:35,940
and thought provoking, so if there is any time you have a question or you want to provide some

7
00:00:35,940 --> 00:00:41,320
feedback or  comments or whatever, I strongly encourage you to raise your hand or interrupt

8
00:00:41,320 --> 00:00:50,940
but my goal for this is for you as individuals interested in accessibility to really start thinking about this rather than

9
00:00:50,940 --> 00:00:58,800
in your own discipline, but in a multi-discipline and more engaging effort to broaden your knowledge and your

10
00:00:58,800 --> 00:01:06,600
way to communicate the importance of this in various areas, so with that I will start with

11
00:01:07,800 --> 00:01:16,060
Standards. So, I don't know if you can read that in the back, I wasn't expecting a thirty-foot table

12
00:01:16,060 --> 00:01:21,140
but, basically standards is something set up and established by an authority as a rule

13
00:01:21,140 --> 00:01:29,200
for the measure of quantity, weight, extent, value and quality, and I emphasize quality

14
00:01:29,200 --> 00:01:36,540
I want us all to think about the beginning part of this presentation as more common elements

15
00:01:36,540 --> 00:01:43,300
in our real world, and how we can apply simple understandings of standards to

16
00:01:43,300 --> 00:01:46,800
accessibility, and other things as well.

17
00:01:46,800 --> 00:01:52,520
So, some examples. Standards can be found in almost every area of our daily lives

18
00:01:52,520 --> 00:02:00,340
Some obvious ones, are like stop lights. Just about every stop light in the world works and looks and behaves

19
00:02:00,340 --> 00:02:08,900
in the exact same way. In some countries, they flip them left to right, but really its either top to bottom, left to right

20
00:02:08,900 --> 00:02:17,060
and that's why the color isn't necessarily irrelevant, because the red is always either at the top or on the left

21
00:02:17,060 --> 00:02:20,200
and that's a standard that is being followed internationally.

22
00:02:20,200 --> 00:02:25,260
Turning signal levers, I don't know if you have ever thought about it, but where is your turn signal lever

23
00:02:25,260 --> 00:02:31,220
in your car? Raise the hand that you use to turn your turn signals on or off.

24
00:02:37,520 --> 00:02:45,440
So most cars are on the outside of the steering wheel, unless it's an internationally, kind of type car

25
00:02:45,440 --> 00:02:50,300
so like, cars that might be sold in both markets, they might be changed, but that's another standard that

26
00:02:50,300 --> 00:02:56,100
usually all car manufacturers will follow for usability purposes and things like that.

27
00:02:56,140 --> 00:03:02,580
Nuts and bolts is an obvious one. Like lefty loosey, righty tighty. Now, there aren't very many

28
00:03:02,580 --> 00:03:06,660
examples out there of nuts and bolts that don't follow that standard so to speak

29
00:03:06,660 --> 00:03:11,680
and I would imagine that we could probably sit here for days and talk about various other ones

30
00:03:11,680 --> 00:03:16,560
but those are some common elements, some things that the rules are really never broken

31
00:03:16,560 --> 00:03:20,160
its just things that occur in our everyday lives.

32
00:03:20,600 --> 00:03:24,500
And with that note, are there web standards?

33
00:03:25,100 --> 00:03:30,460
Well obviously, the answer is yes. Right? We all know that there is various ones

34
00:03:30,460 --> 00:03:34,300
and some might be known and some might not be known so just a quick reference

35
00:03:34,300 --> 00:03:40,480
like the W3C, that's basically the organization that sets all the browser standards

36
00:03:40,480 --> 00:03:45,000
some of the code standards and, that we work with every day.

37
00:03:45,000 --> 00:03:51,800
There's a less known one, I don't even know how they pronounce it, so I'm just going to call it

38
00:03:51,800 --> 00:03:58,920
the Web Hypertext Application Technology Working Group. They basically contribute to the W3C.

39
00:03:58,920 --> 00:04:04,860
They're like the workhorses of the W3C. They'll like, actually say "Hey, we want to do something different"

40
00:04:04,860 --> 00:04:10,980
and they'll start really investigating different types of things and determine if it can or can't be a standard

41
00:04:10,980 --> 00:04:14,100
and then present those ideas to the W3C.

42
00:04:14,100 --> 00:04:21,840
ISO, which is not really a web standard but its more of an internationally acclaimed, large, organizational standard

43
00:04:21,840 --> 00:04:29,240
if anybody has heard of ISO 9000 or 9001, some corporations, I'm guessing like United

44
00:04:29,240 --> 00:04:35,820
lives and breathes by that type of thing and those standards can be actually applied to web technologies

45
00:04:35,820 --> 00:04:40,760
and processes and things like that as well, the ADA, Ecma, Section 508

46
00:04:40,760 --> 00:04:45,860
and there's probably a bizillon more and so forth.

47
00:04:47,280 --> 00:04:50,840
So, let's ask why standards?

48
00:04:50,840 --> 00:04:57,120
I looked this up. And basically the dictionary definition more or less, or what I found was a common

49
00:04:57,120 --> 00:05:04,980
term for why ... to answer this question was, it provides a common language.

50
00:05:04,980 --> 00:05:10,400
Right? It sets expectations and enables compatibility. And the first thing that comes to my mind

51
00:05:10,400 --> 00:05:17,720
when I think of that rule of thumb is like electricity and outlets and things like that

52
00:05:17,720 --> 00:05:23,220
Even though that each country they have different types of things but the basic common principles

53
00:05:23,220 --> 00:05:27,100
of the standards are, there's a positive, there's a negative, there's a ground

54
00:05:27,100 --> 00:05:32,340
all of those types of things. It never really deviates. And what that does, that provides

55
00:05:32,340 --> 00:05:38,640
the institutional of common language to know how to build something or know how to work something or

56
00:05:38,640 --> 00:05:43,300
or how to integrate it with the most amount of compatibility.

57
00:05:43,300 --> 00:05:50,000
Just imagine if we didn't have standards, what type of house you might live in,

58
00:05:50,000 --> 00:05:54,740
or what type of car you might drive in, or various other types of things.

59
00:05:54,740 --> 00:06:01,160
So, really, this is so important to understand, and how it can relate to what we do

60
00:06:01,160 --> 00:06:08,160
whether you're in content or user experience, or development, those standards should be treated as like

61
00:06:08,160 --> 00:06:11,120
the rules, right? And we shouldn't deviate from that.

62
00:06:11,120 --> 00:06:17,260
And if you were to take away anything from this presentation, it really is basically this.

63
00:06:18,900 --> 00:06:22,580
So with standards, becomes design patterns.

64
00:06:23,240 --> 00:06:28,280
Design patterns are reoccurring solutions that solve common design problems, right?

65
00:06:28,660 --> 00:06:32,320
So, go back to the electricity thing, like an outlet or whatever. Like a plug.

66
00:06:32,320 --> 00:06:35,780
Like , that follows a specific design pattern.

67
00:06:35,780 --> 00:06:43,240
I'm not talking about actually the plug itself, but, you plug it in, and it goes on, and you unplug it, and it turns off.

68
00:06:43,240 --> 00:06:47,880
Right? That's basically a foundational pattern, in the most simplest terms.

69
00:06:47,880 --> 00:06:53,060
Right? Things like, other real life examples would be

70
00:06:53,060 --> 00:06:56,260
like streets. Think about it. A street.

71
00:06:56,260 --> 00:07:01,000
Whether they're in a rural setting or an urban setting, they inherently are made and act and behave

72
00:07:01,000 --> 00:07:06,460
the same exact way. You know, there's left turns, right turns, straights, swervey roads

73
00:07:06,460 --> 00:07:13,340
but there's really no major deviations from a particular pattern or how to create and how to leverage

74
00:07:13,340 --> 00:07:16,160
and work in a street environment.

75
00:07:16,160 --> 00:07:22,120
Another one is buildings or houses. Houses and skyscrapers. They basically follow

76
00:07:22,120 --> 00:07:26,660
the same fundamental building process
 or design pattern.

77
00:07:26,660 --> 00:07:32,140
They first, a foundation, then they go to the frame, then they go to the roof,

78
00:07:32,140 --> 00:07:38,900
and they go from there. You can't build a house without starting at the foundation.

79
00:07:38,900 --> 00:07:44,880
It just won't last. So the pattern to follow is, you understand how it's built, how it's used,

80
00:07:44,880 --> 00:07:50,980
how it matches up with those standards that are incorporated into the design pattern and so forth.

81
00:07:51,640 --> 00:07:57,260
This is my favorite one. And I"m hoping that with the next couple of slides, you'll all agree with me.

82
00:07:57,260 --> 00:08:03,400
But, doors, right? So there's many ways to get in and out of a building. But think about it.

83
00:08:03,400 --> 00:08:09,840
Ok, how do you use a door knob? It's the same way. It's either you turn it or you pull it up or down,

84
00:08:09,840 --> 00:08:16,160
you either push or pull to get in. There's different particular solutions to different particular types.

85
00:08:16,160 --> 00:08:21,840
But really, across the board, it's the same way. 
Every single type of door.

86
00:08:21,840 --> 00:08:27,020
Until, you get to, well, this is the door.
So the standard door.

87
00:08:27,020 --> 00:08:32,240
So you would open this by either pushing or pulling, right? And then if there was maybe the bar across

88
00:08:32,240 --> 00:08:36,480
you know, horizontal, you'd push or pull or you'd turn a knob or whatever.

89
00:08:36,480 --> 00:08:42,000
But then came the idea of, how do we improve a particular design pattern

90
00:08:42,000 --> 00:08:46,820
like take a door. Is there a better way to do this. Is there a more efficient way to do this.

91
00:08:47,380 --> 00:08:53,160
So, someone came up with this idea. Right? So this is one of those revolving doors.

92
00:08:53,160 --> 00:08:58,640
And even though there are two design patterns, push pull or go around,

93
00:08:59,080 --> 00:09:05,920
this basically is a behavior that is disseminated out, you learn it, you train it, you know

94
00:09:05,920 --> 00:09:10,520
when you walk up to one of these things, do you ever question which way to go in?

95
00:09:10,520 --> 00:09:16,020
Or how to wait for the next person to come out? Because the pattern is a solution to

96
00:09:16,020 --> 00:09:22,060
the problem of getting in. Now this pattern is basically been enhanced from the other one.

97
00:09:22,060 --> 00:09:26,140
Some of the things that it does, maybe simpler to use.

98
00:09:26,620 --> 00:09:32,680
It's faster. You don't necessarily have roadblocks. It's also energy efficient

99
00:09:33,780 --> 00:09:38,480
So there's other things that you may be solving for on this particular design pattern

100
00:09:38,480 --> 00:09:42,540
that might also cause problems. Can anyone think of a problem with these things?

101
00:09:44,200 --> 00:09:44,980
What?

102
00:09:44,980 --> 00:09:45,740
[Attendee]: Wheelchair

103
00:09:45,760 --> 00:09:49,880
[Seth]: Right, wheelchair, or you try to being your luggage through, it's difficult, right?

104
00:09:49,880 --> 00:09:57,820
So upon a design pattern as innovators of various industries and things we try to evolve

105
00:09:57,820 --> 00:10:00,800
and make those design patterns better, right?

106
00:10:00,800 --> 00:10:03,600
So what happens if we change the design pattern?

107
00:10:05,580 --> 00:10:07,800
Hopefully, everybody nods their head.

108
00:10:08,440 --> 00:10:10,160
Have you ever run into one of these?

109
00:10:10,780 --> 00:10:13,940
Especially at like IKEA. Right, that's the big one that I always run into.

110
00:10:14,540 --> 00:10:23,640
So this is the next evolution of the resolving door design pattern. But, have you ever walk through one of these

111
00:10:23,640 --> 00:10:25,620
and had a problem with how it works?

112
00:10:26,800 --> 00:10:28,900
You're shaking your head ... what's the problem with it?

113
00:10:29,600 --> 00:10:47,240
[Attendee] Well, uh, first of all, ... [mumble]

114
00:10:47,240 --> 00:10:52,860
[Seth] Right, so I have had a similar experience. I want to go through it faster, I've seen, a thousand times,

115
00:10:52,860 --> 00:10:57,860
people pushing on it. And all of a sudden it stops because it thinks its an emergency push

116
00:10:57,860 --> 00:11:05,620
that actually executes the emergency brake of it. So this design pattern was evolved

117
00:11:05,620 --> 00:11:11,540
but it might not have actually been thought through or it might not have been disseminated well enough

118
00:11:11,540 --> 00:11:17,700
to actually educate people to know how to use it. So they have to stick these little yellow things on there

119
00:11:17,700 --> 00:11:21,260
and say it's automatic. Don't push. Right?

120
00:11:21,260 --> 00:11:27,720
So one could argue that, this is a new, innovative way to think, or do something.

121
00:11:27,720 --> 00:11:35,020
But maybe it didn't follow the native pattern of what it is that we are accustom to or what we want to do.

122
00:11:35,020 --> 00:11:38,420
Now I'm guessing over a period of time, these will become more popular,

123
00:11:38,420 --> 00:11:44,920
and people will learn how to use them, but think about what we do in our businesses

124
00:11:44,920 --> 00:11:49,680
and we try to do something new, or we're innovative or we change the pattern,

125
00:11:50,140 --> 00:11:55,420
you end up with something like this. And I guessing everybody has had a problem at one point or another

126
00:11:55,420 --> 00:11:57,080
with this particular design

127
00:11:57,560 --> 00:12:01,380
[Attendee]: [mumble]

128
00:12:01,680 --> 00:12:05,900
[Seth] True. But on the other hand, people with luggage and wheelchairs could actually go through them, right?

129
00:12:05,900 --> 00:12:09,180
So, they might be solving one problem
but creating another

130
00:12:09,180 --> 00:12:16,540
And those are the types of thought provoking things that as innovators or user experience or content strategists

131
00:12:16,540 --> 00:12:22,260
or developers that you have to think through. And the best way to think through that is kind of like

132
00:12:22,260 --> 00:12:25,560
through, first the standards and then with patterns.

133
00:12:26,700 --> 00:12:30,120
So how does this relate to inclusive design
and accessibility?

134
00:12:32,860 --> 00:12:35,900
Well, before we answer that, let's test ourselves.

135
00:12:36,140 --> 00:12:40,120
So, I've come up with some common things that I'm guessing we all do.

136
00:12:40,500 --> 00:12:42,420
That we can probably all answer.

137
00:12:42,420 --> 00:12:45,340
How do we open a new page on our computer
like through our browser?

138
00:12:47,360 --> 00:12:47,880
[Attendee] Tab

139
00:12:47,880 --> 00:12:48,760
[Seth] What?

140
00:12:49,260 --> 00:12:49,960
Tab or ...

141
00:12:50,900 --> 00:12:55,480
Command T, that opens a tab. Command U or Control U, depending on whether you're on a Mac or PC

142
00:12:56,100 --> 00:13:01,100
How do you quit a program? You know, Apple Q, or Windows Q or whatever.

143
00:13:01,400 --> 00:13:03,080
These are things that are very very common, you know,

144
00:13:03,100 --> 00:13:06,180
which button on a mouse do we use to select something?

145
00:13:07,020 --> 00:13:11,640
The left one, right? We know that. Even on our touch pad, it's a totally different design pattern

146
00:13:12,000 --> 00:13:17,100
but it uses the same basic standards
to mimic a similar pattern.

147
00:13:17,300 --> 00:13:22,280
Right, how do we make something bold using the keyboard? Control B, right?

148
00:13:22,280 --> 00:13:28,340
So basically, our industry or computers itself have set forth some examples of common things

149
00:13:28,340 --> 00:13:34,740
that they've vetted through, that they know they work and they know that people know how to use it

150
00:13:34,740 --> 00:13:40,340
and you really don't have to train for it. You might actually like hover over the little B in Microsoft Word

151
00:13:40,340 --> 00:13:44,900
and it'll tell you how to do it. And then for the next time you'll know that it's going to come up, right?

152
00:13:45,020 --> 00:13:47,140
How do we navigate a web page?

153
00:13:47,460 --> 00:13:53,500
You know, like, this one, to me, is simple, but, do people that don't do what we do know this?

154
00:13:53,500 --> 00:13:57,500
They use the mouse, right? 
But how do you do it without the mouse?

155
00:13:57,500 --> 00:14:03,540
Do they know the standards, the base practices of navigating a website, you know, with it?

156
00:14:03,540 --> 00:14:06,900
You know, how do we use a module component? We're not going to answer that one because

157
00:14:06,900 --> 00:14:11,700
there is no in-depth example, but, like, think about the next time you design something

158
00:14:11,700 --> 00:14:17,660
or you build something. Is your module or component so intuitive that it

159
00:14:17,660 --> 00:14:22,880
follows the standards and design patterns, so they know right away how to use it?

160
00:14:22,880 --> 00:14:25,380
They don't even have to think about it.

161
00:14:25,380 --> 00:14:31,340
So, if we didn't follow standards and pattens, accessibility would be very difficult.

162
00:14:31,340 --> 00:14:33,480
I was kind of being PC with that.

163
00:14:33,480 --> 00:14:41,460
It would be, in my opinion, nearly impossible, right? So let's get some examples of how to

164
00:14:41,460 --> 00:14:48,700
make our work more accessible by following the standards and design patterns

165
00:14:48,700 --> 00:14:52,220
and here are some simple steps that we should follow.

166
00:14:52,220 --> 00:14:58,340
So, even though I am in technology, and most people in accessibility think that accessibility is

167
00:14:58,340 --> 00:15:05,040
a byproduct of the technology implementation portion of the project, but I believe it is the opposite

168
00:15:05,040 --> 00:15:09,080
It actually should follow the same methodologies of building a house.

169
00:15:09,080 --> 00:15:12,720
It should start at the foundation, the blueprints, right?

170
00:15:12,720 --> 00:15:19,280
You have to vet to make sure that everything that is going to be proposed or that you are going to experience

171
00:15:19,280 --> 00:15:21,740
or interact with is accessible.

172
00:15:21,740 --> 00:15:27,680
I believe in asking the right questions, and the first place that I do it at is talk through the experience.

173
00:15:27,680 --> 00:15:36,120
So when I sit down with user experience folks, I basically ask them to explain the experience

174
00:15:36,120 --> 00:15:40,040
in layman's terms, not in technical, design details.

175
00:15:40,040 --> 00:15:44,060
It like, what do you want them to do? How do you want them to interact with it?

176
00:15:44,060 --> 00:15:48,880
An example would be, the user will move their mouse and hover over a call to action

177
00:15:49,540 --> 00:15:54,260
then they click the call to action, upon clicking the call to action, maybe a modal appears

178
00:15:54,260 --> 00:15:59,460
you know, the user will interact with that modal, right, and then when they decide to close the modal,

179
00:15:59,460 --> 00:16:00,600
they'll move on.

180
00:16:01,180 --> 00:16:07,020
So that's the interaction. But how does that actually get translated into what it is that we are doing?

181
00:16:07,380 --> 00:16:14,620
So those are the questions that I will engage with people to make sure that they're actually able to explain it to me

182
00:16:14,620 --> 00:16:19,160
in the most simplest terms. A modal or call to action is fairly simple,

183
00:16:19,160 --> 00:16:26,580
so let's just hypothetically talk about something like a new, you know, way to navigate,

184
00:16:26,580 --> 00:16:34,180
or add to cart, or shop or drag and drop, whatever it could be, can they explain the experience

185
00:16:34,180 --> 00:16:36,520
to me in the most simplest terms.

186
00:16:36,520 --> 00:16:42,180
Those will usually lead to things that tell us to design patterns and standards.

187
00:16:42,180 --> 00:16:45,660
Then I basically say, okay so now we've got the experience explained out,

188
00:16:45,660 --> 00:16:52,100
from more of a foundational point of view, I'll go to kind of like the decorating or the design elements.

189
00:16:52,100 --> 00:16:57,180
So I would likely sit down with the design team at that point, and  basically, I would ask them

190
00:16:57,180 --> 00:17:03,400
we expect designers to, you know, get creative, get like blue style, they want to be the most innovative

191
00:17:03,400 --> 00:17:10,660
they want to be the most creative folks. But it's important for them in particular to understand

192
00:17:11,280 --> 00:17:15,400
the feature or the intent, in addition to what it looks like.

193
00:17:15,400 --> 00:17:21,160
So my example is, this designer wants to use a switch, right, like an on off kind of like toggle

194
00:17:21,160 --> 00:17:26,600
you've seen them on mobile devices all the time, but they might not fully understand,

195
00:17:26,600 --> 00:17:31,600
both technically and experience what that switch actually is.

196
00:17:31,600 --> 00:17:36,920
Does everybody, can they visualize an on off like switch toggle like right?

197
00:17:37,820 --> 00:17:44,080
Most, I would say, probably on the record like 90 plus percent of the time, a switch is a boolean,

198
00:17:44,080 --> 00:17:50,020
right? In technical terms, an on or off, yes or no, true or false, right? Zero or one.

199
00:17:50,420 --> 00:17:55,720
And in that case, most times when you are switching, with those terms in play,

200
00:17:55,720 --> 00:18:01,360
you're actually using a form, or you're submitting data, a yes no answer response

201
00:18:01,660 --> 00:18:08,100
So it's checkbox, it's a simple checkbox, right? So if the designer doesn't know the intent of it

202
00:18:08,100 --> 00:18:11,120
of how it is going to be implemented or how it's going to be interacted with,

203
00:18:11,120 --> 00:18:19,280
they may design an on off switch that might not work the same way a checkbox would work

204
00:18:19,280 --> 00:18:23,780
and that's a big problem. And we've probably seen it a thousand times.

205
00:18:24,120 --> 00:18:29,340
Then we come to the technical aspect of it. And it's like do we understand the implementation?

206
00:18:29,480 --> 00:18:36,040
So, developers can read documentation and they can learn all the W3C standards and things like that.

207
00:18:36,260 --> 00:18:42,360
But, it's often that the developer looks at like a set of wires or a Photoshop document

208
00:18:42,360 --> 00:18:47,920
and then just goes off and builds something, right, and understanding the design pattern to follow and the intent

209
00:18:47,920 --> 00:18:55,740
of the design element is the key to successfully executing it with accessibility in mind.

210
00:18:56,120 --> 00:19:03,820
So, take the switch, right?
So like how do they implement the design

211
00:19:04,660 --> 00:19:11,580
but as a radio or a checkbox? Or how do they create this new fancy like custom dropdown,

212
00:19:11,580 --> 00:19:19,620
like simple state selection UI, but they want it fancy with flags or with you know

213
00:19:19,620 --> 00:19:24,760
borders or whatever like we can implement that, but if it doesn't follow the standards and

214
00:19:24,760 --> 00:19:28,600
if it doesn't follow the design patterns,
you won't be able to use it.

215
00:19:29,040 --> 00:19:32,860
And most actual backends won't be able to consume it.

216
00:19:33,400 --> 00:19:38,780
So it's really important for the developers to not just consume the documentation

217
00:19:38,780 --> 00:19:45,580
but to understand the intent, standards and the design patterns, because that's where they will know

218
00:19:45,580 --> 00:19:51,300
which tags to use, which ARIA,
things like that and so forth.

219
00:19:51,300 --> 00:20:00,620
I wanted to show you some examples of where, I think, the industry at large has missed and has done well.

220
00:20:00,620 --> 00:20:07,240
Ok, so this is a little video. So hopefully you can kind of see it. You'll see my mouse move.

221
00:20:07,440 --> 00:20:12,880
This is an example of a bad modal pattern. And just so I can throw them under the bus,

222
00:20:12,880 --> 00:20:19,500
this is jQuery modal dot com. So, number one in the search results, right?

223
00:20:19,500 --> 00:20:25,040
So what you'll see here is, I'm tabbing, so I'm using the keyboard to go between links

224
00:20:25,040 --> 00:20:30,220
and I click that call to action and its really hard to see because the screen is so dark, but

225
00:20:30,220 --> 00:20:36,680
when it opens again, I'm tabbing, and I'm actually tabbing the page links, not the modal links.

226
00:20:36,680 --> 00:20:43,460
So I can't actually interact with the modal at all. It's completely inaccessible.

227
00:20:43,920 --> 00:20:49,460
So it doesn't follow either the standards or the design patterns, which I'll get into a little bit later.

228
00:20:50,360 --> 00:20:52,440
[Attendee] Sorry I'm not clear

229
00:20:52,600 --> 00:20:55,180
[Seth] Ok, I"m going to show you really quick.

230
00:20:55,400 --> 00:20:59,660
So I'm using a keyboard only to get to this. And I click enter.

231
00:21:00,000 --> 00:21:06,040
And it's really dark, but what you'll see is once the modal opens,  you'll see that it's moving in the background.

232
00:21:06,480 --> 00:21:10,540
But I'm not able to interact with the components
within the modal

233
00:21:10,540 --> 00:21:17,860
like I can't actually click the close button and I can't click the blue call-to-action inside the modal, the close.

234
00:21:18,140 --> 00:21:19,420
So, making that modal...

235
00:21:19,420 --> 00:21:20,120
[Attendee] keyboard

236
00:21:20,120 --> 00:21:21,480
[Seth]Correct  [Attendee] OK

237
00:21:21,480 --> 00:21:25,580
So someone with a visual disability in particular needs to use a keyboard

238
00:21:25,580 --> 00:21:33,520
but someone, let's say, with Parkinson's, they may not be using a mouse because of you know, motor disabilities

239
00:21:33,520 --> 00:21:37,640
and they'll force themselves, more structurally,
to use the keyboard.

240
00:21:37,640 --> 00:21:41,860
So, this particular modal, if you implemented this
on your website,

241
00:21:41,860 --> 00:21:46,820
it would be completely unaccessible to people with disabilities.

242
00:21:47,620 --> 00:21:52,400
On the other hand, I found a good one, which believe it or not is Bootstrap,

243
00:21:52,400 --> 00:21:55,800
so, this is the call to action, and you'll notice

244
00:21:55,900 --> 00:21:59,280
now i'm actually interacting with the element in the model

245
00:22:00,080 --> 00:22:04,820
now can you see I'm tabbing the same type of thing but once i'm open

246
00:22:04,820 --> 00:22:09,940
I'm now forced inside the model and I have to make a decision

247
00:22:09,940 --> 00:22:12,360
to either act on it or close it

248
00:22:12,360 --> 00:22:15,520
so this is a actual good design path

249
00:22:15,620 --> 00:22:20,740
so basically  you tab to the call to action, you click or enter to open it

250
00:22:20,740 --> 00:22:24,520
you focus on the model which is the blue ring around the white box

251
00:22:24,520 --> 00:22:29,280
you click tab, your tab lock aside and you can either close the model

252
00:22:29,320 --> 00:22:30,680
or return to your call to action

253
00:22:30,680 --> 00:22:36,520
That's the other key feature to, is when you close it, you return back to where you came from

254
00:22:36,520 --> 00:22:39,540
unrecognisable chatter

255
00:22:39,540 --> 00:22:44,420
... a good design pattern with regards to a modal. Ok.

256
00:22:45,420 --> 00:22:53,300
So let's look at some , you know, some more examples. So what I want to do here quickly

257
00:22:53,320 --> 00:22:57,740
if this works is I'm gonna switch to my browser,  which I did

258
00:22:57,760 --> 00:23:01,320
Ok [Dennis] Oh, That part is not straight

259
00:23:01,400 --> 00:23:08,500
[Seth] Ohhhh, really, even if I don't, if I share the hangout? Where's my hangout?

260
00:23:08,500 --> 00:23:10,580
Maybe I need to share ...

261
00:23:11,080 --> 00:23:14,820
[Dennis] Yeah, again I think ...

262
00:23:15,500 --> 00:23:18,780
Ok, but I'm gonna to move this over so you don't see it twice.

263
00:23:22,520 --> 00:23:27,920
So, this is an example of actually, the W3C, they link to this ...

264
00:23:27,920 --> 00:23:32,000
but this is like a tooltip so let me go back here really quickly.

265
00:23:32,000 --> 00:23:35,220
So a tool tip, so according to ...

266
00:23:38,540 --> 00:23:40,940
Alright, maybe I won't change ...

267
00:23:47,300 --> 00:23:50,940
... change screens ... technical difficulties ...

268
00:24:03,320 --> 00:24:10,020
Ok, well, this is the wrong screen but that's alright, that's ok well we'll stick with this for now

269
00:24:10,020 --> 00:24:15,420
[Dennis]well, yeah, unfortunately I think it's looping on to itself

270
00:24:18,060 --> 00:24:21,100
Yeah,  that's a issue with Hangout

271
00:24:28,640 --> 00:24:32,420
Ok. Well now you see my notes but that's ok ...

272
00:24:32,440 --> 00:24:34,840
[Dennis] Those are not shared, your site notes

273
00:24:34,840 --> 00:24:35,940
[Seth] right

274
00:24:35,940 --> 00:24:37,200
[Dennis] Oh here they are but not ...

275
00:24:37,200 --> 00:24:37,840
[Seth] Right.

276
00:24:37,840 --> 00:24:43,980
Ok, so basically this is ... according to the W3C, at the bottom here I linked to it

277
00:24:43,980 --> 00:24:48,460
and this particular, you know, example is with, you know, tooltips

278
00:24:48,460 --> 00:24:52,560
so a tooltip is like if you hover on something you get a real dialog of sorts, so

279
00:24:52,560 --> 00:24:56,820
a popup that displays a description for an element when the user passes over

280
00:24:56,820 --> 00:25:01,680
or rests on the element, supplements to a normal tooltip, blah blah blah ...

281
00:25:01,700 --> 00:25:06,080
but here's the key, right, so the triggering element to which the tooltip is attached

282
00:25:06,080 --> 00:25:12,680
link should never actually lose input or focus. So accordingly to the W3C for a tooltip

283
00:25:12,680 --> 00:25:17,180
there's a rule to be followed. Right? And the next one is if the tooltip

284
00:25:17,180 --> 00:25:20,820
is invoked when the trigger element gets focused then it should be dismissed

285
00:25:20,820 --> 00:25:22,620
when it no longer has focus.

286
00:25:22,620 --> 00:25:26,800
So those are things that user experienced people need to know

287
00:25:27,000 --> 00:25:30,200
and developers need to know when their actually like saying hey

288
00:25:30,440 --> 00:25:35,180
this is what it is that I'm going to represent, so, let me try and switch here

289
00:25:35,540 --> 00:25:37,660
I know I might have to go back ...

290
00:25:38,020 --> 00:25:44,260
hold on ... you can see that, now I'm going to become an expert at this soon

291
00:25:44,260 --> 00:25:45,000
[Dennis] [Laugh]

292
00:25:45,000 --> 00:25:48,060
[Seth] You think ... if I can find my hangout ...

293
00:25:51,380 --> 00:25:57,700
... thats cool. I think ... two screens ... Ok, this will help

294
00:26:01,940 --> 00:26:05,540
This is was actually my intention on how I would fill up time ...

295
00:26:05,540 --> 00:26:08,360
[Dennis] [Laugh] ... good job ...

296
00:26:08,360 --> 00:26:16,220
[Seth] Ok, so we're sharing this right? Ok, so everybody can see. So this is an example of a tooltip.

297
00:26:16,220 --> 00:26:20,000
So I mouse over this field and it says oh your first name is optional

298
00:26:20,000 --> 00:26:23,840
and I moused over another field, you know, your last name is optional

299
00:26:23,840 --> 00:26:27,940
and it disappears. If I'm in the box it stays there, if I leave the box

300
00:26:27,940 --> 00:26:31,440
technically, oh my mouse is still there.

301
00:26:31,440 --> 00:26:37,300
So when I switch between these, these tooltips are showing and hiding according to the spec.

302
00:26:37,300 --> 00:26:43,440
So this is key so when someone goes and reinvents the wheel or thinks of another way to do it

303
00:26:43,520 --> 00:26:48,700
the best place for everybody to start is is back at the design pattern

304
00:26:48,700 --> 00:26:53,860
and the standards. Ok, let me show you one more so I don't have to keep going back

305
00:26:53,860 --> 00:26:57,140
and forth between things so here is another one on Bootstrap

306
00:26:57,200 --> 00:27:01,760
right so if I hover it shows up on the left if I hover it shows up on the right you know whatever

307
00:27:01,840 --> 00:27:06,980
that with the mouse. If I get to this, on it here, eventually you'll see

308
00:27:06,980 --> 00:27:12,420
I'm tabbing, I'm not using my mouse and hopefully somewhere down here is a tooltip

309
00:27:18,900 --> 00:27:24,900
...this is a whole different discussion to have.
Let's see here ...

310
00:27:24,960 --> 00:27:28,500
So I should follow the thing.  Oh, here we go.

311
00:27:30,140 --> 00:27:34,060
So you'l see that I've tabbed on the tooltip on the right and I've tabbed that

312
00:27:34,060 --> 00:27:39,500
I'm on the top, the bottom, the top, left, and if I go through it shows a lot

313
00:27:39,500 --> 00:27:46,220
it's a perfect example of following spec so there's rules to be, you know, followed and so forth.

314
00:27:46,220 --> 00:27:49,000
Let me show one more.

315
00:27:49,000 --> 00:27:53,580
Another tool tip, right so if I come down to here ...

316
00:27:57,640 --> 00:27:59,440
... so it's like this guy right?

317
00:27:59,440 --> 00:28:04,240
So if I tap to these guys, it shows me, if I tap out, goes to the next one

318
00:28:04,240 --> 00:28:08,440
and so forth, so again a simple example of following the spec.

319
00:28:08,440 --> 00:28:10,060
Let's go back ...

320
00:28:12,540 --> 00:28:19,260
So were talking about like the ability to interact with it right now, but technically

321
00:28:19,260 --> 00:28:24,980
making it accessible for screen readers is a whole separate step

322
00:28:24,980 --> 00:28:29,500
so one thing I tell the people that I am auditing or

323
00:28:29,500 --> 00:28:34,820
that I say "Hey, is this accessible or not?" the number one thing I say is "go use your keyboard."

324
00:28:34,820 --> 00:28:40,200
If you can't interact with it with the keyboard, I can pretty much guarantee you're not going to be able

325
00:28:40,200 --> 00:28:41,460
to use it with a screen reader.

326
00:28:41,460 --> 00:28:44,760
So foundation again, if you can't use it with a keyboard

327
00:28:44,760 --> 00:28:47,120
you'e likely not going to be able to use it with a screenreader.

328
00:28:47,120 --> 00:28:50,340
If you can use it with your keyboard you got to go to the next level

329
00:28:50,340 --> 00:28:51,920
kind of like a video game.

330
00:28:51,920 --> 00:28:56,280
Ok, so now I got to go back to my Hangout,
which I think is over here ...

331
00:29:00,680 --> 00:29:08,820
[Attendee]:  So, the process of, it's keyboard accessible,

332
00:29:08,820 --> 00:29:17,680
means the screen reader won't get stuck inside the modal. But, it still doesn't mean the modal is usable.

333
00:29:20,740 --> 00:29:22,860
[Seth]: So are you talking about the tool tip
or the modal?

334
00:29:22,860 --> 00:29:24,860
I just want to make sure we're talking about the same thing.

335
00:29:32,100 --> 00:29:38,360
So in this case the tooltip ... so the question was again just repeat it so ...

336
00:29:38,360 --> 00:29:43,960
[Attendee]: So if not getting through it on a keyboard
is not a problem ...

337
00:30:03,020 --> 00:30:07,200
[Seth]: Not necessarily, because ... 
think about it from let's say

338
00:30:07,200 --> 00:30:11,120
someone that's forced to use a keyboard, but isn't visually impaired

339
00:30:12,660 --> 00:30:16,420
they are going to use the keyboard to navigate to something

340
00:30:16,420 --> 00:30:20,540
and they are going to want to know what that acronym is or whatever it is at the tooltip is

341
00:30:20,540 --> 00:30:24,680
and because they can't use the mouse they need to have that thing be visible.

342
00:30:26,300 --> 00:30:29,480
So that information is pertinent enough for them to access.

343
00:30:29,480 --> 00:30:34,960
[Attendee]: So, this would be ... of keyboard, ah ...

344
00:30:35,240 --> 00:30:38,980
[Seth]: Well, that's the baseline. So then you take it to the next level and someone

345
00:30:38,980 --> 00:30:44,860
is totally blind, what you would do
which is getting a little deeper

346
00:30:44,860 --> 00:30:49,420
into the later parts of the presentation is, you can add extra elements like ARIA

347
00:30:49,420 --> 00:30:55,120
that will make it ... the information, the supplemental information available verbally

348
00:30:55,120 --> 00:30:59,620
for auditory, right so

349
00:30:59,620 --> 00:31:04,500
they will never see the tooltip but they know that when they tap to it

350
00:31:04,500 --> 00:31:11,180
it says "ABC has tooltip" and it will say "ABC is a XYZ"

351
00:31:11,180 --> 00:31:16,280
or whatever, it will announce to them whatever you programmatically want to tell them.

352
00:31:16,340 --> 00:31:21,680
[Attendee]:  I just didn't know, I never tried it.

353
00:31:22,360 --> 00:31:23,780
[Seth] Makes perfect sense.

354
00:31:23,780 --> 00:31:28,840
Ok, so that was a tool tip. One more, ok  this is my favorite one.

355
00:31:31,760 --> 00:31:35,540
There's too much to read through here, 
but a date picker, right

356
00:31:35,540 --> 00:31:39,480
I'm not going to through you under the bus, but I'm going to use one of your competitors.

357
00:31:39,480 --> 00:31:43,800
Ok, so a date picker is, you have a field, right and it says

358
00:31:43,800 --> 00:31:47,300
"when do you wana leave" or "what's your birthday" or whatever

359
00:31:47,300 --> 00:31:53,140
and you tab into it and it says, oh this big magical popup says, with a calendar looking thing, right?

360
00:31:53,140 --> 00:31:59,720
Ok, so that is what a date picker is. And this goes into significant detail

361
00:31:59,720 --> 00:32:04,980
of what the spec and what the standards are, of how that date picker should

362
00:32:04,980 --> 00:32:10,240
or shouldn't work and to give you an idea, I needed two pages plus.

363
00:32:10,240 --> 00:32:14,480
I didn't even go down that. I'll read a couple of these as an example,

364
00:32:14,480 --> 00:32:19,040
so you have a good understanding. So basically, keyboard navagation

365
00:32:19,040 --> 00:32:22,660
on days that are not included on the currently displayed month

366
00:32:22,660 --> 00:32:27,540
should move to the month automatically and lead to the date in the next previous month.

367
00:32:27,540 --> 00:32:32,980
So basically when you focus in, the highlight of the component should go to today.

368
00:32:33,740 --> 00:32:38,280
Then there's like tab, like other widgets, the date picker receives focus by tabbing in,

369
00:32:38,640 --> 00:32:41,080
once focus is received, focus is repositioned on

370
00:32:41,080 --> 00:32:43,660
today's date in the grid, on the day of the week

371
00:32:43,660 --> 00:32:47,320
a second tab will take the user out of the date picker wizard

372
00:32:47,320 --> 00:32:50,480
focusing initially is placed on today's date so

373
00:32:50,480 --> 00:32:54,420
most date pickers don't follow that. I'll show you that

374
00:32:54,420 --> 00:32:58,360
when you tab and it focuses the date picker, if you hit tab again

375
00:32:58,360 --> 00:33:00,440
it might actually start tabbing through the dates

376
00:33:00,440 --> 00:33:02,920
which means you can never get out of it.

377
00:33:02,920 --> 00:33:07,040
So using something like shift tab reverses the direction of

378
00:33:07,040 --> 00:33:09,780
the tab focus or up and down arrows

379
00:33:09,780 --> 00:33:13,080
that allows you to actually pick supplemental dates ...

380
00:33:13,080 --> 00:33:15,280
...we'll get into that

381
00:33:15,280 --> 00:33:19,340
and things like that so there's a really really long list and I put down here

382
00:33:19,360 --> 00:33:23,520
which you can't see in the presentation a link to the spec that is overwhelming

383
00:33:23,520 --> 00:33:27,060
and I guarantee you that those UX people that are envisioning

384
00:33:27,060 --> 00:33:32,520
the next best date picker which most airlines are usually trying to do

385
00:33:32,520 --> 00:33:37,540
because they want an easier hotels in particular, I've gone through these conversations

386
00:33:37,540 --> 00:33:41,140
they wana make it simple and intuitive in check in check out  ya know

387
00:33:41,140 --> 00:33:45,760
departure return they want it really cool and really innovative

388
00:33:45,760 --> 00:33:48,760
but there never following the specs here so

389
00:33:48,760 --> 00:33:55,480
I can't find a single one that follows the spec and I looked

390
00:33:55,480 --> 00:34:02,660
but I did however, find some that do let's go show what

391
00:34:02,660 --> 00:34:05,720
let's get outa here and go back to my little example

392
00:34:05,720 --> 00:34:09,600
which I'm becoming expert at this now, come on

393
00:34:09,600 --> 00:34:17,880
Ok, I want share my screen ... I'm not sharing

394
00:34:20,180 --> 00:34:25,080
Let's go to this one, this fantastic one

395
00:34:25,080 --> 00:34:30,340
distributed by the largest JavaScript framework known to man basically.

396
00:34:30,340 --> 00:34:35,660
Ok, everybody starts here so I'm going to show you what it looks like

397
00:34:35,660 --> 00:34:39,720
with a mouse first so I enter in here and I get this fancy

398
00:34:39,720 --> 00:34:43,080
little date thing, I can go back and forth and you know I can

399
00:34:43,080 --> 00:34:45,580
pick the seventeenth and I can do this and all

400
00:34:45,580 --> 00:34:47,580
that kina stuff right

401
00:34:47,580 --> 00:34:51,200
but lets try to do it with a mouse ok I mean with a keyboard

402
00:34:51,200 --> 00:34:56,940
I hit tab ok and tab number one but it immediately closes.

403
00:34:56,940 --> 00:35:03,240
Ok so I hit tab, I can't use it. I hit the arrows,
I'm hitting the arrows,

404
00:35:03,240 --> 00:35:06,380
and all I am doing is cycling through you know the dates

405
00:35:07,060 --> 00:35:11,240
The actual date picker module is not accessible.

406
00:35:14,260 --> 00:35:15,620
Should we try something else?

407
00:35:18,380 --> 00:35:21,040
Shift Enter? Ok, I'm just winging it with you.

408
00:35:21,400 --> 00:35:23,640
Shift Enter. Ok.

409
00:35:24,360 --> 00:35:29,440
One could argue, and this is where the debates will typically happen,

410
00:35:29,440 --> 00:35:33,900
is that, does the actual picker itself
need to be made accessible?

411
00:35:35,460 --> 00:35:38,080
One could argue that I could just type my date.

412
00:35:39,520 --> 00:35:42,560
I'm not blocked by doing this with the keyboard.

413
00:35:43,360 --> 00:35:46,180
One one, two thousand twenty, right?

414
00:35:47,440 --> 00:35:49,820
I didn't get the date picker, I was able to enter my date

415
00:35:49,820 --> 00:35:53,500
but I'm not getting the same experience, so to speak.

416
00:35:53,500 --> 00:35:56,100
So that's where the debate will likely come in.

417
00:35:56,300 --> 00:36:02,660
But, if you are going to try to create an inclusive design, one for all and all for one,

418
00:36:02,660 --> 00:36:06,680
you would likely want the date picker to be available to

419
00:36:07,280 --> 00:36:12,000
people with certain disabilities, they can fast and easily use it

420
00:36:12,000 --> 00:36:13,980
just like if I were to use a mouse.

421
00:36:15,040 --> 00:36:18,160
Bad example. Let's go to a good one.

422
00:36:18,900 --> 00:36:21,520
Let's go to ... this one is okay.

423
00:36:26,820 --> 00:36:29,420
So this is pickadate, so I found a different plug-in.

424
00:36:30,340 --> 00:36:35,420
So this one looks really cool, right? And I can click these arrows and I can pick a date

425
00:36:35,420 --> 00:36:40,480
I can even go to today and I can clear my entry. All that kind of stuff

426
00:36:40,480 --> 00:36:44,800
A great user experience so to speak, I'm not going to go too much into detail

427
00:36:44,800 --> 00:36:52,820
But for a mouse user, its fantastic, right? If I'm using it on a keyboard, I can actually use this.

428
00:36:53,080 --> 00:36:58,960
It doesn't follow the spec, because I can't do things like, you know, Shift-Enter,

429
00:36:58,960 --> 00:37:04,260
I don't have these things memorized, like go from today's date from a previous month

430
00:37:04,260 --> 00:37:08,780
but I can at least interact and go and use it.

431
00:37:09,240 --> 00:37:14,780
So it is a much better following practice of both the standards and the design spec.

432
00:37:17,580 --> 00:37:18,840
One more here...

433
00:37:20,860 --> 00:37:23,800
And this is where I apologize to Dennis

434
00:37:23,800 --> 00:37:27,640
[Dennis]: You're right. You're right

435
00:37:27,920 --> 00:37:37,120
[Seth] So, I'm ... if you guys want to see some really good accessibility, like, I just started really nit-picking this site,

436
00:37:37,480 --> 00:37:43,900
it's very good, and it's getting even better, and I didn't realize there was a standard

437
00:37:43,900 --> 00:37:49,720
or a date timeline for all the airlines. And now it makes perfect sense to me.

438
00:37:50,040 --> 00:37:54,500
why this is so good. Because I would have expected this to be bad.

439
00:37:54,500 --> 00:37:59,840
But, so date picker. So you get this cool thing, it's awesome, it shows me two months at a time

440
00:37:59,840 --> 00:38:06,820
and I can go forward, I can go back with a mouse and it shows me really, visually how awesome this this is.

441
00:38:06,820 --> 00:38:09,640
If I use it with a mouse, I mean a keyboard ...

442
00:38:10,840 --> 00:38:13,960
I'll get into the bottom section of this in a little bit.

443
00:38:15,420 --> 00:38:22,400
But, I can actually, if I can remember, I don't remember the controls

444
00:38:22,400 --> 00:38:29,220
So there, I'm going. So I can go forward, I can go down, I can actually go month to month

445
00:38:29,220 --> 00:38:34,040
if I click there, right. All of these kind of things. This is impressive.

446
00:38:34,280 --> 00:38:39,500
Ok, and there are actually, if we reviewed those design patterns, according to ARIA

447
00:38:39,500 --> 00:38:42,180
all of those, or most of them are pretty available.

448
00:38:42,180 --> 00:38:47,540
The other thing that I will highlight at the bottom, is really impressive.

449
00:38:47,540 --> 00:38:50,840
So let me explain this quickly, and then I'll get into it in more detail.

450
00:38:50,840 --> 00:38:54,800
Notice how when I use my mouse, you don't see that bottom.

451
00:38:56,100 --> 00:38:58,900
But when I use my keyboard, I do.

452
00:39:00,200 --> 00:39:02,860
That's awesome and I'll explain why in a little bit.

453
00:39:03,000 --> 00:39:05,080
Ok, so let me go back to this guy.

454
00:39:36,980 --> 00:39:40,620
I don't have much more. I do not have much more.

455
00:39:46,220 --> 00:39:50,420
Ok, so, we couldn't find the specs, so now let's talk about ARIA.

456
00:39:50,420 --> 00:39:56,720
Right, so this is like the technical thing that some of you may or may not be aware of.

457
00:39:56,960 --> 00:40:02,700
ARIA is the Accessible Rich Internet Applications suite, defines a way to make web content

458
00:40:02,700 --> 00:40:08,440
and web applications more accessible to people with disabilities. It especially helps with the dynamic content

459
00:40:08,440 --> 00:40:15,100
and advance users, interface controls, development with AJAX, HTML, JavaScript and related technologies.

460
00:40:15,100 --> 00:40:19,840
So this is basically like a secondary language
to what we do, that helps

461
00:40:21,140 --> 00:40:25,840
code talk to assistive technologies, 
and assistive technologies to talk to code.

462
00:40:26,200 --> 00:40:33,120
So all of those design patterns basically got augmented and got enhanced with ARIA.

463
00:40:33,780 --> 00:40:40,260
So, understanding some basics, this is a little more technical, so let me know if you have any questions.

464
00:40:40,260 --> 00:40:43,280
Sight and mobility-impaired users must be able to

465
00:40:43,920 --> 00:40:47,540
quickly access a list of landmarks
for a web page that they use.

466
00:40:47,540 --> 00:40:53,060
So basically think of it like a table of contents, so we want to define using landmarks.

467
00:40:54,020 --> 00:41:00,580
Code, on the page, that tells a user with various disabilities that there's a navigation,

468
00:41:01,120 --> 00:41:07,900
there's a side navigation, there's a search, there's content, you want to be explicit so they can, you know,

469
00:41:07,900 --> 00:41:12,140
go to those areas with ease. Remember those examples with tabbing tabbing tabbing tabbing,

470
00:41:12,140 --> 00:41:17,320
and trying to get to something? This prevents that because they can use assistive technology to

471
00:41:17,320 --> 00:41:21,200
access shortcuts to skip the navigation,
we've all heard that, right?

472
00:41:21,560 --> 00:41:24,940
Skip to navigation when you first tab?
This eliminates that.

473
00:41:25,420 --> 00:41:31,760
You don't have to add some extra visual and contextual, you can just basically add some code

474
00:41:31,760 --> 00:41:35,840
and they automatically add this glorious
table of contents.

475
00:41:36,580 --> 00:41:44,180
Roles. So, once you get landmarks, then you might want to specify each particular thing.

476
00:41:44,320 --> 00:41:52,460
What is this? So like, it's a banner, right? It's a main section, it's a navigation. It's a search.

477
00:41:52,460 --> 00:41:59,500
Imagine you trying to execute a specific task, and there's a lot of content on that page.

478
00:42:00,440 --> 00:42:06,120
This is a way for you to quickly access something without question of what it is.

479
00:42:06,560 --> 00:42:10,860
And this is something that really is very foundational.

480
00:42:10,860 --> 00:42:17,100
This takes a developer no effort whatsoever to implement. It just takes him to do it.

481
00:42:17,100 --> 00:42:22,340
But there's no advanced learnings. Just understanding what is available and going from there.

482
00:42:22,340 --> 00:42:25,180
And then we get into a little more advanced stuff.

483
00:42:25,440 --> 00:42:27,200
So States and Properties.

484
00:42:27,200 --> 00:42:29,720
And this is where ARIA kicks in.

485
00:42:30,380 --> 00:42:35,920
So this is, prior to ARIA, there was no consistent, bidirectional, cross-browser implementation between

486
00:42:35,920 --> 00:42:40,140
assistive technologies and applications to communicate.

487
00:42:40,280 --> 00:42:44,260
So like for instance, take my on off switch, right?

488
00:42:44,960 --> 00:42:52,660
I can click it or I can tab it, bit there was no way for a custom built switch

489
00:42:52,660 --> 00:42:55,580
to communicate with an assistive technology.

490
00:42:56,320 --> 00:43:01,120
Because there's that no standard, right? We are losing the communication gap.

491
00:43:01,560 --> 00:43:08,520
So ARIA allows us to do things like expanded or checked or selected or labelledby, there's a lot of that.

492
00:43:08,840 --> 00:43:14,100
So like take a toggle, right. Open, close. Well, it is expanded. Or it is not expanded.

493
00:43:15,200 --> 00:43:17,260
It's checked, or it's not checked.

494
00:43:17,540 --> 00:43:23,680
We can build very creative experiences and visual designs now, and use ARIA

495
00:43:23,680 --> 00:43:27,200
to bridge the communication gap between those technologies.

496
00:43:27,680 --> 00:43:33,540
There's so much to go into that I couldn't do it here. But to give you an example of

497
00:43:33,540 --> 00:43:38,200
where it can be applied is like, so take ARIA for content strategists.

498
00:43:40,180 --> 00:43:47,800
One of the common things they always complain about is "click here" or "explore" or, they want to be

499
00:43:47,800 --> 00:43:52,780
very simple and plain in their nomenclature of buttons in particular.

500
00:43:53,480 --> 00:44:02,480
So, they can add contextual elements that are not visually there, but are to the assistive technologies

501
00:44:02,480 --> 00:44:08,400
using labelledby or describedby. Or they can actually announce what's actually happened.

502
00:44:08,400 --> 00:44:16,480
So, it's hard to see, but in the case of Southwest, when I actually focus in to the box

503
00:44:16,480 --> 00:44:20,640
this black area here is what the screen reader is actually reading.

504
00:44:21,280 --> 00:44:28,660
Ok, so it's reading, content selected, date depart, date depart and formats mm dd

505
00:44:28,920 --> 00:44:34,140
valid dates for March fourth and November fourth, keyboard instructions up down arrow

506
00:44:34,140 --> 00:44:39,380
access the widget shift right, I mean like, imagine coming to this for the very first time

507
00:44:39,380 --> 00:44:41,320
and not having that instruction

508
00:44:41,920 --> 00:44:48,460
There would be no way for you to know how to use that unless you were following the design pattern to spec.

509
00:44:48,460 --> 00:44:51,500
Which we've all clearly noticed it's very hard to do.

510
00:44:51,500 --> 00:44:57,480
So, content strategists can add contextual information to help for accessibility.

511
00:44:58,560 --> 00:45:04,740
So this is an example of where you can go the extra mile if the people are thinking about the intent.

512
00:45:05,120 --> 00:45:12,640
Another one is for UX folks. So, Apple is a great example. They kill it when is comes to accessibility.

513
00:45:12,660 --> 00:45:17,100
So, what I'm doing is I'm using the search box,
using the keyboard.

514
00:45:17,100 --> 00:45:22,180
And the things that I've noticed is, they're using ARIA autocomplete

515
00:45:22,180 --> 00:45:27,900
to tell the user that while you start typing your search phrase, that basically a list of things are autocompleting

516
00:45:27,900 --> 00:45:33,700
so, you'll see it's giving me hints. It's telling me that
that's actually happening.

517
00:45:34,400 --> 00:45:40,680
ARIA has popup. It told me that its popping up with a new feature or so fourth.

518
00:45:40,680 --> 00:45:45,120
So these are the things that the developers can implement without any question.

519
00:45:45,480 --> 00:45:53,160
But it's the user experience people, to go back to that intent, how do I want them to use it?

520
00:45:53,160 --> 00:45:57,280
How do I want them to interact with it? If they don't tell the developer that

521
00:45:57,280 --> 00:46:03,540
the developers won't necessarily know what ARIA to actually use, okay?

522
00:46:05,480 --> 00:46:07,840
This is for the geeks in the room.

523
00:46:07,840 --> 00:46:13,640
The bad news for you front-end web developers is, for you to do this right,

524
00:46:13,640 --> 00:46:18,000
developers not only need to utilize the appropriate ARIA roles, states and properties,

525
00:46:18,000 --> 00:46:23,620
they also have to leverage and use JavaScript to help manage the constant flux of

526
00:46:23,620 --> 00:46:26,280
content, interactions and states.

527
00:46:26,280 --> 00:46:30,740
Some of the things to think about while leveraging all the JavaScript are

528
00:46:31,020 --> 00:46:35,260
that sites using JavaScript typically will be fully accessible.

529
00:46:35,260 --> 00:46:39,780
There's been a lot of data to show that people, even with people with assistive technologies

530
00:46:39,780 --> 00:46:41,420
they don't disable JavaScript anymore.

531
00:46:41,860 --> 00:46:46,200
So all of the screen readers and other assistive technologies are being incorporated

532
00:46:46,200 --> 00:46:50,420
with JavaScript enabled, through ARIA and following those specs and standards.

533
00:46:50,740 --> 00:46:57,420
Ensure that your scripts are both mouse and keyboard enabled. A typical one is

534
00:46:57,920 --> 00:47:04,880
you'll use a click handler. Well, a click handler isn't focus, right? It's not keyboard. It's click. Things like that.

535
00:47:04,880 --> 00:47:10,040
You have to actually think about all the extra JavaScript that you'll have to work with

536
00:47:10,040 --> 00:47:12,660
especially, I think I heard someone talk about Ember.

537
00:47:12,660 --> 00:47:19,820
You know, like if you're talking about single page application that is constantly changing in its state,

538
00:47:20,820 --> 00:47:23,720
This is going to be a lot of work.

539
00:47:24,180 --> 00:47:27,660
Leverage dependent and independant event triggers.

540
00:47:27,980 --> 00:47:31,880
This is relatively new actually, 
or at least I thought is was.

541
00:47:31,880 --> 00:47:36,580
You can track if it's a click or keyboard event

542
00:47:36,580 --> 00:47:38,640
So go back to that Southwest example.

543
00:47:39,200 --> 00:47:44,880
They didn't show the additional help at the bottom if I used my mouse.

544
00:47:45,540 --> 00:47:51,820
But if I used my keyboard, it added actual content and context to the screen.

545
00:47:52,060 --> 00:47:59,000
So they're using independent and dependent triggers to differentiate between mouse and keyboard.

546
00:47:59,000 --> 00:48:02,580
So they're going the extra mile,
with that type of philosophy.

547
00:48:02,780 --> 00:48:06,180
Managing focus and refocus, so like, a good example is,

548
00:48:06,180 --> 00:48:11,820
we always thinking about going somewhere, but if they close it or if they do a negative action,

549
00:48:11,820 --> 00:48:20,240
does it take them back to where they were. Like one thing I often find is like, when I use a table of contents

550
00:48:20,240 --> 00:48:24,100
if I click the table of contents, and I get sent down to the bottom of the page,

551
00:48:24,100 --> 00:48:26,920
but what happens when I want to get back?

552
00:48:28,280 --> 00:48:35,380
There's no way back. You have to tab shift all the way through every single link to get back.

553
00:48:35,720 --> 00:48:41,420
There should be potentially a way to track where you came from and where you might want to go back.

554
00:48:41,660 --> 00:48:43,220
Things like that.

555
00:48:43,220 --> 00:48:47,840
And then the biggest one for you developers, read and follow the design patterns.

556
00:48:47,840 --> 00:48:49,820
I cannot emphasize that enough.

557
00:48:49,940 --> 00:48:56,580
There are, there's so much but that really the only way to make the assistive technologies

558
00:48:56,580 --> 00:49:01,720
to be able to communicate to the browser 
is through the standards.

559
00:49:01,720 --> 00:49:05,800
Some don't follow them, some do but at least we can go with the baseline.

560
00:49:06,100 --> 00:49:12,620
So, here's an example of all of the design patterns that are already specified.

561
00:49:13,920 --> 00:49:20,380
Accordions, alert boxes, dialogs, autocomplete, buttons, checkboxes, comboboxes, date pickers, modals,

562
00:49:20,380 --> 00:49:27,340
drag and drop, grid, I mean, I'm guessing there might be a small percentage of user experiences out there

563
00:49:27,340 --> 00:49:32,720
that comes up wth something brand new. But you can't, I would be surprised if you can't correlate it back to this.

564
00:49:33,560 --> 00:49:37,620
So like, take an accordion.
Oh, not an accordion, a carousel.

565
00:49:37,620 --> 00:49:44,220
There's no carousel in this. So let's think about it, break it apart. Buttons, content, links.

566
00:49:44,440 --> 00:49:49,360
Each little piece of the carousel can be broken up into a standard.

567
00:49:49,940 --> 00:49:55,780
And that's really where you want to focus on both, I would say if you are a UX person,

568
00:49:56,300 --> 00:50:01,980
this is a great place to start building that next best experience but following the standard

569
00:50:02,080 --> 00:50:10,840
take the turnstyle door, right? If you follow these, it'll be more easy to recognize, know how it works,

570
00:50:10,840 --> 00:50:14,900
you won't be pushing it, you won't be bouncing it because it's going to slow or whatever may be,

571
00:50:14,900 --> 00:50:19,460
and then from a developers point of view, this is the place where you really need to

572
00:50:19,460 --> 00:50:25,520
make sure, because if you don't follow these at least the majority of the way through,

573
00:50:25,520 --> 00:50:29,900
screen readers in particular won't be accessible.

574
00:50:29,900 --> 00:50:32,060
And that concludes the presentation.

575
00:50:33,080 --> 00:50:34,420
Thank you.

576
00:50:34,420 --> 00:50:39,700
[Applause]

577
00:50:39,700 --> 00:50:40,820
[Dennis]: Any questions...

578
00:50:41,200 --> 00:50:45,900
[Steve]: So, how does this impact mobile phones?

579
00:50:47,000 --> 00:50:51,600
[Seth]: So, it impacts nearly one to one.

580
00:50:52,080 --> 00:50:59,900
If you are talking about native application, so like your Facebook app, there's a lot more nuance

581
00:50:59,900 --> 00:51:04,020
and a lot more spec out there that hasn't been defined.

582
00:51:04,260 --> 00:51:08,440
But I would say that if you are talking mobile web, so like responsive design,

583
00:51:08,440 --> 00:51:14,720
like, screen readers on mobile phones are following the same standards as desktops are.

584
00:51:14,960 --> 00:51:21,540
And the design pattern, if you think about the analogy of roads or outlooks or whatever,

585
00:51:21,540 --> 00:51:27,840
it's the same thing, right, a switch is a switch, a carousel is a carousel, whether it is in a native app

586
00:51:27,840 --> 00:51:34,040
or in a web page, it's the same intuitive thing. The only thing that is different is how you interact with it.

587
00:51:34,540 --> 00:51:39,940
So if you're able-bodied, you might use swipe, right?
For something, or touch, or tap.

588
00:51:39,940 --> 00:51:46,980
If you're not, you use a screen reader that basically has to intuitively, you know,

589
00:51:47,620 --> 00:51:51,600
communicate to whatever it is that it wants to do, and what it should be doing.

590
00:51:52,040 --> 00:51:56,320
So, if you have an iPhone, try your VoiceOver on it.

591
00:51:56,320 --> 00:52:02,780
It's awesome. It does it very well. And you'll find that the sites or the apps that are following most of the patterns

592
00:52:03,360 --> 00:52:05,200
are the ones you can actually use.

593
00:52:05,660 --> 00:52:09,020
So I would say that in most cases, it's a one to one.

594
00:52:09,020 --> 00:52:14,660
[Steve]: Great. And then the second question, most of these things are JavaScript?

595
00:52:16,600 --> 00:52:27,600
[Seth]: No, so, most, so the screen where I had landmarks, roles and then states and properties,

596
00:52:28,060 --> 00:52:34,800
landmarks and roles are pure HTML. They are just straight-up HTML. There are no ifs, ands or buts.

597
00:52:35,520 --> 00:52:42,100
The state changing, when you need to interact with it on a dynamic element

598
00:52:42,100 --> 00:52:45,580
so, does everybody understand what stateless
or state means?

599
00:52:45,580 --> 00:52:49,000
It means that it is either ... like static or it can be a constant across ...

600
00:52:49,000 --> 00:52:55,800
if it doesn't have a state, that it can change, you have to track that through JavaScript.

601
00:52:55,800 --> 00:53:02,140
So there are instances of sites out there that don't really leverage a lot of dynamically changing components

602
00:53:02,140 --> 00:53:09,520
and elements that you can make purely accessible, which is some basic ARIA tags, roles and landmarks.

603
00:53:11,920 --> 00:53:12,660
[Attendee]: I have a question

604
00:53:12,660 --> 00:53:13,220
[Seth]: Sure.

605
00:53:13,220 --> 00:53:22,860
[Attendee]: So I read somewhere where ARIA was ... and a lot of the default HTML5

606
00:53:22,860 --> 00:53:27,600
elements and landmarks actually have the ARIA ...  within them.

607
00:53:27,600 --> 00:53:28,100
[Seth]: Correct.

608
00:53:28,100 --> 00:53:40,720
[Attendee]: So would it be better to just try to ...
I don't know, not be so redundant ...

609
00:53:40,720 --> 00:53:47,900
[Seth]: Correct. So in the absence of, if I were to use the nav tag, which is navigation,

610
00:53:47,900 --> 00:53:52,580
you wouldn't need to add role navigation to it.
You would not need to do that.

611
00:53:52,580 --> 00:53:57,080
But in the instance of, you know, progressive enhancement and graceful degradation,

612
00:53:57,080 --> 00:54:02,300
when you have to accommodate a non-HTML5 browser, you then need to

613
00:54:02,300 --> 00:54:07,480
a shim it, if no one knows what that is, I will explain later, but be basically, add the role.

614
00:54:07,480 --> 00:54:09,860
That's usually what shimming will do.

615
00:54:10,780 --> 00:54:16,900
But, yes, generally speaking, you don't need to over tag, and the way to learn more about that is

616
00:54:17,520 --> 00:54:24,060
what I do a lot now, which is, a lot quicker and a lot easier is to use a fiddle, like a js fiddle or like a codepen

617
00:54:24,060 --> 00:54:28,700
I'll stick one tiny tag in that fiddle and I'll open up my screen reader

618
00:54:28,700 --> 00:54:35,240
rather than going through the whole page and figuring out the page, I will go component and elements alone

619
00:54:35,240 --> 00:54:38,160
and hear it and learn from it and see if it actually works.

620
00:54:38,160 --> 00:54:42,920
It's an extra step, it's kind of a poc, a proof of concept.

621
00:54:42,920 --> 00:54:47,900
So, thats how I'll do that. You could go in,
type a tag and test it and be like

622
00:54:47,900 --> 00:54:52,260
"ok, well, maybe that's not intuitive enough,
I'm going to add something else."

623
00:54:52,260 --> 00:54:57,660
[Dennis]: We actually did something similar, we've had an ongoing debate

624
00:54:57,660 --> 00:55:10,560
between aria-label, aria-labelledby and aria-describedby. We had one of our folks in requirements saying

625
00:55:10,560 --> 00:55:18,280
aria-labelledby and then the text they want to appear. For any of you who do not know,

626
00:55:18,280 --> 00:55:25,160
aria-labelledby and describedby, they typically point to an ID, which has the textual content

627
00:55:25,160 --> 00:55:32,880
that is describing the label. Aria-label actually contains the text string that is used as the label.

628
00:55:32,880 --> 00:55:42,600
But we ... I knew that as being the fact, but the UX person that I'm collaborated with kept on saying

629
00:55:42,600 --> 00:55:52,760
aria-describedby and then the text. So I literally created just a flat, HTML file with every variation of these three

630
00:55:52,760 --> 00:55:58,300
ARIAs used, and then we just listened to it in two different screen readers and said

631
00:55:58,300 --> 00:56:07,940
done. And I think that's really what you have to do with ARIA. In our initial requirements,

632
00:56:07,940 --> 00:56:12,500
the requirements folks, next to every link,
would say role equals link.

633
00:56:14,140 --> 00:56:16,100
And I'm like ... all that extra work.

634
00:56:16,100 --> 00:56:18,580
[Seth]: Yeah, there's intent for each of them.

635
00:56:18,580 --> 00:56:23,480
And understanding the intent of them could sometimes be ambiguous.

636
00:56:23,480 --> 00:56:28,320
But like, just like, for front-end developers, when do you use an ID and when do you use a class

637
00:56:28,320 --> 00:56:32,340
or when do you use a data selector, all of these type of things come into the discussion.

638
00:56:32,860 --> 00:56:39,820
There is original intent behind those attributes and parameters. And if you stick to the original intent,

639
00:56:39,820 --> 00:56:47,540
you'll likely succeed more across a wider range than if you change it, like for instance, like

640
00:56:47,540 --> 00:56:53,960
I could not use any class or ID on any div or any element ever, right?

641
00:56:53,960 --> 00:56:59,140
And I could use data selectors. I could manipulate it and manage the page any way I wanted to.

642
00:56:59,140 --> 00:57:07,880
It's possible. Should you? No. So you want to try and research back to the intent of the littlest nuance

643
00:57:07,880 --> 00:57:14,360
to ensure that the widest range of things are actually working. So like labelledby would widely be used

644
00:57:14,360 --> 00:57:22,100
for a one to many relationship. So you have one description like "this link opens in a new window"

645
00:57:22,100 --> 00:57:29,380
but you have ten links on the page. So those ten links will have labelledby and that one ID

646
00:57:29,380 --> 00:57:36,560
like Dennis said, and your leveraging a better experience and a better codebase to do it as well.

647
00:57:38,240 --> 00:57:44,740
[Attendee]: How different would you say the experience is between different screen readers?

648
00:57:44,740 --> 00:57:46,420
[Seth]: I'm glad you asked.

649
00:57:46,420 --> 00:57:59,460
I would say that it is an exact, same paradigm as between Safari, Firefox, Mozilla, IE, Chrome

650
00:57:59,460 --> 00:58:01,520
It is just a different browser.

651
00:58:01,880 --> 00:58:11,560
I mean, essentially what it is. NVDA doesn't do exactly what JAWS does, JAWS doesn't do what VoiceOver does

652
00:58:11,560 --> 00:58:15,440
They're all trying to follow the specs but they all behave differently.

653
00:58:16,360 --> 00:58:22,500
[Dennis]: One thing I'll say about that, just from an experience within the last six to eight months is

654
00:58:22,880 --> 00:58:34,460
it's also a difference between platforms ... JAWS, handle things in a similar manner.

655
00:58:34,460 --> 00:58:42,500
JAWS is more robust than NVDA. Safari which is on a different platform, reads the DOM in a different manner.

656
00:58:42,500 --> 00:58:51,300
Therefore, certain things that may work in JAWS and NVDA does not seem to work in Safari

657
00:58:51,300 --> 00:59:00,840
It doesn't mean that Safari is broken, it just that it does it differently. From my experience, Safari and VoiceOver

658
00:59:00,840 --> 00:59:10,480
are the most strict combination that you can use. So if you don't know if something works or not,

659
00:59:10,480 --> 00:59:15,560
try it in Safari and VoiceOver first, then test on the Windows platform.

660
00:59:15,560 --> 00:59:20,920
[Seth]: Right, and it's also a paradigm between which screen reader or assistive technology you are using

661
00:59:20,920 --> 00:59:23,020
and which browser you are using.

662
00:59:23,020 --> 00:59:23,960
[Dennis]: Don't use Chrome.

663
00:59:23,960 --> 00:59:28,620
[Seth]: Right? So for instance, you're using VoiceOver and you're using Chrome,

664
00:59:28,620 --> 00:59:35,880
it won't work as well if you're using VoiceOver with Safari. Or if you're using JAWS with Firefox

665
00:59:35,880 --> 00:59:37,920
versus JAWS with IE.

666
00:59:37,920 --> 01:00:32,720
[Attendee]: [Unrecognizable]

667
01:00:32,720 --> 01:00:37,980
[Dennis]: So, two things. They're not telling us.

668
01:00:37,980 --> 01:00:40,100
[Laughter]

669
01:00:40,100 --> 01:00:50,620
[Dennis]: So two things. One, WebAim, which is a website, they have an annual screen reader survey.

670
01:00:51,320 --> 01:00:56,640
Check out the survey, the last one was last July, they'll likely be putting out another one soon.

671
01:00:56,640 --> 01:01:04,000
And they tell you the combinations of browser and screen reader, and it actually changed big time last year

672
01:01:04,000 --> 01:01:12,660
because of the folks that run Windows Eyes, they actually announced to their users

673
01:01:12,660 --> 01:01:19,420
that there was a survey going on and NVDA dropped clear to second to last place

674
01:01:19,420 --> 01:01:27,980
and Windows Eyes was second to JAWS. But you'll get a feel for how actually screen reader users are

675
01:01:27,980 --> 01:01:34,520
using the tools, with which browsers and such, that's a great resource.

676
01:01:34,520 --> 01:01:36,920
Now, how are the airlines handling it?

677
01:01:39,380 --> 01:01:41,940
[Attendee]: Somebody is going to come back and judge you, right?

678
01:01:42,980 --> 01:01:54,460
[Dennis]: Yes, and that is the users. So, it's been an emotional roller coaster the last year

679
01:01:54,460 --> 01:02:01,420
because the DOT is not telling us what their going to do. First, we thought they were going to hire auditors.

680
01:02:01,900 --> 01:02:13,240
What's going to happen is, when users find an issue, they won't come to us, they'll go to the DOT.

681
01:02:13,240 --> 01:02:19,840
The DOT will file a complaint with us, we have however long, we don't even know how long the grace period is

682
01:02:19,840 --> 01:02:27,000
but we will have, however many weeks to fix that particular problem, or else we will be fined

683
01:02:27,000 --> 01:02:30,880
$27,000 dollars per instance per day.

684
01:02:30,880 --> 01:02:36,320
[Seth]: The thing to keep in mind, and I'll kind of go back to the original question

685
01:02:36,320 --> 01:02:42,040
so A: if you are in the position to make a choice of what requirements you have

686
01:02:42,040 --> 01:02:45,320
just like any sort of requirements, you follow the numbers.

687
01:02:45,320 --> 01:02:48,660
So like JAWS is 75% of the screen reader market.

688
01:02:48,660 --> 01:02:53,320
So by using ChromeVox, which is a good example,
it's like zero percent.

689
01:02:53,320 --> 01:02:54,520
So it's a testing tool.

690
01:02:54,520 --> 01:02:59,140
[Dennis]: Yeah, it's a testing tool, we actually thought it would be great for our developers,

691
01:02:59,140 --> 01:03:06,920
because it's like handy. Experience has told us that it works completely differently

692
01:03:06,920 --> 01:03:12,380
As well as Chrome in general works differently with any screen reader.

693
01:03:12,380 --> 01:03:18,180
We're heavy Chrome users for development, but when it comes time to using a screen reader,

694
01:03:18,180 --> 01:03:23,140
open up Firefox and NVDA or IE and JAWS.

695
01:03:23,140 --> 01:03:30,280
[Seth]: Just like you would do in a normal QA cycle, so at Critical Mass, we test every browser

696
01:03:30,280 --> 01:03:33,800
that meets our client's or the industry's requirements.

697
01:03:33,800 --> 01:03:44,120
So, when it comes down to it, we can't guarantee that it'll work in every single browser and every single device

698
01:03:44,120 --> 01:03:50,280
or every single orientation, it's not possible. But we can do our best.

699
01:03:50,280 --> 01:03:55,120
And our best, the easiest way to achieve the best, is to follow the specs.

700
01:03:55,120 --> 01:04:02,680
And I will say that, in my experience, JAWS and VoiceOver and NVDA, they all behave

701
01:04:02,680 --> 01:04:09,760
very very similar from a code perspective, you might just need to know the nuances

702
01:04:09,760 --> 01:04:18,220
of how to access that. Like, as a tester. So, your testers might actually not know how to use the devices

703
01:04:18,220 --> 01:04:23,040
or the assistive technology well enough, and they'll get false positives.

704
01:04:24,880 --> 01:04:30,060
So just like I did an example, I pulled up Southwest, I couldn't figure it out, I said ok, that's how.

705
01:04:30,060 --> 01:04:35,660
It was eventually accessible, once I remembered the right types of things to do.

706
01:04:35,660 --> 01:04:42,540
So your testers have to really know the devices that they're using to test on.

707
01:04:42,540 --> 01:04:49,620
It's like, a mobile phone or a desktop, you test differently from a mobile phone to a desktop, right?

708
01:04:49,620 --> 01:04:56,800
You test differently from NVDA to JAWS, JAWS to VoiceOver. So if you're doing the full gamut,

709
01:04:56,800 --> 01:04:59,360
it's part of the biz, so to speak.

710
01:05:01,260 --> 01:05:22,640
[Attendee]: Dennis, the Feds, there's no way the Feds will ...

711
01:05:22,640 --> 01:05:24,320
[Seth]: There's a question back over here.

712
01:05:24,320 --> 01:05:32,240
[Attendee]: ...

713
01:05:32,240 --> 01:05:41,040
[Seth]: So yes. So that is the W3C created WCAG 2.0, which is relatively recent, and then there's three levels,

714
01:05:41,040 --> 01:05:47,360
within that, so that's the standards that basically both the browsers are following and

715
01:05:47,360 --> 01:05:52,600
the assistive technologies are trying to mimic towards, but as we all know,

716
01:05:53,120 --> 01:05:57,600
browsers and companies and businesses like to make their own nuances

717
01:05:58,060 --> 01:06:05,720
and they don't always follow the standards, right? And that's why we have kit CSS, we have Mozilla,

718
01:06:05,720 --> 01:06:10,900
hyphen Mozilla because they wanted to do something before the standard was finished

719
01:06:11,420 --> 01:06:17,480
or before there was a standard. So every browser and every assistive technology,

720
01:06:17,480 --> 01:06:23,580
they all try and follow a certain set of rules, but this is not a perfect utopia.

721
01:06:24,000 --> 01:06:25,660
So that rarely ever happens.

722
01:06:26,640 --> 01:06:29,680
[Dennis]: We have time for one more question.

723
01:06:32,880 --> 01:06:46,880
[Attendee]: ...

724
01:06:47,080 --> 01:06:56,460
[Dennis]: So, that ... I believe that was started by Stephen Faulkner who contributes to the W3C spec for ARIA.

725
01:06:56,600 --> 01:07:03,340
But also on WebAim.org their forum, let's put it this way,

726
01:07:03,340 --> 01:07:09,740
I joined the International Association of Accessibility Professionals last year

727
01:07:09,740 --> 01:07:17,860
primarily for the forums. I did not renew, because WebAim, and their forums, which are free,

728
01:07:18,920 --> 01:07:22,940
are almost richer for my particular needs.

729
01:07:24,740 --> 01:07:34,120
It's a little antiquated, because it's driven by email. But if you want to learn like ...

730
01:07:34,120 --> 01:07:39,500
I started a thread, however many months ago, a button versus a link.

731
01:07:39,500 --> 01:07:46,660
And actually, the information I was receiving, which was from like Steven Faulkner from the W3C

732
01:07:46,660 --> 01:07:53,960
and Leonie Watson and such, they were contradicting what the advice we were being given

733
01:07:53,960 --> 01:08:04,860
by an agency, and that was helpful because I actually have a high level of respect for these particular people.

734
01:08:04,860 --> 01:08:14,900
They basically said, code to spec, let the assistive technology catch up, which sounds like IE, so.

735
01:08:14,900 --> 01:08:19,180
It's just history repeating itself.

736
01:08:21,580 --> 01:08:24,240
Well, once again, Seth, thank you so much.

737
01:08:24,240 --> 01:08:29,520
[Applause]

