> [[Wiki|Home]] ▸ [[Security culture]] ▸ [[Persona-based training matrix]] ▸ **Security training: Organizers and Journalists versus The State**

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
      <strong>Organizers &amp; Journalists vs The State</strong>
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

# Organizers and Journalists versus The State

## Prerequisites

Before you dive too deeply into this practice material, you should first explore the following lower-hanging fruit in the following order:

1. [[Security training: Individuals versus Random Assholes]]
1. [[Security training: Individuals versus Assholes with Resources]]
1. [[Security training: Individuals versus The State]]
1. [[Security training: Organizers and Journalists versus Random Assholes]]
1. [[Security training: Organizers and Journalists versus Assholes with Resources]]

# Practices

* Use alternate service providers (don't use Google's GMail)
  * See [LibreProjects.net, a list of hosted alternatives](http://libreprojects.net/)
  * See [AlternativeTo.net's list of self-hosted options](https://alternativeto.net/platform/self-hosted/)
* Ideally, use *decentralized* alternate services/networks
  * Have a Jabber+OMEMO fallback for Signal (for the truly frightening case where Signal is censored)
* [Secure your SSH servers](https://stribika.github.io/2015/01/04/secure-secure-shell.html).
* Use [DNS CAA](https://en.wikipedia.org/wiki/DNS_Certification_Authority_Authorization) records to help cut down on TLS certificate spoofing.
* Monitor [Certificate Transparency (CT) logs](https://scotthelme.co.uk/certificate-transparency-an-introduction/) to be notified of spoofed (faked) TLS certificates for your domain.
* Use Tor!!!!!11! (or a VPN, such as [OpenVPN](https://openvpn.net/), [Wireguard](https://wireguard.com/), [Outline VPN](https://getoutline.org/)/[Shadowsocks](https://shadowsocks.org/)).
* Host sites somewhere safe (privacytools.io)
* Consider [setting up an `.onion` service to access your site/domain](https://riseup.net/en/security/network-security/tor/onionservices-best-practices)
* Journalistic organizations should consider [SecureDrop](https://securedrop.org/)
* Use [MAT](https://mat.boum.org/) (or another tool) to remove document metadata before sharing online (specially if you need to protects your source)
* If you are providing shared hosting (virtualized, cloud, or shared) environments and infrastructure on legacy hardware, patch the (Intel) hardware on which these environments run using the [Intel Microcode Boot Loader](https://www.ngohq.com/intel-microcode-boot-loader.html).

## See also

* [awesome-selfhosted](https://github.com/Kickball/awesome-selfhosted) - a thorough list of "awesome" self-hosted alternatives to managed services