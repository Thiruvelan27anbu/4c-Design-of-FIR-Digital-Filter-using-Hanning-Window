# FIR-FILTER-DESIGN
# EXP 4 c: Design-of-FIR-Digital-Filter-using-Hanning-Window

AIM:
To generate design of low pass FIR digital filter using SCILAB

APPARATUS REQUIRED:
PC Installed with SCILAB

PROGRAM
clc; clear; close;

// Input values M = input('Enter the Odd Filter Length = '); Wc = input('Enter the Digital Cut off frequency = ');

// Centre value alpha = (M - 1)/2;

// Ideal LPF impulse response for n = 1:M if (n == alpha + 1) then hd(n) = Wc/%pi; else hd(n) = sin(Wc*((n-1)-alpha)) / (((n-1)-alpha)*%pi); end end

// Hanning Window for n = 1:M W(n) = 0.5 - (0.5cos((2%pi*(n-1))/(M-1))); end

// Windowing process h = hd .* W;

// Display filter coefficients disp(h, 'Filter Coefficients are');

// Frequency response [hzm, fr] = frmag(h, 256);

// Magnitude response subplot(2,1,1); plot(2*fr, hzm); xlabel('Normalized Digital Frequency W'); ylabel('Magnitude'); title('Frequency Response of FIR LPF using Hanning Window');

// Magnitude response in dB hzm_dB = 20*log10(hzm);

subplot(2,1,2); plot(2*fr, hzm_dB); xlabel('Normalized Digital Frequency W'); ylabel('Magnitude in dB'); title('Frequency Response of FIR LPF using Hanning Window');

OUTPUT

<img width="761" height="722" alt="image" src="https://github.com/user-attachments/assets/98ff9686-5322-4305-b6ce-3acd7421b146" />
RESULT
Thus, the FIR Low-Pass Filter using the Hanning Window was successfully designed and implemented in Scilab.
