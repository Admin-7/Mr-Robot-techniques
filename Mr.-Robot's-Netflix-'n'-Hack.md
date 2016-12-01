> [[Wiki|Home]] ▸ [[Activities and events]] ▸ **Mr. Robot's Netflix 'n' Hack**

* Tagline: Let Mr. Robot teach you how to hack.
* Description: Watch an episode of "[Mr. Robot](http://www.imdb.com/title/tt4158110/)," a TV show dramatizing the lives of rogue hackers in NYC with unparalleled technical accuracy, and then get an introduction to how the tools, techniques, and procedures shown in the episode work in real life. After we watch an episode of the show, we'll discuss the tools used, get them installed on our laptops, and try them out. Then we'll meet again next week to show one another what we've learned, and continue with the next episode. By the end of the 10-week season, you'll have gotten a hands-on tour of various tools in the Kali Linux penetration testing distro, and a better sense of how to separate fiction from reality in contemporary hacking dramas in pop culture.
* Facilitating: [[How to facilitate Mr. Robot's Netflix 'n' Hack]]
* See also [[InfoSec]].

Watch the [Mr. Robot trailer](http://www.youtube.com/watch?v=U94litUpZuc) to see if this is a show you might enjoy watching and learning from:

[![Mr. Robot Season 1, extended trailer](http://img.youtube.com/vi/U94litUpZuc/0.jpg)](http://www.youtube.com/watch?v=U94litUpZuc)

* [Week 1 (S01E01)](#week-1-s01e01)
* [Week 2 (S01E02)](#week-2-s01e02)
* [Week 3 (S01E03)](#week-3-s01e03)

# Week 1 (S01E01)

* [Tor](https://torproject.org/)
  * [Onion routing](https://en.wikipedia.org/wiki/Onion_routing),
  * ["Onion services" (formerly known as "hidden services")](https://www.torproject.org/docs/hidden-services.html.en)
  * "Deep Web" sites ([how to search](http://deep-web.org/how-to-research/deep-web-search-engines/), check out [The Hidden Wiki](https://thehiddenwiki.org/))
* [RUDY attacks](https://en.wikipedia.org/wiki/Denial-of-service_attack#R-U-Dead-Yet.3F_.28RUDY.29)
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
* "DDoS attack"
  * "DDoS protection" - really, really big pipes, see [CloudFlare](https://www.cloudflare.com/ddos/)
* DNS
* "fingerblasting"
* `astsu` is [not real](https://www.leaseweb.com/labs/2015/09/linux-commands-astu-and-astsu-in-mr-robot/), but! `traceroute` is
* [rootkit](https://en.wikipedia.org/wiki/Rootkit)
* `ifconfig` ("redirect the traffic"), when done on a router, we're probably more talking more about [CISCO iOS switches](https://en.wikipedia.org/wiki/Cisco_IOS)
  * [VyOS](https://vyos.io/) is a free software clone of Cisco's iOS, useful if you can't pay for an iOS license
* On the server's command line:
  * `locate`
  * `kill`
  * `rm` (`-norecycle` is not real, is it?)
  * "Reconfigure the access to the directory" -> `chmod`
* "I'll ask my IRC contacts…"
  * [IRC](http://www.irchelp.org/) is Internet chat rooms before the Web came around and shoved everything over port 80
* [VPN](https://en.wikipedia.org/wiki/Virtual_private_network)
* [US Cyber Command](https://en.wikipedia.org/wiki/United_States_Cyber_Command)
* [Google (News) Alerts](https://www.google.com/alerts)
* "…with a custom dictionary, my program can crack his password in two minutes." -> [Generating wordlists](https://netsec.ws/?p=457)
  * [`crunch`](http://tools.kali.org/password-attacks/crunch) ([blog post](https://pentestlab.wordpress.com/2012/07/12/creating-wordlists-with-crunch/))
  * [CeWL](https://digi.ninja/projects/cewl.php) ([blog post](http://www.drchaos.com/creating-custom-dictionary-files-using-cewl/))
* "Now Michael Hanson gets buried in my digital cemetary" -> [Steganography](https://en.wikipedia.org/wiki/Steganography), hiding data among other inconspicuous data:
  * [DeepSound](http://jpinsoft.net/deepsound/)
  * Not shown in the episode, but [PixelKnot](https://guardianproject.info/apps/pixelknot/) for steganographic data in images.

During post-show discussion, we brought up:

* [TorMessenger](https://blog.torproject.org/blog/tor-messenger-beta-chat-over-tor-easily)
* [OnionShare](https://onionshare.org/)
* [BeEF](http://beefproject.com/)
* NAT/PAT tables and a bit about [NAT traversal](https://en.wikipedia.org/wiki/NAT_traversal) ("NAT punching")

## 

# Week 2 (S01E02)

* [Shellshock](https://en.wikipedia.org/wiki/Shellshock_(software_bug)), a severe and pervasive vulnerability patched in 2014. ("Evil Corp's corporate mail server hadn't been updated since the days of Shellshock.") Try it yourself:
  * [PentesterLab practice VM for CVE-2014-6271](https://pentesterlab.com/exercises/cve-2014-6271)
  * [VulnHub practice VM for CVE-2014-6271](https://www.vulnhub.com/entry/pentester-lab-cve-2014-6271-shellshock,104/)
* "Doesn't even use two-step verification" also known as (2FA) - [Wikipedia page](https://en.wikipedia.org/wiki/Multi-factor_authentication)
  * What are secure "factors"? ->
    1. Something you know (knowledge; e.g., password)
    1. Something you have (posession)
    1. Something you are (biometrics)
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
* "Look at Pastebin, IRC, and set up scripts to monitor round the clock" - places where data dumps often first appear
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

> 🚧 TK-TODO