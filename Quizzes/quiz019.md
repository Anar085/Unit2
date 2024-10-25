# Quiz 019

## Paper solution


## Code
```.py
import random
random.seed(1234)
def produce(n:int, m:int, s:int):
    print("|   x    |   y    |")
    for i in range(n):
        x=random.randint(0,100)
        y=x**((1/2)*((m/s)**2))
        print(f"|{str(x).center(8, ' ')}|{str(round(y, 2)).center(8, ' ')}|")
    return " "


m=produce(n=5, m=3, s=2)
print(m)

```

## Proof of work
![image](https://github.com/user-attachments/assets/16e4aba3-f0ab-457f-8b69-a3d13cc332f9)








