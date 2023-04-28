Making sure you have a backup of your data is very important for any self-hosted data you don't want to lose. Hardware will fail, and without a backup it will be gone for good.

# 3-2-1

Have **3** copies of your data, with **2** backup copies, **1** of which is in a different location (far enough away to not be destroyed in a fire or natural disaster).

# Data Integrity

## Filesystem and Drives

Hard drives fail, and often they fail slowly and in ways that are hard to predict. I recommend using something like [ZFS](https://en.wikipedia.org/wiki/ZFS) (comes with things like TrueNAS Scale) which will regularly check filesystem integrity on hard drives. You can also run regular [S.M.A.R.T.](https://en.wikipedia.org/wiki/Self-Monitoring,_Analysis_and_Reporting_Technology) checks to interface with hardware running on harddrives to detect when the HDD starts to go bad.

### Backup Solutions

* [Backblaze](https://www.backblaze.com/)
* Another server you run, using something like:
	* `rsync`
	* ZFS send
	* etc...

### Hard Drives

When buying hard drives, try to choose ones that are rated for server usage. These drives are rated for more reads/writes and can withstand vibration when running next to other spinning drives.

### SSDs

SSDs are expensive, but incredibly fast and often last longer than spinning rust. Try to run your OS on an SSD separate from the drives you use for storage. This way, either can fail independently leaving either an OS to be repaired, or data to be recovered, not both at once.

## RAID

If you really care about your data, you'll want to store it on an array of hard drives. [RAID](https://en.wikipedia.org/wiki/RAID) is usually how this is accomplished. There's a lot of nuance here, so I'll recommend the most simple approach. Either:

* Use RAID 10, which stripes data across two or more drives.
	* If you have two drives in RAID 10, you can have one fail and lose no data
* Use RAIDz2 on ZFS for a better guarantee
	* ZFS allows you to regularly scrub the drives and repair errors as bit rot happens
	* RAIDz2 scales to many drives, but eventually you'll want to consider RAIDz3 or higher if you have more disks

