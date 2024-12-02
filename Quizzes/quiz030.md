# Quiz 030



## Code
```.py

server_ip="192.168.4.137"

from matplotlib import pyplot as plt
plt.style.use('ggplot')
import requests
from matplotlib.gridspec import GridSpec
request=requests.get(f'http://{server_ip}/readings')
data=request.json()
readings=data['readings'][0]
fig=plt.figure(figsize=(10,5))
grid=GridSpec(nrows=3, ncols=4,figure=fig  )

box1=fig.add_subplot(grid[1,0])
plt.title("Sensor id=10")
ids=[]
for r in readings:
    if r["sensor_id"]==10:
        ids.append(r["value"])

hum_segment=ids[0:800]
plt.plot(hum_segment)


box2=fig.add_subplot(grid[1,3])
plt.title("Sensor id=11")
ids2=[]
for r in readings:
    if r["sensor_id"]==11:
        ids2.append(r["value"])

temp_segment=ids2[0:800]
plt.plot(temp_segment)



box3=fig.add_subplot(grid[0:3,1:3])
plt.title("Sensor #10 - Sensor #11")
ids3=[]
for hum in ids:
    for temp in ids2:
        ids3.append(hum+temp)
common_segment=ids3[0:800]
plt.plot(common_segment)
plt.show()



```

## Proof of work


![image](https://github.com/user-attachments/assets/2f8255fd-e472-4a9a-802c-946214b0e7c6)








