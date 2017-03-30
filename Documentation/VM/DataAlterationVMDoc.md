# Data Alteration VM Documentation

Brandon Franklin
Capstone IASC-4580
Forensics Tool Analysis Team

### Trail Obfuscation
I first used the built in Windows functionality to modify file extensions to modify an image file named "hidden.jpg" and modified renamed the file such that it was changed from "hidden.jpg" to "hidden.pdf".

Next, HxD was used to modify the file signature bytes within the file's header. When modifying the 7z file named "credentials.7z" this required taking the first 6 bytes, 0x37 0x7A 0xBC 0xAF 0x27 0x1C, and replacing them with the signature bytes of a JPG, 0XFF 0xD8 0xFF with the remaining 3 bytes zero'd out.

Both of these modifications were applied to the image "key.gif" in which the gif signature header of 0x47 0x49 0x46 0x38 was replaced with the JPG signature of 0xFF 0xD8 0xFF with the remaining byte zero'd out. Afterwards, the built in Windows renaming functionality was used to rename the file from "key.gif" to "key.jpg".
 
Afterwards, the meta data alteration tool Attribute Changer 8 was used to modify date/time values for Created/Modified/Accessed times for text file "entrance.txt". This was done by loading the file in Attribute Changer and manually updating each of the times from 3/28/2017 6:40:34 PM to 6/15/2017 6:34:05 PM.

### Encryption

In the creation of an encrypted volume, VeraCrypt was used in order to generate a volume protected only be a key file. This was done by using VeraCrypt to create a (standard) encrypted file container named "coolstuff" under C:\Users\John\Documents with AES encryption and SHA-512 hashing with 2MB of space allocated. In order to protect the file, the "Desert.jpg" image under "Sample Pictures" was selected as the key file, with no passphrase chosen. Within this volume, a file named "sites.txt" was generated to act as the actual contents of the volume. FAT FS and default clustering were used in the formatting of the volume.

Pairing the above example with a password, a similar procedure was followed in the creation of a encrypted volume named "plans" under C:\Users\John\Documents with AES encryption and SHA-512 hashing with 5MB of space allocated. The password for the volume was set to "CryptoVera" with the file "Jellyfish.jpg" within "Sample Pictures" selected as the only key file. FAT FS and default clustering were used in the formatting of the volume.

Lastly, VeraCrypt was used to generate an encrypted volume which contained both an outer (visible) volume and an inner (hidden) volume with the volume carrying the name "phases" under C:\Users\John\Documents. For the generation of the outer volume, the encryption algorithm was set to AES with SHA-512 Hashing with 5MB allocated. For this part of the volume, the password was set to 53crE7ToY0u and did not utilize a key file. FAT FS and default clustering were used in the formatting of this volume. For the inner volume, the AES and SHA-512 were also used with only 2MB of the volume allocated to the inner volume. The password for the inner volume was set to EZ1234S6T89Oa and also did not use a key file. FAT FS and default clustering were also used in the formatting of the inner volume. Within the outer volume, two text files "phase1.txt" and "phase2.txt" were placed. Within the hidden, inner volume a text file "phase3.txt" was placed.