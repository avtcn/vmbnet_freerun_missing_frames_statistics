Vimba .NET 图像采集状态统计例程 - vmbnet_freerun_missing_frames_statistics
---

# 简介

VimbaNET_Examples\AsynchronousGrab-Console Example with missing/incomplete frames counting functions.  
基于VimbaNET_Examples\AsynchronousGrab-Console例程，增加图像接收统计功能。  
通过每张图片的连续递增序号以及每张图片的状态值来判断丢失或者不完整的图片数量。

# 例程使用说明

![Vmbnet-async-console-sample-missing-incomplete-frames-screenshot.png](Vmbnet-async-console-sample-missing-incomplete-frames-screenshot.png)
* FrameID: 自从相机上电运行后，每一张图片都具有一个连续递增的序列号。
* Missed: 已经累积丢失的图片数量。
* Incomplete: 已经累积收到的不完整图片数量。
例如，下面是主要的采图失败状态码：
```
    public enum VmbFrameStatusType
    {
        VmbFrameStatusFault = -4,
        VmbFrameStatusInvalid = -3,
        VmbFrameStatusTooSmall = -2,
        VmbFrameStatusIncomplete = -1,
        VmbFrameStatusComplete = 0
    }
```

# 代码及编译  
## 代码
在这里：https://github.com/avtcn/vmbnet_freerun_missing_frames_statistics
## 编译运行
可以使用[Visual Studio 2010](https://visualstudio.microsoft.com/) 或者更高版本，Vimba SDK 建议使用 [2.1.3或者更高版本](https://www.alliedvision.com/en/products/software.html)。
## 运行结果
```

///////////////////////////////////////////
/// Vimba API Asynchronous Grab Example ///
///////////////////////////////////////////

Vimba .NET API Version 1.7.0
Finding camera with ID: DEV_1AB2280009CC
Opening camera with ID: DEV_1AB2280009CC

Press <enter> to stop acquisition...
Frame received
FrameID:0 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:0.8
FrameID:1 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:21.3
FrameID:2 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:3 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:15.9
FrameID:4 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:5 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:15.9
FrameID:6 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:7 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:16.1
FrameID:8 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:9 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:10 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:15.9
FrameID:11 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:12 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:15.9
FrameID:13 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:14 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:16.1
FrameID:15 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:16 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:15.9
FrameID:17 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:18 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:19 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:15.9
FrameID:20 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:21 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:16.1
FrameID:22 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:23 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:15.9
FrameID:24 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:25 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:16.1
FrameID:26 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.7
FrameID:27 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:28 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:16.1
FrameID:29 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:30 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:15.9
FrameID:31 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:32 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:16.1
FrameID:33 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.7
FrameID:34 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:35 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:16.1
FrameID:36 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:37 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:15.9
FrameID:38 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.8
FrameID:39 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:16.1
FrameID:40 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:12.7
FrameID:41 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 FPS:16.1

Acquisition stopped.
Press any Key to exit!

```
