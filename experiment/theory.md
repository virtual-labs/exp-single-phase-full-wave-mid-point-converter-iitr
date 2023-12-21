
<head>

<script type="text/javascript" async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML"> 
  
</script>

</head>

<div style="font-family: 'Nunito Sans', sans-serif; font-size: 20px;text-align: justify;">

### **Introduction**

A full-wave controlled mid-point converter is a power electronics circuit that is used to convert alternating current (AC) input voltage to a desired output voltage level. It is called a mid-point converter because it operates with a mid-point voltage, which is typically half of the input voltage.

The full-wave controlled mid-point converter consists of a bridge rectifier, a center-tapped transformer and two thyristors (SCRs). The bridge rectifier is connected to the AC input voltage source, and its output is connected to the center-tapped transformer. The center tap of the transformer is connected to the ground or reference potential.

The operation of the full-wave controlled mid-point converter can be divided into two modes: positive half-cycle mode and negative half-cycle mode.<br>

<b>During the positive half-cycle mode:</b><br>
1. The thyristor connected to the positive terminal of the bridge rectifier is triggered and conducts current. This allows the positive half-cycle of the AC voltage to flow through the transformer.<br>
2. The mid-point voltage, which is half of the input voltage, is developed across the center tap of the transformer and is available for use.<br>

<b>During the negative half-cycle mode:</b><br>
1. The thyristor connected to the negative terminal of the bridge rectifier is triggered and conducts current. This allows the negative half-cycle of the AC voltage to flow through the transformer.<br>
2. The same mid-point voltage is developed across the center tap of the transformer and is available for use.<br>

By controlling the triggering angles of the thyristors, the output voltage of the full-wave controlled mid-point converter can be varied. By delaying or advancing the triggering of the thyristors, the conduction angle of the AC voltage can be controlled, thereby controlling the average output voltage. This control enables regulation of the output voltage despite variations in the input voltage.<br>

### **1. Single Phase Full Wave Mid-point Converter - R Load**<br>

<center><img src="images\R load circuit.png" alt="R load circuit" height="250" width="450" style="mix-blend-mode: darken; -webkit-filter:contrast(220%);"></center>
<center><b>Fig. 1 Single Phase Full Wave Mid-point Converter with R Load</b></center><br>

<center><img src="images\R load waveform.png" alt="Input waveform" height="500" width="500" style="mix-blend-mode: darken; -webkit-filter:contrast(120%);"></center>
<center><b>Fig. 2 Waveforms of Single Phase Full Wave Mid-point Converter with R Load</b></center><br>

When terminal A shown in the circuit is positive w.r.t. mid­point N of the transformer secondary, point B will have negative polarity w.r.t. mid-point. Under this condition the thyristor TH<sub>1</sub> conducts when it is fired at an angle α. The waveforms of the load voltage and load current are shown in Fig. 2. The current continues to flow up to angle π radians or 180° when the supply voltage reverses its polarity and thyristor TH<sub>1</sub> gets turned off by natural commutation. During the negative half cycle of ac supply, the terminal B of the transformer secondary is positive w.r.t. to mid-point N. Thyristor TH<sub>2</sub> gets turned on when it is gated. Usually the firing angles for the two thyristors are taken to be equal so as to avoid unequal distribution of load current in the two halves of input cycle. Each half of the input wave is applied across the load. Thus, across the load, there are two pulses of current in the same direction. Hence the ripple frequency across the load is twice that of the input supply frequency. It is clear from Fig. 2 that with pure resistive load, the load current is always discontinuous.<br><br>
The output dc voltage across the resistive load is given by<br>

<center>

$$V_{dc} = \frac {1}{\pi} \int_{\alpha}^{\pi} V_{max}\ sinwt \ dwt$$

</center>

<center>

$$V_{dc} = \frac {V_{max}}{\pi}(1+cos\alpha)..........(1)$$

</center>

The average load current is given by<br>

<center>

$$I_{dc} = \frac {V_{dc}}{R} = \frac {V_{max}}{\pi R}(1+cos\alpha)..........(2)$$

</center>

The rms of output voltage is<br>

<center>

$$V_{o~(rms)} = \left[ \frac {1}{\pi} \int_{0}^{\pi} V_{max}^2 ~ sin^2wt ~ dwt \right]^{1/2}$$

</center>

<center>

$$V_{o~(rms)} = V_{max} \left[ \frac {\pi-\alpha}{2\pi} + \frac {sin2\alpha}{4\pi} \right]^{1/2}..........(3)$$

</center>

The rms of output current is<br>

<center>

$$I_{o~(rms)} = \frac {V_{o~(rms)}}{R} = \frac {V_{max}}{R} \left[ \frac {\pi-\alpha}{2\pi} + \frac {sin2\alpha}{4\pi} \right]^{1/2}..........(4)$$

</center>


### **2. Single Phase Full Wave Mid-point Converter - RL Load**

<center><img src="images\RL load circuit.png" alt="1 phase controlled bridge rectifier" height="250"
            width="500" style="mix-blend-mode: darken; -webkit-filter:contrast(220%);"></center>
        
<center><b style="font-size:18px;">Fig. 3 Single Phase Full Wave Mid-point Converter with RL Load</b></center><br>

<center><img src="images\RL load waveform.png" alt="Input waveform" height="600" width="550" style="mix-blend-mode: darken; -webkit-filter:contrast(120%);"></center>
<center><b style="font-size:18px;">Fig. 4 Waveforms of Single Phase Full Wave Mid-point Converter with RL Load</b></center><br>
In positive half cycle thyristor TH1 conducts when it is fired at an angle α. When ωt = π the cycle reverses and the voltage at terminal A goes negative while at terminal B it goes positive. At this value of angle thyristor TH1 still conducts due to current circulated as a result of decay of energy stored in the inductor. The rate of decay is determined by L/R ratio. When the energy stored in the inductor falls to zero, thyristor TH<sub>1</sub> is turned off and the load current falls to zero value at an angle called extinc­tion angle β. The extinc­tion angle β may be greater than, equal to, or less than the firing angle α depending upon whether the value of in­ductance is more than, equal to or less than the critical value respectively.<br>

<center>

$$V_{dc} = \int_{\alpha}^{\pi+\alpha} V_{max} ~ sinwt ~ dwt$$

</center>

<center>

$$V_{dc} = \frac {2V_{max}}{\pi}cos\alpha..........(5)$$

</center>

Some conclusions may be made from above equation:<br>

1. Output voltage will have the highest value for α = 0.<br>
2. Output voltage will be zero for α = 90°. It means that the output voltage will contain equal positive and negative areas, giving zero output voltage.<br>
3. For firing angle α exceeding 90°, the converter operates in inversion mode. The voltage will be negative maximum for α = 180°.<br>

### **Advantages of Single Phase Full Wave Mid-point Converter**

1. The full wave controlled mid-point converter allows power to flow in both directions, enabling bidirectional energy transfer. This feature is especially useful in applications where power needs to be converted between AC and DC, or where energy needs to be stored and retrieved, such as in energy storage systems or electric vehicle charging.<br>

2. By using a full wave configuration, the mid-point converter can achieve lower input and output current ripple compared to half-wave converters. This results in improved power quality, reduced electromagnetic interference (EMI), and lower stress on connected components.<br>

3. The full wave controlled mid-point converter has a higher efficiency compared to other converter topologies. This is because it utilizes both the positive and negative halves of the input waveform, maximizing the power conversion efficiency.<br>

4. The full wave controlled mid-point converter reduces harmonic distortion in the output waveform. This is beneficial for applications that require a clean and sinusoidal output voltage, such as grid-connected systems or sensitive loads.<br>

5. The mid-point converter provides better voltage regulation capabilities due to its ability to control the output voltage by adjusting the phase angle and duty cycle of the switching devices. This allows for precise control over the output voltage, making it suitable for applications that require tight voltage regulation, such as power supplies or motor drives.<br>

6. The full wave controlled mid-point converter can achieve higher power density and compact size compared to other converter topologies. This is advantageous in applications where space is limited or weight reduction is important, such as in portable devices or electric vehicles.<br>

7. The full wave controlled mid-point converter can be easily interfaced with various control strategies and modulation techniques. It can also accommodate different types of loads, making it a versatile choice for a wide range of applications.<br>

### **Disadvantages of Single Phase Full Wave Mid-point Converter**

1. Compared to simpler converters like half-wave rectifiers, full wave controlled mid-point converters are more complex in terms of circuitry and control algorithms. This complexity can lead to increased costs, design challenges, and potential points of failure.<br>

2. The operation of a full wave controlled mid-point converter involves switching actions that can introduce higher levels of harmonic distortion into the output waveform. This can lead to increased losses, reduced power quality, and potential interference with other sensitive equipment connected to the system.<br>

3. The full wave controlled mid-point converter requires the use of semiconductor devices (such as thyristors or transistors) for switching actions. These devices have finite switching times and can experience switching losses, resulting in reduced efficiency compared to simpler rectifier topologies.<br>

4. The full wave controlled mid-point converter operates with a floating mid-point voltage, which requires careful balancing to ensure that the two output voltages are equal. Any imbalance in the mid-point voltage can lead to uneven voltage sharing between the two output phases, potentially causing issues in connected loads or requiring additional control measures.<br>

5. The full wave controlled mid-point converter is generally suitable for applications where the output voltage is lower than the input voltage. It becomes less efficient and more complex to implement when higher output voltages are required.<br>

6. The control strategy for the full wave controlled mid-point converter can be more challenging compared to simpler converters. The control algorithm needs to manage the switching of multiple semiconductor devices and ensure proper synchronization and voltage balancing, which can increase the complexity of the control system.<br>

### **Applications of Single Phase Full Wave Mid-point Converter**

1. Renewable Energy Systems<br>

2. Energy Storage Systems<br>

3. Microgrids and Islanded Systems<br>

4. Battery Charging Systems<br>

5. Variable Frequency Drives<br>


</div>