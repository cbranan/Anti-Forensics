# Data Alteration Toolkit Evaluation Form

*Evaluator: Casey Branan*

*Forensics Toolkit: SANS SIFT* 

Brandon Franklin

Capstone IASC-4580

Forensics Tool Analysis Team

### Purpose

The purpose of this is to test the analysis component of each of our forensic toolkits. Since the user story we will be testing is “As a **Computer Forensic Analyst**, I want to **identify and understand system contents** so I can **develop an overview of user activity**”, we will be investigate the ability of forensic toolkits to analyze and recover manipulated system contents. Such anti-forensic techniques involving the manipulation of system contents for the goal of trail obfuscation have been applied to the altered VM which will serve as a baseline for identifying the toolkit's ability to counteract such techniques.

### Type Manipulation
hidden.pdf file - JPG file displaying hidden password

| File Not Recovered | File Recovered | Actual Type Identified | File Contents Recovered |
|---|---|---|---|
|   |   |   | **X(3)**  |

Comments: mactime -d hidden.pdf -d -i hour data/tl-hour-sum.txt > timeline.txt  
Then, I saw it was actually a JPG file, so I opened it as a JPG.


credentials.7z - 7Zip file containing text

| File Not Recovered | File Recovered | Actual Type Identified | File Contents Recovered |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

key.jpg -  GIF file displaying secret password

| File Not Recovered | File Recovered | Actual Type Identified | File Contents Recovered |
|---|---|---|---|
|   |   |   | **X(3)**  |

Comments: mactime -d key.jpg -d -i hour data/tl-hour-sum.txt > timeline.txt  
Then, I saw it was actually a GIF file, so I opened it as a GIF.


### Timestamp Manipulation
entrance.txt - Text file containing message created 3/28/2017 6:40:34 PM

| File Not Recovered | File Recovered | Change to Timestamp Detected | Original Timestamp Determined |
|---|---|---|---|
|   |   |   | **X(3)**  |

Comments: mactime -d entrance.txt -d -i hour data/tl-hour-sum.txt > timeline.txt  
Can clearly see all timestamps for the file


### VeraCrypt

coolstuff - KeyFile protected volume containing a list of sites

| Volume Not Recovered | Volume Recovered | Partial Content Recovery | Full Content Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

plans - Password protected volume containing a list of plans

| Volume Not Recovered | Volume Recovered | Partial Content Recovery | Full Content Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

phases - KeyFile & Password protected volume containing secret messages

| Volume Not Recovered | Volume Recovered | Partial Content Recovery | Full Content Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:
13/21  
Overall, SIFT offered no support to Volume, which missed out on a lot of evidence. Luckily, the SIFT using SluethKit helped the investigation a great deal, due to the mactime tool. This allowed me to get a full history on a file and recover the data based off of that history. 
