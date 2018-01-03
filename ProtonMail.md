> [[Wiki|Home]] ▸ **ProtonMail**

[ProtonMail.com](https://protonmail.com/) is an e-mail service provider that has become wildly popular amongst activist groups and politically vocal individuals. This page offers a several evolving critiques of this phenomenon and warns comrades against using ProtonMail without first understanding the severe risks involved. This page is not an opinionated editorial; it is a technical and sociopolitical analysis of the ProtonMail service, along with its cultural impact on activist groups, from an anarchist and autonomist perspective.

**TL;DR:** ProtonMail uses weasel words to give less technically-experienced people the impression that their service is capable of more than it is. The brand relies on continued ignorance of important details to thrive. If you insist upon using e-mail for any sort of communication, there is no substitute for using PGP/GPG yourself; you can do this with ProtonMail as your service provider, or you can do this with Google. As long as you take the steps necessary to secure the privacy of your email communications on your own, without relying on the promises of a service provider (like ProtonMail) to do this for you, then you can comfortably use ProtonMail or any other service that you wish.

The above summary has its own caveats, but if you haven't the time to read further, that's what you need to know and need to start telling your friends. To learn more about PGP/GPG e-mail encryption, see 🚧 TK-TODO: WE NEED A BETTER GPG GUIDE OR A LINK TO ONE.

# Contents

1. [TK-TODO](#)
1. [TK-TODO](#)
1. [TK-TODO](#)

# Scratchpad

"was there a reason Proton Mail is, like, bad? morally?"

There are reasons I distrust and dislike protonmail, but they are a bit "misty" (like, not one direct thing that's bad).  The main reason I dislike them is that they are a silicon valley group who puts forward buzz words to sound magic about personal security.

Protonmail is problematic for a few reasons. The biggest one in my mind is the way they advertise themselves. "Encrypted mail!" They say, but what they don't tell the average person (whom they are targeting with their ads and aesthetic) is how encryption actually *works*. Namely, that you can't have encrypted correspondence without there being an *end to end* exchange of some kind. Be that a keypairing, as in the case of PGP/GPG, or in the case of an encrypted server, such as RiseUp or Protonmail. However, these two things are totally different things. When you use PGP/GPG, your message is encrypted. Meaning that only the recipient can read it. This exchange is automatically handled by Protonmail *only* when both users are using it.

Notice that this is a service that one can use anywhere, even on Gmail, if they are applying GPG themselves.

Their first tagline is "secure email based in switzerland" but the actual team behind the company are Americans based outta harvard and caltech, with significant funding from the valley.  So the "based in" is partially about the press history and also that their servers literally live in Switzerland.

In the case of an encrypted server, like RiseUp, this does not mean the messages themselves are encrypted end to end. Only the data being stored on that server is encrypted, after the fact. This is a deterrent against police raids, for example - the cops cannot read what is stored on that server.

it is that they remove instruction in place of pictures of swiss mountains.  They want to hand-wave the actual important things to say "you have security cos of swiss privacy laws and no cop will enter a mountain?  also we are SMART like CERN SMART?!? So we got this."

One major point there is that Protonmail does NOT encrypt emails that are not sent to another Protonmail account, because they can't handle the way anyone else, like Gmail, handles encryption. So, therefore, they are slinging "encrypted email" without explaining that MAJOR caveat, which is mad irresponsible.

This all gives off a feeling that they want to become a new niche titan.  They want to replace companies instead of empower people, and not teach them what all this actually means so that you _have_ to rely on them (the way their encryption work points to that reliance).

they even recently created "[ProtonMail Bridge](https://protonmail.com/blog/thunderbird-outlook-encrypted-email/)" Which attempts to "solve" this problem, but it solves the problem with their own proprietary solution. Which means it's actually a nonsolution to no problem, because we already have had PGP for, like, ever. Literally since the 1980s.

fuck.  and the problem is educational.

So, their motives for doing these things are highly suspect. Well, actually, they're very transparently "LET US MAGIC AWAY THE INFORMATION FOR YOU," which, when it comes to encryption, is not a good idea. When done in the hands of a company whose interests are clearly those of the Silicon Valley mainstream.

There are two "kinds" of encryption happening here, people often get them confused. The first is email message content encryption, i.e., the text you're actually looking at. This is what PGP encrypts.

The second is transport encryption, i.e., the equivalent for email as HTTPS is for the Web. HTTPS does not encrypt the page content, it encrypts the transit of that content across the Internet. This is SMTPS (SMTP over SSL/TLS) and IMAPS (IMAP over SSL/TLS). The SSL/TLS is exactly the same for email as it is for Web browsing, but you almost never have to interact with it because you don't run your own email server.

Both Gmail and ProtonMail support SMTPS, i.e., when a ProtonMail user sends email to a Gmail user, the following happens:

1. The ProtonMail user opens a Web browser and makes a connection to ProtonMail, writes an email, and hits send.
2. ProtonMail looks at the recipient email address and, upon seeing that it does not end in `@protonmail.com`, immediately sends the email to Gmail *over an SMTPS* (encrypted transport connection). The email contents are not encrypted, so ProtonMail AND Google both can read the email contents.
3. Gmail receives the email, and will tell you whether or not the message was "delivered securely."

For instance, in the Gmail app or Android, you can see a "Security details" user-interface fragment that describes the email's *delivery* security properties (whether Google received the email from an SMTP server that used TLS).

So the point is, this lets ProtonMail claim to have "encryption," but what they're really saying is "no one except your mail provider can read your email." This is *true*, because as long as ProtonMail uses transport-layer protections (i.e., they are protecting data "in motion") and Gmail uses transport-layer protections (and they are), then the contents of the email are encrypted when traveling from your Web browser to ProtonMail, then decrypted, then re-encrypted for transit to Google, then decrypted, then re-encrypted for transit from Google to your phone. I bring this clarification up is because it's not correct to say that ProtonMail doesn't handle encryption the same way others, like GMail, do. They do, for SMTPS/IMAPS, but they don't for PGP, but that's because Gmail *doesn't do PGP at all.* So, that's the first nuance to understand.

The second thing to note is that insofar as message *content* encryption is concerned, what ProtonMail offers to users of ProtonMail who send email to other users of ProtonMail is the same thing as, say, Signal *in principle* but not *in practice* because ProtonMail chooses which lock to put on your message: if I were a ProtonMail programmer, I could write a line of code that says "When Bob sends an email to Alice, instead of using Alice's lock, use mine." And Bob would never be the wiser, because there is no point during the experience of using ProtonMail that Alice is ever presented with the option to choose Alice's lock. This is what is meant by "key management." When I say, in the WP PGP Encrypted Email that "users manage their own keys," it means that the software does not make choices for you about which public key (lock) to encrypt the message to. That's GOOD, because it means *you* get to choose that. This, of course, is "hard for users," and so "secure messaging apps" like ProtonMail, or Apple's iMessage,  which "manage the keys for the user," are *technically* "end-to-end encrypted," but not actually trustworthy unless you trust the service provider *managing the keys.*

Reasons to distrust Protonmail:

(1) Protonmail stores users' private keys on Protonmail's server. This requires trust in the provider, as noted above, which a truly "trustworthy" provider would never ask for.  Requiring trust is a big no-no in any service that purports to be secure in-depth (for example: against attacks carried out via legal compulsion leverated over otherwise trustworthy sysadmins), It should be noted that requiring users to trust Protonmail to store and decrypt their private keys requires even *more* trust than Signal, whose servers only stores "pre-key" material and not actual private key material, which is always stored in clients.).

(2) Protonmail purports to safely store a user's private key by encrypting it to a password that the user must provide upon login (much like you are prompted for a password to gain access to your private key when using gpg from the command line or Engmail in Thunderbird).  *But* the fact that Protonmail asks for this password via the browser, and then allows you to temporarily store private key material in the browser raises *serious* concerns that (to my knowledge) they nowhere address.

in the browser are problematic for a few reasons. The core reason is that there is a long-running controversy over whether pgp encryption can be safely accomplished in javascript at all (see, eg: https://www.nccgroup.trust/us/about-us/newsroom-and-events/blog/2011/august/javascript-cryptography-considered-harmful/), which is what the underlying PGP implementation that Protonmail uses (https://openpgpjs.org/) claims to do. So, assuming a perfectly trustworthy sofware provider under no compulsion, given the fact that they are attempting to perform crypto in javascript, I would at least expect a detailed explanation as to why they feel they have accomplished this and I should "trust" it. To my knowledge (I'd love to learn I'm wrong), they neither provide such an explanation or even acknowledge that it is a known Hard Problem (tm).

Further eroding my trust in the fact that the code runs in the browser is, despite this being mitigated somewhat by the recently standardized [W3C's Subresource Integrity (SRI) mechanisms](https://www.w3.org/TR/SRI/) to whitelist remote resource contents, the fact that *by virtue* of it running the browser, I have no strong guarantee that the code that is running is actually the code that has been published and audited by Protonmail. Quite literally upon every HTTP request, a different javascript payload could be provided and unless I am manually inspecting the (minified) source code (which would show me very little because that's what minification accomplishes: https://en.wikipedia.org/wiki/Minification_(programming)), then I have no guarantee that malicious code has not been injected and compromising my private key (and with it the ability to decrypt all my messages and pose as me).

But even *furthermore* the fact that I am asked to transmit this password to a server I do not control. How do I know that the code is not siphoning off my password? Where is the code that I may inspect? How do I know that Protonmail has not been forced under compulsion to provide my password? Which is just to say: why do they have to *know* my password at all in order for their encryption story to work?

All of these problems were present in the last two examples of PGP email solutions that sought mass adoption my asking users to trust either a browser (hushmail) or a provider with access to private key materials (lavabit). In both cases, government agencies sought to compel the provider to substitute code that would compromise passwords for targeted users (hushmail) or directly provide the ability to decrypt private key material (lavabit).

That is why anyone who has thought seriously about the problem of "user-friendly" encrypted email (riseup's LEAP project is a decent example: https://leap.se/en/docs/tech) has gone to great lengths to (1) keep encryption operations out of the browser and in code that executes as a desktop binary that can be "reproducibly built" (https://reproducible-builds.org/) and thus verified to match the published code. They also (2) ask for passwords through "zero knowledge" methods such as SRP (https://en.wikipedia.org/wiki/Secure_Remote_Password_protocol) such that even a compromised (or legally compelled) provider would not be able to control the private key it stores encrypted at rest. But most importantly: (3) they acknowledge that these problems are HARD (https://leap.se/en/docs/tech/hard-problems) and try to bring users along on the ride of understanding why they have made the choices they have made in trying to solve them.

This just reduces back to our key points: they try to "magic away" all the problem solving that's going on, and in so doing, induce a passive/consumptive relationship to technology ("verbing" not only themselves but the actual and real friction of the problem they're trying to solve for me out of existence) instead of helping me build an active and empowered one. At the bottom of it, that's why I will never trust their solutions. Because they ask me to. And don't acknowledge that this is what they're asking me. And I've never built a truly trustworthy relationship that started with a lie.

So, because of SRI, the only thing in your beautiful rant that I would quibble with at all is the part about the browser itself, by virtue of being a browser, does not offer a guarantee that the code you're getting from ProtonMail is the code you expect. You perfectly describe exactly what would need to be done to ensure that the code you are getting is the code you want, which is to audit the source (minified if necessary) and then take the hash of that code, and then *on each HTTP request* verify that the code you received is the code you expected. Thankfully, that's *exactly* what the `integrity` attribute defined by the W3C's SRI Rec is designed to automate. :D

There are, of course, reasons why a site would not want to do this, and interestingly they are the same reasons pointed out about "magicking away" the details for people: if I am widgetco.com and I want it to be "easy" for you to display my widget in your site's sidebar, I want to give you a URL like `https://widgetco.com/sidebar_widget.js`. The point here is that the URL doesn't declare anything about its content, which makes it easy for me to update it when *I* want to.

What I'm saying with a URL like this is, "Hey, don't worry about updating your copy of my example widget in your sidebar when I release a new version. *I'll do it for you.*"

To understand that, let's compare it with another way of doing something like this. I'm widgetco and I know you care about knowing what code you're running. So I give you a URL like this: `https://widgetco.com/v1/sidebar_widget.js` Now, I'm telling you, "Here is the version of the program you intended to install. It's version 1. It's at this URL. And I *promise* I will not change it." Now the question is: how much do you trust my promise?

And that is *also* what SRI *could* be for: giving the end-user the ability to say, "Hey, you promised you wouldn't change the code coming from this URL, and since I wasn't automating checking up on that all the time, I didn't notice, until now." Which is…neat. :)
