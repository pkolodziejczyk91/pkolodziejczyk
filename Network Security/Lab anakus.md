https://blueteamlabs.online/home/investigation/anakus-dfea6f86e0

1. Using Detect it Easy, what is the SHA256 hash of the malware in question, and what language was it written in? Feel free to utilize VirusTotal to garner more information (Format: SHA256, Language)
FB20FC4E474369E6D8626BE3EF6E79027C2DB3BA0A46F7B68C6981D6859D6D32, C++
![image](https://github.com/user-attachments/assets/b110820e-a5e1-4dfa-bd50-05f75c33d0d9)
![image](https://github.com/user-attachments/assets/0da90ba6-ce0c-4bd1-b5a6-294c21a549ff)

2. The total entropy value in Detect it Easy gives us a general indication of the randomness across the entire file, but the presence of a highly entropic-packed section indicates a portion of the file containing data that has been compressed—packed. Usually, an entropy above 7.2 is considered malicious, what is the name of this section in question? (Format: .xxxx)
.rsrc
![image](https://github.com/user-attachments/assets/223e1119-03d5-430a-94a4-cc013a87bb5f)

3. Given the file’s entropy level, reputation on VirusTotal, and weird characteristics, it is clear that is malicious. However, attackers will sometimes use the names of security companies in their malware to bypass detection. In this case, what product name is this malware impersonating?
Sophos Anti-Virus
![image](https://github.com/user-attachments/assets/fe955422-a074-4701-9b53-8f7a8bdcf784)
![image](https://github.com/user-attachments/assets/36ae4735-3924-4e5c-957d-cfe69ac1f0e2)

4. Using SigCheck, let's see if the file has been signed with a code-signing certificate—proving its validity. Include the “Verified” status and “Signing date” also known as Link Date (Format: Status, X:XX PM X/X/XXXX)
Unsigned, 4:59 PM 9/1/2022
![image](https://github.com/user-attachments/assets/1c68d777-2190-44d7-8a07-e4c1262711ca)

5. Let’s look at the alleged malware “hataker.exe”. Judging from its hash, it is not apparent on most malware platforms—albeit, it does not exclude its maliciousness. Turn on Windows Defender and run the malware until it picks it up. What is the name given to this alleged, malicious trojan-type program? (Format: Trojan:full name)
Trojan:Win32/Meterpreter.RPZIMTB  
![image](https://github.com/user-attachments/assets/c9a08502-eddf-4515-ad15-d99f26de1d20)

6. Interestingly, now knowing the trojan type for the “hataker.exe”, we can safely assume the attacker was planning to initiate a connection from the victim’s endpoint to its command and control server. What is this method called? (Format: Xxxxxxx Xxxxx)
Reverse Shell

7. Sticking to the same context, let’s dissect the malware further. What dynamic domain is the malware “hataker.exe” using to establish a connection back to the attacker’s system? (Format: Domain name)
0.tcp.ngrok.io
![image](https://github.com/user-attachments/assets/a8c2640c-e2dc-4ffa-8c78-31ced40919b3)

8. Using Timeline Explorer, look at the “Threat Logs” from the incident, how many high-risk alerts were tracked? (Format: Count)
6
![image](https://github.com/user-attachments/assets/51a4f2a3-5b12-427d-9062-914b8d04c390)

9. What are the two “Rule Titles” with the highest count under the high-risk alerts level group—in respective order? (Format: Rule Title 1, Rule Title 2)
Important Log File Cleared, Important Windows Service Terminated WIth Error
![image](https://github.com/user-attachments/assets/a091238c-2765-4242-91ae-871d896daf03)


10. Examine the last “Rule Title” for the high-risk alerts level group: what MITRE ID does this correspond to and what is the TgtGrp in question? (Format: TechniqueID, TgtGrp)
T1098, Administrators
![image](https://github.com/user-attachments/assets/9b1b38f7-26ea-46c3-abff-140209f8031f)


11. Looking at the medium-risk level alerts, what is the “Rule Title” and count of the popular alert group? (Format: Rule Title, Count)
Potentially Malicious PwSh, 457
![image](https://github.com/user-attachments/assets/2c5c00e9-0494-4919-8266-44946ebcc515)


12. What module was used for the password spray attack? Lists its MITRE ID for this type of attack as well (Format: powershell-module, TXXXX.xxx)
Invoke-LocalPasswordSpray, T1110.003
![image](https://github.com/user-attachments/assets/b280fbfb-a04a-47ef-920f-82dd68a7b9fe)

