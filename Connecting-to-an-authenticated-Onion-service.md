> [[Wiki|Home]] ▸ [[Tor]] ▸ [[Onion services]] ▸ **Connecting to an authenticated Onion service**

An authenticated Onion service is a certain kind of [Tor "hidden service"](https://www.torproject.org/docs/onion-services) that requires clients (you) to supply an authentication token (colloquially, a password) before responding to incoming connection requests. There are two different, incompatible Onion service versions that support client authentication: Version 2, and Version 3. This page covers both versions, describes how to tell one version apart from the other, and lists the steps you can take to configure a Tor client, such as Tor Browser or a system Tor service to supply your authentication credentials to the remote Tor server when connecting to its Onion services.

> 💡 🔰 If you are trying to use Tor as a file sharing tool, consider following the instructions in [Secretly sharing files with OnionShare and TorBrowser](https://github.com/AnarchoTechNYC/meta/blob/main/train-the-trainers/mr-robots-netflix-n-hack/week-1/secretly-sharing-files-with-onionshare-and-tor-browser/README.md#readme) instead. [OnionShare's "Advanced" options will automate the server-side portion of creating an authenticated stealth Version 2 Onion service](https://github.com/micahflee/onionshare/wiki/Stealth-Onion-Services) as well as Version 3 Onion services with optional additional application-layer password protection.

> 💡 🌐 [See the Tor project's own site for instructions on configuring unauthenticated Onion services](https://www.torproject.org/docs/tor-onion-service).

> 🔰 🎓 For more education and training about Tor or its Onion service features, we recommend [Tech Learning Collective's "Tor: What is it Good For? (Absolutely Everything!)" workshop](https://techlearningcollective.com/workshops/Tor-What-is-it-Good-For-%28Absolutely-Everything%21%29).

# Contents

1. [Identifying the Onion service version](#identifying-the-onion-service-version)
1. [Connecting to authenticated Version 3 Onion services](#connecting-to-authenticated-version-3-onion-services)
    1. [Overview for Version 3 Onion services](#overview-for-version-3-onion-services)
    1. [Procedure for Version 3 Onion services](#procedure-for-version-3-onion-services)
        1. [Generating authentication credentials for Version 3 Onion services](#generating-authentication-credentials-for-version-3-onion-services)
        1. [Configuring Tor Browser for authenticated Version 3 Onion services](#configuring-tor-browser-for-authenticated-version-3-onion-services)
        1. [Configuring a laptop or desktop computer for authenticated Version 3 Onion services](#configuring-a-laptop-or-desktop-computer-for-authenticated-version-3-onion-services)
        1. [Configuring an Android-based mobile device for authenticated Version 3 Onion services](#configuring-an-android-based-mobile-device-for-authenticated-version-3-onion-services)
        1. [Configuring an Apple iOS device for Version 3 authenticated Onion services](#configuring-an-apple-ios-device-for-authenticated-version-3-onion-services)
1. [Connecting to authenticated Version 2 Onion services](#connecting-to-authenticated-version-2-onion-services)
    1. [Overview for Version 2 Onion services](#overview-for-version-2-onion-services)
    1. [Procedure for Version 2 Onion services](#procedure-for-version-2-onion-services)
        1. [Configuring a laptop or desktop computer for authenticated Version 2 Onion services](#configuring-a-laptop-or-desktop-computer-for-authenticated-version-2-onion-services)
        1. [Configuring an Android-based mobile device for authenticated Version 2 Onion services](#configuring-an-android-based-mobile-device-for-authenticated-version-2-onion-services)
        1. [Configuring an Apple iOS device for Version 2 authenticated Onion services](#configuring-an-apple-ios-device-for-authenticated-version-2-onion-services)

# Identifying the Onion service version

Before you attempt to configure your Tor to connect to an authenticated Onion service, you must first know which Onion service version you are connecting to. If the operator of the Onion service did not already tell you, then you may need to deduce this information for yourself. The simplest way to do so is to examine the Onion domain name you were given (the long string of letters and numbers that end in `.onion`).

* Version 2 Onion services have `.onion` addresses that are sixteen (16) characters long before the `.onion` part.
* Version 3 Onion services have `.onion` addresses that are fifty-six (56) characters long before the `.onion` part.

Using the above rules, the length of the Onion domain name can tell you whether the Onion service you are going to be connecting to is a [Version 2](#connecting-to-authenticated-version-2-onion-services) or [Version 3](#connecting-to-authenticated-version-3-onion-services) Onion service.

# Connecting to authenticated Version 3 Onion services

This section provides an overview as well as a step-by-step procedure for configuring your Tor client to connect to authenticated Version 3 Onion service servers.

## Overview for Version 3 Onion services

To connect to an authenticated Version 3 Onion service, you must first create a two-part access credential called a public/private keypair. Your access credential ("keypair") is so named because one part of the access credential is "public," which is to say that it is intended to be shared, while the other part is "private," which is to say that it is intended to remain a secret known only by you (or, more accurately, your computer). The public and private portions of your access credential are related in that they function like a digital lock and key: the public part is the lock and the private part is the corresponding key that "opens" the lock.

You will generate and store these two parts of your access credential ("keypair") in two separate files. The public portion will ultimately reside in a file that ends with `.auth`. The private portion will ultimately reside in a file ending with `.auth_private`.

> 💡🔰 In some situations, the Onion service operator may give you the private part of your keypair. This will arrive as a small file with a `.auth_private` extension. In this case, you need not generate another one on your own and can safely skip the [§ Generating authentication credentials for Version 3 Onion services](#generating-authentication-credentials-for-version-3-onion-services) section in [the procedure outlined below](#procedure-for-version-3-onion-services).

Once you have your `.auth` and `.auth_private` files containing the public and private portion of your access credential, respectively, you will need to ensure that your Tor software knows where to find the `.auth_private` file. This is done by adding a configuration line to your Tor's configuration file, a file called `torrc`. The configuration file tells Tor certain things about how it should operate, exactly like a settings screen.

The configuration line you will add (or ensure already exists) will look something like this:

```
ClientOnionAuthDir /path/to/the/folder/containing/your/auth_private_files
```

This is a Tor configuration directive (a [`ClientOnionAuthDir` directive](https://www.torproject.org/docs/tor-manual.html#ClientOnionAuthDir)). It has two parts, separated by spaces, and it breaks down as follows:

1. `ClientOnionAuthDir` - Designates that whatever comes next is the location of a folder containing `.auth_private` files.
1. `/path/to/the/folder/containing/your/auth_private_files` - Tells Tor which folder to look inside of to find `.auth_private` files.

Although the folder containing your `.auth_private` files can be anywhere you like and can contain other files in addition to your `.auth_private` files, we suggest that you create a new folder for the exclusive purpose of storing your private `.auth_private` files.

## Procedure for Version 3 Onion services

As described in the [Overview for Version 3 Onion services](#overview-for-version-3-onion-services), access credentials for Version 3 Onion services are composed of a public/private keypair and are ideally created by you, the client, so that the Onion service operator need not ever have access to your Onion service private key. The [§ Generating authentication credentials for Version 3 Onion services](#generating-authentication-credentials-for-version-3-onion-services) section, below, offers a step-by-step guide for generating such a keypair.

Once generated, you can safely send the public portion of your keypair to the Onion service operator (ideally over a secure channel such as [Signal](https://Signal.org/)). Finally, you will inform your Tor software where to find the private portion of your keypair.

### Generating authentication credentials for Version 3 Onion services

> 💡🔰 If you were given a `.auth_private` file by your Onion service operator, you already have an authentication credential and can skip this section.

The easiest way to generate a valid Tor v3 Onion credential is to use the [`tor-auth-x25519-gen.py` Python script we maintain](https://github.com/AnarchoTechNYC/ansible-role-tor/tree/master/molecule/default/scripts/tor-auth-x25519-gen.py). Run the script using the `-d` or `--onion-domain` option, passing in the `.onion` address of the site you'd like to generate an Onion credential for, and the `-f` or `--credential-file` option, passing in a file path where you'd like to write your new Tor credential files. For example:

```sh
./tor-auth-x25519-gen.py \
  -d rh5d6reakhpvuxe2t3next6um6iiq4jf43m7gmdrphfhopfpnoglzcyd.onion \
  -f my_onion
```

The above command will produce two files:

* `my_onion.auth` - This the file you should share with the operator of the Onion service at the `rh5d6reakhpvuxe2t3next6um6iiq4jf43m7gmdrphfhopfpnoglzcyd.onion` domain.
* `my_onion.auth_private` - This is the file you should keep secret and protect, because it is your key to access the Onion domain. Put this file wherever you [configured your Tor to look for your private keys via its `ClientOnionAuthDir` directive](#configuring-a-laptop-or-desktop-computer-for-authenticated-version-3-onion-services).

Fuller instructions, for example if you don't have Python and so can't run the above script, are also available from the Tor Project at [Onion Services: Advanced settings § Client Authorization](https://community.torproject.org/onion-services/advanced/client-auth/).

### Configuring Tor Browser for authenticated Version 3 Onion services

The [Tor (Web) Browser is a two-for-one software package that bundles a Tor client and a Web browser in one installation](https://github.com/AnarchoTechNYC/meta/blob/main/train-the-trainers/practice-labs/introduction-to-anonymous-communications-using-tor/README.md#understanding-the-difference-between-tor-and-tor-browser). Installing and using the latest version of Tor Browser is the easiest and recommended way to access authenticated Version 3 Onion services hosting Web sites (often called "dark net" or "deep web" sites) because it provides a familiar graphical dialogue box in which to enter your credentials. The [Onion Service Authentication section of the Onion Services page in the Tor Browser's User Manual](https://tb-manual.torproject.org/onion-services/#onion-service-authentication) provides a screenshot and instructions demonstrating the procedure:

![Screenshot of the Tor Browser's](https://web.archive.org/web/20200602195259im_/https://tb-manual.torproject.org/static/images/client-auth.png)

This feature became available in Tor Browser version 9.5 (circa June 2020). For more information on Tor Browser, read the [Tor Browser User Manual](https://tb-manual.torproject.org/) in full, or participate in one of our educational partners' Tor workshops, such as the [Tor workshop provided by Tech Learning Collective](https://techlearningcollective.com/workshops/Tor-What-is-it-Good-For-%28Absolutely-Everything%21%29#events).

### Configuring a laptop or desktop computer for authenticated Version 3 Onion services

**Do this** to connect to an authenticated Version 3 Onion service from a Tor client installed on your laptop or desktop computer. The procedure here assumes the use of the Tor client built-in to the Tor Browser, but the same procedure applies to a system Tor with appropriately modified filesystem paths:

1. Install Tor Browser from [TorProject.org](https://www.torproject.org/download/download-easy.html).
1. Ensure you have a valid `.auth_private` file. You can either [generate one yourself](#generating-authentication-credentials-for-version-3-onion-services), or in some cases you may have already received one from the operator of your Onion service.
1. Choose or make a sensible folder to store all of your Version 3 Onion service access credential files. For example, a folder called "`Onions`" in your home folder would work well.
1. Move the `.auth_private` file into the folder you chose to store your Version 3 Onion service access credential files.
1. Find the filesystem path of the folder you chose to store your Version 3 Onion service access credential files. Make a note of this filesystem path, as we'll use it in a future step.
    * In *macOS*:
        1. Single-click on the folder to select it.
        1. From the menu bar, choose *File* &rarr; *Get Info*. The folder Info window will open.
        1. Click on the *General* section's disclosure triangle to expose the General Information panel.
        1. Select and copy the entire value of the *Where* line, as shown below, then paste it into your notes:  
            ![Screenshot of the macOS Finder's "Get Info" window for a folder named "Onions" in a user's home folder.](https://i.imgur.com/cuoHUj2.png)
        1. If the folder you chose was `Onions` in your home folder, your path will probably look something like `/Users/YOUR_USER_NAME/Onions`.
    * In *GNU/Linux*, first use the `cd` command to go to the folder itself, then use [the `pwd` command](https://explainshell.com/explain?cmd=pwd) to find the full filesystem path of the folder. If the folder you chose was `Onions` in your home folder, your path will probably look something like `/home/YOUR_USER_NAME/Onions`.
    * In *Windows*:
        1. Right-click on the folder and choose *Properties* from the contextual menu.
        1. In the *General* tab, find and copy the full value of the *Location* line.
        1. If the folder you chose was `Onions` in your home folder, your path will probably look something like `C:\Users\YOUR_USER_NAME\Onions`.
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
1. Add a line to the `torrc` file that begins with `ClientOnionAuthDir` and ends with the filesystem path of the folder you chose to store your Version 3 Onion service access credential files that you noted earlier. For example, on a macOS computer, the full line in your `torrc` file might look like this:
    ```
    ClientOnionAuthDir /Users/YOUR_USER_NAME/Onions
    ```
1. Save the `torrc` file.
1. Restart (quit and re-launch) Tor Browser.

After re-opening Tor Browser, you should now be able to connect to the `.onion` address described in your `.auth_private` file (assuming, of course, that the Onion service hosts a website).

### Configuring an Android-based mobile device for authenticated Version 3 Onion services

**Do this** to connect to an authenticated Version 3 Onion service from your Android-based phone:

1. Install [Orbot](https://guardianproject.info/apps/orbot/). You can acquire Orbot from the Google Play Store or, preferably, from [F-Droid](https://f-droid.org/), a [Free Software](https://www.gnu.org/philosophy/free-sw.html) app store that offers most of the same apps as the Google Play Store, but free of charge.
1. Configure Orbot:
    1. Tap the vertical ellipse menu at the top-right of the screen.
    1. Open the *Onion Services* menu.
    1. Select the *v3 Onion Service Client Authorization* menu item.
    1. Tap the compose button on the bottom-right of the screen.
    1. In the *v3 onion Domain* field, enter the full 56 character Onion address (optionally including the `.onion` suffix) of the Onion service.
    1. In the *x25519 Private Key in Base 32* field, enter the hash of the private key for this Onion Service.
    1. Tap the *Save* button.
    1. Tap the back button (&larr;) in the top-left corner of the screen to return to Orbot's main activity screen.
1. Restart Orbot:
    1. Tap the vertical ellipse menu at the top-right of the screen.
    1. Select the *Exit* menu item. This will fully close Orbot.
    1. Launch Orbot again. This time, Orbot will be able to connect you to the Onion service.

> 💡🔰 If you were given a `.auth_private` file by your Onion service operator, you can tap the verticle ellipse menu on the *v3 Onion Service Client Authorization* screen and select *Import .auth_private* to load the file from your device's filesystem. After confirming that you can now access the Onion service, you should consider deleting the `.auth_private` file from your device's filesystem because storing sensitive files on an Android device's external storage can be dangerous as other apps may be able to access them there.

### Configuring an Apple iOS device for authenticated Version 3 Onion services

At the time of this writing, iOS cannot connect to authenticated Version 3 Onion services. When available, [iCepa](https://github.com/iCepa/iCepa) may make it possible to connect to Onion services on devices running Apple's iOS.

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

## Procedure for Version 2 Onion services

The exact procedure for setting up your Tor client to connect to a Tor server's authenticated Version 2 Onion service varies slightly depending on the device you're using.

### Configuring a laptop or desktop computer for authenticated Version 2 Onion services

**Do this** to connect to an authenticated Version 2 Onion service from your laptop or desktop computer. The procedure here assumes the use of the Tor client built-in to the Tor Browser, but the same procedure applies to a system Tor with appropriately modified filesystem paths:

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

### Configuring an Android-based mobile device for authenticated Version 2 Onion Services

**Do this** to connect to an authenticated Version 2 Onion service from your Android-based phone:

1. Install [Orbot](https://guardianproject.info/apps/orbot/). You can acquire Orbot from the Google Play Store or, preferably, from [F-Droid](https://f-droid.org/), a [Free Software](https://www.gnu.org/philosophy/free-sw.html) app store that offers most of the same apps as the Google Play Store, but free of charge.
1. Configure Orbot:
    1. Tap the vertical ellipse menu at the top-right.
    1. Tap the *Onion Services* menu.
    1. Tap the *v2 Onion Services (Deprecated)* menu.
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

### Configuring an Apple iOS device for authenticated Version 2 Onion services

At the time of this writing, iOS cannot connect to authenticated Version 2 Onion services. When available, [iCepa](https://github.com/iCepa/iCepa) may make it possible to connect to Onion services on devices running Apple's iOS.
