---
title: Weekly Summary W8 (2.19-2.25)
comments: true
date: 2018-02-25 12:46:53
updated:
tags: Weekly Summary
categories: Weekly Summary
---
# placeholder in UITextField

``` swift
if let placeholderLabel = textField.value(forKey: "_placeholderLabel") as ? UILabel {
	placeholderLabel.adjustFontSizeToFitSize = true
}
```

<!-- more -->

# CLLocationManager
## Judge if current service is enabled
``` swift
CLLocationManager.locationServiceEnabled()
```
## Request authorization
``` swift
requestWhenInUseAuthorization()
```
## desiredAccuray
## distanceFilter

# Facebook share
Reference:
[share in iOS](https://developers.facebook.com/docs/sharing/ios)

# Twitter share
Reference:
[twitter-kit-iOS](https://github.com/twitter/twitter-kit-ios/wiki/Installation)

#Barcode
``` swift
AVCaptureDevice
```

# Open Settings URL
``` swift
UIApplication.shared.openURL(URL(String: UIApplicationOpenSettingsURLString)!)
```

# Deep Link

## Set URL scheme
> TARGET -> Info -> URL Types -> URL Schemes -> app url scheme

Reference:[Inter-App Communication](https://developer.apple.com/library/content/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Inter-AppCommunication/Inter-AppCommunication.html)

# Open another app
``` switch
if UIApplication.shared.canOpenURL(app_scheme_url) {
	UIApplication.shared.openURL(app_scheme_url)
} else {
	UIApplication.shared.openURL(app_sotre_url)
}
```

# Xcode Swift executable size much bigger than Objective-C executable

because swift executable file contains all framework files

Reference:[Xcode Swift executable size much bigger than Objective-C executable](https://stackoverflow.com/questions/28741895/xcode-swift-executable-size-much-bigger-than-objective-c-executable)
 