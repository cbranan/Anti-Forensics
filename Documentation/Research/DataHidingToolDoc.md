# Data Hiding Tool Documentation

Casey Branan
Capstone IASC-4580
Forensics Tool Analysis Team

#### Out of Scope:
Due to this being a virtual machine, any physical hardware data hiding will not be achievable. As a result, hiding data in the hardware, such as the Master Boot Record (MBR), Host Protected Area (HPA), and the Device Configuration Overlay (DCO) will not be included in the scope of the hiding and toolkit evaluation.

### Alternate Data Streams

Alternate Data Streams were originally created for legitimate reasons for compatibility with Macintosh files and for Windows to put information such as file attributes and temporary storage without effecting the files size or functionality. This of course is being abused by attackers now to hide tools and data from system admins and forensic analysts without leaving any easy to find traces. A simple command such as “type c:\anyfile.exe > c:\winnt\system32 \calc.exe :anyfile.exe” will hide the anyfile in with the calculator and not show the right size or a trace of evidence besides and updated timestamp on the calculator file, which of course can then be overridden back to what it was before with a time-stomper program.
This will not require an actual tool download. I will use the VM’s Windows 7 operating system to create ADSs. Then under these streams, I will create files and attempt to hide data.

### Steganography

Steganography came about as the simple idea of hiding things in plain sight back in the early days of humans. It is still used today in modern day computing, by hiding text or files in other files in plain sight. The approach is simple, take one or more ordinary videos and/or images to use as a carrier file, and then inject the hidden data (text or images etc) into the carrier files with any of the numerous tools to make a payload file. The payload file looks and acts just like the original file, and the message can be transmitted or stored without any suspicion. The hidden data can then be later retrieved by using the same tool to unload the payload file, and separate the payload from the carrier, making the two original files separate once more.
Tools that will be used for Steganography will include: Xiao for the most basic Steganography. Then OpenPuff will be used for password protect payloads, to see if the forensics kit can recover the file and be able to decrypt the protection. Then OpenPuff with obfuscation and password protected will be implemented as well to see how the toolkits can handle this built in security.

### Slack Space

One of the biggest and most common ways to hide data in hardware is the topic of slack space. Slack space is well known when looking into computer architecture, and how data is stored in computer hardware. To talk about slack space, we must first look into how files are stored in the hardware. Memory that is saved to disk is saved in chunks known as blocks. These blocks are all the same size, and saved information can span multiple blocks until the information is completely stored. This is paired then with paging, but that is not involved in the slack space hiding. What happens is that a program/file will very rarely fill a block, and there is almost always left over space in the block. This unused area, known as slack space, is filled with null values to the end of the block allocated. The area filled with null values can be overridden to actual hide information.

The current hope is to find a tool such as Slacker.exe that was a part of the Metasploit MAFIA tools to hide data. However, there are currently no download links or pages that allow MAFIA or Slacker to be downloaded. I have reached out to William Mahoney to see if he has this tool or has another idea, and will continue to see if there are any tools I can find to do this type of data hiding. Depending on what we can find in research, this may or may not be implemented in the hidden data VM.

### Fake File System

Deniable encryption could be an option for a user using a fake file system to combat forensics. The idea here is that users may convincingly deny that a given piece of data is encrypted, or that they are able to decrypt a given piece of encrypted data, or that encrypted data even exists in the first place. 
What I plan to do is to have the normal file-system untouched, and then make another filesystem that is all encrypted. That second filesystem that is encrypted can be used to claim that we do not know how to decrypt the encryption, and we can see what the toolkits will be able to detect and recover. I will use the free project LibreCrypt to attempt this.
https://github.com/t-d-k/LibreCrypt/blob/master/README.md