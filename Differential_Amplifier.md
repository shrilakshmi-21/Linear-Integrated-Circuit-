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

# COMPONENTS REQUIRED:
* NMOS4
* Current source
* Resistors-36kohm and 800ohm
* Voltage source

# CIRCUIT 1: 
  Differential amplifier with Rss  
  
  <img width="1470" alt="C1" src="https://github.com/user-attachments/assets/175c9830-9f67-400f-bea8-e43c87b65136" />

## DC ANALYSIS:  
  ### PROCEDURE:
  * Make the circuit as per the designed specification.
  * Give the length and width of both the MOSFETS.
  * Go to the simulation>operating point>place the .op extension.
  * Run the simulation.
  * You will find all the voltages and current flowing in the circuit.
  * Compare the obtained result with the designed values and ensure if the values match for the given length and width of the MOSFET.
    
  The main motive is to ensure the power specification, i.e., P<=1mW  
  For l=180n and w=19.3625u, got the following specification:  
  <br>
  <img width="382" alt="op analysis" src="https://github.com/user-attachments/assets/d0485cd3-1e0a-49dd-b0f0-cef45fb44d00" />  
  <br>
  ![image](https://github.com/user-attachments/assets/83399eb7-e92e-4cfa-97f2-c9f3a961fefe)
  <br>
  Obtained values:  
  * Vp=0.4V
  * Id1=Id2=0.25mA
  * Idss=0.5mA
  * Vout=1.1V

    This implies that for the given width and length, the output obtained matches exactly with the designed values.  

## TRANSIENT ANALYSIS:
  ### PROCEDURE
  * After getting the required operating points from the DC Analysis, right click on the input voltages>advanced>sinusoidal and give the specified DC voltage, amplitude and freuency
  * Go the transient analysis part and give the reqired end time like 5ms.
  * Run the simulation.
  * Calculate the gain of the amplification part.


  ### Maximum input and output swing:
  Maximum input swing is the maximum volatge difference that can be given to the input terminals, while still maintaining linear operation and the output obtained at the corresponding value of input is the output swing.  
  
  Minimum input swing is given by the formula:  
  Vicm(min)=-Vss+Vp+Vgs= 0+0.4+0.6=1V  
  Maximum input swing is given by the formula:  
  Vicm(max)=vt+Vdd-(I*Rd)/2= 0.497+2-(0.5m*3.6K)/2=1.597V  

  This is the transient analysis obtained when the following values were given:  
  * DC Value: 1V
  * Amplitude: 50m
  * Frequency 1Khz

  <img width="1470" alt="Screenshot 2025-03-05 at 9 45 26 PM" src="https://github.com/user-attachments/assets/d6fe4001-3107-4ccc-a0d7-7f8725a6442e" />  
  
* From the above waveform, the gain obtained is:  
* Av=(1.10-1.37)/50m=-5.4  
* In dB, 20logAv=14.647dB  
   <br>
   <br>
  Maximum input swing:  
  <img width="1470" alt="Screenshot 2025-03-05 at 10 02 04 PM" src="https://github.com/user-attachments/assets/661dc344-026a-48cd-8706-111a5bc83538" />
   <br>
   <br>
* The output waveform is clipped indicating that it has reached saturation region.  
The maximum output obtained is around 2V, which matches with the value of supply voltage, Vdd.  

## AC ANALYSIS:
  ### PROCEDURE:
  * Right click on the voltage>Advanced>SinE, give AC amplitude as 1.
  * Go to the AC analysis part and run the simulation.
  * The frequency response will appear and calculate 3dB bandwidth.


<img width="1470" alt="Screenshot 2025-03-05 at 10 29 26 PM" src="https://github.com/user-attachments/assets/5f48ea23-b16b-477d-8f64-5508d6220d50" />  
 <br>
<br>
* It is observed that the low frequency response of amplifier is absent and the width of the bandwidth is increased.  
3dB bandwidth= 15.05dB-3dB=12.05dB=3.79Ghz.

# CIRCUIT 2  
  ### Replacing the source resistance with current source  
  <img width="1470" alt="Screenshot 2025-03-05 at 11 09 39 PM" src="https://github.com/user-attachments/assets/fdfd7a86-0e48-4057-a622-967c58d8d9ba" />  
  <br>
  


## DC ANALYSIS  
* For the same design, replace the sourc resistor with a current source and give the Iss value to the current source.
* Check for the operating point.
* Observe if the obtained value matches with the previous one for the same length and width.

<img width="390" alt="Screenshot 2025-03-04 at 10 27 06 PM" src="https://github.com/user-attachments/assets/301ec408-7ccb-4fd1-81d6-4802bdb0d08f" />  
<br>
<br>

Obtained values:
* Vout=1.1V
* Vp=0.4V
* Id1=Id2=0.25mA

## TRANSIENT ANALYSIS:
* Follow the same procedure as in the circuit 1 and observe the gain.

  <img width="1470" alt="Screenshot 2025-03-06 at 7 59 10 PM" src="https://github.com/user-attachments/assets/f4de0434-adfb-4121-add6-fe6d508b712b" />

 * Gain, Av=(1.10-1.33)/50m = -4.6
 * 20logAv=13.25dB

## AC ANALYSIS:

<img width="1470" alt="Screenshot 2025-03-06 at 7 33 43 PM" src="https://github.com/user-attachments/assets/0afa3ad3-c2f6-4079-a145-324085baf18a" />

* 3dB bandwidth = 13.5-3 = 10.5 = 4.10Ghz.
* It is observed that the bandwidth has been increased when compared to the circuit 1.

# CIRCUIT 3
### Replacing the current source with a NMOS:  
<img width="1470" alt="Screenshot 2025-03-06 at 7 54 11 PM" src="https://github.com/user-attachments/assets/4b443172-545c-4653-98db-1e98675ef970" />  

## DC OPERATING POINT
* First, we need to calculate value of Vb of 3rd MOSFET.
* It should be in the saturation region.
* Condition for saturation region:
  Vds>=Vov
  Vds>=Vgs-Vth
  Vd-Vs>=Vg-Vs-Vth
  0.4-0>=Vg-o-0.497
  Vg<=0.897V
* According to the condition, Vb should be less than or equal to 0.897V, thereby take Vb as 0.7V.
* length and width obtained to get the values as per the designed specifications are 180nm and 14.1579um respectively.
  <br>
  <br>
  <img width="390" alt="Screenshot 2025-03-04 at 10 27 06 PM" src="https://github.com/user-attachments/assets/f216673f-7797-4da3-a7ae-d96f31bcf92d" />
  <br>
  <br>
* Obtained values are:
  Idss=0.5mA
  Id1=Id2=0.25mA
  Vp=0.4V
  Vout=1.1V
  <br>
  <br>

## TRANSIENT ANALYSIS:

  <img width="1470" alt="Screenshot 2025-03-06 at 7 59 10 PM" src="https://github.com/user-attachments/assets/f4de0434-adfb-4121-add6-fe6d508b712b" />  
  <br>
  <br>
  * Gain, Av=(1.10-1.33)/50m=-4.6
  * 20logAv=13.25dB

## AC ANALYSIS: 

<img width="1470" alt="Screenshot 2025-03-06 at 7 51 43 PM" src="https://github.com/user-attachments/assets/3abe299b-26d5-4506-8abb-0ce2c0267dd3" />  

Bandwidth = 13.8-3dB=10.8dB=4.37Ghz.
Bandwidth has been increased from the previous two circuits.  

# RESULTS:  
 
 | PARAMETER  | CIRCUIT 1 |  CIRCUIT 2  |  CIRCUIT 3  |  
| ------------- | ------------- | ------------- | ------------- |
| Id  | 0.5mA  |  0.5mA  |  0.5mA|
| Id1,Id2  | 0.25mA  |  0.25mA  |  0.25mA  |
|  Vout  |  1.1V  |  1.1V  |  1.1V  |  
|  Vp  |  0.4V  |  0.4V  |  0.4V  |
|  Gain  |  -5.4  |  -4.6  |  -4.6  |
|  Bandwidth  |  3.66Ghz  |  4.10Ghz  |  4.37Ghz  |  

# INFERENCE:

### **Gain:**
  <br>
  <br>
  **Expected:** Circuit 2 should have the highest gain since an ideal current source has infinite resistance (no source degeneration) and circuit 3 as lowest gain.
  <br>
  <br>
  **Observed:** The gain has decreased in circuit 2 and 3.
  <br>
  Possible reasons for the decreament of gain in circuit 2:
  
  The current source may not be completely ideal, causing source degeneration.

### **Bandwidth:**

  **Expected:** A differential amplifier with a current source instead of Rss should have a higher bandwidth due to       reduced source degeneration.  
  Circuit 3 should have slightly lower bandwidth than Circuit 2 because the NMOS current source has finite output         resistance.  
  <br>
  **Observed:** Bandwidth increases from Circuit 1 → Circuit 2 → Circuit 3, which aligns with expectations.
  Circuit 3 (NMOS current source) has the highest bandwidth despite its finite output resistance.



  







  



  
  
  
  




