Using LED As A Light Sensor

Description
This circuit shows how to use an ordinary LED as a light sensor. It makes use of the photovoltaic voltage developed across the LED when it is exposed to light. LEDs are cheaper than photodiodes and come with a built-in filter, which is useful when the application involves colour discrimination. The photo-voltage of a red LED (its bandgap voltage) is typically about 2V. The source impedance of this voltage is about 800MΩ in daylight, rising to infinity in darkness. A TL071 JFET input op amp is used to amplify and buffer this extremely high impedance signal.

Circuit diagram:
Using LED As A Light Sensor-Circuit diagram
![image](https://github.com/user-attachments/assets/3e6cc32c-facc-43a2-81eb-2268ed51d81a)

Resistor R1 ensures that the op amp "sees" a 0V input when the LED is in total darkness. To avoid undue loading of the signal, R1 would ideally be a 100MΩ or larger resistor but since such high values are rare and expensive I used a smaller value and increased the gain of the op amp to compensate for the voltage loss. To avoid the need for a second variable resistor to set the op amp’s input offset to zero, R1 must be large enough for the reduced voltage across the LED to swamp the op amp’s input offset voltage. With a 30MΩ resistor for R1, the voltage at the op amp input when the LED is exposed to bright light is reduced to about 60mV.

This is just over four times the 13mV maximum input offset of the TL071 op amp. R1 can be three 10MΩ resistors in series. Alternatively, I have found that a reverse-biased 1N4148 diode has an impedance of about 30MΩ (connect it in the circuit with the anode to ground). The output of the circuit is about 0V when the LED is in darkness. VR1 sets the gain of the op amp and it should be adjusted to give the required output voltage when the LED is exposed to bright light.
