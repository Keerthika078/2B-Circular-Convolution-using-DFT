# EXPT 2B:CIRCULAR-CONVOLUTION-USING-DFT
## AIM
To perform and verify circular convolution operation of two given sequences using SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM:
## CIRCULAR CONVOLUTION
```
clc; clear; 
x=[1 1 1 1]; 
n1=0:1:length(x)-1; 
subplot(3,1,1); 
plot2d3(n1,x); 
xlabel('time'); 
ylabel('amplitude'); 
title('input sequence'); 
h=[1 2 3]; 
n2=0:1:length(h)-1; 
subplot(3,1,2); 
plot2d3(n2,h); 
xlabel('time');
ylabel('amplitude'); 
title('impulse sequence'); 
N1=length(x); 
N2=length(h); 
N=max(N1,N2); 
N3=N1-N2; 
if(N3>0) 
h=[h,zeros(1,N3)]; 
else 
x=[x,zeros(1,abs(N3))]; 
end 
disp(x) 
disp(h) 
for n=1:N 
y(n)=0; 
for i=1:N 
j=n-i+1; 
if(j<=0) 
end 
j=N+j; 
y(n)=y(n)+x(i)*h(j); 
end 
end 
 
disp(y) 

 
n=0:N-1; 
 
subplot(3,1,3); 
 
plot2d3(n,y); 
 
xlabel('time'); 
ylabel('amplitude'); 
title('circular convolution');

```
### CALCULATIONS:
![WhatsApp Image 2026-03-26 at 9 53 26 PM](https://github.com/user-attachments/assets/1428e60c-f5f3-4473-ac2d-f13876fbc9c6)

### SAMPLE OUTPUT:
![WhatsApp Image 2026-03-26 at 9 53 38 PM](https://github.com/user-attachments/assets/4b97649d-de5b-4ba9-b8ad-0f3e508e3f6b)




## RESULT:
Thus, the circular convolution of the two given sequences were performed and its result was verified.

