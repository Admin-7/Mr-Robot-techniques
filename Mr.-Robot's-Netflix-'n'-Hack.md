> [[Wiki|Home]] ▸ [[Activities and events]] ▸ **Mr. Robot's Netflix 'n' Hack**

* Tagline: Let Mr. Robot teach you how to hack.
* Description: Watch an episode of "[Mr. Robot](http://www.imdb.com/title/tt4158110/)," a TV show dramatizing the lives of rogue hackers in NYC with unparalleled technical accuracy, and then get an introduction to how the tools, techniques, and procedures shown in the episode work in real life. After we watch an episode of the show, we'll discuss the tools used, get them installed on our laptops, and try them out. Then we'll meet again next week to show one another what we've learned, and continue with the next episode. By the end of the 10-week season, you'll have gotten a hands-on tour of various tools in the Kali Linux penetration testing distro, and a better sense of how to separate fiction from reality in contemporary hacking dramas in pop culture.
* Facilitating: [[How to facilitate Mr. Robot's Netflix 'n' Hack]]
* See also [[InfoSec]], [🌐 GeekWire's "Mr. Robot Rewind" series](http://www.geekwire.com/tag/mr-robot/) (*contains spoilers*).

Watch the [Mr. Robot trailer](http://www.youtube.com/watch?v=U94litUpZuc) to see if this is a show you might enjoy watching and learning from:

[![Mr. Robot Season 1, extended trailer](http://img.youtube.com/vi/U94litUpZuc/0.jpg)](http://www.youtube.com/watch?v=U94litUpZuc)

* [Week 1 (S01E01)](#week-1-s01e01)
* [Week 2 (S01E02)](#week-2-s01e02)
* [Week 3 (S01E03)](#week-3-s01e03)
* [Week 4 (S01E04)](#week-4-s01e04)
* [Week 5 (S01E05)](#week-5-s01e05)
* [Week 6 (S01E06)](#week-6-s01e06)
* [Week 7 (S01E07)](#week-7-s01e07)
* [Week 8 (S01E08)](#week-8-s01e08)

# Week 1 (S01E01)

* [Tor](https://torproject.org/)
  * [Onion routing](https://en.wikipedia.org/wiki/Onion_routing),
  * ["Onion services" (formerly known as "hidden services")](https://www.torproject.org/docs/hidden-services.html.en)
  * "[Deep Web](https://www.youtube.com/watch?v=CHOjbPI-B8E)" sites ([how to search](http://deep-web.org/how-to-research/deep-web-search-engines/), check out [The Hidden Wiki](https://thehiddenwiki.org/))
* [RUDY attacks](https://en.wikipedia.org/wiki/Denial-of-service_attack#R-U-Dead-Yet.3F_.28RUDY.29)
  * [Incapsula's DDoS Attack Glossary entry for "RUDY attack"](https://www.incapsula.com/ddos/attack-glossary/rudy-r-u-dead-yet.html)
* "Good at reading people" (social engineering…a [blog post](https://web.archive.org/web/20020125012547/http://www.securityfocus.com/cgi-bin/infocus.pl?id=1527) to maybe read, also a book [The Art of Deception](http://sbisc.ut.ac.ir/wp-content/uploads/2015/10/mitnick.pdf), see also: [Freedom Downtime](https://www.youtube.com/watch?v=qMzRRVgEuWc))
  * "I left my keys in one of your cabs…"
  * "Can I borrow your phone?" (also deleted the outgoing call log)
  * "This is Sam from Bank of E fraud department."
* `ping`
* Password cracking:
  * An important distinction between online versus offline attacks.
  * [Hashcat](https://hashcat.net/hashcat/) (not actually the tool shown, maybe Eliot has a script that wraps this?) - offline tool
    * ["dictionary brute force"](https://hashcat.net/wiki/doku.php?id=dictionary_attack)
  * [Hydra](http://sectools.org/tool/hydra/) - online tool
* Information gathering via social media sleuthing (kind of general, eh? was a specific tool shown?)
* Blackberry mobile phones (and their, uh, [security problems](https://motherboard.vice.com/read/rcmp-blackberry-project-clemenza-global-encryption-key-canada))
* "[Desktop environment](https://en.wikipedia.org/wiki/Desktop_environment)s":
  * [GNOME](https://www.gnome.org/)
  * [KDE](https://www.kde.org/)
* "DDoS attack" is a Distributed Denial of Service attack
  * Understanding DDoS basics, read "[What is LOIC and can I be arrested for DDoS'ing someone?](https://www.troyhunt.com/what-is-loic-and-can-i-be-arrested-for/)"
  * [Deep Inside a DNS Amplification DDoS Attack](https://blog.cloudflare.com/deep-inside-a-dns-amplification-ddos-attack/)
  * "DDoS protection" - really, really big pipes, see [CloudFlare](https://www.cloudflare.com/ddos/), [Google's Project Shield](https://projectshield.withgoogle.com/public/), and [Deflect.ca](https://deflect.ca/)
* DNS
* "fingerblasting"
  * Historical sidenote: read about the [`finger` Protocol](https://en.wikipedia.org/wiki/Finger_protocol)
* `astsu` is [not real](https://www.leaseweb.com/labs/2015/09/linux-commands-astu-and-astsu-in-mr-robot/), but! `traceroute` is
* [rootkit](https://en.wikipedia.org/wiki/Rootkit)
  * Blog post: [Basics of Making a Rootkit](https://d0hnuts.com/2016/12/21/basics-of-making-a-rootkit-from-syscall-to-hook/)
* `ifconfig` ("redirect the traffic"), when done on a router, we're probably more talking more about [CISCO iOS switches](https://en.wikipedia.org/wiki/Cisco_IOS)
  * [VyOS](https://vyos.io/) is a free software clone of Cisco's iOS, useful if you can't pay for an iOS license
* On the server's command line:
  * `locate`
  * `kill`
  * `rm` (`-norecycle` is not real, is it?)
  * "Reconfigure the access to the directory" -> `chmod`
* "I'll ask my IRC contacts…"
  * IRC is [Internet Relay Chat](https://en.wikipedia.org/wiki/Internet_Relay_Chat), an aging chat room technology that is still popular with techies and hackers.
  * Guide to IRC for novices: [IRCHelp.org](http://www.irchelp.org/)
* [VPN](https://en.wikipedia.org/wiki/Virtual_private_network)
* [US Cyber Command](https://en.wikipedia.org/wiki/United_States_Cyber_Command)
* [Google (News) Alerts](https://www.google.com/alerts)
* "…with a custom dictionary, my program can crack his password in two minutes." -> [Generating wordlists](https://netsec.ws/?p=457)
  * [`crunch`](http://tools.kali.org/password-attacks/crunch) ([blog post](https://pentestlab.wordpress.com/2012/07/12/creating-wordlists-with-crunch/))
  * [CeWL](https://digi.ninja/projects/cewl.php) ([blog post](http://www.drchaos.com/creating-custom-dictionary-files-using-cewl/))
* Ashley Madison, a famous hacked site
  * [Krebs on Security: Online Cheating Site AshleyMadison Hacked](https://krebsonsecurity.com/2015/07/online-cheating-site-ashleymadison-hacked/)
* "Now Michael Hanson gets buried in my digital cemetary" -> [Steganography](https://en.wikipedia.org/wiki/Steganography), hiding data among other inconspicuous data:
  * [DeepSound](http://jpinsoft.net/deepsound/)
  * Not shown in the episode, but [PixelKnot](https://guardianproject.info/apps/pixelknot/) for steganographic data in images.

During post-show discussion, we brought up:

* [TorMessenger](https://blog.torproject.org/blog/tor-messenger-beta-chat-over-tor-easily)
* [OnionShare](https://onionshare.org/)
* [BeEF](http://beefproject.com/)
* NAT/PAT tables and a bit about [NAT traversal](https://en.wikipedia.org/wiki/NAT_traversal) ("NAT punching")

# Week 2 (S01E02)

* "Evil Corp's corporate mail server hadn't been updated since the days of Shellshock."  
  ![Wget exploiting shellshock, :robot: screenshot 📷](https://web.archive.org/web/20161213025246/https://hackertarget.com/mrrobot/wget-shellshock-john.png)
  * [`wget`](https://en.wikipedia.org/wiki/Wget), a command line tool to get files over the Web
  * [Shellshock](https://en.wikipedia.org/wiki/Shellshock_(software_bug)), a severe and pervasive vulnerability patched in 2014. Read "[Inside Shellshock](https://blog.cloudflare.com/inside-shellshock/)," then try it yourself:
    * [PentesterLab practice VM for CVE-2014-6271](https://pentesterlab.com/exercises/cve-2014-6271)
    * [VulnHub practice VM for CVE-2014-6271](https://www.vulnhub.com/entry/pentester-lab-cve-2014-6271-shellshock,104/)
* "Doesn't even use two-step verification" also known as (2FA) - [Wikipedia page](https://en.wikipedia.org/wiki/Multi-factor_authentication)
  * What are secure "factors"? ->
    1. Something you know (knowledge; e.g., a password)
    1. Something you have (possession; e.g., a physical [security token](https://en.wikipedia.org/wiki/Security_token) such as a [YubiKey](https://www.yubico.com/))
    1. Something you are (biometrics; e.g., a [retinal scan](https://en.wikipedia.org/wiki/Retinal_scan))
* [`john` password cracker](http://www.openwall.com/john/)
* Microwaving electronics:
  * debatable way of destroying info on a hard drive ([use a drill instead](https://www.theguardian.com/uk-news/2014/jan/31/footage-released-guardian-editors-snowden-hard-drives-gchq));
  * microwaving can destroy transistors on chips;
  * effective for [RFID](https://en.wikipedia.org/wiki/Radio-frequency_identification) chips inside credit cards, passports, etc.
* "Who knows how deep these data dumps will get?"
  * "Data dump" is data acquired from a breach; read [Troy Hunt on how he verifies data breaches](https://www.troyhunt.com/heres-how-i-verify-data-breaches/)
  * Also sign up for https://HaveIBeenPwned.org
  * DO. NOT. RE. USE. PASSWORDS. Password managers like [LastPass](http://lastpass.com/), [KeePass](http://keepass.info/), 1Password, etc.
* Darlene is a "malware coder," writes exploits:
  * [McAffee's malware search database](http://www.mcafee.com/threat-intelligence/malware/latest.aspx)
  * [Blog post listing malware sources](https://zeltser.com/malware-sample-sources/)
* "Use your AllSafe security clearance to hack the Comet(R) PLC…"
  * a "PLC" is a [Programmable Logic Controller](https://en.wikipedia.org/wiki/Programmable_logic_controller), embedded devices that are typically used as sensors or controllers for [SCADA](https://en.wikipedia.org/wiki/SCADA) devices (industrial control systems, see also "critical infrastructure," dams, power plants, heating and ventilation [HVAC](https://en.wikipedia.org/wiki/HVAC) and so on)
  * Read: [Target Hackers Broke in Via HVAC Company](http://krebsonsecurity.com/2014/02/target-hackers-broke-in-via-hvac-company/).
* ["Worm"](https://en.wikipedia.org/wiki/Computer_worm): an autonomously propagating malware (distinct from "virus")
* Fernando Vera (a drug dealer) "conducts all his transactions via IMs, emails, and text messages."
  * Use [Signal](https://whispersystems.org/) to protect IM/txt-style communications.
  * Use PGP (aka GPG) to encrypt email communications.
    * [Windows GPG guide](https://ssd.eff.org/en/module/how-use-pgp-windows)
    * [macOS GPG guide](https://ssd.eff.org/en/module/how-use-pgp-mac-os-x)
* "timing his tweets to recent news articles" -> Google Dorking -> see also [Exploit-DB's Google Hacking Database](https://www.exploit-db.com/google-hacking-database/)
  * Using advanced search terms to filter search engine results to far more relevant pieces of information based on time, metadata (title, publisher, outbound and inbound links, etc.)
  * [Wired: Use These Secret NSA Google Search Tips to Become Your Own Spy Agency](https://www.wired.com/2013/05/nsa-manual-on-hacking-internet/) ([PDF](https://commons.wikimedia.org/wiki/File:Untangling_the_Web.pdf))
  * Reference the [GoogleGuide.com site](http://www.googleguide.com/advanced_operators_reference.html)
  * Can "dork" using other search engines, such as GitHub! See [GitHub dorks](https://github.com/techgaun/github-dorks)
* Lockpicking
  * [Toool](http://toool.us/meetings.html) - the largest sport lockpicking group, has meetings in NYC!
  * [Southord](https://www.southord.com/) has good sets!
* DeepSound (again)
* "My album just dropped. … Check track 2 out!" - > social engineering to get Windows malware via autorun on CD
  * [Prevent viruses from using AutoRun to spread](https://support.symantec.com/en_US/article.TECH104447.html)
  * Real-life example: [Sony Rootkit](https://archive.wired.com/politics/security/news/2005/11/69573?currentPage=all)
* Webcam spying! Read about "RATs" (remote access tools/trojans)
  * A (simplistic) overview of [Remote Access Tools](http://resources.infosecinstitute.com/remote-access-tool/)
  * [cover your webcam with tape](https://www.theguardian.com/world/2016/jun/06/surveillance-camera-laptop-smartphone-cover-tape) (or a cam-cover) as an easy mitigation

# Week 3 (S01E03)

* Understaffed/overworked IT departments:
  * [Security Intelligence: Why Overworked Employees Are Security Risks](https://securityintelligence.com/security-risk-staffing-it-teams-overworked-employees/)
* Security risks of old software, read "[Malware Infection Vectors: Past, Present, and Future](https://www.symantec.com/connect/articles/malware-infection-vectors-past-present-and-future)"
  * Windows 98
  * Microsoft Outlook, a common infection vector
* Virus scanners, e.g., [Norton Security Scan](https://security.symantec.com/nss/getnss.aspx?langid=ie&venid=sym)
* [Voice changer](https://en.wikipedia.org/wiki/Voice_changer) (voice disguising software)
* Webcam spying via RATs, read "[Meet the men who spy on women through their webcams](http://arstechnica.com/tech-policy/2013/03/rat-breeders-meet-the-men-who-spy-on-women-through-their-webcams/)"
* "We should also monitor social media traffic, as well as IRC, Pastebin, and set up scripts to keep going, 24/7" - places where data dumps often first appear
  * [Pastebin: Running the site where hackers publicise their attacks](http://www.bbc.com/news/technology-17524822)
  * [The Next Web: Pastebin: How a popular code-sharing site became the ultimate hacker hangout](http://thenextweb.com/socialmedia/2011/06/05/pastebin-how-a-popular-code-sharing-site-became-the-ultimate-hacker-hangout/)
* Facebook location check-ins (also Foursquare, Yelp, any location-based service) - Tyrel following Anwar to the Kiss and Fly club, [learn about "EXIF data"](http://www.howtogeek.com/203592/what-is-exif-data-and-how-to-remove-it/) (metadata in some file formats, like images)
  * [Turn off location tagging for your smartphone camera](https://www.wired.com/2013/07/tip-smartphone-camera-gps/) - Facebook/Instagram photos have can embed GPS coordinates, reveals locations
  * Real-life example: [Fugitive John McAfee’s location revealed by photo meta-data screw-up](https://nakedsecurity.sophos.com/2012/12/03/john-mcafee-location-exif/)
  * [Jeffrey Friedl's Image Metadata Viewer](http://regex.info/exif.cgi/exif.cgi)
  * View file [EXIF Data](http://exifdata.com/)
  * Command-line tools: `exif`, [`ffmpeg`](https://ffmpeg.org/) for extracting metadata from video files
* "With a simple [phishing](https://en.wikipedia.org/wiki/Phishing) scam I owned her password pretty easy."
  * Historical example: [AOHell](https://en.wikipedia.org/wiki/AOHell)
* Mobile phone spyware, [Android device "rooting"](https://lifehacker.com/5789397/the-always-up-to-date-guide-to-rooting-any-android-phone):
  * "RooterFrame" is not real, but [Framaroot](http://framaroot.net/?scn=2) is!
  * Commercial mobile phone malware/spyware software as a service vendors:
    * [FlexiSPY](https://www.flexispy.com/)
    * [Highster Mobile](http://highstermobile.com/)
    * [Spyera](https://spyera.com/)
  * [SuperSU](http://www.supersu.com/) - Android app to manage `sudo`-like access to installed apps
  * Read: [CitizenLab report on iOS "Trident" vulnerabilities installing a RAT against human rights defenders](https://citizenlab.org/2016/08/million-dollar-dissident-iphone-zero-day-nso-group-uae/)
* Identity theft, financial blackmail, "[carding](https://en.wikipedia.org/wiki/Carding_(fraud))" (credit card market)
  * Apply a [credit freeze](https://en.wikipedia.org/wiki/Credit_freeze) to your personal credit line
  * [Krebs On Security: Peek Inside a Professional Carding Shop](https://krebsonsecurity.com/2014/06/peek-inside-a-professional-carding-shop/)
  * [IdentityTheft.gov](https://www.identitytheft.gov/) - US government recommendations/resources to "recover from identity theft"

During post-show discussion, we brought up:

* [Cree.py](http://www.geocreepy.com/) - geolocation OSINT tool
* [TrackIMEI](http://www.trackimei.com/) Using a SIM card/IMEI number to track the location of a mobile phone

# Week 4 (S01E04)

* [Linear Tape-Open (LTO)](https://en.wikipedia.org/wiki/Linear_Tape-Open) is old-school tape cassette storage
  * "Open Standard 9" [doesn't actually exist (yet)](http://www.burameter.com/Articles/ArtMID/422/ArticleID/51/LTO-Tape-Even-Mr-Robot-proof)
* "the circuit board, if installed behind a thermostat, it lets us plant an [asymmetric backdoor](https://en.wikipedia.org/wiki/Backdoor_(computing)#Asymmetric_backdoors) and then create a [VPN](https://en.wikipedia.org/wiki/Virtual_private_network) in the Steel Mountain Intranet."
  * "the circuit board" would be a [Raspberry Pi](https://en.wikipedia.org/wiki/Raspberry_Pi), and LifeHacker has [a good guide to getting started with a Raspberry Pi](https://lifehacker.com/the-always-up-to-date-guide-to-setting-up-your-raspberr-1781419054)
* [HVAC](https://en.wikipedia.org/wiki/HVAC)
* "own the facility's [SCADA](https://en.wikipedia.org/wiki/SCADA) network"
* "the distro"
* FTP server
* Unlocking a car door wirelessly
  * These cars use Passive Keyless Entry and Start (PKES), aka "[Smart key](https://en.wikipedia.org/wiki/Smart_key)"
  * [Security Now! Episode 508, "Exploiting Keyless Entry" show notes (PDF)](https://www.grc.com/sn/sn-508-notes.pdf)
  * See Atmel microchip manufacturer pages on "[Passive Entry/Passive Start (PEPS)](http://www.atmel.com/applications/automotive/car_access/passive-entry-passive-start.aspx)" and "[Remote Keyless Entry (RKE)](http://www.atmel.com/applications/automotive/car_access/remote-keyless-entry.aspx)"
  * ["Relay Attacks on Passive Keyless Entry and Start Systems in Modern Cars" (PDF)](https://eprint.iacr.org/2010/332.pdf)
* Starting a car using its [Controller Area Network (CAN) Bus](https://en.wikipedia.org/wiki/CAN_bus)  
  ![CAN bus hacking, :robot: screenshot 📷](https://web.archive.org/web/20161213025246/https://hackertarget.com/mrrobot/canbus-hack.png)
  * Real-life example, read "[Hackers Remotely Kill a Jeep on the Highway—With Me in It](http://www.wired.com/2015/07/hackers-remotely-kill-jeep-highway/)"
  * [InfoSec Institute: Car Hacking](http://resources.infosecinstitute.com/future-now-car-hacking/)
  * Blog post: [Hacking into a Vehicle CAN bus (Toyothack and SocketCAN)](https://fabiobaltieri.com/2013/07/23/hacking-into-a-vehicle-can-bus-toyothack-and-socketcan/)
  * [`candump` and other Linux-CAN userland utilities](https://github.com/linux-can/can-utils/)
* [Daemon](https://en.wikipedia.org/wiki/Daemon_%28computing%29)
* "Hollywood hacker bullshit," Romero and Mobley are watching ["Hackers" (1995)](https://www.imdb.com/title/tt0113243/)
* "[Rabbit virus](https://en.wikipedia.org/wiki/Rabbit_virus)," also called a [fork bomb](https://en.wikipedia.org/wiki/Fork_bomb)
* "Error 404 Not Found", a well-known HTTP status code
  * See [IANA's HTTP Status Code Registry](https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml)
* Windows malware via autorun on CD, again! ;)

# Week 5 (S01E05)

* [RFID skimming](https://en.wikipedia.org/wiki/RFID_skimming) aka "cloning". Read, "[Hackers Could Clone Your Entry Card from Your Pocket](http://www.tomsguide.com/us/hackers-pin-code-clone-pin-rfid,news-17197.html)" and then [No building access card? No problem if you have new Def Con tools](http://www.computerworld.com/article/2953660/security/no-building-access-card-no-problem-if-you-have-new-def-con-tools.html)  
  ![Messenger bag contains a Tastic RFID Thief, :robot: screenshot 📷](https://web.archive.org/web/20170106001919/https://www.mrrobothacks.com/wp-content/uploads/2016/10/rfid.jpg)  
  ![Key card cloning, :robot: screenshot 📷](https://web.archive.org/web/20170106001938/http://cdn.geekwire.com/wp-content/uploads/2015/07/mrrobot55.png)
  * [Tastic RFID Thief](https://www.bishopfox.com/resources/tools/rfid-hacking/attack-tools/#tastic-rfid-thief), the tool inside Mobley's messenger bag used for copying a proximity card's [radio-frequency identification (RFID)](https://en.wikipedia.org/wiki/Radio-frequency_identification) or [near field communication (NFC)](https://en.wikipedia.org/wiki/Near_field_communication) signals.
  * "xCARD PROGRAMMER - v1.05" is not real, but the [GeZhi HID Cloner V3.0](https://web.archive.org/web/20170106000622/http://www.xfpga.com/pic/big/34_1.jpg) made by [GeZhi Electronic Co](http://www.xfpga.com/) is real! ([HID](https://en.wikipedia.org/wiki/HID_Global) is an contactless access key card brand name.)
  * Article: [Understanding the confusing world of RFID tags and readers in access control](http://www.nedapidentification.com/news/insights/understanding-the-confusing-world-of-rfid-tags-and-readers-in-access-control.html)
  * Same or similar tech is used instead of magnetic strips on credit/debit cards, see [How to Disable Contactless Payment on Your Debit Card](http://www.instructables.com/id/How-to-Disable-Contactless-Payment-on-Your-Debit-C/?ALLSTEPS)
  * Do-It-Yourself [electronic projects](http://www.eng.tau.ac.il/~yash/kw-usenix06/index.html) to make [your own low-cost own RFID cloner](https://hackaday.com/2011/09/30/passive-rfid-tag-cloning/), more at [ProxClone.com](http://www.proxclone.com/)
  * [Offensive Security: Clone RFID Tags with Proxmark3](https://www.offensive-security.com/offsec/cloning-rfid-tags-with-proxmark-3/)
  * [FuzzySecurity: RFID Tutorial (Part 1)](http://www.fuzzysecurity.com/tutorials/rfid/1.html)
  * [RFIDIOt](https://github.com/AdamLaurie/RFIDIOt), a collection of Python utilities to work with RFID and NFC
* Editing Wikipedia with fake information, see [Wikipedia:List of hoaxes on Wikipedia](https://en.wikipedia.org/wiki/Wikipedia:List_of_hoaxes_on_Wikipedia)
* Digital reconnaissance
  * [Maltego](https://paterva.com/web7/docs/documentation.php), a graphical tool for digital reconnaissance
* [Kali Linux](https://www.kali.org/), the penetration testing Linux distribution Romero is using
* "I spoofed a TXT," Mobley says, using the [Social-Engineer Toolkit (SET)](https://github.com/trustedsec/social-engineer-toolkit/)  
  ![Using SET, :robot: screenshot 📷](https://web.archive.org/web/20161213025246/https://hackertarget.com/mrrobot/social-engineer-toolkit.png)
* "It's a palm-print scanner." A form of biometric access control device. Real life vendors:
  * [Fujitsu PalmSecure(R)](http://www.fujitsu.com/us/solutions/business-technology/security/palmsecure/)
  * [BioLink LiveScan](http://biolinksolutions.com/afis-law-enforcement/livescan/)
* "I think you can pick it." More lockpicking.
  * Elliot carries [a covert "lockpick card" set](https://www.lockpickshop.com/CC-LOCK-PICK-SET.html)
* Wire splicing, placing a device directly on the cabling of another wired device
  * Related terms: wire stripping (removing the insulation off electric cables), wire snipping (cutting cables to custom lengths), and wire crimping (attaching connectors to the ends of wires). Some tutorials:
    * [MAKE: How to Splice Wire to NASA Standards](http://makezine.com/2012/02/28/how-to-splice-wire-to-nasa-standards/)
    * [LinuxPlanet: How to Crimp Your Own Ethernet Cables](http://www.linuxplanet.com/linuxplanet/tutorials/6892/1)
    * [Instructables: How to Crimp Cables and Wires!](http://www.instructables.com/id/How-to-Crimp-Cables-and-Wires!/)
  * See also: [DIY.org's "Hardware Hacker" projects](https://diy.org/skills/hardwarehacker).
* Dark Army's IRC chat room:  
  ![IRC chat closeup showing "MOTD" and being "kicked," :robot: screenshot 📷](https://web.archive.org/web/20170205043350/https://i.imgur.com/1OFvB0H.jpg)  
  ![IRC chat closeup showing "/join" command, :robot: screenshot 📷](https://web.archive.org/web/20170205043404/https://i.imgur.com/e2NG0Sz.jpg)
  * IRC commands are written starting with a `/` (a "slash-command"), see [Wikipedia's List of Internet Relay Chat Commands](https://en.wikipedia.org/wiki/List_of_Internet_Relay_Chat_commands)
  * IRC rooms, called "channels," are prefixed with an octothorpe (`#`).
  * [Freenode](https://freenode.net/) is a famous and free public IRC server.
  * Darlene uses `/join #da7Q_9RnPjm` to try joining the room after she was ejected ("kicked"), but she was subsequently banned.
  * ["MOTD" is a UNIX initialism and idiom](https://en.wikipedia.org/wiki/Motd_(Unix)) for "Message of the Day."
* [SSH, the *S*ecure *Sh*ell program](https://en.wikipedia.org/wiki/Secure_Shell), is an encrypted remote login tool, offering command-line access to remote systems attached to a network.  
  ![Closeup of fsociety terminal showing SSH login, :robot: screenshot 📷](https://web.archive.org/web/20170205044319/https://i.imgur.com/h6d2svk.jpg)
  * The `-l` option specifies a *l*ogin (user) name; Darlene is using the `root` user.
  * No passwords were being asked for, so Darlene has [configured SSH for key-based authentication](http://www.systutorials.com/1500/enabling-password-less-ssh-login/). [GitHub has a good guide for setting up SSH with key-based (aka. "password-less") logins](https://help.github.com/articles/connecting-to-github-with-ssh/).
  * On Windows, you may need to install [PuTTY](http://www.putty.org/). On macOS/*nix systems, SSH is usually pre-installed.
  * Complete reference guidebook: [SSH, The Secure Shell: The definitive guide, 2nd Edition](https://web.archive.org/web/20170122005724/https://courseweb.pitt.edu/bbcswebdav/institution/Pitt%20Online/MLIS_Pitt_Online/LIS%202600/Intro%20Module/SSH_Second_Edition.pdf)
  * [Secure Secure Shell](https://stribika.github.io/2015/01/04/secure-secure-shell.html), a guide for the "paranoid" SSH user.

# Week 6 (S01E06)

* Standard industrial control system to operate prison doors?
  *  White paper: "[SCADA & PLC Vulnerabilities In Correctional Facilities](https://web.archive.org/web/20160409040119/http://www.wired.com/images_blogs/threatlevel/2011/07/PLC-White-Paper_Newman_Rad_Strauchs_July22_2011.pdf)"
* Bluetooth scan - what tool did Elliot use?
  * [Blog post with links to various Bluetooth tools](http://www.kalilinuxdojo.com/2015/10/hack-bluetooth-and-other-wireless-tools.html)
* AllSafe uses Windows 8(?) for its office desktop computers
* Office printers (can also be a network vulnerability)
  * [PRET - Printer Exploitation Toolkit](https://github.com/RUB-NDS/PRET#readme)
* Angela uses an iPhone :)
  * Check out [Apple's iOS Security Guide](https://www.apple.com/business/docs/iOS_Security_Guide.pdf)
* Sprinkling USB thumbdrives in the parking lot
* [Avast!](https://www.avast.com/), a low-end anti-virus and anti-malware software suite
  * [Security in a Box's guide to Avast on Windows](https://securityinabox.org/en/guide/avast/windows/)
* "You just pulled code from Rapid9 or some shit? When did you become a script kiddie?"
  * Rapid9 is not real, but is a reference to the famous [Rapid7](https://www.rapid7.com/).
  * A "script kiddie" is hacker lingo for an unskilled techie, like a "noob."
* "Malware detection must have caught it," Elliot says.
  * There are ways to make malware evade anti-virus/anti-malware detection. See, for instance, [Veil-Framework](https://www.veil-framework.com/).
* "I can run circles around an ICS given the right white papers and some time," Darlene says.
  * She probably means an "IDS" or "IPS," an [Intrusion Detection System](https://en.wikipedia.org/wiki/Intrusion_detection_system) or [Intrusion Prevention System](https://en.wikipedia.org/wiki/Intrusion_detection_system#Intrusion_prevention), respectively.
* Terry Colby is wearing an [ankle tether](https://en.wikipedia.org/wiki/Ankle_monitor) - which make & model?
* Elliot's Android-based Wi-Fi scanner - what tool was that?
  * "WPA2, borderline unhackable." - [Cracking of wireless networks](https://en.wikipedia.org/wiki/Cracking_of_wireless_networks)
* Bluetooth hacking, with related terms "[Bluejacking](http://www.bluejackingtools.com/what-is-bluejacking/)," "[Bluebugging](http://www.bluejackingtools.com/bluebugging/)," and "[Bluesnarfing](http://www.bluejackingtools.com/bluesnarfing/)"
  * [`bluesniff`](http://bluesniff.shmoo.com/), a Bluetooth wardriving utility for Linux useful for finding hidden Bluetooth-capable devices
  * `hcitool`
  * `hciconfig`
* Elliot uses a Windows virtual machine(?) to attach to cop car's laptop's Bluetooth keyboard?
* [`ftp`](https://en.wikipedia.org/wiki/File_Transfer_Protocol)
* [Meterpreter](https://www.offensive-security.com/metasploit-unleashed/about-meterpreter/)

# Week 7 (S01E07)

> 🚧 TK-TODO

# Week 8 (S01E08)

> 🚧 TK-TODO