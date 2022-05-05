# ffmpeg-cmd
常用的FFmpeg命令

### 指定流并转码和添加字幕
```
ffmpeg.exe -i '.\甲贺忍法帖 第02话 两幕胎动 [1080p].mkv' -map 0:a:1 -map 0:v:0 -c:v hevc_nvenc -c:a copy -vf "subtitles='2.ass'" 2.mp4
```
