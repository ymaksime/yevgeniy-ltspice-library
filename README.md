# yevgeniy-ltspice-library
This is my LTSpice library with different .models

Here is a short description about different parameters in the LTSpice .model blocks and their corresponding entries in datasheets

BJT Model Example
FMMT458
Datasheet: https://www.diodes.com/assets/Datasheets/FMMT458.pdf

LTSpice Model
.MODEL FMMT458 NPN ( IS=5.32E-14 NF=1 BF=230 IKF=1.5 VAF=1500
    + ISE=2.1E-14 NE=1.385 NR=1.05 BR=8 IKR=0.7 VAR=64 ISC=6.42E-12
    + NC=1.25 RB=0.5 RE=0.224 RC=0.134 QUASIMOD=1 RCO=80 GAMMA=4E-7
    + CJC=9.5E-12 MJC=0.32 VJC=0.4 CJE=115E-12 MJE=0.37 VJE=0.8
    + TF=1.3E-9 TR=16E-6 TRC1=.004 TRB1=.004 TRE1=.004 XTB=1.4 )
	
Correclation
source: https://www.youspice.com/spice-modeling-of-a-bjt-from-datasheet/

".MODEL" = LTSpice directive for primitive components (resistors, capacitors, inductors, diodes, transistors)
"FMMT485" = Name of the component.  It should match with the component name in the schematic
"NPN" = type
"IS" = Transport saturation current (default = 1e-16) | A | Ie = Is*(e^(q*Vbe/k/T)-1)
"NF" = 
"BF" = Ideal maximum forward beta | no unit dimension |
"IKF" = Corner for forward-beta high-current roll-off | A |
"VAF" = Forward Early voltage | V |
"ISE" = Base-emitter leakage saturation current | A |
"NE" = Base-emitter leakage emission coefficient | no unit dimension |
"NR" = 
"BR" = Ideal maximum reverse beta | no unit dimension |
"IKR" = Corner for reverse-beta high-current roll-off | A |
"VAR" = 
"ISC" = Base-collector leakage saturation current | A |
"NC" = Base-collector leakage emission coefficient | A |
"RB" = Zero-bias (maximum) base resistance | Ohm |
"RE" = 
"RC" = Collector ohmic resistance | Ohm |
"QUASIMOD" = 
"RCO" = 
"GAMMA" = 
"CJC" = Base-collector zero-bias p-n capacitance | F |
"MJC" = Base-collector p-n grading factor | no unit dimension |
"VJC" = 
"CJE" = Base-emitter zero-bias p-n capacitance | F |
"MJE" = Base-emitter p-n grading factor | no unit dimension |
"VJE" = Base-emitter built-in potential | V |
"TF" = Ideal forward transit time | sec |
"TR" = Ideal reverse transit time | sec |
"TRC1" = 
"TRB1" = 
"TRE1" = 
"XTB" = Forward and reverse beta temperature coefficient | no unit dimension |