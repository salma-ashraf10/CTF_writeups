# ADSL Modem - Forensics challenge

  platform: Cyber Talents

  category: Forensics   medium(100 points)

## Challenge Description: 

    a firmware image extracted from a DSL modem was obtained.
    
----
## Tools Used

 - file command
 - unrar for uncompromising
 
----

## Analysis Steps:

### 1. Download the attached file.

### 2. use file command for knowing the type of this file

     /home/kali/Pictures/Screenshot_2025-12-06_20_48_13.png

  
### 3. the result is rar file , so let's uncompromise it.

### 4. use unrar command 

### 5. the result is the flag:
---
## Impact summary:
   Credentials were exposed through easily reversible JavaScript obfuscation.
    
---
## Mitigations:
   Never hardcode credentials in client-side JavaScript.

   Avoid relying on JavaScript obfuscation for security.

---
### The flag: 
     {J4V4_Scr1Pt_1S_Aw3s0me}
     
[The challenge link](https://cybertalents.com/challenges/web/this-is-sparta)



      



 
