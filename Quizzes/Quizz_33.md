#Quiz 33

```diff
```diff

```.py
def mystery(list1:list,list2:list)->list:
    output = []
    for i in range(len(list1)):
        for r in range(len(list2)):
            if list1[i] == list2[r]:
               output.append(list1[i])

    return output
```
