# Linear-Integrated-Circuit-
## Aim
Analyse the CS Amplifier and extract the parameters: DC Operating point, DC analysis, gain, power  
<br>
## Specifications
180nm, tsmc, VDD=1.8V, Power budget=50uW




## Components required
Resistor(1Kohm), NMOS4, DC power supply, PMOS4

## Introduction
CS Amplifier is a voltage amplification circuit, where input signal is applied at the gate terminal and output is taken at the drain of the circuit. This configuration yields high gain and less power dissipiation.  
A circuit to act as an amplifier, it should be in the saturation region  
Condition for saturation region:  
* NMOS: Vgs>Vt & Vds>Vov
* PMOS: Vsg>Vt & Vsd>Vov
Gain:
Av=Vout/Vin & Av=-Gm*Rout this indicates how much the input signal is amplified with respect to voltage 

## Task 1: CS Amplifier with resistive load
## Procedure
1. Set VDD=1.8V, input voltage as 0.9V.
2. Connect the resitor(1kohm) to the drain of the NMOS and make the source as ground.
3. Set the width and length of the NMOS to get the required current.
4. Give the appropriate values so as to get the DC, Transient and AC analysis.
5. Extract the required parameters.

## Analysis
For the given specification we have to ensure that the MOSFET operates in saturation region and obtain the current as 27.77uA.
So to get the required current, the obtained length and width of the MOSFET is 500nm and 487nm respectively. The circuit diagram is shown in the fig below.
  
  ![image](https://github.com/user-attachments/assets/5808b121-3db3-4f2d-8eb6-26ce52d2bfa1)

### DC Operating point
  ![image](https://github.com/user-attachments/assets/fc1c1ded-6419-4110-ad42-aee89b1156a5)
              
The output voltage obtained is 1.772V.
Power dissipiation across resistive load=(Vdd-Vout)*IR1=5.97uW

### Transient analysis
  ![image](https://github.com/user-attachments/assets/62066575-7eb1-4945-8706-d521f0583420)

From the above waveform we can see that the MOSFET acts as a linear amplifier.
Av=Vout/Vin=2(approx)

### AC Analysis
  ![image](https://github.com/user-attachments/assets/9e221784-3b75-4837-8b5c-219f202a41e4)
  ![image](https://github.com/user-attachments/assets/1cb0f361-4de5-4da3-8cb8-714e4468aa7d)

The gain obtained is 30.54dB

## Task 2: CS Amplifier with current source load
## Procedure
For the previous circuit replace the load resistor with the PMOS and give the required voltage.

## Analysis
For the given specification we have to ensure that both the MOSFETS operates in the saturation region and obtain the current as 27.77uA.
So to get the required current, the obtained length and width of the NMOS is 180nm and 300um respectively.

### DC Operating point
  ![WhatsApp Image 2025-02-17 at 21 51 56_f96d02ea](https://github.com/user-attachments/assets/9f097dfb-a5f5-48e4-893b-aefaec9bb538)

The output voltage obtained is 1.79986V.
Power dissipiation in PMOS=(Vdd-Vout)*Id=3.9nW

### Transient analysis
![WhatsApp Image 2025-02-17 at 21 55 50_2b7c2955](https://github.com/user-attachments/assets/ab280f43-c367-47d3-ad50-1390c2522752) ![WhatsApp Image 2025-02-17 at 21 54 47_05ed27c3](https://github.com/user-attachments/assets/2df975be-c9e2-4fa2-884f-d51d04e81e45)
When the resistive load is replaced with the pmos, it acts like an inverter

### AC analysis
![WhatsApp Image 2025-02-17 at 21 57 29_cf6eaae7](https://github.com/user-attachments/assets/51cb3c96-3a9f-4b51-9362-e5b34060b17a)
![WhatsApp Image 2025-02-17 at 21 59 04_ed01b0df](https://github.com/user-attachments/assets/c9e71e70-08a9-40a5-8b96-f71b863ba2e7)  

The gain obtained is 37.019dB

## RESULT
### CS Amplifier with resistive load
* L=500nm, W=487nm
* Id= 27.727uA for power 50uW
* Q point= (1.77V, 27.7uA)
* Gain=30.54dB
* Power=5.97uW

### CS Amplifier with current source load
* L=180nm, W=300um
* Id= 27.7uA
* Q point=(1.79V, 27.7uA)
* Gain=37.019dB
* Power=3.9nW

## INFERENCE
* By replacing the resistive load with PMOS it is observed that the gain is increased.
* It is also observed that the power dissipation is also decreased when resistive load is replaced with the PMOS.






 




