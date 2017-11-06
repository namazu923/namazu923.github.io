---
title: Points Versus Pixels
comments: true
date: 2017-11-06 20:43:13
updated:
tags: UI
categories: UI
---
In iOS there is a distinction between the coordinates you specify in your drawing code and the pixels of the underlying device. When using native drawing technologies such as Quartz, UIKit, and Core Animation, the drawing coordinate space and the view’s coordinate space are both logical coordinate spaces, with distances measured in <font color=blue>**points**</font>. These logical coordinate systems are decoupled from the device coordinate space used by the system frameworks to manage the <font color=blue>**pixels** onscreen</font>.

The system automatically maps points in the view’s coordinate space to pixels in the device coordinate space, but this mapping is not always one-to-one. This behavior leads to an important fact that you should always remember:

- **One point does not necessarily correspond to one physical pixel.**
<!-- more -->
The purpose of using points (and the logical coordinate system) is <font color=blue>to provide a consistent size of output that is device independent</font>. For most purposes, the actual size of a point is irrelevant. The goal of points is to provide a relatively consistent scale that you can use in your code to specify the size and position of views and rendered content. How points are actually mapped to pixels is a detail that is handled by the system frameworks. For example, on a device with a high-resolution screen, a line that is one point wide may actually result in a line that is two physical pixels wide. The result is that if you draw the same content on two similar devices, with only one of them having a high-resolution screen, the content appears to be about the same size on both devices.

>Note: In the context of PDF rendering and printing, Core Graphics defines "point" using the industry standard mapping of one point to 1/72 of an inch.

Reference:  
[Drawing and Printing Guide for iOS](https://developer.apple.com/library/content/documentation/2DDrawing/Conceptual/DrawingPrintingiOS/GraphicsDrawingOverview/GraphicsDrawingOverview.html)