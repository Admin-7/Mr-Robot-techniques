> [[Wiki|Home]] ▸ **Signal Private Messenger**

TL;DR: Use Signal. [[We do|New member orientation guide#signal]]. You should.

**Signal Private Messenger** ([Signal.org](https://Signal.org/)) is a free service with companion smartphone (Android and Apple iOS) and desktop apps that provides encrypted text, voice and video calling, and small file sharing capabilities over an Internet connection. It is used by journalists, activists, and ordinary citizens all across the globe as well as being the [United States military's recommended communications tool for its soldiers](https://www.militarytimes.com/flashpoints/2020/01/23/deployed-82nd-airborne-unit-told-to-use-these-encrypted-messaging-apps-on-government-cellphones/). Its eponymous encryption protocol has been audited by lauded cryptographers like Matthew Green and whistleblowers including Chelsea Manning and Edward Snowden.

The Signal encryption protocol is also licensed for use by corporations such as Facebook, Inc. for features in their WhatsApp and Facebook Messenger apps (although users of [Facebook Messenger must opt-in to a "secret conversation"](https://www.facebook.com/help/messenger-app/1084673321594605/) in order to protect their messages). However, Signal's own apps are strongly recommended instead of Facebook's. Learn more about Signal [via our Signal practice exercises](https://github.com/AnarchoTechNYC/meta/blob/master/train-the-trainers/mr-robots-netflix-n-hack/week-16/using-signal-to-communicate-with-your-team-safely/README.md) or by attending [Tech Learning Collective's Signal and Surveillance online workshops](https://techlearningcollective.com/workshops/Signal-and-Surveillance-How-to-Exercise-Digital-Civil-Liberties-in-a-Surveillance-State#events).

# Contents

1. [Signalboost](#signal)
    1. [List of Signalboost channels](#list-of-signalboost-channels)
1. [Tips and tricks](#tips-and-tricks)

# Signalboost

**Signalboost** ([Signalboost.info](https://signalboost.info/)) lets activists use Signal to send text blasts and receive hotline tips without revealing their identity or spending money. It is secure, simple, and free. It relies on both the Signal service proper as well as an additional service (also free-to-use) paid for and maintained by activist developers and administrators.

Signalboost channels are just Signal numbers, same as yours. You can send and receive encrypted messages to those numbers, which will be forwarded to one or more other Signal numbers, possibly a lot more. Technically, this makes the Signalboost service a proxy for Signal messages, which means the Signalboost servers, unlike the Signal service proper, *can* see some information about your activity such as which Signal numbers are subscribed to which Signalboost channels.

**The Anarcho-Tech NYC Collective vouches for the Signalboost service and recommends its use** for appropriate use cases. We have very good (very personal) reasons to trust the intentions and the capabilities of the Signalboost developers and their operations team.

Visit the [Signalboost FAQ](https://signalboost.info/faq/) and the [Signalboost How-to](https://signalboost.info/how-to/) pages to learn more.

## List of Signalboost channels

To subscribe to a Signalboost channel, send `HELLO` via your Signal app to the Signalboost channel number. Send `HELP` to see the commands you can use and `GOODBYE` to leave. Before you join a channel on this list, we suggest you first try joining the "playground" (test) channel at [+1-938-222-9889](sms:+1-938-222-9889).

### Regional channels

#### New York City

* [FTP Channel: (718) 550-6436](sms:7185506436) - Action thread administered by the organizers of recent FTP actions.
* [NYC JAIL SUPPORT: (718) 550-2312](sms:7185502312) - Announce/hotline channel with updates on jail support and staff answering questions about how to support arrestees.

# Tips and tricks

* [`signal-switch.sh`](https://gist.github.com/fabacab/e85c21215dfcef2b085a11cfdb4ddaa2) - Flip between two Signal accounts on a single Signal Desktop installation on macOS