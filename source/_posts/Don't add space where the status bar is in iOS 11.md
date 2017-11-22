---
title: Don't add space where the status bar is in iOS 11
comments: true
date: 2017-11-22 19:54:26
updated:
tags: iOS 11
categories: iOS
---

set` view.contentInsetAdjustmentBehavior = .never`

<!-- more -->

* About `contentInsetAdjustmentBehavior`  
		
	> This property specifies how the safe area insets are used to modify the content area of the scroll view. The default value of this property is automatic.
	
	* case **automatic**
		
		>Automatically adjust the scroll view insets.
		
	* case **scrollableAxes**
	
		> Adjust the insets only in the scrollable directions.

	* case **never**

		> Do not adjust the scroll view insets.
		
	* case **always**
	
		> Always include the safe area insets in the content adjustment.
		
Reference : 
	[contentInsetAdjustmentBehavior](https://developer.apple.com/documentation/uikit/uiscrollview/2902261-contentinsetadjustmentbehavior)