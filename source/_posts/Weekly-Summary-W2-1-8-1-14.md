---
title: Weekly Summary W2 (1.8-1.14)
comments: true
date: 2018-01-14 20:22:59
updated:
tags: Weekly Summary
categories: Weekly Summary
---
# iOS


## 1 WKWebView & JS

```swift
var dict = [String: Any]()
dict["msg"]  = "This is a message from Native"

let dataJson = try JSONSerialization.data(withJSONObject: dict, options: .WritingOptions())
let strJson  = String(data: dataJson, encoding: String.Encoding.UTF8)

wkWebView.evaluateJavaScript("webFunction('\(strJson)')")
```

### 1.1 WritingOption & ReadingOption

```swift
struct JSONSerialization.ReadingOptions 
```
>  Options used when creating Foundation objects from JSON data.

```swift
struct JSONSerialization.WritingOptions
```
> Options for writing JSON data
<!-- more -->
## 2 NotificationCenter

```swift
func addObserver(_ observer: Any, 
         selector aSelector: Selector, 
                 name aName: NSNotification.Name?, 
            object anObject: Any?)
```

> anObject
>> The object whose notifications the observer wants to receive; that is, only notifications sent by this sender are delivered to the observer.
If you pass nil, the notification center doesn’t use a notification’s sender to decide whether to deliver it to the observer.

```swift
func post(name aName: NSNotification.Name, 
     object anObject: Any?, 
  userInfo aUserInfo: [AnyHashable : Any]? = nil)
```
 
> aUserInfo
>> Optional information about the the notification.

## 3 Protocol in class
```swift
protocol aDelegate: class {

}
class A {
	weak var delegate: aDelegate?
} 
```
> In Swift, protocol will not only be class's but also structure and enums'  
> 
> So if we want to use a `weak` statement(class's statement),  
> we should add `: class` to designate it as a class's protocol.  
> 
> Otherwise we should add @objc between protocol as `@objc protocol`

## 4 Xcode
**Cmd + T**
> Add a new tab in Xcode

## 5 CocoaPods

> Alamofire  
> Kingfisher  
> SwiftyJSON  
> SVProgressHUD

Refference: [Top 10 Libraries for iOS Developers](https://www.raywenderlich.com/177482/top-10-ios-developer-libraries)
