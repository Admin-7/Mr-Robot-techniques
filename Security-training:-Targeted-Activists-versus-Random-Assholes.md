> [[Wiki|Home]] ▸ [[Security culture]] ▸ [[Persona-based training matrix]] ▸ **Security training: Targeted Activists versus Random Assholes**

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
      <strong>Targeted Activists vs Random Assholes</strong>
    </td>
    <td>
      [[Targeted Activists vs Assholes with Resources|Security training: Targeted Activists versus Assholes with Resources#targeted-activists-versus-assholes-with-resources]]
    </td>
    <td>
      [[Targeted Activists vs The State|Security training: Targeted Activists versus The State#targeted-activists-versus-the-state]]
    </td>
  </tr>
</table>

# Targeted Activists versus Random Assholes

## Prerequisites

Before you dive too deeply into this practice material, you should first explore the following lower-hanging fruit in the following order:

1. [[Security training: Individuals versus Random Assholes]]
1. [[Security training: Organizers and Journalists versus Random Assholes]]

## Practices
* Use a data broker scrubbing service. They cost money, which sucks, but if you are busy and stressed out you may not be able to go through the arduous process of really thoroughly opting out of every data broker. The best service we can recommend is [Privacy Duck](https://www.privacyduck.com/services/), which is a reasonably ethical company that activists we know have had good experiences with. Reach out to your community (especially to privileged allies) for financial support. You deserve it.
* If you have to mobilize people on major social networks like Facebook and Twitter, lock down your accounts and use separate activism accounts whenever possible. If you have a personal / family Facebook account, note that Facebook will expose your family connections and often photos, so make sure that you [lock it down](https://github.com/actsecure/resources/wiki/Securing-your-Facebook-profile) or ideally get off Facebook entirely.
* Don't work under your legal / government name. For many activists, it's too late for this, but if your name is not widely publicized yet, working under a name which is not your government name will make it much harder to find information about you in data brokers. Even just altering the spelling of your name or adding a false middle name or initial can help (this may be easier than a full-on name change if your trust network already knows your name and changing it would be problematic).
* Don't put your birthday on the public internet. If you have a common name, your birthday is a great way to verify that data broker information is in fact you. Consistently using a false birthday or using random birthdays on social media can help make it harder to pinpoint you in data brokers.
* Compartmentalize your identity. This takes some creativity and diligence, but doing everything you can to keep your activism identity separate from your professional and personal identities will make it harder for attackers to get at you and the people you love.
  * Alter your name and birth date consistently or use a separate but consistent social media handle for activism work.
  * Use a separate email for high risk activism work. Although this can be a hassle to keep up, it is safer. You can use [SMTP](https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol) to send and receive email from several addresses all from one account. This is not currently possible with encrypted email, but is a useful convenience for unencrypted email. Be careful though, because some email providers (like gmail) [will still show the address you're sending from](https://webapps.stackexchange.com/questions/77767/gmail-hiding-the-original-from-sender-address-when-using-send-as#84165) which can lead to cross-contaminating your identities. Make sure you use an email service that will not do this. 🚧 TK-TODO: do we have recommendations for email services like this?
  * Not everyone has the logistical capacity to separate your friends, family, fellow activists, and co-workers, especially because there is often overlap between these groups. Pick the connection that is the most high-risk for you (Want to protect your kids? Need to keep your activism secret from your employer?) and focus on separating those two identities.