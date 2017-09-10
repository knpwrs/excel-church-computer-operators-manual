# Media Prep

## Videos

The following `ffmpeg` command will prepare videos for our projection setup:

```
ffmpeg -i input.mp4 -filter:v "scale=1920:1080, crop=1920:650:0:215, pad=1920:1080:0:0" output.mp4
```

Breaking it down:

1. `ffmpeg -i input.mp4` - `ffmpeg` will read the video file `input.mp4`.
1. `-filter:v "` - Specify video filters for `ffmpeg`.
1. `scale=1920:1080, ` - Scales the video to `1080p`. Lots of videos are still `720p`. This is not necessary when working with a video that is already `1080p`.
1. `crop=1920:650:0:215, ` - Crops the video to `1920x650` (our visible projection resolution) cutting off the top and bottom `215` pixels. `0:215` specifies the top-left corner of the crop box.
1. `pad=1920:1080:0:0" ` - Pads the video back out to `1080p` placing black bars in the remaining space. `0:0` specifies putting the video in the top-left corner of the resulting `1080p` image, leaving `430` pixels of black bar on the bottom.
1. `output.mp4` - Tells `ffmpeg` to write the resulting video file to `output.mp4`.

### Pillar Box

Alternatively, use the following `ffmpeg` command to pillar-box a video for our projection setup:

```
ffmpeg -i input.mp4 -filter:v "scale=1156:650,pad=1920:1080:382" output.mp4
```
