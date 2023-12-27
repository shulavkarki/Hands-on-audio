# Mel Spectrogram

why?

- Human auditory system does not percieve all frequencies equally.

### Mel Scale

**mel** abbrevation for `**melody**`

- Logarithmic Scale
- Equal distances on the scale have same “perceptual distance”
- 1000Hz = 1000 Mel
    
    ![Screenshot from 2023-12-01 13-43-03.png](Mel%20Spectrogram/Screenshot_from_2023-12-01_13-43-03.png)
    
    ### Relations frequncy and mel frequency
    
    ![Screenshot from 2023-12-01 13-44-38.png](Mel%20Spectrogram/Screenshot_from_2023-12-01_13-44-38.png)
    
    ### Extract Mel Spectrogram
    
    1. Extract STFT
    2. Convert amplitude to dBs
    3. Convert frequencies to Mel scale
        1. Choose number of mel bands
        2. Construct mel filter banks
        3. Apply mel filter banks to spectrogram

### Number of mel bands

- It depends on the problem.
- Hyper-parameter
- Eg: 40, 60, 90, 128

### Construct Mel filter banks

1. Convert lowest/highest frequency to Mel
    
    ![Screenshot from 2023-12-01 13-51-27.png](Mel%20Spectrogram/Screenshot_from_2023-12-01_13-51-27.png)
    
2. Create # bands equally spaced points
    
    ![Screenshot from 2023-12-01 13-52-45.png](Mel%20Spectrogram/Screenshot_from_2023-12-01_13-52-45.png)
    
3. Convert points back to Hertz
    
    ![Screenshot from 2023-12-01 13-53-07.png](Mel%20Spectrogram/Screenshot_from_2023-12-01_13-53-07.png)
    
4. Round to nearest frequency bin
5. Create triangular filters

### Apply Mel filter banks to spectrogram

 **mel filter banks(M) = (# bands, framesize/2 + 1)

Spectrogram(Y) = ( framesize/2 + 1, #frames)

![Screenshot from 2023-12-01 14-09-34.png](Mel%20Spectrogram/Screenshot_from_2023-12-01_14-09-34.png)

(# bands, # frames)

frequency → Mel bands

![Screenshot from 2023-12-01 14-11-10.png](Mel%20Spectrogram/Screenshot_from_2023-12-01_14-11-10.png)

**X-axis** = Time

**Y-axis** = Frequency

But, in mel spectrogram, frequency bins are not linear bins that we used in spectrogram but rather a mel bands which are perceptually relevant.

**Color** = represents how presence a certain mel bands is at certain point at time

### Applications

- Audio Classification
- Audion mood recognition
- Music Genre Classification
- Music instrument classification
-