> [[Wiki|Home]] ▸ [[Activities and events]] ▸ [[Mr. Robot's Netflix 'n' Hack]] ▸ **How to facilitate Mr. Robot's Netflix 'n' Hack**

Thanks for volunteering to facilitate Mr. Robot's Netflix 'n' Hack sessions!

Mr. Robot's Netflix 'n' Hack is a loosely structured opportunity to explore [[InfoSec]] and cybersecurity topics. It seems to work best when there is someone able and willing to focus group conversation on a particular topic, and is at least generally familiar with the material showcased in the episode. Alternate modes of facilitation may also work; feel free to explore! The instructions in this guide are just suggestions. :)

1. [Goals](#goals)
1. [Requirements](#requirements)
1. [Checklist](#checklist)
1. [Exercise suggestions](#exercise-suggestions)

# Goals

As the facilitator, your primary goals are to:

* assist participants who volunteer to give demos/run exercises (or present a demo/run an exercise yourself);
* keep the evening moving forward, and steer the conversation towards topics of interest for the group rather than an individual (individuals can always find time later to ask more in-depth questions of a knowledgeable participant);
* create the list of TTPs for the episode and/or iteratively add to it as a discussion progresses;
* play the episodes of the show!

# Requirements

The following equipment is needed for a successful hack night:

* [ ] A room with little ambient light. (The episodes of Mr. Robot are fairly dark on-screen. Light gets in the way.) The room must be large enough to accommodate all viewers and possibly their open laptops.
* [ ] A projector or large screen (large enough for easy viewing by a group of 5 to 20 individuals or so).
* [ ] A decent sound system for audio to be heard by everyone in attendance.
* [ ] Adapter cabling for the A/V setup.
* [ ] Access to decent Wi-Fi. Post-show discussions are greatly aided by being able to perform Internet searches to find resources.
* [ ] Video files of the show itself to play back. (One does not *technically* need to acquire these files legally.)
* [ ] Power strips and/or extension cords so everyone in attendance who brought a CPU can keep it powered on.

# Checklist

Use the following checklists to ensure you're ready for the session.

## T-2 days

1. [ ] get the episode's video file, if you don't already have access to it!

## T-30 minutes

1. [ ] make sure you have the projector, cables, and speakers handy, and plug it all in.
  * cables needed:
    * plain HDMI cable, or
    * VGA cable + Mini DisplayPort adapter, and
    * dual-colored stereo audio cables with headphone jack
  * please test all cable configs each time
1. [ ] test the sound and video of the video playback to ensure the episode screening is visible and audible
1. [ ] set up your computer *not* to mirror your display; you will need to project the episode on one screen while keeping notes in a second.

## T-0 minutes

1. [ ] give a brief intro; a welcome & reminder about timing/format should suffice.
1. [ ] turn things over to the demos and/or start the demo or exercise yourself
1. [ ] when it's time to play the show, give a brief "trigger warning" to remind folks that the Mr. Robot TV show deals with dark topics such as physical violence, including sexual assault, has swear words; generally, this is an "R-rated" show.
1. [ ] during the episode screening, open the [[Mr. Robot's Netflix 'n' Hack]] wiki page and edit it if necessary to include new TTPs (don't worry too much about missing any, but try to note as many as you can)
1. [ ] when the episode finishes screening, move the list of TTPs to the projected screen and ask if anyone finds a particular item interesting to start a conversation about it
1. [ ] solicit demos for next week from the people who show enthusiasm about a particular item!
1. [ ] lather, rinse, repeat until time's up. :)

# Exercise suggestions

## Week 1

### Beginner

* Use `ping` to ask a remote system if it is responsive or not.
* Log on to an IRC network and join a channel to watch the chatter.
* Use `locate` to find indexed files on your local system.
* Use TorBrowser to access the Web more anonymously.

### Intermediate

* Use `ifconfig` to take down or bring up a network interface.
* Use `kill` to stop a running process.
* Use `chmod` to change the permissions for a file.
* Use TorBrowser to access a "hidden service" (Onion site).
* Connect to a VPN. (Recommendation for demo: [RiseUp Black](https://riseup.net/en/vpn).)
* Use LOIC to DDoS *yourself*.
* Install and explore an alternate Desktop Environment.

### Advanced

* Bring up a trivial Onion site using Apache, Nginx, Lighttpd, etc.
  * Run [OnionScan](https://onionscan.org/) against your Onion site.
* Use `hashcat` or `john` to crack some password hashes.

### Expert

* Write a basic rootkit.
* 🚧 TK-TODO