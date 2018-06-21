> [[Wiki|Home]] ▸ [[Activities and events]] ▸ [[Trivia night]] ▸ **How to facilitate Trivia night**

Thanks for volunteering to facilitate Trivia night!

Trivia night is a digitized equivalent of a classic bar trivia game.

1. [Goals](#goals)
1. [Variations](#variations)
1. [Requirements](#requirements)
1. [Checklist](#checklist)

# Goals

> 🚧 TK-TODO

# Variations

The FBCTF platform provides numerous options and settings to play games in a variety of ways. Depending on the physical-world context, some variations will be infeasible to play. For example, Trivia night played at an *actual bar* will mean most participants only have access to smartphones, not laptops, which cannot interact with the FBCTF interface. In this context, use the [classic bar trivia](#classic-bar-trivia) variation.

## Classic bar trivia

In this variation

* teams are directed to an Etherpad or other shared document editing tool,
* there are no bonuses for first or fast captures (successful answers),
* questions are announced and enabled in the game interface individually, as "rounds."

# Requirements

The following equipment is needed for a successful Trivia night:

* [ ] The [FBCTF](https://github.com/facebook/fbctf) platform exposed to the event venue's LAN; the FBCTF "Quiz Levels" ([see the Admin Guide](https://github.com/facebook/fbctf/wiki/Admin-Guide)) are the night's Trivia Questions.
* [ ] A projector or large screen (large enough for easy viewing by a group of 20 or so).
* [ ] Adapter cabling for the A/V setup, if necessary.
* [ ] Access to decent Wi-Fi; the digital scorecards are accessed over the venue's WLAN to the trivia server (FBCTF server).
* [ ] A list of prepared trivia questions, complete with:
    * [ ] Point values per question
    * [ ] Optionally, a single hint for each question
    * [ ] Optionally, a hint penalty in points for each question's hint

# Checklist

## T-1 day

1. Create a FBCTF server for the evening. For example, using [FBCTF's standard Vagrant startup](https://github.com/facebook/fbctf/wiki/Quick-Setup-Guide#standard-vagrant-startup):
    ```sh
    git clone https://github.com/facebook/fbctf.git
    cd fbctf.git
    source ./extra/lib.sh
    quick_setup start_vagrant prod
    ```
1. Login as the admin.
1. Define the Quiz ("Trivia") questions:
    1. Enter the trivia questions as Quiz Levels in the admin interface.
1. Set the Game Configuration options:
    1. Set Registration options:
        1. Turn registration *ON*.
    1. Set branding:
        1. Turn on *Custom Logo* (because we don't really care to advertise for Facebook, now do we?)
        1. Set Custom Organization to the name of the venue at which the event is played.
        1. Set the Custom Byline to something of your choosing.
1. Ensure all Quiz Levels are set to *OFF*.

## T-60 minutes

1. Connect the FBCTF server computer to the digital projector.
1. Make the FBCTF server available to the event's WLAN if not already done. For example:
    1. Forward the host's port `8443` to the guest's port `443`.

## T-30 minutes

1. Turn Scoring *ON* in the admin interface.
1. Advertise the game system to the event venue. For example, shout:
    > Hey everyone, we'll be hosting Trivia night; to play, point your web browser on your laptop or phone to `https://<THE_IP_ADDRESS_HERE>:8443` and don't worry about the certificate error. ;)
1. Encourage everyone to register a team of their own or join up with (sit next to?) players in a fellow team.

## T-0

1. Click on *Begin Game* in the admin interface.
1. When the game admins are ready to ask the first question, enable the first Quiz level, lather rinse and repeat.