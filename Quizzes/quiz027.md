# Quiz 024




## Code
```.py
def sort_dict(mydict:dict):
    numbers=[]
    for item in mydict:
        numbers.append(mydict[item])
    numbers.sort()
    out={}
    for number in numbers:
        for item in mydict:
            if number==mydict[item]:
                out[item]=mydict[item]
    return out
m=sort_dict(mydict={'apple':5, 'banana': 2, 'orange': 8, 'grape': 1})
print(m)




```

## Proof of work







