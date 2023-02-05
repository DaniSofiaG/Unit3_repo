# 37.
```diff
An Accounting firm needs a software package to calculate compound interest. Draw the UML diagram.
```
<img width="801" alt="Screen Shot 2023-02-05 at 13 31 45" src="https://user-images.githubusercontent.com/111941990/216801687-b4e37818-c466-45b2-be7b-819703bdea71.png">


## Code
```.py
class Accounting:
    def __init__(self):
        self.data = CompoundInterest(principal=0,rate=0,year=0) #composition
    def set_principal(self,principal):
        if principal < 0:
            raise ValueError("Principal should be greater than zero")
        else:
            self.data.principal = principal
        return principal
    def set_rate(self,rate):
        if rate < 0:
            raise ValueError("Interest rate should be greater than zero")
        else:
            self.data.rate = rate
        return rate
    def set_years(self,year:int):
        if year < 0:
            raise ValueError("Years should be greater than zero")
        else:
            self.data.year = year
        return year
    def calculate_interest(self):
        interest = self.data.principal * (1+self.data.rate)**self.data.year
        interest = float("{:.2f}".format(interest))
        return interest
```

## Test
<img width="1400" alt="Screen Shot 2023-02-05 at 13 39 37" src="https://user-images.githubusercontent.com/111941990/216802125-e5b159cd-5a5b-4c75-8282-111a34f55b4a.png">

## UML
