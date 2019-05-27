Wavelet Tranform

Use various class of functions well localized in time and frequency (time-frequency resolution). To do this, it is used:
  - Translation (shifting) by a factor b
  The wavelet is aligned with the desired feature present in the signal.
  - Scaling by a factor a -> inversely proportional to the frequency of the wavelet.
  Compress the wavelet, allows me to capture the abrupt changes (high-frequencies) and viceversa.

Each compressed wavelet is compared with all the signal when the translation is executed. So therefore, the resultant coefficients are
a function of shifting (time) and scale (frequency) values.

Continous (CWT):


Discrete (DWT):



What is a wavelet?
A wavelet is a fast oscillation wave with a zero-mean, existing for a finite duration.

Why wavelets?


Types of families


Wavelet Implementation

How to choose the right wavelet?
