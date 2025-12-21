# This is Sparta - Web challenge

  platform: Cyber Talents

  category: Web    easy(50points)

## Challenge Description: 

     The challenge provides a web login page that requires a username and password.
    
----
## Tools Used

  Browser Developer Tools (Inspect Element)

----

## Analysis Steps:

### 1. when I open the website , I found a login page that need username and password 

### 2. I I attempted common credentials : user = admin , pass = admin but The login attempt failed.

### 3. I open Dev tool (inspect) by clicking ctrl + shift + I go to elements tab

### 4. At line 34, I discovered an obfuscated JavaScript function responsible for validating login credentials.

### 5. I observe that the JavaScript code was using an array-based obfuscation technique:

        document[_0xae5b[2]](_0xae5b[1])[_0xae5b[0]]

### 6. By logging the array values using console.log() in the browser console, the obfuscated expressions were resolved into readable JavaScript.

### 7. the result is : { value user getElementById pass Cyber-Talent Congratz wrong Password}

### 8. the rest of code :
         function check(){var _0xeb80x2=document[_0xae5b[2]](_0xae5b[1])[_0xae5b[0]];var _0xeb80x3=document[_0xae5b[2]](_0xae5b[3])[_0xae5b[0]];if(_0xeb80x2==_0xae5b[4]&&_0xeb80x3==_0xae5b[4]){alert(_0xae5b[5]);} else {alert(_0xae5b[6]);}}
         meaning:
            document[_0xae5b[2]](_0xae5b[1])[_0xae5b[0]] --> document.getElementById("user").value
            document[_0xae5b[2]](_0xae5b[3])[_0xae5b[0]] --> document.getElementById("pass").value
            so,
              username --> Cyber-Talent 
              password --> Cyber-Talent 
           let's try it!
### 9.  After entering the discovered credentials, authentication succeeded and the flag was revealed.
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



      



 
