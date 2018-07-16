http://www.ebookconverting.com/zip-up-an-epub-on-a-mac

There was a very cool blog post I found that shared how to zip up an ePUB properly. Unfortunately, last time I checked the link, the website had changed. The information was so useful to me that I thought I would try to reproduce their instructions. Although I am a PC girl, the instructions were for Mac, so that’s what I am using.

Open Terminal Services: Applications/Utilities/Terminal Services and go to your file – I usually put a folder on the desktop with the ePub file in it, so to get to it, I use the following:

`cd desktop/epub_folder`

If you are unzipping the folder, use this command:

`unzip epubfilename.epub`

(At this point, if you’re doing a fixed format file, you will put Apple’s display options file inside the META-INF folder. This is also the only way I know of to add audio and video files to an ePUB, and to make all the updates required to make these files work).

When you zip the ePub file back up, it’s important to zip an ePub up in the correct order. mimetype goes in first, with no compression. We’re also going to rename the file so we know we’re creating a new version. Here’s how:

`zip -X newepubname.epub mimetype`

Next up is the META-INF folder. You also want to suppress adding any MAC O/S .DS_Store files.

`zip -rg newepubname.epub META-INF -x \*.DS_Store`

Next is the OEBPS folder:

`zip -rg newepubname.epub OEBPS -x \*.DS_Store`

That’s it!

---
by ldespain, September 29, 2011
