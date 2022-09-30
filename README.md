# Daily Piano Miniatures

Every day I play a short piano piece as well as I can quickly learn it.

I want to:

1. Cache audio versions of everything in the [YouTube playlist](https://youtube.com/playlist?list=PLkuryjnRFclQJqoIVpk9W9-eIRswejo-R) in my own music collection
2. Publish each audio track, along with the text of its associated Twitter commentary, as a podcast episode

Whenever I remember, I run `download-new-mp3`. Whatever's new in the YouTube playlist compared to what's in Music.app gets downloaded to the current working directory and ID3-tagged. Then I drag the new MP3 files into Music.app, where they automatically land in the right place. This accomplishes (1).

Then I run `download-new-mp3` once more. Whatever's new in Music.app compared to what's in `audio/` gets copied in there with a web-ready filename. This gets me most of the way to (2). All that's left is to script something that pulls the right text out of Twitter.

## Annoyances

One time the YouTube Studio UI tricked me into uploading the same video a second time (because the first upload wasn't showing up). I deleted the duplicate, which turns out to be an unfetchable track 98. My script downloads YouTube tracks 99 and up as local tracks 98 and up, to keep the local numbering contiguous like a human person would expect.
