The best place to go for an overview of services that are available for you to self-host for free would be the [Awesome Selfhosted list](https://github.com/awesome-selfhosted/awesome-selfhosted) on GitHub. I'll list a few of the ones I like the most here just to share some ideas of what is possible.

# Home Automation

## Home Assistant

![[Pasted image 20230428092842.png|800]]

[Home Assistant](https://www.home-assistant.io/) is a wonderfully polished home dashboard for all things [[IoT]] and non-IoT. Here you can:

* Control and automate smart lights
* Add graphs for things like air quality sensors, power consumption, and occupancy
* Hook up to security camera systems and automate anything in your house using them
* Monitor energy usage or solar power generation
* Track the battery status of every device in your house

There are tons of plugins, and getting it set up is pretty straight forward.

# Media

## Plex

![[Pasted image 20230428093156.png|800]]

[Plex](https://www.plex.tv/) is a place to store all of your legally acquired media and stream locally. For the longest time, we couldn't stream media at our house so we were able to watch shows and movies by streaming locally.

## Jellyfin

Like plex, [Jellyfin](https://jellyfin.org/) allows you to host media locally but is also centered around letting you self-host a music library that you can stream anywhere you have access to your system.

# Networking

## SmokePing

![[Pasted image 20230428093422.png]]

[SmokePing](https://oss.oetiker.ch/smokeping/) is a network latency monitoring tool that lets you see how your network is faring over time both in latency, packet loss, and jitter. As you can see, StarLink is variable but overall very good when compared to most satellite services (400+ms of latency normally).

## PiHole

![[Pasted image 20230428093757.png|800]]

[Pi-Hole](https://pi-hole.net/) lets you block advertisments at the source by hosting a local DNS server that will not resolve any services that are known to serve ads. This can even block ads inside of mobile applications or on streaming services.

# Archival

## Kiwix

![[Pasted image 20230428093941.png|200]]

[Kiwix](https://www.kiwix.org/en/) lets you archive entire websites like Wikipedia, Stack Exchange, and many others. You can even get this app on your phone so that you can take all of Wikipedia with you on the go (including images!).

## ArchiveBox

[ArchiveBox](https://archivebox.io/) saves your entire internet history for offline browsing. You can even have it save all the videos you watch if you have the storage for it all.

## Paperless NGX

[Paperless-NGX](https://github.com/paperless-ngx/paperless-ngx) lets you scan, upload, and store all of your paper/digital documents and emails in a database that is searchable. It will OCR documents so that even paper ones become searchable as well.

# Personal Cloud and Storage

## NextCloud

[NextCloud](https://nextcloud.com/) is a personal replacement for Google services like Docs, Sheets, image storage, and much more.