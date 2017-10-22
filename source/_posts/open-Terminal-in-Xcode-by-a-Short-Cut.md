---
title: open Terminal in Xcode by a Short Cut
comments: true
date: 2017-10-22 21:10:39
updated:
tags: Short Cut
categories: Xcode
---

At first, we should prepare a **script** to open the Terminal.

{% note info %}
To prepare the script:  
In Terminal, use `vi script.sh(e.g.)` to create the script with content:  

`#! /bin/bash`
`open -a Terminal .`

Press colon WQ to exit.  
Then Type `chomd +x script.sh` to make the script executable.
{% endnote %}
<!-- more -->
In Xcode, do **'Cmd + Comma'** to open the **Preference** window. Then select the **Behaviors** tab.  

At the left list's bottom, add a new Custom Behavior called 'open Terminal(e.g.)'. Then click the right Command button, set a command **'Ctrl + Cmd + T (e.g.)'** as the short cut .  
![](https://github.com/namazu923/namazu923.github.io/blob/hexo/source/images/open-Terminal-in-Xcode-by-a-Short-Cut/CustomBehavior.jpeg?raw=true)

Check **Run** at the bottom of right area, then select **script.sh** and close Preference window.

Now, when you do **'Ctrl + Cmd + T'** in Xcode, a Terminal with current project's path will show.


Done with **Xcode 9**

