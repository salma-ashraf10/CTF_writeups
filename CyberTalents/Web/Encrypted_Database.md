# Encrypted_Database - Web challenge

  platform: Cyber Talents

  category: Web    easy(50points)

## Challenge Description: 

     The challenge provides a static website called TopNewsJournal Website
     
   <img width="1765" height="883" alt="image" src="https://github.com/user-attachments/assets/de015e4e-ddba-414d-9e14-36bf351734a3" />
  
    
----
## Tools Used

  Browser Developer Tools (Inspect Element)

----

## Analysis Steps:

### 1. when I open the website , I found a page that have many tabs like home , about,..etc.

### 2. I open Dev tool (inspect) by clicking ctrl + shift + I go to elements tab

### 3. At line 32, I discovered a script tag and found a path [admin/assests/app.js] in its src.

   <img width="636" height="74" alt="image" src="https://github.com/user-attachments/assets/b8057ff6-69ec-49fa-9b87-a019db390224" />

### 4. so , we can understand that there is an endpoint called admin.

### 5. so, by trying enter in it by added it in the url , we got an admin login page. but, we didn't have any credentials

  <img width="839" height="598" alt="image" src="https://github.com/user-attachments/assets/acbaf519-6bd9-4515-b5fb-c64a2eaa3edc" />


### 6. opening inspect again . when I read , I observed a suspecious code at line 39 --> an hidden input and its value contains an endpoit

   <img width="842" height="74" alt="image" src="https://github.com/user-attachments/assets/fe00a6bd-f4d1-426d-94b1-5bde06943b57" />


### 7. by trying add it . so, the full path becomes http://[your machine]/admin/secret-database/db.json

### 8. we found a hash flag . By using hash identifier tool or it gui , the result is md5 hash.

  <img width="658" height="231" alt="image" src="https://github.com/user-attachments/assets/8462ea8c-49f6-41a9-a33f-f6296c68d21e" />

### 9. let's crack it by crackstation tool.

   <img width="1394" height="88" alt="image" src="https://github.com/user-attachments/assets/303018b7-364a-49b5-9157-384e7bad2a9a" />


### 10. and finally, we've got the flag: badboy

----

### The flag: 

     badboy
     
[The challenge link](https://cybertalents.com/challenges/web/encrypted-database)



      



 
