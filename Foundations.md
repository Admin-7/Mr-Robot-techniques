> [[Wiki|Home]] ▸ :beginner: **Foundations**

Our *Foundations* pages are designed to help you get up to speed quickly, or fill in gaps in fundamental knowledge areas. These explanations assume you have no prior knowledge or experience. Pair these pages with a [suggested learning path](#suggested-learning-path).

* [[BitTorrent]]
* [[Bytes]]
* [[Command line interface (CLI)]]
* [[Configuration file]]
* [[Cryptographic hash]]
* [[DDoS]]
* [[DHCP]]
* [[Dark Web (dark net)]]
* [[Graphical user interface (GUI)]]
* [[Hash algorithms|Cryptographic hash]]
* [[Hidden files or folders ("dotfiles")]]
* [[IP address]]
* [[Internet]]
* [[Internet Service Provider (ISP)]]
* [[Malware]]
* [[Manual pages (man pages)]]
* [[Open source]]
* [[Operating System]]
* [[Password cracking]]
* [[passwd file]]
* [[SQL injection]]
* [[Salted hash]]
* [[Servers]]
* [[Secure Shell (SSH)]]
* [[Shell]]
* [[Terminal]]
* [[Transport Layer Security (TLS)]]
* [[Tor]]
* [[Torrents]]

See also: [[Glossary]].

# Contents

1. [Suggested learning path](#suggested-learning-path)
    * [System administration](#system-administration)
    * [General programming](#general-programming)
    * [Web development](#web-development)
    * [Information security](#information-security)

# Suggested learning path

If you don't know where to start *and* don't really know where to go in your studies next, consider starting here:

1. [Code: The Hidden Language of Computer Hardware and Software](http://www.charlespetzold.com/code/) - How can a metal box emulate intelligent capabilities like decision making, memory and recollection of past events, or general problem-solving? This book answers that question by starting at the very beginning, which turns out not to be that long ago. Inside a computer, there are only two words, "yes" and "no," yet this is enough to express a bewildering range of ideas and activities. And what is a computer "word?" This book explains it, and does it very well. Read this before you read anything else.

## System administration

Sometimes also referred to as "DevOps" or [Site Reliability Engineering (SRE)](https://landing.google.com/sre/books/) these days, system administration is the practice of utilizing computer systems as infrastructural tooling to support the work of others who need to use those systems. System administrators ensure that information technology systems are available for use and are operating within acceptable parameters. Therefore, a system administrator is sometimes also referred to as a "system operator" or "sysop" for short. It is our collective's belief that this area of skill is among the most, if not *the* most, important area for radical technologists to develop.

1. [Servers For Hackers](https://serversforhackers.com/) - One of the basic building blocks of any digital infrastructure is the [[server|Servers]], literally a machine that services requests that are made of it. What that machine actually is, and what services it actually offers, is up to the system administrator to define, deploy, and maintain. This book takes a practical approach to configuring servers from their Operating System up to the applications running atop them, and goes in-depth on numerous popular programs like the Nginx HTTP server that provide services such as Web site publishing that almost every organization needs.
1. [Ops School](https://opsschool.org/) - Comprehensive curriculum designed to help you learn to be an operations engineer (a newer term for "system administrator").
1. [Ansible for DevOps](https://www.ansiblefordevops.com/) - Once a server is running ("provisioned"), it must be monitored to ensure that it keeps running. It must be protected from security vulnerabilities. Its data must be backed up to guard against disaster scenarios in which you (and your comrades) lose all your work. This is a lot of work when performed manually, especially as the number of servers you need to maintain increases. With Ansible, however, you can describe your digital infrastructure and the procedures you use for managing it as a set of text files ("playbooks") that can be automatically run through at your command, massively simplifying the process of provisioning, maintaining, patching, and monitoring large server fleets.
1. [Kubernetes in Action](https://www.manning.com/books/kubernetes-in-action)

## General programming

In general, programming is the art of describing something about how the world is, or how you would like to see the world be in the future. Much like writing a book, this is a creative, generative process that requires as much imagination as it does logical and objective reasoning. This is why we (all used to) say that programs are "written," not "built." There is immense power in the ability to write computer programs, but be careful not to mistake this ability for an understanding of the environment in which those programs run. The latter is system administration, and our collective believes it is both more immediately useful and politically impactful to gain sysadmin skills than to join the ever-increasing ranks of computer programmers. That said, sysadmins benefit greatly from being able to act within a programmer's mindset and paradigm, so here we present a heavily curated list of resources useful for growing—but not starting out—as a programmer.

1. [Exercises in Programming Style](http://www.amazon.com/Exercises-Programming-Style-Cristina-Videira/dp/1482227371/) - A [companion code repository](https://github.com/crista/exercises-in-programming-style) is on GitHub.

## Web development

Web development ("[[WebDev]]") is a general term that describes the process of creating a Web site or Web application for publication on the Internet or for private use within an organization's intranet. Be careful not to confuse Web development with architecting digital infrastructure more generally; Web development can result in the creation of tools such as event calendars (like Google Calendar), contact lists (like Facebook friend lists), group chats (like Slack), or media streaming sites (like Spotify), but each of these capabilities can be accomplished without Web sites. For this reason ([[among others|Coding bootcamps considered harmful]]), we intentionally avoid focusing on Web development as a core skill.

Nevertheless, the ubiquity of Web technologies such as HTML, CSS, and JavaScript means that a working knowledge of WebDev foundations can be very useful. Here, we present a heavily curated ordered list of suggested reading material to jumpstart your capabilities in this area.

1. [Foundation Website Creation](https://www.worldcat.org/title/foundation-website-creation-with-css-xhtml-and-javascript/oclc/646766089) - Before you read any other Web development resource, read chapters 4, 5, and 6 of this book. Ignore the other chapters (as they focus primarily with business considerations and [general programming](#general-programming) information). These chapters will lay a foundation that is almost always missing from other reosurces on the topic.
1. [AdvancED CSS](https://www.worldcat.org/title/advanced-css/oclc/500470223)
1. [The New CSS Layout](https://abookapart.com/products/the-new-css-layout)

## Information security

Information security ("[[InfoSec]]") is the practice of protecting (possibly very sensitive) information from unauthorized or unintentional access, modification, or outright destruction. Our collective's work is atypical in that we make every attempt to discuss security-related concepts and considerations inline at every opportunity, which supports our [Train the Trainers](https://github.com/AnarchoTechNYC/meta/blob/master/train-the-trainers/README.md) project. Nevertheless, we also offer a learning path and study guide for those interested in developing their InfoSec skills, specifically.

See [[Getting started on InfoSec]] for InfoSec learning path recommendations.