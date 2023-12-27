# Discrete Fourier Transform

![Untitled](Discrete%20Fourier%20Transform/Untitled.png)

Fourier transform basically takes area of the rectangle to approximate the overall area below the signal.

Transfrom signal from time domain to frequency domain. 

![Untitled](Discrete%20Fourier%20Transform/Untitled%201.png)

Sampling rate/2 = Nyquist Frequency , threshold above which it is not able to reconstructing digital signal to original analog signal

### Short-Time Fourier Transform

Extension of DFT that allows for analyzing how the frequency content of a signal canges over time. 

It divides the signal into short overlapping windws, and the applies DFT to each window. Useful for analyzing signals that have time-varying frequency such as music or speech.

![Untitled](Discrete%20Fourier%20Transform/Untitled%202.png)

![Screenshot from 2023-11-30 13-38-16.png](Discrete%20Fourier%20Transform/Screenshot_from_2023-11-30_13-38-16.png)

## Ouputs

### DFT

- Spectral vector (#frequency bins)
- N complex Fourier coefficients

### STFT

- Spectral matrix (# frequency bins, # frames)
- Complex Fourier Coefficents

### Equations

$$
frequency bins = {{framesize}/{2}} +1
$$

$$
frames = {(samples-framesize)}/hopsize + 1
$$

Example:

Signal = 10k samples

Frame size = 1000

hop size = 500 

frequency bins = 1000/2 + 1 = 501 (0, sampling_rate / 2)

frames = (10000-1000)/500 + 1 = 19

STFT = (501, 19)