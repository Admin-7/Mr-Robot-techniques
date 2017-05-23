> [[Wiki|Home]] ▸ [[Security culture]] ▸ [[Persona-based training matrix]] ▸ **Security training: Targeted Activists versus The State**

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
      [[Targeted Activists vs Random Assholes|Security training: Targeted Activists versus Random Assholes#targeted-activists-versus-random-assholes]]
    </td>
    <td>
      [[Targeted Activists vs Assholes with Resources|Security training: Targeted Activists versus Assholes with Resources#targeted-activists-versus-assholes-with-resources]]
    </td>
    <td>
      <strong>Targeted Activists vs The State</strong>
    </td>
  </tr>
</table>

# Targeted Activists versus The State

## Prerequisites

Before you dive too deeply into this practice material, you should first explore the following lower-hanging fruit in the following order:

1. [[Security training: Individuals versus Random Assholes]]
1. [[Security training: Individuals versus Assholes with Resources]]
1. [[Security training: Individuals versus The State]]
1. [[Security training: Organizers and Journalists versus Random Assholes]]
1. [[Security training: Organizers and Journalists versus Assholes with Resources]]
1. [[Security training: Organizers and Journalists versus The State]]
1. [[Security training: Targeted Activists versus Random Assholes]]
1. [[Security training: Targeted Activists versus Assholes with Resources]]

# Security hygiene and habits

* [Don't maintain long-term OpenPGP keys](https://blog.filippo.io/giving-up-on-long-term-pgp/), try following the suggestions in [Operational PGP](https://gist.github.com/grugq/03167bed45e774551155) instead
* Use *only* hardware you trust:
  * Replace any commercial firmware on your devices with [LibreBoot](https://libreboot.org/).
  * If you can't use LibreBoot, at least patch against CVE-2017-5689 (see [Wikipedia](https://en.wikipedia.org/wiki/Intel_Active_Management_Technology#Silent_Bob_is_Silent)).

## Helpful tools

* encrypted email (GPG)
* Use [Qubes](https://www.qubes-os.org/), a hardened and security compartmentalized operating system generally
* Use [Tails](https://tails.boum.org/) for handling specific, extremely sensitive material
