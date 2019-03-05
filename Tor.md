> [[Wiki|Home]] ▸ **Tor**

[**Tor**](https://torproject.org/) is a privacy-enhancing computer networking tool that can be used in concert with complementary tools like Web browsers for a number of different purposes. These include accessing (or publishing) information that is likely to be censored and hiding your physical and/or network address from other systems you want to communicate with. While extremely powerful, it is also extremely easy to misuse.

So that it is harder to make privacy mistakes while using Tor, the Tor Project makes a special Web browser called the **Tor Browser**, which guarantees that certain information (like the make and model of your computer) divulged by normal Web browsers are not automatically revealed to Web sites that you visit. This makes using the Tor Browser one of the most private ways to browse the Web.

One of Tor's most powerful features, called [[Onion services]], allows for any network service that uses the underlying TCP protocol to be similarly privacy-enhanced by making it harder (but [not inherently impossible](https://github.com/AnarchoTechNYC/CTF/wiki/Tor#de-anonymizing-onion-sites)) to reveal the [[IP address]] of the computer hosting the service.

# Projects

* [AnarchoTechNYC/ansible-role-tor](https://github.com/AnarchoTechNYC/ansible-role-tor) - Our [Ansible](https://ansible.com/) role for securely building a system Tor from source and optionally configuring numerous high-security Onion services.