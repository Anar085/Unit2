# Quiz 021


## Code
```.py

from matplotlib import pyplot as plt
plt.style.use('ggplot')


x,y=[],[]
start=-10
step=0.01
for i in range(int(20//step)):
    x.append(start+i*step)
    y.append(2*(x[-1]+5)**2)


plt.plot(x,y, linewidth=2, color='red')
plt.xlabel("x variable")
plt.ylabel("y variable")
plt.title("Parabola $2(x+5)^2$")
plt.show()

```

## Proof of work

![image](https://github.com/user-attachments/assets/6aa2b67c-196e-43b5-866d-c05b2b2a42b6)

## Circuit for  not(bit0 bit1 + not (bit0 + bit1)) 



![quiz21](https://github.com/user-attachments/assets/3303b048-87de-4e13-a5dd-8e1dbf7ce0de)



