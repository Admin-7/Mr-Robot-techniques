> [[Wiki|Home]] ▸ **GPG and PGP**

> :construction: TK-TODO: Make this better.

A GPG key is a cryptographic mechanism used for encryption and verification in a myriad of circumstances. It's a generic method of encryption and verification that can be applied from anything from e-mail and file encryption to commit signing.

A GPG/PGP key is really one thing in two "pieces," known as a **key pair.** A key pair is called a pair because it includes two parts: a **public key** and a **private key**. The public key is just what it sounds like: this is the one you can share with the world. It's perfectly safe for that key to find its way onto other servers or be seen by anyone's eyes; that's what it's there for!

The private key, meanwhile, is the key you want to always keep secret. The private key is the thing that authenticates the public half of the key. Without a matching private key to pair with the public key, many uses for your GPG key − such as encrypting messages − will not work. For the purpose of signing git commits, for example, the integrity of your private key matters a lot, as it verifies the integrity of the private key, which is the whole point of signing commits in the first place.

* [[Signing git commits using GPG keys]]