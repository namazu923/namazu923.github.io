---
title: Human Interface Design
comments: true
date: 2018-01-23 19:39:40
updated:
tags: Design
categories: iOS
---

Refference: [Human Interface Guidelines](https://developer.apple.com/ios/human-interface-guidelines/user-interaction/authentication/)

# App Architecture

## Loading
* **Make it clear when loading is occurring**
* **Show content as soon as possible.**

## Modality
* **Keep modal tasks simple, short, and narrowly focused.**
<!-- more -->
## Onboarding
* **Get to the action quickly.**

	>If your app needs tutorials or intro sequences, provide a way to `skip` them and don't show them to returning users.

* **Anticipate the need for help.**

* **Stick to the essentials in tutorials.**
	> First and foremost, make your app `intuitive`. If too much guidance is needed, revisit the design of your app.

* **Make learning fun and discoverable.** 
	> Use `animation` and `interactivity` to teach gradually and in context. Avoid displaying screenshots that appear interactive.

## Settings
* **Provide shortcuts to Settings when appropriate.**

	> Refference: [Settings Launch URL](https://developer.apple.com/documentation/uikit/uiapplication/settings_launch_url)


# User Interaction
## 3D Touch
* **Provide action buttons when appropriate.**

	>  If your app already provides custom touch-and-hold actions for items, it’s good practice to include the same actions during peeks.
	
	> Avoid displaying button-like elements in a peek view. 

## Authentication
* **Delay sign-in as long as possible.**

	> People often abandon apps when they're forced to sign in before doing anything useful. Give them a chance to fall in love with your app before making a commitment to it.

* **Explain the benefits of authentication and how to sign up for your service.**
	>  If your app requires authentication, display a brief, friendly explanation on the login screen that describes the reasons for the requirement and its benefits. Also, remember that not everyone using your app has an account from the start. Make sure you explain how to get one, or provide a simple in-app way to sign up.
	
### Face ID and Touch ID
* **Whenever possible, support biometric authentication.**
* **Always identify the authentication method.**

	> A button for signing in to your app using Face ID, for example, should be titled `"Sign In with Face ID"` rather than "Sign In."
	
* **Reference authentication methods accurately.**
	> [LABiometryType](https://developer.apple.com/documentation/localauthentication/labiometrytype)
	
* **In general, avoid offering a setting for opting in to biometric authentication within your app.**
	> If biometric authentication is `enabled` at the system level, just `assume the user wants to use it`.

