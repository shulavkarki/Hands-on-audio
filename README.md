# Audio

### Sampling and Sampling Rate

![https://huggingface.co/datasets/huggingface-course/audio-course-images/resolve/main/Signal_Sampling.png](https://huggingface.co/datasets/huggingface-course/audio-course-images/resolve/main/Signal_Sampling.png)

**Sampling** is the process of measuring the value of a continuous signal at fixed time steps.

**************************************Sampling Rate************************************** is the number of samples taken in one second and is measured in hertz(Hz).

> All audio examples in dataset must have sample sampling rate. Also, sampling rate of custom audio data should match the sampling rate of data the model was pre-trained on.
> 

### Amplitude and Bit Depth

**************Amplitude************** describes the sound pressure level at any given instant and measured in decibels(dB). We perceive the amplitude as loudness. 

In Digital audio, each audio samples records the amplitude of the audio wave at a point in time.

********************Bit Depth******************** determines with how much precision this amplitude value can be described. Refers to the number of bits used to represent each sample's amplitude. The higher the bit depth, the more faithfully the digital representation approximates the original continuous sound wave. Most common audio bit depths are 16-bit and 24-bit.

For example, 16 bit depth audio will have 2^16 = 65,536 steps, to convert from continuous to discrete. 

> However, for digital audio signals, 0 dB is the loudest possible amplitude, while all other amplitudes are negative. As a quick rule of thumb: every -6 dB is a halving of the amplitude, and anything below -60 dB is generally inaudible unless you really crank up the volume.
> 

### Audio as Waveform

![https://huggingface.co/datasets/huggingface-course/audio-course-images/resolve/main/waveform_plot.png](https://huggingface.co/datasets/huggingface-course/audio-course-images/resolve/main/waveform_plot.png)

### ****The frequency spectrum****

### Spectrogram

[Discrete Fourier Transform](docs/Discrete%20Fourier%20Transform.md)

[Mel Spectrogram](docs/Mel%20Spectrogram.md)