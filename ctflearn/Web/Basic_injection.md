# Basic injection - Web challenge

  platform: ctflearn

  category: Web   30points

## Challenge Description: 
    We are asked to leak the whole database using SQL Injection.

----

## Analysis Steps:
### 1. Initial observation: An input field takes user-supplied data which is used in a database query.
### 2. Hypothesis: SQL injection may be possible by turning the WHERE clause into a tautology (true/false payloads)
### 3. Attempt 1 (failed): Payload tried: ' OR 1 = 1; 
        Result : no successful result.
### 4. Attempt 2 (failed): Payload tried: 'or ''='
        Result : no successful result.
### 5. Attempt 3 (successful): payload tried: 'or 1 or' 
        Result : successful result so I could see the leaked database and I find the flag in 'Data' key.
        
      
---
## Impact summary:
         Ability to bypass WHERE logic, potentially disclose data.

## Mitigations:
        Use parameterized queries, implement proper escaping if needed, apply least privilege.

---
### The flag: 
      CTFlearn{th4t_is_why_you_n33d_to_sanitiz3_inputs}

[The challenge link](https://ctflearn.com/challenge/88)



      



 
