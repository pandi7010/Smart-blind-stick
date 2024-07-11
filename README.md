Connections:

ULTRASONIC SENSOR (HC-SR04) to ARDUINO:

1) VCC to Arduino 5V
2) GND to Arduino GND
3) Trig to Arduino Digital Pin 9
4) Echo to Arduino Digital Pin 10

BUZZER CONNECTION to ARDUINO

1) Positive lead to Arduino Digital Pin 11
2) Negative lead to Arduino GND

LED CONNECTION to ARDUINO:

1) Anode (longer leg) to Arduino Digital Pin 12
2) Cathode (shorter leg) to a resistor (220Ω or 330Ω) to Arduino GND

Explanation:

1. SETUP: Initializes the pins for the ultrasonic sensor, buzzer, and LED. Also starts the serial communication for debugging.

2. LOOP:
      a) Sends a trigger pulse to the ultrasonic sensor.
   
      b) Measures the echo pulse duration.
   
      c) Calculates the distance.
   
      d) Checks if the distance is less than or equal to the threshold distance.
   
      e) If the distance is less than or equal to the threshold, the buzzer and LED are activated. The LED blinks with a 100ms delay.
   
      f) If the distance is greater than the threshold, the buzzer and LED are turned off.
   
This code will make the buzzer sound and the LED blink when an object is detected within 2 cm of the ultrasonic sensor.

Made by Pandiselvam BE Electronics and communication Engineering , Any querries contact me at pandiselvam1216@gmail.com
