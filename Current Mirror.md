# AIM:
Design and analyze current mirror circuit as an active load in an amplifier and to analyze the characteristics of the circuit with DC, AC and transient analysis.

# THEORY:
A current mirror is a circuit designed to copy(mirror) a refrence current from one branch to another. It is widely used in biasing and active loads in amplifier circuits due to its high output resistance and ability to provide stable current.  
* __Common-source amplifier:__ Current mirror improves gain by increasing output resistance.  
* __Differential amplifier:__ Current mirror enchances gain by common-mode rejection, and signal symmetry.

__Advantages:__
* Increased gain
* Increased bias stability
* Enhances Common-Mode Rejection
* Better Linearity

# DESIGN SPECIFICATIONS:
Av>=10V/V, Vdd=1.8V, P<=1mW  
__Design:__  
* P<=1mW<br>
I=P/Vdd=0.5555mA
* 1:1 Ratio<br>
Itotal=0.5555mA<br>
Iref=Ix=0.2777mA
* 1:2 Ratio<br>
Itotal=0.5555mA<br>
Iref=0.1851mA and Ix=0.3703mA

# CIRCUIT 1:
Common source amplifier:  
![image](https://github.com/user-attachments/assets/24601c01-0791-4015-acf1-7913bc3491fe)  

# 1:1 Current Ratio:
## L=180nm:
## DC ANALYSIS:  

* __M1:(PMOS)__<br>
L=180n, W=10u
* __M2:(PMOS)__<br>
L=180n, W=10u
* __M3:(NMOS)__<br>
L=180n, W=2.179u
![image](https://github.com/user-attachments/assets/3c468ed6-7bdf-4300-8c42-aad3b43609d2)

## TRANSIENT ANALYSIS:
![image](https://github.com/user-attachments/assets/98af6882-4209-4c0e-bbb6-7779d062dde5)  
* Peak voltage: 1.411V
* Minimum voltage: 0.477
* Gain: 1.411 - 0.477 / 0.899 - 0.850  <br>
Av: 9.67V/V

## AC ANALYSIS:
![image](https://github.com/user-attachments/assets/4fb3e322-b98a-4016-a120-b5bb9a4e72a9)  
3dB gain: 21dB-3dB= 18dB => 1.009GHz

## L=500nm:
## DC ANALYSIS
* __M1:(PMOS)__<br>
L=180n, W=10u
* __M2:(PMOS)__<br>
L=180n, W=10u
* __M3:(NMOS)__<br>
l=500n, W=5.71u<br>
![image](https://github.com/user-attachments/assets/581fee7e-d83e-46f2-b5d9-071df64b67ab)

## TRANSIENT ANALYSIS: 
![image](https://github.com/user-attachments/assets/04de7153-75e6-46bd-9788-5a55a4165a0f)  
* Peak voltage: 1.48V
* Minimum voltage: 0.321V

## AC ANALYSIS:
![image](https://github.com/user-attachments/assets/50bec916-5ead-4886-ab91-29cc3bf83cf1)  
3dB gain: 25.371dB-3dB => 531.987MHz

## L=1u:
## DC ANALYSIS:
* __M1:(PMOS)__<br>
L=180n, W=10u
* __M2:(PMOS)__<br>
L=180n, W=10u
* __M3:(NMOS)__<br>
L=1u, W=10.253u<br>
![image](https://github.com/user-attachments/assets/b557299f-2b01-4ebf-88fd-974895cc9895)

## TRANSIENT ANALYSIS:
![image](https://github.com/user-attachments/assets/a4658a52-02d2-4586-b792-16a34353e4aa)  
* Peak voltage: 1.5V
* *Minimum voltage: 0.316V

## AC ANALYSIS:
![image](https://github.com/user-attachments/assets/2ae2c540-bd8c-4ff7-8622-a354f37112b5)  
3dB gain: 25.824dB-3dB => 463.226MHz

# 1:2 CURRENT RATIO:
## L=180nm:  
## DC ANALYSIS:
* __M1:(PMOS)__<br>
L=180n, W=10u
* __M2:(PMOS)__<br>
L=180n, W=20u
* __M3:(NMOS)__<br>
L=180n, W=3.02u<br>














