# cgroups-cpu-stats-reset
A patch that gives cpu.stats the ability to reset the counters like other cgroup components

This patch allows the cpu.stats values to be reset in cgroups
without having to remove and recreate it.  I wrote this patch
because I had a use case where resetting the values was required.
Many other components of cgroups allows stats to be reset, such
as cpuacct.stats.  To reset the stats, simple `echo 0 > cpu.stats`
