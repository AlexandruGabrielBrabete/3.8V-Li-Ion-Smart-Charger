# 3.8V-Li-Ion-Smart-Charger

Project Overview


This project focuses on the design and physical implementation of an intelligent charging system for 3.8V nominal Li-Ion/LiFePO4 batteries. The system utilizes a high-precision LT3080 linear regulator for voltage and current control, an AD8210 bidirectional amplifier for current monitoring, and a 4-stage LED bargraph for real-time visual feedback.
LTSpice Simulation and Design

The circuit was validated through LTSpice simulations to ensure the correct functioning of the charging logic:

    CC/CV Charging Strategy: The simulation confirms a Constant Current (CC) phase at approximately 201mA, followed by a Constant Voltage (CV) phase capped at 4.2V.

    Control Loops: The LM339 manages the CC mode by monitoring the AD8210 output, while the LM741 acts as an error amplifier for the CV mode to maintain the 4.2V threshold.

    Visual Validation: Activation thresholds for the 4 LEDs (Red, Yellow, Green, Blue) were simulated at specific voltage points: 2.85V, 3.34V, 3.74V, and 4.117V.

Hardware Implementation

The physical prototype was constructed on a dual-breadboard system and powered via a micro-USB module:

    Core Components: An LT3080 serves as the main power regulation element, an AD8210 monitors current across a shunt resistor, and an AD584 provides a stable voltage reference for threshold comparisons.

    Testing Configuration: To validate the circuit without a live battery, specific resistive loads were used: two 10 Ohm resistors for discharge simulation, and 270 Ohm and 22 Ohm resistors for precise current and voltage drop measurements.

    Hardware Results: Physical testing showed an output voltage of 4.17V and a current of 149.9mA on the 22 Ohm load with the potentiometer fully open.

Word Documentation and Analysis

The project includes a detailed technical report covering:

    Mathematical Dimensioning: Calculations for the resistive dividers used to set the CC/CV limits and the bargraph trigger levels.

    Functional Decomposition: A breakdown of the power control block, the precision reference block, and the visual monitoring logic.

    Result Interpretation: Analysis of the transient response during the control transfer between current and voltage loops.

Students

    Alexandru Gabriel Brabete 

    Botizan Thomas 

Year of Study: 3

University: Technical University of Cluj-Napoca 

Faculty: Faculty of Electronics, Telecommunications and Information Technology
