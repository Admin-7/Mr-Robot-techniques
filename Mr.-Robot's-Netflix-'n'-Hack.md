> [[Wiki|Home]] ▸ [[Activities and events]] ▸ **Mr. Robot's Netflix 'n' Hack**

* Tagline: Let Mr. Robot teach you how to hack. (And how to stop hackers from hacking you!)
* Description: Watch an episode of "[Mr. Robot](http://www.imdb.com/title/tt4158110/)," a TV show dramatizing the lives of rogue hackers in NYC with unparalleled technical accuracy, and then get an introduction to how the tools, techniques, and procedures shown in the episode work in real life. After we watch an episode of the show, we'll discuss the tools used, get them installed on our laptops, and try them out. Then we'll meet again next week to show one another what we've learned, and continue with the next episode. By the end of the 10-week season, you'll have gotten a hands-on tour of various tools in the Kali Linux penetration testing distro, and a better sense of how to separate fiction from reality in contemporary hacking dramas in pop culture.
* Facilitating: [[How to facilitate Mr. Robot's Netflix 'n' Hack]]
* See also [[InfoSec]], [Mr. Robot Trains the Trainers](https://github.com/AnarchoTechNYC/meta/tree/master/train-the-trainers/mr-robots-netflix-n-hack/#readme), [🌐 GeekWire's "Mr. Robot Rewind" series](http://www.geekwire.com/tag/mr-robot/) (*contains spoilers*).

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
  ![Elliot deletes outgoing call history, :robot: screenshot 📷](https://web.archive.org/web/20170219210213/https://i.imgur.com/OitLffX.jpg)
  * "This is Sam from Bank of E fraud department."
* `ping`
* Password cracking:  
  ![Output of Elliot's password cracking script, :robot: screenshot 📷](https://web.archive.org/web/20170219205412/https://i.imgur.com/jVXUP0W.jpg)
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
  ![Elliot looks at AllSafe's Security Operations Center (SOC) monitor, :robot: screenshot 📷](https://web.archive.org/web/20170219211108/https://i.imgur.com/dIBabZf.jpg)  
  ![Screenshot of Evil Corp's firewall log file during DDoS attack,  :robot: screenshot 📷](https://web.archive.org/web/20170219211115/https://i.imgur.com/aY1xerf.jpg)
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
  ![Screenshot of using `locate`, `ps` griped to `grep`, :robot: screenshot 📷](https://web.archive.org/web/20170219211851/https://i.imgur.com/4j13i0F.jpg)  
  ![Screenshot of using `more`, :robot: screenshot 📷](https://web.archive.org/web/20170219211843/https://i.imgur.com/YBQRhNq.jpg)  
  ![Screenshot of using `sudo`, `kill`, and `chmod`, :robot: screenshot 📷](https://web.archive.org/web/20170219211843/https://i.imgur.com/YBQRhNq.jpg)
  * `locate`
  * `ps`
  * `grep`
  * `more` (kind of unlikely, Elliot is more likely to use `less` instead)
  * `kill`
  * `rm` (`-norecycle` is not real, is it?)
  * "Reconfigure the access to the directory" -> `chmod`
* "Remember that hacker group, Omegz?" -> This is probably a reference to the real-life group [LulzSec](https://en.wikipedia.org/wiki/LulzSec)
* "I'll ask my IRC contacts…"
  * IRC is [Internet Relay Chat](https://en.wikipedia.org/wiki/Internet_Relay_Chat), an aging chat room technology that is still popular with techies and hackers.
  * Guide to IRC for novices: [IRCHelp.org](http://www.irchelp.org/)
* [VPN](https://en.wikipedia.org/wiki/Virtual_private_network)
* [US Cyber Command](https://en.wikipedia.org/wiki/United_States_Cyber_Command)
* [Google (News) Alerts](https://www.google.com/alerts)
* "…with a custom dictionary, my program can crack his password in two minutes." -> [Generating wordlists](https://netsec.ws/?p=457)  
  ![Screenshot of Elliot building a custom wordlist for password brute forcing, :robot: screenshot📷](https://web.archive.org/web/20170219213210/https://i.imgur.com/M7UWEhq.jpg)
  * [`crunch`](http://tools.kali.org/password-attacks/crunch) ([blog post](https://pentestlab.wordpress.com/2012/07/12/creating-wordlists-with-crunch/))
  * [CeWL](https://digi.ninja/projects/cewl.php) ([blog post](http://www.drchaos.com/creating-custom-dictionary-files-using-cewl/))
* Ashley Madison, a famous hacked site
  * [Krebs on Security: Online Cheating Site AshleyMadison Hacked](https://krebsonsecurity.com/2015/07/online-cheating-site-ashleymadison-hacked/)
* "Now Michael Hansen gets buried in my digital cemetary" -> [Steganography](https://en.wikipedia.org/wiki/Steganography), hiding data among other inconspicuous data:
  * [DeepSound](http://jpinsoft.net/deepsound/)  
  ![Screenshot of using a music stegonographic tool, :robot: screenshot 📷](https://web.archive.org/web/20170219213216/https://i.imgur.com/PxgQwy9.jpg)
  * Not shown in the episode, but [PixelKnot](https://guardianproject.info/apps/pixelknot/) for steganographic data in images.

During post-show discussion, we brought up:

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
  ![Sending an anonymous online tip line on Fernando Vera, :robot: screenshot 📷](https://web.archive.org/web/20170304003134/https://i.imgur.com/ovMz8AL.jpg)
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
  ![Cisco watches Ollie and Angela using a Remote Access Trojan that operates a webcam, :robot: screenshot 📷](https://web.archive.org/web/20170304003311/https://i.imgur.com/A7WSjSj.jpg)
  * A (simplistic) overview of [Remote Access Tools](http://resources.infosecinstitute.com/remote-access-tool/)
  * [cover your webcam with tape](https://www.theguardian.com/world/2016/jun/06/surveillance-camera-laptop-smartphone-cover-tape) (or a cam-cover) as an easy mitigation

# Week 3 (S01E03)

* Understaffed/overworked IT departments:  
  ![William Highsmith, also known as "the IT department," :robot: screenshot 📷](https://web.archive.org/web/20170317230645/https://i.imgur.com/mbDq3Dm.jpg)
  * [Security Intelligence: Why Overworked Employees Are Security Risks](https://securityintelligence.com/security-risk-staffing-it-teams-overworked-employees/)
* Security risks of old software, read "[Malware Infection Vectors: Past, Present, and Future](https://www.symantec.com/connect/articles/malware-infection-vectors-past-present-and-future)"
  * [Windows 98](https://en.wikipedia.org/wiki/Windows_98)
  * [Microsoft Outlook](https://en.wikipedia.org/wiki/Microsoft_Outlook), a "personal information management" package that has become a notorious malware infection vector  
    ![Screenshot of a dated email client, :robot: screenshot 📷](https://web.archive.org/web/20170317230657/https://i.imgur.com/pXs6wAo.jpg)
* Virus scanners, e.g., [Norton Security Scan](https://security.symantec.com/nss/getnss.aspx?langid=ie&venid=sym)  
  ![Performing a "virus scan" on Windows 98, :robot: screenshot 📷](https://web.archive.org/web/20170317230637/https://i.imgur.com/enrz1ij.jpg)
* Hackers can corrupt the integrity of digitized health and medical records  
  ![Elliot Alderson's digitized health records, :robot: screenshot 📷](https://web.archive.org/web/20170317230620/https://i.imgur.com/SSiYRPf.jpg)  
  ![Editing a positive drug panel result to appear like "every other obedient zombie," :robot: screenshot 📷](https://web.archive.org/web/20170317230611/https://i.imgur.com/oyXCjx9.jpg)
  * Privacy concerns amount to breaches of confidentiality, read [Google’s Handling of Public Health Data Should Serve as a Cautionary Tale, Report Says](https://motherboard.vice.com/en_us/article/googles-handling-of-public-health-data-should-serve-as-a-cautionary-tale-report-says)
* [Voice changer](https://en.wikipedia.org/wiki/Voice_changer) (voice disguising software)
* Webcam spying via RATs, read "[Meet the men who spy on women through their webcams](http://arstechnica.com/tech-policy/2013/03/rat-breeders-meet-the-men-who-spy-on-women-through-their-webcams/)"  
  ![Ollie is observed via his laptop's hacked webcam, :robot: screenshot 📷](https://web.archive.org/web/20170317230630/https://i.imgur.com/SVDpCdq.jpg)
* Onion site ("hidden service") used as an IRC server  
  ![Screenshot of a Chinese IRC channel, :robot: screenshot 📷](https://web.archive.org/web/20170317230419/https://i.imgur.com/V08jbFH.jpg)
  * Use [TorMessenger](https://blog.torproject.org/blog/tor-messenger-beta-chat-over-tor-easily) to access such servers easily, if you know the `.onion` address
  * This technique was [used by Anonymous](https://nakedsecurity.sophos.com/2016/04/22/anonymous-launches-onionirc-a-school-for-hacktivists-on-the-dark-web/) for some of their chat services
* "We should also monitor social media traffic, as well as IRC, Pastebin, and set up scripts to keep going, 24/7" - places where data dumps often first appear
  * [Pastebin: Running the site where hackers publicise their attacks](http://www.bbc.com/news/technology-17524822)
  * [The Next Web: Pastebin: How a popular code-sharing site became the ultimate hacker hangout](http://thenextweb.com/socialmedia/2011/06/05/pastebin-how-a-popular-code-sharing-site-became-the-ultimate-hacker-hangout/)
* "Never show them my [source code](https://en.wikipedia.org/wiki/Source_code)"
  * "Closed" versus "open" is a longstanding debate, and is primarily a political divide
  * "Open Source" versus "Free Software," read [Open Source Misses the Point of Free Software](https://www.gnu.org/philosophy/open-source-misses-the-point.html)
* Facebook location check-ins (also Foursquare, Yelp, any location-based service) is how Tyrell follows Anwar to the Kiss and Fly club  
  ![Anwar's profile on Facebook, :robot: screenshot 📷](https://web.archive.org/web/20170317233703/https://i.imgur.com/ZpYw3dd.jpg)  
  ![Anwar's most recent picture posted to Facebook, :robot: screenshot 📷](https://web.archive.org/web/20170317233724/https://i.imgur.com/N3Rq2vP.jpg)
  ![Facebook automatically correlated Anwar's location from his photo metadata, :robot: screenshot 📷](https://web.archive.org/web/20170317233731/https://i.imgur.com/4ZiFJ66.jpg)
  * Seriously, [audit your social media account's privacy settings](https://hackblossom.org/cybersecurity/#privacysettings)
  * Also, learn about [EXIF data](http://www.howtogeek.com/203592/what-is-exif-data-and-how-to-remove-it/) (metadata in some file formats, like images)
    * [Turn off location tagging for your smartphone camera](https://www.wired.com/2013/07/tip-smartphone-camera-gps/) - Facebook/Instagram photos have can embed GPS coordinates, reveals locations
    * Real-life example: [Fugitive John McAfee’s location revealed by photo meta-data screw-up](https://nakedsecurity.sophos.com/2012/12/03/john-mcafee-location-exif/)
    * Web tools: [Jeffrey Friedl's Image Metadata Viewer](http://regex.info/exif.cgi/exif.cgi), [ImageForensic.org](https://www.imageforensic.org/), [EXIFData.com](http://exifdata.com/)
    * Command-line tools: `exif`, [`ffmpeg`](https://ffmpeg.org/) for extracting metadata from video files
* "With a simple [phishing](https://en.wikipedia.org/wiki/Phishing) scam I owned her password pretty easy."  
  ![Elliot's phishing email appears in Shayla's inbox, :robot: screenshot 📷](https://web.archive.org/web/20170317233813/https://i.imgur.com/5js8hxe.jpg)  
  ![Shayla enters her password into Elliot's phishing site, :robot: screenshot 📷](https://web.archive.org/web/20170317233820/https://i.imgur.com/RpstaKr.jpg)
  * Historical example: [AOHell](https://en.wikipedia.org/wiki/AOHell)
  * In modern-day, read "[Highly Effective Gmail Phishing Technique Being Exploited](https://www.wordfence.com/blog/2017/01/gmail-phishing-data-uri/)"
* [Android device "rooting"](https://lifehacker.com/5789397/the-always-up-to-date-guide-to-rooting-any-android-phone) in order to install [commercial phone spyware](https://boingboing.net/2017/02/22/misogyny-with-a-business-model.html):  
  ![Tyrell inserts a microSD card loaded with spyware into Anwar's Android phone, :robot: screenshot 📷](https://web.archive.org/web/20170317235510/https://i.imgur.com/QLyjMts.jpg)  
  ![Tyrell launches a rooting app on Anwar's phone, :robot: screenshot 📷](https://web.archive.org/web/20170317235502/https://i.imgur.com/tCUtRnm.jpg)  
  ![Tyrell reboots Anwar's phone to complete the rooting process, :robot: screenshot 📷](https://web.archive.org/web/20170317235436/https://i.imgur.com/e5fU7Nv.jpg)  
  ![Tyrell installed SuperSU as part of rooting Anwar's Android phone, :robot: screenshot 📷](https://web.archive.org/web/20170317235531/https://i.imgur.com/HiqKGKY.jpg)  
  ![A notification on Anwar's Android phone after being rooted, :robot: screenshot 📷](https://web.archive.org/web/20170317235446/https://i.imgur.com/i9cn04A.jpg)  
  ![SuperSU asks for root access privileges, :robot: screenshot 📷](https://web.archive.org/web/20170317235457/https://i.imgur.com/w666E7Q.jpg)  
  ![The installed spyware asks whether to stealth the SuperSU icon and related artifacts, :robot: screenshot 📷](https://web.archive.org/web/20170317235538/https://i.imgur.com/Ks1ug5J.jpg)  
  ![Tyrell chooses to hide the commercial spyware on Anwar's Android phone, :robot: screenshot 📷](https://web.archive.org/web/20170317235524/https://i.imgur.com/TDrxim2.jpg)  
  ![Tyrell activates his account with the commercial spyware provider to begin surreptitiously collecting data from Anwar's Android phone, :robot: screenshot 📷](https://web.archive.org/web/20170317235426/https://i.imgur.com/CKgTaVV.jpg)  
  * "RooterFrame" is not real, but [Framaroot](http://framaroot.net/?scn=2) is!
  * [SuperSU](http://www.supersu.com/) is real, too! An Android app to manage `sudo`-like access to installed apps
  * Commercial mobile phone malware/spyware software as a service vendors:
    * [FlexiSPY](https://www.flexispy.com/)
    * [Highster Mobile](http://highstermobile.com/)
    * [Spyera](https://spyera.com/)
    * [HelloSpy](http://hellospy.com/)
  * Read: [CitizenLab report on iOS "Trident" vulnerabilities installing a RAT against human rights defenders](https://citizenlab.org/2016/08/million-dollar-dissident-iphone-zero-day-nso-group-uae/)
* Identity theft, financial blackmail, "[carding](https://en.wikipedia.org/wiki/Carding_(fraud))" (credit card market), [doxing](https://en.wikipedia.org/wiki/Doxing)  
  ![Angela's information is caught up in the dox on Ollie, :robot: screenshot 📷](https://web.archive.org/web/20170318001822/https://i.imgur.com/yUuLVN7.jpg)
  * Apply a [credit freeze](https://en.wikipedia.org/wiki/Credit_freeze) to your personal credit line
  * [Krebs On Security: Peek Inside a Professional Carding Shop](https://krebsonsecurity.com/2014/06/peek-inside-a-professional-carding-shop/)
  * [IdentityTheft.gov](https://www.identitytheft.gov/) - US government recommendations/resources to "recover from identity theft"
  * Read [Crash // Override's "Prevent Doxing" guide](http://www.crashoverridenetwork.com/preventingdoxing.html)
* Incident response (IR), and digital forensic examination reports  
  ![Gideon examines Elliot's forensic examiner report on the encrypted .dat file, :robot: screenshot 📷](https://web.archive.org/web/20170318002151/https://i.imgur.com/nSn0Y1o.jpg)
  * [MD5 hashing algorithm](https://en.wikipedia.org/wiki/MD5)
    * hashes (also called digests) are [used in digital forensics extensively](http://forensicswiki.org/wiki/Hashing)
  * [ForensicsWiki](http://forensicswiki.org/wiki/Main_Page) is a Wikipedia-like site for digital forensics tools and standards
  * [SANS Digital Forensics Blog](https://digital-forensics.sans.org/blog/), a regularly-updating industry blog

During post-show discussion, we brought up:

* [Cree.py](http://www.geocreepy.com/) - geolocation OSINT tool
* [TrackIMEI](http://www.trackimei.com/) Using a SIM card/IMEI number to track the location of a mobile phone

# Week 4 (S01E04)

* [Linear Tape-Open (LTO)](https://en.wikipedia.org/wiki/Linear_Tape-Open) is old-school tape cassette storage
  * "Open Standard 9" [doesn't actually exist (yet)](http://www.burameter.com/Articles/ArtMID/422/ArticleID/51/LTO-Tape-Even-Mr-Robot-proof)
* "the circuit board, if installed behind a thermostat, it lets us plant an [asymmetric backdoor](https://en.wikipedia.org/wiki/Backdoor_(computing)#Asymmetric_backdoors) and then create a [VPN](https://en.wikipedia.org/wiki/Virtual_private_network) in the Steel Mountain intranet."  
  ![Elliot holds up a Raspberry Pi, :robot: screenshot 📷](https://web.archive.org/web/20170328205032/https://i.imgur.com/hxA3B4x.png)
  * "the circuit board" would be a [Raspberry Pi](https://en.wikipedia.org/wiki/Raspberry_Pi), and LifeHacker has [a good guide to getting started with a Raspberry Pi](https://lifehacker.com/the-always-up-to-date-guide-to-setting-up-your-raspberr-1781419054)
* [HVAC](https://en.wikipedia.org/wiki/HVAC), again
* "I see six [security vulnerabilities] walking around right now."  
  ![Reconnaissance images of Steel Mountain employees walking about their workplace, :robot: screenshot 📷](https://web.archive.org/web/20170328205909/https://i.imgur.com/egnYzgi.jpg)
  ![Picture of a Steel Mountain externally-mounted surveillance camera, :robot: screenshot 📷](https://web.archive.org/web/20170328205911/https://i.imgur.com/Mdse5aX.jpg)
  * Physical reconnaissance and surveillance, read:
    * [How to Conduct Surveillance Detection On Yourself](https://protectioncircle.org/2016/05/25/surveillance-detection-on-yourself/)
    * [Surveillance Evasion](https://protectioncircle.org/2016/06/14/surveillance-evasion/)
  * Surveillance cameras, read:
    * [Mass. Pirate's CCTV map](http://cctv.masspirates.org/), and [Website Aims to Map Surveillance Cameras Across the Nation, and the World](https://activism.tech/?p=69)
    * "Camover," [Game to Destroy CCTV Cameras: Vandalism or valid protest?](https://www.theguardian.com/theguardian/shortcuts/2013/jan/25/game-destroy-cctv-cameras-berlin)
* "own the facility's [SCADA](https://en.wikipedia.org/wiki/SCADA) network," taking control over the building's control systems (like [IoT](https://en.wikipedia.org/wiki/Internet_of_things), but bigger)
  * [Cyberwar: How a Cyber Attack Left Thousands of Ukrainians in the Dark](https://www.vice.com/en_us/article/tonight-on-viceland-cyberwar-ukraine-lights-out)
  * Read, [Hackers exploit SCADA holes to take full control of critical infrastructure](http://www.computerworld.com/article/2475789/cybercrime-hacking/hackers-exploit-scada-holes-to-take-full-control-of-critical-infrastructure.html)
  * [OWASP SCADA Security Project](https://www.owasp.org/index.php/OWASP_Scada_Security_Project)
* "the distro," slang for "distribution," i.e., the file (payload) being distributed
* [FTP](https://en.wikipedia.org/wiki/File_Transfer_Protocol) server, an older way of transferring files across a network
* Unlocking a car door wirelessly  
  ![Romero uses a wireless keyfob amplifier to remotely unlock a car, :robot: screenshot 📷](https://web.archive.org/web/20170328212519/https://i.imgur.com/CEyOihp.jpg)
  * These cars use Passive Keyless Entry and Start (PKES), aka "[Smart key](https://en.wikipedia.org/wiki/Smart_key)"
  * [Security Now! Episode 508, "Exploiting Keyless Entry" show notes (PDF)](https://www.grc.com/sn/sn-508-notes.pdf)
  * See Atmel microchip manufacturer pages on "[Passive Entry/Passive Start (PEPS)](http://www.atmel.com/applications/automotive/car_access/passive-entry-passive-start.aspx)" and "[Remote Keyless Entry (RKE)](http://www.atmel.com/applications/automotive/car_access/remote-keyless-entry.aspx)"
  * ["Relay Attacks on Passive Keyless Entry and Start Systems in Modern Cars" (PDF)](https://eprint.iacr.org/2010/332.pdf)
* Starting a car using its [Controller Area Network (CAN) Bus](https://en.wikipedia.org/wiki/CAN_bus)  
  ![Mobley uses read the car's control data, :robot: screenshot 📷](https://web.archive.org/web/20170328212925/https://i.imgur.com/hKP7267.jpg)  
  ![CAN-bus hacking, :robot: screenshot 📷](https://web.archive.org/web/20161213025246/https://hackertarget.com/mrrobot/canbus-hack.png)
  * Real-life example, read "[Hackers Remotely Kill a Jeep on the Highway—With Me in It](http://www.wired.com/2015/07/hackers-remotely-kill-jeep-highway/)"
  * [InfoSec Institute: Car Hacking](http://resources.infosecinstitute.com/future-now-car-hacking/)
  * Blog post: [Hacking into a Vehicle CAN bus (Toyothack and SocketCAN)](https://fabiobaltieri.com/2013/07/23/hacking-into-a-vehicle-can-bus-toyothack-and-socketcan/)
  * [`candump` and other Linux-CAN userland utilities](https://github.com/linux-can/can-utils/)
* [Daemon](https://en.wikipedia.org/wiki/Daemon_%28computing%29)
* Breaking into a motel room  
  ![Mobley opens the motel room door, :robot: screenshot 📷](https://web.archive.org/web/20170328213356/https://i.imgur.com/RXsmwij.png)
* "Hollywood hacker bullshit," Romero and Mobley are watching ["Hackers" (1995)](https://www.imdb.com/title/tt0113243/)  
  ![Romero and Mobley kill time watching "Hackers," a movie from 1995 movie, :robot: screenshot 📷](https://web.archive.org/web/20170328213658/https://i.imgur.com/KCdXefY.jpg)
* "[Rabbit virus](https://en.wikipedia.org/wiki/Rabbit_virus)," also called a [fork bomb](https://en.wikipedia.org/wiki/Fork_bomb)
* Trenton prepares the HVAC exploit for Steel Mountain  
  ![Trenton's exploit development setup, :robot: screenshot 📷](https://web.archive.org/web/20170329015222/https://i.imgur.com/en2XoVE.jpg)
  ![Trenton uses a graphical file transfer program to send her exploit to her FTP server, :robot: screenshot 📷](http://web.archive.org/web/https://i.imgur.com/itKd65b.jpg)
  * Trenton's exploit is written in the [Python](https://www.python.org/) programming language, a language popular with attackers (see the book, "[Violent Python: A Cookbook for Hackers, Forensic Analysts, Penetration Testers, and Security Engineers](https://repo.zenk-security.com/Programmation/Violent%20Python%20a%20Cookbook%20for%20Hackers-Forensic%20Analysts-Penetration%20testers%20and%20Security%20Engineers.pdf)")
  * [`tar`](https://en.wikipedia.org/wiki/Tar_%28computing%29), a command to create a single file ("archive") out of many
* "Error 404 Not Found", a well-known HTTP status code
  * See [IANA's HTTP Status Code Registry](https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml)
* Getting rid of mobile phones to avoid being tracked either through [cell tower dumps](https://www.aclu.org/blog/cell-tower-dumps-another-surveillance-technique-another-set-unanswered-questions) or by an [IMSI-catcher](https://en.wikipedia.org/wiki/IMSI-catcher) (a "Stingray")
  * [Wired: Cops and Feds Routinely ‘Dump’ Cell Towers to Track Everyone Nearby](https://www.wired.com/2013/12/massive-domestic-monitorning/)
  * [ACLU: Stingray Tracking Devices, Who's Got Them?](https://www.aclu.org/map/stingray-tracking-devices-whos-got-them)
  * [PrivacySOS.org: How to Defeat FBI or Police Stingray Surveillance](https://privacysos.org/blog/how-to-defeat-fbi-or-police-stingray-surveillance/)
* Employee access cards, usually [RFID](https://en.wikipedia.org/wiki/Radio-frequency_identification) technology activated by proximity  
  ![Angela uses an employee access card to enter AllSafe Cybersecurity offices, :robot: screenshot 📷](https://i.imgur.com/63d95Ip.png)
* Windows malware via autorun on CD, again! ;)  
  ![A command prompt automatically opens on a Windows PC, :robot: screenshot 📷](https://web.archive.org/web/20170328222528/https://i.imgur.com/ezVDz0j.jpg)

# Week 5 (S01E05)

* Copying an employee badge through [RFID skimming](https://en.wikipedia.org/wiki/RFID_skimming) aka "cloning":  
  ![Messenger bag contains a Tastic RFID Thief, :robot: screenshot 📷](https://web.archive.org/web/20170106001919/https://www.mrrobothacks.com/wp-content/uploads/2016/10/rfid.jpg)  
  ![Key card cloning, :robot: screenshot 📷](https://web.archive.org/web/20170106001938/http://cdn.geekwire.com/wp-content/uploads/2015/07/mrrobot55.png)
  * Articles:
    * Tom's Guide: "[Hackers Could Clone Your Entry Card from Your Pocket](http://www.tomsguide.com/us/hackers-pin-code-clone-pin-rfid,news-17197.html)"
    * Computer World: "[No building access card? No problem if you have new Def Con tools](http://www.computerworld.com/article/2953660/security/no-building-access-card-no-problem-if-you-have-new-def-con-tools.html)"
  * [Tastic RFID Thief](https://www.bishopfox.com/resources/tools/rfid-hacking/attack-tools/#tastic-rfid-thief), the tool inside Mobley's messenger bag used for copying a proximity card's [radio-frequency identification (RFID)](https://en.wikipedia.org/wiki/Radio-frequency_identification) or [near field communication (NFC)](https://en.wikipedia.org/wiki/Near_field_communication) signals.
  * "xCARD PROGRAMMER - v1.05" is not real, but the [GeZhi HID Cloner V3.0](https://web.archive.org/web/20170106000622/http://www.xfpga.com/pic/big/34_1.jpg) made by [GeZhi Electronic Co](http://www.xfpga.com/) is real! ([HID](https://en.wikipedia.org/wiki/HID_Global) is an contactless access key card brand name.)
  * Article: [Understanding the confusing world of RFID tags and readers in access control](http://www.nedapidentification.com/news/insights/understanding-the-confusing-world-of-rfid-tags-and-readers-in-access-control.html)
  * Same or similar tech is used instead of magnetic strips on credit/debit cards, see [How to Disable Contactless Payment on Your Debit Card](http://www.instructables.com/id/How-to-Disable-Contactless-Payment-on-Your-Debit-C/?ALLSTEPS)
  * Do-It-Yourself [electronic projects](http://www.eng.tau.ac.il/~yash/kw-usenix06/index.html) to make [your own low-cost own RFID cloner](https://hackaday.com/2011/09/30/passive-rfid-tag-cloning/), more at [ProxClone.com](http://www.proxclone.com/)
  * [Offensive Security: Clone RFID Tags with Proxmark3](https://www.offensive-security.com/offsec/cloning-rfid-tags-with-proxmark-3/)
  * [FuzzySecurity: RFID Tutorial (Part 1)](http://www.fuzzysecurity.com/tutorials/rfid/1.html)
  * [RFIDIOt](https://github.com/AdamLaurie/RFIDIOt), a collection of Python utilities to work with RFID and NFC
* Steel Mountain, Incorporated is probably a reference to the real-world [Iron Mountain, Incorporated](https://en.wikipedia.org/wiki/Iron_Mountain_%28company%29)
* Digital reconnaissance using public information, called [open-source intelligence ("OSINT")](https://en.wikipedia.org/wiki/Open-source_intelligence)
  ![Bill Harper's employee profile page on the public Steel Mountain website, :robot: screenshot 📷](https://web.archive.org/web/20170406194019/https://i.imgur.com/nFqTi5Q.jpg)  
  ![Bill Harper's supervisor, Wendy Gallagher, also has an employee profile page on the public Steel Mountain website, :robot: screenshot 📷](https://web.archive.org/web/20170406194121/https://i.imgur.com/HYQjXLF.jpg)  
  ![Bill Harper's LinkedIn profile page lists his employment status and history, :robot: screenshot 📷](https://web.archive.org/web/20170406201321/https://i.imgur.com/XAN5Gen.jpg)  
  ![Bill Harper's Instagram feed shows his love of cats and betrays his loneliness, :robot: screenshot 📷](https://web.archive.org/web/20170406201331/https://i.imgur.com/eKlkBbk.jpg)
  ![Wendy Gallagher's Instagram feed shows the progression of her pregnancy, :robot: screenshot 📷](https://web.archive.org/web/20170406202101/https://i.imgur.com/J6ucJLd.jpg)  
  ![Wendy Gallagher's Facebook profile photo update celebrates her newborn baby, :robot: screenshot 📷](https://web.archive.org/web/20170406202136/https://i.imgur.com/90paCcU.jpg)  
  ![An Internet search for "Trudy Davis" turns up much less useful information, :robot: screenshot 📷](https://web.archive.org/web/20170406202222/https://i.imgur.com/hT56ONO.jpg)
  * Read, "[This Is Almost Certainly [FBI Director] James Comey’s Twitter Account](https://gizmodo.com/this-is-almost-certainly-james-comey-s-twitter-account-1793843641)"
  * [OSINTFramework.com](http://osintframework.com/), a collection of various OSInt tools broken out by category.
  * [Maltego](https://paterva.com/web7/docs/documentation.php), a graphical tool for digital reconnaissance
* Covert ear-piece, usually connects using Bluetooth to a nearby smartphone
  * Sold as exam or test-taking cheating devices, for example by [GSM-Earpiece](http://www.gsm-earpiece.com/products/)
  * Sold to law enforcement and security services, for example by [EarHero](https://www.earhero.com/)
* Creating a fake or "cover" identity for fictional tech billionaire, "Sam Sepiol"  
  ![Internet search results for "Sam Sepiol" links to Wikipedia and other (fake) news sites, :robot: screenshot 📷](https://web.archive.org/web/20170406195612/https://i.imgur.com/o6b9UEf.jpg)  
  ![Wikipedia page for "Sam Sepiol" sounds convincing and looks authentic, but isn't, :robot: screenshot 📷](https://web.archive.org/web/20170406195620/https://i.imgur.com/sOiUQoC.jpg)  
  ![Mobley uses his own fake identity with which he has accrued reputation within the Wikipedian community to create the "Sam Sepiol" fake page, :robot: screenshot 📷](https://web.archive.org/web/20170406195626/https://i.imgur.com/XD2kw2M.jpg)
  * Editing Wikipedia with fake information, see [Wikipedia:List of hoaxes on Wikipedia](https://en.wikipedia.org/wiki/Wikipedia:List_of_hoaxes_on_Wikipedia)
  * [LifeHacker: How to Choose (and Maintain) a Cover Identity](https://lifehacker.com/5960441/how-to-choose-and-maintain-a-cover-identity)
  * [FakeNameGenerator.com](http://www.fakenamegenerator.com/), automatically generated yet realistic-sounding fake names, addresses, passwords, and more
  * On "fake news" and spotting hoaxes:
    * [How Fake News Goes Viral: A Case Study](https://www.nytimes.com/2016/11/20/business/media/how-fake-news-spreads.html)
    * [Fake Or Real? How To Self-Check The News And Get The Facts](http://www.npr.org/sections/alltechconsidered/2016/12/05/503581220/fake-or-real-how-to-self-check-the-news-and-get-the-facts)
    * [Snopes.com](http://snopes.com), a famous fact-checking site for debunking popular hoaxes
* [Kali Linux](https://www.kali.org/), the penetration testing Linux distribution Romero is using
* "I spoofed a TXT," Mobley says, using the [Social-Engineer Toolkit (SET)](https://github.com/trustedsec/social-engineer-toolkit/)  
  ![Using SET, :robot: screenshot 📷](https://web.archive.org/web/20161213025246/https://hackertarget.com/mrrobot/social-engineer-toolkit.png)  
  ![Mobley uses a generic psychological ploy to lure Trudy Davis away with a spoofed SMS message from her husband's number, :robot: screenshot 📷](https://web.archive.org/web/20170406202309/https://i.imgur.com/sePP34T.jpg)
* "It's a palm-print scanner." A form of biometric access control device.  
  ![The elevators in Steel Mountain use palm-print scanners, :robot: screenshot 📷](https://web.archive.org/web/20170406202502/https://i.imgur.com/qB49RQz.jpg)
  * Real life vendors:
    * [Fujitsu PalmSecure(R)](http://www.fujitsu.com/us/solutions/business-technology/security/palmsecure/)
    * [BioLink LiveScan](http://biolinksolutions.com/afis-law-enforcement/livescan/)
* "There's one door, manually locked. It's a fire code thing, and I think you can pick it."  
  ![Romero has downloaded a PDF file showing the Steel Mountain facility's floor plan, :robot: screenshot 📷](https://web.archive.org/web/20170406202714/https://i.imgur.com/txlMdmp.jpg)  
  ![Elliot uses a covert lockpick card set to pick the lock on a stairwell door in Steel Mountain, :robot: screenshot 📷](https://web.archive.org/web/20170406202950/https://i.imgur.com/3AEtWYh.jpg)
  * Elliot carries [a covert "lockpick card" set](https://www.lockpickshop.com/CC-LOCK-PICK-SET.html)
* Wire splicing, placing a device directly on the cabling of another wired device  
  ![Elliot installs a Raspberry Pi behind a thermostat in Steel Mountain, :robot: screenshot 📷](https://web.archive.org/web/20170406203408/https://i.imgur.com/PnvGjL1.jpg)
  ![The "Air-Dream-Software, Inc" thermostat in Steel Mountain, :robot: screenshot 📷](https://web.archive.org/web/20170406203538/https://i.imgur.com/MSJr9YQ.jpg)
  * Related terms: wire stripping (removing the insulation off electric cables), wire snipping (cutting cables to custom lengths), and wire crimping (attaching connectors to the ends of wires). Some tutorials:
    * [MAKE: How to Splice Wire to NASA Standards](http://makezine.com/2012/02/28/how-to-splice-wire-to-nasa-standards/)
    * [LinuxPlanet: How to Crimp Your Own Ethernet Cables](http://www.linuxplanet.com/linuxplanet/tutorials/6892/1)
    * [Instructables: How to Crimp Cables and Wires!](http://www.instructables.com/id/How-to-Crimp-Cables-and-Wires!/)
  * See also: [DIY.org's "Hardware Hacker" projects](https://diy.org/skills/hardwarehacker).
* Dark Army's IRC chat room:  
  ![The chat log between fsociety and the Dark Army in their "IRC island," :robot: screenshot 📷](https://web.archive.org/web/20170407072435/https://i.imgur.com/BwYvMqk.jpg)  
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

* Standard industrial control systems *do* operate some prison's doors:
  *  White paper "[SCADA & PLC Vulnerabilities In Correctional Facilities](https://web.archive.org/web/20160409040119/http://www.wired.com/images_blogs/threatlevel/2011/07/PLC-White-Paper_Newman_Rad_Strauchs_July22_2011.pdf)" and [associated conference presentation by the authors](https://www.youtube.com/watch?v=1MTLuLBiKcc).
* Finding nearby Bluetooth devices  
  ![Elliot scans nearby Bluetooth devices to scan Isaac's iPhone, :robot: screenshot 📷](https://web.archive.org/web/20161213025246/https://hackertarget.com/mrrobot/btscanner-phone.png)
  * [`btscanner`](http://www.pentest.co.uk/downloads.html) ([manual page](http://manpages.ubuntu.com/manpages/utopic/man1/btscanner.1.html)), a tool to extract as much information as possible from a Bluetooth device without  pairing with it
  * [Blog post with links to various Bluetooth tools](https://web.archive.org/web/20161024111000/http://www.kalilinuxdojo.com/2015/10/hack-bluetooth-and-other-wireless-tools.html)
* AllSafe uses Windows 8(?) for its office desktop computers
* [Multifunction printers](https://en.wikipedia.org/wiki/Multifunction_printer) can do more than you might think! Privacy issues and network vulnerability:
  ![Angela prints her research documents with one of AllSafe's printers, :robot: screenshot 📷](https://web.archive.org/web/20170411220804/https://i.imgur.com/fcWrqHP.jpg)
  * [Printer steganography](https://en.wikipedia.org/wiki/Printer_steganography)
  * EFF's privacy advocacy:
    * [Is Your Printer Spying On You?](https://www.eff.org/issues/printers)
    * [List of printers which do or do not display tracking dots](https://www.eff.org/pages/list-printers-which-do-or-do-not-display-tracking-dots)
    * [Tracking Dot Decoding Guide](https://w2.eff.org/Privacy/printers/docucolor/)
  * Article, [Government Uses Color Laser Printer Technology to Track Documents](http://www.pcworld.com/article/118664/article.html)
  * Printers are often a vulnerable device on corporate networks:
    * Article, [Exploiting Corporate Printers](http://resources.infosecinstitute.com/exploiting-corporate-printers/)
    * Blog post, [Printer Exploitation in Corporate Environments](https://www.hackingloops.com/printer-exploitation-in-corporate-environments/)
    * [PRET - Printer Exploitation Toolkit](https://github.com/RUB-NDS/PRET#readme)
* Angela uses an iPhone :)
  ![Angela opens her iPhone's home screen to check a missed call, :robot: screenshot 📷](https://web.archive.org/web/20170411221239/https://i.imgur.com/RNWv775.jpg)
  * Check out [Apple's iOS Security Guide](https://www.apple.com/business/docs/iOS_Security_Guide.pdf)
* Sprinkling USB thumbdrives in the parking lot  
  ![Darlene drops USB thumbdrives in the police station's parking lot, :robot: screenshot 📷](https://web.archive.org/web/20170411221611/https://i.imgur.com/NNZ3Lkd.jpg)
  * Read, "[Almost Half of Dropped USB Sticks Will Get Plugged In](https://nakedsecurity.sophos.com/2016/04/08/almost-half-of-dropped-usb-sticks-will-get-plugged-in/)"
  * Real-life example: [Russian hackers infiltrated NATO using cheap retail thumbdrives](https://web.archive.org/web/20170311014501/https:/twitter.com/Mathew__Clayton/status/837605847257792512/photo/1)
* [Avast!](https://www.avast.com/), a low-end anti-virus and anti-malware software suite
  * [Security in a Box's guide to Avast on Windows](https://securityinabox.org/en/guide/avast/windows/)
* "You just pulled code from Rapid9 or some shit? When did you become a script kiddie?"
  * Rapid9 is not real, but is a reference to the famous [Rapid7](https://www.rapid7.com/).
  * A "[script kiddie](https://www.urbandictionary.com/define.php?term=script%20kiddie)" is hacker lingo for an unskilled techie, like a "noob" or "newbie."
* "Malware detection must have caught it," Elliot says.
  * There are ways to make malware evade anti-virus/anti-malware detection. See, for instance, [Veil-Framework](https://www.veil-framework.com/).
* An ICS is an [Industrial Control System](https://en.wikipedia.org/wiki/Industrial_control_system): "I can run circles around an ICS given the right white papers and some time," Darlene says.
  * She might also mean an "IDS" or "IPS," an [Intrusion Detection System](https://en.wikipedia.org/wiki/Intrusion_detection_system) or [Intrusion Prevention System](https://en.wikipedia.org/wiki/Intrusion_detection_system#Intrusion_prevention), respectively.
* Terry Colby is wearing an [ankle tether](https://en.wikipedia.org/wiki/Ankle_monitor) - which make & model?
* Elliot's Android-based Wi-Fi scanner - what tool was that?
  * "WPA2, borderline unhackable." - [Cracking of wireless networks](https://en.wikipedia.org/wiki/Cracking_of_wireless_networks)
* Bluetooth hacking, with related terms "[Bluejacking](http://www.bluejackingtools.com/what-is-bluejacking/)," "[Bluebugging](http://www.bluejackingtools.com/bluebugging/)," and "[Bluesnarfing](http://www.bluejackingtools.com/bluesnarfing/)"
  * [`bluesniff`](http://bluesniff.shmoo.com/), a Bluetooth wardriving utility for Linux useful for finding hidden Bluetooth-capable devices
  * [`hcitool`](http://linuxcommand.org/man_pages/hcitool1.html), command-line utility to communicate with Bluetooth device and create device-to-device connections
  * [`hciconfig`](http://linuxcommand.org/man_pages/hciconfig8.html), command-line utility to configure a system's Bluetooth devices
* Elliot uses a Windows virtual machine(?) to attach to cop car's laptop's Bluetooth keyboard?
* [`ftp`](https://en.wikipedia.org/wiki/File_Transfer_Protocol)
* [Meterpreter](https://www.offensive-security.com/metasploit-unleashed/about-meterpreter/)

# Week 7 (S01E07)

* [Netscape Communicator](https://en.wikipedia.org/wiki/Netscape_Communicator), one of the early pioneering Web browsers in the 1990's
  * Check out the [evolt.org Browser Archive](http://browsers.evolt.org/), copies of every version of every Web browser ever released
* [Windows 95](https://en.wikipedia.org/wiki/Windows_95) (or Windows 98)
* [2600.com](https://www.2600.com/), a famous, long-running hacker periodical
  * View [the 1999 version of the 2600.com website](https://web.archive.org/web/19990116232336/http://www.2600.com/mindex.html) using [the Internet Archive's Wayback Machine](https://archive.org/web/).
* [Atari 2600](https://en.wikipedia.org/wiki/Atari_2600), a 1980's-era video game console
* ["View source" functionality in Web browsers](http://www.computerhope.com/issues/ch000746.htm)
* [Deepsound](http://jpinsoft.net/deepsound/) (again)
* [Microchip implants](https://en.wikipedia.org/wiki/Microchip_implant_%28animal%29) (in Flipper)

# Week 8 (S01E08)

> 🚧 TK-TODO