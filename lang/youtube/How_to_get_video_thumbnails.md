---
title: How to get video thumbnails
keywords: [youtube]
---
First get the video id, this will be a string following '?v=' in the youtube
url. For example:
In `https://www.youtube.com/watch?v=vYvjDmcHpYU`, the video ID is `vYvjDmcHpYU`.

Now you can use ID with the following URL's to get all the different thumbnails.

-`http://img.youtube.com/vi/ID/0.jpg`
First image extracted from the video and image by default.
480x360 px, jpg

-`http://img.youtube.com/vi/ID/1.jpg`
Second image extracted from the video.
120x90 px, jpg

-`http://img.youtube.com/vi/ID/2.jpg`
Third image extracted from the video.
120x90 px, jpg

-`http://img.youtube.com/vi/ID/3.jpg`
Forth image extracted from the video.
120x90 px, jpg

-`http://img.youtube.com/vi/ID/default.jpg`
Thumbnail low res, same as 0.jpg.
120x90 px, jpg

-`http://img.youtube.com/vi/ID/mqdefault.jpg`
Thumbnail med low res, same as 0.jpg.
320x180 px, jpg

-`http://img.youtube.com/vi/ID/hqdefault.jpg`
Thumbnail med res, same as 0.jpg.
480x360 px, jpg

-`http://img.youtube.com/vi/ID/sddefault.jpg`
Thumbnail med hi res, same as 0.jpg.
640x480 px, jpg

-`http://img.youtube.com/vi/ID/maxresdefault.jpg`
Thumbnail hi res, same as 0.jpg.
Variable size (1920x1080 px / 1280x720 px .. ).jpg
