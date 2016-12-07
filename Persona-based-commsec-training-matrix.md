> 📝 Editor's note: This is a **work in progress**.
>
> The goal is to create a digital security training material that focuses on filling in the gaps of other guides and highlighting appropriate practices at certain levels of concern. There are three broad categories of "defenders" (you) and "attackers" (them) in increasing sophistication/resource requirements, creating a 3-by-3 matrix. This matrix is linearized below.
> 
> The process we're using to create this material:
> 
> 1. Add any/all security practices that fit the persona's risk level as line items in this list
> 1. Search for and link to appropriate existing guides/educational materials for the line item
> 1. Categorize the listed practices based on a "Z-axis" in a subsection of the persona heading
> 1. ~~Tabularize the information~~
> 1. Copy to the [[Security culture training#digital-security]] section, for now.

<table border="1" cellpadding="10" cellspacing="0">
  <tr>
    <th></th>
    <th></th>
    <th colspan="3"><a href="#attackers">Attackers</a></th>
  </tr>
  <tr>
    <th></th>
    <th></th>
    <th>Random Assholes</th>
    <th>Assholes with Resources</th>
    <th>The State</th>
  </tr>
  <tr>
    <th rowspan="3"><a href="#defenders">Defenders</a></th>
    <th>Individuals</th>
    <td>
      <a href="#individuals-vs-random-assholes">Individuals vs Random Assholes</a>
    </td>
    <td>
      <a href="#individuals-vs-assholes-with-resources">Individuals vs Assholes with Resources</a>
    </td>
    <td>
      <a href="#individuals-vs-the-state">Individuals vs The State</a>
    </td>
  </tr>
  <tr>
    <th>Organizers &amp; journalists</th>
    <td>
      <a href="#organizers--journalists-vs-random-assholes">Organizers &amp; journalists vs Random Assholes</a>
    </td>
    <td>
      <a href="#organizers--journalists-vs-assholes-with-resources">Organizers &amp; journalists vs Assholes with Resources</a>
    </td>
    <td>
      <a href="#organizers--journalists-vs-the-state">Organizers &amp; journalists vs The State</a>
    </td>
  </tr>
  <tr>
    <th>Targeted Activists</th>
    <td>
      <a href="#targeted-activists-vs-random-assholes">Targeted Activists vs Random Assholes</a>
    </td>
    <td>
      <a href="#targeted-activists-vs-assholes-with-resources">Targeted Activists vs Assholes with Resources</a>
    </td>
    <td>
      <a href="#targeted-activists-vs-the-state">Targeted Activists vs The State</a>
    </td>
  </tr>
</table>

# Personas

In the context of this resource, a "persona" is simply a coarse grouping of entities, divided into two opposing categories: "defenders" and "attackers." There are three defenders per persona category.

## Defenders:

A "defender" is a [persona](#personas) that roughly describes one "half" of a given threat model. Defenders in our framework are:

* **[Individuals](#individuals):** people responsible for themselves
* **[Organizers and journalists](#organizers-and-journalists):** people responsible for other people as well
* **[Targeted activists](#targeted-activists):** you know who you are

### Individuals

An "individual," for our purposes, is any person who is primarily concerned with *their own* privacy and security. This can be:

* A citizen of a country who uses social media to post about their mundane daily activities.
* An employee of a corporation who uses company resources (either hardware, software, or network infrastructure) to perform personal tasks such as banking, emailing, and so on.
* A member of an oppressed group who faces threats other individuals may not, such as a woman with a jilted ex-lover, an undocumented immigrant, people of color, queer youth, and so on.

### Organizers and journalists

An "organizer," for our purposes, is any person whose safety concerns extend to other people as well as themselves, for any reason. This notably includes "journalists" because, by definition, they are responsible for the safety of their source as well as themselves, but can also include other roles as well. Some examples of other social roles who our framework considered "organizers" include:

* System administrators responsible for maintaining the information systems of companies or community groups
* Community organizers (activists) who take some part in explicit political activity
* Individuals who engage in controversial subcultures and practices, despite not being "explicitly political" about it, such as people who run or simply participate regularly in LGBT or mental health support groups, and so on.

### Targeted activists

If you are a "targeted activist," you probably know who you are because you've self-identified yourself to yourself as one, and we'll just leave it at that.

## Attackers

A "defender" is a [persona](#personas) that roughly describes one "half" of a given threat model. Attackers in our framework are:

* **[Random Assholes](#random-assholes):** malicious individuals, harassers or unsophisticated mobs
* **[Assholes with Resources](#assholes-with-resources):** organized hate groups, rogue cops, more sophisticated / technical Random Assholes, more dedicated assholes (e.g. "jilted lovers" with resources)  
* **[The State](#the-state):** Governments, surveillance apparatus & multinational corporations (Wal-Mart, Apple+Google+Facebook, etc.)

### Random assholes

A "random asshole," for our purposes, is an individual or uncoordinated mob whose intent is to cause malicious harm. This can include:

* Twitter eggs, individual Trump supporters, and so on
* A (relatively *un*skilled) person who holds a grudge against you for some reason
* Racist co-workers
* Loosely coordinated mobs of trolls and hate-mongers such as Stormfront, "4chan," and so on

### Assholes with Resources

The ambiguous part of this persona is the "resources" part. This can mean a number of different things in practice, but the unifying thread is that there is some additional capability that these specific assholes have that "random assholes" don't. That distinction means that "assholes with resources" could be:

* A jilted ex-lover who happens to be an employee of a company such as Google or Facebook that has access to your personal information
* Technically skilled individuals with grudges
* Unethical app/web service developers, even and perhaps especially the "well-intentioned" ones
* Government or law enforcement employees (who are acting without formal backing from their agency) such as rogue cops
* Organized "cybercrime" groups who have some cyber-attack infrastructure in place for other means (botnet herders, phishers, and so on)

### The State

The our purposes, "The State" is an attacker persona that combines multinational corporations and governments, because corporations and governments tend to have similar if not identical resources and also often act in tandem/cooperation with one another to achieve their ends. This means that "The State" can, concretely, include entities such as:

* Advertising-funded corporations such as Google and Facebook
* "Vertically integrated" tech companies such as Apple
* Intelligence community organizations such as the CIA, NSA, and so on
* Surveillance companies/cyberweapon manufacturers, including intelligence community contractors

# "Z-axis" aspects:

> 🚧 TK-TODO: This parts needs a closer look:
> 
> 1. Read through the list, categorizing each line item along a "z-axis"
> 1. Group the line items according to their z-axis
>   * **What about line items matching more than one z-axis; place in both subheads or just the one?

* Technical: "Categories" from [PRISM-Break](https://prism-break.org/en/all/), i.e., what to do for server security versus what to do for device/endpoint security versus what to do for data in motion/at rest.
* Behavior/habitual: [data management](https://myshadow.org/) and/or security hygiene best practices
* Financial: issues relating specifically to currency systems (which are de-facto surveillance apparati by definition)

# Individuals vs. Random Assholes

## Data management

* Scrub personal data and [opt-out](https://www.privacyrights.org/data-brokers) from "[Data broker/vendor](https://www.privacyrights.org/consumer-guides/data-brokers-and-people-search-sites)" sites such as Spokeo/PeopleSearch/Pipl.com, etc.

## Security hygiene and habits

* Don't check in to places on Facebook/Foursquare/Yelp/etc publicly
* turn off location services (GPS) on your phone when you don't need it (also saves battery!)
* [Turn off location tagging for your smartphone camera](https://www.wired.com/2013/07/tip-smartphone-camera-gps/)
* Audit/improve your social network privacy settings
  * Verify friend requests with actual friends: When you get a Friend request from someone you don't know, but have mutual friends in common, send your mutual friend a private message asking for info about who the supposed person who may have sent the friend request actually is; avoids friending malicious/fake accounts.
* turn off "auto-pay" (and use Password Manager fill-in instead)

## Helpful tools

* Use a password manager (and all that that entails!)
  * Do the same for "password reset questions" (i.e., don't answer such questions honestly or with info that is posted to social media)

# Individuals vs. Assholes with Resources

## Security hygiene and habits

* Audit/revoke your social network account "Connected Apps" settings for apps you don't use
  * [For Twitter](https://myshadow.org/how-to-increase-your-privacy-on-twitter)
* Possibly put a [credit freeze](https://en.wikipedia.org/wiki/Credit_freeze) on your credit line at the three major credit
* Turn on "automatic updates" for software you use.
* Don't click on links in emails you didn't solicit yourself; when you get an email "from PayPal" asking to verify your account *close* the email, *open* a Web browser yourself, and *manually* type `paypal.com` into the address bar, yourself, don't just click the link.
* turn off "show remote images/content" and other "preview" features in your mail, RSS reader, etc apps
* Turn off auto-play on videos, etc.

## Helpful tools

* Adblockers (uBlock Origin, etc.)
* Clear cookies (cookie-clearing/whitelisting plugins)
* Signal (because of authentication, not just for encryption)
* Tape or a sticker over your webcam to frustrate video recording. (Cheap and easy!)
* Take a headset (headphones + microphone), chop off the wiring below the sensors, and plug that in to your headset jack to frustrate audio recordings.

# Individuals vs. The State

## Data management

* Encrypt your phone/laptop disk at rest (FileVault, Android Encryption, LUKS/cryptsetup)
* Make sure you read the privacy terms/terms of service/terms and policies of a service you sign up for. Remember, when you sign up for a online service, you are agreeing on a contract.
* Make sure you can actually delete your account after signing up and keep in mind that some services keep your data forever (even if you requested a deletion). You can use [Just delete me's](http://backgroundchecks.org/justdeleteme/) service so it warns you on how difficult is it to delete an account on the service you are currently browsing.
* Remember that using a service from a foreign country, you are subjected (in some terms) by their law, so make sure you go through the following check list (also make sure you do the same for your local service).
  1. Does the foreign/local service store your data in your country?
  1. Does the foreign/local service share any personal data with the government or any third party?
  1. Does the foreign/local service requires any personal data that may harm you in the future? If so, ask what they do with this information.
  1. Does the foreign/local service have any history with the government/police or any "privacy/corruption" scandal?
  1. Does the foreign/local service keep a [Canary Statement](https://en.wikipedia.org/wiki/Warrant_canary)? Check [Canary Watch](https://canarywatch.org) to see if your service is listed there, and if not, mail them asking if they keep such information public.

## Security hygiene and habits

* Use passphrases, not biometric unlock features such as fingerprints
* Use cash whenever possible, not a credit card or electronic payment system
* If you **need** to use credit-card to buy something (and you are currently based in US), use a random credit-card for each service. You can get that at [Privacy.com](https://privacy.com/).
* Switch your default search provider to a Google-alternative
* Uninstall the Facebook/Twitter/etc. apps and use the mobile web versions of these sites
* Use temporary emails/identities when making temporary use of services: use a [temporary email](https://temp-mail.org/en/) ([FakeMailGenerator.com](http://fakemailgenerator.com/) and similar sites) for that, and [fake names, birth dates and etc.](http://fakenamegenerator.com/) to go along with that temporary identity
* If possible, don't use hardware received from employer for personal use. (Why? "[Employee monitoring](https://www.privacyrights.org/consumer-guides/workplace-privacy-and-employee-monitoring).")
  * Similarly, never tell your boss/employer the passwords to personal accounts, even if "required" to by employment contracts (these clauses are illegal).
* Check the validity of the lock icon in your Web browser's address bar (TLS certificate validation practices)
* Don't use the default DNS your network provides, most of them are used for surveillance and profiling. Use [DNSCrypt](https://dnscrypt.org/) instead or the DNS provided by [OpenNIC Project](https://www.opennicproject.org/).

## Helpful tools

* Use [TermsOfService;Didn't Read](https://tosdr.org/) to get up-to-speed on legal terms for a given service you're considering using.
* Turn off JavaScript using blockers such as [ScriptSafe](https://chrome.google.com/webstore/detail/scriptsafe/oiigbmnaadbkfbmpbfijlflahbdbdgdf) and [NoScript](https://noscript.net/) and re-enable it only on sites you purposefully visit
* Use [HTTPS Everywhere](https://www.eff.org/https-everywhere%20) so you make sure you send data to the service using HTTPS and not HTTP.

# Organizers & journalists vs. Random Assholes

## Data management

* Use a [WHOIS privacy ("Domain privacy")](https://en.wikipedia.org/wiki/Domain_privacy) service (or, if you're okay taking the small risk, provide inaccurate WHOIS information)

## Security hygiene and habits

* 2FA (on your own accounts and, if you're running a group blog, on your blog site, etc.)

## Helpful tools

* Use OnionShare/TorBrowser or share.RiseUp.net to share files rather than public Dropbox/Google Docs, etc.

# Organizers & journalists vs. Assholes with Resources

## Security hygiene and habits

* Audit your webserver for information disclosure vulns ([a thorough treatment of webdev security things](https://github.com/FallibleInc/security-guide-for-developers)):
  * Turn off "directory listings" on your webserver
* Use alternatives to Google Docs such as pad.RiseUp.net or share.RiseUp.net, etc.
* Prevent spoofing of emails claiming to be from your domain by [implementing DKIM](https://scotthelme.co.uk/email-security-dkim/) for email services you provide
## Helpful tools

* On your server(s), use LetsEncrypt to enable TLS connections (for Web+Mail+any hosted service)
* Use Tor to hide your physical-world location
* Consider placing your own domain behind CloudFlare to hide your server's origin
* Replace Facebook (or other similar) group chats with secure messenger (e.g., Signal) group chats

# Organizers & journalists vs. The State

## Security hygiene and habits

* Use alternate service providers (don't use Google's GMail)
* Ideally, use *decentralized* alternate services/networks
  * Have a Jabber+OMEMO fallback for Signal (for the truly frightening case where Signal is censored)

## Helpful tools

* Use Tor!!!!!11!
* Host sites somewhere safe (privacytools.io)
* Consider [setting up an `.onion` service to access your site/domain](https://riseup.net/en/security/network-security/tor/onionservices-best-practices)
* Journalistic organizations should consider [SecureDrop](https://securedrop.org/)

# Targeted activists vs. Random Assholes

# Targeted activists vs. Assholes with Resources

* Use the "High" security level in your TorBrowser (disables JavaScript, HTML5 Web Fonts, etc.)
* [Use dedicated virtual machines for specific purposes](https://theintercept.com/2015/09/16/getting-hacked-doesnt-bad/) to open documents you don't trust, and take other specialized tasks

# Targeted activists vs. The State

## Helpful tools

* encrypted email (GPG)
* Use [Qubes](https://www.qubes-os.org/), a hardened and security compartmentalized operating system generally
* Use [Tails](https://tails.boum.org/) for handling specific, extremely sensitive material