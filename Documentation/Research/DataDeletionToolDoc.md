# Data Deletion Tool Documentation

Preston Wells
Capstone IASC-4580
Forensics Tool Analysis Team

### Disk Cleaning Utilities

Disk cleaning utilities are ways to delete data from a disk but instead of doing it individually you are deleting all of the data on the entire disk. Leaves a signature that the file system was wiped which is why some people say that this technique isn't as good as Disk Degaussing.

### File Wiping Utilities

File wiping utilities are similar to disk cleaning utilities as they can wipe information off of a drive. But the main difference is that they can do it per file instead of just wiping the entire drive all at once. Leaves a smaller signature than disk cleaning, but still leave a signature. A couple of disadvantages are that they require user involvement and the fact that some people believe they don't completely wipe file information.

### Disk Degaussing

This is a process by which you apply a magnetic feild to a digital media device, resulting in an entirely clean media device. Even though this is probably the mose effective technique, it is not used in anti-forensics very often because of the high cost of degaussing machines. 

### Limitations

Because of the fact that we will only be working with virtual devices the only area of data destruction that we will be working with will be File Wiping. Since we don't have the money to get a disk degaussing machine even if we wanted to and secondly we will not be working with physical drives so wiping full drives will be tricky.
