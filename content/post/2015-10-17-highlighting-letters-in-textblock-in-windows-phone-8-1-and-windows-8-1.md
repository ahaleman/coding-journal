---
title: Highlighting letters in TextBlock in Windows Phone 8.1 and Windows 8.1
author: Igor Kulman
layout: post
date: 2015-10-17
url: /highlighting-letters-in-textblock-in-windows-phone-8-1-and-windows-8-1/
twitterCardType:
  - summary
cardImageWidth:
  - 280
cardImageHeight:
  - 150
cardImage_id:
  - 1272
cardImage:
  - http://blog.kulman.sk/wp-content/uploads/2015/10/highlighting.png
dsq_thread_id:
  - 4233511341
categories:
  - Windows Phone
  - WinRT
tags:
  - 'c#'
  - Windows Phone
  - winrt
  - xaml
---
In my current project I had to implement an interesting feature for both Windows Phone 8.1 and Windows 8.1 project of the Universal app. The idea is simply. The users want to search for a movie. They enter a search term into a TextBox and a list of results is shown. The results should have the search term highlighted in them.

{{% img-responsive "/images/highlighting.png" %}}

<!--more-->

The standard TextBlock used to display the movie titles does not support any kind of letter highlighting, so I had to write a custom one. I created a custom UserControl. The UserControl contains a few dependency properties Text, HighlightedText, HighlightBrush and a TextBlock. When Text or HighlightedText change, the Text is then split into multiple Runs that are added to the TextBlock.

{{< gist 87b051f2f3a54bf895f0>}}

The whole working custom control is available at Github: <https://github.com/igorkulman/Kulman.WPA81.HighlightTextBox>.