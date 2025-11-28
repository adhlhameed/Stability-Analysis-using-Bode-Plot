# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/8086a9ac-c321-4697-b84d-c606a3f1bd0b" />
<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/4a173e4b-b65c-4a79-9acd-ccfb788b7d5e" />
<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/db379f98-fb03-4f9f-bb6a-fbb4538fba65" />



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wps>Wgc)
disp('stable')
elseif(Wpc == Wgc)
disp('marginally stable')
else
disp('unstable')
end
## Output:
<img width="707" height="630" alt="image" src="https://github.com/user-attachments/assets/7b8135e9-2e0a-43bb-87f3-bb392a442cbd" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin =12 <br>
Phase Margin =60 <br>
Gain crossover frequency =0.907 <br>
Phase crossover frequency = 4.4721<br>
The system is stable
