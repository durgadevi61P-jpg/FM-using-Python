# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt

Am = 3.3
fm = 224
Ac = 6.6
fc = 2240
fs = 224000

t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
efm = Ac * np.cos((2 * np.pi * fc * t) + (2.4 * np.sin(2 * np.pi * fm * t)))
plt.subplot(3, 1, 3)
plt.plot(t, efm)
`````

Output Waveform
![WhatsApp Image 2025-10-08 at 20 54 45_77abadd1](https://github.com/user-attachments/assets/44ab0865-c10c-490c-8d60-ebc98bcd00bf)


Tabular Column
![WhatsApp Image 2025-10-07 at 19 03 17_7142951c](https://github.com/user-attachments/assets/82469431-b3bc-4a5d-876c-77044a1e4178)


Calculation

![WhatsApp Image 2025-10-08 at 21 05 24_58ebe9bf](https://github.com/user-attachments/assets/3faaabaf-ae24-4bc8-a830-6178f9716a29)


Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
