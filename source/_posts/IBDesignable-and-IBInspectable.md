---
title: '@IBDesignable and @IBInspectable'
date: 2017-10-21 13:05:41
tags: StoryBoard
categories: Interface Builder
---

@IBDesignable and @IBInspectable is used for **Live Rendering** in Interface Builder
{% note info %}
You can use two different attributes—@IBDesignable and @IBInspectable—to enable live, interactive custom view design in Interface Builder.

<!-- more -->
When you create a custom view that inherits from the UIView class or the NSView class, you can add the <font color=blue>@IBDesignable</font> attribute just before the class declaration. After you add the custom view to Interface Builder (by setting the custom class of the view in the inspector pane), Interface Builder renders your view in the canvas.

You can also add the <font color=blue>@IBInspectable</font> attribute to properties with types compatible with user defined runtime attributes. After you add your custom view to Interface Builder, you can edit these properties in the inspector.
{% endnote %}

```swift
@IBDesignable
class MyCustomView: UIView {
@IBInspectable var textColor: UIColor
@IBInspectable var iconHeight: CGFloat
// ...
}
```
***
Reference:
[<font color=blue>Live Rendering</font>](https://developer.apple.com/library/content/documentation/Swift/Conceptual/BuildingCocoaApps/WritingSwiftClassesWithObjective-CBehavior.html)
[<font color=blue>Implement a Custom Control</font>](https://developer.apple.com/library/content/referencelibrary/GettingStarted/DevelopiOSAppsSwift/ImplementingACustomControl.html)
[<font color=blue>WWDC2015: Implementing UI Designs in Interface Builder</font>](https://developer.apple.com/videos/play/wwdc2015/407/)
[<font color=blue>IBDesignable和IBInspectable</font>](http://www.jianshu.com/p/83161b02b792)
