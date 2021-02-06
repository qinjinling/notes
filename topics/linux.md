# 视频剪辑
```bash
# transcode
ffmpeg -i input.mkv -codec copy output.mp4
# cut
# 画面声音不同步 ffmpeg -ss 00:02:00.0 -i input.mkv -t 30 -c copy output.mkv
ffmpeg -i input.mkv -ss 00:02:00.0 -t 30 -c copy output.mkv
# screenshot
ffmpeg -ss 00:30:14.435 -i input.mkv -vframes 1 out.png
```