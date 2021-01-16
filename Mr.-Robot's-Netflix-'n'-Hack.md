> [[Wiki|Home]] ▸ [[Activities and events]] ▸ **Mr. Robot's Netflix 'n' Hack**

* Tagline: Let Mr. Robot teach you how to hack—and how to stop hackers from hacking you!
* Description: Watch an episode of "[Mr. Robot](https://www.themoviedb.org/tv/62560-mr-robot)," a TV show dramatizing the lives of rogue hackers in NYC with unparalleled technical accuracy, and then get an introduction to how the tools, techniques, and procedures ("[TTPs](https://forensicswiki.xyz/wiki/index.php?title=Cyber_Threat_Intelligence#TTP)") shown in the episode work in real life. After we watch an episode of the show, we'll discuss the tools used, get them installed on our laptops, and try them out. When we meet next, we'll show one another what we've learned, and continue with the next episode. By the end of the 10 week first season, you'll have gotten a hands-on tour of various tools in the [Kali Linux](https://www.kali.org/) penetration testing distro, and a better sense of how to separate fiction from reality in contemporary hacking dramas in pop culture. We'll finish by tackling [a Mr. Robot themed hacking challenge](https://www.vulnhub.com/entry/mr-robot-1,151/) so you can practice what you've learned, and maybe even join a [[hacking team|CTF team]].
* Facilitating: [[How to facilitate Mr. Robot's Netflix 'n' Hack]]
* See also: [[InfoSec]], [Mr. Robot Trains the Trainers](https://github.com/AnarchoTechNYC/meta/tree/master/train-the-trainers/mr-robots-netflix-n-hack/#readme), [🌐 GeekWire's "Mr. Robot Rewind" series](http://www.geekwire.com/tag/mr-robot/) (*contains spoilers*), [Manisso/fsociety](https://github.com/Manisso/fsociety), [[Glossary]].

Watch the [Mr. Robot trailer](http://www.youtube.com/watch?v=U94litUpZuc) to see if this is a show you might enjoy watching and learning from:

[![Mr. Robot Season 1, extended trailer](http://img.youtube.com/vi/U94litUpZuc/0.jpg)](http://www.youtube.com/watch?v=U94litUpZuc)

1. [🌐 Season 1](https://www.themoviedb.org/tv/62560-mr-robot/season/1)
    1. [Week 1 (S01E01)](#week-1-s01e01)
    1. [Week 2 (S01E02)](#week-2-s01e02)
    1. [Week 3 (S01E03)](#week-3-s01e03)
    1. [Week 4 (S01E04)](#week-4-s01e04)
    1. [Week 5 (S01E05)](#week-5-s01e05)
    1. [Week 6 (S01E06)](#week-6-s01e06)
    1. [Week 7 (S01E07)](#week-7-s01e07)
    1. [Week 8 (S01E08)](#week-8-s01e08)
    1. [Week 9 (S01E09)](#week-9-s01e09)
    1. [Week 10 (S01E10)](#week-10-s01e10)
1. [🌐 Season 2](https://www.themoviedb.org/tv/62560-mr-robot/season/2)
    1. [Week 11 (S02E01)](#week-11-s02e01)
    1. [Week 12 (S02E02)](#week-12-s02e02)
    1. [Week 13 (S02E03)](#week-13-s02e03)
    1. [Week 14 (S02E04)](#week-14-s02e04)
    1. [Week 15 (S02E05)](#week-15-s02e05)
    1. [Week 16 (S02E06)](#week-16-s02e06)
    1. [Week 17 (S02E07)](#week-17-s02e07)
    1. [Week 18 (S02E08)](#week-18-s02e08)
    1. [Week 19 (S02E09)](#week-19-s02e09)
    1. [Week 20 (S02E10)](#week-20-s02e10)
    1. [Week 21 (S02E11)](#week-21-s02e11)
    1. [Week 22 (S02E12)](#week-22-s02e12)
1. [🌐 Season 3](https://www.themoviedb.org/tv/62560-mr-robot/season/3)
    1. [Week 23 (S03E01)](#week-23-s03e01)
    1. [Week 24 (S03E02)](#week-24-s03e02)
    1. [Week 25 (S03E03)](#week-25-s03e03)
    1. [Week 26 (S03E04)](#week-26-s03e04)
    1. [Week 27 (S03E05)](#week-27-s03e05)
    1. [Week 28 (S03E06)](#week-28-s03e06)
    1. [Week 29 (S03E07)](#week-29-s03e07)
    1. [Week 30 (S03E08)](#week-30-s03e08)
    1. [Week 31 (S03E09)](#week-31-s03e09)
    1. [Week 32 (S03E10)](#week-32-s03e10)
1. [🌐 Season 4](https://www.themoviedb.org/tv/62560-mr-robot/season/4)
    1. [Week 33 (S04E01)](#week-33-s04e01)
    1. [Week 34 (S04E02)](#week-34-s04e02)
    1. [Week 35 (S04E03)](#week-35-s04e03)
    1. [Week 36 (S04E04)](#week-36-s04e04)
    1. [Week 37 (S04E05)](#week-37-s04e05)
    1. [Week 38 (S04E06)](#week-38-s04e06)
    1. [Week 39 (S04E07)](#week-39-s04e07)
    1. [Week 40 (S04E08)](#week-40-s04e08)
    1. [Week 41 (S04E09)](#week-41-s04e09)
    1. [Week 42 (S04E10)](#week-42-s04e10)
    1. [Week 43 (S04E11)](#week-43-s04e11)
    1. [Week 44 (S04E12)](#week-44-s04e12)
    1. [Week 45 (S04E13)](#week-45-s04e13)

# Week 1 (S01E01)

* [Tor](https://torproject.org/), a commonly used privacy-enhancing and censorship circumvention internetworking tool
  * [Onion routing](https://en.wikipedia.org/wiki/Onion_routing),
  * "[[Onion services]]" [(formerly known as "hidden services")](https://www.torproject.org/docs/hidden-services.html.en)
  * "[Deep Web](https://www.youtube.com/watch?v=CHOjbPI-B8E)" sites ([how to search](http://deep-web.org/how-to-research/deep-web-search-engines/), check out [The Hidden Wiki](https://thehiddenwiki.org/))
  * [OnionShare](https://onionshare.org/) sets up an ephemeral Onion service for filesharing; read [Secretly sharing files with OnionShare and Tor Browser](https://github.com/AnarchoTechNYC/meta/blob/master/train-the-trainers/mr-robots-netflix-n-hack/week-1/secretly-sharing-files-with-onionshare-and-tor-browser/README.md).
  * [OnionScan](https://onionscan.org/), "a free and open source tool for investigating the Dark Web."
* [RUDY attacks](https://en.wikipedia.org/wiki/Denial-of-service_attack#R-U-Dead-Yet.3F_.28RUDY.29)
  * [Incapsula's DDoS Attack Glossary entry for "RUDY attack"](https://www.incapsula.com/ddos/attack-glossary/rudy-r-u-dead-yet.html)
* "Good at reading people" ([social engineering](https://en.wikipedia.org/wiki/Social_engineering_%28security%29)…a [blog post](https://web.archive.org/web/20020125012547/http://www.securityfocus.com/cgi-bin/infocus.pl?id=1527) to maybe read, also a book [The Art of Deception](http://sbisc.ut.ac.ir/wp-content/uploads/2015/10/mitnick.pdf), see also: [Freedom Downtime](https://www.youtube.com/watch?v=qMzRRVgEuWc))
  * "I left my keys in one of your cabs…"
  * "Can I borrow your phone?" (also deleted the outgoing call log)  
  ![Elliot deletes outgoing call history, :robot: screenshot 📷](https://web.archive.org/web/20170219210213/https://i.imgur.com/OitLffX.jpg)
  * "This is Sam from Bank of E fraud department."
* [`ping`](https://en.wikipedia.org/wiki/Ping_%28networking_utility%29) is the "*p*acket *in*formation *g*roper"
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
  * [Deep Inside a DNS Amplification DDoS Attack](https://blog.cloudflare.com/deep-inside-a-dns-amplification-ddos-attack/), and later, [an NTP amplification DDoS attack](https://blog.cloudflare.com/technical-details-behind-a-400gbps-ntp-amplification-ddos-attack/)
  * "DDoS protection" - really, really big pipes, see [CloudFlare](https://www.cloudflare.com/ddos/), [Google's Project Shield](https://projectshield.withgoogle.com/public/), and [Deflect.ca](https://deflect.ca/)
  * ["DDoS as Direct Action," chapter three of The Coming Swarm, by Molly Sauter](http://oddletters.com/files/2014/04/Sauter-The-Coming-Swarm-CC-Copy.pdf) (PDF)
* DNS
* "fingerblasting"
  * Historical sidenote: read about the [`finger` Protocol](https://en.wikipedia.org/wiki/Finger_protocol)
* `astsu` is [not real](https://www.leaseweb.com/labs/2015/09/linux-commands-astu-and-astsu-in-mr-robot/), but! `traceroute` is
* [rootkit](https://en.wikipedia.org/wiki/Rootkit)
  * Blog post: [Basics of Making a Rootkit](https://web.archive.org/web/20170810234123/https://d0hnuts.com/2016/12/21/basics-of-making-a-rootkit-from-syscall-to-hook/)
* "Redirect the traffic…" Gideon says.
  * Using [`ifconfig`](https://linux.die.net/man/8/ifconfig), a command line tool to *config*ure a network *i*nter*f*ace.
  * "Routers" are just computers, but with dedicated operating systems with different network interface configuration commands, such as [CISCO iOS](https://en.wikipedia.org/wiki/Cisco_IOS) (proprietary) or [VyOS](https://vyos.io/), a free software clone of Cisco's iOS, useful if you can't pay for an iOS license.
  * "Redirecting," in the context of the episode's scene, may mean:
    * re-route incoming packets that are part of the DDoS to [a network black hole](https://en.wikipedia.org/wiki/Black_hole_%28networking%29), if the packets can be identified as part of the attack.
    * And if not, then he may mean "redirect" incoming visitors to a [high-availability](https://en.wikipedia.org/wiki/High_availability) version of the hosted services, such as a read-only or otherwise low-resource use instance.
    * The specific intent depends on AllSafe's and ECorp's specific setup, and it's not clear what's actually happening, except that this is the kind of chatter you might hear from [SOC](https://en.wikipedia.org/wiki/Security_operations_center) or [NOC](https://en.wikipedia.org/wiki/Network_operations_center) workers.
* "…and call [Prolexic](https://en.wikipedia.org/wiki/Prolexic_Technologies) for help!"
* On the server's command line:  
  ![Screenshot of using `locate`, `ps` griped to `grep`, :robot: screenshot 📷](https://web.archive.org/web/20170219211851/https://i.imgur.com/4j13i0F.jpg)  
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

# Week 2 (S01E02)

* "Evil Corp's corporate mail server hadn't been updated since the days of Shellshock."  
  [![Wget exploiting shellshock, :robot: screenshot 📷](https://web.archive.org/web/20161213025246/https://hackertarget.com/mrrobot/wget-shellshock-john.png)](https://github.com/AnarchoTechNYC/meta/blob/master/train-the-trainers/mr-robots-netflix-n-hack/week-2/strengthening-passwords-to-defend-against-john/Mr.%20Robot%20S01E02%20-%20Hacking%20Tyrell%20Wellick.mp4?raw=true)
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
  * [Mr. Robot Trains the Trainers password cracking lab: "Strengthening passwords to defend against `john`"](https://github.com/AnarchoTechNYC/meta/blob/master/train-the-trainers/mr-robots-netflix-n-hack/week-2/strengthening-passwords-to-defend-against-john/README.md)
* Microwaving electronics:
  * debatable way of destroying info on a hard drive ([use a drill instead](https://www.theguardian.com/uk-news/2014/jan/31/footage-released-guardian-editors-snowden-hard-drives-gchq));
  * microwaving can destroy transistors on chips;
  * effective for [RFID](https://en.wikipedia.org/wiki/Radio-frequency_identification) chips inside credit cards, passports, etc.
* "Who knows how deep these data dumps will get?"
  * "Data dump" is data acquired from a breach; read [Troy Hunt on how he verifies data breaches](https://www.troyhunt.com/heres-how-i-verify-data-breaches/)
  * Also sign up for https://HaveIBeenPwned.org
  * DO. NOT. RE. USE. PASSWORDS. Do [use password managers](https://github.com/AnarchoTechNYC/meta/tree/master/train-the-trainers/mr-robots-netflix-n-hack/week-2/strengthening-passwords-to-defend-against-john#using-a-password-manager) like [LastPass](http://lastpass.com/), [KeePass](http://keepass.info/), [etc](https://prism-break.org/en/all/#password-managers).
* Darlene is a "malware coder," writes exploits:
  * [McAffee's malware search database](http://www.mcafee.com/threat-intelligence/malware/latest.aspx)
  * [Blog post listing malware sources](https://zeltser.com/malware-sample-sources/)
* "Use your AllSafe security clearance to hack the Comet(R) PLC…"
  * a "PLC" is a [Programmable Logic Controller](https://en.wikipedia.org/wiki/Programmable_logic_controller), embedded devices that are typically used as sensors or controllers for [SCADA](https://en.wikipedia.org/wiki/SCADA) devices (industrial control systems, see also "critical infrastructure," dams, power plants, heating and ventilation [HVAC](https://en.wikipedia.org/wiki/HVAC) and so on)
  * Read: [Target Hackers Broke in Via HVAC Company](http://krebsonsecurity.com/2014/02/target-hackers-broke-in-via-hvac-company/), [Hackers Find Celebrities’ Weak Links in Their Vendor Chains](https://www.nytimes.com/2017/05/07/technology/hackers-exploit-celebrities-vendor-chains.html)
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
* [Lockpicking](https://github.com/meitar/awesome-lockpicking/#readme)  
  ![Elliot picks the lock to Shayla's bathroom door after Fernando Vera leaves, :robot: screenshot 📷](https://web.archive.org/web/20170619201226/https://i.imgur.com/AfM6u6c.jpg)  
  * [TOOOL](http://toool.us/meetings.html) - the largest sport lockpicking group, has meetings in NYC!
  * [Southord](https://www.southord.com/) has good sets!
  * [LockWiki](http://lockwiki.com/) is a wiki all about compromising the security of lockd, safes, and keys.
  * This is part of "physical security," often abbreviated as [[PHYSEC|PhySec]].
* Elliot's exploit against Fernando Vera uses C language code and references [Andersson (AA) trees](https://en.wikipedia.org/wiki/AA_tree).
  ![Elliot uses some kind of HTTP attack vector to compromise Vera, :robot: screenshot 📷](https://web.archive.org/web/20200624052855if_/https://i.imgur.com/epkxKTo.png)
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
  * [IPv6 address(?)](https://github.com/AnarchoTechNYC/meta/wiki/IP-address) in the URL bar
  * ["Hacking Europe" book](https://www.springer.com/gp/book/9781447154921) on the bookshelf is an academic work about famous European hacker communities
* Onion site ("hidden service") used as an IRC server  
  ![Screenshot of a Chinese IRC channel, :robot: screenshot 📷](https://web.archive.org/web/20170317230419/https://i.imgur.com/V08jbFH.jpg)
  * The now-defunct [TorMessenger](https://blog.torproject.org/blog/tor-messenger-beta-chat-over-tor-easily) was a chat app that enabled access to such servers easily, if you know the `.onion` address. (Nowawadays you should choose and configure an existing IRC and Tor client yourself. [Instructions for Freenode on Tor](https://freenode.net/news/tor-online). )
  * This technique was [used by Anonymous](https://nakedsecurity.sophos.com/2016/04/22/anonymous-launches-onionirc-a-school-for-hacktivists-on-the-dark-web/) for some of their chat services
* "And it's not enough to just focus your attention on the logs. We should also monitor social media traffic, as well as IRC, Pastebin, and set up scripts to keep going, 24/7" - places where data dumps often first appear
  * System logging, [NetFlow](https://en.wikipedia.org/wiki/NetFlow) logging, etc….
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
  * [PhishTank](https://www.phishtank.com/) is a public clearinghouse cataloguing known or suspected phishing sites.
  * [Phish5](https://phish5.com/) is a commercial service that lets you easily create phishing campaigns to target users of your own domains for educational purposes.
  * [BeEF](http://beefproject.com/), the free software Browser Exploitation Framework, can be used to launch one-off phishing attacks against "hooked" Web browsers.
  * [KingPhisher](https://github.com/securestate/king-phisher) is free software that operates entire phishing campaigns and offers its own phishing toolkit. 
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
    * [FlexiSPY](https://www.flexispy.com/) (try a [demo](https://portal.flexispy.com/demo.html))
    * [Highster Mobile](http://highstermobile.com/)
    * [Spyera](https://spyera.com/)
    * [HelloSpy](http://hellospy.com/)
    * [Retina-X](http://www.retinax.com/)
  * Real life examples:
    * ['I See You': A Domestic Violence Survivor Talks About Being Surveilled By Her Ex](https://motherboard.vice.com/en_us/article/i-see-you-a-domestic-violence-survivor-talks-about-being-surveilled-by-her-ex)
    * [Inside the 'Stalkerware' Surveillance Market, Where Ordinary People Tap Each Other's Phones](https://motherboard.vice.com/en_us/article/inside-stalkerware-surveillance-market-flexispy-retina-x)
    * [CitizenLab report on iOS "Trident" vulnerabilities installing a RAT against human rights defenders](https://citizenlab.org/2016/08/million-dollar-dissident-iphone-zero-day-nso-group-uae/)
* Identity theft, financial blackmail, "[carding](https://en.wikipedia.org/wiki/Carding_(fraud))" (credit card market), [doxing](https://en.wikipedia.org/wiki/Doxing)  
  ![Angela's information is caught up in the dox on Ollie, :robot: screenshot 📷](https://web.archive.org/web/20170318001822/https://i.imgur.com/yUuLVN7.jpg)
  * Apply a [credit freeze](https://en.wikipedia.org/wiki/Credit_freeze) to your personal credit line
  * [Krebs On Security: Peek Inside a Professional Carding Shop](https://krebsonsecurity.com/2014/06/peek-inside-a-professional-carding-shop/)
  * [IdentityTheft.gov](https://www.identitytheft.gov/) - US government recommendations/resources to "recover from identity theft"
  * Read [Crash // Override's "Prevent Doxing" guide](http://www.crashoverridenetwork.com/preventingdoxing.html)
* Incident response (IR), and digital forensic examination reports  
  ![Gideon examines Elliot's forensic examiner report on the encrypted .dat file, :robot: screenshot 📷](https://web.archive.org/web/20170318002151/https://i.imgur.com/nSn0Y1o.jpg)  
  ![Close up on the DFIR report, 1, :robot: screenshot 📷](https://web.archive.org/web/20200704054322if_/https://i.imgur.com/yZrG8yo.png)  
  ![Close up on the DFIR report, 2, :robot: screenshot 📷](https://web.archive.org/web/20200704054325if_/https://i.imgur.com/7wkpDNc.png)  
  ![Close up on the DFIR report, 3, :robot: screenshot 📷](https://web.archive.org/web/20200704054327if_/https://i.imgur.com/O19VwTZ.png)
  * [MD5 hashing algorithm](https://en.wikipedia.org/wiki/MD5)
    * hashes (also called digests) are [used in digital forensics extensively](http://forensicswiki.org/wiki/Hashing)
  * [ForensicsWiki](http://forensicswiki.org/wiki/Main_Page) is a Wikipedia-like site for digital forensics tools and standards
  * [SANS Digital Forensics Blog](https://digital-forensics.sans.org/blog/), a regularly-updating industry blog
* Gideon Goddard's phone shows location services are disabled, a better-than-average privacy practice:
  ![Closeup of Gideon's Android smartphone, :robot: screenshot 📷](https://web.archive.org/web/20200704054618if_/https://i.imgur.com/UyIHJCO.png)

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
  * Internet recon sites like [Shodan](https://shodan.io/), [Censys](https://censys.io/) can find any Internet-connected device
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
* "Hollywood hacker bullshit," Romero and Mobley are watching ["Hackers" (1995)](https://www.themoviedb.org/movie/10428-hackers)  
  ![Romero and Mobley kill time watching "Hackers," a movie from 1995 movie, :robot: screenshot 📷](https://web.archive.org/web/20170328213658/https://i.imgur.com/KCdXefY.jpg)
* "[Rabbit virus](https://en.wikipedia.org/wiki/Rabbit_virus)," also called a [fork bomb](https://en.wikipedia.org/wiki/Fork_bomb)
* Trenton prepares the HVAC exploit for Steel Mountain  
  ![Trenton's exploit development setup, :robot: screenshot 📷](https://web.archive.org/web/20170329015222/https://i.imgur.com/en2XoVE.jpg)
  ![Trenton uses a graphical file transfer program to send her exploit to her FTP server, :robot: screenshot 📷](http://web.archive.org/web/https://i.imgur.com/itKd65b.jpg)
  * Trenton's exploit is written in the [Python](https://www.python.org/) programming language, a language popular with attackers (see the book, "[Violent Python: A Cookbook for Hackers, Forensic Analysts, Penetration Testers, and Security Engineers](https://repo.zenk-security.com/Programmation/Violent%20Python%20a%20Cookbook%20for%20Hackers-Forensic%20Analysts-Penetration%20testers%20and%20Security%20Engineers.pdf)")
  * [`tar`](https://en.wikipedia.org/wiki/Tar_%28computing%29), a command to create a single file ("archive") out of many
* "Error 404 Not Found", a well-known HTTP status code
  * See [IANA's HTTP Status Code Registry](https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml)
* Getting rid of mobile phones to avoid being tracked by Law Enforcement Officers (LEOs) through [cell tower dumps](https://www.aclu.org/blog/cell-tower-dumps-another-surveillance-technique-another-set-unanswered-questions) or by an [IMSI-catcher](https://en.wikipedia.org/wiki/IMSI-catcher) (a "Stingray"), or other hackers via [VoLTE vulnerabilities](https://www.bleepingcomputer.com/news/security/hackers-can-spoof-phone-numbers-track-users-via-4g-volte-mobile-technology/)
  * [Atlas of Surveillance](https://atlasofsurveillance.org/)
  * [Wired: Cops and Feds Routinely ‘Dump’ Cell Towers to Track Everyone Nearby](https://www.wired.com/2013/12/massive-domestic-monitorning/)
  * [ACLU: Stingray Tracking Devices, Who's Got Them?](https://www.aclu.org/map/stingray-tracking-devices-whos-got-them)
  * [PrivacySOS.org: How to Defeat FBI or Police Stingray Surveillance](https://privacysos.org/blog/how-to-defeat-fbi-or-police-stingray-surveillance/)
* Employee access cards, usually [RFID](https://en.wikipedia.org/wiki/Radio-frequency_identification) technology activated by proximity  
  ![Angela uses an employee access card to enter AllSafe Cybersecurity offices, :robot: screenshot 📷](https://i.imgur.com/63d95Ip.png)
  * Read: [Intro to SDR and RF Signal Analysis](https://www.elttam.com.au/blog/intro-sdr-and-rf-analysis/)
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
  * "xCARD PROGRAMMER - v1.05" is not real, but the [GeZhi HID Cloner V3.0](https://web.archive.org/web/20170106000622/http://www.xfpga.com/pic/big/34_1.jpg) made by [GeZhi Electronic Co](http://www.xfpga.com/) is real! ([HID](https://en.wikipedia.org/wiki/HID_Global) is a contactless access key card brand name.)
  * Article: [Understanding the confusing world of RFID tags and readers in access control](http://www.nedapidentification.com/news/insights/understanding-the-confusing-world-of-rfid-tags-and-readers-in-access-control.html)
  * Same or similar tech is used instead of magnetic strips on credit/debit cards, see [How to Disable Contactless Payment on Your Debit Card](http://www.instructables.com/id/How-to-Disable-Contactless-Payment-on-Your-Debit-C/?ALLSTEPS)
  * Do-It-Yourself [electronic projects](http://www.eng.tau.ac.il/~yash/kw-usenix06/index.html) to make [your own low-cost RFID cloner](https://hackaday.com/2011/09/30/passive-rfid-tag-cloning/), more at [ProxClone.com](http://www.proxclone.com/)
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
  * [Maltego](https://paterva.com/web7/docs/documentation.php), a proprietary graphical tool for digital reconnaissance
  * [`recon-ng`](https://bitbucket.org/LaNMaSteR53/recon-ng), a free software command-line tool for digital reconnaissance
* Covert ear-piece, usually connects using [Bluetooth](https://en.wikipedia.org/wiki/Bluetooth) to a nearby smartphone
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
  * News article: [A rogue Raspberry Pi helped hackers access NASA JPL systems](https://www.engadget.com/2019/06/20/nasa-jpl-cybersecurity-weaknesses/) ([news source](https://threatpost.com/feds-hackers-mission-control-data-nasa-jpl/145842/))
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
  * The `-l` option specifies a *l*ogin (user) name; Darlene is using the `root` user (sometimes also called the "[superuser](https://en.wikipedia.org/wiki/Superuser)").
  * No passwords were being asked for, so Darlene has [configured SSH for key-based authentication](http://www.systutorials.com/1500/enabling-password-less-ssh-login/). [GitHub has a good guide for setting up SSH with key-based (aka. "password-less") logins](https://help.github.com/articles/connecting-to-github-with-ssh/).
  * On Windows, you may need to install [PuTTY](http://www.putty.org/). On macOS/*nix systems, SSH is usually pre-installed.
  * Complete reference guidebook: [SSH, The Secure Shell: The definitive guide, 2nd Edition](https://web.archive.org/web/20170122005724/https://courseweb.pitt.edu/bbcswebdav/institution/Pitt%20Online/MLIS_Pitt_Online/LIS%202600/Intro%20Module/SSH_Second_Edition.pdf)
  * [Secure Secure Shell](https://stribika.github.io/2015/01/04/secure-secure-shell.html), a guide for the "paranoid" SSH user.

# Week 6 (S01E06)

* Standard industrial control systems *do* operate some prison's doors:  
  ![Elliot looks up technical specifications of prison system electronic device controllers, :robot: screenshot 📷](https://web.archive.org/web/20170411223837/https://i.imgur.com/M7EoAJa.jpg)
  *  White paper "[SCADA & PLC Vulnerabilities In Correctional Facilities](https://web.archive.org/web/20160409040119/http://www.wired.com/images_blogs/threatlevel/2011/07/PLC-White-Paper_Newman_Rad_Strauchs_July22_2011.pdf)" and [associated conference presentation by the authors](https://www.youtube.com/watch?v=1MTLuLBiKcc).
* Finding nearby [Bluetooth](https://en.wikipedia.org/wiki/Bluetooth) devices  
  ![Elliot scans nearby Bluetooth devices to scan Isaac's iPhone, :robot: screenshot 📷](https://web.archive.org/web/20161213025246/https://hackertarget.com/mrrobot/btscanner-phone.png)
  * [`btscanner`](http://www.pentest.co.uk/downloads.html) ([manual page](http://manpages.ubuntu.com/manpages/utopic/man1/btscanner.1.html)), a tool to extract as much information as possible from a Bluetooth device without  pairing with it
  * `btscanner` is included in many [penetration testing distros](https://github.com/enaqx/awesome-pentest#penetration-testing-distributions), including Elliot's choice, [Kali Linux](https://www.kali.org/)
  * [Blog post with links to various Bluetooth tools](https://web.archive.org/web/20161024111000/http://www.kalilinuxdojo.com/2015/10/hack-bluetooth-and-other-wireless-tools.html)
* AllSafe uses Windows 8(?) for its office desktop computers
* [Multifunction printers](https://en.wikipedia.org/wiki/Multifunction_printer) can do more than you might think! Privacy issues and network vulnerabilities:
  ![Angela prints her research documents with one of AllSafe's printers, :robot: screenshot 📷](https://web.archive.org/web/20170411220804/https://i.imgur.com/fcWrqHP.jpg)
  * "Tracking dots" (aka [Printer steganography](https://en.wikipedia.org/wiki/Printer_steganography)) are used to link a printed document with the device that printed it:
    * [Is Your Printer Spying On You?](https://www.eff.org/issues/printers)
    * [Incomplete list of printers which do or do not display tracking dots](https://www.eff.org/pages/list-printers-which-do-or-do-not-display-tracking-dots)
    * [Seeing Yellow](http://seeingyellow.com/) - How to find printer dots ([more instructions](http://www.instructables.com/id/Yellow-Dots-of-Mystery-Is-Your-Printer-Spying-on-/)), and how to complain about it.
    * [Tracking Dot Decoding Guide](https://w2.eff.org/Privacy/printers/docucolor/)
    * Article, [Government Uses Color Laser Printer Technology to Track Documents](http://www.pcworld.com/article/118664/article.html)
    * Real-life example: [How the NSA tracked down and arrested the alleged Russian hacking story leaker, Reality Leigh Winner](http://blog.erratasec.com/2017/06/how-intercept-outed-reality-winner.html)
  * Printers are often a vulnerable device on corporate networks, read [Exploiting Corporate Printers](http://resources.infosecinstitute.com/exploiting-corporate-printers/) and [Printer Exploitation in Corporate Environments](https://www.hackingloops.com/printer-exploitation-in-corporate-environments/)
    * Real-life example, "[Rooting a Printer: From Security Bulletin to Remote Code Execution](https://www.tenable.com/blog/rooting-a-printer-from-security-bulletin-to-remote-code-execution)" by Tenable Security.
    * [Hacking-Printers.net](http://hacking-printers.net/) wiki is a great resource.
    * [PRET, the Printer Exploitation Toolkit](https://github.com/RUB-NDS/PRET#readme) is penetration testing framework targeting networked printers.
* Angela uses an iPhone :)
  ![Angela opens her iPhone's home screen to check a missed call, :robot: screenshot 📷](https://web.archive.org/web/20170411221239/https://i.imgur.com/RNWv775.jpg)
  * Check out [Apple's iOS Security Guide](https://www.apple.com/business/docs/iOS_Security_Guide.pdf)
* Sprinkling USB thumbdrives in the parking lot  
  ![Darlene drops USB thumbdrives in the police station's parking lot, :robot: screenshot 📷](https://web.archive.org/web/20170411221611/https://i.imgur.com/NNZ3Lkd.jpg)
  * Read, "[Almost Half of Dropped USB Sticks Will Get Plugged In](https://nakedsecurity.sophos.com/2016/04/08/almost-half-of-dropped-usb-sticks-will-get-plugged-in/)"
  * [Yet Another "People Plug in Strange USB Sticks" Story](https://www.schneier.com/blog/archives/2011/06/yet_another_peo.html)
  * Real-life example: [Russian hackers infiltrated NATO using cheap retail thumbdrives](https://web.archive.org/web/20170311014501/https:/twitter.com/Mathew__Clayton/status/837605847257792512/photo/1)
* Plugging in USB devices can unleash malware  
  ![A cop plugs in a stray USB drive to his work computer claiming to be an "eTunes" gift card, :robot: screenshot 📷](https://web.archive.org/web/20170411222314/https://i.imgur.com/TB9V9ao.jpg)  
  ![The malware is disguised as an "eTunes" survey, :robot: screenshot 📷](https://web.archive.org/web/20170411222711/https://i.imgur.com/HaPBzpy.jpg)
  ![The exploit is triggered using a basic phishing attack that gets an end-user to click and activate it, :robot: screenshot 📷](https://web.archive.org/web/20170411222808/https://i.imgur.com/E6KJRPV.jpg)  
  ![The Avast! Anti-Virus suite detected and blocked the malware and shows a pop-up warning, :robot: screenshot 📷](https://web.archive.org/web/20170411222859/https://i.imgur.com/PNY07TR.jpg)  
  ![Elliot's computer is disconnected from the cop's computer when Avast! blocked the malware, :robot: screenshot 📷](https://web.archive.org/web/20170411223017/https://i.imgur.com/usjYhUO.png)
  * Article, [BadUSB](http://mashable.com/2014/10/03/bad-usb/)
  * Not shown in the show, but similarly, check out [Poisontap](https://samy.pl/poisontap/)
  * [Avast!](https://www.avast.com/), a low-end anti-virus and anti-malware software suite:
    * [Security in a Box's guide to Avast on Windows](https://securityinabox.org/en/guide/avast/windows/)
  * Read [about "bind shells" and "reverse shells,"](https://irichmore.wordpress.com/2015/06/04/bind-shell-vs-reverse-shell/) the basics of getting remote control over a computer. [`nc` is often used](http://www.hackingtutorials.org/networking/hacking-netcat-part-2-bind-reverse-shells/), although Elliot is using `ssh` in this screenshot.
  * Relatedly, police departments are not immune:
    * [Police Department Loses Years Worth of Evidence in Ransomware Incident](https://www.bleepingcomputer.com/news/security/police-department-loses-years-worth-of-evidence-in-ransomware-incident/)
    * [PoliceOne hacked – Hacker is selling thousands police officials’ accounts](http://securityaffairs.co/wordpress/55967/data-breach/policeone-data-breach.html)
    * [A Notorious Hacker Is Trying to Start a ‘Hack Back’ Political Movement](https://motherboard.vice.com/en_us/article/notorious-hacker-phineas-fishers-is-trying-to-start-a-hack-back-political-movement)
* "You just pulled code from Rapid9 or some shit? When did you become a script kiddie?"
  * Rapid9 is not real, but is a reference to the famous [Rapid7](https://www.rapid7.com/).
  * A "[script kiddie](https://www.urbandictionary.com/define.php?term=script%20kiddie)" is hacker lingo for an unskilled techie, like a "noob" or "newbie."
* "Malware detection must have caught it," Elliot says.
  * There are ways to make malware evade anti-virus/anti-malware detection. See, for instance, [Veil-Framework](https://www.veil-framework.com/).
  * Hackers often test exploits against [VirusTotal.com](https://www.virustotal.com/) to see if evasion is successful.
* An ICS is an [Industrial Control System](https://en.wikipedia.org/wiki/Industrial_control_system): "I can run circles around an ICS given the right white papers and some time," Darlene says.
  * She might also mean an "IDS" or "IPS," an [Intrusion Detection System](https://en.wikipedia.org/wiki/Intrusion_detection_system) or [Intrusion Prevention System](https://en.wikipedia.org/wiki/Intrusion_detection_system#Intrusion_prevention), respectively.
* Terry Colby is wearing an [ankle monitor](https://en.wikipedia.org/wiki/Ankle_monitor) as part of [electronic home monitoring ("house arrest")](http://www.attorneys.com/parole-and-probation/electronic-home-monitoring) - which make & model?  
  ![Closeup of the ankle tether Terry Colby wears under house arrest, :robot: screenshot 📷](https://web.archive.org/web/20170411225808/https://i.imgur.com/rtKgdUh.jpg)
  * Service provider, [Guardian/Shield Ankle Monitoring Service](http://www.georgiahousearrest.com/)
  * Ankle monitors are overwhelmingly used to control the movement of oppressed groups. Articles:
    * [No Alternative: Ankle Monitors Expand the Reach of Immigration Detention](https://nacla.org/news/2015/01/06/no-alternative-ankle-monitors-expand-reach-immigration-detention)
    * [Chain Gang 2.0: If You Can’t Afford This GPS Ankle Bracelet, You Get Thrown In Jail](http://www.ibtimes.com/chain-gang-20-if-you-cant-afford-gps-ankle-bracelet-you-get-thrown-jail-2065283)
    * [Getting Immigrants Out of Detention Is Very Profitable (for Ankle Monitor Manufacturers)](http://www.motherjones.com/politics/2016/09/immigration-detainees-bond-ankle-monitors-libre/)
* "Shit. WPA2, borderline unhackable. Getting that [handshake](http://www.kalitutorials.net/2014/06/hack-wpa-2-psk-capturing-handshake.html), it could take days."
  ![Elliot's Android phone runs a version of Wifite to find nearby networks, :robot: screenshot 📷](https://web.archive.org/web/20170411230748/https://i.imgur.com/PkuQrDZ.jpg)
  * Wikipedia article: [Cracking of wireless networks](https://en.wikipedia.org/wiki/Cracking_of_wireless_networks)
  * Elliot is using a [Pwn Phone](https://github.com/thehackingsage/pwnphone) to run [`wifite`](http://www.kalitutorials.net/2014/04/wifite-hacking-wifi-easy-way-kali-linux.html), an automated Wi-Fi cracking tool that uses [`aircrack-ng`](https://en.wikipedia.org/wiki/Aircrack-ng), [`reaver`](https://lifehacker.com/5873407/how-to-crack-a-wi-fi-networks-wpa-password-with-reaver), and other tools under the hood
* "Discoverable" Bluetooth devices can reveal device names  
  ![Elliot looks for nearby Bluetooth devices that are discoverable, :robot: screenshot 📷](https://web.archive.org/web/20170411231559/https://i.imgur.com/6Gywvp5.jpg)
* Cop cars use "dedicated 4G," which is a cell (mobile phone) technology, and Bluetooth-enabled endpoints in the cab
  ![Closeup of a cop car's laptop uplink, :robot: screenshot 📷](https://web.archive.org/web/20170411233719/https://i.imgur.com/7edDLHr.jpg)
  * PoliceOne.com, a popular forum for law enforcement officers: [Police Mobile Computers](https://web.archive.org/web/20170130072148/https://www.policeone.com/police-products/police-technology/mobile-computers/)
  * PoliceMag.com: [A Guide to Understanding Law Enforcement Field Technology](https://web.archive.org/web/20161009110144/http://www.policemag.com/channel/technology/articles/2016/10/a-guide-to-understanding-law-enforcement-field-technology.aspx)
  * News article: [Tech in police cars cause cops to crash their vehicles due to distracted driving](http://www.kshb.com/news/local-news/investigations/surge-of-technology-inside-police-vehicles-can-lead-to-officer-distraction-causing-wrecks)
* Bluetooth hacking, with related terms "[Bluejacking](http://www.bluejackingtools.com/what-is-bluejacking/)," "[Bluebugging](http://www.bluejackingtools.com/bluebugging/)," and "[Bluesnarfing](http://www.bluejackingtools.com/bluesnarfing/)"  
  ![Elliot attaches an extra Bluetooth device in dongle form to his laptop, :robot: screenshot 📷](https://web.archive.org/web/20170411234200/https://i.imgur.com/5w5tJi5.jpg)
  ![Three terminals show various Bluetooth userspace utilities in Linux, :robot: screenshot 📷](https://web.archive.org/web/20170411233555/https://i.imgur.com/lnHNTjN.jpg)
  * [`bluesniff`](http://bluesniff.shmoo.com/), a Bluetooth wardriving utility for Linux useful for finding hidden Bluetooth-capable devices
  * [`hcitool`](http://linuxcommand.org/man_pages/hcitool1.html), command-line utility to communicate with Bluetooth device and create device-to-device connections
  * [`hciconfig`](http://linuxcommand.org/man_pages/hciconfig8.html), command-line utility to configure a system's Bluetooth devices
* Elliot uses a Windows [virtual machine](https://en.wikipedia.org/wiki/Virtual_machine) to attach to cop car's laptop's Bluetooth keyboard  
  ![Elliot hijacks the cop car's Bluetooth keyboard, :robot: screenshot 📷](https://web.archive.org/web/20170411233455/https://i.imgur.com/nFkpvP6.jpg)
* [`ftp`](https://en.wikipedia.org/wiki/File_Transfer_Protocol)  
  ![Elliot downloads his exploit to the cop's laptop through `ftp`, :robot: screenshot 📷](https://web.archive.org/web/20170411234307/https://i.imgur.com/XjUyEEy.jpg)
* [Metasploit](https://en.wikipedia.org/wiki/Metasploit_Project) Meterpreter, a famous exploitation toolkit  
  ![Running an exploit with Meterpreter, :robot: screenshot 📷](https://web.archive.org/web/20161213025246/https://hackertarget.com/mrrobot/meterpreter.png)  
  ![Closeup of Meterpreter output, :robot: screenshot 📷](https://web.archive.org/web/20170411233135/https://i.imgur.com/J1slcx3.jpg)
  ![The cop notices his computer acting like it's "on the fritz," :robot: screenshot 📷](https://web.archive.org/web/20170411234436/https://i.imgur.com/TB6zbkW.jpg)
  * [About the Metasploit Meterpreter](https://www.offensive-security.com/metasploit-unleashed/about-meterpreter/)
  * [How does process migration work in Meterpreter?](https://security.stackexchange.com/questions/90578/how-does-process-migration-work-in-meterpreter)
  * [MeterpreterClient - Wikibooks](https://en.wikibooks.org/wiki/Metasploit/MeterpreterClient#migrate)

# Week 7 (S01E07)

* ["View source" functionality in Web browsers](http://www.computerhope.com/issues/ch000746.htm) &larr; "I got into web design by ripping off sites I liked."
  !["Vintage" computer equipment browsing the old 2600 website, :robot: screenshot 📷](https://web.archive.org/web/20170503023411/https://i.imgur.com/hCbxfmP.jpg)
  ![Netscape Communicator's "Page Source" menu option showed the source code for any website, :robot: screenshot 📷](http://web.archive.org/save/https://i.imgur.com/NvPG9It.jpg)  
  ![Elliot copied the source code into a text editor and edits the page title, :robot: screenshot 📷](https://web.archive.org/web/20170503023415/https://i.imgur.com/pjj5ITP.jpg)
* [Netscape Communicator](https://en.wikipedia.org/wiki/Netscape_Communicator), one of the earliest commercial Web browsers first released in the late 1990's
  * Check out the [evolt.org Browser Archive](http://browsers.evolt.org/), copies of every version of every Web browser ever released
* [Windows 95](https://en.wikipedia.org/wiki/Windows_95) (or Windows 98?)
* [2600.com](https://www.2600.com/), a famous, long-running hacker periodical ([Wikipedia article](https://en.wikipedia.org/wiki/2600:_The_Hacker_Quarterly))
  * View [the 1999 version of the 2600.com website](https://web.archive.org/web/19990116232336/http://www.2600.com/mindex.html) using [the Internet Archive's Wayback Machine](https://archive.org/web/).
  * In a similar vein, check out [Phrack](http://phrack.org/) and [its Wikipedia article](https://en.wikipedia.org/wiki/Phrack).
* [Atari 2600](https://en.wikipedia.org/wiki/Atari_2600), a 1980's-era video game console
* [Deepsound](http://jpinsoft.net/deepsound/), a Windows audio CD/DVD [steganographic](https://en.wikipedia.org/wiki/Steganography) utility (again)
  ![Elliot burns all the data he has on Shayla Nico to a CD, :robot: screenshot 📷](http://web.archive.org/save/https://i.imgur.com/JSZZbjM.jpg)
* Pets are "microchipped," meaning small electronic chips implanted ([microchip implants](https://en.wikipedia.org/wiki/Microchip_implant_%28animal%29)) under their skin  
  ![The vet reads out data from a microchip implanted in Flipper's skin, :robot: screenshot 📷](https://web.archive.org/web/20170503031433/https://i.imgur.com/CE1kFEH.jpg)
* "You got root on my box, and found the IP, then you joined their channel with my handle."  
  ![Cisco meets Darlene at a Chess table in a park, angered that she hacked him, :robot: screenshot 📷](https://web.archive.org/web/20170503034358/https://i.imgur.com/wnLtVw2.jpg)
  * "Getting root" means to "acquire access to the `root` user on a UNIX-like operating system," since that user is by definition granted all [privileges/rights to a system](https://msdn.microsoft.com/en-us/library/windows/desktop/aa379306(v=vs.85).aspx). (In a Windows context, this is called "getting System" and [Meterpreter has a command by that name, `getsystem`](https://www.offensive-security.com/metasploit-unleashed/privilege-escalation/), because [the most privileged user account on a Windows computer is the `LocalSystem` account](https://msdn.microsoft.com/en-us/library/windows/desktop/ms684190(v=vs.85).aspx).)
    * It's less common to get root (or System) privileges directly; often you must first find some other vulnerability to exploit, then "escalate your privileges." This is called *privilege escalation* ("privesc" for short):
      * [Windows Privilege Escalation Methods for Pentesters](https://pentest.blog/windows-privilege-escalation-methods-for-pentesters/)
      * [Windows Privilege Escalation, Part 1: Local Administrator Account](https://blog.netspi.com/windows-privilege-escalation-part-1-local-administrator-privileges/) and [Part 2: Domain Admin Privileges](https://blog.netspi.com/windows-privilege-escalation-part-2-domain-admin-privileges/)
      * [FuzzySecurity Tutorials: Windows Privilege Escalation Fundamentals](http://www.fuzzysecurity.com/tutorials/16.html)
      * [Basic Linux Privilege Escalation](http://blog.g0tmi1k.com:80/2011/08/basic-linux-privilege-escalation/)
      * Standalone tools to check for privilege escalation opportunities: [`windows-privesc-check`](http://pentestmonkey.net/tools/audit/windows-privesc-check), [`unix-privesc-check`](http://pentestmonkey.net/tools/audit/unix-privesc-check)
  * "Box" is just a slang term for "computer."
  * "The IP" refers to the [Internet Protocol address](https://simple.wikipedia.org/wiki/IP_address), literally the equivalent of a computer's "home/mailing address" that anyone who wants to send messages to the computer usually needs to know. Here, Cisco refers not to his box's IP address, but the IP address of the Dark Army's servers.
  * "Their channel" is a reference to the IRC chat room that the Dark Army uses to communicate, seen in an earlier episode. In IRC, chat rooms are called "channels," and hacker slang usually uses the two terms ("chat room" or "channel") somewhat interchangeably.
  * "My [handle](https://en.wikipedia.org/wiki/Handle_%28computing%29)" means "the username (or screen name) I use." Here, Cisco just means that after Darlene hacked his computer, she impersonated him, using his persona to communicate with the Dark Army directly.

# Week 8 (S01E08)

* Guessing the combination lock of the vault by looking around.
  * Look to "characteristics of bad passwords."
* Deepsound (again!)
* "AirDream Advanced Metering;" research by reading PDFs/tech manuals/white papers (this is the part that takes the most time…)
* Dark Army is following Darlene
* (Evading) physical surveillance - https://protectioncircle.org/2016/06/14/surveillance-evasion/
* "Using the backdoor we planted; I installed the patch four weeks and I've been monitoring it daily." […]
* "[Phone home](https://en.wikipedia.org/wiki/Phoning_home)"
* "Reroute (AirDream's) traffic"
* Chain of custody with the dat file - see [handling instructions for digital evidence](http://forensicswiki.org/wiki/Digital_evidence#Handling)
* "[Airgapped](https://en.wikipedia.org/wiki/Air_gap_%28networking%29) your network"
* "Implemented a [honeypot](https://en.wikipedia.org/wiki/Honeypot_(computing))"
  * Vendors, such as [Canary](https://canary.tools/)
* Are Tyrell's GNU/Linux terminal skillz legit? (Pretty much.)
  * `find`
  * `/opt/2/task/2/fdinfo`
    * <-- `f`ile `d`escriptor `info`rmation (look up "file descriptors")
    * <-- Read about the GNU/Linux [Filesystem Hierarchy Standard](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard) for what is in the `/opt` directory (see also LSB, the [Linux Standard Base](https://en.wikipedia.org/wiki/Linux_Standard_Base), a related standard)
  * `ls -l`
* "The ASA Firewall", meaning the [Cisco ASA series device](https://www.cisco.com/c/en/us/products/security/asa-firepower-services/index.html), is a high-end Cisco product that provides network security solition
* Angela tells Elliot about a doxxing threat
* [Faraday cage](https://en.wikipedia.org/wiki/Faraday_cage) - radio frequency blocking
  * https://thelede.blogs.nytimes.com/2013/06/25/why-snowdens-visitors-put-their-phones-in-the-fridge/
  * https://gizmodo.com/193903/faraday-cage-passport-wallets-jams-rfid-chipped-travel-docs
* WTF is up with that shit about time paranoia?
  * Managing time (programming concept of [multiple threads](https://en.wikipedia.org/wiki/Multithreading_(computer_architecture)))
  * [Time-sharing](https://en.wikipedia.org/wiki/Time-sharing)
  * Timers, and "time-outs", like:
    * [Watchdog timers](https://en.wikipedia.org/wiki/Watchdog_timer)
* "Security token" (Gideon's phone)
* Hacking a Smart TV
  * https://arstechnica.com/security/2017/03/smart-tv-hack-embeds-attack-code-into-broadcast-signal-no-access-required/
* Two-factor authentication schemes, such as: time-based one-time password ([TOTP](https://en.wikipedia.org/wiki/Time-based_One-time_Password_Algorithm))
  * Google Authenticator ([Wikipedia](https://en.wikipedia.org/wiki/Google_Authenticator))
  * [U2F](https://en.wikipedia.org/wiki/Universal_2nd_Factor), see also [YubiKeys](https://www.yubico.com/about/background/fido/)
* Enterprise ticketing systems "osTicket"
  * Free software "[Request Tracker](https://en.wikipedia.org/wiki/Request_Tracker)"
  * Wikipedia maintains [a huge list](https://en.wikipedia.org/wiki/Comparison_of_issue-tracking_systems), of course
* Elliot "hacks" himself -> people search sites, FamilyTreeNow, getting real estate deeds and other legal documents, basically "self-doxxing"
  * [Erasing oneself from the Internet](https://gizmodo.com/how-to-erase-yourself-from-the-internet-1456270634)
* [ProtonMail](https://protonmail.com/)  
  ![Screenshot of ProtonMail's Account Access Log interface](https://web.archive.org/web/20200808041255if_/https://i.imgur.com/2ILUYmS.png)
* Running Windows 8.1 in a virtual machine; VMs can be "suspended"/paused, then resumed later  
  ![Screenshot of Elliot's Windows 8.1 virtual machine resuming](https://web.archive.org/web/20200808042004/https://i.imgur.com/7p6PBmf.png)
* DeepSound, but reading instead of writing data this time  
  ![First screenshot of DeepSound](https://web.archive.org/web/20200808042229if_/https://i.imgur.com/dfYVJ91.png)  
  ![Second screenshot of DeepSound](https://web.archive.org/web/20200808042154/https://i.imgur.com/NKbawSZ.png)
* Shared folders on a VM (`/home/VMShare`) http://virtuatopia.com/index.php/VirtualBox_Shared_Folders
  * Used extensively for development as part of [Vagrant](https://www.vagrantup.com/)
* `gnome-open` is GNOME's graphical shell "open this file" command.  
  ![Screenshot of Elliot's terminal running `gnome-open`](https://web.archive.org/web/20200808041856/https://i.imgur.com/J2Rz6zq.png)

# Week 9 (S01E09)

* "Vintage" technology!
    ![Wide shot of the Mr. Robot showroom floor, :robot: screenshot 📷](https://i.imgur.com/6VJaslU.jpg)
    * [Super Nintendo Entertainment System](https://en.wikipedia.org/wiki/Super_Nintendo_Entertainment_System)
    ![Several Super Nintendo Entertainment Systems (SNES) and game cartridges on display at the Mr. Robot storefront, :robot: screenshot 📷](https://i.imgur.com/cRZdY10.jpg)
    * [NEC POWERMATE 433D](https://en.wikipedia.org/wiki/NEC#Products)
    ![An old NEC POWERMATE 433D desktop computer on display in the Mr. Robot storefront, :robot: screenshot 📷](https://i.imgur.com/UGAIPq7.jpg)
    * [Floppy disks](https://en.wikipedia.org/wiki/Floppy_disk)
    ![Mr. Robot repurposing floppy disks, :robot: screenshot 📷](https://i.imgur.com/O31caxo.jpg)
    * "Pentium 90," probably means an [Intel Pentium-branded PC](https://en.wikipedia.org/wiki/Pentium#Pentium), which earlier on ran at ~90Mhz
* Gideon: "They hacked us, you know that, it's been all over the news. Normally a company could get through this, but we're a *cybersecurity* company!" Similar situations in real life:
    * [Spy Tech Company 'Hacking Team' Gets Hacked](https://motherboard.vice.com/en_us/article/gvye3m/spy-tech-company-hacking-team-gets-hacked)
    * [Stratfor](https://en.wikipedia.org/wiki/Stratfor#2011_hacking_incident)
* Angela compulsively refreshes ["Google News"](https://news.google.com)
  ![Angela searches for news on Terry Colby, :robot: screenshot 📷](https://i.imgur.com/W3Nyy1H.jpg)
* Gideon uses [Thunderbird](https://www.mozilla.org/en-US/thunderbird/), apparently on Windows.
  ![Thunderbird on Windows, :robot: screenshot 📷](https://i.imgur.com/TdhWWL4.jpg)


# Week 10 (S01E10)

> 🚧 TK-TODO

# Week 11 (S02E01)

> 🚧 TK-TODO

# Week 12 (S02E02)

> 🚧 TK-TODO

# Week 13 (S02E03)

> 🚧 TK-TODO

# Week 14 (S02E04)

* "Pirating" (illegally downloading) movies using a [BitTorrent](https://simple.wikipedia.org/wiki/BitTorrent) client ([uTorrent](https://www.utorrent.com/), in this case, but a "better" Free Software client is [Deluge](https://deluge-torrent.org/), shown in [S03E04](#week-26-s03e04)):  
  ![Elliot uses uTorrent to download a (fictional) movie.](https://torrentfreak.com/images/robotutorr.jpg)
  * [TorrentFreak.com](https://torrentfreak.com/mr-robot-plugs-utorrent-and-pirate-release-groups-160729/) - Popular, long-running BitTorrent news outlet.

# Week 15 (S02E05)

* Femtocell
  * [DEF CON 21 presentation: Traffic Interception and Remote Mobile Phone Cloning with a Compromised CDMA Femtocell](https://www.youtube.com/watch?v=gfcq8clu1RI)

# Week 16 (S02E06)

* Signal is used to make an encrypted VoIP call.

# Week 17 (S02E07)

# Week 18 (S02E08)

# Week 19 (S02E09)

# Week 20 (S02E10)

* [Cantenna](https://en.wikipedia.org/wiki/Cantenna) (an antenna made out of a can) to boost radio signal (like Wi-Fi network) range.  
  ![](https://web.archive.org/web/20201024020557if_/https://i.imgur.com/J4RZ0oi.png)
* "For impersonating an NYPD officer. All cell carriers have a law enforcement hotline. Instead of hacking the carrier, if the situation's urgent enough, you can just ask them to track a blocked call for you."  
  ![](https://web.archive.org/web/20201024020154if_/https://i.imgur.com/TKXzGez.png)  
  ![](https://web.archive.org/web/20201024020234if_/https://i.imgur.com/4bo8NVA.png)  
  ![](https://web.archive.org/web/20201024020309if_/https://i.imgur.com/EaYd4zO.jpg)  
  ![](https://web.archive.org/web/20201024020344if_/https://i.imgur.com/UzRSXFr.jpg)  
  ![](https://web.archive.org/web/20201024020414if_/https://i.imgur.com/nTsQ7vA.png)  
  ![](https://web.archive.org/web/20201024020647if_/https://i.imgur.com/shIRCg6.png)  
  ![](https://web.archive.org/web/20201024020652if_/https://i.imgur.com/eiWoXb3.jpg)  
  ![](https://web.archive.org/web/20201024020733if_/https://i.imgur.com/HgOrkKE.png)
  * Many companies offer a red carpet for data collection to government law enforcement agencies, including:
    * [Facebook Records](https://facebook.com/records/) request; see [Netzpolitik's guide to the Facebook Records system compiled by and for activists](https://netzpolitik.org/wp-upload/2016/08/facebook-law-enforcement-portal-inofficial-manual.pdf)
    * [Google Law Enforcement Request System (LERS)](https://lers.google.com/)
* "Can you ping that phone for a current location?" Probably referring to a so-called "SMS ping," one type of invisible-to-the-user Short Message Service (cell phone txt message) message more broadly known as "[silent SMS](https://en.wikipedia.org/wiki/SMS#Silent_SMS)".  
  ![](https://web.archive.org/web/20201024020818if_/https://i.imgur.com/84Xahoi.jpg)  
  ![](https://web.archive.org/web/20201024020953if_/https://i.imgur.com/lgpNWz6.png)  
  ![](https://web.archive.org/web/20201024021036if_/https://i.imgur.com/1cWyM0i.jpg)  
  ![](https://web.archive.org/web/20201024021042if_/https://i.imgur.com/Z31j6EG.jpg)  
  ![](https://web.archive.org/web/20201024021048if_/https://i.imgur.com/uw7ABZt.jpg)  
    * Reverse address search features provided by Spokeo and other free/freemium [data brokers](https://privacyrights.org/data-brokers)

# Week 21 (S02E11)

# Week 22 (S02E12)

* 33 Thomas Street in Manhattan, the site of the NSA's "Project X," aka Titanpointe, an illegal domestic spying hub  
  ![](https://web.archive.org/web/20201107034624if_/https://i.imgur.com/X4k16O6.jpg)  
  * [Field of Vision: Project X](https://fieldofvision.org/project-x), a documentary short narrated by Rami Malek and Michelle Williams produced by Loura Poitras and Henrik Moltke

# Week 23 (S03E01)

See also [Mr. Robot Disassembled: eps3.0_power-saver-mode.h](https://medium.com/@ryankazanciyan/mr-robot-disassembled-eps3-0-power-saver-mode-h-1f8a3ba101d6).

* Elliot and Darlene visit "the only [hackerspace](https://en.wikipedia.org/wiki/Hackerspace) with a fiber connection"
* The number "1984" are painted on the wall, a common reference to George Orwell's 1949 novel of the same name warning about a dystopian future society where electronic surveillance controls people's lives and their thoughts; is this the name of the fictional hackerspace?  
  ![](https://web.archive.org/web/20201114021504if_/https://i.imgur.com/9mmRsCK.png)
  * [Hackerspaces.org](https://hackerspaces.org/) is a crowd-sourced directory of information about hackerspaces around the world.
* At the hackerspace, they find "a CTF tournament. [Capture The Flag](https://en.wikipedia.org/wiki/Capture_the_flag#Computer_security), it's like the hacker olympics. [Teams](https://github.com/AnarchoTechNYC/meta/wiki/CTF-team) around the world compete to solve challenges: reverse engineering, protocol exploitation, forensics."  
  ![]()
  * Most CTFs happen virtually, not in large party venues like those depicted on the show.
  * [CTFTime.org](https://ctftime.org/) is among the most prolific continually-updated directories of public CTF competitions.
  * [awesome-ctf](https://github.com/apsdehal/awesome-ctf) provides a listing of "awesome" tools and resources for CTF competitions and competitors.
* Darlene learns that "we're fucked. All the machines are taken. They're in the middle of a final round of the qualifier for a CTF." A few moments later, we learn that the CTF they're competing is the famous [DEF CON](https://defcon.org/) CTF:  
  * ![](https://web.archive.org/web/20201114022557if_/https://i.imgur.com/eivxsNr.png)
* "The backdoor had a hardcoded C2 domain pointing to a listener on Tyrell's machine. All I have to do is hack the [registrar](https://en.wikipedia.org/wiki/Domain_name_registrar) and change the [name server](https://en.wikipedia.org/wiki/Name_server) configs. Once I hijack the domain, I can shut down their access before the dark army notices."
  * C2 is an abbreviation for [Command and Control](https://en.wikipedia.org/wiki/Command_and_control), a generic term describing infrastructure used to send instructions and receive telemetry from targeted and/or compromised devices.
  ![](https://web.archive.org/web/20201114021214if_/https://i.imgur.com/d52DzaL.png)  
  ![](https://web.archive.org/web/20201114024515if_/https://i.imgur.com/gYaoDuB.png)
  * A "registrar" refers to an organization, usually a company, responsible for reserving domain names with a given top-level domain registry, which is also usually a company.
  * The registrar is responsible for asserting the correct IP addresses of the reserved domain's own name servers; if these are changed to attacker-controlled name servers, the attacker can direct any requests for the reserved Internet name to whatever IP addresses they like.
  * [`rwwwshell`](https://github.com/vanhauser-thc/THC-Archive/blob/master/Tools/rwwwshell-2.0.pl.gz), the classic "reverse World Wide Web shell,"  
    * [SANS Institute's Malware FAQ entry for rwww-shell](https://www.sans.org/security-resources/malwarefaq/rwww-shell)
  * [`shred`](https://explainshell.com/explain?cmd=shred+-f+-n+3+*) is a secure file deletion utility that helps prevent forensic recovery by overwriting the file data itself instead of simply unlinking the file from the filesystem like the simpler `rm` command does
* Using the New York State Police (NYSP) [National Crime Information Center (NCIC)](https://en.wikipedia.org/wiki/National_Crime_Information_Center) portal to lookup the [vehicle identification number (VIN)](https://en.wikipedia.org/wiki/Vehicle_identification_number) of the FBI car:
  ![](https://i.imgur.com/onCTaZH.png)
  * [OnStar Emergeny Incidents](https://www.public-safety.onstar.com/emergency-situations/)
* [Shodan.io](https://shodan.io/), "the search engine for Power Plants" and other connected devices
  ![](https://web.archive.org/web/20201114025728if_/https://i.imgur.com/Kf6u7PH.png)
  ![](https://web.archive.org/web/20201114025744if_/https://i.imgur.com/BtiMpQd.png)
  * Another similar tool is [CenSys.io](https://censys.io/).

# Week 24 (S03E02)

See also [Mr. Robot Disassembled: eps3.1_undo.gz](https://medium.com/@ryankazanciyan/mr-robot-disassembled-eps3-1-undo-gz-c9ae6080f574).

* Elliot uses [Rootkit Hunter (`rkhunter`)](http://rkhunter.sourceforge.net/) via [Kali Linux](https://www.kali.org/) to search for a rootkit on his own ([Linux Mint](https://linuxmint.com/)) system when he suspects he's been compromised:  
  ![Closeup of the rkhunter command line.](https://web.archive.org/web/20200329073616/https://i.imgur.com/grfMjYN.png)  
  ![Screenshot of rkhunter running on a Kali Linux system.](https://web.archive.org/web/20200329073855/https://i.imgur.com/dqCcxL7.png)

# Week 25 (S03E03)

See also [Mr. Robot Disassembled: eps3.2_legacy.so](https://medium.com/@ryankazanciyan/mr-robot-disassembled-eps3-2-legacy-so-a1e4bb153073).

# Week 26 (S03E04)

See also [Mr. Robot Disassembled: eps3.3_m3tadata.par2](https://medium.com/@ryankazanciyan/mr-robot-disassembled-eps3-3-m3tadata-par2-baa1e8486dd5).

* "The audio's useless. He's using a goddamn voice protector!" Also known as "speech protector," "noise generator," etc.
  ![](https://web.archive.org/web/20201205030141if_/https://i.imgur.com/8lS7Ui3.png)
  * Elliot looks like he's using [a Rabbler brand noise generator, model NG3000](https://www.kjbsecurity.com/products/detail/rabbler-noise-generator/857/)
* Darlene entertains herself by downloading a pirated movie from BitTorrent using [Deluge](https://deluge-torrent.org/)  
  ![](https://web.archive.org/web/20201205030639if_/https://i.imgur.com/R8tL0Ur.png)
* "We know you posted the F Society video — with a court order, we got the Vimeo connection logs for the account you used, which led us to your IP address and then your home address. That’s why you’re sitting here."
  * Article: [The Mr. Robot Hack Report: Don’t Fear the Rabbler - The Verge](https://www.theverge.com/2017/11/2/16596214/the-mr-robot-hack-report-s3e4-metadata)  
    > This is a really common way to find someone after they’ve done something illegal on the internet! Cops do it all the time[…].
  * Court orders aren't even required in some cases. Many sites provide a metaphorical red carpet specifically for law enforcement requests as discussed in [S02E10](#week-20-s02e10).

# Week 27 (S03E05)

See also [Mr. Robot Disassembled: 3.4_Runtime-Error.R00](https://medium.com/@ryankazanciyan/mr-robot-disassembled-3-4-runtime-error-r00-9319c70c30f2).

* Elliot logs in to his to work PC running Windows at E-Corp.  
  ![](https://web.archive.org/web/20201217022322if_/https://i.imgur.com/9oBwAOu.png)
  * Notice the absurdly long (24 character) password; since we hear him typing, this is probably a [pass*phrase* rather than a pass*word*](https://www.useapassphrase.com/).
  * This Windows PC is connected to a [Windows *domain*](https://en.wikipedia.org/wiki/Windows_domain) called `E Corp-USA`.
* "I need to check my monitoring server." Elliot uses Kibana and Logstash, and accesses the raw logs over SSH via PuTTY:
  ![Screenshot of a Kibana dashboard.](https://web.archive.org/web/20201217023139if_/https://i.imgur.com/lyo0ctN.png)  
  ![Screenshot of PuTTY.](https://web.archive.org/web/20201217023627if_/https://i.imgur.com/ftTjIy2.png)
  ![Screenshot of a terminal `cd`'ing to Logstash's directory.](https://web.archive.org/web/20201217023704if_/https://i.imgur.com/1c55x98.png)
  * [Kibana](https://www.elastic.co/kibana) is a popular and open-source data visualization tool.
  * [Logstash](https://www.elastic.co/logstash) is a popular and open-source data ingestion and processing utility.
  * [PuTTY](http://www.putty.org/) is a popular SSH client for Windows.
* Edie proves a difficult mark: "I've hardened my install, further than the standard configuration, including a restrictive host-based firewall ruleset and whitelisting to block unauthorized apps from running. I think I know your culprit, though. Fred over there uses GoToMyPC all the time." And then she locks her screen!
  ![Edie contests Elliot's social engineering premise.](https://web.archive.org/web/20201217024533if_/https://i.imgur.com/DdN23jA.png)  
  ![And then she locks her screen!](https://web.archive.org/web/20201217025746if_/https://i.imgur.com/UFUl7Mw.png)
  * Since Windows XP, a [host-based firewall has shipped standard with Windows](https://en.wikipedia.org/wiki/Windows_Firewall), now called Windows Defender Firewall as of Windows 10. See [Computer Hope's article, "How to enable or disable the Microsoft Windows Firewall"](https://www.computerhope.com/issues/ch000551.htm) to learn how to enable or disable it.
  * Whitelisting, also called allow-listing, prevents any application not pre-approved from running. In Windows, you can use the Local Security Policy Editor (by launching `secpol.msc`) to tweak the settings of Window's built-in application allow-listing features, [Windows Defender Application Control (WDAC) or AppLocker](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/wdac-and-applocker-overview).
  * [GoToMyPC](https://gotomypc.com) is a popular Windows remote access tool; when installed by end-users in corporate environments it can pose a security risk because of the way it makes PCs behind corporate firewalls accessible to others over the Internet.
  * As Edie gets up to walk Elliot over to Fred, she locks her PC screen immediately so that passersby cannot use her computer while she's gone, a pro move. Read [10 Ways to Lock Your Windows 10 PC](https://www.howtogeek.com/686827/10-ways-to-lock-your-windows-10-pc/).
* "Log data from the Dark Army's backdoored machine. They're using this guy's account, Frank Bowman. He's a member of the [code signing](https://en.wikipedia.org/wiki/Code_signing) architecture team. This is what they're doing: they want to sign their own firmware and bypass my patch. If they do that, they'll blow up the downtown recovery buidling. My only chance to stop it is to get to the [hardware security modules](https://en.wikipedia.org/wiki/Hardware_security_module), the HSMs. They're on the 23rd floor."
  * Read: [Hackers are selling legitimate code-signing certificates to evade malware detection](https://www.zdnet.com/article/hackers-are-selling-legitimate-code-signing-certificates-to-evade-malware-detection/) (February 2018)
  * Read: [APTs, RATs and Code-Signing Attacks](https://securityboulevard.com/2020/04/apts-rats-and-code-signing-attacks/) (April 2020)
* "I'll tailgate someone." Also known as [piggybacking](https://en.wikipedia.org/wiki/Piggybacking_%28security%29).
* Angela accesses the code signing machine on floor 23 of the E-Corp building.  
  ![](https://web.archive.org/web/20201217034046if_/https://i.imgur.com/WQTEnDT.png)  
  ![](https://web.archive.org/web/20201217034114if_/https://i.imgur.com/4AnkkHR.png)
* A sign reading "There's no place like 127.0.0.1" in the geeky code signing architecture team's office.  
  ![](https://web.archive.org/web/20201217034409if_/https://i.imgur.com/7B7tz41.png)
  * `127.0.0.1` is the conventional IPv4 address of "this computer," or "self," or "localhost, or, as Dorothy would say it, "home."
* Irving and Angela use call-and-response code words to authenticate their audio calls: "Marlinspike." "Moxie."  
  ![](https://web.archive.org/web/20201217033917if_/https://i.imgur.com/RVnROmM.png)
  * [Moxie Marlinspike](https://en.wikipedia.org/wiki/Moxie_Marlinspike) is the famous hacker and programmer best known for creating the Signal Protocol (double-ratchet aglorithm) store-and-forward end-to-end encrypted messaging system.

# Week 28 (S03E06)

See also [Mr. Robot Disassembled: eps3.5_kill-process.inc](https://medium.com/@ryankazanciyan/mr-robot-disassembled-eps3-5-kill-process-inc-69deabb5013c).

# Week 29 (S03E07)

See also [Mr. Robot Disassembled: eps3.6_fredrick+tanya.chk](https://medium.com/@ryankazanciyan/mr-robot-disassembled-eps3-6-fredrick-tanya-chk-c05d900b46).

# Week 30 (S03E08)

* [ProtonMail](https://protonmail.com/), a popular web-based e-mail service with built-in support for OpenPGP.  
  ![](https://web.archive.org/web/20210104033945if_/https://i.imgur.com/hPAA3G2.png)
  * But see [[ProtonMail]].

# Week 31 (S03E09)

See also [Mr. Robot Disassembled: eps3.8_stage3.torrent](https://medium.com/@ryankazanciyan/mr-robot-disassembled-eps3-8-stage3-torrent-8b80e14fc6fb).

* Using the [Volatility](https://github.com/volatilityfoundation/volatility/) memory forensics framework:
  ![Several terminal windows show the Volatility framework being used.](https://web.archive.org/web/20200328232610/https://i.imgur.com/5CdeunG.jpg)  
  ![Closeup of Elliot using Volatility, :robot: screenshot 📷](https://web.archive.org/web/20180102044147if_/https://i.imgur.com/xpjaytH.jpg)
* Elliot crafts [shellcode](https://en.wikipedia.org/wiki/Shellcode) to be executed via Python(?) by discovering a vulnerability through [fuzzing](https://en.wikipedia.org/wiki/Fuzzing) using [American Fuzzy Lop (AFL)](https://lcamtuf.coredump.cx/afl/) and inspecting the crashing program with the [GNU Debugger (`gdb`)](https://www.gnu.org/software/gdb/):
  ![Elliot using American Fuzzy Lop (AFL) fuzzer and the GNU Debugger.](https://web.archive.org/web/20200328231155/https://i.imgur.com/pDXwATz.png)  
  ![Closeup of a GDB session depicting a program crash (segfault).](https://web.archive.org/web/20200328231831/https://i.imgur.com/pjrAwjM.jpg)  
  ![Exploit shellcode being written.](https://web.archive.org/web/20200328232220/https://i.imgur.com/Vw5FdxU.jpg)
* Dark Army [Command and Control (C2)](https://en.wikipedia.org/wiki/Command_and_control_%28malware%29) operator station loads Elliot's exploit:  
  ![Screenshot of the Dark Army's C2 user interface.](https://i.imgur.com/YNtDObO.jpg)
* Elliot logs in to a server with a new SSH key (`ssh-add`) to view the keystrokes, and thus username and password, of the compromised Dark Army operator:
  ![Elliot adds an SSH key identity and views the loot.](https://web.archive.org/web/20200328233348/https://i.imgur.com/j9TkWom.jpg)  
  ![The password of the Dark Army operator is revealed in a cleverly named file.](https://web.archive.org/web/20200328233606/https://i.imgur.com/AMXsiWL.jpg)

# Week 32 (S03E10)

See also [Mr. Robot Disassembled: eps3.9_shutdown -r](https://medium.com/@ryankazanciyan/mr-robot-disassembled-eps3-9-shutdown-r-e03d5fa0069a).

* [Slackware](http://www.slackware.com/), a classic, minimalistic, and intentionally UNIX-like Linux distribution.  
  ![](https://web.archive.org/web/20210116044214if_/https://i.imgur.com/yLkAH8x.png)
* [Bit.ly](https://bit.ly/), a popular [URL shortening](https://en.wikipedia.org/wiki/URL_shortening) service  
  ![](https://web.archive.org/web/20210116045619if_/https://i.imgur.com/7TqCLvQ.png)
* [Dropbox](https://dropbox.com/), a popular [online file storage service](https://simple.wikipedia.org/wiki/File_hosting_service)  
  ![](https://web.archive.org/web/20210116045753if_/https://i.imgur.com/0q2Jf9n.png)
* [`cryptsetup`](https://en.wikipedia.org/wiki/Dm-crypt#cryptsetup) and the [Linux Unified Key Setup (LUKS)](https://en.wikipedia.org/wiki/Linux_Unified_Key_Setup)  
  ![](https://web.archive.org/web/20210116050327if_/https://i.imgur.com/wrlXEdP.png)  
  ![](https://web.archive.org/web/20210116051434if_/https://i.imgur.com/hPdP9tb.png)
  ![](https://web.archive.org/web/20210116051433if_/https://i.imgur.com/Tu4P7Al.png) 
  ![](https://web.archive.org/web/20210116050347if_/https://i.imgur.com/q31i8HY.png)
  * Elliot uses [PyLyrics](https://github.com/geekpradd/PyLyrics) to [build a better password cracking wordlist](https://github.com/AnarchoTechNYC/meta/tree/master/train-the-trainers/mr-robots-netflix-n-hack/week-2/strengthening-passwords-to-defend-against-john#better-wordlists) based on his personal knowledge of Romero.
  * [`bruteforce-luks`](https://github.com/glv2/bruteforce-luks)
  * [`lsblk`](https://www.man7.org/linux/man-pages/man8/lsblk.8.html), "list block devices" Linux command

# Week 33 (S04E01)

# Week 34 (S04E02)

# Week 35 (S04E03)

# Week 36 (S04E04)

* Darlene and Elliot use Signal to communicate with one another.  
  ![Still of a TV DVR showing Signal on screen during an episode of Mr. Robot.](https://s19.directupload.net/images/191028/a3e6f5l4.png)

# Week 37 (S04E05)

# Week 38 (S04E06)

# Week 39 (S04E07)

# Week 40 (S04E08)

# Week 41 (S04E09)

# Week 42 (S04E10)

# Week 43 (S04E11)

# Week 44 (S04E12)

# Week 45 (S04E13)

