# Task 1: Create Files 
Create empty file devops.txt using touch  
Create notes.txt with some content using cat or echo  
Create script.sh using vim with content: echo "Hello DevOps"  

<img width="610" height="147" alt="image" src="https://github.com/user-attachments/assets/8b4690f0-4289-4b72-9339-c69331de0e10" />  

# Task 2: Read Files
Read notes.txt using cat
View script.sh in vim read-only mode 

<img width="222" height="735" alt="image" src="https://github.com/user-attachments/assets/e6823a94-c37f-40ea-8dda-5c61130cc92c" />    

Display first 5 lines of /etc/passwd using head  
Display last 5 lines of /etc/passwd using tail  
Output for above comamnds    
<img width="426" height="224" alt="image" src="https://github.com/user-attachments/assets/3fd74f0e-7835-4d32-a776-6d879e1ccc1d" />    

# Task 3: Understand Permissions
Format: rwxrwxrwx (owner-group-others)
r = read (4), w = write (2), x = execute (1)

ls -l devops.txt notes.txt script.sh

<img width="434" height="80" alt="image" src="https://github.com/user-attachments/assets/b197db83-3c83-48e9-ae49-2d028ed08986" />  

user & group : Read and write  
others :Only read  

# Task 4: Modify Permissions  
- Make script.sh executable → run it with ./script.sh  
  - command : chmod +x script.sh  
- Set devops.txt to read-only (remove write for all) 
  - Command :chmod -w script.sh  
- Set notes.txt to 640 (owner: rw, group: r, others: none)  
  - command : chmod 640 notes.txt  
- Create directory project/ with permissions 755    
   - mkdir project
   - chmod 775 project/
<img width="431" height="510" alt="image" src="https://github.com/user-attachments/assets/88836031-3002-4957-99c8-abbe44360afd" />

# Task 5: Test Permissions 
- Try writing to a read-only file - what happens?
  -Writing to read only files will give you permission denied error
- Try executing a file without execute permission
   - Executing the file without permission gives permission denied , because the shell required execute bit
     Document the error messages  

  <img width="406" height="198" alt="image" src="https://github.com/user-attachments/assets/b472154b-0b61-457d-ba09-d783cad38be5" />  





