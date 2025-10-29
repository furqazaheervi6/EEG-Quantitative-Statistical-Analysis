# EEG-Quantitative-Statistical-Analysis
Statistical Analysis of EEG Signals, providing a quantitative analysis to determine how consistent and accurate neural signals are collected from Mark IV Ultracortex Headset

This block diagram outlines the computational sequence for EEG spectral and coherence analysis:

1. **Data Collection:** EEG signals are sampled at 128 Hz for 1 second epochs.
2. **Raw Spectra Calculation:** Compute Fourier transforms (X_k, Y_k) for each channel.
3. **Power Spectral Density (PSD):** Derive (G_{X_k}) and (G_{Y_k}) from squared magnitudes of spectra.
4. **Cross Spectra:** Compute (G_{XY_k}) representing frequency-domain covariance between signals.
5. **Data Smoothing:** Apply averaging or windowing to reduce noise, yielding (\hat{G}*{X_k}, \hat{G}*{Y_k}, \hat{G}_{XY_k}).
6. **Coherence:** Calculate normalized coherence (Y_K^{2XY}) = (|\hat{G}*{XY_k}|^2 / (\hat{G}*{X_k}\hat{G}_{Y_k})).
7. **Phase Shift:** Compute phase difference (\delta(f)) between signals across frequencies.
