> [[Wiki|Home]] ▸ [[Activities and events]] ▸ **Defense Against the Dark Arts**

* Tagline: Duel your classmates in cyberspace by both defending and attacking networks and devices with "live fire" (but simulated) tools and techniques.
* Description: Practice defending against and executing a specific real-world threat in a live (but simulated) duel against your classmates. If you can set up a new email account, you can learn how to set up a network, service, or device as well as how to hack into it. In each session, we'll demystify a specific threat (network monitoring, password recovery, web app compromise, etc) by pairing off into groups and switching between one of two roles: "attacker" or "defender." Defenders are tasked with configuring one or more services, devices, or networks to withstand cyber attacks, while attackers will be tasked with breaching and/or exfiltrating data from those services, devices, or networks. After a short time, attackers become defenders and defenders become attackers, and the duels repeat, so everyone gets a chance to be both an attacker and defender. This is not about winning or losing, but rather sparring in a digital arena to better understand the terrain, expand your capabilities in it, and become an expert at both offensive and defensive magics.

> 🚧 TK-WORK IN PROGRESS: I'm not certain how this format should go, yet. There are many [[CTFs|InfoSec#ctfs-and-hacking-games]] that we could join, but those don't typically require us to *set up* our own infrastructure. The point of *defense* against the dark arts is to do exactly that: learn how to harden and protect our own communities, not just how to go on the offense. So, I'm of two minds. Either:
> 
> * we have somewhat longer classes for one group to set up and the other group to prepare attacks, or
> * we split into groups and *only* set up some infrastructure, then "attack" the other team's infrastructure in the time between the session and the next session

# Exercise ideas

This is a scratchpad of exercise ideas. Specific exercises/classes/sessions should get their own (sub)page.

* Sniffing open Wi-Fi:
  * Answers questions like:
    * "Why should I check for the lock icon in my browser?"
    * "How do I set up a Wi-Fi network securely?"
    * "What is the problem with WPS?"
    * "How do I get started with network sniffing?"
  * Possible tools:
    * Wireshark
    * OpenWRT/alternate router firmware
    * consumer routers generally: firmware updates, etc. (for example, reference CVE-2014-9583)
* Auditing online account password strength:
  * Answers questions like:
    * "How do I know if my password is good enough?"
    * "How can I make sure that my group's members are using good passwords?"
    * "What happens if an account is 'compromised' and what impact could this have on other users?"
  * Possible tools:
    * Using Hydra to brute-force logins
* Phishing emails:
  * Answers questions like:
    * "Why should I be careful when I click links in email?"
    * "Why are email attachments dangerous?"
    * "If I just use webmail instead of an app, am I safe?"
    * "How can I tell if email is real, and not a fake?"
  * Possible tools:
    * `recon-ng`, Maltego, etc.
    * SET for sending spoofed email (or SMS, etc.)
* Compromising a simple group website
  * Answers questions like:
    * "How do I stop my my group's site from getting hacked?"
  * Possible tools:
    * CMS scanners such as `wpscan` to quickly scan for vulnerabilities on a group website
* …?