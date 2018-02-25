---
title:  Weekly Summary W6 (2.5-2.11)
comments: true
date: 2018-02-06 20:49:21
updated:
tags: Weekly Summary
categories: Weekly Summary
---

# WKWebview's UserAgent

## iOS Version more than iOS9:
``` swift
wkWebView.customUserAgent = "your agent"
```
## Any Version
``` swift
    let webview = UIWebView()
    var newUserAgent = webview.stringByEvaluatingJavaScript(from: "navigator.userAgent")
    newUserAgent = newUserAgent?.appending("custom user agent")
    let dictionary = Dictionary(dictionaryLiteral: ("UserAgent", newUserAgent))
    UserDefaults.standard.register(defaults: dictionary)
```

Refference:[Set useragent in WKWebview](https://stackoverflow.com/questions/26994491/set-useragent-in-wkwebview/27058024#27058024)

