## Environment basics
**command** : uname -a  
**output** :Linux ip-172-31-16-9 6.14.0-1018-aws #18~24.04.1-Ubuntu SMP Mon Nov 24 19:46:27 UTC 2025 x86_64 x86_64 x86_64 GNU/Linux  
**observation**: Shows the linux version

**command** : cat /etc/os-release  
**output** :  
<img width="363" height="153" alt="image" src="https://github.com/user-attachments/assets/348d20c7-0d1e-485e-af43-c11de12b6ffb" />  

**observation**: shows the os release version

## Filesystem sanity  
**command** : mkdir /tmp/runbook-demo  
**output** :succcessfully created  
**observation**: created the directory the temp location and directory name is runbook-demo

**command** :cp /etc/hosts /tmp/runbook-demo/hostcopy && ls -l /tmp/runbook-demo    
**output** :  
<img width="663" height="49" alt="image" src="https://github.com/user-attachments/assets/9d43bdf0-3662-40ee-af21-116e568097b7" />  
**observation**:above command is copied the host file from etc location to newly created directory under temp 
location and also listing the file

## CPU / Memory
**command** :ps -o pid,pcpu,pmem,comm -p $(pidof sshd)
**output** :
<img width="482" height="159" alt="image" src="https://github.com/user-attachments/assets/98be4fb8-cc87-4cb4-8664-7726bdb4d17f" />  
**observation**:it shows the process of sshd id , memory and cpu usage

## Disk / IO  
**command** :free -h  
**output** :
ubuntu@ip-172-31-16-9:~$ free -h  
               total        used        free      shared  buff/cache   available
Mem:           914Mi       384Mi        72Mi       2.7Mi       623Mi       530Mi
Swap:             0B          0B          0B

**observation**: shows the swap memory, how much it is used and available  
**command** :df -h    
**output** :   
<img width="444" height="162" alt="image" src="https://github.com/user-attachments/assets/20fc50fb-61de-4cc3-bcf7-de8c4aa83520" />    
**observation**: display disk file system and also space of mounted file system    
**command** :sudo du -sh /var/log    
**output** :    
ubuntu@ip-172-31-16-9:~$ sudo du -sh /var/log    
53M     /var/log  
**observation**:show the size of var/log directory    
## Network
**command** : sudo ss -tulpn|grep sshd   
**output** :  
<img width="870" height="65" alt="image" src="https://github.com/user-attachments/assets/910e0f06-2f0c-4399-9e86-1e5b8e04a2fb" />  
**observation**SSH is listening on port 22, shows the utility to display socket statics   

**command** :curl -I 34.236.75.31 /ping    
**output** :   
<img width="395" height="124" alt="image" src="https://github.com/user-attachments/assets/f4d59db3-5832-4078-82e2-742b35a3b531" />  
**observation**: 

## Logs   
**command** : journalctl -u  docker -n 50   
**output** :  
<img width="825" height="227" alt="image" src="https://github.com/user-attachments/assets/e0977345-4e8c-4d03-9969-d20bd6dd1b6a" />    
**observation**:  Show the last 50 lines , shows normal installation of docker and no error      

**command** :  tail -n 50 /var/log/auth.log 
**output** : <img width="962" height="223" alt="image" src="https://github.com/user-attachments/assets/9390756a-8022-48f6-b386-e69e5f89c0ba" />  
 **observation**: showing logs for  authentication login and user and group related to docker.
