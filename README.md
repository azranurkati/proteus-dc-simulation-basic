# proteus-dc-simulation-basic
Proteus üzerinde DC devre analizi, SPICE modelleme ve temel LED sürücü devresi simülasyonu.
# Proteus Basic DC Circuit Analysis and LED Driver Simulation

This study was carried out to examine the differences between analog and digital simulation models in the Proteus environment, perform DC circuit analysis, and verify circuit theory using current/voltage probes.

Circuit Schematic

![Circuit Schematic](led-simulation.png)

Technical Analysis and Theoretical Calculation

A 10V DC source, a current-limiting resistor (330 Ω), and an analog blue LED model (LED-BIRG) were used in the circuit.

Circuit Analysis with Ohm's Law
- Source Voltage ($V_1$): 10V
- Series Resistor ($R_1$): 330 Ω
- LED Forward Voltage ($V_f$): ~2.28V (Analog SPICE model data)

Voltage drop across the resistor ($V_{R1}$):
$$V_{R1} = V_1 - V_f = 10\text{V} - 2.28\text{V} = 7.72\text{V}$$

Theoretical current expected to pass through the circuit:
$$I = \frac{7.72\text{V}}{330\ \Omega} \approx 0.02339\text{A} \ (23.39\text{ mA})$$

Simulation Results
In the DC analysis performed on Proteus, the current measured via current probes was verified as 23.38 mA. The theoretical calculation and simulation results match with 99.9% accuracy.

 Simulation Outputs and Key Takeaways

- Reference Point (GND): It was observed that when a ground (GND) is not added to the circuit diagram, the simulation engine cannot find a reference point and calculates the voltage values incorrectly. A GND connection is mandatory for a stable simulation.

- Digital vs. Analog Model Difference: When the LED element is left in "Digital" mode, it
