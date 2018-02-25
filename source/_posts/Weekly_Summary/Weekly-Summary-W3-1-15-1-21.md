---
title: Weekly Summary W3 (1.15-1.21)
comments: true
date: 2018-01-21 19:08:22
updated:
tags: Weekly Summary
categories: Weekly Summary
---
# Snap Kit
* SnapKit is also taking care of a few crucial steps in the process:

	1. Determining the best **common superview** to install the constraints on
	2. Ensuring `setTranslatesAutoresizingMaskIntoConstraints(false)` is called on all appropriate views.

* inset

	// make top = superview.top + 5, left = superview.left + 10,  
// bottom = superview.bottom - 15, right = superview.right - 20
```swift
make.edges.equalTo(superview).inset(UIEdgeInsets(top: 5, left: 10, bottom: 15, right: 20))```

* updateConstraints()

	```swift
override func updateConstraints() {
    
   // according to Apple super should be called at end of method
	 super.updateConstraints()
}
```

* topLayoutGuide & sageAreaLayoutGuide
	* `topLayoutGuide.snp.bottom` is similar to `topLayoutGuide.bottomAnchor` and you can also use `bottomLayoutGuide.snp.top` to align view on top of UITabBar.
	* Just like `topLayoutGuide` and `bottomLayoutGuide` using iPhone X’s new `safeAreaLayoutGuide`

Reference:[SNAPKIT](http://snapkit.io/docs/)

<!-- more -->

* Thinking About  **RemoveConstraints**

	> When remake more than two related view's constraints, fisrt removeConstraints to avoid old constraints's influence
	> 
	> classA.snp.makeConstraints()  
	> classB.snp.makeConstraints(edges.equalTo(classA))  
	> classC.snp.makeConstraints(edges.equalTo(classB))  
	
	> classA.snp.removeConstraints()  
	> classB.snp.removeConstraints()  
	> classC.snp.removeConstraints()  
	
	> classA.snp.remakeConstraints()  
	> classB.snp.remakeConstraints()  
	> classC.snp.remakeConstraints()

# Git
* git rebase -i (HEAD~3)

	> Commands:
	
	>> p, pick = use commit  
	> e, edit = use commit, but stop for amending  
	> s, squash = use commit, but meld into previous commit  
	> If you remove a line here THAT COMMIT WILL BE LOST.
However, if you remove everything, the rebase will be aborted.

* git log -10 --pretty=format:"%h %s"
* git filter-branch
	> Reference: [filter-branch](https://git-scm.com/book/zh/v1/Git-工具-重写历史)
* git add -u / git add . / git add -a
* git pull --rebase
	> Reference: [pull and pull --rebase](https://www.cnblogs.com/kevingrace/p/5896706.html)
* git reflog
	> Reference: [reflog](https://git-scm.com/book/zh/v1/Git-内部原理-维护及数据恢复)
* git stash show -p stash@{index}