# Munin Plugins

This is a collection of Munin Plugins maintained by Michael Renner.

# Availability

The latest stable version of the plugins is available at github. To get it, visit:

https://github.com/terrorobe/munin-plugins

# The Plugins

## linux_diskstats

This plugin uses extended blockdevice statistics available via /proc/diskstats (or sysfs) since Linux 2.6.

A sample installation can be seen at [mirror.inode.at](http://mirror.inode.at/munin/inode.at/mirror.inode.at.html#Disk), an annotated example is available at [blogs.amd.co.at](http://blogs.amd.co.at/robe/2008/12/graphing-linux-disk-io-statistics-with-munin.html).

To read the embedded documentation, run "`perldoc ./path/to/linux_diskstat_`".

linux_diskstat has been [merged by upstream](http://munin.projects.linpro.no/log/trunk/plugins/node.d.linux/diskstat_.in) (simply called "diskstat" in the linux-specific modules section) as of October 2009 and is available in the 1.4.0 release.

# Installation of Munin Plugins

Adding a new munin plugin is quite easy:

  1. Copy or (sym-)link the file to the Munin Plugin directory (e.g. `/usr/share/munin/plugins/` on Debian systems)
  2. Run "`munin-node-configure --shell`" and verify that the commands make sense
  3. Invoke the commands

# Distributions

## Debian

linux_diskstat_ is included in the munin-plugins-extra package available in Debian Squeeze
