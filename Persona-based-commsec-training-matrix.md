> 📝 Editor's note: This is a **work in progress**.
>
> The goal is to create a digital security training material that focuses on filling in the gaps of other guides and highlighting appropriate practices at certain levels of concern. There are three broad categories of "defenders" (you) and "attackers" (them) in increasing sophistication/resource requirements, creating a 3-by-3 matrix. This matrix is linearized below.
> 
> The process we're using to create this material:
> 
> 1. Add any/all security practices that fit the persona's risk level as line items in this list
> 1. Search for and link to appropriate existing guides/educational materials for the line item
> 1. Categorize the listed practices based on a "Z-axis" in a subsection of the persona heading
> 1. Tabularize the information and copy to the [[Security culture training#digital-security]] section, for now.

<table border="1" cellpadding="10" cellspacing="0">
  <tr>
    <th></th>
    <th><b>Random Assholes:</b><br />
      malicious individuals, harassers or unsophisticated mobs</th>
    <th><b>Assholes with Resources:</b><br />
      organized hate groups, more sophisticated / technical Random Assholes, more
      dedicated assholes ("jilted lovers" with resources), rogue cops
    </th>
    <th><b>Assholes in Power:</b><br />
      Governments, surveillance apparatus & multinational corporations (Wal-Mart,
      Apple+Google+Facebook, etc.)
    </th>
  </tr>
  <tr>
    <td><b>Individuals:</b><br />people responsible for themselves</td>
    <td>
      <a href="#individuals-vs-random-assholes">
        Individuals vs Random Assholes</a>
    </td>
    <td>
      <a href="#individuals-vs-assholes-with-resources">
        Individuals vs Assholes with Resources</a>
    </td>
    <td>
      <a href="#individuals-vs-assholes-in-power">
        Individuals vs Assholes in Power</a>
    </td>
  </tr>
  <tr>
    <td><b>Organizers &amp; journalists:</b><br />people responsible for other
      people as well</td>
    <td>
      <a href="#organizers--journalists-vs-random-assholes">
        Organizers &amp; journalists vs Random Assholes</a>
    </td>
    <td>
      <a href="#organizers--journalists-vs-assholes-with-resources">
        Organizers &amp; journalists vs Assholes with Resources</a>
    </td>
    <td>
      <a href="#organizers--journalists-vs-assholes-in-power">
        Organizers &amp; journalists vs Assholes in Power</a>
    </td>
  </tr>
  <tr>
    <td><b>Targeted Activists:</b><br />you know who you are</td>
    <td>
      <a href="#targeted-activists-vs-random-assholes">
        Targeted Activists vs Random Assholes</a>
    </td>
    <td>
      <a href="#targeted-activists-vs-assholes-with-resources">
        Targeted Activists vs Assholes with Resources</a>
    </td>
    <td>
      <a href="#targeted-activists-vs-assholes-in-power">
        Targeted Activists vs Assholes in Power</a>
    </td>
  </tr>
</table>


Defenders (columns):

* Individuals - people responsible for themselves
* Organizers & journalists - people responsible for other people as well
* Targeted activists - you know who you are

Attackers (rows):

* Random Assholes - malicious individuals, harassers or unsophisticated mobs
* Assholes with Resources - organized hate groups, more sophisticated / technical Random Assholes, more dedicated assholes ("jilted lovers" with resources), rogue cops
* Assholes in Power - Governments, surveillance apparatus & multinational corporations (Wal-Mart, Apple+Google+Facebook, etc.)

"Z-axis" aspects:

* Technical: "Categories" from [PRISM-Break](https://prism-break.org/en/all/), i.e., what to do for server security versus what to do for device/endpoint security versus what to do for data in motion/at rest.
* Behavior/habitual: "Don't click on links in email" and similar

# Individuals vs. Random Assholes

* Scrub personal data from Spokeo/PeopleSearch/Pipl.com, etc.
* Use a password manager (and all that that entails!)
* Don't check in to places on Facebook/Foursquare/Yelp/etc publicly
* turn off location services (GPS) on your phone when you don't need it (also saves battery!)
* [Turn off location tagging for your smartphone camera](https://www.wired.com/2013/07/tip-smartphone-camera-gps/)
* Audit/improve your social network privacy settings
* turn off "auto-pay" (and use Password Manager fill-in instead)

# Individuals vs. Assholes with Resources

* Adblockers (uBlock Origin, etc.)
* Clear cookies (cookie-clearing/whitelisting plugins)
* Signal (because of authentication, not just for encryption)
* Audit/revoke your social network account "Connected Apps" settings for apps you don't use
* Possibly put a [credit freeze](https://en.wikipedia.org/wiki/Credit_freeze) on your credit line at the three major credit
* Turn on "automatic updates" for software you use.

# Individuals vs. Assholes in Power

* Encrypt your phone/laptop disk at rest (FileVault, Android Encryption, LUKS/cryptsetup)
* Use passphrases, not biometric unlock features such as fingerprints
* Use cash whenever possible, not a credit card or electronic payment system
* Switch your default search provider to a Google-alternative
* Uninstall the Facebook/Twitter/etc. apps and use the mobile web versions of these sites

# Organizers & journalists vs. Random Assholes

* 2FA (on your own accounts and, if you're running a group blog, on your blog site, etc.)
* Use OnionShare/TorBrowser to share files rather than public Dropbox/Google Docs, etc.
* Use a [WHOIS privacy ("Domain privacy")](https://en.wikipedia.org/wiki/Domain_privacy) service (or, if you're okay taking the small risk, provide inaccurate WHOIS information)

# Organizers & journalists vs. Assholes with Resources

* On your server(s), use LetsEncrypt to enable TLS connections (for Web+Mail+any hosted service)
* Use Tor to hide your physical-world location
* Consider placing your own domain behind CloudFlare to hide your server's origin
* Audit your webserver for information disclosure vulns:
  * Turn off "directory listings" on your webserver

# Organizers & journalists vs. Assholes in Power

* Use Tor!!!!!11!
* Host sites somewhere safe (privacytools.io)
* Consider setting up an `.onion` service to access your site/domain
* Don't use gmail

# Targeted activists vs. Random Assholes

# Targeted activists vs. Assholes with Resources

# Targeted activists vs. Assholes in Power

* encrypted email (GPG)
