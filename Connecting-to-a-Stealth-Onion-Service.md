# Getting Started

## Prerequisites

**These instructions are for folks who already have themselves a `.onion` and the relevant client cookie.** 

* By the way, if what you want to do is use an onion service for simply secretly sharing files, you might have more luck [secretly sharing files with OnionShare and Tor Browser](https://github.com/AnarchoTechNYC/meta/blob/baa4dcc07b66477df48798ad43a5bb6d4d5335bc/train-the-trainers/mr-robots-netflix-n-hack/week-1/secretly-sharing-files-with-onionshare-and-tor-browser/README.md).

For a primer on Stealth Onion Services, see [this](https://github.com/micahflee/onionshare/wiki/Stealth-Onion-Services).

## How does it work?

There is a file that is created on your system when you install Tor and/or Tor Browser. This file is called `torrc`, and tells your Tor certain things about how it should operate, exactly like a settings screen. 

# Procedure

## Tools used

* Tor Browser

1. Install Tor Browser from [TorProject.org](https://www.torproject.org/download/download-easy.html).

### 2. The client cookie

The second thing you will need is an **Onion site address**, and a **client cookie**.

Your sysadmin should already have one generated for you. If they do not, harass them until they send one to you. :) 

The line you need will look something like:

`HidServAuth 48fbwufn0bw91xgnv.onion hq4nwfvf3nf39nsnf+2a A description here`

Explained:

`HidServAuth` <- Designates that whatever comes next is the hidden service authentication credentials.

`something.onion` <- Tells tor for which site are the credentials you're going to be using.

`random string of numbers and letters` <- The authentication hash specific to that site.

`some description` <- A description comment, letting *you* know for which site or service these credentials are for. 


Read more about [HidServAuth](https://www.torproject.org/docs/tor-manual.html.en#HidServAuth).

### 3. Editing the `torrc` file

You will be using your text editor of choice for this next part, like Notepad or TextEdit. 

* Add the configuration line to the bottom of the file. 
* Save the `torrc` file.

***Do NOT put these credentials anywhere even remotely public. This includes your e-mail. Saving these credentials anywhere that they could be obtained, by anyone else, defeats the entire purpose. And that would be silly.***

# Done! Finally! 

Your Tor Browser should now be able to connect to the `.onion` site described in your `torrc` file!


