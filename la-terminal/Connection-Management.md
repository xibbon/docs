---
layout: doc
title:  "Connection Management"
---
# La Terminal: Session Restoration
Both iOS and iPadOS are designed to preserve battery and reduce memory usage, which is fine for many use cases, but can be problematic for terminal emulators that are used for long-running sessions with remote hosts.   The problem is that iOS/iPadOS will terminate network connections shortly after a user switches to a different application.

To address this problem, La Terminal offers a number of options for users that want to perform long running operations, and you can choose one based on your specific needs.

* ### **Native** 
The default session preserving technique is called “native” and it works by running a small helper on your remote host that can re-establish your session transparently if the session is disconnected.   


    ***Pros:*** This option is great because it means that all the advanced terminal emulation capabilities of La Terminal continue to work and they are dumbed down at all. 


    ***Cons:*** if the operating system terminates “La Terminal” due to low-memory availability, your long running session will be terminate.

* ### **Tmux** 
With this option, La Terminal relies on the `tmux` command on your server to keep your session alive. 


    ***Pros:*** sessions survive across La Terminal being killed, or even your device rebooting.  Some users also enjoy the additional session management capabilities of `tmux`.


    ***Cons:*** the terminal emulation provided is the subset that tmux provides, and certain keystroke combinations are captured for `tmux` for management purposes, as well as the bottom of your screen contains some status information from tmux.

* ### **None** 
In this mode of operation, your connection will be terminated at the operating system discretion and the contents of your session will be lost.   


    If you have enabled location tracking, La Terminal will be kept alive even if it is send to the background, and your session will be preserved.


    ***Pros:*** your session will continue to run, even if your application is in the background, and has no dependencies on any server software.


    ***Cons:*** will consume additional energy from the battery.



