---
title: Home Network Stack
description: A network stack complete with NAS, DNS resolver, and other niceties
thumbnail: /assets/images/rack.jpg
---
{% capture note %}
**NOTE:** _This was written **before** any posts about this project were written. As such, any documentation on current features are missing. However, new features may be posted since writing this._
{% endcapture %}
{% include md/card.html md=note padding=3 %}

{% assign rack=page.thumbnail | absolute_url %}
{% include md/figure.html src=rack width="250px" height="125%" %}
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
