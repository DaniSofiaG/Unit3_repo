# 35.
```diff
Create a Python class for a Bank Office that follows the UML diagram below and passes the test file test_quiz35.py
```
<img width="504" alt="Screen Shot 2023-02-04 at 19 55 16" src="https://user-images.githubusercontent.com/111941990/216763164-9791d0f2-840f-4306-a069-be5a3772e0f3.png">

## Code
```.py
# quiz35
import random


class Account:
    def __init__(self):
        self.balance = 0
        self.holder_name = ""
        self.holder_email = ""
        first_n = random.randint(100,999)
        second_n = random.randint(10000,99999)
        third_n = random.randint(0,9)
        self.number = [f"{first_n}-{second_n}-{third_n}"]

    def get_account_no(self):
        return self.number[0]

    def set_holder_name(self,name):
        if not isinstance(name, str):
            raise ValueError("Name has be a string")
        self.holder_name = name
        out = f"Holder's name is {self.holder_name}"
        return out

    def set_holder_email(self,email):
        self.holder_email = email
        out = f"Holder's email is {self.holder_email}"
        return out

    def get_balance(self):
        return self.balance

    def deposit(self,amount:int):
        self.balance += amount
        out = f"New balance: ${self.balance}"
        return out
```
<img width="827" alt="Screen Shot 2023-02-05 at 12 01 25" src="https://user-images.githubusercontent.com/111941990/216799258-ec6454c4-4537-4d14-ab7d-ec784f91100a.png">

## Test
<img width="1412" alt="Screen Shot 2023-02-05 at 12 01 54" src="https://user-images.githubusercontent.com/111941990/216799274-d9d06cb5-d72d-4a6f-90c2-12f7aacfad50.png">

