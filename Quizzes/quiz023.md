# Quiz 023

## Code
```.py
from matplotlib import pyplot as plt
plt.style.use('ggplot')
import numpy as np
plt.style.use('ggplot')
t=[]
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
for i in range(0,32):
    t.append(i*10)
plt.plot(t,h, color='red')
plt.title("Scatter Plot of humidity data")
plt.xlabel("after t minutes")
plt.ylabel("humidity level")

m,b=np.polyfit(t,h,1)
print(f"The linear model for the data is h={m:.2f}t+{b:.2f}")
def model(t,m,b):
    return m*t+b
x_model=[min(t),max(t)]
y_model=[model(min(t),m,b),model(max(t),m,b)]

plt.plot(x_model,y_model, linewidth=1, color='blue')

plt.show()


```

## Proof of work

![image](https://github.com/user-attachments/assets/b3b0300f-3b65-48d0-98c9-c0e4df989f09)

## Convert #e6e627 to RGB  



![quiz23](https://github.com/user-attachments/assets/5c32d54d-88da-4034-af28-8c4b1a99d89d)



