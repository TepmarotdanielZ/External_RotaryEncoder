## 1. Enoder Sensor

A rotary encoder is a type of position sensor which is used for determining the angular position of a rotating shaft it generates an electrical signal either analog or digital according to the rotation movement there are many different type of rotary encoders which are classified by either output signal or sensing technology the particular rotary encoder that we will use is incremental rotary encoder and it’s the simplest position sensor to measure rotation this rotary encoder is also known as quadrature encoder or relative rotary encoder and its output is a series of square wave pulse let’s take a closer look at the encoder and see its working principle. How the square wave pulses ate generated the encoder has a disk with evenly spaced contact zones that are connected to the common pin C and two other separate contact pins A and B as illustrated now when the disk will start rotating step by step the pins A and B will start making contact with common pin and the two square wave output signals will be generated accordingly any of the two output pins can be used for determining the rotation position it we just count the pulse of the signal however it we want to determine the rotation direction as well we need to consider both signals at the same time we can notice that the two output signals are displaced tat 90° degrees out of phase from each other it the encoder is rotating clockwise the output a will be ahead of the output B so if we count the steps each time the signal changes from high to low or from low to high we can notice that at that time the two output signals have opposite value vice versa if the encoder is rotating counterclockwise the output signals have equal values so considering this we can easily program our controller to read the encoder position and rotation direction that’s the basic working principle of our rotary encoder .

![image](https://github.com/TepmarotdanielZ/External_RotaryEncoder/assets/139426571/54b10069-5586-41c0-8295-7b2625eae4ef)

This HN3806 incremental Two phases encoder is an two-phase, incremental rotary encoder, which can used for detecting and measuring the position or rotation speed of an object, according to its degree angle locomotion. This incremental encoder converts the angular position of its rotor to a series (AB two-phase) of square waves, by utilizing a rotating grating disk and optocoupler. It can be used for detecting and measuring the angle, speed, length, and acceleration of the desired objects, which is useful for smart controlling of any displacement and fixed-length in CNC machine, motor feedback and any closed-loop control systems.

![image](https://github.com/TepmarotdanielZ/External_RotaryEncoder/assets/139426571/46907905-e12d-4a52-b645-5853a1c17646)

  This is the specification of HN3806.
  • Model: HN3806
  • Pulse Number:600 (Optional)
  • Power source: DC 5-25V
  • Shaft diameter: 6mm
  • Output diameter: 38mm
  • Output: AB 2phase output rectangle orthogonal pulse circuit, the output for the NPN open-collector output type
  • Maximum mechanical speed: 5000R/min
  • Response frequency: 30khz
  • Cable length: 2 meters

## 2. Read Encoder

To get value from two encoder and publisher data every 10ms we use two timer and timer interrupt execute every 10ms, we use timer 3 and timer 4 both timer on AHBP1 have source clock 90Mhz and timer five is timer interrupts. Timer five have source on AHBP1 have source clock 90Mhz,

• General formula calculations timer for execute:

By apply to Equation 1 we get f = 90(83 + 1) (999 + 1) = 100 hz

𝑇 = 1𝑓

𝑇 = 1100 = 0.01𝑠 = 10𝑚𝑠


