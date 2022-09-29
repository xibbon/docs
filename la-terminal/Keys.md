---
layout: doc
title:  "Keys"
---

Keys play an important role with SSH clients, they provide a mechanism to log into remote systems securely.  Each key is made up of two components, the private key that must reside in your phone to access a remote system, and the public key that is added to your remote hosts in their `.ssh/authorized_keys` file.

To manage the keys that you use to connect hosts, go to the "Keys" section in La Terminal.   In there, you can either create new keys, import existing keys and delete keys.

<img width="564" alt="image" src="https://user-images.githubusercontent.com/36863/160485314-041c28a0-9b3d-4d62-9b3c-1a823b92bcd0.png">

## Create Enclave Key

In some iPhone and iPad models, you can create an SSH key that is stored in the Secure Enclave, ensuring that this key never leaves your device.   This is the most secure option as the private key is only ever known to your device.   

Enclave keys can not be moved to new devices, and they are always tied to your device. 

Creating the enclave key is very simple, merely select the Create Enclave Key button, and then optionally change the name of the key.   Once you have that key ready, you can export the public component of that key by tapping on the key.  This will open the iOS share sheet that will allow you to either AirDrop, send via Messages or copy the key into your clipboard.

You then need to add this file to the `.ssh/authorized_keys` on the host you want to access.

## Create Key

You can create SSH keys of type ED25519 or RSA keys of size 1024, 2048 or 4096.   By default there is no passphrase for these keys, but you can set one up here - if you choose to set a passphrase, you will need to enter the passphrase every time you connect.

## Adding an Existing Key

To add an existing key, you will fill this form:

<img width="564" alt="image" src="https://user-images.githubusercontent.com/36863/160486277-86e40476-024a-45e5-84d0-6a8643c3829c.png">

You should provide a name for your key to easily identify it, and you must at least provide the private key.   You can import the private key by either copying the file via your clipboard, or using the File selector icon that will let you bring a file with the private key that you have made accessible to your iPhone via the Files app.