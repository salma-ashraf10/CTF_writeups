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

    
    root㉿kali)-[/home/kali/Downloads]
    └─# file TL-MR3220+V2+_FW.bin
    TL-MR3220+V2+_FW.bin: RAR archive data, v4, os: Win32
    

  
### 3. the result is rar file , so let's uncompromise it.

### 4. use unrar command 
         (root㉿kali)-[/home/kali/Downloads]
          └─# unrar x  TL-MR3220+V2+_FW.bin
          
          UNRAR 7.13 freeware      Copyright (c) 1993-2025 Alexander Roshal
          
          Archive comment:
          Flag{reversing_FW_is_interesting_but_this_is_for_fun}
          
          Extracting from TL-MR3220+V2+_FW.bin

### 5. the result is the flag:
          Flag{reversing_FW_is_interesting_but_this_is_for_fun}
---
### The flag: 
    Flag{reversing_FW_is_interesting_but_this_is_for_fun}
     
[The challenge link](https://cybertalents.com/challenges/forensics/adsl-modem)



      



 
