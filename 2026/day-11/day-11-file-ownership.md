# Task 1: Understanding Ownership  

<img width="380" height="94" alt="image" src="https://github.com/user-attachments/assets/1f5ec851-40d3-4078-b980-e2682467b04f" />

*Owner* - Yaren  - The owner is usually who has created the file or directory. Owner can change the permission of file.  
*group* - Yaren  - Group is collection of user who can access the file.  

# Task 2: Basic chown Operations  
1. Create file devops-file.txt 
touch devops-file.txt
2. Check current owner: ls -l devops-file.txt    
<img width="447" height="161" alt="image" src="https://github.com/user-attachments/assets/ecb89f4e-0cbe-427a-b8d3-c98af71d4c66" />    

3. Change owner to tokyo (create user if needed) 
 
 <img width="464" height="147" alt="image" src="https://github.com/user-attachments/assets/ee0f0a7d-4969-4ba7-a7c2-c3da53b4d96e" />    

 In Screenshot we can se owner has been changed from yaren to tokyo  
4. Change owner to berlin

   <img width="438" height="137" alt="image" src="https://github.com/user-attachments/assets/3e93dca6-82b5-480f-a380-68e568df56ce" />  

   Owner ship has been changed from tokyo to berlin

# Task 3: Basic chgrp Operations  

1. Create file team-notes.txt 
touch  team-notes.txt
2. Check current group: ls -l team-notes.txt  

<img width="436" height="144" alt="image" src="https://github.com/user-attachments/assets/aa9030c7-d577-491d-b7db-d59805488224" />  

3. Create group: sudo groupadd heist-team  
sudo groupadd heist-team  
4. Change file group to heist-team   
 sudo chgrp heist-team team-notes.txt  
5. Verify the changes
   
 <img width="490" height="165" alt="image" src="https://github.com/user-attachments/assets/d0ad1b1b-f892-4466-8b56-779f8f7fd667" />
 
Created the heist team and change the group ubuntu to heist team-notes.txt  

# Task 4: Combined Owner & Group Change  
1. Create file project-config.yaml  
<img width="487" height="162" alt="image" src="https://github.com/user-attachments/assets/426eae0a-bb17-4fb3-8930-10106a7d1d5d" />

2. Change owner to professor AND group to heist-team  
<img width="558" height="204" alt="image" src="https://github.com/user-attachments/assets/29beef4e-f5eb-46d4-a34e-09b96703aac3" />

 Owner and group has been changed from ubuntu to professir and heist team  

3. create directory app-logs
   
<img width="509" height="185" alt="image" src="https://github.com/user-attachments/assets/58dab496-5224-4d9c-80fa-030b5a9ca510" />

Currently ownership is with ubuntu

4. Change its owner to berlin and group to heist-team  
   
   <img width="512" height="188" alt="image" src="https://github.com/user-attachments/assets/7b7f1195-9d75-41e3-8833-2af6bcfd5772" />  

   user berlin and group heist-team has been changed

# Task 5: Recursive Ownership  
1. Create directory structure:
mkdir -p heist-project/vault
mkdir -p heist-project/plans
touch heist-project/vault/gold.txt
touch heist-project/plans/strategy.conf

<img width="442" height="274" alt="image" src="https://github.com/user-attachments/assets/5ff89902-d440-45b3-8095-368b346a64b4" />

3. Create group planners: sudo groupadd planners

4. Change ownership of entire heist-project/ directory:
  -  Owner: professor  
  -  Group: planners  
   - Use recursive flag (-R)
     
5. Verify all files and subdirectories changed: ls -lR heist-project/

   <img width="476" height="203" alt="image" src="https://github.com/user-attachments/assets/f49f523d-b728-4ac7-9914-badaebfdacda" />


# Task 6: Practice Challenge  
Create users: tokyo, berlin, nairobi (if not already created)
 - User already present
Create groups: vault-team, tech-team

Create directory: bank-heist/  

<img width="591" height="198" alt="image" src="https://github.com/user-attachments/assets/b0a24d6f-030b-4e51-ad66-63fe102d2b47" />  

Create 3 files inside:

- touch bank-heist/access-codes.txt  
- touch bank-heist/blueprints.pdf  
- touch bank-heist/escape-plan.txt  
  Set different ownership:
  

*access-codes.txt → owner: tokyo, group: vault-team *

<img width="591" height="198" alt="image" src="https://github.com/user-attachments/assets/b0a24d6f-030b-4e51-ad66-63fe102d2b47" />

*blueprints.pdf → owner: berlin, group: tech-team *
<img width="559" height="108" alt="image" src="https://github.com/user-attachments/assets/a59dfb33-0372-4787-8d4b-f69abd302082" />

*escape-plan.txt → owner: nairobi, group: vault-team *

<img width="567" height="101" alt="image" src="https://github.com/user-attachments/assets/5812726c-e58a-441f-a935-7b45f95c9b0e" />














