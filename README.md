# EXPT-6-Simulation-of-Multirate-DSP-using-Decimation-and-Interpolation

# AIM: 

# To perform and verify Multirate-DSP-using-Decimation-and-Interpolation.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
clear;
close;
n = 0:%pi/50:2*%pi;
x = sin(%pi*n);   // original signal
M = input("Enter the downsampling factor M = ");
L = input("Enter the upsampling factor L = ");
downsampling_x = x(1:M:length(x));
disp("Input signal x(n) = ");
disp(x);
disp("Downsampled Signal = ");
disp(downsampling_x);
figure(1);
subplot(2,1,1);
plot2d3(1:length(x), x);
xtitle("Original Signal");
subplot(2,1,2);
plot2d3(1:length(downsampling_x), downsampling_x);
xtitle("Downsampled Signal by factor M");
upsampling_x = zeros(1, L*length(x));
for i = 1:length(x)
    upsampling_x(1, L*(i-1)+1) = x(i);
end
disp("Upsampled Signal = ");
disp(upsampling_x);
figure(2);
subplot(2,1,1);
plot2d3(1:length(x), x);
xtitle("Original Signal");

subplot(2,1,2);
plot2d3(1:length(upsampling_x), upsampling_x);
xtitle("Upsampled Signal by factor L");
```

# OUTPUT: 
<img width="762" height="705" alt="image" src="https://github.com/user-attachments/assets/9beedd7e-c54b-4358-a329-7b99d734cb7c" />
<img width="759" height="715" alt="image" src="https://github.com/user-attachments/assets/4d2e2fac-3c96-4f99-8fc8-4156ed09c6c3" />


# RESULT: 
Thus the Multirate-DSP-using-Decimation-and-Interpolation using python was performed and verified.
