---
layout: doc
title:  "Connection Management"
---

To minimize battery consumption, iOS and iPadOS generally prevent applications from running in the background and give them a small amount of time to remain active when the application is not visible.

This poses a problem for users of terminal applications that context switch among different applications and could be frustrating to users.   La Terminal offers a couple of options to this problem: keeping the application alive via geo-location updates, or using terminal restoring capabilities using tmux.

The current version of La Terminal (anything available after April 11th, 2023) has a small band-aid that will keep connections alive for 30 seconds without using location tracking - this is as much as iOS will give us by default.

# Keeping La Terminal running with geo-location updates

iOS and iPadOS will keep an application running in the background if the application is receiving location notifications.   To use this feature, go to “Settings” and turn on the “Track Location” feature.    When you have connections established to a remote system, La Terminal will continue executing without terminating your connections.

The downside of this approach is that it shows a blue icon indicating that your location is being tracked and might consume more battery by keeping the application alive.

La Terminal does not upload, sell or publish this information, it all stays in your device.


# Restoring a session using Tmux

If the remote host you are connecting supports the `tmux` command, SwiftTerm can use tmux on first launch, and will reconnect automatically after it restarts to it.

For an optimal experience, it is best to have your host fully configured with a key that has its password already stored, to avoid entering your password every time you reconnect.

The downside of this approach is that you need `tmux` installed on the remote server, and that the `tmux` hot-key (typically control-b) is taken over by tmux, which can interfere for some users that might want to use that key for other purposes.
