> [[Wiki|Home]] ▸ [[Tor]] ▸ [[Onion services]] ▸ **Connecting to a stealth Onion service**

A stealth Onion service is a certain kind of [Tor hidden service](https://www.torproject.org/docs/hidden-services.html.en) that requires clients (you) to supply an authentication token (basically, a password) before responding to incoming connection requests. This page describes how to configure your software to connect to such a service.

> 💡 🔰 If you are trying to use Tor as a file sharing tool, consider following the instructions in [Secretly sharing files with OnionShare and TorBrowser](https://github.com/AnarchoTechNYC/meta/blob/master/train-the-trainers/mr-robots-netflix-n-hack/week-1/secretly-sharing-files-with-onionshare-and-tor-browser/README.md#readme) instead. [OnionShare's "Advanced" options will automate the server-side portion of creating a stealth Onion service](https://github.com/micahflee/onionshare/wiki/Stealth-Onion-Services).

# Overview

To connect to a stealth Onion service, you must first acquire the access credentials (your personalized password) from whoever operates the service. This will likely be a human that you know. You will need to communicate with them (perhaps using [Signal](https://signal.org/)?) to learn what your access credentials will be. Once acquired, your access credentials will look something like the following line of text:

```
HidServAuth 1234567890abcdefg.onion abcdef01234567890+/K A description here
```

This is a Tor configuration directive (a [`HidServAuth` directive](https://www.torproject.org/docs/tor-manual.html#HidServAuth)). It has four parts, separated by spaces, and it breaks down as follows:

1. `HidServAuth` - Designates that whatever comes next is the hidden service authentication credentials.
1. `1234567890abcdefg.onion` - Tells Tor which site the credentials you'll supply should be given to.
1. `abcdef01234567890+/K` - The authentication cookie value (the password) itself.
1. `A description here` - Optionally, you can include a descriptive comment to let *you* know for which site or service these credentials are intended.

You will need to add this configuration line to your Tor's configuration file, called `torrc`. The configuration file tells Tor certain things about how it should operate, exactly like a settings screen.

# Procedure

**Do this** to connect to a stealth Onion service:

1. Install Tor Browser from [TorProject.org](https://www.torproject.org/download/download-easy.html).
1. Acquire the access credentials you need from the Onion service operator. I.e., get in touch with them and ask them for access. If they do not respond, poke them until they send you your access credentials. :) 
1. Locate the `torrc` file that you need to edit. The location of this file is slightly different depending on your computer's operating system:
    * In *macOS*, edit `~/Library/Application Support/TorBrowser-Data/Tor/torrc`.
        1. Open a new Finder window.
        1. From the *Go* menu, select *Go to folder…*
        1. In the *Go to the folder* text box, paste `~/Library/Application Support/TorBrowser-Data/Tor/` and press the *Go* button.
        1. The `torrc` file will be one of the files in the window that opens.
    * In *Windows*, edit `C:\Users\[user]\Desktop\Tor Browser\Browser\TorBrowser\Data\Tor\torrc`.
    * In *GNU/Linux*, edit `~/[path_to_tor_browser]/Browser/TorBrowser/Data/Tor/torrc`.
1. Open the `torrc` file with a text editor, such as Notepad on Windows or TextEdit.app on macOS. Any text editor will do. However, *Microsoft Word and other programs that expect rich text formatting will not work*.
1. Paste the configuration line you received from the Onion service operator on a line by itself in the `torrc` file.
1. Save the `torrc` file.
1. Restart (quit and re-launch) Tor Browser.

> ⚠️ 🔰 Do not put these credentials anywhere even remotely public. This includes sending yourself the credentials via e-mail. Saving these credentials anywhere that they could be obtained, by anyone else, defeats the entire purpose. And that would be silly.

After re-opening Tor Browser, you should now be able to connect to the `.onion` address described in your `torrc` file (assuming, of course, that the Onion service is a website).