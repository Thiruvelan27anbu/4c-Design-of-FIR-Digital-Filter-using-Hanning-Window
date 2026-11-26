FIR-FILTER-DESIGN
EXP 4 c: Design-of-FIR-Digital-Filter-using-Hanning-Window
AIM 1: To perform Design-of-LOWPASS FIR-Digital-Filter-using-Hanning-Window using SCILAB.
APPARATUS REQUIRED:
PC installed with SCILAB.

PROGRAM:
clc; clear; close;

N = 21;
wc = %pi / 2;
alpha = (N - 1) / 2;

hd = zeros(1, N); for n = 0 : N-1 if n == alpha then hd(n+1) = wc / %pi; else hd(n+1) = sin(wc * (n - alpha)) / (%pi * (n - alpha)); end end

w = zeros(1, N); for n = 0 : N-1 w(n+1) = 0.5 - 0.5 * cos((2 * %pi * n) / (N - 1)); end

h = hd .* w;

[H, w_freq] = frmag(h, 256);

figure; subplot(2, 1, 1); plot2d3(0:N-1, h);
plot(0:N-1, h, 'ro');
xtitle('Impulse Response', 'n', 'h(n)'); xgrid(1);

subplot(2, 1, 2); H_dB = 20 * log10(H);
plot(w_freq, H_dB); xtitle('Magnitude Response', 'Normalized Frequency', 'Magnitude (dB)'); xgrid(1);

OUTPUT:
<img width="1912" height="892" alt="image" src="https://github.com/user-attachments/assets/90fbf731-8057-4e23-8426-7b040b969cae" />

RESULT:
Thus design of low pass FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.

AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.
APPARATUS REQUIRED:
PC installed with SCILAB.

PROGRAM:
clc; clear; close;

N = 21;
wc = %pi / 2;
alpha = (N - 1) / 2;

hd = zeros(1, N); for n = 0 : N-1 if n == alpha then hd(n+1) = 1 - (wc / %pi); else hd(n+1) = -sin(wc * (n - alpha)) / (%pi * (n - alpha)); end end

w = zeros(1, N); for n = 0 : N-1 w(n+1) = 0.5 - 0.5 * cos((2 * %pi * n) / (N - 1)); end

h = hd .* w;

[H, w_freq] = frmag(h, 256);

figure; subplot(2, 1, 1); plot2d3(0:N-1, h);
plot(0:N-1, h, 'ro');
xtitle('Impulse Response', 'n', 'h(n)'); xgrid(1);

subplot(2, 1, 2); H_dB = 20 * log10(H);
plot(w_freq, H_dB); xtitle('Magnitude Response', 'Normalized Frequency', 'Magnitude (dB)'); xgrid(1);

OUTPUT:
<img width="1917" height="892" alt="image" src="https://github.com/user-attachments/assets/31a65bb0-358a-444b-b093-2e5d61e69f8f" />
RESULT:
Thus design of HIGH pass FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.

AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.
APPARATUS REQUIRED:
PC installed with SCILAB.

PROGRAM:
clc; clear; close;

N = 21;
wc1 = %pi / 4;
wc2 = 3 * %pi / 4;
alpha = (N - 1) / 2;

hd = zeros(1, N); for n = 0 : N-1 if n == alpha then hd(n+1) = (wc2 - wc1) / %pi; else hd(n+1) = (sin(wc2 * (n - alpha)) - sin(wc1 * (n - alpha))) / (%pi * (n - alpha)); end end

w = zeros(1, N); for n = 0 : N-1 w(n+1) = 0.5 - 0.5 * cos((2 * %pi * n) / (N - 1)); end

h = hd .* w;

[H, w_freq] = frmag(h, 256);

figure; subplot(2, 1, 1); plot2d3(0:N-1, h);
plot(0:N-1, h, 'ro');
xtitle('Impulse Response', 'n', 'h(n)'); xgrid(1);

subplot(2, 1, 2); H_dB = 20 * log10(H);
plot(w_freq, H_dB); xtitle('Magnitude Response', 'Normalized Frequency', 'Magnitude (dB)'); xgrid(1);

OUTPUT:
<img width="1917" height="876" alt="image" src="https://github.com/user-attachments/assets/0afefabe-ace2-4b02-9a87-bc661636495f" />
RESULT:
Thus design of BAND pass FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.

AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.
APPARATUS REQUIRED:
PC installed with SCILAB.

PROGRAM:
clc; clear; close;

N = 21;
wc1 = %pi / 4;
wc2 = 3 * %pi / 4;
alpha = (N - 1) / 2;

hd = zeros(1, N); for n = 0 : N-1 if n == alpha then hd(n+1) = 1 - ((wc2 - wc1) / %pi); else hd(n+1) = (sin(wc1 * (n - alpha)) - sin(wc2 * (n - alpha))) / (%pi * (n - alpha)); end end

w = zeros(1, N); for n = 0 : N-1 w(n+1) = 0.5 - 0.5 * cos((2 * %pi * n) / (N - 1)); end

h = hd .* w;

[H, w_freq] = frmag(h, 256);

figure; subplot(2, 1, 1); plot2d3(0:N-1, h);
plot(0:N-1, h, 'ro');
xtitle('Impulse Response', 'n', 'h(n)'); xgrid(1);

subplot(2, 1, 2); H_dB = 20 * log10(H);
plot(w_freq, H_dB); xtitle('Magnitude Response', 'Normalized Frequency', 'Magnitude (dB)'); xgrid(1);

OUTPUT:
<img width="1917" height="892" alt="image" src="https://github.com/user-attachments/assets/adfcff09-8d4e-4b0a-9377-7cfafdd81fad" />

# RESULT:
Thus design of BAND STOP FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.

