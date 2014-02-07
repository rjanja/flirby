flirby
======

Cinnamon applet for monitoring webcam or device usage.

This applet supports monitoring devices and files a number of ways, using a combination of *inotify*, *GUdev*, *Gio.FileMonitor* and simple polling. Some methods require external libraries to be installed and although this applet can function without their use, it's recommended to choose the correct, most efficient mechanism for the job.

In the case of `/sys/devices`, these files are not normal files in that they are read from the kernel each time they're accessed. So a simple _FileMonitor_ won't suffice to detect device activity.

This applet allows configuration of which detection mechanism to use, how often to do regular polling when selected, and active/inactive status icons. It supports multiple instances in the event that you have multiple files or devices you would like to monitor.

