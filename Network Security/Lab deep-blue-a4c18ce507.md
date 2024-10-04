https://blueteamlabs.online/home/investigation/deep-blue-a4c18ce507

1. Using DeepBlueCLI, investigate the recovered Security log (Security.evtx). Which user account ran GoogleUpdate.exe?
Mike Smith
![image](https://github.com/user-attachments/assets/3a331863-756c-4fa9-b22c-37c21dc90e64)

2. Using DeepBlueCLI investigate the recovered Security.evtx log. At what time is there likely evidence of Meterpreter activity?
4/10/2021 10:48:14
![image](https://github.com/user-attachments/assets/5e5873dc-e375-4a8e-a6b0-ddb16fffd24a)

3. Using DeepBlueCLI investigate the recovered System.evtx log. What is the name of the suspicious service created?
rztbzn
![image](https://github.com/user-attachments/assets/c65a15d5-d2d7-455a-857d-2842c10c8558)

4. Investigate the Security.evtx log in Event Viewer. Process creation is being audited (event ID 4688). Identify the malicious executable downloaded that was used to gain a Meterpreter reverse shell, between 10:30 and 10:50 AM on the 10th of April 2021
Mike Smith, serviceupdate.exe
![image](https://github.com/user-attachments/assets/f9163717-261c-452e-ac16-b0f1b2a65ec8)

5. It's also believed that an additional account was created to ensure persistence between 11:25 AM and 11:40 AM on the 10th April 2021. What was the command line used to create this account? (Make sure you've found the right account!)
net1 user ServiceAct /add
![image](https://github.com/user-attachments/assets/d82e3367-2ad1-42f1-97a0-559ffd632beb)

6. What two local groups was this new account added to?
Administrators, Remote Desktop Users
![image](https://github.com/user-attachments/assets/b7e8286d-7646-4465-b5bd-b81a7a6bf73e)
![image](https://github.com/user-attachments/assets/9a43be0c-f7c7-4993-acc1-c4f630f1effb)


