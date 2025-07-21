# DIGITAL-FILTER-DESIGN

COMPANY: CODTECH IT SOLUTIONS

NAME: ADITI ATTAL

INTERN ID: CITS0D695

DOMAIN: VLSI

DURATION: 6 WEEKS

MENTOR: NEELA SANTOSH

DISCRIPTION:

1. Task Objective and Tool Used
The objective of this task was to design and simulate a digital Finite Impulse Response (FIR) filter using MATLAB, one of the most widely used tools for digital signal processing and filter design. FIR filters are non-recursive filters with finite-duration impulse responses, known for their inherent stability and linear phase characteristics, making them ideal for applications requiring phase preservation, such as audio and biomedical signal processing.

MATLAB was chosen for this task due to its robust DSP toolbox, built-in functions like fir1, freqz, filter, and fvtool, and its ability to visualize filter behavior both in the time and frequency domains. The simulation leverages MATLAB's window method for FIR design using the fir1 function with a Hamming window, which provides a good trade-off between main-lobe width and side-lobe attenuation.

2. Filter Design Parameters and Implementation
The FIR filter was configured as a low-pass filter with the following specifications:

Sampling frequency (Fs): 1000 Hz
Cutoff frequency (Fc): 150 Hz
Filter order (N): 50 (resulting in 51 taps)
Window type: Hamming

The cutoff frequency was normalized to the Nyquist frequency (Fs/2), and the filter coefficients were calculated using MATLAB's fir1 function. A Hamming window was applied to reduce ripples in the passband and improve stopband attenuation.
Once the filter coefficients were obtained, they were applied to a synthetic input signal using the filter() function. The input signal was designed as a 100 Hz sine wave embedded in additive white Gaussian noise, mimicking a real-world scenario of a noisy measurement requiring filtering.

3. Simulation Results and Plots
The MATLAB code generated several key visualizations to analyze filter performance:

Impulse Response (FIR Coefficients): Displayed using a stem plot, this showed the symmetric nature of the FIR filter taps due to the linear phase design. The response lasted 51 samples, indicating the filter length.

Input vs. Output Signal (Time-Domain): The input signal displayed strong high-frequency noise. After filtering, the output showed a clear sinusoidal waveform, indicating successful noise removal while preserving the desired 100 Hz component.

Frequency Response (freqz): The magnitude and phase responses of the filter were plotted. The magnitude plot confirmed that frequencies below 150 Hz were preserved (passband), and those above were attenuated (stopband). The phase plot showed a linear trend, confirming the filter’s linear-phase property.

4. Performance Analysis
A performance evaluation of the filter design showed the following:

Stopband Attenuation: Approximately 53 dB, as expected from a Hamming window FIR filter.
Transition Band: Smooth and moderately sharp due to the Hamming window characteristics.
Group Delay: As with all linear-phase FIR filters, the group delay was constant and equal to (N-1)/2 = 25 samples, which is expected behavior and introduces a fixed time delay.
Stability: The FIR filter was inherently stable, as it did not rely on feedback or recursive elements.
Overall, the design achieved a good balance between transition width and attenuation, suitable for general-purpose low-pass filtering.

5. Observations and Conclusions
Several important observations were made from this task:

The FIR filter effectively removed high-frequency noise while preserving the integrity of the desired signal in the passband.
The linear phase ensured that there was no phase distortion, which is crucial in applications like audio and communication systems.
MATLAB's built-in tools allowed for quick design iteration, visualization, and analysis, significantly speeding up the filter development process.
The filter order (N=50) provided a good trade-off between performance and computational complexity for this basic filtering task.
The design can be extended to other filter types (e.g., high-pass, band-pass) or optimized further using different window functions or advanced techniques like equiripple design (firpm).

In conclusion, this task successfully demonstrated the complete workflow of FIR filter design, simulation, and performance analysis using MATLAB. It provided hands-on understanding of filter characteristics, impulse response behavior, and the practical effect of digital filtering on real-world-like signals.

OUTPUT:

<img width="796" height="594" alt="Image" src="https://github.com/user-attachments/assets/1cc6d8ac-7e4b-4d93-8afc-e1818e537fa4" />
<img width="791" height="578" alt="Image" src="https://github.com/user-attachments/assets/e055e56d-1e3f-4ffa-abd6-fd8b20fb8db2" />
<img width="1919" height="701" alt="Image" src="https://github.com/user-attachments/assets/a748c1ca-ebd2-400c-a3c0-faae521dec22" />
