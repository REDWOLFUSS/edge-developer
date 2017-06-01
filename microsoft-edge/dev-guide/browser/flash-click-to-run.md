---
description: Provide a seamless user experience on sites requiring Adobe Flash.
title: Dev guide - Flash Click-to-Run
author: erikadoyle
ms.author: edoyle
ms.date: 06/02/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, flash
---

# Flash Click-to-Run

Adobe Flash has been an integral part of the web for decades, enabling rich content and animations in browsers since before HTML5 was introduced. In modern browsers, web standards pioneered by Microsoft, Adobe, Google, Apple, Mozilla, and many others are now enabling sites to exceed those experiences without Flash and with improved performance and security. Working in partnership with other browser vendors and with Adobe, we strongly encourage developers to migrate to HTML5 standards including [Encrypted Media Extensions](https://developer.microsoft.com/en-us/microsoft-edge/platform/status/encryptedmediaextensions), [Media Source Extensions](https://developer.microsoft.com/en-us/microsoft-edge/platform/status/mediasourceextensions), [Canvas](https://developer.microsoft.com/en-us/microsoft-edge/platform/status/canvas), [Web Audio](https://developer.microsoft.com/en-us/microsoft-edge/platform/status/webaudioapi), and [Real-Time Communication](https://developer.microsoft.com/en-us/microsoft-edge/platform/status/webrtcobjectrtcapi).

As you transition toward HTML5 standards, there are a few simple things you can do to ensure that your users still have a positive experience visiting your website with Microsoft Edge in the Windows 10 Creators Update. 

If Flash is used on the page, but the user has not enabled it, Microsoft Edge will normally show a puzzle piece icon in the address bar as shown in [this blog](https://blogs.windows.com/msedgedev/2016/12/14/edge-flash-click-run/#41svu6EMwKIAaigx.97). If you are dynamically adding the Flash control after the page is loaded, this puzzle piece icon may not be displayed – in this case it is best to test for the presence of Flash and provide a link as described below.

To ensure that all users have a good experience, continue to test for the presence of Flash using your standard mechanisms. If Microsoft Edge reports that Flash is not available, present the [Flash download link](http://get.adobe.com/flashplayer) and [Flash download image](http://www.adobe.com/legal/permissions/icons-web-logos.html#flashplayer) to the user. When the user clicks on the link, Microsoft Edge (as well as other browsers) will present the necessary prompts to enable Flash Player for the site. The link must appear on the primary domain where you want Flash to be enabled. It won't work if you redirect users to pages on other domains.  [Here's a demo](https://microsoftedge.github.io/MicrosoftEdge-Documentation/flashclicktorun/) of the suggested experience and the corresponding [sample code](https://github.com/MicrosoftEdge/MicrosoftEdge-Documentation/tree/master/docs/flashclicktorun).