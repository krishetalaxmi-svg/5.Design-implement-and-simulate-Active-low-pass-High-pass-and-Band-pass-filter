# 5.Design-implement-and-simulate-Active-low-pass-High-pass-and-Band-pass-filter

**AIM:**
To design and obtain the frequency response of i)	First order Low Pass Filter (LPF) ii)	First order High Pass Filter (HPF) iii)	Band pass filter and also simulate it using LT-Spice.

**APPARATUS  and SOFTWARE REQUIRED:**
S.No	Name of the Apparatus	Range
1.	Function Generator	3 MHz
2.	DSO	30 MHz
3.	Dual RPS	(0 – 30) V
4.	Op-Amp	µA741
5.	Bread Board	
6.	Resistors	1.6K,10K,5.86K,38.8K,7.9K
7.	Connecting wires and probes	As required
8.  LT SPICE software

**THEORY:**

**LOW PASS FILTER**

A LPF allows frequencies from 0 to higher cut of frequency, fH. At fH the gain is 0.707 Amax, and after fH gain decreases at a constant rate with an increase in frequency. The gain decreases 20dB each time the frequency is increased by 10. Hence the rate at which the gain rolls off after fH is 20dB/decade or 6 dB/ octave, where octave signifies a two fold increase in frequency. The frequency f=fH is called the cut off frequency because the gain of the filter at this frequency is down by 3 dB from 0 Hz. Other equivalent terms for cut-off frequency are -3dB frequency, break frequency, or corner frequency.
 
**HIGH PASS FILTER**

The frequency at which the magnitude of the gain is 0.707 times the maximum value of gain is called low cut off frequency. Obviously, all frequencies higher than fL are pass band frequencies with the highest frequency determined by the closed –loop band width all of the op-amp.

**BAND PASS FILTER**

A band pass filter has a pass band between two cutoff frequencies fH and fL such that fH > fL. Any input frequency outside this pass band is attenuated. There are two types of band-pass filters. Wide band pass and Narrow band pass filters. We can define a filter as wide band pass if its quality factor Q <10. If Q>10, then we call the filter a narrow band pass filter. A wide band pass filter can be formed by simply cascading high-pass and low-pass sections. The order of band pass filter depends on the order of high pass and low pass sections.

**DESIGN:LPF & HPF**

Given: fH = 1 KHz = 1/ (2πRC)
Let C = 0.1 µF, R = 1.6 KΩ
For n = 2, α (damping factor) = 1.414, Passband gain = Ao = 3 - α =3 – 1.414 = 1.586.
Transfer function of second order butterworth LPF as:
H(s) = 1.586/S2 + 1.414 s + 1
Now	Ao = 1 + (Rf / R1) = 1.586 = 1 + 0.586
Let Ri = 10 KΩ, then Rf = 5.86 KΩ

**DESIGN: BAND PASS FILTER**

Design a BPF to pass a band of 400Hz to 2KHz with a pass band gain of 4.
1.	Select the highest cut-off frequency of LPF as fH = 10 KHz and the lowest cut-off frequency of HPF as fL = 1 KHz.
2.	Design the HPF first by taking fL = 1KHz. Assume the value of C < 1μf.
3.	 Let C = 0.1μf.
4.	Calculate R from the expression. Given: fH = 2KHz = 1/ (2πR1C1)
5.	Let C1 = 0.1 µF, R1 = 7.9 KΩ
Given: fL = 400Hz = 1/ (2πR2C2)
Let C2 = 0.1 µF, R2 = 39.8 KΩ
Pass band Gain=4
Now		Ao = 1 + (Rf / R1) 2-1=(Rf / Ri)
Ri = Rf
Let Ri = Rf = 10 KΩ


**PROCEDURE - (LPF & HPF):**

1.	Connect the circuit as shown in the circuit diagram.
2.	Select the corresponding cut-off frequency (higher or lower) and determine the value of C&R. select the value of R1 & Rf depending on desired passband gain Af..
3.	Apply a constant voltage input sinusoidal signal to the non-inverting terminal of op-amp.
4.	Tabulate the output voltage Vo with respect to different values of input frequency.
5.	Calculate passband gain and plot the graph of frequency versus voltage gain & check the graph to get approximately the same characteristic as shown in the model graph.
 
**BAND PASS FILTER**

1.	Select the lower and higher cut-off frequency and calculate the value of R & C for the given frequencies.
2.	Design for LPF & HPF separately and then combine the circuit by first placing the HPF followed by a LPF (i.e) HPF in series with LPF.
3.	Connect the circuit as shown in the circuit diagram.
4.	Apply a constant voltage input sinusoidal signal to the non-inverting terminal of op-amp.
5.	Tabulate the output voltage Vo with respect to different values of input frequency.
6.	Calculate passband gain and plot the graph of frequency versus voltage gain & check the graph to get approximately the same characteristic as shown in the model graph.
 

**LPF:**
  **CIRCUIT DIAGRAM**

<img width="430" height="230" alt="image" src="https://github.com/user-attachments/assets/83e8a5b0-30ef-439c-9bdf-143702c6cb94" />


  **MODEL GRAPH:**

<img width="463" height="290" alt="image" src="https://github.com/user-attachments/assets/d04e0417-9f9f-4c88-bf81-9810c2be0230" />


  **TABULATION:**
 
<img width="527" height="230" alt="image" src="https://github.com/user-attachments/assets/dfc90c0f-df4f-4ab3-b007-2b84ab676254" />



**HPF:**
  **CIRCUIT DIAGRAM**

<img width="900" height="1600" alt="image" src="https://github.com/user-attachments/assets/39f1978d-c09b-4ee0-a62e-3cc995b59b3b" />


  **MODEL GRAPH:**

<img width="567" height="262" alt="image" src="https://github.com/user-attachments/assets/43dc1201-94cd-49ca-b9c4-23304835e1b4" />


  **TABULATION:**

<img width="756" height="562" alt="image" src="https://github.com/user-attachments/assets/739a9ab7-32ba-4204-a3df-fd6926c16733" />


  **BPF:**
  **CIRCUIT DIAGRAM**

<img width="581" height="217" alt="image" src="https://github.com/user-attachments/assets/8f50e941-27c2-4a9d-9b00-67b55ec9b06e" />


  **MODEL GRAPH:**

<img width="577" height="300" alt="image" src="https://github.com/user-attachments/assets/12b19f24-dd4d-4f65-a428-461a2a7da14b" />


  **TABULATION:**

<img width="656" height="723" alt="image" src="https://github.com/user-attachments/assets/6f984378-2fd6-4610-b592-171da15874a8" />

<img width="706" height="797" alt="image" src="https://github.com/user-attachments/assets/8a50cc76-8e8e-47ec-b6f8-53de0d3be42b" />

<img width="741" height="833" alt="image" src="https://github.com/user-attachments/assets/e219992e-35c9-46e2-a977-2e0c3af7dc23" />



**LT-SPICE Tool:PROCEDURE:**
•	Double click on LT-Spice icon.
•	New schematic window open.
•	Pick and paste the required component from the library and draw the circuit diagram .
•	Complete the connection.
•	Save the file by giving file name.
•	Click on the run option ->click advanced open ->select Ac analysis->enter the amplitude time delay stop time value.
•	Click on the run option ->simulation window opens->place the probe ->output graph is obtained.
 
  **LT SPICE**
  **CIRCUIT and Waveform**

  <img width="512" height="626" alt="image" src="https://github.com/user-attachments/assets/ea164736-a472-40cb-a342-dd67be5a166d" />

<img width="517" height="591" alt="image" src="https://github.com/user-attachments/assets/acfcf48d-c340-4b19-95b2-0e552083584f" />

<img width="900" height="1600" alt="image" src="https://github.com/user-attachments/assets/120f1b0e-b863-4768-ad11-a2badef9b6d2" />


**RESULT:**
Thus the Active Low pass, High pass and Band Pass Filters are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.
 
