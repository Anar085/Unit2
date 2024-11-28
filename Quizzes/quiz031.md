# Quiz 031



## Code
```.py
from matplotlib import pyplot as plt
import numpy as np
plt.style.use('ggplot')
x1,y1=[],[]
start=-2
step=0.04
for i in range(int(4.08//step)):
    x1.append(start+i*step)
    y1.append(x1[-1]**2)
x2,y2=[],[]
start=-2
step=0.04
for i in range(int(4.08//step)):
    x2.append(start+i*step)
    y2.append((x2[-1]**2)*-1)

plt.plot(x1,y1,color='blue',label='x1')
plt.plot(x2,y2,color='red',label='x2')
plt.plot(y2,x2,color='green',label='x3')
plt.plot(y1,x1,color='black',label='x4')
plt.show()




```

## Proof of work

![image](https://github.com/user-attachments/assets/f4b54133-3f81-4fdb-a5df-4dd2be9c8250)





