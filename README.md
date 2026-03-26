EXPT 2a: LINEAR CONVOLUTION-USING-DFT

AIM

To perform and verify linear convolution operation of two given sequences using SCILAB.

APPARATUS REQUIRED

PC installed with SCILAB

PROGRAM:

LINEAR CONVOLUTION
```
clc;
clear;
x = [1 1 1 1];
h = [1 2 3 4];
m = length(x);
n = length(h);
a = 0:1:m-1;
b = 0:1:n-1;
subplot(3,1,1);
plot2d3(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b,h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
for i = 1:n+m-1
    conv_sum = 0;
    for j = 1:i
        if (((i-j+1) <= n) & (j <= m)) then
            conv_sum = conv_sum + x(j)*h(i-j+1);
        end
    end
    y(i) = conv_sum;
end
disp(y,'Convolution Sum using Direct Formula Method = ')
subplot(3,1,3);
plot2d3(y)
title('Graphical Representation of output Signal y');
```

### CALCULATIONS:
<img width="882" height="1280" alt="image" src="https://github.com/user-attachments/assets/11d29f12-900d-419a-88df-2699931e0a90" />


### SAMPLE OUTPUT:
<img width="752" height="698" alt="Linear Convolution dtsp" src="https://github.com/user-attachments/assets/9a1855eb-5233-458d-bd95-e34f88a3cb9e" />

RESULT:

Thus, the linear convolution of the two given sequences were performed and its result was verified.
