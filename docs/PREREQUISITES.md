# PREREQUISITES

> _If you just go connecting random things you are going to blow up your kit!_ :(  Don't do dat.

## Concepts & Glossary
- Digital information is just 0 and 1
    - `on / off`, `true / false`, `HIGH / LOW`
    - `HIGH / LOW` - Put _simply_, is there a voltage on the pin, or not?
- `voltage` - The “pressure” that pushes electricity. Electrical potential. Voltage is provided by a source. Unit: volt (V).
- `current` - The rate of flow of charged particles through an electrical conductor. Determined by the voltage applied and the circuit's resistance, including the `load`. Unit: ampere or amp (A).
- `load` - The device or circuit consuming electrical power by transforming energy into different forms (heat, sound, motion, etc...). Can be modeled as a source of resistance, or thought of as a "black box" that adds resistance to a circuit.
- A `resistor` is a component that limits the flow of electric current.
    - LEDs and push buttons MUST be used with a `resistor` in series, else you're shorting the voltage / power supply to ground.
        - For LEDs, the amount of resistance chosen determines the current (and power) that passes thru the LED.
        - For push buttons, we would ideally have zero current, as we just need to detect a change in voltage.
- Arduino is (basically) C++
- Make sure +/- on power supply aligns with +/- on bread board
    - `+` is RED
    - `-` is BLUE

[FIRST MILESTONE](./milestones/1-MILESTONE.md)

## Cheatsheet

```cpp
//============== PREPROCESSOR MACROS ==============
#include "OtherFile.h"     // Include local header file
#include <LibraryName.h>   // Include external library
#define STATUS_LED_PIN D3  // Substitutes "D3" wherever STATUS_LED_PIN appears
  
//============== ARDUINO PROGRAM FUNCTIONS =============
void setup();  // Runs once at start of execution
void loop();   // Runs forever -- is the program
  
//============== SERIAL COMMUNICATION ==============
// Initialize serial communication
Serial.begin(uint32_t baudRate);         // baudRate: 9600, 115200 etc.
  
// Output to serial monitor
Serial.print(T value);                   // Print value (any type) without newline
Serial.println(T value);                 // Print value (any type) with newline
Serial.printf(const char* format, ...);  // Formatted print (like printf)
  
//============== DIGITAL I/O ==============
// Set pin mode
pinMode(uint8_t pin, uint8_t mode);        // mode: INPUT/OUTPUT
pinMode(BAT_SIGNAL_PIN, OUTPUT);           // Example
  
// Write digital value to pin
digitalWrite(uint8_t pin, uint8_t state);  // state: HIGH/LOW (1/0)
digitalWrite(LED_PIN, HIGH);               // Example
  
// Read digital value from pin
uint8_t digitalRead(uint8_t pin);          // Returns: HIGH or LOW
boolean value = digitalRead(BUTTON_PIN);   // Example
  
//============== TIMING ==============
// Pause program execution
delay(uint32_t milliseconds);  // Blocks code execution
  
//============== INTERRUPTS ==============
// Attach interrupt to a pin
attachInterrupt(
    uint8_t interrupt,      // Use digitalPinToInterrupt(pin) to convert pin number
    void (*ISR)(void),      // Function pointer to Interrupt Service Routine
    uint8_t mode            // mode: RISING, FALLING, CHANGE, LOW, or HIGH
);
  
// Helper function to convert pin number to interrupt number
uint8_t digitalPinToInterrupt(uint8_t pin);
```
## Usable Pins on the MCU Board
[NodeMCU 1.0 usable pins](https://randomnerdtutorials.com/esp8266-pinout-reference-gpios/#table)
