# FFmpeg一些常用命令

### 指定流并转码和添加字幕

```
ffmpeg.exe -i '.\甲贺忍法帖 第02话 两幕胎动 [1080p].mkv' -map 0:a:1 -map 0:v:0 -c:v hevc_nvenc -c:a copy -vf "subtitles='2.ass'" 2.mp4
```

### 将多声道音频转为双声道

```
ffmpeg.exe -i .\毒液2.2021.BD1080P.x264.CHS-ENG.BTSJ5.mp4 -ac 2 -acodec aac -vcodec copy -preset veryfast dy.mp4
```

### 使用ffprobe分析视频并将结果序列化为Json

```
ffprobe -v quiet -print_format json -show_format -show_streams H:\Demo\Demoh264.mp4
```
