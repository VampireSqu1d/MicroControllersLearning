# arduinoLearning

A collection of small **Arduino learning sketches** (each folder is its own project) covering LEDs, buttons, debouncing, timing without `delay()`, analog input, EEPROM, interrupts, serial communication, LCDs, and an ultrasonic distance sensor.

## What’s in this repo

Each directory contains a standalone `.ino` you can open and upload from the Arduino IDE.

- **`arduinoLEDs/`**: basic LED outputs and blinking
- **`button_statePIN_2/`**: reading a push button on digital pin 2
- **`DebouncePushButton/`**: debounced button input + LED toggling (`DebounceLEDsToggle`)
- **`eeprom/`**: storing a max brightness value in EEPROM and using it as a clamp
- **`fade_LED11/`** and **`pwdLED11/`**: PWM LED fading / brightness control
- **`Interupts/`**: interrupt-driven examples
- **`LCDDisplay/`**:
  - `LCD_display`: show text on a 16x2 LCD over Serial (includes a `clear` command)
  - `LCD_UltrasonicSensor`: display HC-SR04 distance on a 16x2 LCD
- **`potenciometer_Read_A2/`** and **`potenciometer_controlled_LED/`**: reading analog input and controlling LED intensity
- **`powerLEDonButtonPress/`**: turn an LED on while a button is pressed
- **`serial_communication/`**:
  - `serial_communication`: basic Serial IO
  - `Serial_communication_no_delay`: non-blocking style Serial handling
  - `Multitasking`: multiple time-based actions in one loop (no `delay()`)
- **`stoplight_LEDs/`** and **`stoplight_LEDs_with_button/`**: “traffic light” sequences, including button interaction
- **`UltrasonicSensor/`**: HC-SR04 distance measurement using an interrupt + simple filtering and LED feedback

## Requirements

- **Arduino IDE** (or Arduino CLI + your preferred editor)
- **A compatible board** (these sketches are written in “classic Arduino” style and are a good fit for Arduino Uno/Nano-class boards)
- **Common parts** (depending on the sketch):
  - LEDs + resistors
  - push buttons
  - potentiometer
  - 16x2 character LCD (HD44780-compatible)
  - HC-SR04 ultrasonic distance sensor

## Libraries used

- **`LiquidCrystal`** (ships with the Arduino IDE) for the LCD sketches
- **`EEPROM`** (ships with the Arduino IDE) for the EEPROM sketch

## How to run a sketch (Arduino IDE)

1. Open the Arduino IDE.
2. Use **File → Open…** and select the `.ino` inside the sketch folder you want.
3. Choose your **Board** and **Port**.
4. Click **Upload**.

## Serial monitor notes

Several sketches use:

- **baud rate**: `115200`

If a sketch reads text/values from Serial, open the Serial Monitor, set the baud rate to `115200`, and send input as described by that sketch (for example, `LCD_display` accepts `clear` to clear the screen).
