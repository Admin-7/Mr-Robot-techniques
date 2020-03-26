> [[Wiki|Home]] ▸ [[Tor]] ▸ **Onion services**

[Tor's Onion services](https://www.torproject.org/docs/onion-services) make it possible to host long-running services (servers) more anonymously. In earlier versions of Tor, Onion services were called "Hidden Services" or, more accurately, Location-Hidden Services. This is because the purpose of an Onion service is to hide the [IP address](https://simple.wikipedia.org/wiki/IP_address) of the server from connecting clients.

1. [Onion servers as reverse proxies](#onion-servers-as-reverse-proxies)
1. [Tor authentication](#tor-authentication)
1. [Onion sites and HTTPS](#onion-sites-and-https)

# Onion servers as reverse proxies

From the perspective of a system administrator, Tor's Onion service feature is basically a *reverse proxy* that accepts connections only from Tor clients.

```
┌───────────────────────────┐
│ Torified user application │
│    (like Tor Browser)     │
|  http://something.onion/  |
└───────────────────────────┘
            ↓
┌───────────────────────────┐
│ Tor client                │
└───────────────────────────┘
            ↓
┌───────────────────────────┐
│ Internet                  │
└───────────────────────────┘
            ↓
┌───────────────────────────┐
│ Tor server configured as  │
│   Onion service, e.g.     │
|  HiddenServicePort 80     |
└───────────────────────────┘
            ↓
┌───────────────────────────┐
│ Server application which  │
│  is listening, e.g., on   │
│       localhost:80        │
└───────────────────────────┘
```

This means that all requests to the server appear to be coming from the address of the Tor server it is behind; when the Tor server and the server application are on the same host, this means the server application perceives all requests to have come from the loopback IP address (typically `127.0.0.1`), thus anonymizing client queries.

Note, however, that merely operating a server as an Onion service does *not* mean that the server's IP address is hidden from clients in a similar way. The server application itself must also be configured in such a way as to avoid divulging its IP address to clients that request it in one way or another. (See [AnarchoTechNYC's CTF repository wiki](https://github.com/AnarchoTechNYC/CTF/wiki) for more information about [various ways to de-anonymize a server or a user that is trying to remain hidden inside the Tor network](https://github.com/AnarchoTechNYC/CTF/wiki/Tor#de-anonymization-attacks), aka. the "darknet.") This process of further configuration is known as security *hardening*, and is specific to each independent service that is operating on a given server.

# Tor authentication

The Tor server in front of the hidden service can also protect the server application from discovery by requiring that connecting Tor clients authenticate to *it* (the Tor server) before it will agree to pass traffic to the back-end service it has "onionized." This is accomplished by enabling the Onion service authentication configuration directives. See [[Configuring an authenticated Onion service]] and [[Connecting to an authenticated Onion service]] for more information about authenticated Onion service set ups.

# Onion sites and HTTPS

Since Tor's own encrypted transport protects the contents of Onion service traffic as it traverses the Internet, there is not a strict need for additional transport-layer security (TLS) protections, such as in the form of accessing Onion (web)sites over HTTPS. Similarly, since the `.onion` domain name is derived from a private key that presumably only the Onion service operator has a copy of, the domain name itself fulfils the function of a TLS certificate's identity assertion. In this way, Onion services provide both confidentiality and authenticity without the need of TLS.

Nevertheless, many Onion service operators, especially those who are using Tor Onion services for reasons other than publisher anonymity, *do* take the added step of providing TLS certificates for their Onion services. This can cause problems when the domain name in the TLS certificate is for the non-Onion version of the same Onion site. When you connect to, e.g., `https://some-site.onion`, a properly configured Web browser should refuse to load the page if the TLS certificate that the Onion service presents is actually for `some-site.com`.

To get around this, you can configure your Tor client to map the address of `some-site.com` to its `.onion` equivalent. As long as your client application is properly torified, Tor will direct all connections it receives ultimately destined for the clearnet address to the Onion service, instead. This leaves the client application none the wiser, allowing the TLS certificate validation check to succeed.

To accomplish this, set the `MapAddress` configuration directive in your Tor client. For example:

```
# Send all traffic intended for `some-site.com` to `some-site.onion` instead.
MapAddress some-site.com some-site.onion
```