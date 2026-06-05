# Exercise 1: Electrical Circuits



##  Overview
This exercise focuses on building and analyzing basic electrical circuits, including LED control and transistor-based switching. The goal was to understand circuit behavior through measurements, observation, and experimentation.


###  Task 1.1 – Simple LED Circuit

#####  Circuit Setup

<img width="300" height="400" alt="Task 1 1" src="https://github.com/user-attachments/assets/365cd04a-1bb1-4ec8-a2ec-23f25847178b" />

####  Measurements

| R1 (Ω) | V1 (V) | VLED (V) |
|--------|--------|----------|
| 220    |2.76    |2.10      |
| 1000   |2.45    |2.53      |
| 4700   |2.29    |2.71      |

####  Observations
- The LED successfully turned on once all circuit connections were completed.
- Testing confirmed that increasing resistance reduces LED brightness because a higher resistance directly limits the electrical current flowing through the circuit.
- While the voltage across the resistor changed significantly with different resistor values, the voltage across the LED remained relatively stable.


###  Task 1.2 – Switchable LED Circuit

#####  Circuit Setup

<img width="300" height="400" alt="Task 1 2" src="https://github.com/user-attachments/assets/204812d7-938a-4fca-a320-c0b3e02d4137" />

####  Observations
- Closing the switch completed the circuit and turned the LED on, while opening it interrupted the path and turned the LED off, demonstrating how switches control current flow.
- Reversing the orientation of the switch had no impact on functionality, confirming that it acts purely as a non-polar, mechanical connection to open and close the circuit path.
- The task provided a clear, hands-on demonstration of how physical circuit continuity directly dictates component behavior.


###  Task 1.3 – Dimmable LED Circuit

#####  Circuit Setup

<img width="300" height="400" alt="Task 1 3" src="https://github.com/user-attachments/assets/cc9cea5a-0714-4317-a530-b1d7d6264822" />

#####  Demonstration

https://github.com/user-attachments/assets/0e08ca2e-6de7-4b52-b0a2-b69a115ee704

####  Measurements

| Position | VLED (V) | V2 (V) |
|----------|----------|--------|
| Full     |2.97      |2.99    |
| Dim      |2.88      |4.55    |
| OFF      |0.37      |4.58    |

####  Observations
- Rotating the potentiometer gradually adjusted the LED from full brightness to dim, and eventually turned it off, demonstrating how variable resistance provides analog-style control over a circuit.
- Testing confirmed that increasing the potentiometer's resistance directly reduces current flow, which in turn decreases the LED's brightness.
- Voltage measurements shifted in real time based on the potentiometer’s position, practically illustrating how changing resistance alters the voltage distribution across components.


###  Task 2.1 – Switchable LED Strip

#####  Circuit Setup

<img width="300" height="400" alt="Task 2 1" src="https://github.com/user-attachments/assets/8583811d-bc04-4062-b846-60e72516c72f" />

####  Explanation

In this circuit, a MOSFET transistor is used as an electronic switch to control the LED strip. The MOSFET allows a low-power control signal at the gate to switch a higher current flowing through the LED strip.

When no voltage is applied to the gate (LOW), the MOSFET remains OFF and no current flows, so the LED strip is turned OFF. When a voltage is applied to the gate (HIGH), the MOSFET turns ON, allowing current to flow from the power supply through the LED strip to ground, turning it ON.


###  Task 2.2 – PWM Controlled LED Strip

#### A) Duty Cycle Variation

######  Circuit Setup

#####  a) For D=2%

<img width="300" height="400" alt="Task 2 2 Aa)" src="https://github.com/user-attachments/assets/aa1e2a1f-fa4c-4285-b2ce-be41263dad4a" />

#####  b) For D=15%

<img width="300" height="400" alt="Task 2 2 Ab)" src="https://github.com/user-attachments/assets/8872b7fc-b08c-4633-ad18-40035f5b5905" />

#####  c) For D=40%

<img width="300" height="400" alt="Task 2 2 Ac)" src="https://github.com/user-attachments/assets/c5ebd166-49f0-493e-9139-c8499980fce1" />

#####  d) For D=75%

<img width="300" height="400" alt="Task 2 2 Ad)" src="https://github.com/user-attachments/assets/668ea323-836a-4796-a504-7707d8a58781" />

#####  e) For D=100%

<img width="300" height="400" alt="Task 2 2 Ae)" src="https://github.com/user-attachments/assets/d22e9e0e-c591-434f-be32-0c35fa031a51" />

####  Observations
- Brightness increases with duty cycle.
- At low duty cycle → dim light  
- At high duty cycle → bright light  
- Relationship is proportional.


#### B) Frequency Variation

######  Circuit Setup

#####  a) For f=5Hz

https://github.com/user-attachments/assets/535b981b-41b7-46a3-b9cc-9ef392be0bcf

#####  b) For f=25Hz

https://github.com/user-attachments/assets/c7f1d898-b02a-4aea-abdb-0c845ad0c07c

#####  c) For f=45Hz

https://github.com/user-attachments/assets/9359d24f-8974-43af-99d5-4b2e6e588a12

#####  d) For f=100Hz

https://github.com/user-attachments/assets/03f0c349-83cb-4cad-812d-e6dab6092ea7

####  Observations
- Low frequency → visible flickering  
- High frequency → steady light  
- Flicker disappears beyond certain frequency.


---


##  Conclusion
This initial hands-on electronics exercise built my confidence in assembling, analyzing, and debugging breadboard circuits. Step-by-step troubleshooting and multimeter measurements bridged the gap between theory and practice, clarifying voltage distribution and current flow. Key takeaways included observing how adjustments to resistance, switching, duty cycle, and frequency directly affect LED behavior. Furthermore, the transistor and PWM tasks clearly demonstrated how low-voltage signals efficiently control higher-power devices, providing a strong foundation for practical electronic prototyping.



---
