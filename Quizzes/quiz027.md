# Quiz 027




## Code
```.py
def sort_dict(mydict:dict):
    numbers=[]
    words=[]
    for item in mydict.keys():
        if isinstance(mydict[item],int):
            numbers.append(mydict[item])
        else:
            words.append(mydict[item])
    numbers.sort()
    lenghts=[]
    for word in words:
        lenghts.append(len(word))
    lenghts.sort()

    out={}
    for number in numbers:
        for item in mydict:
            if number==mydict[item]:
                out[item]=mydict[item]
    for length in lenghts:
        for item in mydict:
            if isinstance(mydict[item],str):
                if length==len(mydict[item]):
                    out[item]=mydict[item]
    return out
m=sort_dict(mydict={'apple': 'red', 'banana': 2, 'orange': 'orange', 'grape': 1, 'kiwi': 'brown', 'pear': 8})
print(m)




```

## Proof of work

![image](https://github.com/user-attachments/assets/6c188fdf-a455-4c41-90d7-9beb20c407d7)

## Create the graph of the function y=sin(2*pi*x) 0<x<1


![image](https://github.com/user-attachments/assets/ac3ee860-5248-4042-98e7-98b1efbc26df)





