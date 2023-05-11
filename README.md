# vtt2txt-html
simple vtt2txt html page with js to easily paste vtt (tested with Microsoft Stream transscript) to get a converted txt of the transcript.

no support is given for this simple ChatGPT-3.5 generated helper html page. I just needed a quick location to host this, while having the possible to not upload a VTT to some service. In case of issues, please direct them to the real non-human author :)

### example use
#### input:

```vtt
WEBVTT

abcd1234-abcd-efgh-5678-mnbvcxya9876-0
00:00:07.450 --> 00:00:15.012
Hello hello hello Hi I
already started the recording.

1234abcd-abcd-efgh-1234-mnavcxya9876-0
00:00:15.012 --> 00:00:23.770
Then lets start with our
meeting.
```

#### outputs:

```txt
Hello hello hello Hi I already started the recording.
Then lets start with our meeting.
```

### funfact:

I guess I did not saved, or atleast not more than 25% time by using ChatGPT-3.5 to generate this simple function convertVTTtoTXT() (mostly it saves me time). 
But I guess that only took a bit longer, since I did not properly declared the type of VTT (Microsoft Stream transscript) so the (hashes?) werent remove instantly, which are now removed by


```
/^\b[0-9a-f]{8}(?:-[0-9a-f]{4}){3}-[0-9a-f]{12}-\d+\b\s*\n+/gim
```

