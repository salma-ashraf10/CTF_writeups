# The Credit Card Fraudster - Programming challenge

  platform: ctflearn

  category: Programming 20points

## Challenge Description: 
    We are given a scenario where a fraudster tampered with a payment validator so that it accepts card numbers meeting two conditions:
     1. The number is a multiple of `123457`.
     2. The number passes the Luhn check digit validation.
    Our task is to find the secret numeric string (the flag) that satisfies both constraints.
----
## Code snippet
  ```python
   for i in range(999999+1):
    sm =0
    w = 1
    card = f"543210{i:06}1234"
    if int(card) % 123457 == 0:
        for j in range(len(card)):
            if(j % 2 == 0):
                w = 2
            else:
                w = 1
            if(int(card[j]) * w > 9):
                sm -= 9
            sm += (int(card[j]) * w) 
        if sm % 10 == 0:
            print(card)
            break
 ```
---
## Analysis Steps:


---
### The flag
 
      
---
[The challenge link](https://ctflearn.com/challenge/970)



      



 
