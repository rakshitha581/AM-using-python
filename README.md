# AM-using-python
AIM:
To generate and detect the amplitude modulation and demodulation using python code and to calculate modulation index of AM.

EQUIPMENTS REQUIRED
• Computer with i3 Processor
• colab
THEORY:
Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a 
circuit called a modulator. Need for modulation is as follows: • Avoid mixing of signals • Reduction in antenna height • long distance communication • Multiplexing 
• Improve the quality of reception • Ease of radiation. Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal 
Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.
1.Under modulation : m<1, Em < Ec
2.Critical modulation: m-1, Em = Ec
3.Over modulation: m>1, Em > Ec
**ALGORITHM:
1.Define Parameters First, define the parameters for your signals: • Carrier frequency (fc) • Modulating signal frequency (fm) • Sampling frequency (Fs) • Duration of the signal (T)
2.Create a time vector based on the sampling frequency and duration.
3.Create Modulating Signal Define the modulating signal (message signal).
4.Create Carrier Signal Define the carrier signal.
5.Perform Amplitude Modulation Multiply the carrier signal by the modulating signal plus 1 (to ensure the modulation depth).
6.Plot the Signals Visualize the modulating, carrier, and modulated signals.
7.Demodulate the AM Signal To demodulate, you can use envelope detection. One way is to rectify the signal and then apply a low-pass filter.
8.Plot the Demodulated Signal Visualize the demodulated signal.
9.Compare Signals Compare the original modulating signal with the demodulated signal. PROCEDURE • Refer Algorithms and write code for the experiment.
• Open colab in System • Type your code in New Editor • Save the file • Execute the code • If any Error, correct it in code and execute again • Verify the generated waveform using Tabulation and Model Waveform
**PROGRAM
```
import numpy as np
import matplotlib.pyplot as plt
Am = 3.1
Ac = 6.2
fm = 204
fc = 2040
fs = 204400
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
s = (Ac + m) * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()
```
OUTPUT WAVEFORM:
![WhatsApp Image 2025-10-22 at 14 09 51_a0b2ac12](https://github.com/user-attachments/assets/4b7ad913-b9a8-471b-af47-c09cb9c97c86)
TABULATION:
![WhatsApp Image 2025-10-22 at 14 12 53_7db106b2](https://github.com/user-attachments/assets/bef86a2c-6e88-4ccb-a7b9-4f90dfb28455)
CALCULATION:
ma (Theory) = am/ac =0.5
ma(Practical) = (Emax-Emin)/(Emax+Emin) =0.5
![WhatsApp Image 2025-10-22 at 14 14 50_45a4f21c](https://github.com/user-attachments/assets/63f897ba-731d-4e02-b85b-0c4ed98de97d)
MODEL GRAPH:
![WhatsApp Image 2025-10-22 at 14 15 31_483ae234](https://github.com/user-attachments/assets/d82ad359-7059-40b7-a056-ffed08aa0199)
RESULT:
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.


