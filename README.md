# ECE387-BusAssignment

##Background
The bus assignment describes a scenario in which a central microcontroller is responsible for transmitting a coordinated RGB signal to 9 external local controllers. Each of these external controllers are responsible for coordinating the color of 9 RGB LEDs (each requiring three bits of information for RGB values).

##Problem Statement
A problem arises when transmitting the signals to each external controller, which are spread out over significant distance. Transmissions across wires of this length are susceptible to substantial noise. To mitigate losses, the power and ground wires should be arranged in a "twisted pair" formation. In this configuration, magnetic flux through each twisted loop cancels with one another, helping minimize the amount of external noise affecting the transmitted signal.

##Protocol
To utilize these two pairs successfully, the I2C protocol should be used (which supports up to 3.2MBps), more than capable of supporting the data transmission required to control all LEDs without introducing extra wires.

##Cost
Shift Registers (x9) - PN: MC74HC595ADTR2G @ $0.42/unit = $3.78
LEDs (x81) - PN: OVS5MBBCR4 (Surface mounted component) @ $0.41/unit = $33.21
Arduino Uno Unit - @$24.00/unit = $24.00
Assuming negligible cost for wires

**Total Cost: $60.99**

![Bus Drawing](https://github.com/demusjc/ECE387-BusAssignment/blob/master/Bus.jpg)
