## Linux Fundamentals: Read and Write Text Files
**Creating a file**  
touch notes.txt  
**Writing text to a file**  
<img width="795" height="41" alt="image" src="https://github.com/user-attachments/assets/f24f8b6e-8444-4526-9e81-d045a371b61e" />    
>- It will overwrite the text and >> it will append the text line means it will add another line  

**Appending new lines**  
yaren@ip-172-31-16-9:~$ echo "I working as oracle dba but transforming my career into Devops">>notes.sh  
yaren@ip-172-31-16-9:~$ echo "Today i am completing my day 6 task">>notes.sh  
yaren@ip-172-31-16-9:~$ echo "I m=am based out of pune">>notes.sh  

**Reading the file back**  
<img width="335" height="234" alt="image" src="https://github.com/user-attachments/assets/4230df2e-3cae-42eb-b283-1283ec07dfdb" />    

yaren@ip-172-31-16-9:~$ **tail** -n 4 notes.txt  
The >> symbol appends new content.  
Practice makes me more confident.  
Soon I will master automation tools.  
DevOps journey is exciting and rewarding.  

Obeservation :- It will fetch last 4 lines of file  
yaren@ip-172-31-16-9:~$ **head** -n 3 notes.txt  
I am learning DevOps step by step.  
Today is my Day 6 task.  
I am based out of Pune.  

Obeservation :- It will fetch first  3 lines of file  

