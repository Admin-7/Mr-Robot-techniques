> [[Wiki|Home]] ▸ [[Activities and events]] ▸ [[Trivia night]] ▸ **How to facilitate Trivia night**

Thanks for volunteering to facilitate Trivia night!

Trivia night is a digitized equivalent of a classic bar trivia game.

1. [Goals](#goals)
1. [Variations](#variations)
1. [Requirements](#requirements)
1. [Checklist](#checklist)
1. [Suggested questions](#suggested-questions)

# Goals

> 🚧 TK-TODO

# Variations

The FBCTF platform provides numerous options and settings to play games in a variety of ways. Depending on the physical-world context, some variations will be infeasible to play. For example, Trivia night played at an *actual bar* will mean most participants only have access to smartphones, not laptops, which cannot interact with the FBCTF interface. In this context, use the [classic bar trivia](#classic-bar-trivia) variation.

## Classic bar trivia

In this variation

* teams are directed to an Etherpad or other shared document editing tool,
* there are no bonuses for first or fast captures (successful answers),
* questions are announced and enabled in the game interface individually, as "rounds."

# Requirements

The following equipment is needed for a successful Trivia night:

* [ ] The [FBCTF](https://github.com/facebook/fbctf) platform exposed to the event venue's LAN; the FBCTF "Quiz Levels" ([see the Admin Guide](https://github.com/facebook/fbctf/wiki/Admin-Guide)) are the night's Trivia Questions.
* [ ] A projector or large screen (large enough for easy viewing by a group of 20 or so).
* [ ] Adapter cabling for the A/V setup, if necessary.
* [ ] Access to decent Wi-Fi; the digital scorecards are accessed over the venue's WLAN to the trivia server (FBCTF server).
* [ ] A list of [prepared trivia questions](#suggested-questions), complete with:
    * [ ] Point values per question
    * [ ] Optionally, a single hint for each question
    * [ ] Optionally, a hint penalty in points for each question's hint

# Checklist

## T-1 day

1. Create a FBCTF server for the evening. For example, using [FBCTF's standard Vagrant startup](https://github.com/facebook/fbctf/wiki/Quick-Setup-Guide#standard-vagrant-startup):
    ```sh
    git clone https://github.com/facebook/fbctf.git
    cd fbctf
    source ./extra/lib.sh
    quick_setup start_vagrant prod
    ```
1. Login as the `admin` user. Passwords are automatically generated when provisioning a new server and are reported on `stdout` when doing so. Be sure you save the generated password or you may need to re-provision the server.
1. Set the Game Configuration options:
    1. Set Registration options:
        1. Turn registration *ON*.
    1. Set Game options:
        1. **Default bonus**: `0`
        1. **Default bonus dec**: `0`
    1. Set Branding options:
        1. Turn on *Custom Logo* (because we don't really care to advertise for Facebook, now do we?)
        1. Set Custom Organization to the name of the venue at which the event is played.
        1. Set the Custom Byline to something of your choosing.
1. Define the [Quiz ("Trivia") questions](#suggested-questions):
    1. Enter the trivia questions as Quiz Levels in the admin interface.
1. Ensure all Quiz Levels are set to *OFF*.

## T-60 minutes

1. Connect the FBCTF server computer to the digital projector.

### Standard setup

1. Make the FBCTF server available to the event's WLAN if not already done. For example:
    1. Forward the host's port `8443` to the guest's port `443`.

### Bar setup

> TK-TODO

## T-30 minutes

1. Turn Scoring *ON* in the admin interface.

### Standard setup

1. Advertise the game system to the event venue. For example, shout:
    > Hey everyone, we'll be hosting Trivia night; to play, point your web browser on your laptop or phone to `https://<THE_IP_ADDRESS_HERE>:8443` and don't worry about the certificate error. ;)
1. Encourage everyone to register a team of their own or join up with (sit next to?) players in a fellow team.

### Bar setup

1. Advertise the game to the event venue. For example, shout:
    > Hey everyone, we'll be hosting Hacker Trivia night! We'll be coming 'round to ask you for your team names. If you wanna play, just send an email from the email you told us about to `$CHOSEN_EMAIL_HERE`.
1. In a new browser tab, load an email interface, such as one of the [[disposable email services]].

## T-0

1. Click on *Begin Game* in the admin interface.
1. When the game admins are ready to ask the first question, enable the first Quiz level, lather rinse and repeat.

# Suggested questions

> 📝 As the headline implies, these are suggestions. Feel free to use your own. :)
> 
> When editing this list, please retain the quiz format:
>
> ```
> ## Quiz title
> 
> Quiz question?
> 
> * Answer: `The answer. (Case insensitive.)`
> * Points: `Numeric point value`
> * Bonus: `Numeric bonus point value`
> * Bonus-Dec: `Numeric bonus decrement point value`
> * Hint: `A helpful hint.`
> * Hint Penalty: `Numeric penalty in points for accessing the hint`
> * Factoid: An interesting fact or other neat thing to know about why the answer is correct.
> ```
>
> 🔰 If you cannot edit this page, suggest a new question to us by [posting a new issue](https://github.com/AnarchoTechNYC/meta/issues/new).

## Weasel words

Which of the following are email providers that automatically and by default encrypt all of your outgoing email?

A) GMail  
B) RiseUp  
C) ProtonMail  
D) Mailinator  
E) None of the above  
F) All of the above  

* Answer: `E`
* Points: `15`
* Bonus: `0`
* Bonus-Dec: `0`
* Hint: `"Automatically and by default" means the original, 'factory settings' configuration of the service. "All outgoing email" means email that gets copied to your Sent folder.`
* Hint Penalty: `5`
* Factoid: No existing service (known to the game organizer) automatically encrypts email to all possible recipients because standards for encrypted email communications require the prior exchange of public keys. ProtonMail, too, will not encrypt email you send to non-ProtonMail users unless you manually perform the encryption process yourself using an add-on like [Mailvelope](https://mailvelope.com/). There is an emerging standard called [AutoCrypt](https://autocrypt.org/) that attempts to solve this problem in a vendor-neutral manner.

## "Aren't you worried about Signal not being secure?"

Under what conditions would the [Signal Private Messenger](https://signal.org/) app not be able to protect the confidentiality of your messages?

A) Device compromise  
B) Legal subpoena  
C) Network eavesdropping  
D) Compromised Signal server  
E) Rogue Signal server  
F) Signal servers go down  

* Answer: `A`
* Points: `25`
* Bonus: `0`
* Bonus-Dec: `0`
* Hint: `What is "end-to-end encryption" for?`
* Hint Penalty: `10`
* Factoid: Signal is an app for smartphones famous for its invention of [the Signal Protocol](https://en.wikipedia.org/wiki/Signal_Protocol), which standardized  "end-to-end encryption" across popular Communication Service Providers (CSPs) like Facebook. End-to-end encryption is like putting an envelope around your messages, which helps protect against people reading the message while it is being delivered. However, an envelope will not protect against someone who watches from over your shoulder as you write the message (i.e., as you type the message on your endpoint device), which is akin to how a device compromise works. If malware is already running on your specific phone, the malware on your device can read your messages while they are still unencrypted in the Signal app's memory space.

## FU HODL GANG

In what year was the first commercial digital currency company founded?

* Answer: `1990`
* Points: `5`
* Bonus: `0`
* Bonus-Dec: `0`
* Hint: `The same technology that makes BitCoin addresses possible, public key encryption, was used in this early attempt as well.`
* Hint Penalty: `3`
* Factoid: Intrepid academic cryptographer [David Chaum founded his own company called DigiCash in 1990](https://en.wikipedia.org/w/index.php?title=Digital_currency&oldid=846948568#History). DigiCash was known as "e-cash" at the time and used public key cryptography to assign addressees to transactions, in very much the same process that BitCoin addresses are generated today.

## Easy Dox

You get a disappearing Signal message from your friend informing you of a new "alt-right" group whose website claims it is active in your neighborhood. Your friend wants to know the legal identities of the site operators. What is the first tool you run?

* Answer: `whois`
* Points: `25`
* Bonus: `0`
* Bonus-Dec: `0`
* Hint: `Who is the registered domain owner?`
* Hint Penalty: `15`
* Factoid: The [`whois` utility ](https://explainshell.com/explain/1/whois) is a command-line program that looks up the names of people responsible for maintaining certain Internet resources, such as a domain name or IP address. Naive Website administrators will neglect to hide their legal information from the global WHOIS database, which they register with when reserving a domain name.

## What's in a lock icon?

When your Web browser displays a healthy green lock icon near the address bar, indicating that certain portions of your Web browsing activity have been "secured," which of the following are nevertheless visible to a passive, third-party eavesdropper?

A) The entire URL you are loading.  
B) The page contents.  
C) Your IP address.  
D) The page contents and your IP address.  
E) The Web browser you are using.  
F) The domain name of the site you are visiting and your IP address.

* Answer: `F`
* Points: `25`
* Bonus: `0`
* Bonus-Dec: `0`
* Hint: `The lock icon signifies the use of HTTPS, which indicates the use of TLS to encapsulate HTTP protocol traffic. What must remain unencrypted on the outside of the TLS wrapper in order for your Web browser to receive a sensible reply?`
* Hint Penalty: `10`
* Factoid: The lock icon in Web browsers signify that your request to view a given webpage, and the webpage itself was delivered to you, inside a locked package. However, you must still write the address (the domain name) of the website that you want to view on the outside of the package, or the delivery system known as the Internet cannot ferry your request to the website, nor the website's response back to you, successfuly. This means a passive third-party can learn which domain names you're visiting regardless of whether those domains have a lock icon or not in your Web browser window.

## Rumpelstiltskin

The three inventors of this critical technology had the initials RR, AS, and LA. What first name does the "L" refer to?

* Answer: `Leonard`
* Points: `25`
* Bonus: `0`
* Bonus-Dec: `0`
* Hint: `An equivalent technology was independently invented by a second trio about a decade prior but was classified for many years.`
* Hint Penalty: `10`
* Factoid: The [RSA cryptosystem](https://en.wikipedia.org/wiki/RSA_%28cryptosystem%29), the most ubiquitous public-key cryptography algorithm used today and published way back in 1977, was authored by Ron Rivest, Adi Shamir, and *L*eonard Adleman. However, a second trio that included James H. Ellis, Clifford Cocks, and Malcolm Williamson, working for the United Kingdom's national intelligence agency, the Government Communications Headquarters (GCHQ), independently developed effectively equivalent algorithms as early as 1970. Their report, [titled "The Possibility of Non-Secret Digital Encryption,"](https://www.gchq.gov.uk/sites/default/files/document_files/CESG_Research_Report_No_3006_0.pdf), was classified at the time of Rivest, Shamir, and Adleman's publication, cementing the academics' place in history and forever overshadowing the government employees' fame.

## TOS;DR

You are creating your profile on a hip, new dating site. You prefer to fudge the facts on some of the profile fields (age, weight, etc.) when asked. What is the strictest possible legal penalty you could face if your embellishments are discovered by an overzealous government prosecutor (i.e., District Attorney)?

A) Misdemeanor conviction  
B) Felony conviction and 5 years  
C) Felony conviction and 10 years  
D) Felony conviction and 20 years  
E) You must pay a fine  
F) Account suspension

* Answer: `D`
* Points: `15`
* Bonus: `0`
* Bonus-Dec: `0`
* Hint: `Supplying fake information in the process of using a computer system may legally constitute computer fraud.`
* Hint Penalty: `6`
* Factoid: Most websites gleefully accept whatever information you provide for your profiles, and even the strict ones (Facebook names, anyone?) tend not to rise to the level of a legal suit. However, the fine print in the Terms of Service clauses of almost every website forbid misrepresenting yourself or your information to the site, creating a legal cascade effect that can lead all the way to a Computer Fraud and Abuse Act (CFAA) violation, which is a felony carrying a maximum sentence of 20 years in prison under the harshest conditions. This is a prime example of the regime of universal criminality plaguing contemporary technology law, a [regime that the United States Department of Justice regularly attempts to strengthen](https://www.cnet.com/news/doj-lying-on-match-com-needs-to-be-a-crime/).

## Ogres are like onions

In the Tor onion routing scheme, a packet must traverse a minimum number of Tor servers (a "hop") in order to protect both the sender (its source) and the receiver (the destination) from eavesdroppers outside of the Tor network and within the network itself. What is the minimum number of hops through the Tor network a packet must take in order to have this quality of protection?

* Answer: `3`
* Points: `30`
* Bonus: `0`
* Bonus-Dec: `0`
* Hint: `How many different types of Tor nodes are there?`
* Hint Penalty: `15`
* Factoid: The Tor network is a kind of "mix network," or [mixnet](https://en.wikipedia.org/wiki/Mix_network), which accepts incoming packets from many sources and jumbles them together before returning them to the regular Internet (known as the "clearnet"), so that it's difficult to tell which sender sent which outgoing message. In order for the Tor network itself to be unaware of a given packet's sender and receiver, the packet must traverse at least three independent Tor servers. These are known as the entry node, the middle or relay node, and the exit node. In this construction, the entry node is aware of the packet's source, but not its destination. The middle node is unaware of both the packet's source and its destination. The exit node is aware of the packet's destination, but not its source. Using this three-hop scheme, no single Tor server participating in the network is aware of both the source and the destination of any given packet being carried by the network.

## VPN vs. Tor

For reasons, you require an extraordinarily secure and anonymous connection to the public Internet. At your disposal is the Tor network, a VPN provider, and a C2 (Command and Control) server you can use for any purpose. Which of the following configurations do you use for maximum security and the highest anonymity guarantees to build your connection?

A) VPN only; VPNs are safer than Tor  
B) Tor only; Tor is safer than a VPN  
C) Both: connect to the VPN first, then anonymize your connection through Tor  
D) Both: connect to Tor first, then secure your connection through the VPN  
E) Both, plus a Tor bridge on the C2 server: connect to the Tor bridge first, then the Tor network, then the VPN  
F) Neither VPN or Tor; there are far better tools available

* Answer: `E`
* Points: `30`
* Bonus: `0`
* Bonus-Dec: `0`
* Hint: `It's not paranoia if they're really out to get you.`
* Hint Penalty: `10`
* Factoid: A VPN, or Virtual Private Network, is not intended to offer anonymity to its users. It merely offers safe passage to a destination across an unsafe pathway. On the other hand, Tor is not intended to provide safe passage, merely anonymity. Therefore, for the highest security guarantees, you should use both Tor and a VPN. However, the order is important. If you connect to the VPN before you connect to Tor, then the VPN provider knows who you are because Tor has not yet gotten a chance to anonymize you. Meanwhile, anyone watching you can see that you're connecting to Tor. For this reason, you should use a Tor bridge, which is a server designed not to look like a Tor server, then use that to connect to Tor first so that your connection is anonymized, then exit the Tor network destined for the VPN server, and finally use the VPN to connect to your ultimate destination.

## Little Bobby tables

You get a frantic call from your friend who runs a campaign website saying that their homepage has been replaced with a hateful message. During your forensic analysis of the victim site's Web server logs, you see the following snippet:

```
200.123.45.67 - - [02/Jul/2018:22:07:14 -0500] "GET / HTTP/1.1" 200 487
200.123.45.67 - - [02/Jul/2018:22:22:02 -0500] "GET /index.aspx?page=contact HTTP/1.1" 200 23049
200.123.45.67 - - [02/Jul/2018:22:22:24 -0500] "GET /index.aspx?page=' HTTP/1.1" 500 23513
200.123.45.67 - - [02/Jul/2018:22:22:09 -0500] "GET /index.aspx?page=' or 1=1--  HTTP/1.1" 200 23381
29.231.97.105 - - [02/Jul/2018:22:18:56 -0500] "GET / HTTP/1.1" 200 487
29.231.97.105 - - [02/Jul/2018:22:19:23 -0500] "GET /index.aspx?page=contact HTTP/1.1" 200 23049
```

Based on this log snippet, what is the most salient course of action you should advise your friend to take?

A) Fix the homepage, but there is no other action needed because the cross-site scripting (XSS) attack is temporary.

B) Fix the homepage and reset all user passwords because the SQL injection attack may have comrpomised the site's database.

C) Completely wipe the server and rebuild the database and website from from a backup, because the SQL injection attack has likely granted the attacker full control over the website.

D) Completely wipe the server, patch the `index.aspx` script, rebuild the database and website from a backup, and send emails to every subscribed user informing them that their user account details may have been leaked, because the SQL injection attack has likely granted the attacker full control over the website.

E) Restore the website files from a recent backup to fix the homepage, and then change all user passwords, but retain the current database.

F) Fix the homepage and then change hosting providers because the host you are using is vulnerable to HTML injection attacks.

* Answer: `D`
* Points: `35`
* Bonus: `0`
* Bonus-Dec: `0`
* Hint: `At what line in the log is the first indication of an error present?`
* Hint Penalty: `15`
* Factoid: This logfile is an Apache common log format snippet that shows two different clients, one coming from IP address 200.123.45.67 and the other coming from 29.231.97.105, browsing the website. Every request succeeds with a `200` error code (the second to last number in the log file's lines), except for line 3 in the snippet, which shows a Web server error (HTTP error code 500). The requested URL at this line ends in an apostrophe (`'`), a common [SQL injection](https://en.wikipedia.org/wiki/SQL_injection) probe. The next request shows a successful SQL injection by adding `or 1=1-- ` to the URL. Successful SQL injection attacks can completely take over a vulnerable server, meaning that the attacker effectively has administrative access to the entire Website and possibly also the computer on which the website is hosted. This severity of compromise calls for a complete wipe of the affected server and a careful rebuild after patching the discovered vulnerability. 
