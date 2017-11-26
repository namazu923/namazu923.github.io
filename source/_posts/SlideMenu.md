---
title: SlideMenu
comments: true
date: 2017-11-26 13:07:09
updated:
tags:
categories:
---

1. Create `containerViewController` containing both `mainNavigationViewController`(`mainViewController`'s NavigationController) and `slideMenuViewController`

	* 1.1 Child ViewController
		
		> let `mainNavigationViewController` and `slideMenuViewController ` be `containerViewController `'s childViewController
<!-- more -->
		* 1.1.1 Add Child ViewController  
		
			> containerView.addSubview(mainNavigationViewController.view)
addChildViewController(mainNavigationViewController)
mainNavigationViewController.didMove(toParentViewController: self)

		* 1.1.2 Remove Child ViewController

			>
slideMenuViewController.view.removeFromSuperView()
slideMenuViewController = nil


2. Add UIGestureRecognizer to `mainNavigationViewController`  
	* 2.1 Show State
		
		> judge slideMenuView's show state(show/ not show)  
	* 2.2 Dragging direction
	
		> get gesture's dragging direction by check whether  
	  `recognizer.velocity(in: view).x` is more or less than 0 
	* 2.3 Move view
		
		> move `recognizer.view` by setting `view.center.x` with `recognizer.translation(in: view).x`
	* 2.4 Receive Gesture Check
		> func gestureRecognizer(_ gestureRecognizer: UIGestureRecognizer, shouldReceive touch: UITouch) -> Bool {}
		>
		> func gestureRecognizerShouldBegin(_ gestureRecognizer: UIGestureRecognizer) -> Bool {}

   
	

--
Reference:   
[How to Create Your Own Slide-Out Navigation Panel in Swift](https://www.raywenderlich.com/177353/create-slide-navigation-panel-swift)