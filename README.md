## Experiment No: 3
DIFFERENTIATOR USING OP-AMP (μA741)
## Aim
To design and simulate a Differentiator circuit using μA741 in Proteus Design Suite and verify that the output is proportional to the rate of change of input voltage.
## Apparatus Required
•	μA741 Op-Amp
•	Capacitor C = 0.01 µF
•	Resistor Rf = 10 kΩ
•	Signal Generator
•	Dual Power Supply (±15V)
•	CRO / Oscilloscope
•	Connecting wires
## Circuit Diagram

<img width="1226" height="622" alt="image" src="https://github.com/user-attachments/assets/e91bb91f-258f-48b4-9d4e-9877e5c0a202" />

## Connection Details:
•	Input signal → Capacitor (C) → Inverting terminal (Pin 2)
•	Feedback resistor (Rf) → Between Output (Pin 6) and Pin 2
•	Non-inverting terminal (Pin 3) → Ground
•	Pin 7 → +15V
•	Pin 4 → −15V
## Theory
A Differentiator circuit produces an output voltage proportional to the rate of change of input voltage.
## Working Principle:
•	When input changes rapidly → output amplitude increases
•	When input is constant → output is zero
•	Output is inverted
## Procedure
1.	Open Proteus software.
2.	Select μA741, capacitor, resistor, signal generator, and CRO.
3.	Connect circuit in differentiator configuration.
4.	Apply ±15V power supply.
5.	Set input sine wave (1V, 1kHz).
6.	Run simulation.
7.	Observe input and output waveforms on CRO.
## Tabulation
```

S.No 	         Input Signal	          Frequency	      Expected  Output	                                      Practical Observation

1	             Sine wave (2 Vpp)	    500 Hz	        Cosine wave (leads input by 90°), small amplitude	      Cosine waveform observed, slight attenuation
2            	Sine wave (2 Vpp)	      1 kHz	          Cosine wave, higher amplitude than 500 Hz	              Increased amplitude, clear 90° lead
3            	Square wave (2 Vpp)   	1 kHz	          Sharp positive and negative spikes                     	Narrow spikes observed at transitions
4	            Triangular wave (2 Vpp)	1 kHz	          Square wave output	                                    Square waveform observed
```

## Waveforms
•	Sine input → Cosine output (90° phase shift)
•	Square input → Positive & negative spikes
•	Triangular input → Square wave
<img width="1365" height="1171" alt="image" src="https://github.com/user-attachments/assets/7e653614-d70b-4f5b-bf76-869e279e419b" />
<img width="1369" height="1137" alt="image" src="https://github.com/user-attachments/assets/56c4db90-27fa-41b5-bed5-2cf765642f8d" />
<img width="1374" height="1135" alt="image" src="https://github.com/user-attachments/assets/a6cb9a39-37c0-4cb0-b40f-2f3eba3f040d" />


## Result
The Differentiator circuit using μA741 Op-Amp was successfully designed and simulated in Proteus.
The output waveform is proportional to the rate of change of input voltage.
The circuit behaves as a differentiator.
## Conclusion
•	Output depends on frequency.
•	Output leads input by 90° (for sine input).
•	Higher frequency → Higher output amplitude.
•	Used in wave shaping and signal processing applications.
## Viva Questions
```
1.	What is a differentiator?
A Differentiator is an op-amp circuit in which the output voltage is proportional to the rate of change of the input voltage (i.e., derivative of the input signal).
It uses:
Capacitor at the input
Resistor in the feedback path

2.	Write the output equation of differentiator.
The output voltage is: 
Vout = −RC dVin/dt
Where:
R = Feedback resistor
C = Input capacitor
dVin/dt = Rate of change of input voltage
The negative sign indicates phase inversion.

3.	Why is output leading input?
For a sinusoidal input:
𝑑(sin⁡𝜔𝑡)/𝑑𝑡 = 𝜔cos𝜔𝑡dt
Since cosine leads sine by 90°, the output waveform leads the input by 90°.
​
4.	What happens at very high frequency?
At very high frequency:
Capacitive reactance becomes very small
Gain increases
Noise gets amplified
Circuit may become unstable
This makes the ideal differentiator impractical at high frequencies.

5.	What is practical differentiator?
A Practical Differentiator is a modified differentiator circuit that includes:
A resistor in series with the input capacitor
A capacitor in parallel with the feedback resistor
These components:
Reduce noise
Improve stability
Limit high-frequency gain
```
