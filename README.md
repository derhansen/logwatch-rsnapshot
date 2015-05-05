Logwatch configuration for Rsnapshot logfiles
=

What does it do?
-

This is a logwatch filter for Rsnapshot logfiles. It just collects, if there were errors
in the rsnapshot logfile. 

Example output
-
<pre>
--------------------- RSNAPSHOT Begin ------------------------

4 RSnapshot error(s):

[04/May/2015:08:07:48] /usr/bin/rsnapshot daily: ERROR: /usr/bin/rsync returned 255 while processing user@192.168.2.1:/my/dir1
[04/May/2015:08:07:48] /usr/bin/rsnapshot daily: ERROR: /usr/bin/rsync returned 255 while processing user@192.168.2.1:/my/dir2
[04/May/2015:08:07:48] /usr/bin/rsnapshot daily: ERROR: /usr/bin/rsync returned 255 while processing user@192.168.2.1:/my/dir3
[04/May/2015:08:24:30] /usr/bin/rsnapshot daily: ERROR: /usr/bin/rsnapshot daily: completed, but with some errors

---------------------- RSNAPSHOT End -------------------------
</pre>


Installation
-

1. Copy files from 'conf/logfiles/' to '/etc/logwatch/conf/logfiles'
2. Copy files 'conf/services/' to '/etc/logwatch/conf/services'
3. Copy files 'scripts/services/' to '/etc/logwatch/scripts/services'

Usage
-

Display logfile entries (default output)

~# logwatch --service rsnapshot


Feedback / Improvements
-

Feel free to provide feedback or suggestions for improvement.