# Data Hiding Toolkit Evaluation

*Evaluator*: **Casey Branan**
*Forensics Toolkit:* **SANS SIFT Forensic Toolkits**

Casey Branan
Capstone IASC-4580
Forensics Tool Analysis Team

### Purpose

The purpose of this is to test the analysis component of each of our forensic toolkits. Since the user story we will be testing is “As a **Computer Forensic Analyst**, I want to **detect and recover hidden data** so I can **spot trails of evidence**”, we will be analyzing and determining what the forensic toolkits miss or fail to recover. The hidden VM that we will be running our toolkits against has the anti-forensic techniques implemented on it. This means that our toolkit evaluation will show which tools/techniques effectively threaten and possibly even defeat the forensic toolkit user story.

### Findings

These findings tables are broken down into four sections on how well the forensic toolkit worked to fulfill the user story as a whole. The tables are worth points ranging from (0-3) depending on how well the toolkit performs. Zero points are awarded for the first section, where the toolkit does not even have the existence of the carrier, executable, or alternate data stream. One point is awarded for if that piece of data exists, but the analysis does not indicate it is suspicious or there is something hidden. Two points will be awarded if the piece of data not only exists, but also is indicated as suspicious and/or part of the hidden data is recovered. Finally, three points are awarded if the toolkit has the file, found that something was hidden, and entirely recovered the hidden data into a usable and understandable form.

### Steganography
#### Xiao Tool 
MTG1 bitmap file - Hidden text file with secret phrase “Chicken Turtle Bird”
| Carrier File Not Recovered |Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
| --- | --- | ---| --- |
|   | **X(1)**  |   |   |
Comments:

#### OpenPuff
MP3 Adema-Giving in - 	Hidden text file with fake credit card number
| Carrier File Not Recovered | Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
| --- | --- | ---| --- |
|   | **X(1)**  |   |   |
Comments:

MP3 Sugar Ray-Fly -	Hidden text file with a secrete message
| Carrier File Not Recovered | Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
| --- | --- | ---| --- |
|   | **X(1)**  |   |   |
Comments:

MP3 Disturbed Stupify-	Hidden text file with a secrete message
| Carrier File Not Recovered | Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
| --- | --- | ---| --- |
|   | **X(1)**  |   |   |
Comments:

### Slack Space

Xiao Stenography Executable	- Hidden confession starting at 00054910h 
| Executable Not Recovered | Executable Recovered | Partial Message Recovery | Full Message Recovery |
| --- | --- | ---| --- |
|   | **X(1)**  |   |   |
Comments:

### Alternate Data Streams

nothinghere.txt:dontopen.txt	- Hidden message
| ADS Not Recovered | ADS Recovered | Partial Message Recovery | Full Message Recovery |
| --- | --- | ---| --- |
|   |   |   | **X(3)**  |
Comments:

test:hiddendir.txt - 	Hidden message
| ADS Not Recovered | ADS Recovered | Partial Message Recovery | Full Message Recovery |
| --- | --- | ---| --- |
|   |   |   | **X(3)**  |
Comments:

### Appendix 1:

SANS SIFT comes with the following all installed on set up:
afflib
libbde
libesedb
libevt
libevtx
libewf
libfvde
libvshadow
log2timeline
Plaso
qemu
SleuthKit
ewfacquire
MantaRay Forensics

Out of all of these packages, nothing here is designed for steganalysis of looking for steganography. I first used the famous FTK imager to do a full carve of the hidden VM in the richer AFF forensic format. Next, I put the raw carved version onto the SIFT workstation to begin forensic analysis. 

The lib packages that came with SAN SIFT are specifically designed to allow opening, viewing, and editing of specific and sometimes uncommon files that an investigator may come across during investigations that were not useful to me in my case. Next, the qemu package can be used to take a raw format and covert it to a virtual format to use in a VM environment or vice-versa. I also did not use this, because we are operating under the assumption that the forensic investigator would not have the knowledge of tools, passwords, files, etc. for the steganography; he/she would have to find carrier files and their payloads via steganalysis. Plaso is a tool used to extract timestamps that may be useful for the alteration VM later, but not useful in the current hidden VM evaluation. Ewfacquire is another form of a carver used to gain raw formats for analysis, but not needed since I already had a AFF raw forensic format.

Finally, the evaluation comes down to what can MantaRay and SluethKit forensic tools find. MantaRay had some nice packages built in that could be very useful in an actual forensic investigation. However, the only package I was able to find that was relevant to the steganography we were looking to detect was an exfiltration tool for JPEGs. Unfortunately, the FTK fails even on this level, because the steganography that was done was using MP3 and Bitmap files as carrier files. Sluethkit also fails in this aspect, as none of the built-in packages are designed or able to perform any kind of stainless. 

### Verdict:
The SIFT Workstation at this point seems much less like an FTK and more like a distro of Unbunto that has some nice installed packages that can assist in forensics analysis; much like Kali Linux distro has a few nice tools for security, it does not contain near an entire package to call it a whole security kit. The file carver was able to recover the carrier files, but none of the available tools or packages allowed me to complete any kind of steganalysis to see if there was anything hidden in the few files that existed on the VM. As a result, any basic steganography would go undetected with this standard workstation analysis. 

SIFT received 1 point of each of the 4 hidden files (4 points) out of 12, and scored very poorly in the Steganography section. It scored the poorly with only 1 point in the Slack Space section as well out of 3 points. Finally, SIFT finished strong by fully recovering and receiving all 6 points for the Alternate Data Stream Section. The final point score for SAN SIFT was 11 out of 18.


----------
