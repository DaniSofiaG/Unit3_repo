# Quiz 33


## Code
```.py
def mystery(list1:list,list2:list)->list:
    output = []
    for i in range(len(list1)):
        for r in range(len(list2)):
            if list1[i] == list2[r]:
               output.append(list1[i])

    return output
```


## Testing
<img width="699" alt="Screen Shot 2023-01-10 at 17 07 50" src="https://user-images.githubusercontent.com/111941990/211496550-5b63d7ea-37c4-4ac3-b209-5d04a1743d0f.png">
