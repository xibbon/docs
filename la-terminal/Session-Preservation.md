---
layout: doc
title:  "Session Preservation"
---

To preserve your battery, both iOS and iPadOS will suspend background applications, La Terminal requests the maximum amount of time to keep your connection open -about 30 seconds- but after this period, the connection will drop.

To address this problem, there are three possible solutions that you can use:

* ***Enable Location Tracking***: this will track your location while you use your application, so iOS will not suspend your terminal.   The information collected is only stored in your device and never leaves it.    The downside is that this could consume some of your battery when you could have been idling, and also displays a blue indicator which can be distracting.

* ***Native Restoration***: the native restoration installs a small executable on your host that keeps track of your connection, and can resume an existing connection on demand.   

* ***tmux restoration***: this is a variation of the native restoration, but uses a full-blown terminal emulator (tmux) that is ran on your remote host, and can be reconnected at a later time.   The only downside is that this is an emulator-within-an-emulator so some of the high-fidelity terminal capabilities of La Terminal are not available.