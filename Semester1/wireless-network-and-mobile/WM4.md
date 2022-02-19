
# Review of Physical Layer 2
Amazing Resource: 
https://latex.codecogs.com/eqneditor/editor.php
https://latexbase.com/

## Reflection, Diffraction, and Scattering
Receiving power additionalyy influenced by:
**Reflection**: Surface large relative to wavelength of signal.

**Difraction**: Edge of impenetrable body that is large relative to λ. May receive signal even if no **line of sight** (LOS) to transmitter

**Scattering**: wavelength larger than obstacle size, i.e. lamp posts. 

![](attachments/Reflection,%20Scattering,%20Difraction.png)

If there is LOS, diffracted and scattered signals not significant.
If there is no LOS, diffraction and scattering are primary means of reception.

## Multipath Propagation
Signal can take many different paths between sender and receiver due to reflection, diffraction,  and scattering. Fast fading is the negative consequences of this. 

**Fast fading**: waves traveling along different paths may be completely out of phase when they reach the antenna (thereby canceling each other out).
![](attachments/Pasted%20image%2020210909181818.png)

**Delay spread**: time between first and last versions of signal

**Fading**: fluctuation in amplitude, phase, or delay spread

**Inter-symbol interference**
![](attachments/Pasted%20image%2020210909182043.png)
![](attachments/Pasted%20image%2020210909182056.png)

Multipath may add constuctively or destructuvely

## Doppler Shift
If the transmitter or receiver or both are mobile the frequency of received signal changes.
- Moving toward each other increases frequency.
- Moving away each other decreases frequency.

![](attachments/Pasted%20image%2020210909182206.png)

Frequency difference = velocity/Wavelength
![](attachments/Pasted%20image%2020210909182248.png)

## Channel Capacity
Assume the channe is noise free, 
capacity = maximum data rate for a channel

**Nyquist Theorem**: 
Bandwidth = B
Data rate <= 2 B

Bi-level encoding:
![](attachments/Nyquist%20Theorem.png)
![](attachments/CodeCogsEqn%20(1).png)

Multi level: (4 level encoding)
![](attachments/Pasted%20image%2020210909182753.png)
![](attachments/CodeCogsEqn%20(2).png)
![](attachments/CodeCogsEqn%20(3).png)

## Shanon's Theorem
No assumption of noise free
Bandwidth = B Hz
Signal-to-noise ratio = S/N

C = B log2 (1+S/N)
![](attachments/Capacity%20Calculation.png)

dB = 10 log10 S/N

## SNR (Signal to Noise Ratio)
For best performance in a wireless environment, it is key that wireless devices are able to distinguish received signals as legitimate information they should be listening to and ignore any background signals on the spectrum. There is a concept known as the Signal to Noise Ratio or SNR, that ensures the best wireless functionality. 

The SNR is the difference between the received wireless signal and the noise floor. The noise floor is simply erroneous background transmissions that are emitted from either other devices that are too far away for the signal to be intelligible, or by devices that are inadvertently creating interference on the same frequency.

For example, if a client device's radio receives a signal at -75 dBm, and the noise floor is -90 dBm, then the effective SNR is 15 dB. This would then reflect as a signal strength of 15 dB for this wireless connection.
![](attachments/Pasted%20image%2020210910123735.png)

Generally, a signal with an SNR value of 20 dB or more is recommended for data networks where as an SNR value of 25 dB or more is recommended for networks that use voice applications. You can compare SNR requirements vs SNR values:
* 5 dB to 10 dB: no signal.
* 10 dB to 15 dB: very low signal (1 bar); mostly associated; mostly slow.
* 15dB to 25 dB:  low signal (2 bars); always associated; usually fast.
* 25 dB to 40 dB: very good signal (3 - 4 bars); always associated; very fast.
* More than 40 dB: excellent signal (5 bars); always associated; lightening fast.

SNR on noiseless channel
![](attachments/Pasted%20image%2020210910144215.png)

High SNR and low SNR
![](attachments/Pasted%20image%2020210910144131.png)





