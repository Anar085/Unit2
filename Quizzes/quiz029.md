# Quiz 029



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
temp_segment=ids[0:800]
plt.plot(temp_segment)


plt.subplot(3,1,2)
plt.title("Plot of Pressure")
ids2=[]
for r in readings:
    if r["sensor_id"]==12:
        ids2.append(r["value"])
pres_segment=ids2[0:800]
plt.plot(pres_segment)


plt.subplot(3,1,3)
plt.title("Plot of the sum of the Pressure and Temperature")
common_segment=[]
x=[]
for temp in temp_segment:
    for pressure in pres_segment:
        temp=15*(pressure/101)**5.25
        common_segment.append(temp+pressure)

plt.plot(common_segment[0:800])


plt.show()

```

## Proof of work

![image](https://github.com/user-attachments/assets/5d78ed90-9ea6-4d51-80f0-56ae8fe94a16)









