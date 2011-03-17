# Munin Plugins

This is a collection of Munin Plugins maintained by Michael Renner.

# Availability

The latest stable version of the plugins is available at github. To get it, visit:

https://github.com/terrorobe/munin-plugins

# The Plugins

## linux_diskstat_

This plugin uses extended blockdevice statistics available via /proc/diskstats (or sysfs) since Linux 2.6.

An annotated example is available at [blogs.amd.co.at](http://blogs.amd.co.at/robe/2008/12/graphing-linux-disk-io-statistics-with-munin.html).

To read the embedded documentation, run "`perldoc ./path/to/linux_diskstat_`".

linux_diskstat_ has been [merged by upstream](http://munin.projects.linpro.no/log/trunk/plugins/node.d.linux/diskstat_.in) (simply called "diskstat_" in the linux-specific modules section) as of October 2009 and is available in the 1.4.0 release.

## linux_diskstats

This plugin extends on the linux_diskstat_ plugin and makes use of the [multigraph]:http://munin-monitoring.org/wiki/protocol-multigraph feature which is available beginning with Munin 1.4.0. It offers all the information linux_diskstat_ has but has nice overview screens which clutter the node view less; giving detailed information as soon as you click on one of the graphs.

A sample installation can be seen at [mirror.inode.at](http://mirror.inode.at/munin/inode.at/mirror.inode.at.html#Disk).

linux_diskstats has been [merged by upstream](http://munin.projects.linpro.no/log/trunk/plugins/node.d.linux/diskstats.in) (simply called "diskstats" in the linux-specific modules section) as of December 2009 and is available in the 1.4.3 release.

# Installation of Munin Plugins

Adding a new munin plugin is quite easy:

  1. Copy or (sym-)link the file to the Munin Plugin directory (e.g. `/usr/share/munin/plugins/` on Debian systems)
  2. Run "`munin-node-configure --shell`" and verify that the commands make sense
  3. Invoke the commands
  4. Restart munin-node
