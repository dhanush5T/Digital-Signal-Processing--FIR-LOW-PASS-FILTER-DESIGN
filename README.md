# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
 clear all; % clear screen
 close all; % close all figure windows
wc=input('enter the value of cut off frequency'); 
N=input('enter the value of filter'); 
alpha=(N-1)/2; 
eps=0.001; 
%High Pass Filter Coefficient
n=0:1:N-1; 
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)wc))./(pi(n-alpha+eps))
%Hamming Window Sequence 
n=0:1:N-1; 
wh=0.54-0.46*cos((2*pi*n)/(N-1))
hn=hd.*wh 
% Plot the High Pass Filter with Hamming Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
![WhatsApp Image 2025-11-17 at 12 25 41_605e5f47](https://github.com/user-attachments/assets/30730291-52f1-4a38-88f5-8fd49976a6e5)


## RESULT:
![WhatsApp Image 2025-11-28 at 20 40 54_2d70e3f9](https://github.com/user-attachments/assets/73a270d2-c1be-481f-bc63-594c4fff31a4)

