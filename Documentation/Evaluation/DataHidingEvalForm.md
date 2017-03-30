# Data Hiding Toolkit Evaluation Form

*Evaluator:*

*Forensics Toolkit:* 

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
|   |   |   |   |

Comments:

#### OpenPuff
MP3 Adema-Giving in - 	Hidden text file with fake credit card number

| Carrier File Not Recovered | Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
|---|---|---|---|
|   |   |   |   |

Comments:

MP3 Sugar Ray-Fly -	Hidden text file with a secrete message

| Carrier File Not Recovered | Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
|---|---|---|---|
|   |   |   |   |

Comments:

MP3 Disturbed Stupify-	Hidden text file with a secrete message

| Carrier File Not Recovered | Carrier File Recovered | Partial Payload Recovery | Full Payload Recovery |
|---|---|---|---|
|   |   |   |   |

Comments:

### Slack Space

Xiao Stenography Executable	- Hidden confession starting at 00054910h

| Executable Not Recovered | Executable Recovered | Partial Message Recovery | Full Message Recovery |
|---|---|---|---|
|   |   |   |   |

Comments:

### Alternate Data Streams

nothinghere.txt:dontopen.txt	- Hidden message

| ADS Not Recovered | ADS Recovered | Partial Message Recovery | Full Message Recovery |
|---|---|---|---|
|   |   |   |   |

Comments:

test:hiddendir.txt - 	Hidden message

| ADS Not Recovered | ADS Recovered | Partial Message Recovery | Full Message Recovery |
|---|---|---|---|
|   |   |   |   |

Comments:
