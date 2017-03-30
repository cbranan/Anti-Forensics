# Data Hiding VM Documentation

Casey Branan

Capstone IASC-4580

Forensics Tool Analysis Team

### Alternate Data Streams

I created a file titled nothinghere.txt that only contained the text “blank”. I then created an ADS as nothinghere.txt:dontopen.txt that contains a secrete message. I then created a directory called testdir, and created no files for that directory so it appears empty. I then created an ADS titled test:hiddendir.txt with a secret message also.

### Steganography

I used the Xiao tool to inject the secret phrase “Chicken Turtle Bird” into the carrier file MTG1 with RC2 and MD5 as options and a password of “MTG” to test for image steganography.
Up next, I used the more robust tool OpenPuff to inject a fake credit card number into the Song Giving In by Adema with the password “ademagivingin” to test MP3 sound fine steganography. 

Then, I used OpenPuff’s option to have 2 active passwords to inject a file into Sugar Ray’s MP3 song Fly with the passwords “sugar ray” and “wanttofly”.
Finally, I used OpenPuff to inject a file into the Disturbed MP3 song Stupify, and turned on the scrambling feature of OpenPuff with the passwords “hidedata” and “scrambling”.

### Slack Space

I downloaded the PE Browse application to view the Xiao Steganography tool. I found that the first hex location no data is stored by Xiao was at 452A1A, and that I could hide data in the slack space from there till the end of file. I then downloaded a hex editor, and went into the slack space. At hex location 00054910h, I wrote a secrete message into the slack space.
