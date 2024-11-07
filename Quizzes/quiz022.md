# Quiz 022



## Code
```.py

from matplotlib import pyplot as plt
plt.style.use('ggplot')


x,y=[],[]
start=-10
step=2.5
for i in range(int(22.5//step)):
    x.append(start+i*step)
    y.append(abs(start+i*step))



plt.plot(x,y, linewidth=2, color='red')
plt.xlabel("x variable")
plt.ylabel("y variable")
plt.title("Absolute value $f(x)=|x|$")
plt.show()
```

## Proof of work

![image](https://github.com/user-attachments/assets/e47f5c52-8d76-4937-9ceb-86b2bbb68fb2)

## Convert to decimal

![quiz22](https://github.com/user-attachments/assets/22864c24-142d-47a5-a089-f5073c9fb077)





