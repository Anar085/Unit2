# Quiz 028



## Code
```.py
import requests
import datetime
server_ip="192.168.4.137"
from matplotlib import pyplot as plt
plt.style.use('ggplot')
import numpy as np
plt.style.use('ggplot')
import requests
from mylib import moving_average

request=requests.get(f'http://{server_ip}/readings')
data=request.json()
readings=data['readings'][0]
fig=plt.figure(figsize=(15,12))

plt.subplot(3,1,1)
plt.title("Plot of Temperature")

ids=[]
for r in readings:
    if r["sensor_id"]==11:
        ids.append(r["value"])


temp_segment=ids[600:1600]
temp_smoothed=moving_average(windowsize=5, x=temp_segment)

x=[*range(0,len(temp_smoothed))]
m,b=np.polyfit(x,temp_smoothed,deg=1)
plt.plot(temp_segment)
plt.plot([0,x[-1]],[b,m*x[-1]+b],color='green',linewidth=1,linestyle='--')

a,b,c=np.polyfit(x,temp_smoothed,deg=2)
y_quad=[]
for i in x:
    y_quad+=[a*i**2+b*i+c]
plt.plot(x,y_quad,color='blue',linewidth=1,linestyle='-')
d,a,b,c=np.polyfit(x,temp_smoothed,deg=3)
y_cubic=[]
for i in x:
    y_cubic+=[d*i**3+a*i**2+b*i+c]
plt.plot(x,y_cubic,color='yellow',linewidth=2,)
plt.plot(temp_smoothed,color='black')
plt.subplot(3,1,2)
plt.title("Plot of Humidity")

ids3=[]
for r in readings:
    if r["sensor_id"]==10:
        ids3.append(r["value"])

temp_segment=ids3[600:1600]
temp_smoothed=moving_average(windowsize=5, x=temp_segment)


x=[*range(0,len(temp_smoothed))]


m,b=np.polyfit(x,temp_smoothed,deg=1)
plt.plot(temp_segment)
plt.plot([0,x[-1]],[b,m*x[-1]+b],color='green',linewidth=1,linestyle='--')

a,b,c=np.polyfit(x,temp_smoothed,deg=2)
y_quad=[]
for i in x:
    y_quad+=[a*i**2+b*i+c]
plt.plot(x,y_quad,color='blue',linewidth=1,linestyle='-')
d,a,b,c=np.polyfit(x,temp_smoothed,deg=3)
y_cubic=[]
for i in x:
    y_cubic+=[d*i**3+a*i**2+b*i+c]
plt.plot(x,y_cubic,color='yellow',linewidth=2,)
plt.plot(temp_smoothed,color='black')
plt.subplot(3,1,3)
plt.title("Plot of Pressure")
ids2=[]
for r in readings:
    if r["sensor_id"]==12:
        ids2.append(r["value"])
hum_segment=ids2[600:1600]
hum_smoothed=moving_average(windowsize=5, x=hum_segment)
x=[*range(0,len(hum_smoothed))]
m,b=np.polyfit(x,hum_smoothed,deg=1)
plt.plot(hum_segment)
plt.plot([0,x[-1]],[b,m*x[-1]+b],color='green',linewidth=1,linestyle='--')

a,b,c=np.polyfit(x,hum_smoothed,deg=2)
y_quad=[]
for i in x:
    y_quad+=[a*i**2+b*i+c]
plt.plot(x,y_quad,color='blue',linewidth=1,linestyle='-')
d,a,b,c=np.polyfit(x,hum_smoothed,deg=3)
y_cubic=[]
for i in x:
    y_cubic+=[d*i**3+a*i**2+b*i+c]
plt.plot(x,y_cubic,color='yellow',linewidth=2,)
plt.plot(hum_smoothed,color='black')

plt.show()



```

## Proof of work

![image](https://github.com/user-attachments/assets/8d29fe6f-007c-4338-abbb-b699c119434c)
GREEN - Linear Model
BLUE - Quadratic Model
Yellow - Cubic Model







