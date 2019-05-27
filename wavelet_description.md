Wavelet Tranform
--
Use various class of functions well localized in time and frequency (time-frequency resolution). To achieve this, it is used:
  - Translation (shifting) by a factor b
  The wavelet is aligned with the desired feature present in the signal.
  - Scaling by a factor a -> inversely proportional to the frequency of the wavelet.
  Compress the wavelet, allows me to capture the abrupt changes (high-frequencies) and viceversa.

Each compressed wavelet is compared with all the signal when translation is executed (crosscorrelation). Therefore, resultant coefficients are function of shifting (time) and scale (frequency) values.

Continous (CWT)
Intermediate scales in the range of ![Eq. 1](https://latex.codecogs.com/gif.latex?%5B2%5E%7Bn%7D%2C2%5E%7Bn&plus;1%7D%5D) with n integer can be used (number of scales per octave).
- Applications: Time-frequency analysis, and filtering of time localiced of frequency components.

Discrete (DWT)
Scaling ![](https://latex.codecogs.com/gif.latex?2%5E%7Bj%7D) and shifting ![](https://latex.codecogs.com/gif.latex?2%5E%7Bj%7Dm) 
with j and m integers is used (diadic) eliminating redundacy in coefficients.
- Applications: Denoising and compressing.

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
The bank of filters are used (Mallat,Meyer), subband coding, downsampling and oversampling via the filters. The filters have to fullfil various conditions:
- Invertible
- Alliasing cancellation 
- Perfect reconstruction (lossless)
- Subband signals have to be orthogonal

According to these when the ![](https://latex.codecogs.com/gif.latex?H_%7B0%7D%28z%29) filter has been chosen, all the other filters are prescribed.

The filters are know as analysis ![](https://latex.codecogs.com/gif.latex?H_%7B0%7D%28z%29),![](https://latex.codecogs.com/gif.latex?H_%7B1%7D%28z%29) and synthesis G0,G1 filters. The HP filters are analogous to the application of the wavelet, whilst the LP filter is analogous to the application of the scaling function. The analysis filters are used in the decomposition while
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


