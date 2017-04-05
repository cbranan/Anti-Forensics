# Data Hiding Toolkit Evaluation

*Evaluator*: **Preston Wells**

*Forensics Toolkit:* **CAINE 7.0**

Preston Wells

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

MP3 Disturbed Stupify -	Hidden text file with a secrete message

| Carrier File Not Recovered | Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

### Slack Space

Xiao Stenography Executable	- Hidden confession starting at 00054910h

| Executable Not Recovered | Executable Recovered | Partial Message Recovery | Full Message Recovery |
|---|---|---|---|
| **X(0)**  |   |   |   |

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

CAINE 7.0 is in its entirety a computer forensics linux live distribution. 

In this distribution it comes with alot of diffrent tools to do different forensic techniques, unfortunately steganalysis is not one of the capabilities of these tools. Due to this fact I was not able to recover the hidden files in the mp3 and bitmap files. 

As far as the slack space goes, the main way that CAINE analzes this is using Xall 1.5. The problem that I ran into was, that when I tried to use this program on the carved image it would not work properly. Meaning you could pass it all of the correct information but it would not return anything and would seemingly just stop in the middle of the proccess. Since this was happening I was unable to do much analysis on the slack space at all and so wasn't able to recover the executable that was hidden there.

Finally, for the alternate data streams it just came down to looking for the \*:\*.txt in the file system. Which since CAINE has a older version of Autopsy built into it, made for easy searching of that kind of reference. Once that was found the messages were right there in plaintext.  

### Verdict:

CAINE 7.0 is actually just a distro of Ubuntu with some forensics tools on it, but it doesn't contain an entire forensic tookit. For hidden data, any steganography will go missed by this toolkit due to its lack of steganalysis tools. Also, any slack space hidden data will be missed if the same kind of problem that I ran into with it not running Xall happens during analysis.

### Results

| Score | Max Possible Score |
|---|---|
| **10** | **21** |
