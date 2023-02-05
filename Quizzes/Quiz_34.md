
# 34.
```diff
Create a new Python function called to_roman(num) that takes a single integer as input. It returns a string representing the Roman numeral 
equivalent of the input number. 
```

## Code
```.py
def to_roman(num: int):
    if num > 100:
        raise ValueError("Error! Decimal must me less than or equal to 100")
    else:
        dec = [100, 90, 50, 40, 10, 9, 5, 4, 1]
        roman = ["C", "XC", "L", "XL", "X", "IX", "V", "IV", "I"]
        roman_num = ""
        i = 0
        while num > 0:
            for number in range(num // dec[i]):
                roman_num += roman[i]
                num -= dec[i]
            i += 1
        return roman_num
```
<img width="730" alt="Screen Shot 2023-02-05 at 16 59 21" src="https://user-images.githubusercontent.com/111941990/216808069-08579099-a1bf-4b3f-89a4-88d2f4617a8c.png">

## Test
<img width="1424" alt="Screen Shot 2023-02-05 at 16 57 31" src="https://user-images.githubusercontent.com/111941990/216808094-ea0ad244-0924-4992-8963-d08ee6ccf669.png">
