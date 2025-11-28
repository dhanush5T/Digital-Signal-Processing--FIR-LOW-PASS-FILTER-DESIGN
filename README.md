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
wc=input('enter the value of Wc='); 
N=input('enter the value of N=');
alpha=(N-1)/2; 
eps=0.001; 
%Low Pass Filter Coefficient
n=0:1:N-1; 
hd=sin(wc*(n-alpha+eps))./(pi*(n-alpha+eps))
%Blackman Window Sequence 
n=0:1:N-1; 
wh=0.42-0.5*cos((2*pi*n)/(N-1))-0.08*cos((4*pi*n)/(N-1))
hn=hd.*wh 
% Plot the Band Pass Filter with Blackman Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
![WhatsApp Image 2025-11-28 at 20 49 38_1115171f](https://github.com/user-attachments/assets/e9dec861-1dd1-49ea-b97c-6174e3dd95f6)

## RESULT:
<img width="1600" height="594" alt="image" src="https://github.com/user-attachments/assets/39dbc489-785a-4bae-84cc-c5183bb887c7" />


