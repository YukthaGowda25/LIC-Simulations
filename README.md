# LIC-Simulations
Simulations and analysis of Linear Integrated Circuits using LTSpice. Contains schematics, waveform analysis, and circuit design experiments.

# Experiment-1
Question : For the given circuits with power P=50μW, do DC, transient, and AC analysis. Also, check what happens when the width of each MOSFET is increased or decreased.

# Design-1 :

   ![Screenshot 2025-02-17 210653](https://github.com/user-attachments/assets/739b8958-7ec7-4a87-9e13-cdb6594f7ed5)


Components Details

The circuit features a TSMC 180nm NMOS transistor (CMOSN), along with a drain resistor and two voltage sources. The drain resistor regulates the current flow through the transistor, influencing the small signal gain. The NMOS transistor operates in the saturation region, making it ideal for amplification.
Model : CMOSN
MOSFET Length: 180nm
MOSFET Width : 1um
Threshold Voltage : 0.366V
Resistor Value : 1k
Supply Voltage : 1.8V
Signal Generator :
       DC Value : 0.9V
       Amplitude : 50mV
       Frequency : 1kHz

Procedure :

1. Assemble the circuit connections.
2. Connect a 1k ohm drain resistor(RD) to the MOSFET's gate, while keeping the source terminal grounded.
3. Apply a 0.9V voltage source to the MOSFET's gate, while keeping the source terminal grounded.
4. Provide a 1.8V supply (VDD) to the drain resistor (RD).
5. Set the MOSFET's length to 180nm and width to 1μm.
6. Conduct DC analysis, transient analysis, and AC analysis by applying a sine wave to the gate voltage source.
7. Assume power = 50μW and calculate the corresponding drain current (Id).
8. Fix the MOSFET's length at 180nm and adjust the width until the calculated Id is achieved.
9. Perform DC analysis, and transient analysis, and AC analysis again by applying a sine wave to the gate voltage source.

 DC ANALYSIS:

   Procedure for Performing DC Analysis:
   Select the dc output print(DC op pnt) in the Edit Simulation Command and Run the Simulation

   ![image](https://github.com/user-attachments/assets/682cb6c0-8015-4828-ab1b-c2fe8d1bf67b)


   The Figure below shows the Values obtained from the DC Analysis : 
   
   ![Screenshot 2025-02-17 202600](https://github.com/user-attachments/assets/729b5704-6c35-4124-909a-fb3ea8a42040)
   

Transient Analysis:

   Procedure for Performing Transient Analysis:
   Select the Transient Analysis in the Edit Simulation Command,  Give the stop time as 1ms and Run the Simulation.

   ![image](https://github.com/user-attachments/assets/8a268dab-e63f-4419-88ca-5bead7d293ac)


   The Graph below shows the Transient Response of the Given Design;

  ![Screenshot 2025-02-17 202758](https://github.com/user-attachments/assets/2d77caa8-055d-4bcc-81dd-33d71e7e7027)


   
AC Analysis:
   
   The Graph below shows the AC Analysis of the Given Design;

  ![Screenshot 2025-02-17 203009](https://github.com/user-attachments/assets/3b349fed-caf5-4501-ac04-74dd0fa163b7)

# RESULT( Design-1):
 1) DC Analysis:
     -The calculated drain current (Id) matches the expected value based on power and voltage, with Id = 1.52735×10^-4A.
     -By adjusting the MOSFET’s channel dimensions, where lenght is 180nm and width is 1μm and the required current was successfully achieved.
     -The circuit performs as expected under DC conditions.
    
 2) Transient Analysis:
     -The transient response graph shows the circuit’s behavior over time.
     -The response is smooth, with no unexpected delays or distortions.
     -The circuit responds well to changes, confirming its stability.

 3) AC Analysis:
     -The AC response graph verifies that the circuit remains stable at different frequencies.
     -The gain (4.8 dB) and phase shift (nearly 180°) match theoretical expectations.
     -The circuit maintains consistent performance across the tested frequency range.

# INFERENCE( Design-1):
  The experiment shows that by choosing the right MOSFET dimensions, we can control the drain current easily.

Impact of Width Adjustments:

M1 affects Id, which means its width changes the output current. When the width increases, Id increases, and when the width decreases, Id decreases.
The circuit worked well in all three analyses—DC, transient, and AC—showing that it’s stable and reliable.
Overall, the design worked as expected, matching the theory and proving that it’s practical.

