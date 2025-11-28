# EVALUATION OF RADAR RANGE
# AIM
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.
# EQUIPMENTS REQUIRED

• Computer with i3 Processor

• SCI LAB

# THEORY
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:

<img width="457" height="528" alt="image" src="https://github.com/user-attachments/assets/0a3969a4-d771-4537-989c-dc5cf96b7c0e" />

## Algorithm

1. Initialize constants:
   - λ (wavelength) = 0.03 m  
   - σ (radar cross section) = 1 m²  

2. Vary each parameter while keeping the others constant:
   - **Pt:** 0.1 → 10  
   - **Gt:** 1 → 50  
   - **Pm:** 1e⁻¹⁵ → 1e⁻¹⁰  

3. Compute maximum range using:
   R_max = ((Pt * Gt² * λ² * σ) / ((4π)³ * Pm))¼


4. Plot the following:
   - `Pt vs Rmax` 
   - `Gt vs Rmax` 
   - `Pm vs Rmax`
     
---

## Procedure

1. **Refer to the Algorithm** and write the Scilab code for the experiment.  
2. **Open Scilab** on your system.  
3. **Create a New Editor File:**  
   - Go to `File → New → Script`.  
4. **Type Your Code** in the editor window.  
5. **Save the File** with a suitable name (e.g., `radar_range.sce`).  
6. **Execute the Code:**  
   - Press **F5** or click **Execute → File with echo**.  
7. **If Any Errors Occur:**  
   - Review and correct the code.  
   - Save and **run it again** until it executes successfully.

---


# PROGRAM
```ASM
lambda = 0.05;      
sigma  = 2;         

Pt_vals = 0.5:0.5:20;   
Gt_const = 20;          
Pm_const = 1e-14;       

Rmax_Pt = ((Pt_vals .* Gt_const.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_const)).^(1/4);

Gt_vals = 5:2:100;      
Pt_const = 3;           
Pm_const = 1e-14;       

Rmax_Gt = ((Pt_const .* Gt_vals.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_const)).^(1/4);

Pm_vals = logspace(-14, -9, 50);  
Pt_const = 2;          
Gt_const = 25;         

Rmax_Pm = ((Pt_const .* Gt_const.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_vals)).^(1/4);

subplot(3,1,1);
plot(Pt_vals, Rmax_Pt);

subplot(3,1,2);
plot(Gt_vals, Rmax_Gt);

subplot(3,1,3);
plot(Pm_vals, Rmax_Pm);

``` 
# OUTPUT
<img width="940" height="900" alt="image" src="https://github.com/user-attachments/assets/b4ad059d-663c-414c-b628-16d46c557c62" />

# TABULATION
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/90190e0b-9511-49ae-a404-109ffa7f0bb8" />


# RESULT
Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python program.


