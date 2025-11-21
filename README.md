## Amplitude-Modulation-and-Demodulation-using-NumPy-and-Matplotlib

### Aim: 
To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 
### Apparatus Required: 
Software: Python with NumPy and Matplotlib libraries 
Hardware: Personal Computer 
### Theory: 
Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting 
information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of 
the message signal. The general form of an AM signal is: 
### Algorithm:
1. Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency. 
2. Generate Time Axis: Create a time vector for the signal duration. 
3. Generate Message Signal: Define the message signal as a cosine wave. 
4. Generate Carrier Signal: Define the carrier signal as a cosine wave. 
5. Modulate Signal: Apply the AM formula to obtain the modulated signal. 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.
### Program :
```
import numpy as np
import matplotlib.pyplot as plt
Am = 6
fm = 474
Ac = 12
fc = 4740
fs = 47400
t = np.arange(0, 3/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
c = Ac * np.cos(2 * np.pi * fc * t)
s = (Ac + m) * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()
```
### Tabulation :
<img width="801" height="644" alt="image" src="https://github.com/user-attachments/assets/8689ac0c-1d64-48de-85ab-1d3eb91b9e31" />

### Output:
<img width="630" height="469" alt="image" src="https://github.com/user-attachments/assets/5a5d7b46-8c19-4e28-8de1-f1856e414ff6" />

### Result:
The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. 
Thus, AM is implemented using numPy and Matplotlib.
