# my_video_combine
合并MP4视频操作，看demo就会明白，这个当然是巴结丈母娘用的了

操作步骤：

1. windows系统，安装优酷（内置了ffmpeg） or 自己下载ffmpeg安装版安装。
2.  在视频文件目录下依次执行如下命令：（以优酷安装路径为例）

将下载的MP4文件转为ts裸流（视频解压缩）：
> "C:\Program Files (x86)\YouKu\YoukuClient\nplayer\ffmpeg.exe" -i 1.mp4  -vcodec h264   1.ts
> "C:\Program Files (x86)\YouKu\YoukuClient\nplayer\ffmpeg.exe" -i 1.mp4  -vcodec h264   1.ts

合并Ts裸流文件：
> copy /b "1.ts"+"2.ts" /y "combine.ts"

重新转换为MP4文件（视频压缩）：
> "C:\Program Files (x86)\YouKu\YoukuClient\nplayer\ffmpeg.exe" -i combine.ts -vcodec h264 combine.mp4
