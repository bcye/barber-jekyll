---
layout: post
title: Create an App Store-ready iOS content blocker in under one hour without code.
---

Content blockers are awesome. They clean up the internet from classic advertisements, annoying paywalls and chat widgets.

One month ago I added ["Hello, Goodbye"](https://hellogoodbye.app) to the list of blockers to hide annoying chat widgets for Intercom and Co. The app is open source and it is what we will be making. [Find the finished app and source code here](https://github.com/bcye/Hello-Goodbye).

<!--kg-card-begin: hr-->
* * *
<!--kg-card-end: hr-->
## Step 1: Let's get started

_Skip this if you have used Xcode before._

First we need to set up your environment, so you can build the blocker:

- Download [Xcode](https://itunes.apple.com/de/app/xcode/id497799835?l=en&mt=12) from the Mac App Store
- This will take about 5 to 15 minutes, so go get some coffee or snacks and come back in a bit.
- Open Xcode and select "Create New Project"
<!--kg-card-begin: image--><figure class="kg-card kg-image-card"><img src="/content/images/2019/04/Screenshot-2019-04-21-at-13.50.44.png" class="kg-image"></figure><!--kg-card-end: image-->
- Make sure you have iOS selected and select Single View App
<!--kg-card-begin: image--><figure class="kg-card kg-image-card"><img src="/content/images/2019/04/Screenshot-2019-04-21-at-13.52.31.png" class="kg-image"></figure><!--kg-card-end: image-->
- Enter a project name and enter an organisation identifier in a format like this: _com.yourname_, choose where to save your project.
<!--kg-card-begin: image--><figure class="kg-card kg-image-card"><img src="/content/images/2019/04/Screenshot-2019-04-21-at-13.54.44.png" class="kg-image"></figure><!--kg-card-end: image-->
- You're not quite done yet: Go to File -\> New -\> Target
<!--kg-card-begin: image--><figure class="kg-card kg-image-card"><img src="/content/images/2019/04/Screenshot-2019-04-21-at-14.00.10.png" class="kg-image"></figure><!--kg-card-end: image-->
- Select Content Blocker Extension
<!--kg-card-begin: image--><figure class="kg-card kg-image-card"><img src="/content/images/2019/04/Screenshot-2019-04-21-at-14.01.06-1.png" class="kg-image"></figure><!--kg-card-end: image-->
- I recommend typing in BlockerExtension, but it does not matter really.
<!--kg-card-begin: image--><figure class="kg-card kg-image-card"><img src="/content/images/2019/04/Screenshot-2019-04-21-at-14.01.19-1.png" class="kg-image"></figure><!--kg-card-end: image-->
- Congrats you are ready to go!
<!--kg-card-begin: hr-->
* * *
<!--kg-card-end: hr-->
## Step 2: Block Stuff 🤘

_All you can block_

Open BlockerExtension/blockerList.json, you'll find a nice list that is written in JSON.

<!--kg-card-begin: image--><figure class="kg-card kg-image-card"><img src="/content/images/2019/04/Screenshot-2019-04-21-at-14.13.51.png" class="kg-image"></figure><!--kg-card-end: image-->

Blocking is very simple. Under url-filter you enter the URL you want blocked. That's it. There are some advanced options available for more fun, if simply blocking URLs is not enough for you, [check out Apple's documentation which has more detail.](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker)

You'll need to separate each block of action and trigger by a comma. After writing all your rules, this document should look something like [this.](https://github.com/bcye/Hello-Goodbye/blob/master/Safari/BlockerExtension/blockerList.json)

<!--kg-card-begin: image--><figure class="kg-card kg-image-card"><img src="/content/images/2019/04/Screenshot-2019-04-21-at-14.23.56.png" class="kg-image"></figure><!--kg-card-end: image-->

**Congratulations, you're done. 🎉** This was all you need to make a functional content blocker. If you want to make one that gets approved to the App Store,

