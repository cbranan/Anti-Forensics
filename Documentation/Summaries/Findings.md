# Findings Summary

#### Table of Contents
- [Scoring](#scoring)
- [Section 1: Data Hiding](#data-hiding)
- [Section 2: Data Deletion](#data-deletion)
- [Section 3: Data Alteration](#data-alteration)
- [Results](#results)

### Scoring
For each task, points ranging from (0-3) are given depending on how well the toolkit performs. Zero points are awarded where the toolkit does not acknowledge the existence of the specified file. One point is awarded if the existence of the file is acknowledged and the file reference is recovered. Two points will be awarded if the piece of data not only exists, but also is indicated as suspicious and/or part of the original/injected contents. Finally, three points are awarded if the toolkit captured the full original/injected contents.

### Data Hiding
|                                   | SIFT | DFF | CAINE 7 |
| ---                               | --- | --- | --- |
| **Steganography Content Recovery**| | | | 
| *- MTG1 bitmap file*              | 1 | 1 | 1 |
| *- Adema-Giving in MP3*           | 1 | 1 | 1 |
| *- Sugar Ray-Fly MP3*             | 1 | 1 | 1 |
| *- Disturbed Stupify MP3*         | 1 | 1 | 1 |
| **Slack Space Recovery**          | | | |
| *- Xiao Stenography Executable*   | 1 | 1 | 1 |
|**Alternate Data Streams Recovery**| | | |
| *- nothinghere.txt:dontopen.txt*  | 3 | 3 | 3 |
| *- test:hiddendir.txt*            | 3 | 3 | 3 |
| **Total Score:**                  | **11/21** | **11/21** | **11/21** |

### Data Deletion
|                           | SIFT | DFF | CAINE 7 |
| ---                       | --- | --- | --- |
| **Deleted File Recovery** | | | | 
| *- File1_CC.txt*          | 1 | 1 | 0 |
| *- File2_SD.txt*          | 1 | 1 | 0 |
| *- File3_3P.txt*          | 1 | 1 | 0 |
| *- File4_7P.txt*          | 1 | 1 | 0 |
| *- File5_PCC.png*         | 1 | 1 | 0 |
| *- File6_PSD.png*         | 1 | 1 | 0 |
| *- File7_P3P.png*         | 1 | 1 | 0 |
| *- File8_P7P.png*         | 1 | 1 | 0 |
| **Total Score:**          | **8/24** | **8/24** | **0/24** |

### Data Alteration
|                               | SIFT | DFF | CAINE 7 |
| ---                           | --- | --- | --- |
| **Corrupt Data Recovery**     | | | | 
| *- hidden.pdf*                | 3 | 3 | 3 |
| *- credentials.7z*            | 1 | 1 | 3 |
| *- key.jpg*                   | 3 | 1 | 1 |
| **Timestamp Recovery**        | | | |
| *- entrance.txt*              | 3 | 2 | 1 |
| **Encrypted Volume Recovery** | | | |
| *- coolstuff*                 | 1 | 1 | 1 |
| *- plans*                     | 1 | 1 | 1 |
| *- phases*                    | 1 | 1 | 1 |
| **Total Score:**              | **13/21** | **10/21** | **11/21** |

### Results
|                               | SIFT | DFF | CAINE 7 |
| ---                           | --- | --- | --- |
| *Section 1: Data Hiding*      | 11/21 | 11/21 | 11/21 | 
| *Section 2: Data Deletion*    | 8/24 | 8/24 | 0/24 |
| *Section 3: Data Alteration*  | 13/21 | 10/21 | 11/21 |
| **Total Score:**              | **32/66** | **29/66** | **22/66** |
