---
title: class & static var in Swift 4
date: 2017-10-19 22:37:50
tags: Swift 4
---

>You define type properties with the <font color=blue>static</font> keyword. For <font color=blue>computed</font> type properties for class types, you can use the <font color=blue>class</font> keyword instead to <font color=blue>allow subclasses to override the superclass’s implementation</font>. The example below shows the syntax for stored and computed type properties:

```swift
struct SomeStructure {
    static var storedTypeProperty = "Some value."
    static var computedTypeProperty: Int {
        return 1
    }
}
enum SomeEnumeration {
    static var storedTypeProperty = "Some value."
    static var computedTypeProperty: Int {
        return 6
    }
}
class SomeClass {
    static var storedTypeProperty = "Some value."
    static var computedTypeProperty: Int {
        return 27
    }
    class var overrideableComputedTypeProperty: Int {
        return 107
    }
}
```


>NOTE

>The computed type property examples above are for read-only computed type properties, but you can also define read-write computed type properties with the same syntax as for computed instance properties.

Reference: [The Swift Programming Language (Swift 4)](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Properties.html)
