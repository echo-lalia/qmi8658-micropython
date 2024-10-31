Simple port of a QMI8685 sensor driver to MicroPython.

Example usage:
```Python
from machine import Pin, I2C
from qmi8658. import QMI8658
import time


sensor = QMI8658(
    I2C(0, sda=Pin(11), scl=Pin(12)),
)

while True:
    print(f"""
QMI8685
{sensor.temperature=}
{sensor.acceleration=}
{sensor.gyro=}
""")
    time.sleep(1)
```
Example output:
```Python
QMI8685
sensor.temperature=0.6914063
sensor.acceleration=(-0.046875, 1.006836, 0.3925781)
sensor.gyro=(-1.601563, -1.984375, -1.4375)
```
