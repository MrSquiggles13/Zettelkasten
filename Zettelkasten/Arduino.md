20260406-0312
# Arduino

## Notes

A multifunctional programmable circuit board that uses an ATmega microcontroller and multiple pins to connect other components. The programming language is a subset to C++ and can utilize a lot of its features. There are two main functions for Arduino which are:
	1. setup(): This initializes and instantiates any objects or variables needed throughout the program
	2. loop(): Where signals are read and calculations are performed

There are also commonly used functions:
	1. pinMode(pinNumber, INPUT/OUTPUT) - Sets selected pin to either receive or send signals
	2. digitalRead(pinNumber) - Reads the voltage on a pin and gets either HIGH (5 volts) or LOW (0 volts)
	3. digitalWrite(pinNumber, HIGH/LOW) - Sends either a HIGH (5 volts) or LOW (0 volts) signal to selected pin
	4. analogRead(pinNumber) - Reads a variable voltage measured from 0 (0 volts) - 1023 (5 volts) only on pins A0-A5
	5. analogWrite(pinNumber) - Sends a variable voltage only on Pulse Width Modulation pins (denoted by a ~) and has a vaule from 0 (0 volts) - 255 (5 volts)
There are plenty of other functions and libraries for more functionality.

![[Pasted image 20260406035315.png|364]]
The signals that are read and written come in two forms but have many variations and classifications:
	1. Analog Signals - Variable voltage readings that have a continuous range
	2. Digital Signals - Stepped or incremental values that are discrete and normally pulsated through increments of time
	3. Binary Signals - A type of digital signal that has only 2 states

![[Pasted image 20260406035436.png|186]]
Digital signals mimic analog output by utilizing Pulse Width Modulation. This is when digital signals mimic analog output by fluctuating in a wave pattern their stepped signals consistently. This is done so fast that it is able to mimic voltage values in between the digital signals increments.

---
## Links

- [[Electrical Components]]
---

## Source

- 