
**Part 1: Linux File System Hierarchy**

## Core Directories 

- / (root) - The starting point of everything
   - It is base of entire linux file system
   - It is root directory of root user
   - It holds the highest administrative priviledges.
- /home - User home directories
   - It is user home directory where all users personal data get stored
   - Every user account in a Linux system has its own unique home directory, which provides a private and secure space for the user to work and store their data. 
- /root - Root user's home directory
  - It represent with / and it is top most directory in linux, under this directory all the config files and sys related files tored
  - root directory has authority to modify any file.
  - All other file and directories are sub directories of root.  
- /etc - Configuration files
 -It is brain of Linux system where all the configuration file lives like cat /etc/hosts, /etc/passwd.
  - During startup, your system reads files from /etc to know what services to start and how to configure them. 
- /var/log - Log files (very important for DevOps!)
   - Log directories which has auth log, system logs -
   - used to monitor log during failure occurs, check the server issue quickly 
- /tmp - Temporary files
  - it is directory where temp file get stored
  - OS may auto delete is after reboot, kind of short term files

## Other directories
- /bin - Essential command binaries
  -It stands for "Binary" and it holds the essential commands used to interact with the Operating System.
  -Ex commands found under this directory ls, cp, mv
- /usr/bin - User command binaries
  -Stores all the linux based commands under this directory like useradd,df-h,top etc
- /opt - Optional/third-party applications
   -It is a directory which stores data of application
   - Stores the management data

## 

- du -sh /var/log/* 2>/dev/null | sort -h | tail -5 - 

<img width="524" height="104" alt="image" src="https://github.com/user-attachments/assets/c39f8855-d11b-4dd5-8923-043844968140" />  
Observation :- Top 5 largest files showing in human readable format

- cat /etc/hostname
ubuntu@ip-172-31-16-9:~$ cat /etc/hostname
ip-172-31-16-9
ubuntu@ip-172-31-16-9:~$
Observation :- Showsthe hostname

- ls -la
  <img width="500" height="181" alt="image" src="https://github.com/user-attachments/assets/c86582d3-bc0f-489a-b0c5-e7895f758633" />
  Observation :- Shows the hidden file  


 **Part 2: Scenario-Based Practice** 
 **Example Scenario: Check if a service is running**
 Step 1: systemctl status docker
 Observation :- I will check status of docker that dockert is running or not
 Step 2:- systemctl list-units --type =services
 Obs - It will check service for docker is active, failed or stop
 Step 3:- systemctl is-enabled docker
 Obs - It will shows services are enabled or not for boot, mean it will automatically after reboot  

 # Scenario 1: Service Not Starting

 Step1. systemctl status nginx - It will check the status of nginx (active, stopped)
 step2. system is-enabled nginx - Services are enabled for boot, it will start after reboot or not
 step3. Journalctl -u nginx -n 50 - Shows the logs for last 50 lines 

 # Scenario 2: High CPU Usage
 Step 1: htop
 step2 :
 

