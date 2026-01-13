# Help Ann - Forensics challenge

  platform: Cyber Talents
  
  category: Forensics  
  
  Difficulty: Medium (100 points)

## Challenge Description: 

 A scanned QR code was provided, but it was corrupted. 
 The goal was to fix the QR code image and retrieve the hidden information.
    
----
## Tools Used

 - hexedit.
 - file.
 
----

## Analysis Steps:

### 1. Download the attached file named help_ann_please.

### 2. Check its type by file command.

  ```bash
       ──(root㉿kali)-[/home/kali/Downloads]
      └─# file help_ann_please
      help_ann_please: data
  ```
  
  
### 3. Open the file using hexedit to inspect its hex header.

   While inspecting the first bytes, it was clear that the file structure resembled a PNG image, but the header was incorrect.

### 4. After searching for the PNG file signature, the correct hex header was found to be:
            89 50 4E 47  0D 0A 1A 0A
            
### 5. It was observed that the first two bytes of the header were incorrect (00 instead of 89).

### 6. Edit it from 00 to 89 and then save the edit.
    
### 7. Use file command again:
   ```bash
    ┌──(root㉿kali)-[/home/kali/Downloads]
    └─# file help_ann_please    
    help_ann_please: PNG image data, 300 x 300, 8-bit/color RGBA, non-interlaced
   ```

   This confirmed that the file was successfully restored as a valid PNG image.

### 8. Open it with xdg-open tool , so the image was now clearly visible as a QR code.

### 9. After scanning the QR code, the flag was successfully retrieved.                                                                          
---
### The flag: 
   Flag{Aw3s0m3-Y0u-G0t-th1s}




> Until next challenge!

----
[The challenge link](https://cybertalents.com/challenges/forensics/help-ann)




      



 
