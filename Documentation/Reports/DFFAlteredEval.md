# Data Alteration Toolkit Evaluation Form

*Evaluator:* Brandon Franklin

*Forensics Toolkit:* Digital Forensics Framework

Brandon Franklin

Capstone IASC-4580

Forensics Tool Analysis Team

### Purpose

The purpose of this is to test the analysis component of each of our forensic toolkits. Since the user story we will be testing is “As a **Computer Forensic Analyst**, I want to **identify and understand system contents** so I can **develop an overview of user activity**”, we will be investigate the ability of forensic toolkits to analyze and recover manipulated system contents. Such anti-forensic techniques involving the manipulation of system contents for the goal of trail obfuscation have been applied to the altered VM which will serve as a baseline for identifying the toolkit's ability to counteract such techniques.

### Type Manipulation
hidden.pdf file - JPG file displaying hidden password

| File Not Recovered | File Recovered | Actual Type Identified | File Contents Recovered |
|---|---|---|---|
|   |   |   |  X(3) |

Comments: Detected as jpg image, able to display image

credentials.7z - 7Zip file containing text

| File Not Recovered | File Recovered | Actual Type Identified | File Contents Recovered |
|---|---|---|---|
|   | X(1)  |   |   |

Comments: Detected as a jpg image, unable to display

key.jpg -  GIF file displaying secret password

| File Not Recovered | File Recovered | Actual Type Identified | File Contents Recovered |
|---|---|---|---|
|   | X(1)  |   |   |

Comments: Detected as a jpg image, unable to display

### Timestamp Manipulation
entrance.txt - Text file containing message created 3/28/2017 6:40:34 PM

| File Not Recovered | File Recovered | Change to Timestamp Detected | Original Timestamp Determined |
|---|---|---|---|
|   |   | X(2)  |   |

Comments: Able to see time within time frame under MFT modification time of 3/29, all other timestamps pointed to the fake date of June 16th, 2017

### VeraCrypt

coolstuff - KeyFile protected volume containing a list of sites

| Volume Not Recovered | Volume Recovered | Partial Content Recovery | Full Content Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments:

plans - Password protected volume containing a list of plans

| Volume Not Recovered | Volume Recovered | Partial Content Recovery | Full Content Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments:

phases - KeyFile & Password protected volume containing secret messages

| Volume Not Recovered | Volume Recovered | Partial Content Recovery | Full Content Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments:

### Summary:

DFF is provided as a standalone application which provides both graphical and command line access to its forensic capabilities.

Designed to capture information immediately available in the file system and in memory, DFF provides some functionality in the way of identifying modified data and remedying it. Such capabilities do not carry over to changes in the header data as the toolkit was unable to render the contents of these files. Given the graphical nature of DFF, the file that was able to be recovered was simply displayed as the original jpg.

For handling of timestamps, while the associated meta-data displayed in the graphical view of the toolkit did not contain the original time within the list of timestamps, a single field of the MFT modification time of 3/29/17 which clearly differed from the 6/16/17. From this, it was immediately identifiable that modifications had been made to the original timestamps.

Little functionality exists in the detecting and handling of encrypted volumes. While DFF acknowledged the files as volumes, they were only able to be displayed in the graphical view as individual partitions which consisted of bytes that could not be translated to any sort of file structure.

### Verdict:
DFF's greatest strength appears to be in handling memory and latent artifacts that exist within a system. In the handling of altered data, DFF provides some functionality in the identification of file changes and attributes but lacks cryptographic functionality when it comes to the analysis of a disk volume. Lacking this ability, any crypto related actions could not be counter-acted with DFF simply relaying the fact that they were volumes.

### Results

| Score | Max Possible Score |
|---|---|
| **10** | **21** |