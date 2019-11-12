Vimba .NET 图像采集状态统计例程 - vmbnet_freerun_missing_frames_statistics
---

# 使用说明

对于Allied Vision 千兆网相机，如果需要了解其在某个系统上运行状态，可以使用Vimba SDK自带的Vimba Viewer软件进行查看，同时可以看到网络丢包及重传等情况。本程序代码使用于客户自己想编程了解Allied Vision工业相机，特别是USB 3.0相机的运行状态。



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
        `VmbFrameStatusFault = -4,`  
        `VmbFrameStatusInvalid = -3,`   
        `VmbFrameStatusTooSmall = -2,`    
        `VmbFrameStatusIncomplete = -1,`  
        `VmbFrameStatusComplete = 0`  
* Stamp: 相机拍摄图片时的时间戳，也就是相机感光芯片直接成像的时刻。
* StDiff: 与前一张图片时间戳的差。


# 代码及编译  
## 代码
在这里：https://github.com/avtcn/vmbnet_freerun_missing_frames_statistics
## 编译运行
可以使用[Visual Studio 2010](https://visualstudio.microsoft.com/) 或者更高版本，Vimba SDK 建议使用 [2.1.3或者更高版本](https://www.alliedvision.com/en/products/software.html)。
## 运行结果
```

/////////////////////////////////////////////////////////////
///                                                       ///
/// Vimba NET API Asynchronous Console Grab Example       ///
/// with missing/incomplete frames statistics functions   ///
///                                                       ///
/////////////////////////////////////////////////////////////

Vimba .NET API Version 1.7.0
Finding camera with ID: DEV_1AB2280009CC
Opening camera with ID: DEV_1AB2280009CC

Press <q> to stop acquisition...
Frame receiving ...


FrameID:0 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593166076520 StDiff:7593166076520 ClientFPS:0.7
FrameID:1 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593237275360 StDiff:71198840 ClientFPS:16.1
FrameID:2 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593308465590 StDiff:71190230 ClientFPS:15.9
FrameID:3 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593379655860 StDiff:71190270 ClientFPS:12.8
FrameID:4 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593450846090 StDiff:71190230 ClientFPS:16.1
FrameID:5 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593522036360 StDiff:71190270 ClientFPS:12.8
FrameID:6 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593593226590 StDiff:71190230 ClientFPS:15.9
FrameID:7 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593664416860 StDiff:71190270 ClientFPS:12.8
FrameID:8 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593735607090 StDiff:71190230 ClientFPS:15.9
FrameID:9 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593806797360 StDiff:71190270 ClientFPS:12.8
FrameID:10 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593877987590 StDiff:71190230 ClientFPS:12.8
FrameID:11 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7593949177860 StDiff:71190270 ClientFPS:16.1
FrameID:12 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594020368090 StDiff:71190230 ClientFPS:12.8
FrameID:13 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594091558360 StDiff:71190270 ClientFPS:15.9
FrameID:14 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594162748590 StDiff:71190230 ClientFPS:12.8
FrameID:15 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594233938860 StDiff:71190270 ClientFPS:15.9
FrameID:16 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594305129090 StDiff:71190230 ClientFPS:12.8
FrameID:17 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594376319360 StDiff:71190270 ClientFPS:16.1
FrameID:18 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594447509590 StDiff:71190230 ClientFPS:12.8
FrameID:19 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594518699860 StDiff:71190270 ClientFPS:12.8
FrameID:20 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594589890090 StDiff:71190230 ClientFPS:15.9
FrameID:21 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594661080360 StDiff:71190270 ClientFPS:12.8
FrameID:22 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594732270590 StDiff:71190230 ClientFPS:15.9
FrameID:23 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594803460860 StDiff:71190270 ClientFPS:12.8
FrameID:24 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594874651090 StDiff:71190230 ClientFPS:16.1
FrameID:25 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7594945841360 StDiff:71190270 ClientFPS:12.8
FrameID:26 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595017031590 StDiff:71190230 ClientFPS:15.9
FrameID:27 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595088221860 StDiff:71190270 ClientFPS:12.8
FrameID:28 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595159412090 StDiff:71190230 ClientFPS:12.8
FrameID:29 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595230602360 StDiff:71190270 ClientFPS:15.9
FrameID:30 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595301792590 StDiff:71190230 ClientFPS:12.8
FrameID:31 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595372982860 StDiff:71190270 ClientFPS:16.1
FrameID:32 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595444173090 StDiff:71190230 ClientFPS:12.8
FrameID:33 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595515363360 StDiff:71190270 ClientFPS:15.9
FrameID:34 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595586553590 StDiff:71190230 ClientFPS:12.8
FrameID:35 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595657743860 StDiff:71190270 ClientFPS:12.8
FrameID:36 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595728934090 StDiff:71190230 ClientFPS:15.9
FrameID:37 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595800124360 StDiff:71190270 ClientFPS:12.8
FrameID:38 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595871314590 StDiff:71190230 ClientFPS:16.1
FrameID:39 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7595942504860 StDiff:71190270 ClientFPS:12.8
FrameID:40 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596013695090 StDiff:71190230 ClientFPS:15.9
FrameID:41 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596084885360 StDiff:71190270 ClientFPS:12.8
FrameID:42 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596156075590 StDiff:71190230 ClientFPS:16.1
FrameID:43 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596227265860 StDiff:71190270 ClientFPS:12.7
FrameID:44 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596298456090 StDiff:71190230 ClientFPS:16.1
FrameID:45 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596369646360 StDiff:71190270 ClientFPS:12.8
FrameID:46 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596440836590 StDiff:71190230 ClientFPS:12.8
FrameID:47 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596512026860 StDiff:71190270 ClientFPS:15.9
FrameID:48 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596583217090 StDiff:71190230 ClientFPS:12.8
FrameID:49 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596654407360 StDiff:71190270 ClientFPS:16.1

Press <q> to stop acquisition..., The current date and time: 08-29-2019 13:29:31.490

FrameID:50 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596725597590 StDiff:71190230 ClientFPS:12.7
FrameID:51 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596796787860 StDiff:71190270 ClientFPS:16.1
FrameID:52 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596867978090 StDiff:71190230 ClientFPS:12.8
FrameID:53 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7596939168360 StDiff:71190270 ClientFPS:15.9
FrameID:54 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7597010358590 StDiff:71190230 ClientFPS:12.8
FrameID:55 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7597081548860 StDiff:71190270 ClientFPS:12.8
FrameID:56 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7597152739090 StDiff:71190230 ClientFPS:16.1
FrameID:57 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7597223929360 StDiff:71190270 ClientFPS:12.7
FrameID:58 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7597295119590 StDiff:71190230 ClientFPS:16.1
FrameID:59 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7597366309860 StDiff:71190270 ClientFPS:12.8
FrameID:60 [Missed: 0, Incomplete: 0]  Status:Complete Size:2592x1944 Format:VmbPixelFormatMono8 Stamp:7597437500090 StDiff:71190230 ClientFPS:15.9
q
Acquisition stopped. The current date and time: 08-29-2019 13:29:32.477
Press any Key to exit!



```




