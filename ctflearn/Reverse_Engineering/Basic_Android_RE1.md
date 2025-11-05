# Basic Android RE1 - RE challenge

  platform: ctflearn

  category: Reverse Engineering  10points

## Challenge Description: 

    An Android application (.apk) is provided. Our task is to analyze (decompile) the app to find **the hidden flag** inside.
    
----
## Tools Used
   [Decompiler.com](https://www.decompiler.com) – for APK decompilation  
   [Hashes.com](https://hashes.com/) – for MD5 hash cracking

----

## Analysis Steps:

### 1. I downloaded the APK and decompiled it using the Java Decompiler at [decompiler.com](https://www.decompiler.com) to inspect the app's source code. 

### 2. In the decompiled output I located the source code (Main Activity) at: 
       BasicAndroidRE1.apk / sources / com / example / secondapp / MainActivity.java
           
### 3. The code contained a hardcoded MD5 hash, which was used to validate the user’s input

### 4. I copied the MD5 value and looked it up on a hash-cracking database at [hashes.com](https://hashes.com/), which attempts to reverse MD5 hashes using its database.

### 5. The website returned the original plaintext key: `Spring2019`.

### 6. Inspecting the code again showed the flag format is constructed like this:
      Success! CTFlearn{" + editText.getText().toString() + "_is_not_secure!}
      Therefore `editText.getText().toString()` must equal the recovered key `Spring2019`.
      
### 7. Combining the pieces yields the final flag: CTFlearn{Spring2019_is_not_secure!}
---
## Code snippet

 <img width="1352" height="157" alt="image" src="https://github.com/user-attachments/assets/1c54acde-5da3-4f86-b51a-25e74c6397df" />

---
## Impact summary:
    This challenge demonstrates the risk of storing sensitive information (like passwords or keys) directly in client-side code.
    Since the app contains a hardcoded MD5 hash, anyone can decompile the APK, extract the hash, and crack it to reveal the secret.
---
## Mitigations:
    - Do not store secrets or perform authentication checks on the client side. move all sensitive validation to a secure server.
    - Replace MD5 (unsalted hashes) with a secure password hashing algorithm and use salts.
---
### The flag: 
     CTFlearn{Spring2019_is_not_secure!}
     
[The challenge link](https://ctflearn.com/challenge/962)



      



 
