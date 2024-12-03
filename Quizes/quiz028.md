# Code
```.py

import requests
from matplotlib import pyplot as plt
import numpy as np
server_ip = "192.168.4.137"
response = requests.get(f"http://{server_ip}/readings")
data = response.json()
readings = data['readings'][0]

values = []
for r in readings:
    if r["sensor_id"] == 11:
        values.append(r["value"])

plt.figure(figsize=(10, 6))
plt.plot(values, label="Raw Sensor Data")
plt.title("Raw Temperature Readings")
plt.xlabel("Time")
plt.ylabel("Temperature")
plt.legend()
plt.grid()
plt.show()
def moving_average(windowSize: int, y: list) -> list:
    y_smoothed = []
    for i in range(0, len(y) - windowSize):
        y_section = y[i : i + windowSize]
        y_average = sum(y_section) / windowSize
        y_smoothed.append(y_average)
    return y_smoothed

y = values[600:1600]
temp_y = moving_average(50, y)
x = [i for i in range(0, len(temp_y))]

m, b = np.polyfit(x, temp_y, deg=1)
x_linear = [min(x), max(x)]
y_linear = [m * x_linear[0] + b, m * x_linear[1] + b]

a, b, c = np.polyfit(x, temp_y, deg=2)
quadratic_model = [a * i**2 + b * i + c for i in x]

x_scaled = [i / max(x) for i in x]
a_scaled, b_scaled, c_scaled = np.polyfit(x_scaled, temp_y, deg=2)
quadratic_model_scaled = [a_scaled * i**2 + b_scaled * i + c_scaled for i in x_scaled]

plt.figure(figsize=(12, 8))

plt.subplot(2, 1, 1)
plt.plot(temp_y, color="red", linewidth=2, label="Smoothed Data")
plt.plot(x_linear, y_linear, label=f"Linear (m={m:.2f}, b={b:.2f})", linestyle="--")
plt.title("Smoothed with Linear")
plt.ylabel("Temperature")
plt.legend()
plt.grid()

plt.subplot(2, 1, 2)
plt.plot(temp_y, color="blue", linewidth=2, label="Smoothed Data")
plt.plot(x, quadratic_model, label="original", linestyle="--")
plt.plot(x, quadratic_model_scaled, label="Scaled", linestyle="-.")
plt.title("smoothed with quadratic")
plt.xlabel("Time")
plt.ylabel("Temperature")
plt.legend()
plt.grid()

plt.tight_layout()
plt.show()
```

# Proof Code Works
![image](https://github.com/user-attachments/assets/464c4a57-7acf-40f0-a1af-8adfa4475cfd)

![image](https://github.com/user-attachments/assets/264ca4c3-c3b2-4d0f-a3f8-c86be550877c)
