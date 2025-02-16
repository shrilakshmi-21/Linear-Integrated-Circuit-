# Linear-Integrated-Circuit-
## AIM
Analyse the CS Amplifier and extract the parameters: DC Operating point, DC analysis, gain, bandwidth, power 

## SPECIFICATIONS
180nm, tsmc, VDD=1.8V, Power budget=50uW

## COMPONENTS REQUIRED
Resistor(1Kohm), NMOS4, DC power supply, PMOS4

## TASK 1
## PROCEDURE
1. Set VDD=1.8V, input voltage as 0.9V.
2. Connect the resitor(1kohm) to the drain of the NMOS and make the source as ground.
3. Set the width and length of the NMOS to get the required current.
4. Give the appropriate values so as to get the DC, Transient and AC analysis.
5. Extract the required parameters.

## ANALYSIS
For the given specification we have to ensure that the MOSFET operates in saturation region and obtain the current as 27.77uA.
So to get the required current, the obtained length and width of the MOSFET is 500nm and 487nm respectively.
The output voltage obtained is 1.772V.
The gain obtained is 30.54dB

## TASK 2
## PROCEDURE
For the previous circuit replace the load resistor with the PMOS and give the required voltage.

## ANALYSIS
For the given specification we have to ensure that both the MOSFETS operates in the saturation region and obtain the current as 27.77uA.
So to get the required current, the obtained length and width of the NMOS is 180nm and 600nm respectively.
The output voltage obtained is 1.66008V.
The gain obtained is 
![image](https://github.com/user-attachments/assets/5a6a4fde-7869-44d9-af9d-1020747ade7c)



