> [[Wiki|Home]] ▸ [[GPG and PGP]] ▸ **Signing git commits using GPG keys**

# Contents

1. [Note](#note)
1. [Overview](#overview)
1. [Procedure](#procedure)
    1. [Generating a GPG keypair](#generating-a-gpg-keypair)
    1. [Configuring git](#configuring-git)

### Notes:

1. This guide is intended to be a supplemental or alternative guide to the guides provided by GitHub, which are also great and included in the [References](#references) section here. This guide includes a few other details regarding encryption and opsec which those guides don't include.

1. GPG is also known as PGP, and while there _are_ historical differences between what these acronyms mean and where they originated, the technology to which they both refer to is essentially the same thing. For the purposes of this guide, we will be referring to the tool as **GPG**, simply because that is what [[GitHub]] refers to, and since most of you reading are probably going to be using GitHub for your [[git]] commits anyway, this will keep the language consist between this guide and the ones GitHub provides.

For more comprehensive information on GPG/PGP and the difference between the acronyms, see [[GPG and PGP]].

### What is GPG?

A GPG key is a cryptographic mechanism used for encryption and verification in a myriad of circumstances. It's a generic method of encryption and verification that can be applied from anything from e-mail and file encryption to commit signing.

A GPG/PGP key is really one thing in two "pieces," known as a **key pair.** A key pair is called a pair because it includes two parts: a **public key** and a **private key**. The public key is just what it sounds like: this is the one you can share with the world. It's perfectly safe for that key to find its way onto other servers or be seen by anyone's eyes; that's what it's there for!

The private key, meanwhile, is the key you want to always keep secret. The private key is the thing that authenticates the public half of the key. Without a matching private key to pair with the public key, many uses for your GPG key − such as encrypting messages − will not work. For the purpose at hand, signing GPG commits, the integrity of your private key matters a lot, as it verifies the integrity of the private key, which is the whole point of signing commits in the first place.

# Overview

The first thing we need to do to be able to sign our git commits is to first have keys with which to sign those commits. This means we need to _generate_ our own GPG key pairs before we can tell git about them (makes sense, right?). For the purposes of this guide, we are going to be using the slightly newer GPG `gpg2` tool.

# Procedure:

The exact process for generating a good GPG keypair, followed by telling git which one to use, with opsec considerations included.

## Generating a GPG keypair

The exact procedure for generating GPG keys on the command line, and then configuring git to use whichever GPG key you'd like to use to sign commits.

1. Open your Terminal.

1. We're going to need a tool called `gpg` or `gpg2` in order to create our keypair. If you do not already have `gpg2`, you can install it using your package manager (such as `apt` or `yum`), or, for the absolutely most up-to-date version, [you can download it straight from GnuPG here](https://www.gnupg.org/download/index.html).

1. To see whether you have `gpg2` installed, or to check what version of `gpg2` you have, type:

    `gpg2 --version`

This will give you some information about your version of `gpg2`, including what kinds of encryption it can use, such as [[RSA]].

> ⚠️ 🔰 Encryption geeks, please note that git by default uses `gpg`, not `gpg2`. This means things that are specifically supported by `gpg2`, such as newer ciphers like ed25519, are not supported by default. You may [change this setting](https://stackoverflow.com/questions/34766123/signing-commit-with-openpgp-subkey-fails#34767663), but as it is not ubiquitous and GitHub itself suggests using RSA keys with 4096 bits, we're going to stick with this for this guide and it is recommended to use these settings as well for the time being. RSA with 4096 bits is perfectly secure for these purposes.

> 💡 🔰 You may have generated some GPG keys sometime in the past, perhaps if you have learned about GPG in the past. To take a look at the keys you currently have, if you do have any, use the command `gpg2 --list-secret-keys`. This will show you a list of the keys on your machine. **Even if you have keys already,** it's a good idea to generate a new one specifically for the purpose of signing git commits. It's also recommended to make different keys per GitHub (or GitLab, etc.) account, especially if your account information on those services differs from one account to the other. This is just a good way of keeping things clean and well-organized.

2. You'll be using a good password to secure your key Before you start this process, it's a good idea to make the password you'll be using **before** you begin the key generation process, and copy and paste it into your clipboard, or put it into a text editor and place it near the edge of your screen so you can type it in when prompted. 

> 💡 🔰 If you don't already use a password manager such as [LastPass](https://lastpass.com), it's recommended to install one. Most password managers come with a password generator, which you can use to create strong passwords.

3. In your Terminal, use the following command to initiate the interactive `gpg2` key generation process:

`gpg2 --full-gen-key`

4. You will be prompted to select a type of key. For the purposes of this guide, we'll be making an RSA keypair, which means both our public and our private key will be using RSA for encryption. Since this is the default selection, you can hit `Enter`, or else type `1` to be explicit.

5. RSA keys can be between 1024 and 4096 bits long, with 2048 being the default for `gpg2`. 4096 bits gives us the longest and most secure key, so we want that. Go ahead and type in `4096` and hit `Enter`.

6. You'll now be asked how long you want this key to be valid for. This is largely a personal choice,  but if you're really planning on using this key out in the world, you want to pick a time frame that makes sense for the use of the key. 2 years, for example, is an okay time frame for our use of signing git commits. Not too long, but gives us enough time to use the key without needing to regenerate it soon.

7. You'll be given a specific date of expiry based on the length you specified, which you can then confirm.

8. Now you'll be prompted for some details about yourself. If you're using this key to sign commits on a public repo, or on GitHub generally, try to match the information that you've already given GitHub (or whatever service), so that you're not unnecessarily giving out more personal information than needed.

> :exclamation: Before proceeding to the next step, get ready with your password for the GPG key for the next step; either copy it to your clipboard or put it into a text editor near the edge of your screen.

9. Once you've finished filling out this information, you'll be prompted for the password to secure this key. Go ahead and paste or type in your **strong** password.

10. `gpg2` will now tell you that it needs to generate entropy in order to generate the encryption cipher. This will take a little longer based on how many bits you designated (in this case, a 4096 bit key will take a little longer than a smaller, less complex key). It's a good idea to interact with your computer in various ways so that the Random Number Generator can generate enough randomness to make your key more random and thus stronger.

> :construction: TK-TODO: Add a little more info on entropy?

## Configuring git

The key you just created isn't likely to be the only key you ever make. Now that we have our key, we need to tell git which key we want to use to sign our commits.

1. Go back to the Terminal.

1. Navigate to the git directory containing the project with which you want to use GPG signed commits.

1. Take a look, using `ls -a`, in your git directory. You will see the [[hidden directory]] `.git`. If you do a quick `ls .git`, you'll also see a file called `config`. This is the file that will be edited when you use the command `git config`. This config file is specific to this project.

> :bulb:🔰 Most guides will tell you to use the command `git config` with the `--global` option. This is supposed to simplify your use, but this means that everything you do with `git` on your current computer user account will be signed using this key, which includes the information associated with that key, which is a potential opsec risk if you're trying to keep one GitHub account relatively separate from another. Like you probably don't want to use your anti-cop GitHub with your work GitHub, unless your boss is down. :black_flag:

1. To assign your new GPG key to this git project, first find the long "name" for that key. Use the command:

`gpg2 --list-secret-keys --keyid-format LONG`

To show the private keys. Find the one you want to use for your git commits (usually the last in the list, being the most recently generated).

On the lefthand side, you'll see a line that begins with `sec`, and then `rsa4096` (if you did in fact decide to go with RSA format with 4096 bits). **After** the slash, you'll see a 16-character identification number, followed by the date of the key's creation. Copy the 16-character identifier.

1. Now, still in your git directory, use the command:

`git config user.signingkey` followed by a space, and then the 16-character identifier.

For example:

`git config user.signingkey G73JN7HFN2HGK90D`

**Note:** That is not a real key identifier. Come on, now.

And that's it! You're done! :sparkle:

## References

* [GitHub Help: Generating a new GPG key](https://help.github.com/articles/generating-a-new-gpg-key/)

* [Github Help: Telling Git about your GPG key](https://help.github.com/articles/telling-git-about-your-gpg-key/)