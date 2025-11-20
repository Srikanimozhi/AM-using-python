# AM-using-python
EXPT.NO.7	Amplitude Modulation and Demodulation using NumPy and Matplotlib
Aim

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. Apparatus Required
Software: Python with NumPy and Matplotlib libraries

Hardware: Personal Computer

Theory

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of the message signal. The general form of an AM signal is:


Algorithm

1.	Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Generate Carrier Signal: Define the carrier signal as a cosine wave.
5.	Modulate Signal: Apply the AM formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

program:
```asm
import numpy as np
import matplotlib.pyplot as plt
Am = 4.8
Ac = 9.6
fm = 577
fc = 5770
fs = 57700
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
Output:

<img width="627" height="469" alt="image" src="https://github.com/user-attachments/assets/a15f364a-3c48-4347-880f-f37499691e47" />

calculation:

![WhatsApp Image 2025-10-23 at 21 19 55_0ae202c5](https://github.com/user-attachments/assets/aaad8266-d02c-4397-8182-ba251e73ec02)


Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. Thus AM is implemented using numPy and Matplotlib.
