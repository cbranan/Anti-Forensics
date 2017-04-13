# Data Deletion Toolkit Evaluation Form

*Evaluator: Casey Branan*

*Forensics Toolkit: SANS SIFT* 

Preston Wells

Capstone IASC-4580

Forensics Tool Analysis Team

### Purpose

The purpose of this is to test the analysis component of each of our forensic toolkits. Since the user story we will be testing is “As a **Computer Forensic Analyst**, I want to **detect and recover deleted data** so I can **support/define a suspect's intent**”, we will be analyzing and determining what the forensic toolkits miss or fail to recover. The deleted VM that we will be running our toolkits against has eight seperate files that were saved in various locations and then different tools were then used to deleted all eight of these files.

### File Deletion

File1_CC.txt - Text file deleted with CCleaner.

| Deleted File Not Found | Reference to File Found | Partial Recovery | Full Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

File2_SD.txt - Text file deleted with SDelete.

| Deleted File Not Found | Reference to File Found | Partial Recovery | Full Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

File3_3P.txt - Text file deleted with Air Force 5020.

| Deleted File Not Found | Reference to File Found | Partial Recovery | Full Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

File4_7P.txt - Text file deleted with Schneier 7 pass.

| Deleted File Not Found | Reference to File Found | Partial Recovery | Full Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

File5_PCC.png - Image file deleted with CCleaner.

| Deleted File Not Found | Reference to File Found | Partial Recovery | Full Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

File6_PSD.png - Image file deleted with SDelete.

| Deleted File Not Found | Reference to File Found | Partial Recovery | Full Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

File7_P3P.png - Image file deleted with Air Force 5020.

| Deleted File Not Found | Reference to File Found | Partial Recovery | Full Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

File8_P7P.png - Image file deleted with Schneier 7 pass.

| Deleted File Not Found | Reference to File Found | Partial Recovery | Full Recovery |
|---|---|---|---|
|   | **X(1)**  |   |   |

Comments:

8/24

Overall, SIFT 

the SluethKit command fls -rd	lists out all of the MFT for NTFS entries and tells me information about the deleted files. However, none of the recovery worked. This is mainly because overwritten data, even just one pass, has not been recovered by anyone. There are articles about STM microscopy being able to detect a zero that overwrote a one or vice-versa, but so far none of these have lead to actual forensic recovery. In fact, this is all theoretical and has varying degrees of reliability.  
