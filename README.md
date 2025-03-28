## Ideal-Sampling

## Aim: 

To perform ideal (impulse) sampling of a continuous-time sinusoidal signal, visualize the sampled signal, and reconstruct it using Python.

## Tools Required:

 Python Software -> Numpy Library

-> Matplotlib Library

-> Scipy Library (for signal processing)

## Program :
~~~
mpy as np

import matplotlib.pyplot as plt

from scipy.signal import resample

fs = 100

t = np.arange(0, 1, 1/fs)

f = 5

signal = np.sin(2 * np.pi * f * t)

plt.figure(figsize=(10, 4))

plt.plot(t, signal, label='Continuous Signal')

plt.title('Continuous Signal (fs = 100 Hz)')

plt.xlabel('Time [s]')

plt.ylabel('Amplitude')

plt.grid(True)

plt.legend()

plt.show()

t_sampled = np.arange(0, 1, 1/fs)

signal_sampled = np.sin(2 * np.pi * f * t_sampled)

plt.figure(figsize=(10, 4))

plt.plot(t, signal, label='Continuous Signal', alpha=0.7)

plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')

plt.title('Sampling of Continuous Signal (fs = 100 Hz)')

plt.xlabel('Time [s]')

plt.ylabel('Amplitude')

plt.grid(True)

plt.legend()

plt.show()

reconstructed_signal = resample(signal_sampled, len(t))

plt.figure(figsize=(10, 4))

plt.plot(t, signal, label='Continuous Signal', alpha=0.7)

plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')

plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')

plt.xlabel('Time [s]')

plt.ylabel('Amplitude')

plt.grid(True)

plt.legend()

plt.show()
~~~

## Output Waveform :

![WhatsApp Image 2025-03-27 at 19 49 09_144a3fdf](https://github.com/user-attachments/assets/8e868896-af98-4911-8d6e-d7339e6c7030)

![WhatsApp Image 2025-03-27 at 19 49 25_04b096c1](https://github.com/user-attachments/assets/fe1b685a-8193-413f-b9b8-18f3abebc61b)

![WhatsApp Image 2025-03-27 at 19 50 16_12dcf67e](https://github.com/user-attachments/assets/1c8dab17-e32b-4c4b-966a-d70440c9dbb4)

## RESULT:

The Construction or Re-Construction of impulse or ideal sampling using python are verified
