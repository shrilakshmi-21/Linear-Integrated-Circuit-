# AIM:  
Design differential amplifier for the following specifications:  
Vdd=2V, P<=1mW, Vicm=1V, Vocm=1.1V and Vp=0.4V.  
Perform DC analysis, transient analysis, frequency response and extract the required parameters.  

# THEORY:
  Differential amplifier is a type of amplifier which has 2 inputs and amplifies the difference between the two inputs.  
  Advantages of differential amplifiers over normal amplifiers:  
  * Reject noise signals.
  * It has hign gain.
  * Coupling capacitors are not used, thereby incresing the width of the bandwitdh by almost cancelling out the low frequency response of the amplification process.

  It has 2 input signals and can be classified as:
  * Common mode input voltage: We give the same voltage to both the input signals.
  * Differential mode input voltage: Two different voltages are given to different input signals.
In this simulation we are going to observe how the differential amplifier acts when we give common input voltage.  

# DESIGN:
* P=VI  
  P=Vdd*Iss  
  Iss=1m/2=0.5mA  
* Id1=Id2=Iss/2=0.5m/2=0.25mA  
* Rd=(Vdd-Vocm)/Id  
  Rd=(2-1.1)/0.25m=3.6Kohm  
* Rss=Vp/Iss  
  Rss=0.4/0.5m=800ohm
* Vgs=Vg-Vs
  Vgs=1-0.4=0.6V
* Vds=Vd-Vs
  Vds=1.1-0.4=0.7V
* Q-point=(0.7, 0.25m)@Vgs=0.6V

# CIRCUIT 1:  
  <img width="1470" alt="C1" src="https://github.com/user-attachments/assets/175c9830-9f67-400f-bea8-e43c87b65136" />

# DC ANALYSIS:  
  The main motive is to ensure the power specification, i.e., P<=1mW  
  For l=180n and w=19.3625u, got the following specification:  
  <img width="382" alt="op analysis" src="https://github.com/user-attachments/assets/d0485cd3-1e0a-49dd-b0f0-cef45fb44d00" />  
  Obtained values:  
  * Vp=0.4V
  * Id1=Id2=0.25mA
  * Idss=0.5mA
  * Vout=1.1V  

# TRANSIENT ANALYSIS:
  
  




