> [[Wiki|Home]] ▸ [[Security culture]] ▸ [[Persona-based training matrix]] ▸ **Security training: Individuals versus Assholes with Resources**

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
      <strong>Individuals vs Assholes with Resources</strong>
    </td>
    <td>
      [[Individuals vs The State|Security training: Individuals versus The State#individuals-versus-the-state]]
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

# Individuals versus Assholes with Resources

## Prerequisites

Before you dive too deeply into this practice material, you should first explore the following lower-hanging fruit in the following order:

1. [[Security training: Individuals versus Random Assholes]]

## Practices

* [Firefox: Enable punycode in International Domain Names (IDN) display to thwart phishing](https://www.xudongz.com/blog/2017/idn-phishing/)
* Audit/revoke your social network account "Connected Apps" settings for apps you don't use
  * [For Twitter](https://myshadow.org/how-to-increase-your-privacy-on-twitter)
  * [For Google](https://myaccount.google.com/security#connectedapps)
  * [For Facebook](https://www.facebook.com/settings?tab=applications)
* Possibly put a [credit freeze](https://en.wikipedia.org/wiki/Credit_freeze) on your credit line at the three major credit
* Turn on "automatic updates" for software you use.
* Don't click on links in emails you didn't solicit yourself; when you get an email "from PayPal" asking to verify your account *close* the email, *open* a Web browser yourself, and *manually* type `paypal.com` into the address bar, yourself, don't just click the link.
    * Use [DKIM Verifier for Thunderbird](https://addons.mozilla.org/thunderbird/addon/dkim-verifier/) to further test that email you receive is authentic (and not spam or phishing scams).
* turn off "show remote images/content" and other "preview" features in your mail, RSS reader, etc apps
* Turn off auto-play on videos, etc.
* Adblockers (uBlock Origin, etc.)
* Clear cookies (cookie-clearing/whitelisting plugins)
* Signal (because of authentication, not just for encryption)
* Tape or a sticker over your webcam to frustrate video recording. (Cheap and easy!)
* Take a headset (headphones + microphone), chop off the wiring below the sensors, and plug that in to your headset jack to frustrate audio recordings.
* Avoid transmitting or storing sensitive info such as credit card numbers on old devices that you can't keep up-to-date, use a different device for that
* Check or [double-check the HTTPS lock icon's exact fingerprint](https://www.grc.com/fingerprints.htm) for important sites like PayPal or Facebook
* When charging your devices over a USB connection, use a USB "condom" ([data blocking adapter](http://www.portablepowersupplies.co.uk/portapow-fast-charge-data-block-usb-adaptor/)) to ensure only power flows into (or out of) the device
  * [Protect your devices with a $10 USB Condom](http://www.zdnet.com/article/protect-your-devices-with-a-10-usb-condom/)
* Enable [DNS over TLS](https://tools.ietf.org/html/rfc7858) support in your client devices, if available.
* If you use the Chrome Web browser, [enable strict site isolation](https://support.google.com/chrome/answer/7623121?hl=en).