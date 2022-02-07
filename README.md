# FFMPEG Shortcuts

[ffmpeg](https://www.ffmpeg.org/) is awesome! It a complete command line solution record, convert and stream audio and video. 

I mostly use it to quickly convert / compress video files, but I always forget the commands 😕. So I made a few "shortcut" Bash scripts that use (an already installed) ffmpeg that quickly perform the task I want.

### Installation

1. Clone this repo: `git clone https://github.com/Thisura98/ffmpeg-shortcuts.git`
2. cd ffmpeg-shortcuts
3. chmod +x ffmov && chmod +x ffmp4
4. cp ffmov /usr/local/bin/ffmov
5. cp ffmp4 /usr/local/bin/ffmp4

### Shortcuts

#### ffmp4 

Compresses MP4 videos using its filename and quality parameters. The output file is always "filename_c.mp4". Quality parameter is between 0 and 51, where 51 is most compression.

```
ffmp4 my_video.mp4 20
```

#### ffmov

Compresses MOV videos using its filename and quality parameters. The output file is always "filename_c.mov". Quality parameter is between 0 and 51, where 51 is most compression.

```
ffmov my_video.mov 20
```


### Notes

1. The compression utilities use [the "crf" flag](https://trac.ffmpeg.org/wiki/Encode/H.264). It is a scale between 0–51. 0 means you don't do any comprssion, 51 means most compression.