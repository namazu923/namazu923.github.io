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

## Data Entry

* **Dynamically validate field values.**  

	>  It’s frustrating when you have to go back and correct mistakes after filling out a lengthy form. Whenever possible, `check field values immediately after entry` so users can correct them right away.
	
* **Show a hint in a text field to help communicate purpose.**
	> A text field can contain placeholder text—such as "Email" or "Password"—when there’s no other text in the field. `Don’t use a separate label to describe a text field when placeholder text is sufficient`.
	
## Feedback
> Feedback helps people know what an app is doing, discover what they can do next, and understand the results of actions.

## File Handling
* **Don't provide an option to create local-only files.**
 
	> Users often expect all of their files to be available on all of their devices. Whenever possible, your app should support `cloud-based file storage through a service such as iCloud`.
	
## Gestures
* **Don’t block systemwide screen-edge gestures.**

## Undo and Redo
* **If you use the shake gesture for undo and redo, don’t use it for other actions.**

	> Although you can programmatically give multiple meanings to the shake gesture, you run the risk of confusing people and making your app unpredictable.

* **Provide undo and redo buttons sparingly.**

	> `It’s confusing when apps provide multiple ways to perform the same task`. If your app truly warrants dedicated undo and redo buttons, use the standard system-provided icons and put them in an expected location, such as a navigation bar.
	
* **Perform undo and redo operations in the current context only.** 
	
	> Undo and redo should have a clear and immediate effect on the `current context`, not an earlier one.
	
	
# System Capabilities

## Notifications
### Designing a Great Notification Experience
* **Don’t include your app name or icon.**

	> The system automatically shows this information at the top of each notification.
	
### Badging
* **Use badging for notification purposes only.**

	> Badges shouldn't be used to display other types of numeric information, such as air quality, dates, stock prices, or weather.
* **Keep badges up to date.**
	
	> `Update your app’s badge as soon as the corresponding information is read`. You don’t want people to think there’s new information available, only to find that they’ve already seen it. Note that `reducing a badge’s count to zero removes all related notifications from Notification Center`.
	
## Ratings and Reviews

* **Ask for a rating only after the user has demonstrated engagement with your app.**

	> For example, prompt the user upon the completion of a game level or productivity task. Never ask for a rating on first launch or during onboarding. `Allow ample time to form an opinion`.

* **Don’t interrupt the user, especially when they’re performing a time-sensitive or stressful task.**

* **Don’t be a pest.**
	> Repeated rating prompts can be irritating, and may even negatively influence the user’s opinion of your app. Allow `at least a week or two between rating requests` and `only prompt again after the user has demonstrated additional engagement with your app`.
	
### System Rating and Review Prompts
> The system offers a consistent, nonintrusive way for apps to request ratings and reviews. To use this feature, you simply identify places in your app's user experience where it makes sense to ask for feedback. If the user hasn't already given feedback and a request hasn't been made too recently, the system displays an in-app prompt that asks for a rating and an optional written review. The user can supply feedback or dismiss the prompt with a single tap. (In Settings, the user can also opt out of receiving these rating prompts for all apps they have installed.) `The system automatically limits the display of the prompt to three occurrences per app within a 365-day period`.

* **Prefer the system-provided prompt.**
* **Don't use buttons or other controls to request feedback.**
	
	> Since the system limits how often rating prompts occur, attempting to request feedback in response to a control may result in no rating prompt being displayed.

# Visual Design
## Adaptivity and Layout
### Layout Considerations
* **Provide ample touch targets for interactive elements.** 

	> Try to maintain a minimum tappable area of `44pt x 44pt` for all controls.
* **Be prepared for text-size changes.**
	> People expect most apps to respond appropriately when they choose `a different text size in Settings`. To accommodate some text-size changes, you might need to adjust the layout. For more information about text usage in your app, see [Typography](https://developer.apple.com/ios/human-interface-guidelines/visual-design/typography/).
	
## Color

R 255
G 59
B 48
Red
 
R 255
G 149
B 0
Orange
 
R 255
G 204
B 0
Yellow
 
R 76
G 217
B 100
Green
 
R 90
G 200
B 250
Teal Blue
 
R 0
G 122
B 255
Blue
 
R 88
G 86
B 214
Purple
 
R 255
G 45
B 85
Pink

* **Consider choosing a key color to indicate interactivity throughout your app.**
* **Avoid using the same color for interactive and noninteractive elements.**
* **Use sufficient color contrast ratios.**

	>  Insufficient contrast in your app makes content hard to read for everyone. Icons and text might blend with the background, for example. An online `color contrast calculator` can help you accurately analyze the color contrast in your app, to ensure that it meets optimal standards. Strive for a `minimum contrast ratio of 4.5:1`, although `7:1 is preferred `because it meets more stringent accessibility standards.
	
## Terminology
* **Avoid language that might sound patronizing.**

	> `Avoid we, our, me, and my` (for example "our tutorial" and "my workouts"). They're sometimes interpreted as insulting or patronizing.
	
* **Strive for an informal, friendly tone.**
	> An informal, approachable style echoes the way you speak with people over lunch. Use `contractions occasionally`, and `you and your` to address the user directly.
	
* **Refer to dates accurately.**
	>  It’s appropriate to use friendly terms like today and tomorrow, but these terms can be confusing or inaccurate if you don’t account for the current locale. Consider an event that starts just before midnight. In one time zone, the event may start today. In another time zone, the same event may have started yesterday. Generally, dates should reflect the time zone of the person viewing the event. However, in some cases, such as in a flight tracking app, it may be clearer to explicitly show the start date and time zone where the flight originates.

## Typography
* **Use built-in text styles whenever possible.**
	> [UIFontTextStyle](https://developer.apple.com/documentation/uikit/uifonttextstyle)
### Dynamic Type Sizes

# Icons and Images
## Image Size and Resolution
### Designing High-Resolution Artwork
* **Produce artwork in the appropriate format.**

	> In general, use de-interlaced `PNG files for bitmap/raster artwork`. PNG supports transparency and, because it's lossless, compression artifacts don't blur important details or alter colors. It's a good choice for intricate artwork that requires effects like shading, textures, and highlights. `Use JPEG for photos`. Its compression algorithm usually produces smaller sizes than lossless formats and artifacts are harder to discern in photos. `Photo-realistic app icons, however, look best as PNGs`. `Use PDF for glyphs and other flat, vector artwork that requires high-resolution scaling`.	
* **Provide alternative text labels for images and icons**
	>  Alternative text labels aren’t visible onscreen, but they let `VoiceOver` audibly describe what's onscreen, making navigation easier for people with visual impairments.
	
## App Icon
* **Use words only when they’re essential or part of a logo.**

	> An app’s name appears below its icon on the Home screen. Don’t include nonessential words that repeat the name or tell people what to do with your app, like "Watch" or "Play." If your design includes any text, emphasize words that relate to the actual content your app offers

* **Don’t place your app icon throughout the interface.**

	>  It can be confusing to see an icon used for different purposes throughout an app. Instead, consider incorporating your icon’s color scheme.
	
### App Icon Sizes
* Mimic your small icon with your App Store icon.

### Spotlight, Settings, and Notification Icons
> Every app should also provide a small icon that iOS can display when the app name matches a term in a Spotlight search. Additionally, apps with settings should provide a small icon to display in the built-in Settings app, and apps that support notifications should provide a small icon to display in notifications. All icons should clearly identify your app—ideally, they should match your app icon. `If you don’t provide these icons, iOS might shrink your main app icon for display in these locations`.

* **Don’t add an overlay or border to your Settings icon.**

	>  iOS automatically adds a 1-pixel stroke to all icons so that they look good on the white background of Settings.
	
### User-Selectable App Icons

## Custom Icons
* **Design icons as glyphs.**

	>  A glyph, also known as a template image, is a monochromatic image with transparency, anti-aliasing, and no drop shadow that uses a mask to define its shape. `Glyphs automatically receive the appropriate appearance—including coloring, highlighting, and vibrancy—based on the context and user interactions.` A variety of standard interface elements support glyphs, including navigation bars, tab bars, toolbars, and Home screen quick actions.
	
* **Prepare glyphs with a scale factor of @2x and save them as PDFs**

	> Because PDF is a `vector format` that allows for high-resolution scaling, it's typically sufficient to provide a single `@2x` version in your app and allow it to scale for other resolutions.

* **Make sure icons are legible.**

	> In general, `solid icons` tend to be clearer than outlined icons. If an icon must includes lines, coordinate the weight with other icons and your app's typography.

* **Use color to communicate selected and deselected states.**

	> Avoid toggling between two different icon designs, like a solid version and an outlined version.

* **Avoid including text in an icon.**

	> If you need text, display a label beneath the icon and adjust its placement accordingly.

### Custom Icon Sizes

* **Navigation Bar and Toolbar Icon Size**

	> Target sizes	Maximum sizes
	
	> 72px × 72px (24pt × 24pt @3x)	84px × 84px (28pt × 28pt @3x)
	
	> 48px × 48px (24pt × 24pt @2x)	56px × 56px (28pt × 28pt @2x)
	
* **Tab Bar Icon Size**

## Launch Screen

* **Design a launch screen that’s nearly identical to the first screen of your app.**

	>  If you include elements that look different when the app finishes launching, people can experience an unpleasant flash between the launch screen and the first screen of the app.
	
* **Avoid including text on your launch screen.**

	> Because launch screens are static, any displayed `text won’t be localized`.
	
### Static Launch Screen Images

## System Icons
### Navigation Bar and Toolbar Icons
### Home Screen Quick Action Icons

# Bars
## Navigation Bars
### Navigation Bar Controls
* **Give text-titled buttons enough room.**

	>  If your navigation bar includes multiple text buttons, the text of those buttons may appear to run together, making the buttons indistinguishable. Add separation by inserting a fixed space item between the buttons. For developer guidance, see the `UIBarButtonSystemItemFixedSpace` constant value in UIBarButtonItem.

* **Consider using a segmented control in a navigation bar to flatten your app's information hierarchy. **

	>  If you use a segmented control in a navigation bar, do so only at the top level of your hierarchy and be sure to choose accurate back-button titles at lower levels. For additional guidance, see Segmented Controls.
	
## Search Bars

* **Enable the Clear button.**

	> Most search bars include a Clear button that erases the contents of the field.
	
* **Enable the Cancel button when appropriate.**

	> Most dedicated search bars include a Cancel button that immediately terminates the search.

* **If necessary, provide hints and context in a search bar**

	> A search bar's field can contain placeholder text—like “Search Clothing, Shoes and Accessories” or simply “Search”—as a reminder of the context being searched. A succinct, one-line `prompt` with appropriate punctuation can also appear directly above a search bar to provide guidance. Stocks uses a prompt to let people know they can enter a company name or stock symbol.
	
* **Consider providing helpful shortcuts and other content below a search bar.**

	> Use the area under a search bar to help people get to content faster. Safari, for example, shows your bookmarks as soon as you tap the search field. Select one to go right to it without entering any search terms. Stocks shows a list of results as you type into the search field. Tap one at any time without typing any more characters.

###Scope Bars

## Status Bars

* **Consider temporarily hiding the status bar when displaying full-screen media.**
* **Avoid permanently hiding the status bar. **
	> Without a status bar, people must leave your app to check the time or see if they have a Wi-Fi connection. Let people redisplay a hidden status bar by using a simple, discoverable gesture. When browsing full-screen photos in the Photos app, a single tap shows the status bar again.
* **Use the status bar to denote network activity.**
	> When your app uses the network, especially for lengthy operations, show the network activity status bar indicator so people know activity is occurring. See `Network Activity Indicators`.

## Tab Bars

* **Don’t remove or disable a tab when its function is unavailable.**
	
	>  If tabs are available in some cases but not in others, your app’s interface becomes unstable and unpredictable. Ensure that `all tabs are always enabled, and explain why a tab’s content is unavailable`. For example, if there are no songs on an iOS device, the My Music tab in the Music app explains how to download songs. 

* **Use badging to communicate unobtrusively.**

	> You can display a badge—a red oval containing white text and either a number or an exclamation point—on a tab to indicate that new information is associated with that view or mode.

## Toolbars

* **Consider whether icons or text-titled buttons are right for your app.**

	> `Icons work well` when you need `more than three` toolbar buttons. When you have `three buttons or fewer`, `text can sometimes be clearer`. In Calendar, for example, text is used because icons would be confusing. The use of text also allows the Inbox button to show a count of calendar and event invitations.

* **Give text-titled buttons enough room.**

	> If your toolbar includes multiple buttons, the text of those buttons may appear to run together, making the buttons indistinguishable. Add separation by inserting fixed space between the buttons. For developer guidance, see the `UIBarButtonSystemItemFixedSpace` constant value in UIBarButtonItem.

### TIP
> It’s important to understand the difference between a toolbar and a tab bar, because both types of bars appear at the bottom of an app screen. A `toolbar` contains buttons for performing actions related to the `current context`, such as creating an item, deleting an item, adding an annotation, or taking a photo. A `tab bar` lets the user switch quickly between `different sections of an app`, for example, the Alarm, Stopwatch, and Timer tabs in the Clock app. See Tab Bars. Toolbars and tab bars never appear together in the same view.

# Views
## Action Sheets
* **Provide a Cancel button if it adds clarity.**

	> A Cancel button instills confidence when the user is abandoning a task. `Cancel buttons should always be included in action sheets at the bottom of the screen`.
	
* **Make destructive choices prominent.**

	> Use `red` for buttons that perform `destructive or dangerous` actions, and display these buttons at the `top` of an action sheet.
	
* **Avoid enabling scrolling in an action sheet.**

	> If an action sheet has too many options, people must scroll to see all of the choices. Scrolling requires extra time to make a choice and is hard to do without inadvertently tapping a button.

## Activity Views
* **Design simple template images to represent your custom activities.**

	> A template image uses a mask to create an icon. Use `black and white with appropriate transparency and antialiasing, and don’t include a drop shadow`. Template images should be centered in an area measuring about `70px × 70px`.

* **Make sure activities are appropriate for the current context.**

	> Although system-provided tasks can’t be reordered in an activity, they can be `excluded` if they aren’t applicable to your app. For example, to prevent people from printing images, you can exclude the Print activity. You can also identify which custom tasks to show at any given time.

* **Use the Action button to display an activity view.**

	> People are accustomed to accessing system-provided activities when they tap the Action button. Avoid confusing people by providing an alternative way to do the same thing.

## Alerts

* **Minimize alerts.**

	> Alerts disrupt the user experience and should only be used in important situations like confirming purchases and destructive actions (such as deletions), or notifying people about problems. The infrequency of alerts helps ensure that people take them seriously. Ensure that `each alert offers critical information and useful choices`.


### Alert Titles and Messages
* **Avoid sounding accusatory, judgmental, or insulting.**

	> People know that alerts notify them about problems and dangerous situations. As long as you use a friendly tone, it’s `better to be negative and direct than positive and oblique`. `Avoid` pronouns such as `you, your, me, and my`, which are sometimes interpreted as insulting or patronizing.

### Alert Buttons
* **Generally, use two-button alerts.**

	> Two-button alerts provide an easy choice between `two alternatives`. Single-button alerts inform, but give no control over the situation. Alerts with three or more buttons create complexity and can require scrolling, which is a bad user experience. `If you find that you need more than two choices, consider using an action sheet instead`. See Action Sheets.
	
* **Give alert buttons succinct, logical titles.**

	> The best button titles consist of one or two words that describe the result of selecting the button. As with all button titles, use `title-style capitalization and no ending punctuation`. To the extent possible, use `verbs and verb phrases` that relate directly to the alert title and message—for example, View All, Reply, or Ignore. Use `OK` for simple acceptance. `Avoid using Yes and No`.
	
* **Place buttons where people expect them.**

	> In general, buttons people are `most likely to tap should be on the right`. `Cancel buttons should always be on the left`.

* **Label cancellation buttons appropriately.**

	> A button that cancels an alert’s action should always be labeled `Cancel`.
	
* **Identify destructive buttons.**

	> If an alert button results in a destructive action, such as deleting content, set the button’s style to Destructive so that it gets appropriate formatting by the system. For developer guidance, see the UIAlertActionStyleDestructive constant of UIAlertAction. Additionally, provide a Cancel button so people can safely opt out of the destructive action. `Make the Cancel button bold by marking it as the default button`.
	
## Collections
* **Consider using a table instead of a collection for text.**

	> It’s generally simpler and more efficient to view and digest textual information when it’s displayed in a scrollable list.
	
* **Image Views**

	> NOTE
	
	> An image that’s been configured as a template image discards its color and adopts any tint that’s been applied to the enclosing image view. See Custom Icons. For developer guidance, see `UIImageRenderingModeAlwaysTemplate` in UIImage.
	
## Pages
* **If appropriate, implement a way to navigate nonlinearly.**


## Scroll Views
* **Consider showing a page control element when a scroll view is in paging mode.**

	> A page control shows how many pages, screens, or other chunks of content are available and indicates which one is currently visible. `If you show a page control with a scroll view, disable the scrolling indicator on the same axis to avoid confusion`. For additional guidance, see Page Controls.

## Tables

* **Begin showing table content quickly.**

	> Don’t wait for extensive table content to load before showing something. Fill onscreen rows with textual data immediately and show more complex data—such as images—as it becomes available. This technique `gives people useful information right away` and increases the perceived responsiveness of your app. In some cases, showing stale, older data may make sense until fresh, new data arrives.

* **Communicate progress as content loads.**

	> If a table’s data takes time to load, show a progress bar or spinning activity indicator to reassure people that your app is still running.
	
* **Keep content fresh.**

	> Consider updating your table’s content regularly to reflect newer data. Just don’t change the scrolling position. Instead, add the content to the beginning or end of the table, and let people scroll to it when they’re ready. Some apps display an indicator when new data has been added, and provide a control for jumping right to it. It’s also a good idea to include a refresh control, so people can manually perform an update at any time. See Refresh Content Controls.

* **Avoid combining an index with table rows containing right-aligned elements.**

	> An index is controlled by performing large swiping gestures. If other interactive elements reside nearby, such as disclosure indicators, it may be difficult to discern the user’s intent when a gesture occurs and the wrong element may be activated.

### Table Rows

* **Provide feedback when a selection is made.**

	> People expect a row to highlight briefly when its content is tapped. Then, people expect a new view to appear or something to change, such as a checkmark appearing, that indicates a selection has been made.
	
## Text Views

* **Show the appropriate keyboard type.**

	> iOS provides several different keyboard types, each designed to facilitate a different type of input. To streamline data entry, the keyboard displayed during the editing of a text view should be appropriate for the type of content in the field. For a complete list of available keyboard types, see the UIKeyboardType constant of UITextInputTraits.

## Web Views

* **Enable forward and back navigation when appropriate.**

	> Web views support forward and back navigation, but this behavior is disabled by default. If people will use your web view to visit multiple pages, enable forward and back navigation, and provide corresponding controls to initiate these features.

# Controls

## Buttons
### System Buttons
* **Use verbs in titles.**

	> An action-specific title shows that a button is interactive and says what happens when you tap it.

* **Use title-case for titles.**

	> Capitalize every word except articles, coordinating conjunctions, and prepositions of four or fewer letters.
	
* **Keep titles short.**

	> Overly long text can crowd your interface and may get truncated on smaller screens.

### Detail Disclosure Buttons

* **Use Detail Disclosure buttons appropriately in tables.**

	> When a Detail Disclosure button is present in a table row, tapping the button shows additional information. Tapping elsewhere selects the row or results in app-defined behavior. If you want people to tap the entire row to see additional detail, don’t use a Detail Disclosure button. Instead, use a detail disclosure accessory control, which appears as a chevron. See UITableViewCellAccessoryType in UITableViewCell.

## Edit Menus

* **Show appropriate commands for the current context.**

	> By default, the options include Cut, Copy, Paste, Select, Select All, and Delete commands, any of which can optionally be disabled. If nothing is selected, the menu shouldn’t show options that require a selection, such as Copy or Cut. Similarly, the menu shouldn’t have a Select option if something is already selected.
	
* **Adjust placement of edit options, if necessary.**

	> By default, the menu is positioned above or below the insertion point or selection, depending on available space, and includes a pointer to the related content. Although you can’t change the shape of the menu, its position is configurable—you can prevent it from covering important content or parts of your interface.

* **Don’t implement other controls with the same functionality as the edit menu.**

	> Providing multiple ways to initiate an operation results in an inconsistent user experience and leads to confusion. `If your app lets people use the menu to copy content, for example, don’t implement a copy button too`.
	
* **Don’t add edit options to a button.**

	> If you do this, people attempting to reveal the options will end up activating the button instead.
	
* **Make edit operations undoable.**

	> The menu doesn’t require confirmation before its actions are performed. Because someone could change their mind after performing an operation, `always implement undo and redo support`.
	
* **Expand edit options with useful custom commands.**

	> You can add value by providing additional app-specific commands. Like the standard commands, any custom commands should operate on selected text or objects.
	
* **Show custom commands after the system-provided ones.**

	> Don’t intersperse custom commands with the system-provided ones, which are well known and frequently used.

* **Minimize the number of custom commands.**

	> Don’t overwhelm people with too many choices.
	
* **Keep custom command names short.**

	> Command names should be verbs or short verb phrases that succinctly describe the action to be performed. Use title-style capitalization—capitalize every word except articles, coordinating conjunctions, and prepositions of four or fewer letters.


## Page Controls

* **Don’t display too many pages.**

	> More than about 10 dots are hard to count at a glance, and more than about 20 open pages are time-consuming to visit in sequence. If your app needs to display more than 20 pages as peers, consider using a different arrangement—such as a `grid`—that enables nonsequential navigation.

* **Center page controls at the bottom of the screen.**

	> A page control should always be centered and positioned `between the bottom of the content and the bottom of the screen`. This keeps it visible, without blocking content.


## Pickers

* **Use predictable and logically ordered values.**

	> Many values in a picker may be hidden when the scrollable lists are stationary. It's best when people can predict what these values are, such as with a list of alphabetized countries, so they can move through the lists quickly.

* **Use a table instead of a picker for large value lists.**

	>  Long lists can be tedious to navigate in a picker. A table has adjustable height and can include an index, making scrolling much faster.
	
## Progress Indicators

###Activity Indicators**

* **Favor progress bars over activity indicators.**

	> If activity is `quantifiable`, use a progress bar instead of an activity indicator so people can better gauge what’s happening and how long it will take.

* **If it’s helpful, provide useful information while waiting for a task to complete.**

	> Include a label above an activity indicator to give extra context. Avoid vague terms like loading or authenticating because they don’t usually add any value.

### Progress Bars
* **Always report progress accurately.**

	> Don’t display inaccurate progress information just to make your app appear busy. Only use progress bars for tasks that are quantifiable. Otherwise, use an activity indicator.
	
* **Hide the unfilled portion of track in navigation bars and toolbars.**

	> By default, a progress bar’s track includes both filled and unfilled portions. When used in a navigation bar or toolbar, such as to denote a page loading, a progress bar should be configured to hide the unfilled portion of the track.
	
### Network Activity Indicators
* **Show this indicator only for network operations lasting more than a few seconds.**

	> Don’t display the indicator for quick network operations because it’s likely to disappear before anyone notices its presence or realizes what it’s meant to communicate.
	
## Refresh Content Controls
* **Perform automatic content updates.**

	> Although people appreciate being able to trigger an immediate content refresh, they also expect automatic refreshes to occur periodically. Don’t make users responsible for initiating every update. Keep data fresh by updating it regularly.
	
* **Supply a short title only if it adds value.**

	> Optionally, a refresh control can include a title. In most cases, this is unnecessary, as the animation of the control indicates that content is loading. If you do include a title, don’t use it to explain how to perform a refresh. Instead, `provide information of value about the content being refreshed`. A refresh control in Podcasts, for example, uses a title to tell people when the last podcast update occurred.
	
## Segmented Controls

* **Limit the number of segments to improve usability.**

	> Wider segments are easier to tap. On iPhone, a segmented control should have `five or fewer segments`. 
	
* **Try to keep segment content size consistent.**

	> Because all segments have equal width, it doesn’t look great if content fills some segments but not others.
	
* **Avoid mixing text and images in a segmented control.**

	> Although individual segments can contain text or images, mixing the two in a single control can lead to a disconnected and confusing interface.
	
## Sliders

* **Don’t use a slider to adjust audio volume.**

	> If you need to provide volume control in your app, use a volume view, which is customizable and includes a volume-level slider and a control for changing the active audio output device. To learn about implementing a volume view, see MPVolumeView.
	
## Switches

* **Use switches in table rows only.**

	> Switches are intended for use in tables, such as in a list of settings that can be toggled on and off. If you need similar functionality `in a toolbar or navigation bar, use a button instead`, and `provide two distinct icons that communicate the states`.

## Text Fields

* **Show a hint in a text field to help communicate purpose.**

	> A text field can contain placeholder text—such as "Email" or "Password"—when there’s no other text in the field. Don’t use a separate label to describe a text field when placeholder text is sufficient.
	
* **Display a Clear button in the right end of a text field when appropriate.**

	> When this element is present, tapping it clears the contents of the text field, eliminating the need to keep tapping the Delete key.
	
* **Use secure text fields when appropriate.**

	> Always use a secure text field when your app asks for sensitive data, such as a password.
	
* **Use images and buttons to provide clarity and functionality in text fields.**

	> You can display custom images in the left or right sides of a text field, or you can add a system-provided button, such as the Bookmarks button. In general, use the left end of a text field to indicate a field’s purpose and the right end to indicate the presence of additional features, such as bookmarking.