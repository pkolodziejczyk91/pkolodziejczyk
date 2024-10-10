1.Run Live Forensicator using the "-EVTX EVTX" flag. Open the created output .HTML files in Chrome. According to Live Forensicator, which user accounts were locked out? (Alphabetical order) (3 points)
Administrator, Brittany.Song, John.Raymond, ServiceAccount
![image](https://github.com/user-attachments/assets/329c892f-c4ed-4a85-a3bd-6f2bdaa92419)


2. Review the Lockout Policy on the machine. What is the number of failed logons before an account is locked, and what is the lockout duration? (3 points)
10, 10
![image](https://github.com/user-attachments/assets/c3a85e98-374a-4217-886d-c9baf0404eb7)

4. Which accounts were successfully accessed during the bruteforce attack? (3 points)
Claire.Daniels, ServiceAccount

6. What is the IP address that conducted the bruteforce attack and accessed these accounts, and what country is it associated with? (3 points)
82.2.66.222, GB
![image](https://github.com/user-attachments/assets/2f44ff2b-d080-4a9d-b30c-0d2e981a7d03)
![image](https://github.com/user-attachments/assets/b3bd370b-db5b-4d81-8ba2-f305d42fb17e)


8. What account is created by the attacker, what is the Time associated with this activity according to Live Forensicator? (3 points)
ServiceAccountBackup 8/26/2022 3:13:02PM
![image](https://github.com/user-attachments/assets/453a4e3b-a9b7-4ec4-a023-f769eaa37831)

10. Use Chainsaw with the -r flag and point the tool at the Live Forensics EVT output folder to further investigate the RDP bruteforce activity. How many failed logins are detected across all affected accounts? (3 points)

11. What local accounts were NOT targeted in this attack, according to Chainsaw's output for Login Attacks? (Only include accounts that are likely used by humans! and no, don't include BTLO!) (3 points)

12. Using Live Forensicator, identify the script that the attacker attempted to use for persistence. Submit the filepath and filename (Hint: Think about the account that is actively being used by the attacker to identify the right file!) (3 points)

13. What are the contents of the script file? (3 points)

14. We can't always trust the output from our tools. Manually investigate the machine's Run, RunOnce, RunServiceOnce registry keys. List the keynames where the persistence script is being executed (3 points)

15. Run Live Forensicator again using the flag to get browser history. Look at the BROWSING_HISTORY directory first, focusing on history from the compromised account used by the attacker. Three websites are a concern for data exfiltration, what are the URLs? (Alphabetical order based on subdomain or domain) (4 points)

16. Look at Live Forensicator's BrowserHistory.html output and search through the results for Pastebin. What is the URL that contains exfiltrated company data? (4 points)

17. Visit this page directly (or if it is removed, use web.archive.org). How many rows of data have been exfiltrated by the attacker? (4 points)

18. Revisiting the malicious script created by the attacker, according to Live Forensicator, what is the creation date for the .ps1 file? (3 points)

19. What is the Last logon value for the attacker manually accessing the compromised account? (Remember, certain persistence mechanisms might log in as the user, so think about the timestamp that makes sense within the timeline) (2 points)

20. Based on the information in the data dump, investigate the files of each user on the system to locate the document. What is the filename, and which account was it stored on? 
