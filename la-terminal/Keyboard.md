---
layout: doc
title:  "Keyboard"
---

La Terminal extends the standard iOS keyboard with a custom accessory that provides both some common shortcuts to characters that are used when logging into Unix systems, as well as a couple of important toggles:

![image](https://user-images.githubusercontent.com/36863/160489442-5cb12217-8c44-4804-8943-34566a6c4a31.png)

In addition there is a keyboard icon at the top of the navigation bar - that keyboard icon will toggle the visibility of the iOS keyboard on and off, for cases where you need more screen real estate.

# ESC key

This sends the escape key to the remote host.   Some applications understand the combination ESC+letter to mean alt-letter or meta-letter.

# Control Key

When you press this key, the next letter entered will be turned into the equivalent control sequence.   So pressing Control then A, will send the control-A sequence to the remote end, and will then automatically revert the state of the control key.

# Arrow keys

The arrow keys are mapped to the cursor keys and can be used for navigation.

# Finger Icon

This toggles the behavior of touches on the terminal, but it depends on the kind of application that is running.

On the default state of the terminal, motion gestures on the terminal will translate into scrolling the history buffer back and forth, but if you turn on this button, panning gestures will be translated into cursor moving operations.   When you are in this mode, the cursor operation will be repeated as long as you keep on moving your finger on the screen without lifting and the direction of your finger will be converted to one of left, right, up or down movements.

When the terminal is running a mouse aware (touch aware in this case) application, the default will send the pan gestures as cursor movement, otherwise they are used to trigger the selection mechanism.

# Keyboard Icon

The rightmost icon with a keyboard when toggled, will replace the standard iOS keyboard with keys that are frequently used by terminal users:

<img width="412" alt="image" src="https://user-images.githubusercontent.com/36863/160489619-5cfbf40c-0f51-42c9-b783-63e417af7646.png">

