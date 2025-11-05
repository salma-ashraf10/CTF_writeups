# Character Encoding - Cryptography challenge

  platform: ctflearn

  category: Cryptography  20points
---
## Challenge Description: 
   We are given a sequence of hexadecimal bytes that hides the flag. 
   Interpret the bytes correctly to reveal an ASCII message that follows the competition's flag format.

---
## Tool used:
   (cryptii.com)[https://cryptii.com/pipes/hex-decoder] --> decoding the hexa code
---

## Analysis Steps:
### 1. The challenge provides a sequence of hexadecimal bytes:  
        `41 42 43 54 46 7B 34 35 43 31 31 5F 31 35 5F 55 35 33 46 55 4C 7D`.

### 2. I converted the hex string to ASCII text using (cryptii.com)[https://cryptii.com/pipes/hex-decoder].

### 3. The website returned the ASCII text:  
             `ABCTF{45C11_15_U53FUL}`
        
---
### The flag: 
      ABCTF{45C11_15_U53FUL}

[The challenge link](https://ctflearn.com/challenge/115)



      



 
