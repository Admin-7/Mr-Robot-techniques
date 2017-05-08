> [[Wiki|Home]] ▸ [[Security culture]] ▸ [[Persona-based training matrix]] ▸ **Security training: Individuals versus The State**

<table border="1" cellpadding="10" cellspacing="0">
  <caption>
    <p>How to use this persona-based threat modeling matrix:</p>
    <ol>
      <li>You are a "defender" (a given row). Find yourself there.</li>
      <li>Your concern(s) map to a given "attacker" (a given column). Find your attacker.</li>
      <li>Find the cell at which these two personas intersect. Everything listed in the cells above and to the left of your cell applies to you, too.</li>
      <li>Start at the top-left cell and read the advice from left-to-right, top-to-bottom, until you reach your cell. Then stop worrying. :)</li>
    </ol>
  </caption>
  <tr>
    <th></th>
    <th></th>
    <th colspan="3">[[Attackers|Persona-based training matrix#attackers]]</th>
  </tr>
  <tr>
    <th></th>
    <th></th>
    <th>[[Random Assholes|Persona-based training matrix#random-assholes]]</th>
    <th>[[Assholes with Resources|Persona-based training matrix#assholes-with-resources]]</th>
    <th>[[The State|Persona-based training matrix#the-state]]</th>
  </tr>
  <tr>
    <th rowspan="3">[[Defenders|Persona-based training matrix#defenders]]</th>
    <th>[[Individuals|Persona-based training matrix#individuals]]</th>
    <td>
      [[Individuals vs Random Assholes|Security training: Individuals versus Random Assholes#individuals-versus-random-assholes]]
    </td>
    <td>
      [[Individuals vs Assholes with Resources|Security training: Individuals versus Assholes with Resources#individuals-versus-assholes-with-resources]]
    </td>
    <td>
      <strong>Individuals vs The State</strong>
    </td>
  </tr>
  <tr>
    <th>[[Organizers and Journalists|Persona-based training matrix#organizers-and-journalists]]</th>
    <td>
      [[Organizers &amp; Journalists vs Random Assholes|Security training: Organizers and Journalists versus Random Assholes#organizers-and-journalists-versus-random-assholes]]
    </td>
    <td>
      [[Organizers &amp; Journalists vs Assholes with Resources|Security training: Organizers and Journalists versus Assholes with Resources#organizers-and-journalists-versus-assholes-with-resources]]
    </td>
    <td>
      [[Organizers &amp; Journalists vs The State|Security Training: Organizers and Journalists versus The State#organizers-and-journalists-versus-the-state]]
    </td>
  </tr>
  <tr>
    <th>[[Targeted Activists|Persona-based training matrix#targeted-activists]]</th>
    <td>
      [[Targeted Activists vs Random Assholes|Security training: Targeted Activists versus Random Assholes#targeted-activists-versus-random-assholes]]
    </td>
    <td>
      [[Targeted Activists vs Assholes with Resources|Security training: Targeted Activists versus Assholes with Resources#targeted-activists-versus-assholes-with-resources]]
    </td>
    <td>
      [[Targeted Activists vs The State|Security training: Targeted Activists versus The State#targeted-activists-versus-the-state]]
    </td>
  </tr>
</table>

# Individuals versus The State

## Prerequisites

Before you dive too deeply into this practice material, you should first explore the following lower-hanging fruit in the following order:

1. [[Security training: Individuals versus Random Assholes]]
1. [[Security training: Individuals versus Assholes with Resources]]

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
* Use passphrases for locking your phone instead of PIN or Pattern.
* Use cash whenever possible, not a credit card or electronic payment system
* If you **need** to use credit-card to buy something (and you are currently based in US), use a random credit-card for each service. You can get that at [Privacy.com](https://privacy.com/).
* Switch your default search provider to a Google-alternative
* Uninstall the Facebook/Twitter/etc. apps and use the mobile web versions of these sites
* [Audit your Android device's app permissions](http://www.howtogeek.com/230683/how-to-manage-app-permissions-on-android-6.0/) and revoke any permissions granted to apps that enable features you don't use
* Use temporary emails/identities when making temporary use of services: use a [temporary email](https://temp-mail.org/en/) ([FakeMailGenerator.com](http://fakemailgenerator.com/) and similar sites) for that, and [fake names, birth dates and etc.](http://fakenamegenerator.com/) to go along with that temporary identity
* If possible, don't use hardware received from employer for personal use. (Why? "[Employee monitoring](https://www.privacyrights.org/consumer-guides/workplace-privacy-and-employee-monitoring).")
  * Similarly, never tell your boss/employer the passwords to personal accounts, even if "required" to by employment contracts (these clauses are illegal).
* Check the validity of the lock icon in your Web browser's address bar (TLS certificate validation practices)
* Don't use the default DNS your network provides, most of them are used for surveillance and profiling. Use [DNSCrypt](https://dnscrypt.org/) instead or the DNS provided by [OpenNIC Project](https://www.opennicproject.org/).
* [Disable third-party cookies](https://www.howtogeek.com/241006/how-to-block-third-party-cookies-in-every-web-browser/) (and then [verify your browser is obeying your settings](https://www.grc.com/cookies/forensics.htm)).

## Helpful tools

* Use certificate transparency monitoring tools ([like Facebook's](https://developers.facebook.com/tools/ct/)) to further check the trustworthiness of a given certificate (but, because FB is shit, they require you be logged in to a FB account)
* Use [TermsOfService;Didn't Read](https://tosdr.org/) to get up-to-speed on legal terms for a given service you're considering using.
* Turn off JavaScript using blockers such as [ScriptSafe](https://chrome.google.com/webstore/detail/scriptsafe/oiigbmnaadbkfbmpbfijlflahbdbdgdf) and [NoScript](https://noscript.net/) and re-enable it only on sites you purposefully visit
* Use [HTTPS Everywhere](https://www.eff.org/https-everywhere%20) so you make sure you send data to the service using HTTPS and not HTTP.
* Use the [Direct Links](http://canisbos.com/directlinks) extension to circumvent common Google/Facebook click tracking techniques.

Also, a guide: [Digital Security Tips for Protesters](https://www.eff.org/deeplinks/2016/11/digital-security-tips-for-protesters)