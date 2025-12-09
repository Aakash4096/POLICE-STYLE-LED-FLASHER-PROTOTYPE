# POLICE-STYLE-LED-FLASHER-PROTOTYPE
## INTRODUCTION  
•	This project is a police-style LED flasher built using the popular 555 Timer IC. 
•	The circuit uses two 555 timers (IC 555-2) arranged in simple astable mode to generate blinking signals. 
•	It operates from a 9V battery, making it suitable for: 
    o	Model vehicles 
    o	Emergency display units 
o	Electronics hobby demonstrations 
•	The flashing pattern is created by alternating a Red LED and a Blue LED, commonly used in police lights. 
•	The design focuses on: 
o	Minimal components 
o	Stable flashing 
o	Simple timing control using RC networks. 
-----------------------------------------------------------------------------------------------------------

## COMPONENTS USED  
1. 555 TIMER IC (2 Pieces)
2. RESISTORS (47Ω × 2, 1MΩ × 2)
3. CAPACITORS (1µF Polarized + 100nF Ceramic)
4. LEDs (Red + Blue)
5. 12V/9V Battery
6. Buzzer
7. Zero PCB
-----------------------------------------------------------------------------------------------------------
## CIRCUIT CONNECTIONS   

### KiCAD model  

 
![Kicad-schematics](https://github.com/Aakash4096/POLICE-STYLE-LED-FLASHER-PROTOTYPE/tree/main/Project_Assets/kicad-assets/schematics-kicad.png)        



![Kicad-wiring](https://github.com/Aakash4096/POLICE-STYLE-LED-FLASHER-PROTOTYPE/tree/main/Project_Assets/kicad-assets/PCB-2d-kicad-wiring.png)        



![Kicad-3D](https://github.com/Aakash4096/POLICE-STYLE-LED-FLASHER-PROTOTYPE/tree/main/Project_Assets/kicad-assets/PCB-3d-kicad.png)        



### LtSpice Model
![ltspice-schematics](https://github.com/Aakash4096/POLICE-STYLE-LED-FLASHER-PROTOTYPE/tree/main/Project_Assets/ltspice-assets/ltspice-schematics.png)        



![ltspice-current-through-LED](https://github.com/Aakash4096/POLICE-STYLE-LED-FLASHER-PROTOTYPE/tree/main/Project_Assets/ltspice-assets/LtSpice-current-LED.png)       



### Final outcome(real-time)  

  
![ltspice-current-through-LED](https://github.com/Aakash4096/POLICE-STYLE-LED-FLASHER-PROTOTYPE/tree/main/Project_Assets/Project_Electronics_Picture.jpg)
-----------------------------------------------------------------------------------------------------------

### Working Principle   

1. Charging Phase (Output HIGH) 
•	The 1µF capacitor charges through R1 and 0.1µF capacitor charges through R3  . 
•	While it charges from 1/3 Vcc → 2/3 Vcc, the 555 output (Pin 3) stays HIGH. 
•	This turns Red LED ON (Blue OFF). 
2. Threshold Point Reached 
•	When capacitor voltage hits 2/3 of 12V, 
 → Upper comparator triggers 
 → Flip-flop resets 
 → Output goes LOW 
 → Discharge transistor activates 
3. Discharging Phase (Output LOW) 
•	The capacitor discharges only through R2 . 
•	During discharge from 2/3 Vcc → 1/3 Vcc, 
 → Output stays LOW 
 → Blue LED turns ON (Red OFF). 
4. Trigger Point Reached 
•	When voltage reaches 1/3 Vcc, 
 → Lower comparator triggers 
 → Flip-flop sets 
 → Output returns HIGH 
The cycle repeats endlessly. 
-----------------------------------------------------------------------------------------------------------

### Timing Formula for 555 Astable Mode 
#### First 555IC 
•	ONE timing resistor (1ΜΩ) 
•	ONE timing capacitor (1µF) 
•	A diode around the capacitor making charge/discharge symmetrical 
•	The ON and OFF times use the same formula: 
T=0.693 ×R×C 
So: 
Charging time (output HIGH): 
•	THIGH = 0.693 × 1ΜΩ × 1μF THIGH = 0.693 seconds 
Discharging time (output LOW): 
Same resistor, same capacitor. 
•	TLOW = 0.693 × 1ΜΩ × 1μF 
•	TLOW = 0.693 seconds 
3. TOTAL Flash Period 
TTOTAL THIGH + TLOW T=0.693+0.6931.386 seconds 
Full flash cycle ≈ 1.4 seconds 
About 0.7 seconds ON and 0.7 seconds OFF 
#### Second 555IC   


Full flash cycle ≈ 1.4 seconds/10=0.14s 

-----------------------------------------------------------------------------------------------------------

### What We Learned From This Project 
1. Understanding of Electronic Components 
2. KiCad PCB Design Knowledge 
3. LTSpice Simulation Skills 
4. Real-Time Testing and Troubleshooting 
5. Hands-on Experience 

-----------------------------------------------------------------------------------------------------------

### Conclusion 
Built a fully functional Police Light + Siren Unit. 
Combined visual signaling (LED flashes) with audio signaling (buzzer). 
Successfully implemented: 
•	Design → Simulation → PCB → Soldering → Testing → Final working model 
Gained both theoretical knowledge and hands-on engineering experience. 
-----------------------------------------------------------------------------------------------------------

## THANKING OUR TEAM
#### Project Performed By :  
1. KUSHAL GARG ( 2024UEC1635 ) 
2. VIRENDER MEENA ( 2024UEC1711) 
3. RAHUL LAMBA ( 2024UEC1704 ) 
4. PRIYANSHU MEEL ( 2024UEC1714 ) 
5. AAKASH KUMAR( 2024UEC1706 ) 


#### Under Guidance Of : 
•Dr. Ritu Sharma 
•Sonu Jain


