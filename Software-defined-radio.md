> [[Wiki|Home]] ▸ **Software defined radio**

* * *

> 📝 **WORK IN PROGRESS**: This is a drafting pad, simply notes at the moment. I'm learning a lot about this specific technology and don't know enough to teach, so I'm currently just compiling my own research (in public). Please don't consider this recommendations of "good" educational material, especially if you're coming from the much-more polished [[InfoSec]] page(s).

* * *

# "Learn from…"

> 📝 Editor's note: This list is not quite ordered but does attempt to provide a "from top to bottom/from start to finish" sorting for the complete beginner.

* [Software Defined Radio - An Introduction](https://www.youtube.com/watch?v=kWfU1G3Jq4w)

  An introductory overview of Software Defined Radio (SDR) is given by Schuyler St. Leger at Desert Code Camp at Chandler-Gilbert Community College. The hour-long talk covers what SDR is and how it differs from hardware radio, SDR hardware available today, software tools to use with SDR HW, and live demonstrations of how to use SDR. (Here's a [video of the same presentation, about a year later](https://www.youtube.com/watch?v=Wjik-PjJA1w).)

* [Hak5 playlist: Software Defined Radio](https://www.youtube.com/playlist?list=PLBmFDs_1nZfBN2x5dbFXO7RfcwVGrqQy-)

  The male co-host of this show, Darren Kitchen, behaves like a classic techbro prick and his explanations aren't great but there is some decent beginner-level information here in a playlist that is sorted sensibly (from basic to advanced). The real value is in paying attention to the female co-host's (Shannon Morse's) learning process, which seems like it begins to carve a learning path for newbies like me.

* [Basics of IQ Signals and IQ modulation & demodulation - A tutorial](https://www.youtube.com/watch?v=h_7d-m1ehoY)

  This video presents an introductory tutorial on IQ signals - their definition, and some of the ways that they are used to both create / generate modulated RF signals, and demodulate / analyze RF signals. IQ signals are most often used in the transmit and receive paths of Software Define Radios (SDR). A [PDF of the drawings](http://www.qsl.net/w/w2aew/youtube/Basics_IQ_signals_modulation.pdf).

* [Software Defined Radio (SDR) Tutorials, by Michael Ossmann](http://greatscottgadgets.com/sdr/)

  This ongoing video series will be a complete course in Software Defined Radio (SDR). In this course, you'll build flexible SDR applications using GNU Radio through exercises that will help you learn the fundamentals of Digital Signal Processing (DSP) needed to master SDR. For the over-the-air exercises, you'll need a HackRF One or other SDR peripheral, such as an inexpensive RTL-SDR. (See [#hardware](#hardware).)

* [GNU Radio Tutorials: Labs 1–5, by Balint Seeber](https://files.ettus.com/tutorials/labs/Lab_1-5.pdf)

  Slide deck that contains some very important information regarding GNURadio. This has exercises and lessons so that participants can try them at their own pace.

* [Technician Ham Radio License, by David Casler](https://www.youtube.com/playlist?list=PL07A7D1C9D7BF7F48)

  The ARRL is a licensing body that administers examinations and awards credentials for legal compliance in operating radio transmitters (it is generally safe and legal to passively receive radio signals, i.e., to listen to electro-magnetic spectrum radiation, but it is not legal to transmit, i.e., to speak using the same mechanism, i.e., EM/radio). This video series is a "teach-to-the-test" free course by a long-time licensed ham radio operator that for the most basic of these licenses, the "Tech" exam. The next exam is the "[General](https://www.youtube.com/playlist?list=PL0R9jy9LZw_35KimLiSIOH0YdNtCeYcRe)" license and finally the "[Amateur Extra](https://www.youtube.com/playlist?list=PL0R9jy9LZw_3CHCH-5A8faeIA-H3e4ZNC)" license.

# Awesome List (DRAFT)

## Tools

### Hardware

* [RTL-SDR](http://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/) - Inexpensive (~$20), common peripheral based on the R820T2 chipset, which has a frequency range of  24 – 1766 MHz.
* [HackRF](https://greatscottgadgets.com/hackrf/) - Open source hardware platform that can be used as a USB peripheral capable of transmission or reception of radio signals from 1 MHz to 6 GHz.
* [BladeRF](https://www.nuand.com/) - SDR transciever capable of full-duplex, very wide spectrum analysis and transmission with an integrated field-programmable gate array (FPGA).

### Software

* [GQRX](http://gqrx.dk/) - Open source SDR receiver available for GNU/Linux and macOS.
* [SDR#](http://sdrsharp.com/) - Freeware, proprietary SDR receiver package for the Windows operating system.
* [HDSDR](http://www.hdsdr.de/) - Freeware, proprietary SDR spectrum analyzer for the Windows operating system.
* [rtl_fm](http://manpages.ubuntu.com/manpages/trusty/man1/rtl_fm.1.html) - Simple FM demodulator for RTL2832 based DVB-T receivers.
* [GNU Radio](https://gnuradio.org) - Free and open-source toolkit for software radio.
* [GrOsmoSDR](https://osmocom.org/projects/sdr/wiki/GrOsmoSDR) - Versatile library that provides a GNU Radio Companion block for interfacing with numerous SDR hardware devices.
* [Linad](http://www.sm5bsz.com/linuxdsp/linrad.htm) - Free software, cross-platform radio spectrum viewer and digital signal processing (DSP) program.
* [SDR Touch](http://sdrtouch.com/) - Freeware radio spectrum viewer app for Android.
* [SDRoid](http://sdr-labs.com/software/sdroid) - Free software radio spectrum viewer app for Android.

## Online communities

* [/r/RTLSDR](https://www.reddit.com/r/RTLSDR/) - Low-cost software defined radio (RTL2832 SDR) community.

## UNCATEGORIZED (FOR NOW)

* [FCC.io](https://fcc.io/) - Simple search and URL shortener for FCC ID queries.
* [RadioReference Frequency Database](https://www.radioreference.com/apps/db/) - World's largest freely accessible radio frequency lookup database.
* [Signal Identification Guide](https://www.sigidwiki.com/) - Crowdsourced database of signal recordings to help identify radio signals through example sounds and waterfall images.
* [ADSB Receiver](http://hiz.ch/index.php/home/adsb-receiver) - Android app providing an all-in-one ADSB decoder. (A limited tool, but a fun demo.)
* [ADSB Receiver Project](https://www.adsbreceiver.net/) - Zero-hardware-required software package that creates a self-hosted Web-based ADSB portal site on a Debian system. (Not SDR specific but fun to know about.)

* * *

See also:

* related pages: [[Favorite conference talks]] has several videos dealing with "wireless" and "radio" hacking, worth watching.