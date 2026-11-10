# EXP 1 A : COMPUTATION OF DFT USING DIRECT AND FFT

# AIM: 
To Obtain DFT and FFT of a given sequence in SCILAB. 

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
// DISCRETE FOURIER TRANSFORM 
clc; clear; clf;

xn = [1,2,3,4,4,3,2,1];

N = length(xn); n = 0:N-1; j = %i;

Xk = zeros(1, N);

// Direct DFT calculation for k = 0:N-1 for r = 0:N-1 Xk(k+1) = Xk(k+1) + ... xn(r+1)exp(-j2*%pikr/N); end end

disp("DFT output:"); disp(Xk);

K = 0:N-1; magnitude = abs(Xk); phase = atan(imag(Xk), real(Xk));

subplot(3,1,1); plot2d3(n, xn); xtitle("Input Sequence", "n", "x(n)");

subplot(3,1,2); plot2d3(K, magnitude); xtitle("Magnitude Spectrum", "k", "|X(k)|");

subplot(3,1,3); plot2d3(K, phase); xtitle("Phase Spectrum", "k", "Phase (radians)")

clc; clear; clf;

xn = [1,2,3,4,4,3,2,1]; N = length(xn); n = 0:N-1;

Xk = fft(xn);

disp("FFT output:"); disp(Xk);

K = 0:N-1; magnitude = abs(Xk); phase = atan(imag(Xk), real(Xk));

y = ifft(Xk);

subplot(2,2,1); plot2d3(n, xn); xtitle("Input Sequence", "n", "x(n)");

subplot(2,2,2); plot2d3(K, magnitude); xtitle("Magnitude Spectrum", "k", "|X(k)|");

subplot(2,2,3); plot2d3(K, phase); xtitle("Phase Spectrum", "k", "Phase (radians)");

subplot(2,2,4); plot2d3(n, real(y)); xtitle("Inverse FFT Output", "n", "x(n)");



# OUTPUT: 
<img width="915" height="1279" alt="WhatsApp Image 2026-11-10 at 11 43 42" src="https://github.com/user-attachments/assets/ee914003-4efd-4855-85a3-84ab6c4d4c11" />

# RESULT:
<img width="1023" height="1280" alt="WhatsApp Image 2026-11-10 at 11 43 43" src="https://github.com/user-attachments/assets/9748d99c-24c2-47e1-af26-b0b57e8085f0" />





