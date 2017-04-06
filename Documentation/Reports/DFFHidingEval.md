# Data Hiding Toolkit Evaluation

*Evaluator*: **Brandon Franklin**

*Forensics Toolkit:* **Digital Forensics Framwork**

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
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

#### OpenPuff
MP3 Adema-Giving in - 	Hidden text file with fake credit card number

| Carrier File Not Recovered | Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

MP3 Sugar Ray-Fly -	Hidden text file with a secrete message

| Carrier File Not Recovered | Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

MP3 Disturbed Stupify-	Hidden text file with a secrete message

| Carrier File Not Recovered | Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

### Slack Space

Xiao Stenography Executable	- Hidden confession starting at 00054910h

| Executable Not Recovered | Executable Recovered | Partial Message Recovery | Full Message Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

### Alternate Data Streams

nothinghere.txt:dontopen.txt	- Hidden message

| ADS Not Recovered | ADS Recovered | Partial Message Recovery | Full Message Recovery |
|---|---|---|---|
|   |   |   | **X(3)**  |

Comments:

test:hiddendir.txt - 	Hidden message

| ADS Not Recovered | ADS Recovered | Partial Message Recovery | Full Message Recovery |
|---|---|---|---|
|   |   |   | **X(3)**  |

Comments:

### Summary:

DFF is provided as a standalone application which provides both graphical and command line access to its forensic capabilities. 

Designed to capture information immediately available in the file system and in memory, DFF provides little functionality in the way of detecting and handling steganography. While DFF provides a bitmap and hex view, the only option for attempting to interpret the state of a file is through manual inspection which is not feasible in a time-critical field. As such DFF only managed to capture the files themselves but was unable to provide any information that was embedded in them.

With respect to slack space, with the only option for analysis of slack space within programs was also through the earlier mentioned hex view of the application. Although the tool attempts to capture strings contained within the raw hex, strings of relevance were not detected by this component in this case. While this may aid in the application of searching for text within corrupted files, this provided no benefit as the string entered into the files slack space was not detected.

In the handling of alternate data streams, such contents were made immediately visible as part of the file structure when browsing the disk, making detection of such items trivial.

### Verdict:
DFF's greatest strength appears to be in handling memory and latent artifacts that exist within a system. In the handling of hidden data, DFF provides no distinct functionality in the way of analysis given that any items it did pickup were simply made available as part of the preparation of the disk. While there exist many tools to at least detect steganography on a per file basis, DFF presented no such functionality. Lacking this ability, any steganography related actions went completely unnoticed by the toolkit.

### Results

| Score | Max Possible Score |
|---|---|
| **11** | **21** |
