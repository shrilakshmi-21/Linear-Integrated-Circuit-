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
__Common source amplifier:__
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
* Gain: 21dB
* 3dB bandwidth: 21dB-3dB= 18dB => 1.009GHz

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
* Gain: 25.371dB
* 3dB bandwidth: 25.371dB-3dB => 531.987MHz

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
* Minimum voltage: 0.316V

## AC ANALYSIS:
![image](https://github.com/user-attachments/assets/2ae2c540-bd8c-4ff7-8622-a354f37112b5)  
* Gain: 25.824dB
* 3dB bandwidth: 25.824dB-3dB => 463.226MHz

# RESULT:
## For 1:1 Ratio
| LENGTH | W/L | GAIN(in dB) | BANDWIDTH |
| ------ | --- | ----------- | --------- |
| 180n   | 2.179u/180n | 21dB | 1.009GHz |

# 1:2 CURRENT RATIO:
## L=180nm:  
## DC ANALYSIS:
* __M1:(PMOS)__<br>
L=180n, W=10u
* __M2:(PMOS)__<br>
L=180n, W=20u
* __M3:(NMOS)__<br>
L=180n, W=3.02u<br>
![image](https://github.com/user-attachments/assets/21714b50-1ecd-4b89-8978-c66cca19efb6)

## TRANSIENT ANALYSIS:
<img width="1470" alt="Screenshot 2025-04-03 at 10 57 21 PM" src="https://github.com/user-attachments/assets/486ed226-5f03-42a3-ab4b-d67c0a784965" />  

* Peak voltage: 1.407V
* Minimum voltage: 0.417V

## AC ANALYSIS:
<img width="1470" alt="Screenshot 2025-04-03 at 11 02 00 PM" src="https://github.com/user-attachments/assets/fdbe587e-fe37-479a-86d0-b9ca57c2bd96" />  
* Gain: 21.389dB
* 3dB bandwidth: 21.389dB-3dB => 406.105MHz

## L=500nm:
## DC ANALYSIS:
* __M1:(PMOS)__<br>
L=180n, W=10u
* __M2:(PMOS)__<br>
L=180n, W=20u
* __M3:(NMOS)__<br>
L=500n, W=7.68u<br>
<img width="582" alt="Screenshot 2025-04-03 at 11 06 25 PM" src="https://github.com/user-attachments/assets/d8f48abb-53df-4a3f-8df5-12ab9f2eee7e" />

## TRANSIENT ANALYSIS:
<img width="1470" alt="Screenshot 2025-04-03 at 11 11 12 PM" src="https://github.com/user-attachments/assets/9cde1d13-51ea-4fc7-bf02-b967621d1e09" />
* Peak voltage: 1.513V
* Minimum voltage: 0.315V

## AC ANALYSIS:
<img width="1470" alt="Screenshot 2025-04-03 at 11 13 27 PM" src="https://github.com/user-attachments/assets/0d3625c9-8e61-4b29-b870-3cda51b87495" />  
* Gain: 25.626dB
* 3dB bandwidth: 25.626dB-3dB => 254.229MHz

## L=1um:
## DC ANALYSIS:
* __M1:(PMOS)__<br>
L=180n, W=10u
* __M2:(PMOS)__<br>
L=180n, W=20u
* __M3:(NMOS)__<br>
L=1u, W=13.75u<br>
<img width="561" alt="Screenshot 2025-04-03 at 11 18 21 PM" src="https://github.com/user-attachments/assets/bd22cdb8-9a7b-4b81-b898-06117733429c" />

## TRANSIENT ANALYSIS:
<img width="1470" alt="Screenshot 2025-04-03 at 11 20 12 PM" src="https://github.com/user-attachments/assets/b7004e83-94f5-4dfc-9bf1-ae7a795fedc3" />
* Peak voltage: 1.521V
* Minimum voltage: 0.317V

## AC ANALYSIS: 
![image](https://github.com/user-attachments/assets/f84c3f24-390f-4ec4-871e-83e6ffbc022d)  
* Gain: 26.080dB
* 3dB bandwidth: 26.080-3dB => 195.658MHz  

# CIRCUIT 2:
__Differential amplifier__
![image](https://github.com/user-attachments/assets/d134c271-d32d-428d-b352-3a36cac4e938)  

## DC ANALYSIS:
![image](https://github.com/user-attachments/assets/f5e2aee1-c8b3-41de-86c5-704160228c0d)  

## TRANSIENT ANALYSIS:
![image](https://github.com/user-attachments/assets/68ea57c3-90c5-4fde-89ca-eb8434df9425)

## AC ANALYSIS:
![image](https://github.com/user-attachments/assets/4fefb772-ae9c-4378-a9c2-98048fdd0d63)  
* Gain: 28.12dB
* 3dB bandwidth: 28.12dB-25.12dB => 741.443MHz



















