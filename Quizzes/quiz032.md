# Quiz 032

## Paper Solution
![IMG_0500](https://github.com/user-attachments/assets/463161c0-5cd8-4741-80e5-d77becdd2c6a)


## Code
```.py
def mystery(a:list,b:list)->list:
    empty_list=[]
    for el in a:
        for el2 in b:
            if el==el2:
                empty_list.append(el)
    return empty_list
m=mystery(a=[1,2,3,4],b=[3,4,5,6])
print(*m)


```

## Proof of work
![image](https://github.com/user-attachments/assets/23899b11-55e3-4a79-93c1-7ddc0676b623)










