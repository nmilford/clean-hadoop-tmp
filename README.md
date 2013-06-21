clean-hadoop-tmp
================

Hive does not always do a good job cleaning up after itself and will, many time leave lots of stuff in /tmp on HDFS.

Today I saw that I had 63T of data in `/tmp/hive-*` #humblebrag.  

This script cleans up data older than N seconds, similar to ```find /tmp  -mmin +360 -exec rm {} \;```

Dump it in cron and you're good to go.
