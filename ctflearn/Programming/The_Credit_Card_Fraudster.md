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
1- I generated all possible numbers in the format 543210{i:06}1234, where i ranges from 000000 to 999999.

2- For each generated number, I checked if it was divisible by 123457

3- I also applied the Luhn algorithm to verify if the card number passed the checksum validation.

4- The first number that satisfied both conditions was:
     5432103279251234
   CTFlearn{card_number} --> CTFlearn{5432103279251234}

---
### The flag
    CTFlearn{5432103279251234}
      
---
[The challenge link](https://ctflearn.com/challenge/970)



      



 
