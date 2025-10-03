# Arduino-Thermostat

This project is a simple weather station/thermostat made using a Arduino Mega 2560 on a prototyping board.

As of the purpose of this project was showcasing the use of baremetal programming, register manipulation and hone my soldering skills.

The Arduino Mega board uses its ADC circuits to read the voltage of a NTC resistor, coupled to a voltage divider circuit. The setting of the ADC is done by setting the bits of the ADMUX and ADCSRA registers. The read information is displayed on a 4-digit, 7-segment display.

The circuit features two modes for the user to access, using two buttons. One mode will show the current temperature read by the sensor the the other will allow the user to set a desired temperature. If the desired temperature is below the current one
an blue LED will activate signaling cooling mode and the fan will turn on. If the desired temperature is above the current one a red LED will activate signaling heating mode.

There was also an attempt of implementing a third mode in which the Arduino would read the RPM of the fan using a Hall Effect sensor and a magnet but incompatibility of components such as the non variable speed fan and the limiting factor of using interrupts to calculate the speed lead to the third mode to be scraped.
