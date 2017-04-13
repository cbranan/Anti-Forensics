# Data Deletion Toolkit Evaluation Form

*Evaluator:*

*Forensics Toolkit:* 

Preston Wells

Capstone IASC-4580

Forensics Tool Analysis Team

### Purpose

The purpose of this is to test the analysis component of each of our forensic toolkits. Since the user story we will be testing is “As a **Computer Forensic Analyst**, I want to **detect and recover deleted data** so I can **support/define a suspect's intent**”, we will be analyzing and determining what the forensic toolkits miss or fail to recover. The deleted VM that we will be running our toolkits against has eight seperate files that were saved in various locations and then different tools were then used to deleted all eight of these files.

### File Deletion

File1_CC.txt - Text file deleted with CCleaner.

| Deleted File Not Found |Deleted File Found/Not Recovered | Deleted File Found/Partial Recovery | Deleted File Found/Full Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments: For all files, DFF identified each of the links to the files but did not provide file type or file data. Only the file names are visible.

File2_SD.txt - Text file deleted with SDelete.

| Deleted File Not Found |Deleted File Found/Not Recovered | Deleted File Found/Partial Recovery | Deleted File Found/Full Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments:

File3_3P.txt - Text file deleted with Air Force 5020.

| Deleted File Not Found |Deleted File Found/Not Recovered | Deleted File Found/Partial Recovery | Deleted File Found/Full Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments:

File4_7P.txt - Text file deleted with Schneier 7 pass.

| Deleted File Not Found |Deleted File Found/Not Recovered | Deleted File Found/Partial Recovery | Deleted File Found/Full Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments:

File5_PCC.png - Image file deleted with CCleaner.

| Deleted File Not Found |Deleted File Found/Not Recovered | Deleted File Found/Partial Recovery | Deleted File Found/Full Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments:

File6_PSD.png - Image file deleted with SDelete.

| Deleted File Not Found |Deleted File Found/Not Recovered | Deleted File Found/Partial Recovery | Deleted File Found/Full Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments:

File7_P3P.png - Image file deleted with Air Force 5020.

| Deleted File Not Found |Deleted File Found/Not Recovered | Deleted File Found/Partial Recovery | Deleted File Found/Full Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments:

File8_P7P.png - Image file deleted with Schneier 7 pass.

| Deleted File Not Found |Deleted File Found/Not Recovered | Deleted File Found/Partial Recovery | Deleted File Found/Full Recovery |
|---|---|---|---|
|   | X(1)  |   |   |

Comments:

### Summary:

DFF is provided as a standalone application which provides both graphical and command line access to its forensic capabilities.

Designed to capture information immediately available in the file system and in memory, DFF provides some functionality in the way of identifying and recovering deleted files. Given the approach taken in the deletion of these files, without access to memory captures dff was only able to provide reference to the link files associated with each of these files. As such the individual file could be identified by name but the contents could not be referenced as no remnants were detectable by the FTK given that such bytes were overwritten.

### Verdict:
DFF's greatest strength appears to be in handling memory and latent artifacts that exist within a system. In the handling of deleted data, DFF provides functionality in identifying deleted files, but is unable to take any actions beyond identifying file references given that the employed methods overwrite locations where the DFF would otherwise expect to recover data remnants. While DFF may have fared better if provided with a memory dump to recover and persistent data, no actual contents could be recovered based solely on the disk's image.

### Results

| Score | Max Possible Score |
|---|---|
| **8** | **24** |