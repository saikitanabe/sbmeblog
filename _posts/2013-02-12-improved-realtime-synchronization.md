---
layout: post
title: "Improved Realtime Synchronization"
description: ""
category: 
tags: []
---
{% include JB/setup %}

Sketchboard.Me uses amazing Lift as it’s backend. However current Sketchboard.Me implementation has not been able to guarantee that synchronization between client boards is 100%. Especially when Sketchboard.Me works in Operational Transfer manner, it sends only changes not the whole board.

You might have suffered losing some of the changes, you are seeing different version of the board than your team mate. This could have happened due to number of different reasons and not for least because of bugs. But sometimes there are network failures, it cannot be guaranteed that all operations are delivered to all clients.

Sketchboard.Me is also going towards mobile devices. iPad is the first “mobile” device that Sketchboard.Me supports, it is possible to use Sketchboard.Me on iPad Safari and Chrome web browsers.

Another reason for lost operations on mobile devices might be power saving. Mobile devices shut down network traffic, if you are not using the device. The server cannot deliver operations for those devices during that time. Lift takes care automatically the situation when client session is dead - the board will be automatically reloaded, Lift does also amazing job to guarantee the delivery, but sometimes deliveries are lost.

To fix these lost deliveries and guarantee better board synchronization, Sketchboard.Me implements checksum with Operational Transform. It might not check every move that you do, because checksum calculation is little bit heavy. To keep client as responsive as possible, for your moves, as a compromise Sketchboard.Me will check the board checksum when user is not modifying the board. In case the client and the server checksum differs and the client has lost some operations, the board will reload. For now it just reloads the whole page, since it is still quite rare situation and as a user you will notice a page refresh.

Hopefully you will enjoy improved synchronization!

