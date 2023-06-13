---
title: "Real-Time Light Sensor Data Plotting using Python and Matplotlib"

date: 2023-03-19 00:00:00 -500
categories: [arduino, code, python]
tags: [arduino, code, python]
---
# Monitoring Light Intensity with a Light Sensor and Python

In this blog, we'll explore how to use Python to monitor light intensity using a light sensor and visualize the data with matplotlib. We'll walk through the code, explain what each section does, and provide some context around the project.

## Hardware Required

* Arduino board (Uno, Nano, or any other)
* Light sensor module
* USB cable
* Jumper wires

## Software Required

* Arduino IDE
* Python 3.x installed
* matplotlib library for Python (can be installed using pip)

## The Circuit

Before we get into the Python code, let's first discuss the circuitry. We'll be using an Arduino board to read the data from the light sensor and send it to the computer via the serial port. Connect the light sensor module to the Arduino as follows:

* Connect the VCC pin of the light sensor module to the 5V pin of the Arduino board.
* Connect the GND pin of the light sensor module to the GND pin of the Arduino board.
* Connect the OUT pin of the light sensor module to any of the analog input pins (A0 to A5) of the Arduino board.

Once the circuit is set up, upload the following code to the Arduino board:

```c
void setup() {
Serial.begin(9600);
}

void loop() {
int sensorValue = analogRead(sensorPin);
Serial.println(sensorValue);
delay(1000);
}
```

This code reads the analog value from the light sensor module and sends it to the serial port every second.

The Python Code
Now let's dive into the Python code. We'll be using the pyserial and matplotlib libraries to read the data from the serial port and visualize it.

First, we import the necessary libraries:

```python
from serial import Serial
import matplotlib.pyplot as plt
```

Next, we establish a serial connection with the Arduino board:

```python
ser = Serial('COM4', 9600)
```

Replace 'COM4' with the name of the serial port your Arduino board is connected to (you can find this in the Arduino IDE under Tools > Port).

We then set up the matplotlib figure:

```python
plt.ion() # turn on interactive mode
fig, ax = plt.subplots()
ax.set_title('Light Sensor')
ax.set_xlabel('Time')
ax.set_ylabel('Light Intensity')
```

We turn on interactive mode with plt.ion() so that the figure updates in real-time. We create a new figure and axis object and set the title and axis labels.

Next, we define empty lists for the x and y data, create a line object to plot the data, and enter into a loop to continuously read the data from the serial port:

```python
x, y = [], []
line, = ax.plot(x, y)

while True:
    try:
        data = ser.readline().decode().strip()
        x.append(len(x))
        ligma=1000-float(data)
        y.append(ligma)

        line.set_data(x, y)

        ax.relim()
        ax.autoscale_view(True,True,True)

        fig.canvas.draw()
        fig.canvas.flush_events()

    except KeyboardInterrupt:
        ser.close()
        break
```

Inside the loop, we read the data from the serial port, convert it to a float, subtract it from 1000 (since the light sensor module outputs higher values for lower light intensity), and append it to the y data list. We also append the length of the x data list to the x data list to keep track of time. We then update the line object with the new data and adjust the axis limits and scale. Finally, we draw the updated figure and flush the event queue.

For more info you can visit  [my github](https://github.com/ifsvivek/Plot-Arduino-Data-in-Real-Time)
