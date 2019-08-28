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
可以使用Visual Studio 2010 或者更高版本，Vimba SDK 建议使用 2.1.3或者更高版本。
