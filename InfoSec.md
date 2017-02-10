> [[Wiki|Home]] ▸ **InfoSec**

Cool stuff for "[the Cyber](https://www.theatlantic.com/technology/archive/2016/09/trumps-incoherent-ideas-about-the-cyber/501839/)" that tech antifa folks have played around with/contributed to/enjoyed pentesting in the past.

1. [At AnarchoTechNYC](#at-anarchotechnyc)
1. [CTFs and Hacking Games](#ctfs-and-hacking-games)
  1. [CTFs](#ctfs)
    1. [CTF calendars and archives](#ctf-calendars-and-archives)
    1. [Recommended CTFs](#recommended-ctfs)
  1. [Hacking challenges](#hacking-challenges)
1. [Labs and practice VMs](#labs-and-practice-vms)
1. [Lesson plans and guidance](#lesson-plans-and-guidance)
1. [For defenders](#for-defenders)
1. [Other lists](#other-lists)

# At AnarchoTechNYC

* [[Mr. Robot's Netflix 'n' Hack]], a weekly guided tour of hacking tools in pop culture

# CTFs and Hacking Games

[**Capture The Flag competitions (CTFs)**](https://en.wikipedia.org/wiki/Capture_the_flag#Computer_security) are sets of puzzles intended to distill the essence of many aspects of professional computer security work into a single short-lived exercise that is objectively measurable. Most competitions are free to participate, and some even award prizes to winners. They are often associated with a conference or event, so are open only at certain times, run for a short while, then close and rank the participants according to the competition's scoring rules.

[**Wargames**](https://en.wikipedia.org/wiki/Wargame_(hacking)), sometimes also called **hacking challenges**, are stand-alone puzzlers that are always available (they are not associated with a time or event). Typically, they are organized into levels that get progressively harder as you solve more of them. Some hacking/wargame sites also organize challenges into categories based on the skills you need to solve them.

## CTFs

### CTF calendars and archives

Hundreds of upcoming CTFs are listed at:

* [CTFTime.org](https://ctftime.org/) - List of upcoming CTFs to compete in, central (unofficial) directory of teams, and archive of previous challenge write-ups for educational purposes.
* [CapTF Calendar](http://captf.com/calendar/)

If others are interested, we could probably field our own team(s). It also might be fun to hang out with the [opentoall team](http://opentoallctf.com/) on IRC.

### Recommended CTFs

* [Ghost in the Shellcode](http://ghostintheshellcode.com/)

  An annual capture-the-flag contest that takes place every winter -- generally in January, but sometimes in February.

## Hacking challenges

* [Microcorruption](https://www.microcorruption.com)

  The fact that this wargame can be played entirely in your browser makes it really great if you are new to reverse engineering and binary exploitation as you do not have to worry about learning GDB or other tools to get going. It's still really fun even if you are not new. The levels start out simple -- grabbing a key from memory, basic stack smashing -- and get more complicated as defensive measures are enabled and the reversing task is made more complicated by obfuscation.

* [SmashTheStack](http://www.smashthestack.org/)

  🚧 TK-TODO (needs a good, succinct description)

* [Cryptopals](http://cryptopals.com)

  Learn how cryptosystems are built and how they are attacked. By the same creators as Microcorruption.

* [Ghost in the Shellcode -- Pwn Adventure](http://pwnadventure.com)

  The CTF has ended but the game server and clients are freely available. There's an MMO-style game that's vulnerable to tampering. I guess the idea is to proxy your connection through some code that will alter your requests and give you superpowers in-game. We could get the server running if a group of people is interested in playing together.

* [Over the Wire](http://overthewire.org)

  This is a series of games played over SSH. Each level corresponds to a user with a shell account on the game server. There's a set of binaries with their setuid flags set. The tasks are typically in the form of: exploit the binary, become the next user, repeat. Unlike micorcorruption, there's no nice webapp debugger, so you'll need to learn GDB, [radare2](http://radare.org) or something. I thought these were really fun, and because the environment is a lot less controlled than microcorruption, I learned a lot about how subtle factors can foil your exploit.

* [io](http://io.netgarage.org), [io64](http://io.netgarage.org:8064), [ioarm](http://188.166.114.127)
  
  Like Over the Wire, the io games are played over SSH with the goal of escalating privileges to advance levels. Home to a great IRC channel too.

* [Exploit Exercises](https://exploit-exercises.com/)

  A variety of virtual machines, documentation and challenges that can be used to learn about a variety of computer security issues such as privilege escalation, vulnerability analysis, exploit development, debugging, reverse engineering, and general cyber security issues. 

* [BreakThiSQLi](http://breakthisqli.rf.gd/)

  SQL injection challenges by increasing difficulty. Fun for the whole database family!

* [CanYouHack.Us](https://canyouhack.us/)

  Mixture of Web and binary security challenges.

* [id0-rsa](https://id0-rsa.pub/)

  Cryptography challenges.

* [pwnable.kr](https://pwnable.kr)

  More memory corruption. Most levels are vulnerable services running on a particular port. You can exploit them remotely to get a shell, read a "flag" file, and register it with the website to be awarded "points."

* [RingZer0team.com](https://ringzer0team.com/)

  Several hundred challenges across numerous cybersecurity categories that you can tackle on your own time. Also includes a leaderboard and encourages participants to post write-ups of their solutions to the hacking puzzles, so you can learn from others' successful hacks.

# Labs and practice VMs

* [Hacking Lab](https://www.hacking-lab.com)

* [Penteseter Lab](https://PentesterLab.com)

* [VulnHub](https://www.vulnhub.com)

# Lesson plans and guidance

* [HackerHigherschool.org](http://hackerhighschool.org/)

  Exceptionally friendly and thorough introduction to penetration testing ("hacking") and general security concepts written with teenagers in mind. Perfect for people who want a more guided path to learning network security and computer exploitation basics.

* [CTF Field Guide](https://trailofbits.github.io/ctf/)

  A handy companion guide for learning an interdisciplinary set of skills in infosec, with a mind towards practicing them by puzzling out various CTF challenges.

* [Programming Linux Anti-Reversing Techniques](https://leanpub.com/anti-reverse-engineering-linux)

  A free e-book with a pre-compiled binary that "teaches the reader how to code and analyze well known anti-reversing techniques for Linux. The book shows how a reverse engineer analyzes a binary using tools like IDA, Radare2, GDB, readelf, and more." Useful for learning reverse engineering beginners. Its [companion repositories can be found on GitHub](https://github.com/antire-book).

# For defenders

* [PrivacyTools.io](https://privacytools.io)

  Simply start at the top and read down the page. This is as guided an introduction to privacy issues and what to do about them as it gets.

* [Surveillance Self-Defense](https://ssd.eff.org/)

  The Electronic Frontier Foundation's thorough guide to defending yourself and your friends from surveillance by using secure technology and developing careful practices.

* [An Activist's Guide to Information Security](https://archive.org/download/AnActivistsGuideToInformationSecurity/activist-info-sec-SCREEN.pdf)

  A brief and attractive zine written by ABC Dresden that introduces activist laypeople to various components of infosec.  There is also an [imposed version](https://archive.org/download/AnActivistsGuideToInformationSecurity/activist-info-sec-IMPOSED.pdf) for printing and distributing in meatspace.

* [Digital Security Tips for Protesters](https://www.eff.org/deeplinks/2016/11/digital-security-tips-for-protesters)

  A top-ten list of digital security tips intended for a specific type of defender ("protesters"). Possibly easier to digest than the more thorough "Surveillance Self-Defense" guide, despite being written by the same source.

# Other lists

* [awesome-pentest](https://github.com/enaqx/awesome-pentest)
* [awesome-ctf](https://github.com/apsdehal/awesome-ctf)
* [pentest-links](https://github.com/meitar/pentest-links)
* [awesome-reversing](https://github.com/tylerph3/awesome-reversing)

***

See also

* [NYC-InfoSec.com](https://www.nyc-infosec.com/), a calendar of infosec-related events in the New York City area.
* [Zapya's list of CTF and hacking challenge sites](http://www.zapyaapkforpc.com/2016/12/top-hacking-sites-ctfs-and-wargames-to.html)