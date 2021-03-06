> [[Wiki|Home]] ▸ **Favorite conference talks**

Sometimes, the best way to learn a thing is to just find someone willing to show-and-tell you stuff about it. It's also useful to have a mix of active (practice) and passive (consumptive) educational material.

> 📝 🚧 This is somewhat of an experiment to see if a list like this is useful. It's intended to be a sort of passive-study supplement to the material in the rest of this wiki. My thinking is that it's nice to be given a guided path through "the black hole of YouTube" for long bus rides, meal times, or other periods where our hands cannot be on the keyboard.

# Contents

1. [Computer Systems](#computer-systems)
    1. [Phones](#phones)
1. [Security](#security)
    1. [Privacy and anonymity](#privacy-and-anonymity)
    1. [Hacking](#hacking)
        1. [Hacking demonstrations](#hacking-demonstrations)
        1. [Law and Politics](#law-and-politics)
1. [Fun](#fun)
    1. [Biotechnology](#biotechnology)

# Computer Systems

* [The Future of Computing - DBX 2013](https://www.youtube.com/watch?v=8pTEmbeENF4)

  For his recent DBX Conference talk, Victor took attendees back to the year 1973, donning the uniform of an IBM systems engineer of the times, delivering his presentation on an overhead projector. The '60s and early '70s were a fertile time for CS ideas, reminds Victor, but even more importantly, it was a time of unfettered thinking, unconstrained by programming dogma, authority, and tradition. 'The most dangerous thought that you can have as a creative person is to think that you know what you're doing,' explains Victor. 'Because once you think you know what you're doing you stop looking around for other ways of doing things and you stop being able to see other ways of doing things. You become blind.' He concludes, 'I think you have to say: "We don't know what programming is. We don't know what computing is. We don't even know what a computer is." And once you truly understand that, and once you truly believe that, then you're free, and you can think anything.'"

* [You Don't Know Jack About .bash_history - SANS DFIR Summit 2016](https://www.youtube.com/watch?v=wv1xqOV2RyE)

  The .bash_history file tracks a user’s command history and is an important artifact in Linux and Mac forensics. But many investigators don’t understand the rules for how and when they are written and can make wrong investigative assumptions. Suspects may attempt anti-forensic techniques to corrupt or remove .bash_history content. In other words, “It’s complicated.” Using both disk and memory based forensics, Hal Pomeranz will shine a little light on some of the darker corners of bash behavior. What does “normal” look like? What artifacts besides the .bash_history itself can we use to achieve certainty about user behavior? How does a combination of disk and memory forensics help us when interpreting a user’s command history?

* [The Tragedy of systemd - linux.conf.au 2019](https://www.youtube.com/watch?v=o_AIw9bGogo)

  A January, 2019 presentation by [FreeBSD](https://www.freebsd.org/) developer [Benno Rice](https://twitter.com/jeamland) discussing the origins of [systemd](https://freedesktop.org/wiki/Software/systemd/), and its role in providing a set of "system layer" functions that conceptually sit between the traditional notions of kernelspace and userspace. He also discusses the contention around the use and adoption of systemd, how contempt culture stifles progress, and how the systemd project ought to be looked at as a source of ideas rather than a problematic piece of software.

* [Kubernetes Deconstructed: Understanding Kubernetes by Breaking It Down - Carson Anderson, DOMO](https://vimeo.com/245778144/4d1d597c5e)

  Understanding [Kubernetes](https://kubernetes.io/) as a whole can be daunting. With so many different components working together it can be hard to know how the pieces work together or where new products and features fit in. I will start at the highest level and then peel off the layers one at time to explain how some of the "magic" happens. ([Abridged version](https://www.youtube.com/watch?v=90kZRyPcRZw).)

* [Censorship Is No Longer Interpreted as Damage (And What We Can Do About It) - HOPE 2020](https://archive.org/details/hopeconf2020/20200727_1200_Censorship_Is_No_Longer_Interpreted_as_Damage.mp4)

  In 2020, the Internet no longer interprets censorship as damage. Countrywide targeted web blocks are in effect everywhere from the Azerbaijan to Zimbabwe. TLS SNI-based blocking is deployed in places like Kazakhstan. And the only "solutions" seemingly on the table lead to further centralization via gatekeepers like CloudFlare. Many Internet censorship circumvention tools are available to users, but it's unreasonable to expect whole populations to switch to the Tor Browser or Psiphon in order to access a blocked site. At the same time, effective strategies that website admins can implement on their own seem few and far between. In this talk, based on years of experience running a high-profile site censored in several countries, Michal "rysiek" Wozniak will go through some of these strategies.

  He'll start with moving to static content and enabling some decent caching on your own edge, through using Web Archive as a live backup, and focus on some funky p2p technologies (like IPFS or `dat://`) which, when deployed, could make censoring a website way, way harder. Browser vendors will not be let off the hook. Internet gatekeepers will receive dishonorable mentions. Blockchain will only be discussed sarcastically.

## Phones

* [The Secret Life of SIM Cards - DEF CON 21](https://www.youtube.com/watch?v=31D94QOo2gY)

  An August, 2013 presentation detailing everything you wanted to know about SIM cards, which are basically an additional mini-computer inside your mobile phone (including "dumb" phones, not just smartphones), but didn't know to ask. This talk introduces you to what a SIM card is, why it exists, and what your telephone company uses them for.

* [Practical Cellphone Spying - DEF CON 18](https://www.youtube.com/watch?v=DU8hg4FTm0g)

  In this 2010 talk, Kristin Paget (of [Microsoft, Apple](https://www.wired.com/2012/12/apple-hires-hacker/), and Lyft security) demonstrates how her home-made IMSI catcher built with a [Debian](https://www.debian.org/) distribution of GNU/Linux, [OpenBTS](http://openbts.org/), and [Asterisk](https://www.asterisk.org/) can spoof cell phone networks and intercept plaintext mobile phone calls, SMS, and other data. She discusses the insecure nature of the second-generation (2G) GSM protocol, and offers advice for both attackers and defenders occupying the cell phone radio band.

# Security

* [The Science of Insecurity - ShmooCon 2012](https://www.youtube.com/watch?v=CiqioE1zGCw)

  Why is the overwhelming majority of networked software still not secure, despite all effort to the contrary? In this talk we'll draw a direct connection between this ubiquitous insecurity and basic computer science concepts of Turing completeness and theory of languages. We will show how well-meant protocol designs are doomed to their implementations becoming clusters of 0day, and will show where to look for these 0day. We will also discuss simple principles of how to avoid designing such protocols.

* [SecureDrop: Leaking safely to modern news organizations - LibrePlanet 2017](https://media.libreplanet.org/u/libreplanet/m/securedrop-leaking-safely-to-modern-news-organizations/)

  Learn how [Freedom of the Press Foundation](https://freedom.press/) maintains a free software anonymous whistleblowing platform used by major news organizations, called [SecureDrop](https://securedrop.org/). Senior DevOps Engineer for the SecureDrop project, Conor Schaefer, outlines the project's history, provides an overview of its current architecture, and discusses the challenges of managing a largely decentralized platform with high security requirements.

* [Something Something Security, by Troy Hunt](https://www.youtube.com/watch?v=gVXEwfH6FLc)

  A humorous look into the abysmal state of online security: "How do dormant cyber pathogens spread? Do hackers really wear hoodies while they hack? And how hard is to become a genuine, bona fide evil cyber hacker anyway? These and many more burning cyber security questions will be tackled in a non-stop action packed look at the state of online security."

* [Physical Security on the Front Lines by Deviant Ollam](https://www.youtube.com/watch?v=bWGOpd-N9JA)

  This talk gives a look at some of the more novel ways that people can gain rapid entry using cursory tactics, many of which ignore lock cylinders entirely! As always, tactical and military analogies will be employed to make direct connections between INFOSEC and any other engagement where assailants must be kept at bay for as long as possible using the resources you have available. Remember the "Three R's" of Physical Security? How about the "Three B's" of tactical defense? If you don't, you'll learn them this time.

* [My year on the front line - cleaning infected [WordPress] sites](https://www.youtube.com/watch?v=dzuQYV-diZg)

  In this talk, a former [WordFence](https://www.wordfence.com/) site cleaner will share stories from the more memorable sites he cleaned (names changed to protect the innocent), including revealing his all-time favorite WP malware, and the epic tale of the persistent attacker that almost thwarted the Wordfence team completely. Scattered throughout will be tips and ideas to help protect your site from compromise and keep everyone (except the bad guys!) happy.

## Privacy and anonymity

* ["EXCUSE ME, I THINK YOUR DARK WEB IS LEAKING!" by Sarah Jamie Lewis - BSides Vancouver 2017](https://www.youtube.com/watch?v=ShrZ4B9R3NQ)

  Former GCHQ and Amazon security employee Sarah Jamie Lewis discusses several common [Tor Onion service de-anonymization vectors](https://github.com/AnarchoTechNYC/CTF/wiki/Tor) including `localhost` bypasses and information disclosure vulnerabilities that can be found using [OnionScan](https://onionscan.org/), an Onion site auditing tool that she wrote.

## Hacking

### Hacking demonstrations

* ["Look Ma, No Exploits!" The Recon-NG Framework - DerbyCon 2013](https://www.youtube.com/watch?v=vkmNTNl6urw)

  Tim Tomes, aka "LaNMaSteR53," introduces `recon-ng`, a free and open source software toolkit for performing OSINT gathering and reconnaissance tasks ahead of penetration tests. The tool is now a staple of online investigators and has hundreds of contributed modules and plugins. Its similarity to and tight integration with Metasploit makes it easy to learn and use for numerous common penetration testing tasks.

* [Advanced SQL Injection, by Joseph McCray - DEF CON 17](https://www.youtube.com/watch?v=rdyQoUNeXSg)

  Manually testing for SQL injection vulnerabilities will still expose many problems that automated vulnerability scanners report as not exploitable. In his "Advanced SQL Injection" talk, Joe talks about the difference between SQLi in [[deliberately vulnerable systems|InfoSec#deliberately-vulnerable-systems]] like [WebGoat](https://www.owasp.org/index.php/Category:OWASP_WebGoat_Project) versus what it takes to exploit SQLi vulnerabilities in the real world. He details how to perform manual discovery of injection points, manual enumeration of database internals, and manual techniques for evading IDS/IPS/WAF defenses. The key takeaway: always do at least some manual SQLi testing so you can be sure your automated, black box vuln scanners have not missed anything.

* [Exploiting Network Surveillance Cameras Like a Hollywood Hacker, by Craig Heffner - Black Hat 2013](https://www.youtube.com/watch?v=B8DjTcANBx0)

  You don't need to buy expensive cameras to find exploitable vulnerabilities in them. Moreover, *very* expensive cameras have trivially exploitable remote code execution vulnerabilities. Using `binwalk`, IDA Pro, and several other basic [reverse engineering tools](https://github.com/enaqx/awesome-pentest#reverse-engineering-tools), former National Security Agency analyst Craig Heffner describes how he (and you!) can pwn some very popular, and very expensive, Internet-connected "security" cameras.

* [Radio Hacking: Cars, Hardware, and more! - Samy Kamkar - AppSec California 2016](https://www.youtube.com/watch?v=1RipwqJG50c)

  "In this talk I'll introduce radio hacking, and take it a few levels into hacking real world devices like wirelessly controlled gates, garages, and cars. Many vehicles are now controlled from mobile devices over GSM and the web, while even more can be unlocked and ignitions started from wireless keyfobs over RF. All of these are subject to attack with low-cost tools (such as RTL-SDR, GNU Radio, HackRF, Arduino, and even a Mattel toy). We'll investigate how these features work, and of course, how they can be exploited." (Pair with "Hacking the Wireless World with Software Defined Radio - Black Hat Europe 2014," below.)

* [Hacking the Wireless World with Software Defined Radio - Black Hat Europe 2014](https://www.youtube.com/watch?v=N0p3_ES2dBU)

  "What sorts of RF transactions take place in RFID systems, such as toll booths, building security and vehicular keyless entry? […] Wireless systems, and their radio signals, are everywhere: consumer, corporate, government, amateur - widely deployed and often vulnerable. If you have ever wondered what sort of information is buzzing around you, this talk will introduce how you can dominate the RF spectrum by 'blindly' analysing any signal, and then begin reverse engineering it from the physical layer up. I will demonstrate how these techniques can be applied to dissect and hack RF communications systems, such as those above, using open source software and cheap radio hardware. In addition, I'll show how long-term radio data gathering can be used to crack poorly-implemented encryption schemes, such as the Radio Data Service's Traffic Message Channel." (See also: [All Your RFz Are Belong to Me - Hacking the Wireless World with Software Defined Radio - DEF CON 21](https://www.youtube.com/watch?v=ZuNOD3XWp4A).) (Pair with "Radio Hacking: Cars, Hardware, and more! - Samy Kamkar - AppSec California 2016," above.)

### Law and Politics

* [How Tor Users Got Caught - DEF CON 22 (Part 1)](https://www.youtube.com/watch?v=7G1LjQSYM5Q), and [Part 2](https://www.youtube.com/watch?v=TQ2bk9kMneI)

  Four examples of people who have used Tor for illegal activities and how they were caught. Multiple Tor de-anonymization attacks are shown at the end of the video. [Source](http://se.azinstall.net/2015/11/how-tor-users-got-caught.html).

* [Don't Fuck It Up! by Zoz - DEF CON 22](https://www.youtube.com/watch?v=J1q4Ir2J8P8)

  Learn how not to fuck up covering your tracks on the Internet, using burner phones, collaborating with other dissidents and more. If you have anything to hide, and all of us do, pay attention and Don't. Fuck. It. Up! [Zoz introduces his idea of The 7 Deadly Fuckups, "what makes you a candidate for getting busted,"](https://www.youtube.com/watch?v=J1q4Ir2J8P8&t=11m56s) and urges anyone getting up to any kind of mischief to take their OPSEC seriously. Remember, "using a tool badly or stupidly can be worse than not using the tool at all. […] Two questions when it comes to tools: 'should I use it?' And, 'how should I use it?' […I]f your life or your freedom depend on it, don't trust one single element. This includes Tor and lots of other tools in your communication chain. Do your tradecraft analysis."

# Fun

* [Owning NFC toys I own: a case study by Vitorio Miliano](https://nfc.toys/) ([video](https://livestream.com/internetsociety3/hope/videos/178835170))

## Biotechnology

* [DNA: The Code of Life (SHA2017) by Bert Hubert](https://www.youtube.com/watch?v=EcGM_cNzQmE)

  DNA is the code of life. It encodes how we are built, how nature operates. Science learns more and more about this uniquely digital language. This talk will excite hackers and anyone who knows a little bit about computing, since it turns out DNA is better explained in terms of bits than in terms of classical biology. Prepare to be blown away! Continued in [DNA: More Greatest Hits (SHA2017)](https://www.youtube.com/watch?v=rCdhsN--Mdo).

# Triage

> :memo: This section contains a list of links to videos that have not yet been curated. It's a link-dump, and is need of editorial review.

* Drupal Flyover Camp 2019 - Jeff Geerling - Everything I Know About Kubernetes I Learned from a Cluster of Raspberry Pis https://youtube.com/watch?v=QbdLO-IKFzc
* Summercon 2019 - Ben Perez - Trail of Bits - Fuck RSA https://youtube.com/watch?v=lElHzac8DDI
* Hacktivity 2012 - Joe McCray - Big Bang Theory - Pentesting high security environments https://www.youtube.com/watch?v=qBVThFwdYTc
* DEF CON 22 - Deviant Ollam & Howard Payne - Elevator Hacking - From the Pit to the Penthouse https://www.youtube.com/watch?v=oHf1vD5_b5I
* Black Hat USA 2013 - Lessons from Surviving a 300Gbps Denial of Service Attack https://www.youtube.com/watch?v=w04ZAXftQ_Y
* Blackhat - 2010 How to Hack Millions of Routers https://www.youtube.com/watch?v=0duYxPIx8gU
* 111 Attacking EvilCorp Anatomy of a Corporate Hack https://www.youtube.com/watch?v=nJSMJyRNvlM
* Defcon 21 - Traffic Interception and Remote Mobile Phone Cloning with a Compromised CDMA Femtocell https://www.youtube.com/watch?v=gfcq8clu1RI
* DEFCON 20: Can You Track Me Now? Government And Corporate Surveillance Of Mobile Geo-Location Data https://www.youtube.com/watch?v=NjuhdKUH6U4
* How to disappear completely - LinuxConf.com.au 2019 https://www.youtube.com/watch?v=LOulCAz4S0M
* Apathy and Arsenic: a Victorian Era lesson on fighting the surveillance state https://www.youtube.com/watch?v=egi8Lm5W3FY
* See what your computer is doing with Ftrace utilities https://www.youtube.com/watch?v=68osT1soAPM
* Kernel Security Is Cool Again https://www.youtube.com/watch?v=GFGJ3e3oj2c
* Web Security 2019 https://www.youtube.com/watch?v=q99Nj-_oaQc
* The Tor censorship arms race: https://www.youtube.com/watch?v=ZB8ODpw_om8
* * *

See also: [`awesome-sec-talks`, a curated list of awesome Security talks](https://github.com/PaulSec/awesome-sec-talks), [:globe_with_meridians: InfoCon.org](https://infocon.org/).