# arduino_lcd_thermometor

Arduino project that uses a thermistor to read temperature and displays it on an LCD display.

This project was put together after learning the basics of Arduino and experimenting with circuitry. Other circuits I built included ultrasonic sensors, motors, buzzers, buttons, LEDs, and more. Putting together these simple connections gave me a strong base to build on, and understand the components of circuits that I am building. 

This build was inspired by a tutorial provided by Elegoo. --> https://www.elegoo.com/

Here is a picture of the circuit put together where you can see the thermistor, potentiometer, LCD display, and Arduino Uno Board.

![circuit board](https://github.com/brendanartley/arduino_lcd_thermometor/blob/main/circuit_pic.png)

The code that is uploaded to the board uses the liquid crystal library to write onto the LCD display. The input pin (pin 0) is defined and we set up a liquid crystal object so that we can write text directly to the board. 

In the loop function, we are reading the resistance from the thermistor to determine the temperature. The thermistor changes its resistance based on outside temperature, and we convert this resistance into our temperature of choice. See more about the calculations regarding converting the resistance to temperature (Steinhart-Hart equation) --> [Thermistors](https://www.jameco.com/Jameco/workshop/TechTip/temperature-measurement-ntc-thermistors.html#:~:text=To%20convert%20ADC%20data%20to,it%20to%20find%20the%20temperature.&text=That%20is%2C%20the%20ratio%20of,by%20the%20ADC%20(adcVal).)

Note -- As stated in the article the Steinhart-Hart method is not exact but provides a close approximation of temperature readings. This is partly because the resistance-temperature relationship in the thermistors is not linear.

