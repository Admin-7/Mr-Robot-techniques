> [[Wiki|Home]] ▸ **InfoSec**

Cool stuff for "The Cyber" that tech antifa folks have played around with/contributed to/enjoyed pentesting in the past.

1. [At AnarchoTechNYC](#at-anarchotechnyc)
1. [CTFs and Hacking Games](#ctfs-and-hacking-games)
1. [Labs and practice VMs](#labs-and-practice-vms)
1. [Lesson plans and guidance](#lesson-plans-and-guidance)
1. [For defenders](#for-defenders)

# At AnarchoTechNYC

* [[Mr. Robot's Netflix 'n' Hack]], a weekly guided tour of hacking tools in pop culture

# CTFs and Hacking Games

* [Microcorruption](https://www.microcorruption.com)

  The fact that this CTF can be played entirely in your browser makes it really great if you are new to reverse engineering and binary exploitation as you do not have to worry about learning GDB or other tools to get going. It's still really fun even if you are not new. The levels start out simple -- grabbing a key from memory, basic stack smashing -- and get more complicated as defensive measures are enabled and the reversing task is made more complicated by obfuscation.

* [Cryptopals](http://cryptopals.com)

  Learn how cryptosystems are built and how they are attacked. By the same creators as Microcorruption.

* [Ghost in the Shellcode -- Pwn Adventure](http://pwnadventure.com)

  The CTF has ended but the game server and clients are freely available. There's an MMO-style game that's vulnerable to tampering. I guess the idea is to proxy your connection through some code that will alter your requests and give you superpowers in-game. We could get the server running if a group of people is interested in playing together.

* [Over the Wire](http://overthewire.org)

  This is a series of games played over SSH. Each level corresponds to a user with a shell account on the game server. There's a set of binaries with their setuid flags set. The tasks are typically in the form of: exploit the binary, become the next user, repeat. Unlike micorcorruption, there's no nice webapp debugger, so you'll need to learn GDB, [radare2](http://radare.org) or something. I thought these were really fun, and because the environment is a lot less controlled than microcorruption, I learned a lot about how subtle factors can foil your exploit.

* [io](http://io.netgarage.org), [io64](http://io.netgarage.org:8064), [ioarm](http://188.166.114.127)
  
  Like Over the Wire, the io games are played over SSH with the goal of escalating privileges to advance levels. Home to a great IRC channel too.

* [CTF Time](http://ctftime.org)

  List of upcoming CTFs to compete in. If others are interested, we could probably field an RC team. It also might be fun to hang out with the [opentoall team](http://opentoallctf.com/) on IRC.

* [BreakThiSQLi](http://breakthisqli.rf.gd/)

  SQL injection challenges by increasing difficulty. Fun for the whole database family!

* [CanYouHack.Us](https://canyouhack.us/)

  Mixture of Web and binary security challenges.

* [id0-rsa](https://id0-rsa.pub/)

  Cryptography challenges.

* [pwnable.kr](https://pwnable.kr)

  More memory corruption. Most levels are vulnerable services running on a particular port. You can exploit them remotely to get a shell, read a "flag" file, and register it with the website to be awarded "points."

## Other lists

* [awesome-ctf](https://github.com/apsdehal/awesome-ctf)
* [pentest-links](https://github.com/meitar/pentest-links)
* [awesome-reversing](https://github.com/tylerph3/awesome-reversing)

# Labs and practice VMs

* [Hacking Lab](https://www.hacking-lab.com)

* [Penteseter Lab](https://PentesterLab.com)

* [VulnHub](https://www.vulnhub.com)

# Lesson plans and guidance

* [HackerHigherschool.org](http://hackerhighschool.org/)

  Exceptionally friendly and thorough introduction to penetration testing ("hacking") and general security concepts written with teenagers in mind. Perfect for people who want a more guided path to learning network security and computer exploitation basics.

# For defenders

* [PrivacyTools.io](https://privacytools.io)

  Simply start at the top and read down the page. This is as guided an introduction to privacy issues and what to do about them as it gets.

* [Surveillance Self-Defense](https://ssd.eff.org/)

  The Electronic Frontier Foundation's thorough guide to defending yourself and your friends from surveillance by using secure technology and developing careful practices.

* [An Activist's Guide to Information Security](https://archive.org/download/AnActivistsGuideToInformationSecurity/activist-info-sec-SCREEN.pdf)

  A brief and attractive zine written by ABC Dresden that introduces activist laypeople to various components of infosec.  There is also an [imposed version](https://archive.org/download/AnActivistsGuideToInformationSecurity/activist-info-sec-IMPOSED.pdf) for printing and distributing in meatspace.

* [Digital Security Tips for Protesters](https://www.eff.org/deeplinks/2016/11/digital-security-tips-for-protesters)

  A top-ten list of digital security tips intended for a specific type of defender ("protesters"). Possibly easier to digest than the more thorough "Surveillance Self-Defense" guide, despite being written by the same source.

***

See also

* [NYC-InfoSec.com](https://www.nyc-infosec.com/), a calendar of infosec-related events in the New York City area.