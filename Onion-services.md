> [[Wiki|Home]] ▸ [[Tor]] ▸ **Onion services**

[Tor's Onion services](https://www.torproject.org/docs/onion-services) make it possible to host long-running services (servers) more anonymously. In earlier versions of Tor, Onion services were called "Hidden Services" or, more accurately, Location-Hidden Services. This is because the purpose of an Onion service is to hide the [IP address](https://simple.wikipedia.org/wiki/IP_address) of the server from connecting clients.

Operating a server with an Onion service does *not* mean that the server's IP address is hidden from clients merely by running behind Tor. The server itself must also be configured in such a way as to avoid divulging its IP address to clients that request it in one way or another. ([See AnarchoTechNYC's CTF repository wiki for more information about various ways to de-anonymize a server or a user that is trying to remain hidden inside the Tor network](https://github.com/AnarchoTechNYC/CTF/wiki/Tor#de-anonymization-attacks), aka. the "darknet.") This process of further configuration is known as security *hardening*, and is specific to each independent service that is operating on a given server.

* [[Configuring an authenticated Onion service]]
* [[Connecting to an authenticated Onion service]]