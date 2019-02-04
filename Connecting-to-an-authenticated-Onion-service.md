> [[Wiki|Home]] ▸ [[Tor]] ▸ [[Onion services]] ▸ **Connecting to an authenticated Onion service**

An authenticated Onion service is a certain kind of [Tor "hidden service"](https://www.torproject.org/docs/onion-services) that requires clients (you) to supply an authentication token (basically, a password) before responding to incoming connection requests. There are two different, incompatible Onion service versions that support client authentication: Version 2, and Version 3. This page covers both versions and describes how to tell one version apart from the other.

> 💡 🔰 If you are trying to use Tor as a file sharing tool, consider following the instructions in [Secretly sharing files with OnionShare and TorBrowser](https://github.com/AnarchoTechNYC/meta/blob/master/train-the-trainers/mr-robots-netflix-n-hack/week-1/secretly-sharing-files-with-onionshare-and-tor-browser/README.md#readme) instead. [OnionShare's "Advanced" options will automate the server-side portion of creating a stealth Onion service](https://github.com/micahflee/onionshare/wiki/Stealth-Onion-Services).

> 💡 🌐 [See the Tor project's own site for instructions on configuring unauthenticated Onion services](https://www.torproject.org/docs/tor-onion-service).

# Contents

1. [Identifying the Onion service version](#identifying-the-onion-service-version)
1. [Connecting to authenticated Version 3 Onion services](#connecting-to-authenticated-version-3-onion-services)
    1. [Overview for Version 3 Onion services](#overview-for-version-3-onion-services)
    1. [Procedure for Version 3 Onion services](#procedure-for-version-3-onion-services)
1. [Connecting to authenticated Version 2 Onion services](#connecting-to-authenticated-version-2-onion-services)
    1. [Overview for Version 2 Onion services](#overview-for-version-2-onion-services)
    1. [Procedure for Version 2 Onion services](#procedure-for-version-2-onion-services)
        1. [Laptop or desktop computer](#laptop-or-desktop-computer)
        1. [Android-based mobile device](#android-based-mobile-device)
        1. [Apple iOS device](#apple-ios-device)

# Identifying the Onion service version

Before you attempt to configure your Tor to connect to an authenticated Onion service, you must first know which Onion service version you are connecting to. If the operator of the Onion service did not already tell you, then you may need to deduce this information for yourself. The simplest way to do so is to examine the Onion domain name you were given (the long string of letters and numbers that end in `.onion`).

* Version 2 Onion services have `.onion` addresses that are sixteen (16) characters long before the `.onion` part.
* Version 3 Onion services have `.onion` addresses that are fifty-six (56) characters long before the `.onion` part.

Using the above rules, the length of the Onion domain name can tell you whether the Onion service you are going to be connecting to is a [Version 2](#connecting-to-authenticated-version-2-onion-services) or [Version 3](#connecting-to-authenticated-version-3-onion-services) Onion service.

# Connecting to authenticated Version 3 Onion services

This section provides an overview as well as a step-by-step procedure for configuring your Tor client to connect to authenticated Version 3 Onion service servers.

## Overview for Version 3 Onion services

> 🚧 TODO: Complete the overview for Version 3 Onion services.

To connect to an authenticated Version 3 Onion service, you must first create a two-part access credential called a public/private keypair. Your access credential ("keypair") is so named because one part of the access credential is "public," which is to say that it is intended to be shared, while the other part is "private," which is to say that it is intended to remain a secret known only by you. The public and private portions of your access credential are special in that they function like a digital lock-and-key: the public part is the lock, which you will give to the Onion service operator so that the Onion service can lock any messages intended for you in such a way that only you can unlock them with your corresponding (secret and private!) key.

You will generate and store these two parts of your access credential ("keypair") in two separate files. The public portion will ultimately reside in a file that ends with a `.auth` extension. The private portion will ultimately reside in a file of the same name, but ending with a `.auth_private` extension.

> 💡🔰 In some situations, the Onion service operator may give you the private part of your keypair. This will arrive to as a small file with a `.auth_private` extension. In this case, you need not generate another one on your own and can safely skip to step TK in the procedure outlined below.

Once you have your `.auth` and `.auth_private` files containing the public and private portion of your access credential, respectively, you will need to TK

## Procedure for Version 3 Onion services

> 🚧 TODO: Complete the procedure section for Version 3 Onion services.

# Connecting to authenticated Version 2 Onion services

This section provides an overview as well as a step-by-step procedure for configuring your Tor client to connect to authenticated Version 2 Onion service servers.

## Overview for Version 2 Onion services

To connect to an authenticated Version 2 Onion service, you must first acquire the access credentials (your personalized password) from whoever operates the service. This will likely be a human that you know. You will need to communicate with them (perhaps using [Signal](https://signal.org/)?) to learn what your access credentials will be. Once acquired, your access credentials will look something like the following line of text:

```
HidServAuth 1234567890abcdefg.onion abcdef01234567890+/K A description here
```

> ⚠️ 🔰 Do not put these credentials anywhere even remotely public. This includes sending yourself the credentials via e-mail. Saving these credentials anywhere that they could be obtained, by anyone else, defeats the entire purpose. And that would be silly.

This is a Tor configuration directive (a [`HidServAuth` directive](https://www.torproject.org/docs/tor-manual.html#HidServAuth)). It has four parts, separated by spaces, and it breaks down as follows:

1. `HidServAuth` - Designates that whatever comes next is the hidden service authentication credentials.
1. `1234567890abcdefg.onion` - Tells Tor which site the credentials you'll supply should be given to.
1. `abcdef01234567890+/K` - The authentication cookie value (the password) itself.
1. `A description here` - Optionally, you can include a descriptive comment to let *you* know for which site or service these credentials are intended.
    > 🔰 💡 If the Onion service is particularly sensitive, avoid including personally identifying information in the comment. For example, `Chris's message board` is an unsafe description. A better one might simply be, `Message board`.

On a typical computer such as a [laptop or desktop workstation, you will need to add this configuration line to your Tor's configuration file](#laptop-or-desktop-computer), called `torrc`. The configuration file tells Tor certain things about how it should operate, exactly like a settings screen. If you are [using an Android-based mobile phone](#android-based-mobile-device), you'll enter the Onion address and the authentication cookie value into an actual settings screen.

# Procedure for Version 2 Onion services

The exact procedure for setting up your Tor client to connect to a Tor server's authenticated Version 2 Onion service varies slightly depending on the device you're using.

## Laptop or desktop computer

**Do this** to connect to an authenticated Version 2 Onion service from your laptop or desktop computer:

1. Install Tor Browser from [TorProject.org](https://www.torproject.org/download/download-easy.html).
1. Acquire the access credentials you need from the Onion service operator. I.e., get in touch with them and ask them for access. If they do not respond, poke them until they send you your access credentials. :) 
1. Locate the `torrc` file that you need to edit. The location of this file is slightly different depending on your computer's operating system:
    > 🔰 In the following file paths, the `~` character or the `%HOMEDRIVE%%HOMEPATH%` sequence refers to "wherever your home folder is."
    * In *macOS*, edit `~/Library/Application Support/TorBrowser-Data/Tor/torrc`.
        1. Open a new Finder window.
        1. From the *Go* menu, select *Go to folder…*
        1. In the *Go to the folder* text box, paste `~/Library/Application Support/TorBrowser-Data/Tor/` and press the *Go* button.
        1. The `torrc` file will be one of the files in the window that opens.
    * In *GNU/Linux*, edit `~/[path_to_tor_browser]/Browser/TorBrowser/Data/Tor/torrc`.
    * In *Windows*, edit `"%HOMEDRIVE%%HOMEPATH%"\Desktop\Tor Browser\Browser\TorBrowser\Data\Tor\torrc`.
1. Open the `torrc` file with a text editor, such as [Notepad](https://en.wikipedia.org/wiki/Microsoft_Notepad) on Windows or [TextEdit.app](https://en.wikipedia.org/wiki/TextEdit) on macOS. Any [text editor](https://simple.wikipedia.org/wiki/Text_editor) will do. However, *Microsoft Word and other programs that expect rich text formatting will not work*.
1. Paste the configuration line you received from the Onion service operator on a line by itself in the `torrc` file.
1. Save the `torrc` file.
1. Restart (quit and re-launch) Tor Browser.

After re-opening Tor Browser, you should now be able to connect to the `.onion` address described in your `torrc` file (assuming, of course, that the Onion service hosts a website).

## Android-based mobile device

**Do this** to connect to an authenticated Version 2 Onion service from your Android-based phone:

1. Install [Orbot](https://guardianproject.info/apps/orbot/). You can acquire Orbot from the Google Play Store or, preferably, from [F-Droid](https://f-droid.org/), a [Free Software](https://www.gnu.org/philosophy/free-sw.html) app store that offers most of the same apps as the Google Play Store, but free of charge.
1. Install [Orfox](https://guardianproject.info/apps/orfox/). You can acquire Orfox from the Google Play Store or, preferably, from F-Droid.
1. Configure Orbot:
    1. Tap the vertical ellipse menu at the top-right.
    1. Tap the *Hidden Services* menu.
    1. Tap the *Client cookies* menu item. The Client cookies activity screen will appear.
    1. Tap the compose button on the bottom-right of the screen.
    1. In the *.onion* field, enter the full Onion address (including the `.onion` suffix) of your Onion service.
    1. In the *Auth cookie* field, enter the full authentication cookie value as you received it. (The authentication cookie value is the third item in the `HidServAuth` configuration line, [described above](#overview).)
    1. Tap the *Save* button.
    1. Tap the back button (&larr;) in the top-left corner of the screen to return to Orbot's main activity screen.
1. Restart Orbot:
    1. Tap the vertical ellipse menu at the top-right.
    1. Tap the *Exit* menu item. This will fully close Orbot.
    1. Launch Orbot again. This time, Orbot will be able to connect you to the Onion service.
1. Launch Orfox.
    1. From Orbot's main screen, press the *Browse* button. This will launch Orfox if it is already installed.
1. Type in the Onion service URL (including the `.onion` suffix) into Orfox's Web address bar, then press *Go* on your software keyboard.

You should now be able to connect to the `.onion` address that you configured in Orbot's "Hidden Services" menu (assuming, of course, that the Onion service is a website).

## Apple iOS device

At the time of this writing, iOS cannot connect to authenticated Onion services. When available, [iCepa](https://github.com/iCepa/iCepa) may make it possible to connect to Onion services on devices running Apple's iOS.