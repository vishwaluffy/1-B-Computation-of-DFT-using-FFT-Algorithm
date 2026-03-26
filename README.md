# EXPT 1b: Computation-of-DFT-using-FFT-ALGORITHM

## AIM
To perform and verify DFT using FFT-ALGORITHM by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT FFT-ALGORITHM
```
clear;
clc;
close all;
xn = [1 2 3 4 4 3 2 1];
n1 = 0:1:length(xn)-1;
subplot(2,2,1);
plot2d3(n1, xn);
xlabel('Time n');
ylabel('Amplitude');
title('Input Sequence');
Xk = fft(xn);
K1 = 0:1:length(Xk)-1;
magnitude = abs(Xk);
subplot(2,2,2);
plot2d3(K1, magnitude);
xlabel('Frequency (Hz)');
ylabel('Magnitude (gain)');
title('Magnitude Spectrum');
angle = atan2(imag(Xk), real(Xk));
subplot(2,2,3);
plot2d3(K1, angle);
xlabel('Frequency (Hz)');
ylabel('Phase');
title('Phase Spectrum');
y = ifft(Xk);
n2 = 0:1:length(y)-1;
subplot(2,2,4);
plot2d3(n2, y);
xlabel('Time n');
ylabel('Amplitude');
title('Inverse FFT of X(k)');
```
### CALCULATIONS:
<img width="1186" height="1302" alt="image" src="https://github.com/user-attachments/assets/a548c09a-93e3-4c07-8f3b-8e3f7d55d205" />
<img width="1070" height="1600" alt="image" src="https://github.com/user-attachments/assets/117b5bcd-c712-4108-b712-edd993f122d8" />
<img width="1299" height="1453" alt="image" src="https://github.com/user-attachments/assets/22f46e1e-2367-421e-9e22-7e8be6ead10a" />


### SAMPLE OUTPUT:
<img width="876" height="697" alt="DFT using FFT" src="https://github.com/user-attachments/assets/79c7d5f1-7c8b-4090-bf88-1d75724fd0f1" />

## RESULT:
Thus,  DFT using FFT-ALGORITHM for two given sequences were performed and its result was verified.
