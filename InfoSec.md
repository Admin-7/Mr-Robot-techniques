> [[Wiki|Home]] ▸ **InfoSec**

Cool stuff for "[the Cyber](https://www.theatlantic.com/technology/archive/2016/09/trumps-incoherent-ideas-about-the-cyber/501839/)" that tech antifa folks have played around with/contributed to/enjoyed pentesting in the past.

> 🔰 Are you a newbie and feeling a little overwhelmed by this page? Try our [[starting recommendations|Getting started on InfoSec]].

1. [At AnarchoTechNYC](#at-anarchotechnyc)
1. [CTFs and Hacking Games](#ctfs-and-hacking-games)
    1. [CTFs](#ctfs)
        1. [CTF calendars and archives](#ctf-calendars-and-archives)
        1. [Recommended CTFs](#recommended-ctfs)
    1. [Hacking challenges](#hacking-challenges)
    1. [Cyberwarfare ranges](#cyberwarfare-ranges)
1. [Labs and practice VMs](#labs-and-practice-vms)
    1. [Deliberately vulnerable systems](#deliberately-vulnerable-systems)
1. [Lesson plans and guidance](#lesson-plans-and-guidance)
    * [More lesson material](#more-lesson-material)
1. [For defenders](#for-defenders)
1. [Other lists](#other-lists)

# At AnarchoTechNYC

* [[CTF team]], a semi-private cybersecurity study group that puts the "ethical" back into "ethical hacking."
* [[Lockpicking club]], a locksport practice session and meditative discussion circle featuring those most ubiquitous of doorway decorations.
* [[Mr. Robot's Netflix 'n' Hack]], a weekly guided tour of hacking tools in pop culture.

# CTFs and Hacking Games

[**Capture The Flag competitions (CTFs)**](https://en.wikipedia.org/wiki/Capture_the_flag#Computer_security) are sets of puzzles intended to distill the essence of many aspects of professional computer security work into a single short-lived exercise that is objectively measurable. Most competitions are free to participate, and some even award prizes to winners. They are often associated with a conference or event, so are open only at certain times, run for a short while, then close and rank the participants according to the competition's scoring rules.

[**Wargames**](https://en.wikipedia.org/wiki/Wargame_(hacking)), sometimes also called **hacking challenges**, are stand-alone puzzlers that are always available (they are not associated with a time or event). Typically, they are organized into levels that get progressively harder as you solve more of them. Some hacking/wargame sites also organize challenges into categories based on the skills you need to solve them.

**Deliberately vulnerable systems**, or deliberately exploitable apps, are bundled software packages that are intentionally designed to be practice targets for exploitation attempts. These tools sometimes contain self-describing tutorials or exercise descriptions so that they can be used as a self-contained educational course. They are a noteworthy variant of wargames that can be played "offline" because you can download them to your own computer, like a practice lab.

**Cyberwarfare Ranges** are digital live-fire ranges, semi-private inter-networks where participants can set up and attack other participant's servers and services for educational purposes. They are typically heavily firewalled and accessible only with an invitation and/or through a VPN tunnel; think of them like the digital equivalent of paintball arenas or live-fire gun ranges.

> ℹ️ **A note on netiquette.** While each of these gaming styles offer educational opportunities, most have slightly different etiquette. For instance, it's customary for participants to publish solutions to the challenges presented during CTF competitions in the form of writeups on blogs, but this is discouraged by many hacking challenge sites. Take a moment to familiarize yourself with the publisher of the challenge you're tackling before you publish your solution to the whole Internet, as you may be spoiling the fun of the game for others.

> 💡 **There are more resources on this wiki.** If you do end up tackling some of these hacking puzzlers, you'll definitely find some help elsewhere on this wiki, or the [AnarchoTechNYC CTF team's wiki](https://github.com/AnarchoTechNYC/CTF/wiki). For instance, sooner rather than later you'll find yourself [[identifying data formats]] you never recognized before.

## CTFs

### CTF calendars and archives

Hundreds of upcoming CTFs are listed at:

* [CTFTime.org](https://ctftime.org/) - List of upcoming CTFs to compete in, central (unofficial) directory of teams, and archive of previous challenge write-ups for educational purposes.
* [CapTF Calendar](http://captf.com/calendar/)

If others are interested, we could probably field [[our own team(s)|CTF team]]. It also might be fun to hang out with the [OpenToAll team](http://opentoallctf.com/) on IRC.

### Recommended CTFs

* [PicoCTF](https://picoctf.com/)

  An always-open game targeted for high school students but useful for anyone who is just starting out in computer security. Available games are [PicoCTF 2013](https://2013.picoctf.com/), [PicoCTF 2014](https://2014.picoctf.com/), and [PicoCTF 2017](https://2017.picoctf.com/).

* [Ghost in the Shellcode](http://ghostintheshellcode.com/)

  An annual capture-the-flag contest that takes place every winter -- generally in January, but sometimes in February.

## Hacking challenges

* [CTFLearn](https://ctflearn.com/)

  A crowdsourced collection of practice problems ranging from beginner to expert difficulty. Accounts are free, and anyone can post problems, solve problems, or share news about CTFs. Kind of like a [HackerRank](https://www.hackerrank.com/) or [CodeWars](https://www.codewars.com/) for cybersecurity challenges.

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

* [pwnable.kr](https://pwnable.kr/)

  More memory corruption. Most levels are vulnerable services running on a particular port. You can exploit them remotely to get a shell, read a "flag" file, and register it with the website to be awarded "points."

* [Reversing.kr](https://reversing.kr/)

  A couple dozen diverse reverse engineering challenges, including Java programs, Windows executables, Linux binaries, and more.

* [RingZer0team.com](https://ringzer0team.com/)

  Several hundred challenges across numerous cybersecurity categories that you can tackle on your own time. Also includes a leaderboard and encourages participants to post write-ups of their solutions to the hacking puzzles, so you can learn from others' successful hacks.

* [HackMethod Challenge](http://challenge.hackmethod.com/)

  Month-long "Capture the Flag" and "Root the Box" style challenges, appearing monthly, and with a rolling scoreboard. They also provide (some) guidance in the form of a [roadmap](https://hackmethod.com/roadmap/) that may help guide you through some of their challenges. (But see also [#Lesson plans and guidance](#lesson-plans-and-guidance), below.)

* [HackThisSite](https://www.hackthissite.org/)

  An older (mid-2000's era) set of challenges in Web, IRC, steganograhy, and a few other categories. Notable partly for its hacktivist co-founder, [Jeremy Hammond](https://en.wikipedia.org/wiki/Jeremy_Hammond), famed member of [the Anonymous-affiliated group LulzSec](https://arstechnica.com/tech-policy/2013/05/lulzsec-member-jeremy-hammond-pleads-guilty-to-stratfor-hack/). While outdated, most of the hacking challenges (called "missions") on this site are still decent practice for technology basics that haven't changed much such as fundamental crypto maths, the HTTP protocol, and JavaScript exploitation techniques.

* [HackerTest.net](http://www.hackertest.net/)

  A set of increasingly difficult hacking "levels."

* [W3Challs](https://w3challs.com/)

  Mostly a community site and forum, but has a number of categorized challenges as well, including a couple entirely about writing Web scraping programs.

* [Root Me](https://root-me.org/)

  A collection of a couple hundred stand-alone online challenges and several dozen practice labs ("virtual environments") in a variety of categories.

* [Enigma Group](https://www.enigmagroup.org/)

  A set of challenges in categories such as cryptography, steganography, and Web exploitation "cover[ing] the exploits listed in the OWASP Top 10 Project [to] teach members the many other types of exploits that are found in today's applications; thus, helping them to become better programmers in the mean time."

# Cyberwarfare ranges

* [Arizona Cyberwarfare Range](https://web.archive.org/web/20170211144448/http://azcwr.org/)

# Labs and practice VMs

* [Penteseter Lab](https://PentesterLab.com)
* [VulnHub](https://www.vulnhub.com)
* [Malware Unicorn Workshops](https://securedorg.github.io/)
* [Root Me](https://root-me.org/)
* [Open Security Training](http://opensecuritytraining.info/)
* [FuzzySecurity: Tutorials](https://www.fuzzysecurity.com/tutorials.html)
* [Hacking Lab](https://www.hacking-lab.com)
* [PentestIT Labs](https://lab.pentestit.ru/)

## Deliberately vulnerable systems

* [OWASP Vulnerable Web Applications Directory Project](https://www.owasp.org/index.php/OWASP_Vulnerable_Web_Applications_Directory_Project)

  The OWASP Vulnerable Web Applications Directory Project (VWAD) is a comprehensive and well maintained registry of all known vulnerable web applications currently available for legal security and vulnerability testing of various kinds. Notable items include [Google Gruyere](http://google-gruyere.appspot.com/), the [Damn Vulnerable Web Application](http://www.dvwa.co.uk/), and [WebGoat](https://www.owasp.org/index.php/Category:OWASP_WebGoat_Project).

* [Damn Vulnerable iOS App](http://damnvulnerableiosapp.com/)

  "[T]his application can be used by mobile security enthusiasts and students to learn or review the basics of mobile application security." Supplemental guides can be found on [the author's site's DVIA page](https://n0where.net/damn-vulnerable-ios-app-dvia/).

# Lesson plans and guidance

This section contains a curated, ordered list of supplementary educational content in an effort to provide those who want it with a suggested course "to go from start to finish." Although listed "in order," there are no rules for how you go about your own education. Many topics reference related subjects, or provide only a shallow examination of them so if you find something confusing, consider jumping around a bit until you feel more at ease, or take a break and watch one of our [[favorite conference talks]] from years past.

1. [Hacker Highschool](http://hackerhighschool.org/)  
    Exceptionally friendly and thorough introduction to penetration testing ("hacking") and general security concepts written with teenagers in mind. Perfect for people who want a more guided path to learning network security and computer exploitation basics. Pair with [PicoCTF](https://picoctf.com/) ([described above](#recommended-ctfs)).
1. [Build a Computer from First Principles - Nand2Tetris](http://nand2tetris.org/)  
    A freely available course and textbook for self-learners about the construction of modern, full-scale computer systems—hardware and software. The course follows a bottom-up path beginning with how simple electrical circuits can store information (i.e., "computer memory") all the way through to the workings of a modern laptop. The lectures, book chapters and projects are modular, so you can pursue subsets of them in any desired order and scope. The chapters and projects related to memory storage, the assembler, and the parser have profound implications for and are thus particularly relevant to security.
1. [Linux From Scratch](http://www.linuxfromscratch.org/)  
    These free guidebooks offer step-by-step instruction manuals for building a GNU/Linux system entirely from source code. (If you don't know what "a GNU/Linux system" is, read about [Why Linux Is Better](http://www.whylinuxisbetter.net/) first.) Being able to build directly from source, rather than rely on difficult-to-inspect binary packages distributed by vendors, offers extreme advantages to security-conscious users, so it's wise to gain experience doing this. After completing the main guide, additional guides focus on particular interest areas. Of these, the "[Hardened Linux From Scratch](http://www.linuxfromscratch.org/hlfs/)" guidebook, which "focuses on building an LFS system with heightened security," is of special note as it walks you through the process of configuring many of GNU/Linux's built-in security features. (Pair with [Michiel Derhaeg's "Build Linux" tutorial](https://github.com/MichielDerhaeg/build-linux).)
1. [CTF Field Guide](https://trailofbits.github.io/ctf/)  
    A handy companion guide for learning an interdisciplinary set of skills in infosec, with a mind towards practicing them by puzzling out various CTF challenges.
1. [Metasploit Unleashed](https://www.offensive-security.com/metasploit-unleashed/)  
    A free guide by the makers of the free software exploitation framework known as Metasploit covering the basics of its use through a hands-on introduction in a practice environment against a pre-configured and deliberately vulnerable Linux system. Rather than expect this walk-through to explain the details of exploitation, use this guide to get a feel for the overall process of vulnerability discovery, assessment, exploitation, and persistence so that later guides that reference Metasploit and its numerous utilities are already at least cursorily familiar to you.
1. [Lecture Series: Introductory x86 (32 bit)](https://www.youtube.com/playlist?list=PL038BE01D3BAEFDB0)  
    A series of video lectures from Xeno Kovah's 2 day "Introductory x86" class in Fall of 2010. This is one of the more comprehensive free video resources for learning low-level programming (assembly language) and provides much of the background knowledge required to understand machine instructions and operation, for later use in exploit development ("shellcode") and reverse engineering. If you're having fun, continue on to [ARM Assembly Basics from Azeria Labs](https://azeria-labs.com/writing-arm-assembly-part-1/).
1. [Reverse Engineering for Beginners](https://beginners.re/)  
    A free e-book providing a complete study guide for learning how to analyze raw computer instructions and recover meaningful source code in the process. It provides practice exercises for those with a modest existing understanding of compiled languages like C or Java to work through and explanations of each step in the process. Pair with [Malware Unicorn's Reverse Engineering 101 workshop](https://securedorg.github.io/RE101/).
1. [Programming Linux Anti-Reversing Techniques](https://leanpub.com/anti-reverse-engineering-linux)  
    A free e-book, with an accompanying pre-compiled binary, that "teaches the reader how to code and analyze well known anti-reversing techniques for Linux. The book shows how a reverse engineer analyzes a binary using tools like IDA, Radare2, GDB, readelf, and more." Useful for learning reverse engineering beginners. Its [companion repositories can be found on GitHub](https://github.com/antire-book).
1. [Crypto 101](https://www.crypto101.io/)  
    A free and condensed practical introductory course on cryptography, "freely available for programmers of all ages and skill levels." The book's Forward says it "starts with very simple primitives, and gradually introduces new ones, demonstrating why they’re necessary. Eventually, all of this is put together into complete, practical cryptosystems, such as TLS, GPG and OTR. The goal of this book is not to make anyone a cryptographer or a security researcher. The goal of this book is to understand how complete cryptosystems work from a bird’s eye view, and how to apply them in real software."
1. [A Graduate Course in Applied Cryptography](http://toc.cryptobook.us)  
    A free textbook developed for use in Stanford's and New York University's computer science and mathematics departments covering cryptography. A beginning reader can read though the book to learn how cryptographic systems work and why they are secure. Some knowledge of basic algebra and probability is assumed but you do not need prior experience with graduate-level mathematics courses to utilize this book. (See also [Coursera.org's Cryptography I course](https://www.coursera.org/learn/crypto), taught by one of this book's co-authors.) Use this text if you are already well-versed with the material covered in "Crypto 101" (above).

## More lesson material

* [Internet Security - Weaknesses and Targets (WT 2016/17)](https://www.tele-task.de/archive/series/overview/1130/)

  Lectures by Prof. Dr. Christoph Meinel on "Internet Security - Weaknesses and Targets" gives a detailed introduction on problems concerning Internet and intranet security. After starting with some remarks on risk analysis and computer crimes, security weaknesses and targets are discussed in detail. The lecture concludes with the discussion on possibilities to detect attacks and intrusions and ethical issuses are introduced as well.

# For defenders

* [PrivacyTools.io](https://privacytools.io/)

  Simply start at the top and read down the page for an introduction to various privacy tools and relevant legal concepts. Each section provides a limited set of specific recommendations to follow up on. This is as brief a guided introduction to privacy issues and what to do about them as it gets.

* [Me and My Shadow](https://myshadow.org/)

  Start here if you're unconvinced that you "have something to hide." This site offers an accessible deep-dive into research about the data industry, how advertisers and communication service providers (like [Facebook](https://myshadow.org/lost-in-small-print/facebooks-data-policy) and [Google](https://myshadow.org/lost-in-small-print/googles-privacy-policy)) track you online, what they do with your information, and what you can do about it. It includes several [short privacy guides](https://myshadow.org/increase-your-privacy) along with a helpful [interactive visualization breaking down which activity leaves what type of data trail](https://myshadow.org/trace-my-shadow) and even an "[8-day data detox](https://myshadow.org/detox)" plan.

* [DIY Feminist Cybersecurity](https://hackblossom.org/resources/)

  A thorough walk-through showing how to implement basic and intermediate cybersecurity best practices, geared for oppressed groups whose likely adversary are trolls, white supremacists, and other individuals or mob-sized malicious actors. Written with careful explanations and a good grasp of the state of the art. Highly recommended reading for the politically conscious defender.

* [DIY Cybersecurity for Domestic Violence](https://hackblossom.org/domestic-violence/)

  A super-accessible guide providing "imminent technical support to survivors of domestic violence." This resource can be of use both to people facing intimate partner or domestic violence scenarios as well as anyone seeking a more focused guide regarding adversaries who are not State-level actors.

* [Crash Override Network // Resources](http://www.crashoverridenetwork.com/resources.html)

  A meta-list of additional resources written, compiled, and maintained by the Crash Override Network, including links to purpose-built guides such as [Prevent Doxxing](http://www.crashoverridenetwork.com/preventingdoxing.html) and additional pointers to third-party explainers, such as the [Nonconsensual Intimate Images ("Revenge Porn") Removal Guide](http://www.endrevengeporn.org/online-removal/).

* [Surveillance Self-Defense](https://ssd.eff.org/)

  The [Electronic Frontier Foundation](https://eff.org/)'s comprehensive guide to using privacy-enhancing technologies for defending yourself and your friends from (primarily corporate and State) surveillance. You can [read it like a book, from beginning to end](https://ssd.eff.org/en/index), or you can jump to tutorials on specific tools, advice about choosing the tools in the first place ("[threat modeling](https://ssd.eff.org/en/module/introduction-threat-modeling)" for a [specific kind of user](https://ssd.eff.org/en/playlist)). Similar to [Security In a Box](https://securityinabox.org/).

* [Security In a Box](https://securityinabox.org/)

  A set of comprehensive guides to tools, tactics, and procedures for staying safer online and while using modern day necessities, like phones. The site is organized into sections covering basic principles ("Tactics Guides"), step-by-step instructions for specific tools ("Tool Guides"), and advice for people of specific demographics ("Community Guides") such as [women who are human rights defenders](https://securityinabox.org/en/women-hrds/). Similar to the [Electronic Frontier Foundation's Surveillance Self-Defense](https://ssd.eff.org/).

* [Exposing the Invisible: Watching Out for Yourself](https://exposingtheinvisible.org/resources/watching-out-yourself/)

  The [Tactical Technology Collective](https://tacticaltech.org/)'s "[Exposing the Invisible](https://exposingtheinvisible.org/)" project includes its own self-defense resource listing geared specifically for people using the Internet to conduct journalistic investigations. Notably, this resource includes discussions of how to more safely and [anonymously publish the results of investigations online](https://exposingtheinvisible.org/resources/watching-out-yourself/domain-games). Pair with the [Info-Activism How To Guide](https://howto.informationactivism.org/).

* [GenderSec: Zen and the Art of Making Technology Work for You](https://gendersec.tacticaltech.org/wiki/index.php/Complete_manual)

  The "complete manual" of personal digital security maintained by the Tactical Tech Collective's GenderSec Wiki. Available in English and in [Spanish](https://gendersec.tacticaltech.org/wiki/index.php/Complete_manual/es).

* [Digital Privacy at the U.S. Border](https://www.eff.org/wp/digital-privacy-us-border-2017)

  A detailed report regarding the special-case risks travelers face at the United States border circa 2017. The report includes suggestions for what to do before, during, and after crossing the border to protect your personal data, privacy, and legal rights from violation by border agents.

* [Current Digital Security Resources](https://medium.com/@mshelton/current-digital-security-resources-5c88ba40ce5c)

   A meta-list of additional security training resources for defenders in various situations, curated by digital security trainers making commitments update the list regularly. (This resource is probably more useful for trainers than it is for students, but it is useful nonetheless.) See also our own [[Persona-based training matrix]].

* [Radical Servers](https://riseup.net/en/security/resources/radical-servers)

  A directory of dozens of radical server projects around the world where you can get free or low-cost email, chat, VPN, social media, and other anti-corporate services. The tools available to you on one or more of these servers can be used as drop-in replacements for the so-called "free" services offered by corporations funded by surveillance capitalism, such as GMail, Facebook, Twitter, OneDrive, Dropbox, and so on. See also [LibreProjects.net](http://libreprojects.net/) for another view of the same information, and [AlternativeTo.net's "Open Source Self-Hosted" directory](https://alternativeto.net/platform/self-hosted/?license=opensource) for details about the free software powering these anti-corporate services, themselves.

# Other lists

* [awesome-android-security](https://github.com/ashishb/android-security-awesome)
* [awesome-appsec](https://github.com/paragonie/awesome-appsec)
* [awesome-ctf](https://github.com/apsdehal/awesome-ctf)
* [awesome-forensics](https://github.com/Cugu/awesome-forensics)
* [awesome-hacking](https://github.com/Hack-with-Github/Awesome-Hacking)
* [awesome-honeypots](https://github.com/paralax/awesome-honeypots)
* [awesome-incident-response](https://github.com/meirwah/awesome-incident-response)
* [awesome-infosec](https://github.com/onlurking/awesome-infosec)
* [awesome-lockpicking](https://github.com/meitar/awesome-lockpicking)
* [awesome-malware-analysis](https://github.com/rshipp/awesome-malware-analysis)
* [awesome-osint](https://github.com/jivoi/awesome-osint)
* [awesome-pcaptools](https://github.com/caesar0301/awesome-pcaptools)
* [awesome-pentest](https://github.com/enaqx/awesome-pentest)
* [awesome-pentest-cheat-sheets](https://github.com/coreb1t/awesome-pentest-cheat-sheets)
* [awesome-reversing](https://github.com/tylerph3/awesome-reversing)
* [awesome-sec-talks](https://github.com/PaulSec/awesome-sec-talks)
* [awesome-vehicle-security](https://github.com/jaredthecoder/awesome-vehicle-security)
* [awesome-web-security](https://github.com/qazbnm456/awesome-web-security)
* [awesome-windows-domain-hardening](https://github.com/PaulSec/awesome-windows-domain-hardening)
* [Aman Hardikar's mindmaps](http://www.amanhardikar.com/mindmaps.html)
* [NetSec Focus - Learning Resources](https://docs.google.com/spreadsheets/d/1TD8KTRXvXwy1yU6s7Nz_JuNh7b7fa7pINZuHOVjtAAg/htmlview)
* [MalwareAnalysis.Tools](http://malwareanalysis.tools/)
* [Sneakerhax's Getting Started Resources](https://github.com/sneakerhax/Resources/blob/master/links/getting-started.md)

***

See also:

* related pages: [[Security culture]], [[PhySec]]
* [NYC-InfoSec.com](https://www.nyc-infosec.com/), a calendar of infosec-related events in the New York City area.
* [New York Security Community](http://nysec.isis.poly.edu/), an informal meetup of infosec professionals in NYC.