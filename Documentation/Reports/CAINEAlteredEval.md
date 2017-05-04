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

Proccess:
Create a Caine VM, and then attach the hard drive that I wanted to inspect to that VM. Once the machine was booted up, I used Guymager to carve the image and save the imaged in a .E0 format. Once the carver was done I then went into the version of autopsy that was on this tool kit and created a new case with the approriate images. Once that case was added, seeing as though for the purpose of this assignment we already new what the names of the files we were looking for were. I just used the file search, to search for the names of the appropriate files. For the first two, once I found them all that I needed to do was click on them and the information that I was looking for appeared in a preview box. For the third one that had a file extension on top of the header change this was not possible. So I looked around in the different tools to see if I could find some tool in the system that would either change the extension back or allow me to just look at the information in the file directly. But, unfortunately there was on such tool. For the time stamp manipulation file I found that file again using autopsy but my toolkit did not have a way to find any of the time stamps that it needed. 
The vera crypt volumes once I found them in autopsy I went and tryied to use any kind of encryption and decryption tool that I had, but all that my toolkit would allow me to do is re-encrypt them and then decrypt the encryption that I just put on them, which did not end up being helpful at all.
