Wavelet Tranform
--
Use various class of functions well localized in time and frequency (time-frequency resolution). To achieve this, it is used:
  - Translation (shifting) by a factor b
  The wavelet is aligned with the desired feature present in the signal.
  - Scaling by a factor a -> inversely proportional to the frequency of the wavelet.
  Compress the wavelet, allows me to capture the abrupt changes (high-frequencies) and viceversa.

Each compressed wavelet is compared with all the signal when translation is executed (crosscorrelation). Therefore, resultant coefficients are function of shifting (time) and scale (frequency) values.

Continous (CWT):

Discrete (DWT):

What is a wavelet?
-
A wavelet is a fast oscillation wave with a zero-mean, existing for a finite duration.

Why wavelets?
-

Types of families
-
- Daubechies
- Symlet
- Coifflet
- Meyer
- Mexican Hat


Wavelet Implementation
-
Bank of filters are used (Mallat,Meyer), subband coding, downsampling and oversampling via the filters. The filters have to fullfil various conditions:
- Perfect reconstruction
- x
- x

The filters are know as analysis H0,H1 and synthesis G0,G1 filters. The analysis filters are used in the decomposition while
the synthesis filters are used in the reconstruction of the signal.

- A: Approximation coefficients (LP filter)
- D: Detailed coefficients (HP filter)

Types of configurations
- Logaritmic Tree:
- Packet Tree:

How to choose the right wavelet?
-


Filtering
-
Mainly, thresholding method are used for filtering the coefficients:
- D
- J

By the way of threating the coefficients under the threshold, they classify as:
- Soft
- Hard


