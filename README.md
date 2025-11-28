# Mean-and-Variance-AC
mean_and_varaiance
Aim

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

Equipments Needed

1.Computer with i3 Processor

2.SCI LAB

Algorithm

Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
Evaluate the Function: Compute the function values at each of these sample points.
Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
Display Results: Output the computed mean variance and Cross Correlation.
Procedure

Refer Algorithms and write code for the experiment.
Open SCILAB in System
Type your code in New Editor
Save the file
Execute the code
If any Error, correct it in code and execute again
Verify the generated results

Program
~~~
Mean

function y = f(x)
    z = 3.6 * (1 - x)^2;
    y = x * z;
endfunction
function y = c(y_input)
    z = 3.6 * (1 - y_input)^2;
    y = y_input * z;
endfunction
a = 0;
b = 1;
EX = intg(a, b, f);
EY = intg(a, b, c);
disp(EX, "i) Mean of X = ");
disp(EY, "Mean of Y = ");
Varaince

function y=g(x)
    z= 3.6*(1-x).^2;
    y=x.^2 .*z;
endfunction
a=0;
b=1;
[EX2, errX2]= intg(a,b,g);
function y=h(yv)
    z= 3.6*(1-yv).^2;
    y=yv.^2 .*z;
endfunction
[EY2, errY2]=intg(a,b,h)
vX2=EX2-EX^2;
vY2=EY2-EY^2;
disp(vX2, "ii)Variance of X=");
disp(vY2, " Variance of Y=");
Cross Correlation

x=input("type in the referance sequence=");
y=input("type in the second sequence=");
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
~~~
Output Waveform

<img width="1920" height="1200" alt="Screenshot (127)" src="https://github.com/user-attachments/assets/94561ad0-c2a5-4529-8555-0ad798918b9a" />

Calculation

<img width="752" height="1280" alt="image" src="https://github.com/user-attachments/assets/f7d0c6b9-2e28-40a6-80b7-375542438c29" />
<img width="851" height="1280" alt="image" src="https://github.com/user-attachments/assets/e6328dbd-9aa3-4c93-9d80-c29373932033" />


Result 

Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
