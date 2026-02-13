## Task 1: Create Users  
- Command :- sudo useradd -m username -p password      
<img width="472" height="211" alt="image" src="https://github.com/user-attachments/assets/e4159d76-2e6e-410b-b1ef-2a19ad7e9d88" />    

- command :- egrep 'tokyo|berlin|professor' /etc/passwd //user egroup to show all users in single command  
<img width="506" height="104" alt="image" src="https://github.com/user-attachments/assets/d6fccb2e-b337-45c5-ae90-c08b2cd83dc7" />    

- **changed deafult shell to bin bash** - sudo usermod -s /bin/bash username 
<img width="462" height="103" alt="image" src="https://github.com/user-attachments/assets/9c3c4e3f-f379-4712-b71d-0f7cabd3bc71" />


## Task 2: Create Groups
- sudo groupadd group name  
<img width="388" height="184" alt="image" src="https://github.com/user-attachments/assets/00829792-33bf-4482-a2a1-8e604850d193" />  
 
 - cat /etc/group |tail -10  
<img width="504" height="64" alt="image" src="https://github.com/user-attachments/assets/662499f2-464b-4d0f-ac03-6e974aafa36a" />

 cat /etc/group | tail -8  
<img width="367" height="147" alt="image" src="https://github.com/user-attachments/assets/b11e8f73-2724-406b-af1b-ced9479a8393" />

## Task 3: Assign to Groups
command :   
1.sudo usermod -aG developers,admins berlin   
2.sudo gpasswd -a professor admin  
<img width="497" height="37" alt="image" src="https://github.com/user-attachments/assets/47cb35e1-767c-49e9-8a13-7edad8c6dba2" />   

## Task 4 Shared Directory  
<img width="466" height="216" alt="image" src="https://github.com/user-attachments/assets/da3d3e1d-387d-4b15-816f-31240a54f4e7" />  

Able to create file with tokyo user but not with berlin  

<img width="430" height="183" alt="image" src="https://github.com/user-attachments/assets/88967dfa-c5e1-41af-8adc-38515040f626" />  

Berlin  
<img width="479" height="63" alt="image" src="https://github.com/user-attachments/assets/7cc6ade8-2b8c-4eb8-b237-d3e2bcb5db3c" />  


## Task 5: Team Workspace    
**sudo useradd -m nairobi  
groupadd project-team**  
<img width="403" height="78" alt="image" src="https://github.com/user-attachments/assets/3411f482-ea53-435a-839b-0eac0af42316" /> 

**sudo usermod -aG project-team tokyo  
sudo usermod -aG project-team nairobi  
sudo mkdir /opt/team-workspace  
sudo chgrp project-team team-workspace  
sudo chmod 775 team-workspace  
sudo su - nairobi**  
**touch /opt/team-workspace/task5.txt**  

<img width="500" height="424" alt="image" src="https://github.com/user-attachments/assets/109a6c07-10c6-4f9c-9fa8-cec558130a8f" />

