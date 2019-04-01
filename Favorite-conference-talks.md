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

# Computer Systems

* [The Tragedy of systemd - linux.conf.au 2019](https://www.youtube.com/watch?v=o_AIw9bGogo)

  A January, 2019 presentation by [FreeBSD](https://www.freebsd.org/) developer [Benno Rice](https://twitter.com/jeamland) discussing the origins of [systemd](https://freedesktop.org/wiki/Software/systemd/), and its role in providing a set of "system layer" functions that conceptually sit between the traditional notions of kernelspace and userspace. He also discusses the contention around the use and adoption of systemd, how contempt culture stifles progress, and how the systemd project ought to be looked at as a source of ideas rather than a problematic piece of software.

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

# Triage

> :memo: This section contains a list of links to videos that have not yet been curated. It's a link-dump, and is need of editorial review.

* Hacktivity 2012 - Joe McCray - Big Bang Theory - Pentesting high security environments https://www.youtube.com/watch?v=qBVThFwdYTc
* DEF CON 22 - Deviant Ollam & Howard Payne - Elevator Hacking - From the Pit to the Penthouse https://www.youtube.com/watch?v=oHf1vD5_b5I
* Black Hat USA 2013 - Lessons from Surviving a 300Gbps Denial of Service Attack https://www.youtube.com/watch?v=w04ZAXftQ_Y
* Blackhat - 2010 How to Hack Millions of Routers https://www.youtube.com/watch?v=0duYxPIx8gU
* 111 Attacking EvilCorp Anatomy of a Corporate Hack https://www.youtube.com/watch?v=nJSMJyRNvlM
* Defcon 21 - Traffic Interception and Remote Mobile Phone Cloning with a Compromised CDMA Femtocell https://www.youtube.com/watch?v=gfcq8clu1RI
* DEFCON 20: Can You Track Me Now? Government And Corporate Surveillance Of Mobile Geo-Location Data https://www.youtube.com/watch?v=NjuhdKUH6U4
* How to disappear completely - LinuxConf.com.au 2019 https://www.youtube.com/watch?v=LOulCAz4S0M

* * *

See also: [`awesome-sec-talks`, a curated list of awesome Security talks](https://github.com/PaulSec/awesome-sec-talks).