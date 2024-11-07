# Quiz 019

## Paper solution
![quiz19](https://github.com/user-attachments/assets/c7df6504-ca6f-47a8-9139-c6962080ff50)


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

## Proof for : A (A + B) = A 

![quiz19s](https://github.com/user-attachments/assets/7dfa4e53-08e3-4879-bb24-0a3e85259ed9)









