https://blueteamlabs.online/home/investigation/foxy-45e69136ae

1. The SOC recently observed network connections from 3 internal hosts towards hxxp://45.63.126[.]199/dot.gif (URL has been sanitized). What is this activity likely related to?
CobalStrike
![image](https://github.com/user-attachments/assets/9d366533-7f7a-4d37-80b6-77e09280e978)

2. How many URLs are using the same endpoint 'dot.gif', across all export files? (include duplicates)
568
![image](https://github.com/user-attachments/assets/4eedcf13-2d9f-455c-beef-f274f8f40958)

3. The SHA256 hash of a file was detected and quarantined on one of the Executives old android phones. We are trying to work out what this file does so we can take next steps.
The hash value is 6461851c092d0074150e4e56a146108ae82130c22580fb444c1444e7d936e0b5. Is this file associated with malware? If so, what is the malware name? (as stated by Malware Bazaar)
IRATA
![image](https://github.com/user-attachments/assets/2e1d3986-6450-49c1-a9ec-21f2de453d00)
![image](https://github.com/user-attachments/assets/09ac584e-5a79-403f-aa72-dc5257a1187b)

4. Investigate the reference link for this SHA256 hash value. Submit the threat name (acronym only), the C2 domain, IP, and the domain registrar.
IRATA, uklivemy[.]gq, 20.238.64.240, freenom
![image](https://github.com/user-attachments/assets/d09b4b6a-6377-440a-866d-b39fad0a3188)

5. Visit https://www.joesandbox.com/analysis/1319345/1/html. Investigate the MITRE ATT&CK Matrix to understand the Collection activities this file can take, and what the potential impact is to the Executives work mobile phone.
Submit the 5 Technique names in alphabetical order: 
Access Contact List, Access Stored Application Data, Capture SMS Messages, Location Tracking, Network Information Discovery

6. A junior analyst was handling an event that involved outbound connections to a private address and didn't perform any further analysis on the IP. What are the two ports used by the IP 192.236.198.236?
1505, 1506
![image](https://github.com/user-attachments/assets/b857a478-724e-4fd4-84e6-f1fe92b6103f)

7.Use the reference to help you further research the IP. What is the C2 domain?
ianticrish[.]tk

8. What is the likely delivery method into our organization? Provide the Technique name and Technique ID from ATT&CK.
Phishing, T1566
![image](https://github.com/user-attachments/assets/7a85f8e8-9e62-49cd-b111-038b346301dc)


10. Investigate further and try to find the name of the weaponized Word document, so we can use our EDR to check if it is present anywhere else within the organization.


12. What is the name of the .JAR file dropped by the Word document?

13. Executives have expressed concern about allowing employees to visit Discord on the corporate network because of online reports that it can be used for malware delivery and data exfiltration. 
Investigate how Discord can be abused for malicious file storage/distribution! What is the URL of the Discord CDN, ending with /attachments/?

14. Looking at all export files, how many rows reference this URL? (include duplicates)

15. Based on this information, what is the name of the malware family that is being widely distributed via Discord?

16. We can proactively use indicators from threat feeds for detection, or for prevention via blocking. When it comes to blocking indicators, it is crucial that they are from a reputable source and have a high level of confidence to prevent blocking legitimate entities.
How many rows in the full_urls.csv have a confidence rating of 100, and would likely be safe to block on the web proxy?

17. An analyst has reported activity coming from an IP address using source port 8001, but they don't understand what this IP is trying to achieve. Looking at full_ip-port.csv in Gnumeric, filter on malware_printable = Unknown malware, and find an IP that is using port 8001. What is the IP address value?

18. Investigating the reference material, what is the CVE ID of the vulnerability that this IP has been trying to exploit? And what is the industry nickname for this vulnerability?
