# LIC-Simulations
Simulations and analysis of Linear Integrated Circuits using LTSpice. Contains schematics, waveform analysis, and circuit design experiments.

# Experiment-1
Question : For the given circuits with power P=50μW, do DC, transient, and AC analysis. Also, check what happens when the width of each MOSFET is increased or decreased.


# Theory

A Common Source (CS) amplifier is a basic transistor amplifier where the input is applied to the gate and the output is taken from the drain of a MOSFET. It provides high voltage gain and inverts the output signal. The amplifier works by controlling the drain current based on the gate-to-source voltage, which amplifies the input signal. The CS amplifier has high input impedance and moderate to high output impedance, making it useful in amplifying small signals in various electronic applications.


#  Circuit Design-1 :

   ![Screenshot 2025-02-17 210653](https://github.com/user-attachments/assets/739b8958-7ec7-4a87-9e13-cdb6594f7ed5)


# Components Details

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

# Procedure :

1. Assemble the circuit connections.
2. Connect a 1k ohm drain resistor(RD) to the MOSFET's gate, while keeping the source terminal grounded.
3. Apply a 0.9V voltage source to the MOSFET's gate, while keeping the source terminal grounded.
4. Provide a 1.8V supply (VDD) to the drain resistor (RD).
5. Set the MOSFET's length to 180nm and width to 1μm.
6. Conduct DC analysis, transient analysis, and AC analysis by applying a sine wave to the gate voltage source.
7. Assume power = 50μW and calculate the corresponding drain current (Id).
8. Fix the MOSFET's length at 180nm and adjust the width until the calculated Id is achieved.
9. Perform DC analysis, and transient analysis, and AC analysis again by applying a sine wave to the gate voltage source.

 DC Analysis:
 
   DC analysis examines how a circuit behaves with direct current (constant voltage) applied. It helps determine values like current and voltage in a steady-state 
   condition, where everything is stable and not changing over time.

   Procedure for Performing DC Analysis:
   Select the dc output print(DC op pnt) in the Edit Simulation Command and Run the Simulation

   ![image](https://github.com/user-attachments/assets/682cb6c0-8015-4828-ab1b-c2fe8d1bf67b)


   The Figure below shows the Values obtained from the DC Analysis : 
   
   ![Screenshot 2025-02-17 202600](https://github.com/user-attachments/assets/729b5704-6c35-4124-909a-fb3ea8a42040)
   

Transient Analysis:

   Transient analysis shows how a circuit responds over time to changes, like when a signal is applied or turned off. It helps us understand how voltages and currents 
   change before the circuit stabilizes.

   Procedure for Performing Transient Analysis:
   Select the Transient Analysis in the Edit Simulation Command,  Give the stop time as 1ms and Run the Simulation.

   ![image](https://github.com/user-attachments/assets/8a268dab-e63f-4419-88ca-5bead7d293ac)


   The Graph below shows the Transient Response of the Given Design;

  ![Screenshot 2025-02-17 202758](https://github.com/user-attachments/assets/2d77caa8-055d-4bcc-81dd-33d71e7e7027)
  
  V2 is a sine wave that starts at 0.9V, has a peak-to-peak variation of 50mV, and oscillates at a frequency of 1kHz.

   
AC Analysis:

   AC analysis looks at how a circuit behaves when alternating current (AC) signals are applied. It helps measure how the circuit responds to different frequencies, 
   including changes in voltage, current, gain, and phase shift.

   Procedure for Performing Transient Analysis:
   ![Screenshot 2025-02-17 212924](https://github.com/user-attachments/assets/0e4fcf35-33c9-46e3-9bfb-0ea262e28149)

   
   The Graph below shows the AC Analysis of the Given Design;

  ![Screenshot 2025-02-17 203009](https://github.com/user-attachments/assets/3b349fed-caf5-4501-ac04-74dd0fa163b7)

When Power = 50μW 

DC Analysis:

![Screenshot 2025-02-17 213831](https://github.com/user-attachments/assets/f9d5a7ee-fb03-41d6-b9f3-9f9961fbedee)

![Screenshot 2025-02-17 213818](https://github.com/user-attachments/assets/2518f107-6281-4bf3-b86a-8df5693386ad)

Transient Analysis:

![Screenshot Image 2025-02-17 at 9 34 55 PM](https://github.com/user-attachments/assets/faa597a4-9595-4096-a157-dcb68d40292f)

AC Analysis:

![Screenshot 2025-02-17 212924](https://github.com/user-attachments/assets/be0b7a6b-3e73-465c-8f35-1c77d8bab210)


![screenshot Image 2025-02-17 at 9 34 55 PM (2)](https://github.com/user-attachments/assets/76d55a42-7fe8-4ad4-bcd6-957128df144f)

# Calculation

Given power = 50 µW and VDD = 1.8 V,

Using the formula for power:
Power = Voltage × Current

We can rearrange to find the drain current (Id):
P = VDD x Id
Id = P/VDD
Substituting the values,
Id = 50μW/1.8V
Id = 2.77 × 10^-5 A

# RESULT( Design-1):
 1) DC Analysis:
     -The calculated drain current (Id) matches the expected value based on power and voltage, with Id = 1.52735×10^-4A
     -By adjusting the MOSFET’s channel dimensions, where length is 180nm and width is 1μm and the required current was successfully achieved.
     -The circuit performs as expected under DC conditions.
    
 2) Transient Analysis:
     -The transient response graph shows the circuit’s behavior over time.
     -The response is smooth, with no unexpected delays or distortions.
     -The circuit responds well to changes, confirming its stability.

 3) AC Analysis:
     -The AC response graph verifies that the circuit remains stable at different frequencies.
     -The gain (4.8 dB) when power = 50μW and phase shift (nearly 180°) match theoretical expectations 
     -The circuit maintains consistent performance across the tested frequency range.

# INFERENCE( Design-1):
  The experiment shows that by choosing the right MOSFET dimensions, we can control the drain current easily.

Impact of Width Adjustments:

M1 affects Id, which means its width changes the output current. When the width increases, Id increases, and when the width decreases, Id decreases.
The circuit worked well in all three analyses—DC, transient, and AC—showing that it’s stable and reliable.
Overall, the design worked as expected, matching the theory and proving that it’s practical.



# Design-2

![Screenshot 2025-02-17 225356](https://github.com/user-attachments/assets/f07fcf2f-7c9e-4d64-916c-8bbb05f61795)


# Aim : To determine the DC operating point and calculate the gain using transient and AC analysis.

# Components Details

MOSFETs, M1 - NMOS and M2 - PMOS
DC Power Supply

# Procedure :

1. Make the circuit connections.
2. Use a CMOSN MOSFET in the design.
3. Connect the CMOSP to the drain of the CMOSN.
4. Apply a 0.9V voltage source to the gate of CMOSN, and ground the source of CMOSN.
5. Apply a VDD (1.8V) to the CMOSP.
6. Set the length and width of the CMOSN to be the same as in the previous circuit.
7. Set the length of CMOSP to 180n, and vary the width until the calculated Id value matches the previous circuit.
8. Perform DC analysis, transient analysis, and AC analysis by applying a sine wave to the voltage source at the gate.

DC Analysis
 DC analysis examines how a circuit behaves with direct current (constant voltage) applied. It helps determine values like current and voltage in a steady-state 
 condition, where everything is stable and not changing over time.

 Procedure for Performing DC Analysis:
 Select the dc output print(DC op pnt) in the Edit Simulation Command and Run the Simulation

![Screenshot Image 2025-02-17 at 11 13 44 PM](https://github.com/user-attachments/assets/b0eb39c9-8e30-48c2-8f9e-536546f5e664)

![Screenshot Image 2025-02-17 at 11 13 44 PM](https://github.com/user-attachments/assets/50fdaf5d-553d-4afe-b4cd-2ab5cf4503c4)


Transient Analysis
  Transient analysis shows how a circuit responds over time to changes, like when a signal is applied or turned off. It helps us understand how voltages and currents 
  change before the circuit stabilizes.

  Procedure for Performing Transient Analysis:
  Select the Transient Analysis in the Edit Simulation Command,  Give the stop time as 1ms and Run the Simulation.

  ![Screenshot Image 2025-02-17 at 11 13 44 PM](https://github.com/user-attachments/assets/502904ac-690d-41ba-a8c3-a5703dbe08cc)

  ![Screenshot Image 2025-02-17 at 11 13 44 PM](https://github.com/user-attachments/assets/02ddef2c-78e4-4a4a-be18-a7e594ca29f3)

  ![Screenshot Image 2025-02-17 at 11 13 44 PM](https://github.com/user-attachments/assets/a63218ec-7881-4b93-9025-a701461f1f55)


  AC Analysis
     AC analysis looks at how a circuit behaves when alternating current (AC) signals are applied. It helps measure how the circuit responds to different frequencies, 
     including changes in voltage, current, gain, and phase shift.

   Procedure for Performing Transient Analysis:
   
   ![Screenshot Image 2025-02-17 at 11 13 44 PM](https://github.com/user-attachments/assets/efa9b4e6-ae3b-48bd-9d3f-1207faf29902)

   ![Screenshot Image 2025-02-17 at 11 13 45 PM](https://github.com/user-attachments/assets/733c5175-22b1-43e8-8ee3-5785c3434b2e)
   

# Calculation

To find V2:
|VG-VS|>|Vt|
|VG-1.77>|-0.366|
|VG|>1.38

# RESULT( Design-1):
1.DC Analysis:
 The DC analysis shows the steady-state operating points of the circuit. The output point confirms that the MOSFETs are properly biased. The voltage at both the drain and 
 gate matches the expected operating conditions for the CMOSN and CMOSP MOSFETs.

2.Transient Analysis:
 In the transient analysis, the input is a sine wave with a 0.9V DC offset, 50mV amplitude, and 1kHz frequency. The output signal at the drain of the CMOSN MOSFET is an 
 amplified version of the input, showing the expected behavior of amplification.

3.AC Analysis:
 The AC analysis checks the frequency response of the amplifier, sweeping from 0.1Hz to 1THz and analyzing the gain over this range. The resulting graph shows the 
 amplifier’s frequency response, which helps us understand its bandwidth and gain characteristics.

    
# INFERENCE( Design-1):
1. The experiment confirms that by carefully selecting the MOSFET dimensions (L and W), the drain current can be controlled accurately.
2. The voltage transfer characteristics (VTC) were useful in determining the correct operating voltage (0.8V) for saturation.
3. Impact of Width Adjustments:
   - M2 has a greater effect on Id, meaning its width strongly influences the output current. Increasing the width significantly raises Id, and decreasing it lowers Id.
​   - M1 has a lesser effect, so changes in its width only cause minor variations in Id. Increasing its width slightly raises Id, and decreasing it reduces Id.
4. The design meets the expected performance criteria, aligns with theoretical predictions, and shows practical feasibility for real-world applications.

