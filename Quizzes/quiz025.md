# Quiz 025




## Code
```.py

def count_letters(mydict:dict,msg=str):
    for item in mydict:
        for letter in msg:
            if letter==item:
                mydict[item]+=1
    return mydict
m=count_letters({'a':0,'e':0,'i':0,'o':0,'u':0}, msg="Why did I choose CS?")
print(m)



```

## Proof of work


![image](https://github.com/user-attachments/assets/86275d6e-6cda-4255-bb38-ea000f936542)


## How many different colors could you represent in a 6 bit computer?
As colors are represented in binary, then there will be 2^6=64 colors.
