> [[Wiki|Home]] ▸ :beginner: [[Foundations]] ▸ **Pretty Good Privacy (PGP)**

It may surprise you to learn that the same encryption technologies useful for protecting the privacy of our messages like e-mails today were generally available as early as the 1980's. In 1991, Phil Zimmerman released a set of commercial products collectively called **PGP**, short for **Pretty Good Privacy**, to the early PC market ([watch this archival footage!](https://www.youtube.com/watch?v=qz718OZRA2A&t=553)) which set the standard for private communications for the next two decades. These days, you're more likely to hear the phrase "end-to-end encryption," but it's the same exact idea as way back then.

Unfortunately, it was not until well after [the Snowden leaks in 2013](https://en.wikipedia.org/wiki/Edward_Snowden#Global_surveillance_disclosures) that PGP actually became popular. Today, you can use a Free Software version of the PGP suite called **GnuPG** (or **GPG** for short) that is for all intents and purposes identical to the commercial version of the same software. Moreover, a number of companies such as [Keybase](https://keybase.io/) and [[ProtonMail]] have based their own privacy-enhancing products on the now license-free [**OpenPGP** standard, which is more formally known as RFC 4880](https://tools.ietf.org/html/rfc4880).

Like many other popular encryption technologies, PGP works by (metaphorically) creating a sharable digital lockbox for you along with a digital key that can be used to open the lockbox. When someone wants to send a private message to you, like an e-mail, they first download a copy of your digital lockbox, put their message inside that lockbox, lock it, and then send you the locked lockbox. Presumably, unless you have shared your digital key, only you can then open the lockbox and read the message. Obviously, if you share the key to your lockbox with someone else, or if an attacker gets a hold of your private key, they can also read messages that were locked with your digital lockbox, so it's important that your digital key remain private. The technical term for the lockbox is—confusingly—called a *public key*, while the technical term for the key to your lockbox is—much more appropriately—called a *private key*.

One of the reasons PGP is still around and is getting more popular is because it was designed to be a generic cryptosystem capable of protecting arbitrary information, not a specific product that only protected certain kinds of stuff. Thanks to this generality, you can use any PGP-compatible software to do things like password-protect individual files, automatically encrypt e-mail messages, verify the author of particular ("signed") messages to avoid spoofing, and even devise more complex secure sharing scenarios like requiring two out of three people who hold parts of the key to agree before any one of them can unlock something, a technique called [Secret sharing](https://en.wikipedia.org/wiki/Secret_sharing).

> [[Read next: GPG and PGP :arrow_right:|GPG and PGP]]