 # Analysis-of-open-loop-and-closed-loop-control-system
## Aim :
  To analyse the open loop and closed loop system having G(S)=1/(S^2+10S+20)  when an unit step input is applied using MATLAB.
## Apparatus Required:
  Computer with MATLAB software
## Theory
  ### Open loop control system
  In this system, the output doesn’t change the action of the control system. It doesn’t have any feedback. It is very simple, needs low maintenance, quick operation, and cost-effective. The accuracy of this system is low and less dependable.
  <img width="652" height="175" alt="image" src="https://github.com/user-attachments/assets/0a9d8129-eb64-40bb-8efd-434edcb2bd5a" />
 ### Closed loop control System
The closed-loop control system can be defined as the output of the system that depends on the input of the system. This control system has one or more feedback loops among its input & output. This system provides the required output by evaluating its input. This kind of system produces the error signal and it is the main disparity between the output and input of the system.
                     <img width="508" height="220" alt="image" src="https://github.com/user-attachments/assets/ad4b9b9e-bf06-4108-a4c0-5320be064b1f" />

Consider a system having plant G(S)=  1/(S^2+10S+20), H(S) = 1(negative unity feedback system) and Controller C(S) = 300.
C(S) and G(S) are in series, 300/(S^2+10S+20)
300/(S^2+10S+20) and H(S) are in negative feedback.
Therefore, Closed loop transfer function, (C(S))/(R(S))=300/(S^2+10S+320)
## Program: 
### Open loop System
num = [1]
den = [1 10 20]
sys=[tf(num, den)]
step(sys)

### Closed loop System
num=[300]
den=[1 10 320]
sys=[tf(num,den)]
t=0:0.01:2;
num=[300]
den=[1 10 20]
sys=tf(num,den)
sys1=feedback(sys,1)
step(sys1)

## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Analyse the result.
## Output:
### Open Loop System
<img width="1919" height="904" alt="Screenshot 2025-09-24 091151" src="https://github.com/user-attachments/assets/12aac448-1a08-4e8a-b953-a7dbe5888aa3" />
<img width="1919" height="1127" alt="Screenshot 2025-09-24 090745" src="https://github.com/user-attachments/assets/33888454-f12e-496f-a2bc-a4450f6d41fa" />



### Closed Loop System
<img width="1892" height="1019" alt="Screenshot 2025-09-24 092920" src="https://github.com/user-attachments/assets/a4b68048-6a45-4564-9d6a-1dd6f94a4ae2" />
<img width="1919" height="1105" alt="Screenshot 2025-09-24 092946" src="https://github.com/user-attachments/assets/93c1381e-15f4-4257-89e6-3e76c02155e0" />
<img width="683" height="619" alt="Screenshot 2025-09-24 092126" src="https://github.com/user-attachments/assets/d559dcaf-f8ab-4639-a17e-e9ee0c112db9" />




## Result:
Thus the open loop and closed loop system are analysed and the following conclusions are arrived.
### Open loop system
Steady State Error = 0.96
Settling Time =2.13s 
### Closed loop System
Steady State Error = 0.06
Settling Time = 1.38s 





