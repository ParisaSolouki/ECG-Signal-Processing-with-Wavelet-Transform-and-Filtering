# ECG Signal Processing with Wavelet Transform and Filtering
This repository provides an implementation of preprocessing, filtering, wavelet transformation, and denoising of ECG (Electrocardiogram) signals. The code utilizes libraries like wfdb, pandas, numpy, scipy, pywt, and matplotlib for signal processing and visualization.

## ECG Signal Processing Steps
### 1. Load the ECG Signal
- Load the .mat ECG file and flatten the signal to a 1D array for processing.

### 2. Plot Raw ECG Signal
- Plot the original ECG signal to observe any noise or baseline drift that may require correction.

### 3. Butterworth High-Pass Filter
- Apply a high-pass Butterworth filter to remove baseline drift from the signal, with a 0.5 Hz cutoff frequency.
- Plot the filtered ECG signal for comparison.

### 4. Wavelet Transform Decomposition and Reconstruction
- Use the pywt.wavedec function to decompose the ECG signal into wavelet coefficients using the Daubechies wavelet (db6), up to level 4.
- Visualize the decomposition of the signal into approximation and detail coefficients.

### 5. Denoising with Thresholding
- Perform denoising by applying a threshold to the detail coefficients to remove high-frequency noise.
- Use soft thresholding based on a threshold value derived from the median absolute deviation (MAD).

### 6. Signal Reconstruction
- Reconstruct the signal from the modified wavelet coefficients.
- Compare the filtered and reconstructed signals by plotting them together.
