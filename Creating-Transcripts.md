# How to Create Transcript from Captions
## What are We Doing Here

The Chicago Digial Accessibility & Inclusive Design Meetup live streams most of their meetup events. Those recordings are then edited, then posted on their [YouTube Channel](https://www.youtube.com/c/chicagodigitalaccessibilityinclusivedesign). These videos are then sync'd with their captions. Finally, the caption files are formatted here for human and assistive technology consumption.

As the captions are finished for videos, they are placed in this GitHub repository, awaiting formatting into readible text in a markup called Markdown. You can find a [simple guide to Markdown here](https://guides.github.com/features/mastering-markdown/).

## How Do We Format the Text
A proper transcription does not have too many rules to follow. However, there are some things to note.

### Headings
Depending on the presentation, their may be sections of a talk that can be grouped by headings. These headings do not appear in the captions. This will just become apparent, likely after your done.

Headings are marked up usng hash or pound signs.
* One hash is the top page level heading (there's only one). IN HTML, this is the H1.
* Two hashs is the first level sub-heading, or an H2 in HTML.
* Three hashs is the second level sub-heading, or an H3 in HTML.
* Four hashs is the third level sub-heading, or an H4 in HTML.
* Five hashs is the fourth level sub-heading, or an H5 in HTML.
* Six hashs is the fifth level sub-heading, or an H6 in HTML.
Again, many transcripts do not have headings. Some do, as it makes sense. Remember that hedings assist individuals using assistive technology like screen readers how information is grouped, and provides a method of navigation.

### Who's Speaking?
You will need to watch the recording as you transcribe, to know who is speaking. In most cases, the captions provide this identifier. When a new person starts speaking, their identity needs to be called out. The individual's name is wrapped inside brackets "[]" with a colon and bolded (two asterisks on either side of the bolded text). Example:

**[Susan]:** Yeah

**[Anna]:** Of course

**[Sina]:** I'm being arbitrary, you spoke up first, in the front, to my right ...

By the way, and especially during Q&A sessions, you might not know who's speaking. That is complete understandable. Simply list them as "Attendee."

### Non-Spoken Sound
When ever there is non-spoken sound that relates to the presentation and that supports the transcribed text, such as laughter, applause, maybe music playing, this is presented in a simialr manner as when a new speaker is speaking.

**[Laughter]:**

**[Applause]:**

**[Music Playing]:**

## Example Conversion from Caption Format to Transcription Format
A caption file format includes the timings for syncing up with the video. As you format the caption text, you will remove these timing, as they are not needed. 

Here is an example of raw caption text and how it should look formatting for transcriptions.

### Caption Text

507
00:44:40,920 --> 00:44:41,919
How would we know?

508
00:44:41,920 --> 00:44:48,460
There would be no way for you to know how to use that unless you were following the design pattern to spec.

509
00:44:48,460 --> 00:44:51,500
Which we've all clearly noticed it's very hard to do.

510
00:44:51,500 --> 00:44:57,480
So, content strategists can add contextual information to help for accessibility.

### Transcription Text

**[Attendee]:** How would we know?

**[Seth]:** There would be no way for you to know how to use that unless you were following the design pattern to spec. Which we've all clearly noticed it's very hard to do. So, content strategists can add contextual information to help for accessibility.

## Last Thing
Once you've finished formatting the transcription, there are two final things to do:

* Add the Name of the presenter(s) and the date, as a H2 heading
* Add a link to the recording on YouTube

View some of the completed transcriptions for guidance here.

Once you're finished, drop me a line, via email or mssage theough the meetup.com site.

You're all set. Thank you for your assistance in making our meetup s inclusive and accessible as possible.
