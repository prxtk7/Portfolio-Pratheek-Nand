# Exercise 3: Sensors & Actuators



##  Overview
This exercise focused on building an interactive pneumatic circuit using an Arduino to control a pillow's inflation and deflation via two air pumps and a valve. Moving beyond basic displays, this project introduced physical actuation to perform real-world actions.

The workflow was split into two phases: 
- Part A — Pneumatic & Electrical Circuit &
- Part B — Sensor Interaction


---


##  Part A – Pneumatic & Electrical Circuit

###  How MOSFET Modules Work

Each IRF520 MOSFET is mounted in a module between the Arduino and a high-current actuator. The Arduino sends a digital HIGH or LOW to the SIG pin of the module - HIGH turns the load ON and LOW turns it OFF. The load side is powered separately from the lab power supply with a common ground between the two sides. Each module has a status LED on board which lights up when the MOSFET is conducting – very handy for debugging.

###  Pneumatic Circuit Logic

The valve (FA0520E) is a 3-port valve and acts as a pneumatic relay:

- Unpowered → Shared port connected to metal end port (inflation path open)
- Powered → Common port changes to plastic-end port (deflation path open)

By combining the state of the valve with which pump is running , we could switch between inflating and deflating the pillow .

####  Circuit Setup

<img width="400" height="370" alt="pneumatic circuit setup" src="https://github.com/user-attachments/assets/4cb80848-7b53-471a-ba27-eb9e859c7fc9" />

###  Initial Testing & Troubleshooting

Our first test didn’t go quite as planned. While the inflation pump worked perfectly—proving the basic circuit and code were solid—the pillow completely refused to deflate.

At first, I figured it was a software bug or a glitch with the MOSFET switching. However, after double-checking the Arduino code and verifying the outputs, the code checked out. The real culprit was mechanical: the pneumatic plumbing was tangled up.

It took a few tries to figure out how air actually moves through the valve and tubing. My supervisor stepped in to help spot the setup mistakes and explain how the valve physically routes air between the inflation and deflation paths. Once we corrected the tubing layout and tweaked the actuator timing, everything clicked, and the system now inflates and deflates flawlessly.

####  Demonstration

https://github.com/user-attachments/assets/bddcae9d-483e-4206-9605-a52f6742cf2d

###  The Working Prototype

Our first test didn’t go quite as planned. While the inflation pump worked perfectly—proving the basic circuit and code were solid—the pillow completely refused to deflate.

At first, I figured it was a software bug or a glitch with the MOSFET switching. However, after double-checking the Arduino code and verifying the outputs, the code checked out. The real culprit was mechanical: the pneumatic plumbing was tangled up.

It took a few tries to figure out how air actually moves through the valve and tubing. My supervisor stepped in to help spot the setup mistakes and explain how the valve physically routes air between the inflation and deflation paths. Once we corrected the tubing layout and tweaked the actuator timing, everything clicked, and the system now inflates and deflates flawlessly.

####  Demonstration

https://github.com/user-attachments/assets/d4c3e7c1-34e5-424d-a1a1-2b0ddeabde93


###  Observations
- I learned that perfect code and wiring don't guarantee success; the physical air tubing configuration matters just as much as the electronics.
- The status LEDs on the MOSFET modules were lifesavers, letting me instantly verify that the control signals were actually reaching the actuators.
- The experience reinforced the value of systematic debugging—breaking the system down to test the hardware and software separately to pinpoint issues quickly.


##  Part B – Sensor Interaction

###  The Interface: Dual Ultrasonic Sensors (HC-SR04 × 2)

We set up two ultrasonic distance sensors side-by-side to serve as our touch-free control panel. Each sensor constantly monitors the space in front of it, triggering an action whenever your hand gets close enough to cross a set distance threshold:

- Left Sensor: Covers the sensor to turn on the inflation pump, filling the pillow.

- Right Sensor: Covers the sensor to flip the valve and activate the deflation pump.

- Hands Off: Pulling your hands away instantly stops all pumps.

Why this design? Instead of messing with buttons or complex gestures, we wanted the control to feel completely natural and direct. Having two dedicated sensors functions like a hot and cold water tap—one hand handles inflation, the other handles deflation. It is completely intuitive, requires no physical button presses, and responds instantly to simple hand movements.

###  Senor Integration

We started by testing the ultrasonic sensor on its own using basic Arduino example code to make sure it was reading distances correctly. Once verified, we wired it into the main pneumatic circuit and updated our program so that hand movements would trigger the pumps and valve. Finally, we hooked everything up to the inflatable pillow and ran it through multiple test cycles to ensure the inflation and deflation loops worked smoothly and reliably every time.

####  Demonstration

https://github.com/user-attachments/assets/a5ef4165-3fdf-4845-be44-34c02b9cee7f


###  Observations
- The ultrasonic sensors provided a fast, lag-free way to control the pneumatic system.
- Instead of traditional distance tracking, the space in front of the sensors was split into "interaction zones," eliminating the need for physical buttons or switches.
- The setup proved that standard electronic components can be creatively repurposed for unique, touch-free user experiences.
- The exercise perfectly demonstrated how seamlessly sensors and actuators can team up to turn digital code into real-world physical movement.


---


##  Conclusion

By bridging digital sensing with physical plumbing, this project highlighted that successful prototyping goes beyond writing correct code—it requires orchestrating hardware, software, and mechanical dynamics to work as a unified system.



---
