# Final Report

#### Table of Contents
- [Assessment Summary](#assessment-summary)
- [Findings Summary](#findings-summary)
    - [Scoring](#scoring)
    - [Section 1: Data Hiding](#data-hiding)
    - [Section 2: Data Deletion](#data-deletion)
    - [Section 3: Data Alteration](#data-alteration)
    - [Results](#results)

### Assessment Summary

The overall goal of the project was to test and evaluate the performance of popular forensic toolkits against anti-forensic techniques. The beginning of our project started with researching and selecting the forensic toolkits that we would evaluate: Sans SIFT, Caine and DFF. Once the set of toolkits had been selected, we identified and researched the tools and techniques surrounding three categories of anti-forensics: Data Hiding, Data Destruction and Data Alteration ([Associated Research](/Documentation/Research/)). Once all research had been conducted, the particular anti-forensic tools and techniques were leveraged to construct a stand-alone virtual machine which would serve as our platform for evaluating each of the forensic toolkits ([Virtual Machine Setup](/Documentation/VM/)) ([Evaluation Template](/Documentation/Evaluation/)). Following the setup of these systems, each of the chosen toolkits were used to analyze the virtual machine's image. With these results recorded, we took our findings from each of the tests and created reports that evaluated the performance of these toolkits in countering anti-forensics techniques that we used ([Resulting Reports](/Documentation/Reports/)).

### Findings Summary

#### Scoring
For each task, points ranging from (0-3) are given depending on how well the toolkit performs. Zero points are awarded where the toolkit does not acknowledge the existence of the specified file. One point is awarded if the existence of the file is acknowledged and the file reference is recovered. Two points will be awarded if the piece of data not only exists, but also is indicated as suspicious and/or part of the original/injected contents. Finally, three points are awarded if the toolkit captured the full original/injected contents.

#### Data Hiding
|                                   | SIFT | DFF | CAINE 7 |
| ---                               | --- | --- | --- |
| **Steganography Content Recovery**| | | | 
| *- MTG1 bitmap file*              | 1 | 1 | 1 |
| *- Adema-Giving in MP3*           | 1 | 1 | 1 |
| *- Sugar Ray-Fly MP3*             | 1 | 1 | 1 |
| *- Disturbed Stupify MP3*         | 1 | 1 | 1 |
| *Subtotal*                        | 4/12(33%) | 4/12(33%) | 4/12(33%) |
| **Slack Space Recovery**          | | | |
| *- Xiao Stenography Executable*   | 1 | 1 | 1 |
| *Subtotal*                        | 1/3(33%) | 1/3(33%) | 1/3(33%) |
|**Alternate Data Streams Recovery**| | | |
| *- nothinghere.txt:dontopen.txt*  | 3 | 3 | 3 |
| *- test:hiddendir.txt*            | 3 | 3 | 3 |
| *Subtotal*                        | 6/6(100%) | 6/6(100%) | 6/6(100%) |
| **Total Score:**                  | **56%** | **56%** | **56%** |

#### Data Deletion
|                           | SIFT | DFF | CAINE 7 |
| ---                       | --- | --- | --- |
| **Deleted File Recovery** | | | | 
| *- File1_CC.txt*          | 1 | 1 | 1 |
| *- File2_SD.txt*          | 1 | 1 | 1 |
| *- File3_3P.txt*          | 1 | 1 | 1 |
| *- File4_7P.txt*          | 1 | 1 | 1 |
| *- File5_PCC.png*         | 1 | 1 | 1 |
| *- File6_PSD.png*         | 1 | 1 | 1 |
| *- File7_P3P.png*         | 1 | 1 | 1 |
| *- File8_P7P.png*         | 1 | 1 | 1 |
| *Subtotal*                | 8/24(33%) | 8/24(33%) | 8/24(33%) |
| **Total Score:**          | **33%** | **33%** | **33%** |

#### Data Alteration
|                               | SIFT | DFF | CAINE 7 |
| ---                           | --- | --- | --- |
| **Corrupt Data Recovery**     | | | | 
| *- hidden.pdf*                | 3 | 3 | 3 |
| *- credentials.7z*            | 1 | 1 | 3 |
| *- key.jpg*                   | 3 | 1 | 1 |
| *Subtotal*                    | 7/9(78%) | 5/9(56%) | 7/9(78%) |
| **Timestamp Recovery**        | | | |
| *- entrance.txt*              | 3 | 2 | 1 |
| *Subtotal*                    | 3/3(100%) | 2/3(67%) | 1/3(33%) |
| **Encrypted Volume Recovery** | | | |
| *- coolstuff*                 | 1 | 1 | 1 |
| *- plans*                     | 1 | 1 | 1 |
| *- phases*                    | 1 | 1 | 1 |
| *Subtotal*                    | 3/9(33%) | 3/9(33%) | 3/9(33%) |
| **Total Score:**              | **70%** | **52%** | **48%** |

#### Results
|                               | SIFT | DFF | CAINE 7 |
| ---                           | --- | --- | --- |
| *Section 1: Data Hiding*      | 56% | 56% | 56% | 
| *Section 2: Data Deletion*    | 33% | 33% | 33% |
| *Section 3: Data Alteration*  | 70% | 52% | 48% |
| **Total Score:**              | **53%** | **47%** | **46%** |

### Analysis Summary

After evaluation of anti-forensic impact on out forensic toolkits, we discovered several Universal Deficiencies that need to be addressed. A major weakness in each of our toolkits was that there is no support for steganalysis. As a result, and carrier files were not found to contain hidden information, meaning that the hidden data was never implied or discovered. Our toolkits universally struggled with slack space if the data was not hidden in unallocated space. By using any hex editor and a program to find the end of the used file, anyone can write data in slack space at the end of the file and go undetected. 

Our tools had deleted data support, however, society's technological limitations does not have an answer to overwritten data. As a result, all of the anti-forensic techniques involving different overpasses became unrecoverable globally. Cryptanalysis is also a major weakness, as our tools could find the volumes but had no way to detect they were encrypted or break the encryption to recover the data. Finally, these forensic toolkits need a way to find and recover changes to meta data and file signatures to recovery the actual data.
