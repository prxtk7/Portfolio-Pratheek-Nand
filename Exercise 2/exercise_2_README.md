# Exercise 2: Introduction to Arduino



##  Overview
This exercise introduced the fundamentals of Arduino-based prototyping through the development of a functional alarm clock system using multiple electronic components and communication interfaces. The objective of the exercise was to understand how microcontrollers interact with external hardware devices such as buzzers, LCD displays, real-time clock (RTC) modules, and push buttons to create an interactive embedded system.


##  Sub-Circuit 1 – Connecting the Buzzer

###  Circuit Setup

<img width="500 " height="800" alt="Sub-Circuit 1" src="https://github.com/user-attachments/assets/563f031a-68cd-41eb-80d3-eb71e0671203" />

###  Demonstration

https://github.com/user-attachments/assets/879854c3-4b5f-4d25-afbb-ef6e90cfabf7

###  Observations
- The buzzer successfully produced sound according to the programmed timing sequence.
- The Arduino digital output pins can directly control simple electronic actuators such as buzzers through HIGH and LOW output signals.
- This task demonstrated how software timing directly influences hardware behaviour in embedded systems.

---


##  Sub-Circuit 2 – Connceting the LCD Screen

###  Circuit Setup

<img width="350" height="500" alt="Sub-Circuit 2" src="https://github.com/user-attachments/assets/9100da86-4b7a-4a02-8dc9-3c9ceb8d3f0d" />

###  Observations
- The LCD successfully displayed text output correctly, demonstrating proper communication with the Arduino via the I2C protocol.
- Testing confirmed that the I2C interface allows the LCD to display information clearly while requiring only minimal wiring connections.
- The task provided hands-on experience and a practical understanding of how to interface LCDs and manage display-based output systems in Arduino projects.

---


##  Sub-Circuit 3 – Expanding the setup with a Real Time Clock

###  Circuit Setup

<img width="600" height="400" alt="Sub-Circuit 3" src="https://github.com/user-attachments/assets/697395ae-0fe2-496d-b743-4af755a8716f" />

###  Observations
- The Real-Time Clock (RTC) module successfully communicated with the Arduino to track and display the current time on the LCD screen.
- Testing confirmed that both the LCD and the RTC module could seamlessly operate together on the exact same I2C communication lines without interference.
- The task demonstrated the RTC module's ability to continuously maintain and provide accurate, real-time information for embedded applications.

---


##  Sub-Circuit 4 – Using the Push Button

###  Circuit Setup

<img width="700" height="400" alt="Sub-Circuit 4" src="https://github.com/user-attachments/assets/cdd899d2-160b-478a-a542-a782f45b260b" />

###  Observations
- The push buttons successfully sent digital input signals to the Arduino, which processed the presses and displayed the correct outputs on the LCD screen.
- The LCD screen and LEDs provided clear visual feedback, confirming that the system was responding correctly to the button inputs.
- The task demonstrated how to use pull-up resistor configurations to ensure stable and reliable button input detection.

---


##  Building an Arduino Alarm Clock

###  Circuit Integration

The complete alarm clock system was assembled by integrating the RTC module, LCD display, buzzer, and push buttons into a single Arduino-based setup.

The RTC module continuously provided real-time clock data to the Arduino through the I2C communication interface. The LCD display was used to display the current time, alarm configuration, and alarm status messages.

The push buttons were configured for different alarm operations:

- Red Button → Open alarm setup menu
- Green Button → Increase alarm minutes
- Blue Button → Enable the alarm
- Final Alarm State → Trigger buzzer and display alarm notification

The Arduino continuously monitored the RTC time and compared it with the configured alarm time. When both values matched, the buzzer was activated and the LCD displayed the alarm notification.

---


##  Clock functionalities


###  1. Opening the Alarm Setup Menu
Pressing the red button opened the alarm setup interface on the LCD display.

Example LCD Output:

```text
Alarm set:
12:33
```

####  Circuit Setup

<img width="500" height="500" alt="Arduino_Alarm_RPB" src="https://github.com/user-attachments/assets/346ad6b0-aff9-457c-8eea-0c7fd4e18d7d" />

###  2. Increasing Alarm Minutes
Pressing the green button increased the configured alarm minute value.

Example LCD Output:

```text
Alarm set:
12:35
```

####  Circuit Setup

<img width="500" height="500" alt="Arduino_Alarm_GPB" src="https://github.com/user-attachments/assets/f6ad1574-4d9b-4c0f-a075-9afb676ee946" />

###  3. Activating the Alarm
Pressing the blue button enabled the configured alarm.

Example LCD Output:

```text
Time: 13:34:00
Alarm is ON
```

####  Circuit Setup

<img width="500" height="500" alt="Arduino_Alarm_BPB" src="https://github.com/user-attachments/assets/354fae26-c8b9-432f-8206-492b35a46404" />

###  4. Alarm Trigger
When the RTC time matched the configured alarm time, the buzzer was activated and the LCD displayed the alarm notification.

Example LCD Output:

```text
Time: 13:34:00
Alarm Rings!
```

####  Circuit Setup

<img width="500" height="500" alt="Arduino_Alarm_Final_State" src="https://github.com/user-attachments/assets/f0f94c58-c21b-42d5-b870-a44a0a825d2b" />

###  Observations
- The system successfully executed all major requirements: tracking real-time clock data, configuring alarms with push buttons, providing LCD feedback, and triggering the buzzer alarm.
- The project demonstrated how multiple electronic components can be integrated using an Arduino to process real-time information while remaining responsive to user inputs.
- Testing highlighted that combining RTC communication, button inputs, LCD screens, and actuators into one cohesive unit requires organized hardware wiring and structured program logic to function reliably.

---


## Conclusion
The final alarm clock project successfully consolidated multiple sub-circuits into a single, functional embedded application capable of automatically displaying time, configuring user alarms, and triggering notifications. By cleanly uniting inputs, processing, and outputs from scratch, this prototyping exercise reinforced practical, hands-on knowledge in Arduino programming, hardware interfacing, real-time systems, and interactive embedded design.



---
