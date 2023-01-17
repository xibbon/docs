---
layout: doc
title:  "Getting Started"
---

La Terminal is an SSH client for iOS and iPadOS, and you can use it to connect to remote Linux, Unix, Mac and Windows systems using the SSH protocol.

# Creating a Host

To use La Terminal, you start by defining a host that you want to connect to.   This is done by selecting "Hosts" from the launch screen, and then selecting "Add Host".   

<img width="564" alt="image" src="https://user-images.githubusercontent.com/36863/160483727-90e42faa-28f7-4773-af3a-b914004c3c8e.png">

Once you have selected to add a host, you can enter a memorable name for it, and you should provide both an address (can be a hostname, or an IP address) as well as a username to connect as:

<img width="564" alt="image" src="https://user-images.githubusercontent.com/36863/160483663-7dd8a5c9-73cd-4bea-809e-1600cf22f46b.png">

Then you should select what kind of authentication you want to use.   You can either use a password (and you can either provide it now, or provide it every time you login).   I strongly recommend that you use an SSH key instead, that will require an extra step documented below.

Save your host configuration.  At this point, if you selected the password option, you can just tap on the resulting host to connect to it, if you provided a password, it should connect you to your host, otherwise you will be prompted for the password.

For every new host, La Terminal will show you a fingerprint for the remote host - this is shown to ensure that you are connecting to the host you intended to, and not some system that might be pretending to be the host you are connecting to.   If in doubt, consult your network administrator to confirm that the fingerprint is correct.

# Adding SSH keys

To use SSH keys with La Terminal, you need to bring the private SSH component into your SSH keys.

Here are the options under "Keys":

<img width="564" alt="image" src="https://user-images.githubusercontent.com/36863/160484801-0b4a0157-3fa1-4a6d-9c8e-1a1efcbc5ee6.png">

See the page on [Keys](Keys) for detailed information about each option.
