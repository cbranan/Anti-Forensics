# Data Alteration Toolkit Evaluation Form

*Evaluator: Preston Wells*

*Forensics Toolkit: CAINE 7.0* 

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

Comments: Was able to locate the file then when I looked at a preview of the file it showed the jpg.

credentials.7z - 7Zip file containing text

| File Not Recovered | File Recovered | Actual Type Identified | File Contents Recovered |
|---|---|---|---|
|   |   |   | **X(3)**  |

Comments: Was able to view the ASCII character strings in the file which listed out text.

key.jpg -  GIF file displaying secret password

| File Not Recovered | File Recovered | Actual Type Identified | File Contents Recovered |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments: Was able to find the file but was not able to see the content.

### Timestamp Manipulation
entrance.txt - Text file containing message created 3/28/2017 6:40:34 PM

| File Not Recovered | File Recovered | Change to Timestamp Detected | Original Timestamp Determined |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments: 

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

Score:
11/24

Comments:
For the most part I was able to recover alot of the Type Manipulated data. This toolkit did not however have a good way to deal with the jpg to gif conversion. The VeraCrypt problems, the best that I could do with this kit was recover the volume, I was unable to however to access these volumes. Also, this toolkit didn't have a good tool to deal with timestamp manipulation either.
