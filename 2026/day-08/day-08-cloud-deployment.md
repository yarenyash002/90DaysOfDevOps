## Connect via SSH : ssh -i "joshbatch10.pem" ubuntu@ec2-18-234-219-90.compute-1.amazonaws.com
<img width="550" height="377" alt="image" src="https://github.com/user-attachments/assets/dd73cb75-8ec5-4515-bd95-de69a9fd3e4a" />

-Install Nginx
- sudo apt update 
- sudo apt upgrade
- sudo apt install nginx

## Configure security groups for web access (port 80 by default for nginx)
Step 1.Security group >edit inbound rule >add port 80> anywhere> save
Step2 : Go to instance>select public ip address>paste it on brower that ip address>WELCOME NGINX  
<img width="1002" height="462" alt="image" src="https://github.com/user-attachments/assets/02f52c19-41c5-4604-9dc7-f08c1b28dfb7" />  

## Extract and save logs to a file
journalctl -u niginx >nginx.log  
Dowloaded to my local  
<img width="1342" height="90" alt="image" src="https://github.com/user-attachments/assets/56164f9d-d0c6-473a-a223-432eee036068" />
