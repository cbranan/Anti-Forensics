# Data Alteration Tool Documentation

Brandon Franklin

Capstone IASC-4580

Forensics Tool Analysis Team

### Trail Obfuscation

In order to distract the investigator and diminish the credibility and quality of artifacts found on the system, a series of techniques can be applied. In order to accomplish this, a given file's data will be modified such that they do not conform with the expectations the investigator may have regarding the types of artifacts they are searching for. This is based on the fact that Forensics Toolkit have to rely on either file extensions or file headers in filtering information in order to identify items immediately relevant to the investigation. In order to diminish the value and authenticity of any artifacts that an investigator may wish to collect as evidence, file metadata and system activity can be modified such that the artifacts do not fit into a timeline, preventing a set of collective information from being merged into a realistic picture.
The intended tools to be used in the obfuscation of the evidence trail include: Attribute Changer to modify the file metadata, Browsing History View to modify web activity, My Last Search to modify search history, built in operating system functionality to modify file extensions, and PE Explorer paired with HxD for file header manipulation.


### Encryption

As investigators are looking to make sense of a system and the contents on it, encryption serves as a major roadblock by converting artifacts into a state in which a significant portion of usable data is made unusable. While Forensic Toolkits may be capable of brute forcing the key used for the encryption depending on the time to decrypt and the selected password, key file based encryption greatly increases the difficulty of such methods given that file data may be required in addition to the password. Another component that serves to counter the act of forensics revolves around the concept of deniable encryption. Through the usage of hidden volumes within an encrypted container, presumably free space may be left undetected by the operating system. In order to handle the cryptographic approach to anti-forensics, VeraCrypt will be used.
