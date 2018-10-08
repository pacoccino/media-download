# Media toolkit

## Media downloader

Based on [youtube-dl](https://github.com/rg3/youtube-dl)

`brew install youtube-dl`

### Run
`./download.sh TYPE URL`

TYPE = audio/video
URL = any video/song/playlist on youtube, soundcloud ...

## Command line tools

`brew install ..` will do the job

### Add 360 metadata to picture

`exiftool -ProjectionType="equirectangular" photo.jpg`

### Resize pictures
*Height 1500 and to jpg to all in current folder*

`mogrify -resize x1500 \*.jpg`

### Compress video
*Vary crf value depending on quality desired (the less the better)*

`ffmpeg -i alobato1.mp4 -vcodec libx264 -crf 22 c_alobato1.mp4`

### Image sequence to video

`ffmpeg -framerate 16 -i lboom-%05d.jpg out_16fps.mp4`
