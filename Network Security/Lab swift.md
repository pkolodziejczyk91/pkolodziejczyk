1.Run Live Forensicator using the "-EVTX EVTX" flag. Open the created output .HTML files in Chrome. According to Live Forensicator, which user accounts were locked out? (Alphabetical order) (3 points)
Administrator, Brittany.Song, John.Raymond, ServiceAccount

2. Review the Lockout Policy on the machine. What is the number of failed logons before an account is locked, and what is the lockout duration? (3 points)

3. Which accounts were successfully accessed during the bruteforce attack? (3 points)

4. What is the IP address that conducted the bruteforce attack and accessed these accounts, and what country is it associated with? (3 points)

5. What account is created by the attacker, what is the Time associated with this activity according to Live Forensicator? (3 points)

6. Use Chainsaw with the -r flag and point the tool at the Live Forensics EVT output folder to further investigate the RDP bruteforce activity. How many failed logins are detected across all affected accounts? (3 points)

7. What local accounts were NOT targeted in this attack, according to Chainsaw's output for Login Attacks? (Only include accounts that are likely used by humans! and no, don't include BTLO!) (3 points)

8. Using Live Forensicator, identify the script that the attacker attempted to use for persistence. Submit the filepath and filename (Hint: Think about the account that is actively being used by the attacker to identify the right file!) (3 points)

9. What are the contents of the script file? (3 points)

10. We can't always trust the output from our tools. Manually investigate the machine's Run, RunOnce, RunServiceOnce registry keys. List the keynames where the persistence script is being executed (3 points)

11. Run Live Forensicator again using the flag to get browser history. Look at the BROWSING_HISTORY directory first, focusing on history from the compromised account used by the attacker. Three websites are a concern for data exfiltration, what are the URLs? (Alphabetical order based on subdomain or domain) (4 points)

12. Look at Live Forensicator's BrowserHistory.html output and search through the results for Pastebin. What is the URL that contains exfiltrated company data? (4 points)

13. Visit this page directly (or if it is removed, use web.archive.org). How many rows of data have been exfiltrated by the attacker? (4 points)

14. Revisiting the malicious script created by the attacker, according to Live Forensicator, what is the creation date for the .ps1 file? (3 points)

15. What is the Last logon value for the attacker manually accessing the compromised account? (Remember, certain persistence mechanisms might log in as the user, so think about the timestamp that makes sense within the timeline) (2 points)

16. Based on the information in the data dump, investigate the files of each user on the system to locate the document. What is the filename, and which account was it stored on? 
