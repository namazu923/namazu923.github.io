---
title: Make content search in Algolia
comments: true
date: 2017-10-22 18:19:36
updated:
tags: Algolia
categories: Hexo
---

Check the /node_modules/hexo-algolia/lib/command.js, when Algolia can't do search content by default.
<!-- more -->
And in the file, check var **INDEXED_PROPERTIES**, as if there is not a **'content'** value, add **'content'** in the array.
In git bash, do **'hexo clean'** to clean, and then **'hexo algolia'** to regenerate data objects to Algolia.

Try to search again.

Hexo-Next v5.1.3 & hexo-algolia : "^1.2.3",
