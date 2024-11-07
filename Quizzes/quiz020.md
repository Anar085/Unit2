# Quiz 020

## Code
```.py
from matplotlib import pyplot as plt
plt.style.use('ggplot')
import random
random.seed(1243)
def produce(n:int, m:int, s:int):
    x,y=[],[]
    for i in range(n):
        var=random.randint(0,100)
        x.append(var)
        y.append(var**((1/2)*((m/s)**2)))


    plt.plot(x,y, linewidth=2, color='red')
    plt.scatter(x,y,linewidth=5, color='blue')
    plt.xlabel("X variable")
    plt.ylabel("Y variable")
    plt.title("Equation $y=x**((1/2)*((m/s)**2))$")
    plt.show()
m=produce(n=5,m=3,s=2)
print(m)

```

## Proof of work

![image](https://github.com/user-attachments/assets/938fce58-0e0f-45d8-a62c-619f21cb42ef)

## Truth table for: A(A ⊕ B)  

![quiz20](https://github.com/user-attachments/assets/846c8c09-921d-4bb9-8c78-0cce0fdc4491)


