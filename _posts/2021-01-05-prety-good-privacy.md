---
layout: post
title: PGP - Pretty Good Privacy
---


On a Mac computer, you could use `gpg` (version 2.2.1) to setup pgp keys


[kbpgp](https://keybase.io/kbpgp) is Keybase's implementation of PGP in JavaScript. Check out [In the wild](https://keybase.io/kbpgp/docs/in_the_wild) section to find some browser based PGP key generation services.


A great resource for PGP best practices: <https://riseup.net/en/security/message-security/openpgp/best-practices>

According to the best practices listed above, It is a good idea to set an expiry date of less than 2 years.

> People think that they don’t want their keys to expire, but you actually do. Why? Because you can always extend your expiration date, even after it has expired! This “expiration” is actually more of a safety valve or “dead-man switch” that will automatically trigger at some point. If you have access to the secret key material, you can untrigger it. The point is to setup something to disable your key in case you lose access to it (and have no revocation certificate).

## How to change/extend an expiry date?

You may change/extend the expiry date even after the expiry date has passed on a pgp key.

Follow these steps to update the expiry date:

`gpg --list-keys`

`gpg --edit-key (key id)`

Edits the primary key.


`gpg> expire`

Set expiry date based on prompts.


To set the expiry date of the subkey, do the following

`gpg> key 1`
`gpg> expire`


`gpg> save`

Remember to save so that the key gets saved under the ~/.gnupg
Come out of the gpg prompt. Once updated, listing keys would display the udpated expiry date.

This is how the listing looks after the update.


Once both the primary and subkey are udpated, you could send them over to the PGP server.

`gpg --keyserver pgp.mit.edu --send-keys (key id)`



Search for a key on [pgp.mit.edu](http://pgp.mit.edu/)

```
Search results for '0x248e6aa86bb4c388'
Type bits/keyID     Date       User ID
pub  2048R/6BB4C388 2017-10-30 Kiran Adapa <***@gmail.com>
```



Use Encryption in GMail:

- <https://flowcrypt.com/>
- <https://www.mailvelope.com/en> 

