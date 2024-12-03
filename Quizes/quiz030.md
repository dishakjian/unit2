# Code
```.py
import requests
import matplotlib.pyplot as plt
from matplotlib.gridspec import GridSpec

server_ip = "192.168.4.137"
response = requests.get(f"http://{server_ip}/readings")
data = response.json()

readings = data['readings'][0]
temp = []
hum = []
difference = []
for r in readings:
    if r['sensor_id'] == 10:
        hum.append(r["value"])
    elif r['sensor_id'] == 11:
        value = float(r['value'])
        temp.append(r["value"])

for i in range(len(hum)):
    difference.append(int(hum[i]) - int(temp[i]))

fig = plt.figure(figsize=(10,5))
grid = GridSpec(nrows=3,ncols=4, figure = fig)
plt.subplots_adjust(hspace = 0.5) #space between

box1=fig.add_subplot(grid[1,3])
plt.title("temp #11")
plt.plot(temp)

box2=fig.add_subplot(grid[1,0])
plt.title("humidity #10")
plt.plot(hum)

box3 = fig.add_subplot(grid[0:3,1:3])
plt.title("difference")
plt.plot(difference)
plt.show()
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/11a43f64-36bf-4b52-a562-dd0136cff26b)
