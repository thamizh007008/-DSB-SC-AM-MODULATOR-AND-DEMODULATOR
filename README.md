# DSB-SC-AM-MODULATOR-AND-DEMODULATOR
# AIM:
To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

# EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

# Algorithm:

1.	Define Parameters:
   
    •	Fs: Sampling frequency.
  
    •	T: Duration of the signal.
  
    •	Fc: Carrier frequency.
  
    •	Fm: Frequency of the message signal.
  
    •	Amplitude: Maximum amplitude of the message signal.
  	
2.	Generate Signals:

    •	Message Signal: A sinusoidal signal that will be modulated.

  	•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
  	
3.	DSBSC Modulation:
   
    •	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
  	
4.	DSBSC Demodulation:
   
    •	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).

  	•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
  	
5.	Visualization:
   
    Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
  	
# PROCEDURE

•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file
 
•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated waveform using Tabulation and Model Waveform

# PROGRAM:
~~~
Am=11.95;
fm=1840;
fs=184000;
t=0:1/fs:2/fm;
Ac=20.315;
fc=18400;
em=Am*cos(2*3.14*fm*t);
subplot(3,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(3,1,2);
plot(t,ec);
eAM1=(Ac+em).*cos(2*3.14*fc*t); 
eAM2=(Ac-em).*cos(2*3.14*fc*t); 
eDSBSC=eAM1-eAM2;
subplot(3,1,3);
plot(t,eDSBSC);
~~~
# MODEL GRAPH:

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/5138c677-2394-473d-af8a-63d597451e49" />

# OUTPUT WAVEFORM:

<img width="1600" height="832" alt="WhatsApp Image 2026-06-06 at 8 12 52 AM" src="https://github.com/user-attachments/assets/eb8c721e-d131-47e7-a8f4-684e6004fa7a" />

# TABULATION:
<img width="721" height="1280" alt="WhatsApp Image 2026-06-06 at 8 08 15 AM" src="https://github.com/user-attachments/assets/cca54fb6-609e-49e7-b0ba-ca5c7feb8da1" />


# Result:
  Thus the DSB-SC-AM Modulation and Demodulation is generated.
