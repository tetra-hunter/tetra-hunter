# TETRA detection with Android and RTL-SDR: a practical overview

Tetra Hunter is a commercial Android application for detecting nearby TETRA radio
activity using compatible RTL-SDR hardware. This guide explains the setup and
the meaning of an alert. It is not the application's source code or a decoding
tutorial.

## What is the difference between detection and decoding?

Detection asks whether relevant radio activity is present. Decoding attempts to
recover information carried by a signal. Tetra Hunter provides presence alerts;
it does not decrypt or play voice conversations.

A radio-presence alert does not identify the vehicle or distinguish police,
ambulance and fire services. The signal-strength bar is not a distance meter,
direction finder or GPS position.

## Can an Android phone detect TETRA without an SDR?

Not with this setup. The external RTL-SDR receivers provide the radio input;
Android runs the application. A licence alone does not replace the receivers,
antenna, cables and USB connections.

The recommended kit has two receivers, an antenna and splitter, short RF cables,
and a powered USB hub connected to a USB-OTG-capable Android phone. See the
[maintained hardware list and installation guide](https://www.tetrahunter.eu/setup/)
for the current recommendations, rather than treating every Android phone or
every USB tuner as compatible.

## Is a DIY TETRA detector the same as an open-source project?

No. Here, DIY means assembling commercially available hardware yourself.
Tetra Hunter's application and recognizer are closed source. This repository
contains public product information and documentation, not an open-source
demodulator, firmware package or free APK distribution.

## Why do antenna position and power matter?

The app can only examine the radio input delivered by the hardware. Antenna
placement, obstructions, nearby interference and the reliability of the USB/power
setup affect what reaches it. The same installation can behave differently in
different surroundings. A weak indication does not establish an exact distance;
no single range figure describes every installation.

## Does an alert require somebody to be speaking?

The application is intended to notice relevant radio activity, including
signalling, rather than requiring a voice conversation. It still needs an actual
transmission to receive. A vehicle's physical presence alone does not guarantee
an alert when no relevant signal reaches the antenna.

## Can a European frequency table prove country compatibility?

No. Spectrum allocation, the network actually deployed, the equipment in use and
the application's supported configuration are different questions. Do not treat
a country name or a familiar network acronym as proof that a particular setup
works everywhere in that country.

This guide deliberately does not publish an unverified country/frequency table.
Any future table needs current primary sources, dates and clear distinctions
between allocation and measured application compatibility.

## Where can I see actual installations?

- [Member setups and hardware](https://www.tetrahunter.eu/setup/)
- [Member footage](https://www.tetrahunter.eu/members-footage/)
- [Product overview](README.md)
- [Support and community](https://discord.gg/nZPvbwzSpk)

General background: [RTL-SDR Blog's introduction to RTL-SDR](https://www.rtl-sdr.com/about-rtl-sdr/).
It explains RTL-SDR's receive-only hardware and the distinction between the
broader technology/community and individual hardware vendors. Product-specific
statements above describe Tetra Hunter; the external source does not endorse it.
