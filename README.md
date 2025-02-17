# YashasKumar
EXPERIMENT 1

CIRCUIT 1

AIM:To study the characteristics and switching behavior of an NMOS transistor in a common-source configuration. The experiment involves analyzing how the transistor operates as a switch by varying the gate voltage (V₂) and observing the output voltage at the drain.

COMPONENTS REQUIRED:
Mosfet(nmos4 ,pmos4 ), Resistor(22k), voltage supply(1.8V,0.9V) and connecting wires.

THEORY:
Mostfet is one of the most important compontent in electronics .This importance is due to the fact of its compact design , low power consumption ,simple geometry and compatibilty in VLSI technology.There are three different configurations in which the mosfet can be connected (namely common drain,gate and source) the most popular being common source and common drain configurations.The Mosfet acts as an amplifier in the saturation region of operation where Vgs > Vth,Vgd < Vth and Vds>=Vov for an N channel mosfet. In the common source configuration there is a 180 degree phase shift between input and output.
There is very high input impedance (Ig=0) ideally infinite.

The drain current equation Id = 1/2 kn Vov2 ; Vov=Vgs-Vth and kn=un Cox W/L,Output is taken from the drain end rather than simply across the resistor to maintain the common ground referance.

DC ANALYSIS: This to done to analyse the response of the circuit to time varying signals.This is helpful to determine the signl distorton, DC shift between the input and the output. This plays key role in detecting issues like phase distortion.This is essential for high speed applications like communication systems.
![image](https://github.com/user-attachments/assets/9b541255-143f-47de-96b5-4afa7604c330)

AC ANALYSIS: This is nothing but the small signal analysis of the circuit.This is done to determine the Gain of the amplifier circuit .
This also helps to analyze the Frequency Reponse of the amplifier circuit. the gain is given by Av = -gm Rd.
![image](https://github.com/user-attachments/assets/404835e5-5e76-4feb-80e9-e35cb09b3adb)

TRANSIENT ANALYSIS:This to done to analyse the response of the circuit to time varying signals.This is helpful to determine the signl distorton, DC shift between the input and the output. This plays key role in detecting issues like phase distortion.This is essential for high speed applications like communication systems.
![image](https://github.com/user-attachments/assets/105f2045-8e57-48ca-8c62-3a361626d83b)

PROCEDURE:
   * Connect the drain of the NMOS transistor (M1) to the 1kΩ resistor (R1).
   * Connect the other end of R1 to the V1 (1.8V DC power supply).
   * Connect the source of M1 to ground.
   * Connect the gate of M1 to a variable DC voltage source (V2).
   * Set up a multimeter or oscilloscope to measure the drain voltage (V_D).
![image](https://github.com/user-attachments/assets/ed09e428-e3a5-44cb-bd03-77a132781867)

CALCULATION:
Power = 50uW

Loop Equation: Vdd=Vds+Id*Rd

P=I*V (Id=27.08uA , Vdd=1.8V)

clearly Vds=Vout; Vds>=Vgs-Vth

Rd (upon calculation) =10.33Kohm

Widhth=0.3um(Vary width to get the current)

Vds=1.772V

gain=-20dB(from AC analysis)

Q point is (1.772V,27.08uA)

RESULTS:
DC ANALYSIS:Id=27.08uA
Vout=1.772V
Width=1.08um
DC Operating point : (1.772V,27.08uA) is obtained for 0.3um Width and 180nm Length.

TRANSIENT ANALYSIS: Vout=1.772V
There is 180 degree phase shift between input and output or the DC level shift.

AC ANALYSIS: Gain=-20dB

INFERENCE:
1.Current is directly Propotional to the Width of the Mosfet and the current varies with the change in width.
2.Mosfet saturation ensures the mosfet works as an amplifier and produces the desired negative gain as per the equation Av=-gm*Rd.
3.Q point stability is attained in saturation region thus helping in attaining linear amplification .
4.The Mosfet gain is increased in mid band frequency range (small signal analysis).
5.The Transient analysis reveleas the response of the circuit to time domain ssignal and determines how quickly the circuit responds to variation.
This is essential in high speed applications.
6.AC Analysis helps in designing circuits with desired gain and helps in impedance matching.
Also helps in understanding the frequency response and small signal behaviour of the circuit.

CIRCUIT 2

THEORY:
A Diode connected mosfet transistor always is in saturation and acts as a constant current source and acts as a amplifier. The different type of analysis are DC Analysis, AC Analysis and Transient analysis. The drain current obtained is given by the formula
Id = 1/2 kn Vov2 ; Vov=Vgs-Vth and kn=un Cox W/L.

DC ANALYSIS: This is done ensure the mosfet operates in saturation and to calculate the DC operationg point of the transistor. This prevents signal distortion .This helps in the determination of the biasing resistors.This helps in getting a correct operating point despite the fluctuation in the other parameters.
![image](https://github.com/user-attachments/assets/80235237-5c30-4151-8cf1-84c4e8f79679)


TRANSIENT ANALYSIS: This to done to analyse the response of the circuit to time varying signals.This is helpful to determine the signl distorton, DC shift between the input and the output. This plays key role in detecting issues like phase distortion.This is essential for high speed applications like communication systems.
![image](https://github.com/user-attachments/assets/ca00cc7d-204e-41b1-af87-bcaeaaacace3)


AC ANALYSIS: This is nothing but the small signal analysis of the circuit.This is done to determine the Gain of the amplifier circuit .This also helps to analyze the Frequency Reponse of the amplifier circuit. the gain is given by Av = -gm Rd.
![image](https://github.com/user-attachments/assets/d4cc5deb-d61b-494a-85b5-ddb03f1e4f50)


PROCEDURE:
1. Open LTspice and Create a New Schematicand Launch LTspice.Create a new schematic by selecting File → New Schematic.
2. Place Components Voltage Sources (V1 & V2) and Select Voltage and place two sources.Set V1 as a DC source with 1.8V.Set V2 as an AC + sine source: SINE(0.7 50m 1K) AC 1.
Transistors (PMOS & NMOS),Add PMOS and NMOS transistors from the component library.Connect them in a CMOS inverter configuration:M2 (PMOS): Source to V1 (1.8V), Drain to Vout.
M1 (NMOS): Drain to Vout, Source to Ground.Gate of both transistors connected to V2.
3. Define the MOSFET Models
AC Analysis:.ac dec 20 0.1 1T.This performs an AC sweep from 0.1Hz to 1THz in 20 points per decade.
Transient Analysis:.tran 3m,Runs a transient simulation for 3ms.
4.Observe how the circuit responds in time domain (transient).Check the gain and phase shift (AC analysis).
![image](https://github.com/user-attachments/assets/77b1a546-b52a-4995-92df-197c177a3cdf)

CALCULATIONS:
Power = 50mW

P = V*I ; ( V= 1.8 V)
That implies Id = 27.08uA

V out/sub> = 1.658 V

Length= 180nm

Vds = Vout

RESULT:
DC ANALYSIS:( 1.658V ,27.08uA)
TRANSIENT ANALYSIS: There is 180 degree phase shift between input and output and a DC level phase shift observed.
Vout=1.658V and the width =700u
AC ANALYSIS:Gain = -0.92dB

INFERENCE:
1.The Current Id is dependent on width and hence it changes when the width changes whereas the remaining parameters remain constany.
2.DC Analysis ensures proper biasing and hence the mosfet operates in saturation and Q point stability is attained.
3.The Transient analysis reveleas the response of the circuit to time domain ssignal and determines how quickly the circuit responds to variation.
This is essential in high speed applications.
4.AC Analysis helps in designing circuits with desired gain and helps in impedance matching.
Also helps in understanding the frequency response and small signal behaviour of the circuit.
5.Together all the analysis helps in designing and opyimising an amplifier.
