# EVALUATION-OF-RADAR-RANGE-
# AIM
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.
# EQUIPMENTS REQUIRED

• Computer with i3 Processor

• SCI LAB

# THEORY
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:

<img width="457" height="528" alt="image" src="https://github.com/user-attachments/assets/0a3969a4-d771-4537-989c-dc5cf96b7c0e" />

# PROCEDURE

1.	Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice.
2.	Import Necessary Libraries: Import the math library in Python.
3.	Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.
4.	Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.
5.	Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.
6.	Execute the Program: Run the Python script to calculate and display the maximum range of the radar.
# PROGRAM
```ASM
pi = %pi;
lambda = 0.03; 
sigma = 1;
Gt = 30/43;
Gr = 30/456212301;
Pt = 900;
R = 1:1:10000;
Pr = (Pt * Gt * Gr * lambda^2 * sigma) ./ ((4 * pi)^3 * R.^4);
subplot(3,1,1);
plot(R, 10*log10(Pr)); 
Pt_values = 100:100:10000;
R_const = 545100;
Pr_vs_Pt = (Pt_values * Gt * Gr * lambda^2 * sigma) ./ ((4 * pi)^3 * (R_const^4));
subplot(3,1,2);
plot(Pt_values, 10*log10(Pr_vs_Pt));
Gain_values = 10:5:50;
Pr_vs_Gain = (Pt * (Gain_values.^2) * lambda^2 * sigma) ./ ((4 * pi)^3 * (R_const^4));
subplot(3,1,3);
plot(Gain_values, 10*log10(Pr_vs_Gain));
```
# OUTPUT
<img width="756" height="717" alt="image" src="https://github.com/user-attachments/assets/7f0d8563-0c75-4eaa-a822-5f7d3741dda1" />

# TABULATION

# RESULT
Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python program.


