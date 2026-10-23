# The Tortll Project

> **DISCLAIMER**: this is, for now, just a dump of my ideas and experimental code. I'm currently an 18yo student who's learning and experimenting on this field and is considering this theme for the final year exam. Any feedback or tip is very appreciated :)

## Who am I?
Hello! I'm NylonCat, an 18yo Italian student who's facing the final year of high school. I'm very passionate about telecommunications (my school's main subject) and pretty much everything that involves networking and nets. One of my hobbies is also exploring privacy and how to maximize it, and from it branches another activity which is homelabbing (I currently manage a pretty basic but functional Proxmox home machine).

I'm making this page because I want to dump an idea i recently came up with, and hopefully find people who are interested in this project (and know way more than I do) while also creating something I could expose to my final year exam.
All of this is very experimental, I'm just basically toying around, so expect messy codes and texts, or even me disappearing from there, but I actually think that my idea could potentially be applied in the real world someday (I saw a couple of similar projects here), and make a little revolution in this sector.

## What is this project?
All of this starts off from a consideration I had on modern commercial VPNs: as probably everyone who's reading this knows, a VPN roots all traffic of connected clients towards a specific LAN, and potentially anyone in there can log or read everything, basically like a man in the middle attack. I noticed that companies who offer this service never grant you a complete way to trust them if not the usual "trust us, it's secure, we don't use or sell your data". And what concerns me more is that all the ads I see sell VPNs like they're this "magic tool that allows you to travel in the world and protect yourself from public Wi-Fis" while hiding what they actually do.
One of the obvious solutions to this is to host a VPN server ourselves, which is one of the coolest thing to have in my opinion (being able to connect to your home and all your services from across the world is super useful), however you still have to trust your ISP, and you can't "travel the world" if needed.

And from here, I started wondering: is there a way to make a commercial VPN truly zero-trust? Can an hypothetical company "mathematically" prove to the clients that the server isn't logging or stealing anything and it's just being used as a bridge between them and the internet?

## How does it work?
> Note: to be completely transparent, I'm using AI to assist and help me discover and learn these technologies. I'm nowhere near to be an expert on the field, and that's why I'm also seeking out on feedback and opinions! As I said, I'm just a student, I don't (yet) have fancy PhDs, but I'm for sure learning new stuff!

Turns out there **is** a way, using Trusted Execution Environments (TEE)! As the name says, all the software would run inside an encrypted and secure hardware system directly managed by the processor. AMD and Intel already developed CPUs that support these, such as [AMD SEV-SNP](https://www.amd.com/en/developer/sev.html) and [Intel TDX](https://www.intel.com/content/www/us/en/developer/tools/trust-domain-extensions/overview.html) technologies.
To make it simple, these allow to create inside a host operating system (let's say, for example, a Debian machine with an AMD SEV-SNP CPU) virtual machines whose RAM, which is allocated and reserved from the host to the VM, is fully encrypted by a randomly generated key by the CPU that is only known by it and no one else. This ensures that the VM cannot be accessed by the host system or anyone else, because everything, from his RAM to the physical buses used by it, are encrypted by the CPU.
It's not all though, because these processors, when booting and loading the VM, can make a complete hash of it

*WIP*
