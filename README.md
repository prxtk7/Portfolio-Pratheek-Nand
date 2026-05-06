# Digital Design & Fabrication Portfolio

## Student Details
- Name: Pratheek Nand
- Program: M.Sc. Engineering of Socio-Technical Systems
- University: Carl von Ossietzky Universität Oldenburg
- Semester: Summer Semester 2026
- Email: pratheek.nand@uni-oldenburg.de
- Matriculation Number: 6649747

---

## Portfolio Overview
This portfolio presents a structured and continuous documentation of my work throughout the Digital Design & Fabrication course. It captures the complete development lifecycle of each exercise, including problem understanding, design decisions, implementation, challenges, iterations, and final outcomes.

The purpose of this portfolio is to systematically track my technical growth and practical skill development across domains such as electronics, microcontrollers, and digital fabrication. It emphasizes a process-oriented approach, where both successful results and failed attempts are documented and analyzed to reflect iterative learning, problem-solving ability, and design thinking.

---

## About the Course
The course focuses on hands-on learning in digital design and fabrication. It covers areas such as electronics, microcontrollers, CAD design, and fabrication techniques including laser cutting and CNC milling. The emphasis is on practical implementation, experimentation, and iterative problem-solving.

---


# Exercise 1: Electrical Circuits


##  Task 1.1 – Simple LED Circuit

###  Circuit Setup

<img width="300" height="400" alt="Task 1 1" src="https://github.com/user-attachments/assets/365cd04a-1bb1-4ec8-a2ec-23f25847178b" />

###  Measurements

| R1 (Ω) | V1 (V) | VLED (V) |
|--------|--------|----------|
| 220    |2.76    |2.10      |
| 1000   |2.45    |2.53      |
| 4700   |2.29    |2.71      |

###  Observations
- As resistance increases, current decreases.
- LED brightness reduces with higher resistance.
- Voltage drop across resistor changes accordingly.

---


##  Task 1.2 – Switchable LED Circuit

###  Circuit Setup

<img width="300" height="400" alt="Task 1 2" src="https://github.com/user-attachments/assets/204812d7-938a-4fca-a320-c0b3e02d4137" />

###  Observations
- LED turns ON/OFF using the switch.
- Reversing switch changes control behavior.
- Demonstrates simple control mechanism.

---


##  Task 1.3 – Dimmable LED Circuit

###  Circuit Setup

<img width="300" height="400" alt="Task 1 3" src="https://github.com/user-attachments/assets/cc9cea5a-0714-4317-a530-b1d7d6264822" />

###  Demonstration

https://github.com/user-attachments/assets/0e08ca2e-6de7-4b52-b0a2-b69a115ee704

###  Measurements

| Position | VLED (V) | V2 (V) |
|----------|----------|--------|
| Full     |2.97      |2.99    |
| Dim      |2.88      |4.55    |
| OFF      |0.37      |4.58    |

###  Observations
- LED brightness varies with potentiometer position.
- Voltage across LED changes proportionally.
- Relationship is continuous and smooth.

---


##  Task 2.1 – Switchable LED Strip

###  Circuit Setup

<img width="300" height="400" alt="Task 2 1" src="https://github.com/user-attachments/assets/8583811d-bc04-4062-b846-60e72516c72f" />

###  Observations
- LED strip turns ON/OFF via transistor.
- Transistor acts as a switch.
- Gate voltage controls current flow.

###  Explanation
### 🧠 Explanation

In this circuit, a MOSFET transistor is used as an electronic switch to control the LED strip. The MOSFET allows a low-power control signal at the gate to switch a higher current flowing through the LED strip.

When no voltage is applied to the gate (LOW), the MOSFET remains OFF and no current flows, so the LED strip is turned OFF. When a voltage is applied to the gate (HIGH), the MOSFET turns ON, allowing current to flow from the power supply through the LED strip to ground, turning it ON.

This method enables efficient and safe control of higher-power devices using low-power signals and is widely used in practical electronic systems such as lighting control and motor drivers.

---


##  Task 2.2 – PWM Controlled LED Strip

### A) Duty Cycle Variation

###  Circuit Setup

####  a) For D=2%

<img width="300" height="400" alt="Task 2 2 Aa)" src="https://github.com/user-attachments/assets/aa1e2a1f-fa4c-4285-b2ce-be41263dad4a" />



####  b) For D=15%

<img width="300" height="400" alt="Task 2 2 Ab)" src="https://github.com/user-attachments/assets/8872b7fc-b08c-4633-ad18-40035f5b5905" />



####  c) For D=40%

<img width="300" height="400" alt="Task 2 2 Ac)" src="https://github.com/user-attachments/assets/c5ebd166-49f0-493e-9139-c8499980fce1" />



####  d) For D=75%

<img width="300" height="400" alt="Task 2 2 Ad)" src="https://github.com/user-attachments/assets/668ea323-836a-4796-a504-7707d8a58781" />



####  e) For D=100%

<img width="300" height="400" alt="Task 2 2 Ae)" src="https://github.com/user-attachments/assets/d22e9e0e-c591-434f-be32-0c35fa031a51" />

###  Observations
- Brightness increases with duty cycle.
- At low duty cycle → dim light  
- At high duty cycle → bright light  
- Relationship is proportional.

---

### B) Frequency Variation

###  Circuit Setup

####  a) For f=5Hz

https://github.com/user-attachments/assets/535b981b-41b7-46a3-b9cc-9ef392be0bcf



####  b) For f=25Hz

https://github.com/user-attachments/assets/c7f1d898-b02a-4aea-abdb-0c845ad0c07c



####  c) For f=45Hz

https://github.com/user-attachments/assets/9359d24f-8974-43af-99d5-4b2e6e588a12



####  d) For f=100Hz

https://github.com/user-attachments/assets/03f0c349-83cb-4cad-812d-e6dab6092ea7

###  Observations
- Low frequency → visible flickering  
- High frequency → steady light  
- Flicker disappears beyond certain frequency.

---
