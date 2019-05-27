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

Given that equations and the LP filter, the other filters can be obtained:
- Alternating flip algorithm
![](https://latex.codecogs.com/gif.latex?h_%7B1%7D%5Bn%5D%3D%5Bh_%7B0%7D%28N%29%2C-h_%7B0%7D%28N-1%29%2Ch_%7B0%7D%28N-2%29%2C-h_%7B0%7D%28N-3%29...%5D)
- Order flip algorithm

![](https://latex.codecogs.com/gif.latex?g_%7B0%7D%5Bn%5D%3D%5Bh_%7B0%7D%28N%29%2Ch_%7B0%7D%28N-1%29%2Ch_%7B0%7D%28N-2%29%2C...%5D)

![](https://latex.codecogs.com/gif.latex?g_%7B1%7D%5Bn%5D%3D%5Bh_%7B1%7D%28N%29%2Ch_%7B1%7D%28N-1%29%2Ch_%7B1%7D%28N-2%29%2C...%5D)



According to these when the ![](https://latex.codecogs.com/gif.latex?H_%7B0%7D%28z%29) filter has been chosen, all the other filters are prescribed.

The filters are know as analysis ![](https://latex.codecogs.com/gif.latex?H_%7B0%7D%28z%29),![](https://latex.codecogs.com/gif.latex?H_%7B1%7D%28z%29) and synthesis ![](https://latex.codecogs.com/gif.latex?G_%7B0%7D%28z%29),![](https://latex.codecogs.com/gif.latex?G_%7B1%7D%28z%29) filters. The analysis filters are used in the decomposition while the synthesis filters are used in the reconstruction of the signal. The HP filters are analogous to the application of the wavelet, whilst the LP filter is analogous to the application of the scaling function:

- A: Approximation coefficients of the signal (LP filter out)
- D: Detailed coefficients of the signal (HP filter out)

Types of configurations
- Logaritmic Tree:
- Packet Tree:

How to choose the right wavelet?
-


Filtering
-
The filtering is applied to the detailed coefficients (HP outputs). Mainly, thresholding methods are used for filtering the coefficients:
- Universal
- Minmax
- SureShrink
- Heuristic

By the way of threating the coefficients under the threshold. In both cases the coefficients less than the threshold are set to 0. They differenciate in how the coefficients greater in magnitude are treated:
- Soft thresholding: Coefficients are scaled substracting the threshold value.
- Hard thresholding: Coefficients remain unchaiged.


