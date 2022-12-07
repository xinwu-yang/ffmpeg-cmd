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

### 使用ffmpeg截取指定时间的视频

```
ffmpeg.exe -i test.mp4 -codec copy -ss 00:00:00 -to 00:00:30 output.mp4
```

### 提取视频中的音频

```
ffmpeg -i demo.mp4 -vn -codec copy out.m4a
```

### 合并视频

```shell
ffmpeg.exe -f concat -i filelist.txt -c:v hevc_nvenc EKDV-273-HEVC.mp4
```

filelist.txt

```
file '1.mp4'
file '2.mp4'
```
