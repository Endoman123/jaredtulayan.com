---
title: Home Network Stack
description: A network stack complete with NAS, DNS resolver, and other niceties
thumbnail: https://lh3.googleusercontent.com/D-JnEkv9NJ5fPCr9JKei6TqfpvttQ4CVU5X8FOMJNuwTXfTadq-hf9jrOjDgjC86YqoFMbdbXgrvxe4BigSJEYUs_EcvyGiLJKiIAI2s_RuwJO8NiFb6WHPNdXtd-pWG_G_qCbr1cr7W5OjpNbVyBhyfcnESnoz0xEi91GYGAGqwBRl3tOqabs0XUPZkUjaXM31iC1aUCCYje8L4OHjsgvBnawdX95Y9NXuKXLrvQ_-Qay_6qW5DZCwWCM1qxusyR2JctYAY9c4ZFnLrRuoCvzydjYf5FXIliKGCXzIuuPM6yq8M0cYYR1cMwm0fhjjbQQN__7ERv21V99peAHGLvvxGjiGKMYcAtudxP2GJuLGSV4-X80oKBUwrRCPUEpvhfoLm1pflwVI3tSFHZi0YcDhrIaT7Spgp-hmVeMw7ft8ZOBGsIdP7N3LLRKSsseJr0FkCU1vWIQN9WEaZtlGXehIOhbGgh2n4xhIcxDoU6bPA5LlpX3E_pxKtLlEP8PnbWSaRNMB35_eSzDsVrS_AAUxo-IIMSNkSFueY1LDOdpVjUgWjEupIyvhplwNfdejwZPE0Io3cpMmsE-EzctEgznn6NEDU8Dcc-DCUK1s_2iEV2GXPFdiatCfWv6UgnyjOoCvUOToksjx35f4mEqy7RnBSR4cVloSTsnDGBIugQG3pV2mPnp2hZqPuy2R7NPFRG3lCapAt3lpdiPoCMRtv6hAwbL41MA2eD75SmoAJ5uuzU2Mi3tigiSmSMBZ93VDmNrK6ByT0qHs3fm_D5SQOkDU9J69LbSqXO_6IhA=w563-h994-no?authuser=1
---
{% capture note %}
**NOTE:** _This was written **before** any posts about this project were written. As such, any documentation on current features are missing. However, new features may be posted since writing this._
{% endcapture %}
{% include md/card.html md=note padding=3 %}

{% include md/figure.html src=page.thumbnail width="250px" height="125%" %}
Sometime in the summer before my senior year of college, I decided that my home network needed a well-needed makeover.
So with the help of some of my parents' money, as well as some spare parts laying around the house, I built my home network
a full network stack. This was challenging, particularly because of a set of requirements that I wanted to fulfill:
- Unify all devices on the network in this stack
- Desaturate bandwidth
- Add networked storage for backup
- Host my game servers

With this, I invested some money into TIA rails and built a server rack out of some 2x4s and caster wheels that were in
the makerspace. Having a rack that was movable made sense at the time because I didn't know if we were ever going to renovate the house,
or if I ever needed to move the rack. In hindsight, I'd probably also want some female-to-female keystones that would allow me to easily remove
the cables.

I built a NAS for my family to store their photos and files. This was done with a combination of used 3TB WD Blue drives and an old Intel-based board.
While extremely convenient for everyone to be able to access those files whenever they need, I also wish we had better redundancy; the 3-2-1 method of 
storing backups would be good peace of mind in case the NAS hard drives fail. I also wish there was a bigger market for rackmounted ATX cases.

My game server is managed by Pterodactyl, a game server management panel and daemon. The panel, i.e.: frontend, is hosted on my personal VPS,
and the SuperMicro compute unit that I repurposed for this is the daemon. The server is a dual-cpu machine running two Intel Xeons, each with 6 cores and 12 threads,
and is loaded with 96GB of ECC-registered ram. The daemon machine is simply a docker host; The panel accesses this as a single node; If I really wanted to, I could have the
panel communicate with multiple nodes to spawn game servers on different machines.

Since my NAS is run with TrueNAS, I could run some other niceties. For instance, I am running a network-wide recursive DNS resolver through Pi-Hole, run as a virtual machine
on the TrueNAS system. This allows us to have DNS blocking, as well as cache DNS visits for faster access.

Finally, this is all routed through an eero mesh router and an unmanaged switch. Again, in hindsight, I should have taken a managed switch as having VLANs might have beena a
useful feature for isolating all of our IoT devices.

I hope to still add things to this stack; one such thing is a VPS so that my family and I can access this network wherever we are.
