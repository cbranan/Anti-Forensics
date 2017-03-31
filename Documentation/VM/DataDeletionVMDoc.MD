# Data Deletion VM Documentation

Preston Wells

Capstone IASC-4580

Forensics Tool Analysis Team

### File Creation

First, I created eight seperate files on the virtual test machine. Four of which were text files, the other four were image files with png file extensions. I saved all of these eight files to various locations in the VM to get a better scope of if where the file was stored would affect the forensic analysis toolkit. Each of the four text files all contain a message inside of them that pertains to the tool that was used to delete them from the disk. That way if you can view that message you know that you were able to recover the payload. Alternatley, the image files have pictures that I drew in paint that again pertain to the tool that was used to delete them. 

### Data Deletion

Once I had all eight files in place I used three tools to remove these files. The tools that I used to remove these files were CCleaner, sdelete, and Eraser. With both CCleaner and sdelete, I just used the base usage of them to remove one text file and one image file each. Then with Eraser, this tool comes with 13 different erasure methods ranging from First/Last 16KB erasure to a 35 pass erasure. Since this tool had such a wide variety of erasure options I choose two options from it to eliminate the final four files (two text and two image). The two erasure methods that I choose from Eraser were US Air Force 5020, which is a three pass method, and Schneier seven pass, which from the name you can tell was a seven pass method.

Following the completion of deleting all eight files, I removed all of the programs and tools that I used to delete the files from the machine. I did this step because it made sense that the machine you are analyzing to find deleted files won't neccisarily have the programs that were used to delete the files on it.
