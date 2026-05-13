# Motion Detection System using PIR Sensor and Arduino UNO

## Overview

This project demonstrates sensor interfacing using a PIR motion sensor and Arduino UNO in Tinkercad simulation.

The system detects motion and automatically turns ON an LED when movement is detected.



## Components Used

* Arduino UNO
* PIR Motion Sensor
* LED
* 220Ω Resistor
* Breadboard
* Jumper Wires



## Software Used

* Tinkercad Circuits
* Arduino IDE



## Working Principle

The PIR sensor detects infrared radiation emitted by humans or moving objects.

* Motion detected → LED ON
* No motion → LED OFF

Arduino continuously reads the PIR sensor output and controls the LED accordingly.



## Circuit Connections

### PIR Sensor

| PIR Pin | Arduino |
| ------- | ------- |
| Signal  | Pin 2   |
| Power   | 5V      |
| Ground  | GND     |

### LED

| LED Terminal | Connection                   |
| ------------ | ---------------------------- |
| Positive     | Pin 13 through 220Ω resistor |
| Negative     | GND                          |



## Arduino Code

```cpp id="sc4kr7"
int pirPin = 2;
int ledPin = 13;

void setup()
{
  pinMode(pirPin, INPUT);
  pinMode(ledPin, OUTPUT);

  Serial.begin(9600);
}

void loop()
{
  int motion = digitalRead(pirPin);

  if (motion == HIGH)
  {
    digitalWrite(ledPin, HIGH);
    Serial.println("Motion Detected!");
  }
  else
  {
    digitalWrite(ledPin, LOW);
    Serial.println("No Motion");
  }

  delay(500);
}




## Applications

* Home Security Systems
* Smart Lighting
* Motion Detection Systems
* IoT Automation



## Result

The project was successfully designed and simulated using Tinkercad.
