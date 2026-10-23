# The Tortll Project

> **DISCLAIMER**: this is, for now, just a dump of my ideas and experimental code. I'm currently an 18yo student who's learning and experimenting on this field and is considering this theme for the final year exam. Any feedback or tip is very appreciated :)

## Who am I?
Hello! I'm NylonCat, an 18yo Italian student who's facing the final year of high school. I'm very passionate about telecommunications (my school's main subject) and pretty much everything that involves networking and nets. One of my hobbies is also exploring privacy and how to maximize it, and from it branches another activity which is homelabbing (I currently manage a pretty basic but functional Proxmox home machine).

I'm making this page because I want to dump an idea i recently came up with, and hopefully find people who are interested in this project (and know way more than I do) while also creating something I could expose to my final year exam.
All of this is very experimental, I'm just basically toying around, so expect messy codes and texts, or even me disappearing from there, but I actually think that my idea could potentially be applied in the real world someday (I saw a couple of similar projects here), and make a little revolution in this sector.

## What is this project?
All of this starts off from a consideration I had on modern commercial VPNs: as probably everyone who's reading this knows, a VPN roots all traffic of connected clients towards a specific LAN, and potentially anyone in there can log or read everything, basically like a man in the middle attack. I noticed that companies who offer this service never grant you a complete way to trust them if not the usual "trust us, it's secure, we don't use or sell your data". And what concerns me more is that all the ads I see sell VPNs like they're this "magic tool that allows you to travel in the world and protect yourself from public Wi-Fis" while hiding what they actually do.
One of the obvious solutions to this is to host a VPN server ourselves, which is one of the coolest thing to have in my opinion (being able to connect to your home and all your services from across the world is super useful), however you still have to trust your ISP, and you can't "travel the world" if needed.

And from here, I started wondering: is there a way to make a commercial VPN truly zero-trust? Can an hypothetical company mathematically prove to the clients that the server isn't logging or stealing anything and it's just being used as a bridge between them and the internet?
