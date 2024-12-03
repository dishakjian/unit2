# Code
```.py
import numpy as np
import matplotlib.pyplot as plt
import requests

# constants for ideal gas law
V = 1.0  # assume volume is 1 m³
n = 1.0  # assume 1 mole of gas
R = 8.314  # ideal gas constant (J/(mol·K))
API_URL = "192.168.4.137"

request = requests.get(f"http://{API_URL}/readings")
data = request.json()
print("hello")
readings = data['readings'][0]

temp = [r["value"] for r in readings if r["sensor_id"] == 11]

x = np.arange(len(temp))

m, b = np.polyfit(x, temp, deg=1)

# temperature
plt.subplot(3, 1, 1)
plt.plot(temp, color='yellow')
plt.plot(x, m * x + b, '--', color='blue')
plt.title("Temperature")
plt.legend()

pres = [r["value"] for r in readings if r["sensor_id"] == 12]

# convert pressure to temperature using ideal gas law
converted_temp = [(p * V) / (n * R) for p in pres]

# pressure
plt.subplot(3, 1, 2)
plt.plot(pres, color='red')
plt.title("pressure")
plt.legend()

# sum
combined = [t + ct for t, ct in zip(temp, converted_temp)]

plt.subplot(3, 1, 3)
plt.plot(combined, color='green')
plt.title("sum")
plt.legend()

plt.tight_layout()
plt.show()
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/6bd3b6e8-8cd1-43ba-b866-ebaa328085b1)
