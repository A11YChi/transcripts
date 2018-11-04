# Color contrast and alt attributes on npr.org (Lightning Talk)
## Todd Welstein - Wednesday, October 5, 2016
[Source recording](https://www.youtube.com/watch?v=s98z_ThsNC0)

**[Todd]:** Hi, I’m Todd Welstein. I work as a UI developer at NPR. The department that I’m in is called Digital Media, and it is responsible for NPR’s digital presence. It includes developers, QA people, dev ops, product owners, UX designers, product designers. We’re responsible for the website, npr.org, apps like NPR One, APIs that power website and the apps, and the internal content management system. And it’s a high traffic site. So for example, in September, there were 86 million page views and 40 million unique users. And my job as UI developer focuses on writing HTML, CSS and JavaScript.

This particular talk is going to be divided into two parts. The first part is color contrast. And it covers the basics of making adjustments for that. The second part of this related to alt text, specifically the null alt attribute value, and how that helps to reduce redundancy for screen reader users.

13
00:01:21,180 --> 00:01:26,220
So contrast ratio refers to the relationship between foreground and background color.

14
00:01:27,460 --> 00:01:31,900
The Web Content Accessibility Guidelines for double A specifies

15
00:01:31,900 --> 00:01:36,460
a minimum ratio of four and a half for text and images of text.

16
00:01:37,640 --> 00:01:44,000
For large text, if text is over 18 points or 14 point bold, then the requirement gets lowered to 3.0.

17
00:01:44,000 --> 00:01:46,460
But this talk is going to focus on 4.5.

18
00:01:47,500 --> 00:01:49,720
There are some other exceptions to this rule as well.

19
00:01:50,060 --> 00:01:55,640
For example, text that is part of a logo or a brand name also as no requirements.

20
00:01:57,280 --> 00:02:04,460
The ratios themselves range from 1 to 21, 1 being completely invisible, 21 being very visible.

21
00:02:05,100 --> 00:02:10,120
And in this particular example, I increased the font size so you can see it,

22
00:02:10,120 --> 00:02:14,540
but the first item that meets the 4.5 requirement is the third from the top.

23
00:02:17,820 --> 00:02:22,980
So you might be wondering why did they choose 4.5 as the ratio?

24
00:02:23,480 --> 00:02:29,320
Well, according to the W3C, it is to account for the loss in contrast that results from

25
00:02:29,320 --> 00:02:33,980
moderately low visual acuity, congenital or acquired color deficiencies,

26
00:02:33,980 --> 00:02:37,280
or the loss of contrast sensitivity that typically accompanies aging.

27
00:02:38,600 --> 00:02:41,900
It goes on to say that this basically means someone with 20/40 vision.

28
00:02:42,740 --> 00:02:50,440
Someone with 20/40 vision is commonly thought of as having the acuity of someone who is about 80 years old.

29
00:02:51,000 --> 00:02:58,140
However, in addition to helping users with permanent disabilities, permanent visual difficulties,

30
00:02:58,140 --> 00:03:02,020
the guidelines also help people with transient issues.

31
00:03:02,360 --> 00:03:03,660
So what’s a transient issue?

32
00:03:03,660 --> 00:03:08,300
Well, if you’re outside and you’re using your phone on a sunny day, there might be glare on the screen.

33
00:03:08,660 --> 00:03:13,140
Or if you’re viewing a presentation on a bad overhead projector, there also might be issues.

34
00:03:13,980 --> 00:03:16,200
So, this can help everybody.

35
00:03:19,080 --> 00:03:21,720
There are many tools out there that can check color contrast.

36
00:03:22,020 --> 00:03:26,120
A few are listed here, but this talk is going to focus the last one,

37
00:03:26,120 --> 00:03:32,880
which is Google Accessibility Developer Tools, which is a Chrome extension you can get at the Chrome Web Store.

38
00:03:34,580 --> 00:03:36,200
So here is a typical story on npr.org.

39
00:03:36,560 --> 00:03:42,940
There is a large photo, a caption underneath and a photo credit.

40
00:03:44,780 --> 00:03:50,400
I took the photo and changed the caption color so that it no longer meets requirements.

41
00:03:50,880 --> 00:03:54,420
The ratio for the Chicago skyline is right now 2.32.

42
00:03:55,600 --> 00:04:01,140
And so now we can pretend that we’re going to use the Google Accessibility Developer tools to fix this.

43
00:04:02,380 --> 00:04:06,840
So once the extension is installed, you can open dev tools and go to the Audits pane

44
00:04:06,840 --> 00:04:09,960
where there will be a new option for Accessibility.

45
00:04:10,560 --> 00:04:14,100
And you run an audit and your presented with a list of findings.

46
00:04:15,500 --> 00:04:20,300
So one list includes color contrast, which we’re looking at right now.

47
00:04:21,280 --> 00:04:24,660
And the photo caption is highlighted in red, so it’s a paragraph tag.

48
00:04:25,360 --> 00:04:31,000
If you right click that paragraph tag, you’re taken to the elements panel and,

49
00:04:31,000 --> 00:04:37,200
there’s also a new pane here too called Accessibility Properties, all the way on the right side.

50
00:04:37,740 --> 00:04:40,780
And you can see that the contrast is indeed 2.32.

51
00:04:41,900 --> 00:04:47,120
And there’s other options there. So you can test out what double A or triple A will look like.

52
00:04:47,620 --> 00:04:51,560
If you click the icons directly next to those hex codes,

53
00:04:51,980 --> 00:04:55,720
you’ll see immediately in the browser what the new color looks like.

54
00:04:55,720 --> 00:04:59,320
And if you like it, you can copy the hex code and paste it into your CSS.

55
00:04:59,980 --> 00:05:04,500
So, we pretend that we click on the double A icon, we get this.

56
00:05:04,500 --> 00:05:10,320
So the before version is on the left, the after version is on the right.

57
00:05:11,360 --> 00:05:15,800
It’s a little difficult to see on the projector, but there’s a difference.

58
00:05:17,320 --> 00:05:20,960
And this is the process that we went through for the entire site.

59
00:05:20,960 --> 00:05:27,180
But it was a very manual process and there are many different templates for npr.org.

60
00:05:28,020 --> 00:05:31,660
There’s story pages, music homepage, music pages, podcast directory,

61
00:05:32,180 --> 00:05:35,940
and all of these templates have different permutations,

62
00:05:35,940 --> 00:05:38,920
because the content management system is very flexible.

63
00:05:38,920 --> 00:05:44,680
You can put different assets in different categories, different locations and configure them differently.

64
00:05:45,760 --> 00:05:50,200
So, we covered a big chunk of the site, but it’s still an ongoing process.

65
00:05:53,020 --> 00:05:56,120
When you’re doing this, there’s going to be issues outside of your control,

66
00:05:56,120 --> 00:05:59,440
and also false-positives, depending on the tool that you use.

67
00:06:00,740 --> 00:06:08,240
Items outside of your control include ads from a third party server or embeds like video

68
00:06:08,240 --> 00:06:12,440
or any type of third party embed that has content that’s text.

69
00:06:12,440 --> 00:06:18,040
The Google Accessibility Developer Tools looks at those too and will give you warnings,

70
00:06:18,040 --> 00:06:20,480
it will flag them if they don’t meet contrast requirements.

71
00:06:21,100 --> 00:06:22,560
There’s not much you can do about that

72
00:06:22,560 --> 00:06:28,360
except for notify the originators of those ads or embeds about the problem.

73
00:06:29,320 --> 00:06:31,540
False positives include …

74
00:06:32,220 --> 00:06:38,820
so there’s certain ways to hide text from sighted users while keeping it readable by screen readers.

75
00:06:39,160 --> 00:06:45,020
And depending on the CSS technique you use, if you deliberately want to hide text from sighted users,

76
00:06:45,800 --> 00:06:49,700
the Accessibility Developer Tools may still flag those items as being a problem.

77
00:06:50,560 --> 00:06:52,060
So for us, we’re seeing that a lot.

78
00:06:53,380 --> 00:06:59,160
And so you can either ignore them or try to figure out a different technique that the Developer Tools would ignore.

79
00:07:00,220 --> 00:07:07,340
Also, as I mentioned, logos and branding-related text, they are exempt from contrast requirements,

80
00:07:07,660 --> 00:07:10,500
but they’ll still get flagged if your using web fonts or just plain text.

81
00:07:11,480 --> 00:07:18,520
That said, here are a few examples of before and after, from the site.

82
00:07:20,540 --> 00:07:24,580
Again, it may be a little bit difficult to see the difference on the projector,

83
00:07:24,920 --> 00:07:27,960
but on top is before, and on the bottom is after.

84
00:07:27,960 --> 00:07:33,100
This is the homepage. We adjusted the blue color for the navigation links.

85
00:07:33,800 --> 00:07:41,720
This is the small breakpoints navigation and again the blue color has been altered.

86
00:07:42,460 --> 00:07:49,340
This is a larger breakpoint, top is before, bottom is after, it’s a little hard to see.

87
00:07:49,940 --> 00:07:52,660
This type of digital pattern is pretty common on the site.

88
00:07:53,540 --> 00:08:00,340
In this case, the tagline “Stories of Life in a Changing World” was … the difference is pretty obvious here.

89
00:08:01,960 --> 00:08:10,520
Here is a music story page for small screen. Pretty much every element was adjusted.

90
00:08:11,600 --> 00:08:18,020
This is commonly on a story page, it’s a topic related to the topic of the story.

91
00:08:18,880 --> 00:08:21,300
And before is on the left and after is on the right.

92
00:08:22,220 --> 00:08:24,760
Here’s the audio player, when it’s not playing.

93
00:08:25,200 --> 00:08:28,740
The text for zoom listening now meets the requirements.

94
00:08:29,040 --> 00:08:35,820
This is from the podcast directory. The topic “business” was changed.

95
00:08:36,740 --> 00:08:44,120
And then lastly here’s the player, and this is again pretty hard to see, but the light blue background

96
00:08:44,120 --> 00:08:51,000
beneath the bottom portion of the player was made darker so that the timing information

97
00:08:51,640 --> 00:08:55,360
and the text in the center meet contrast requirements.

98
00:08:56,480 --> 00:09:00,880
Keep in mind if you are doing this, there may be other assets on the page that you need to change.

99
00:09:01,620 --> 00:09:07,700
Those icons above, the play icon, the rewind icon, the skip icon, are all SVGs,

100
00:09:07,700 --> 00:09:15,300
and so when we changed the blue of the player, we also had to change the SVG blue color

101
00:09:15,300 --> 00:09:18,280
to match the new shade of blue that we were using.

102
00:09:20,840 --> 00:09:22,780
So those are a few examples, but after doing this,

103
00:09:22,780 --> 00:09:27,120
you may find that the color palette you are using in your CSS may grow.

104
00:09:27,740 --> 00:09:32,820
We already had a problem on the site where there were many several shades of colors,

105
00:09:33,540 --> 00:09:37,360
and it was hard to tell what was intentional and what was caused from

106
00:09:37,360 --> 00:09:40,680
using the eyedropper tool on the wrong part of a compressed palette.

107
00:09:41,740 --> 00:09:44,940
So after doing this, we ended up with 198 colors.

108
00:09:45,260 --> 00:09:47,980
Which is a lot, and some of them are very similar.

109
00:09:50,820 --> 00:09:54,020
So very briefly, there are ways you can slim this down.

110
00:09:54,320 --> 00:10:00,380
There’s a tool called Parker, that will generate a list of all the different colors in your codebase.

111
00:10:00,740 --> 00:10:02,940
You can take that list and run it through a tool

112
00:10:02,940 --> 00:10:05,680
called CSS Colorguard, that will run that list

113
00:10:05,680 --> 00:10:07,680
through an algorithm to show you pairs of

114
00:10:08,160 --> 00:10:13,060
visually, semi-indistinguishable colors.

115
00:10:13,460 --> 00:10:18,300
But when you’re doing that, you have to be mindful that you’re not going to re-introduce color contrast issues.

116
00:10:18,920 --> 00:10:22,520
So we manually went and …

117
00:10:22,900 --> 00:10:29,880
trying to combine colors while making sure that there color contrast was above 4.5.

118
00:10:31,040 --> 00:10:36,000
Once we finished that, we ended up with 78 distinct colors, which still may seem like a lot,

119
00:10:36,000 --> 00:10:40,200
but the site is big and this takes into account everything.

120
00:10:41,340 --> 00:10:47,000
The nice side effect of simplifying colors and organizing them is that you can

121
00:10:47,000 --> 00:10:51,620
programmatically create a color swatch guide for other developers and designers.

122
00:10:52,080 --> 00:10:58,020
This will hopefully allow people to choose combinations that have already been vetted

123
00:10:58,480 --> 00:11:02,180
and less likely to introduce contrast problems.

124
00:11:04,260 --> 00:11:05,460
So that’s Part 1.

125
00:11:06,020 --> 00:11:10,080
Part 2 is about the null alt attribute value.

126
00:11:10,980 --> 00:11:12,980
So what is the null alt attribute value?

127
00:11:13,300 --> 00:11:14,320
So it looks like this.

128
00:11:14,500 --> 00:11:16,960
This is a very simplified img tag.

129
00:11:17,640 --> 00:11:21,820
The alt attribute value is equal to an empty string here.

130
00:11:22,420 --> 00:11:25,920
This is not the same thing as having no alt attribute value.

131
00:11:26,820 --> 00:11:28,240
So why would you want to do this?

132
00:11:28,560 --> 00:11:36,160
Well, alt text should typically not be redundant or provide the same information that is already on the page.

133
00:11:36,680 --> 00:11:41,800
So going back to our example story here. There’s an image with a caption that says Chicago skyline.

134
00:11:42,840 --> 00:11:48,100
In the past, before we made any changes, the img tag was basically like this.

135
00:11:48,480 --> 00:11:54,340
It was the same text in the alt attribute as was already on the page as a caption.

136
00:11:57,980 --> 00:12:03,640
And screen readers will then just read the alt attribute, and directly after that, read the caption.

137
00:12:03,640 --> 00:12:10,140
So its a redundancy. I’ll play a screen recording of it, I’m not sure you’ll be able to hear it, but let’s see.

138
00:12:10,260 --> 00:12:15,340
[Screen reader]: link Adam Frank Chicago Skyline image Chicago Skyline istockphoto

139
00:12:15,640 --> 00:12:20,200
[Todd]: So if you could hear that, it read chicago skyline, and then again chicago skyline.

140
00:12:20,200 --> 00:12:22,200
As it read the alt text and then the caption.

141
00:12:23,680 --> 00:12:31,480
So we would use the null alt attribute value here, and then this is how VoiceOver will read the page.

142
00:12:31,480 --> 00:12:38,080
[Screen reader]: link Adam Frank Chicago Skyline image credit istockphoto

143
00:12:38,080 --> 00:12:41,420
[Todd]: So if you could hear that, it skipped over the image and just read the caption.

144
00:12:42,360 --> 00:12:51,140
You may have also heard these helper words. So we also added ARIA labels to the image credit and caption.

145
00:12:51,600 --> 00:12:56,480
The screen reader will read out image caption before it reads caption, and it’ll read out image credit

146
00:12:57,020 --> 00:13:00,360
before it read the credit. Also, we did that for the byline.

147
00:13:01,060 --> 00:13:03,060
I’ll play it one more time. Hopefully you can hear.

148
00:13:03,060 --> 00:13:09,560
[Screen reader]: byline group link Adam Frank image caption  Chicago Skyline credit istockphoto

149
00:13:09,660 --> 00:13:11,640
[Todd]: So those are from the ARIA labels.

150
00:13:13,720 --> 00:13:22,060
Now, editors can choose to inhibit the captions from showing on any image via a checkbox in the CMS.

151
00:13:22,820 --> 00:13:28,920
If they do that, then having the null alt attribute is not a good idea. So in that case,

152
00:13:29,460 --> 00:13:35,820
what was formerly the caption will then become the alt text again. And that sounds like this.

153
00:13:35,820 --> 00:13:41,620
[Screen reader]: byline link Adam Frank Chicago Skyline image image credit istockphoto

154
00:13:41,620 --> 00:13:45,340
[Todd]: So VoiceOver there read the alt text, because there was nothing else,

155
00:13:46,440 --> 00:13:49,800
there was no image caption, so we used alt text.

156
00:13:52,920 --> 00:13:59,820
Keep in mind that an image that is the only thing inside of a link, must never have the null alt attribute value.

157
00:14:01,600 --> 00:14:08,200
The functionality of the link should be mentioned in the alt text in addition to the content of the image.

158
00:14:09,180 --> 00:14:15,900
If you use a null alt attribute value, and an image is the only thing in a link, in VoiceOver,

159
00:14:16,260 --> 00:14:23,760
it won’t read anything helpful. Also, users that navigate via the tab key are going to hear this out if context.

160
00:14:24,060 --> 00:14:30,400
So if they tab to an image that just talks about … that has alt text that’s just about the image

161
00:14:30,400 --> 00:14:34,960
and not the link, you’re not going to hear anything relevant to where that link actually goes.

162
00:14:36,260 --> 00:14:40,120
It helps sighted users too, because if the image doesn’t load for whatever reason,

163
00:14:40,660 --> 00:14:43,380
then the alt text will be there telling them about the link.

164
00:14:46,240 --> 00:14:53,760
So just to reiterate, if this image was the only thing in the link, even if Chicago Skyline was directly underneath it,

165
00:14:54,120 --> 00:14:58,340
you still need alt text, you can’t use the null attribute value.

166
00:14:58,340 --> 00:15:04,580
Because the alt text for the image should discuss the link as well as the image.

167
00:15:07,300 --> 00:15:11,500
So, if you’re like me and you worry a little bit about getting this perfectly right,

168
00:15:11,900 --> 00:15:18,100
this quote is really helpful for me. It says like many things in web accessibility, determining appropriate,

169
00:15:18,100 --> 00:15:23,540
equivalent, alt text is often a matter of personal interpretation, and there’s often

170
00:15:23,540 --> 00:15:28,920
not one super right answer. So this is really helpful to keep this in mind when you are doing this.

171
00:15:30,140 --> 00:15:32,140
Lastly, some additional resources.

172
00:15:32,140 --> 00:15:37,700
There’s a link to the developer tools, a couple articles that were really helpful, contrast testing,

173
00:15:38,360 --> 00:15:42,420
there’s the mathematic formula to calculate the ratio if you’re interested in that,

174
00:15:43,300 --> 00:15:48,280
an article on alt text and on the bottom, I wrote an article on our tech blog,

175
00:15:48,780 --> 00:15:51,740
basically about what I just spoke about.

176
00:15:51,740 --> 00:15:58,280
Also if you’re interested in what other people from the tech team are doing, check out npr.codes.

177
00:15:58,800 --> 00:15:59,900
Thanks for listening.

178
00:16:00,200 --> 00:16:04,660
[Applause]

179
00:16:04,660 --> 00:16:05,720
[Dennis]: Any questions for Todd?

180
00:16:06,700 --> 00:16:12,300
[Attendee]: So, what was the advantage of having a null alt tag versus not having any alt tag?

181
00:16:12,720 --> 00:16:16,900
[Todd]: If there’s no alt tag at all, then, the screen reader … the question was …

182
00:16:16,900 --> 00:16:24,400
what’s the advantage of using null as an alt attribute value versus nothing, not even having an alt tag.

183
00:16:24,800 --> 00:16:33,320
If there’s no alt tag at all, then, the screen reader will likely read the file name of the image,

184
00:16:33,320 --> 00:16:35,320
which is like super unhelpful.

185
00:16:36,220 --> 00:16:38,220
[Dennis]: Especially on a content management system.

186
00:16:38,620 --> 00:16:40,620
[Todd]: Yes, very long, very long filenames.

187
00:16:41,520 --> 00:16:46,900
[Attendee]: Yeah, I know you are on the UI/UX department at NPR Todd.

188
00:16:46,900 --> 00:16:55,120
I’m just curious, were there other areas of accessibility that NPR undertook in addition to the contrast issue?

189
00:16:56,400 --> 00:17:04,740
Todd]: Yeah, so we recently worked with ARIA landmarks and ARIA labels. I briefly touched on the labels.

190
00:17:04,740 --> 00:17:09,740
We added landmarks also. We have a skip to main content.

191
00:17:10,500 --> 00:17:15,520
For the player, we just launched a consistent player, an audio player. We added keyboard shortcuts for that.

192
00:17:15,520 --> 00:17:22,220
And a link to can get to via the tab key for getting help on keyboard shortcuts themselves.

193
00:17:22,420 --> 00:17:25,820
Those are a few that comes to mind right now. There’s other things too.

194
00:17:27,340 --> 00:17:32,020
[Attendee]: That wasn’t under your task list for your department?

195
00:17:32,020 --> 00:17:34,020
[Todd]: It was, it was, yeah.

196
00:17:37,300 --> 00:17:40,160
[Attendee]: Do you have an accessible video player on your site?

197
00:17:40,920 --> 00:17:50,580
[Todd]: So the question was about an accessible video player. I know we are adding support for video captions;

198
00:17:50,580 --> 00:17:56,040
I don’t know where that is yet, in terms of if it is available. But there was work done for that.

199
00:17:57,460 --> 00:18:03,600
It’s not a Flash player, so its viewable on mobile. So those are two things that come to mind.

200
00:18:04,640 --> 00:18:12,620
[Dennis]: And just so you know, at United, we’re using Able Player, which is, I believe it’s open source.

201
00:18:12,620 --> 00:18:16,120
But if you just search on Able Player, you can find it.

202
00:18:16,120 --> 00:18:23,320
It can obviously just … bring in videos you have locally or from YouTube.

203
00:18:25,600 --> 00:18:30,760
[Attendee]: So once you supplied your color palette, can you go into the whole process?

204
00:18:30,760 --> 00:18:34,640
In my experience, a lot of times the UI designers and the graphic visual designers,

205
00:18:34,640 --> 00:18:40,820
they get kind of territorial about changing colors. So, when you were going through the process,

206
00:18:40,820 --> 00:18:46,580
just some of the reactions from the visual designers and user designers. I would just …

207
00:18:46,580 --> 00:18:50,620
my background was in that space and I always thought once you simplified the color palette,

208
00:18:50,620 --> 00:18:55,780
it makes things a hell of a lot easier, from a creative development perspective.

209
00:18:55,780 --> 00:19:01,520
I was wondering if you could share some of the insights into some of the learnings and growing pains.

210
00:19:01,520 --> 00:19:07,200
[Todd]: Yeah. Well, fortunately our visual designer Josh Osborne was very sympathetic to this,

211
00:19:07,200 --> 00:19:13,640
and so we would work over Slack or video calls, send screen shots back and forth,

212
00:19:13,640 --> 00:19:18,440
like hey, what do you think of this? Does this color look too different to you?

213
00:19:18,440 --> 00:19:27,360
And he was pretty willing to make changes, which really helped. Because, I know …

214
00:19:27,360 --> 00:19:32,580
[Attendee]: Is there any way, because it was somewhat hard in the projection, to see,

215
00:19:32,580 --> 00:19:37,720
is there anyway to get our hands on the this presentation, so I …?

216
00:19:37,720 --> 00:19:42,460
Sometimes, they’re just so subtle and sometimes you just need to show an example to a visual designer,

217
00:19:42,460 --> 00:19:45,820
to say look, we’re not asking you to change everything, such a subtle difference.

218
00:19:45,820 --> 00:19:51,080
Or it really doesn’t change the integrity of the design, it just makes it more accessible.

219
00:19:51,080 --> 00:19:53,460
Is there any way we can get the deck?

220
00:19:53,680 --> 00:19:58,460
[Dennis]: If you’re willing to share the deck out with attendees, we’ll get a link out to everyone.

221
00:19:58,460 --> 00:19:58,960
[Todd]: Sure.

222
00:19:58,960 --> 00:20:02,580
[Dennis]: I know I was going to ask for it for the video editing.

223
00:20:02,580 --> 00:20:03,780
[Todd]: Yeah, I’ll send it to you.

224
00:20:03,780 --> 00:20:06,460
[Dennis]: Cool. Any other questions?

225
00:20:09,760 --> 00:20:11,340
Thank you very much, Todd.

226
00:20:11,340 --> 00:20:14,900
[Applause]

