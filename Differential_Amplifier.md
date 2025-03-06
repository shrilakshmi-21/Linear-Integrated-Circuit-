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
  ### PROCEDURE:
  * Make the circuit as per the designed specification.
  * Give the length and width of both the MOSFETS.
  * Go to the simulation>operating point>place the .op extension.
  * Run the simulation.
  * You will find all the voltages and current flowing in the circuit.
  * Compare the obtained result with the designed values and ensure if the values match for the given length and width of the MOSFET.
    
  The main motive is to ensure the power specification, i.e., P<=1mW  
  For l=180n and w=19.3625u, got the following specification:  
  <img width="382" alt="op analysis" src="https://github.com/user-attachments/assets/d0485cd3-1e0a-49dd-b0f0-cef45fb44d00" />  
  Obtained values:  
  * Vp=0.4V
  * Id1=Id2=0.25mA
  * Idss=0.5mA
  * Vout=1.1V
    This implies that for the given width and length, the output obtained matches exactly with the designed values.  

# TRANSIENT ANALYSIS:
  ### PROCEDURE
  * After getting the required operating points from the DC Analysis, right click on the input voltages>advanced>sinusoidal and give the specified DC voltage, amplitude and freuency
  * Go the transient analysis part and give the reqired end time like 5ms.
  * Run the simulation.
  * Calculate the gain of the amplification part.
  ### Maximum input and output swing:
  Maximum input swing is the maximum volatge difference that can be given to the input terminals, while still maintaining linear operation and the output obtained at the corresponding value of input is the output swing.  
  
  Minimum input swing is given by the formula:  
  Vicm(min)=-Vss+Vp+Vgs= 0+0.4+0.6=1V  
  Maximum output swing is given by the formula:  
  Vicm(max)=vt+Vdd-(I*Rd)/2= 0.497+2-(0.5m*3.6K)/2=1.597V  

  This is the transient analysis obtained when the following values were given:  
  * DC Value: 1V
  * Amplitude: 50m
  * Frequency 1Khz

  <img width="1470" alt="Screenshot 2025-03-05 at 9 45 26 PM" src="https://github.com/user-attachments/assets/d6fe4001-3107-4ccc-a0d7-7f8725a6442e" />  
* From the above waveform, the gain obtained is:  
* Av=(1.10-1.37)/50m=-5.4  
* In dB, 20logAv=14.647dB  

  Maximum input swing:  
  <img width="1470" alt="Screenshot 2025-03-05 at 10 02 04 PM" src="https://github.com/user-attachments/assets/661dc344-026a-48cd-8706-111a5bc83538" />  
* The output waveform is clipped indicating that it has reached saturation region.  
The maximum output obtained is around 2V, which matches with the value of supply voltage, Vdd.  

# AC ANALYSIS:
  ### PROCEDURE:
  * Right click on the voltage>Advanced>Sinusoidal, give AC amplitude as 1.
  * Go to the AC analysis part and run the simulation.
  * The frequency response will appear and calculate 3dB bandwidth.


<img width="1470" alt="Screenshot 2025-03-05 at 10 29 26 PM" src="https://github.com/user-attachments/assets/5f48ea23-b16b-477d-8f64-5508d6220d50" />  
* It is observed that the low frequency response of amplifier is absent and the width of the bandwidth is increased.  
3dB bandwidth= 15.05dB-3dB=12.05dB=3.79Ghz.




  



  
  
  
  




