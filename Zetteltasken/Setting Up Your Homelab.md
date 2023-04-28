![[Pasted image 20230428104315.png|400]]
# Determining Your Needs

* Things that may require special hardware:
	* Network Attached Storage ([[NAS]])
	* Media playback
	* Routing
* Most things won't need that much power, in fact you want to go as small as you can
* Older hardware works great, but be careful about reliability

# How To Make It Easy

Self-hosting your digital life can easily become a hobby requiring constant maintenance, upkeep, development, and learning. For some, this is the draw of self-hosting your own services, but I'd like to share how you can minimize maintenance and time spent while still getting the value of self-hosting.

* Don't feel like you need to get a massive server rack with expensive and powerful hardware
	* Start with something like a Raspberry Pi [[SBC]] or alternative
	* Generally, start small and only increase complexity when your current setup isn't powerful enough
	* Check your local surplus store or thrift shop for old computers, or use an old desktop
* Prefer off-the shelf solutions
	* Building your own infrastructure is [Fun](https://dwarffortresswiki.org/DF2014:Fun&redirect=no), but having something working that you can treat as a service is funner
	* When looking at [[Self-Hosted Services]], check to see if:
		* The codebase on GitHub has had recent and frequent updates and a low issue count
		* The community is large, and knowledge is shared freely and with kindness
		* Documentation is abundant, clear, and current
		* The service has been around for a long time and still has all these things
* Start small
	* Start by picking one thing to self-host
	* It doesn't matter how you do it, just give it a shot
	* Expect the service to fail
		* Once you get the hang of self-hosting it's straight-forward, but getting started has a steeper learning curve
		* Go into it expecting to learn, not to have a perfect setup
* Accept that no system will be perfect, and there will be bugs
	* You will run into problems, sometimes they can be deal breakers, sometimes they are really small and you can just leave them be
	* It can be easy to be discouraged, but don't let hiccups distract from the value of owning your data and services

# Picking Hardware

## Level 0: Personal Computer

You can always try self-hosting on your personal deskop, or even laptop. Making sure that the computer is always on can be a little cumbersome, but this is an awesome way to get started hosting your own services.

## Level 1: SBC

[[SBC]]s are a really easy way to get started, although it may be less appealing now that Raspberry Pi's are so expensive. That being said, there are plenty of alternatives.

### Upsides

* Smol, and very cute computer
* Generally very active and supportive communities
* Very low power consumption

### Downsides

* Often SBCs are ARM based which makes them limited in terms of the software support
* Raw CPU power is pretty limited
* SD cards are prone to failure, and not many have SATA/M.2 support

## Level 2: Desktop or Salvage

![[Pasted image 20230428100102.png|400]]

This is where I think most people would find the easiest path towards self-hosting. If you live near a university, check their surplus stores for cheap desktops or workstations that are generally 1/10th the cost you would pay for them new (or even used sometimes).

* Prefer systems that are guaranteed to be working
* Don't trust old hard drives
* Go for low power consumption
	* You don't generally need a beefy CPU
	* Most phones are more powerful than the server you need

## Level 3: Power Bill > Rent

![[Pasted image 20230428100416.png|300]]

I won't provide too much advice here since I don't advise buying full server-grade hardware since they are:

* Loud
* Expensive
* Large
* Power hungry
* Require arcane knowledge of enterprise software

If building your own server rack excites you, please do it! It's a ton of fun, but as far as self-hosting goes that is beyond the scope of this guide.

# Picking Operating System

## Personal Server Solutions

### TrueNAS Scale

[Scale](https://www.truenas.com/download-truenas-scale/) is my personal choice, and what I would recommend if you want something that will last and give you everything you need out of the box including:

* Configuration of network shares so you can access files over the network
* Regular data integrity checks and email notificaitons when hard drives have errors
* Built-in backup options through the UI
* A rich and well designed web UI
* Application hosting framework based on Kubernetes but simplified by the UI allowing for easy upgrade/rollback of your services
* Excellent support for efficient and fast transfer of files

**Note**: you'll need a fair amount of memory in your system for TrueNAS Scale. It uses half of your memory as a read/write cache for network file transfers.

## Linux Alone

One easy way to get started with self-hosting is to install a Linux operating system with a large community like [Ubuntu](https://ubuntu.com/) or [Ubuntu Server](https://ubuntu.com/download/server). These days, there are a lot of choices for server operating systems. I have a lot of friends who enjoy [Fedora](https://fedoraproject.org/) over OS like Ubuntu, but if you are just getting started out Ubuntu is generally a great choice.

### Headless?

If you can, I recommend installing an OS without a graphical user interface (GUI). This helps:

* Save on processor resources
* Reduce the amount of dependencies running on your OS
* Build a system that incentivises you to manage everything remotely

# Other Considerations

* [[Backup]]
* [[Networking]]