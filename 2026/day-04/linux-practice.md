##  Process commands  
- ps aux |head -5: 5 list running processes

<img width="652" height="98" alt="image" src="https://github.com/user-attachments/assets/6e34d617-dfe2-4e20-8f4c-9f95c1f4fe27" />  

- pgrep -u root sshd :will only list the processes whose name include sshd AND owned by root.  

<img width="330" height="78" alt="image" src="https://github.com/user-attachments/assets/1a39f12d-b75a-4082-b429-cf73adb236b1" />

## Service Account 

- systemctl status ssh : It will shows the status and summary of service SSH

<img width="597" height="190" alt="image" src="https://github.com/user-attachments/assets/c131b197-d6e4-4ef1-ae09-e335d176c823" />

- systemctl list-units |grep acpid.service :- it will print the list units, but used of grep command will show for acpid.service status  
<img width="868" height="54" alt="image" src="https://github.com/user-attachments/assets/c8ea92db-496c-41db-bf4e-37aa154006ce" />

## Log commands
- journalctl -t sshd : Dispaly logs for SSHD service.    
<img width="1168" height="216" alt="image" src="https://github.com/user-attachments/assets/9b86693a-7174-40ad-8457-395b2eab7199" />

- tail -f /var/log/syslog : syslog Contains general system messages and with tail command it is showing last 10 lines  
<img width="900" height="172" alt="image" src="https://github.com/user-attachments/assets/8d933038-4f51-496f-b2da-463fc06444b0" />

- head /var/log/auth.log :auth log contains ercords authentication-related events such as user logins and sudo commands and head command to show first 10 lines  
<img width="1060" height="187" alt="image" src="https://github.com/user-attachments/assets/5b11d32a-45c0-43c2-a992-a64672fc2316" />

## Service for inspection SSH
- systemctl status ssh Checked the status     
<img width="604" height="129" alt="image" src="https://github.com/user-attachments/assets/eba14224-8a3b-487b-b1b1-ef7b0996e499" />
     
- sudo systemctl stop ssh Stopped the SSH     
   <img width="485" height="42" alt="image" src="https://github.com/user-attachments/assets/7b4512e2-6239-4483-8ffd-916bd79e18e1" />
 
- systemctl status ssh: Again checked the status and now it is showing stopped state
  <img width="597" height="115" alt="image" src="https://github.com/user-attachments/assets/26bacd35-7f02-4666-a198-176922349b87" />  

- sudo tail -f /var/log/syslog : checked the syslog file   
<img width="1108" height="166" alt="image" src="https://github.com/user-attachments/assets/c88bc917-aabe-45be-a6be-a02ca52de1bc" />

- started the server and validated the log in  
- sudo systemctl start ssh  
<img width="390" height="28" alt="image" src="https://github.com/user-attachments/assets/8a24707c-eac9-488c-b1a4-e11b5ea27b31" />

- journalctl -u ssh --no-pager | tail -n 20  
<img width="869" height="264" alt="image" src="https://github.com/user-attachments/assets/5283bef1-e004-46ed-8423-53a66d81dbc5" />












