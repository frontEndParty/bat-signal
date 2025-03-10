# **Prerequisite Info**  

## **Concepts & Glossary**  
- **Digital signals** are just **0 and 1** — **on/off**, **true/false**, **HIGH/LOW**.  
  - **HIGH / LOW:** Simply put, **on/off**. HIGH means there's voltage; LOW means there isn’t.  
- **Voltage is supplied** by a power source; **current is drawn** by the connected components (the load).  
- **Resistors are required** in series with LEDs and push buttons:  
  - **LEDs:** The resistor controls the current flowing through the LED.  
  - **Push buttons:** Ideally, minimal current flows; we just need to detect a voltage change.  
- **Arduino code is basically C++.**  
- **Incorrect wiring = fried components.** Double-check before connecting!  
- **Breadboard wiring:**  
  - **Power (+) is RED**  
  - **Ground (-) is BLUE**  
  - Ensure **+/- from the power supply matches +/- on the breadboard**.  

---  

## **Cheat Sheet**  

### **Preprocessor Macros**  
```cpp
#include "OtherFile.h"     // Include a local header file  
#include <LibraryName.h>   // Include an external library  
#define MAX_SENSORS 5      // Define constants  
```  

### **Arduino Program Structure**  
```cpp
void setup();  // Runs once at startup  
void loop();   // Runs continuously after setup  
```  

### **Serial Communication**  
```cpp
Serial.begin(9600);        // Initialize serial communication  
Serial.print("Hello");      // Print without newline  
Serial.println("World");    // Print with newline  
Serial.printf("Value: %d", 42);  // Formatted output  
```  

### **Digital I/O**  
```cpp
pinMode(LED_PIN, OUTPUT);       // Set pin as input/output  
digitalWrite(LED_PIN, HIGH);    // Set pin HIGH (on) or LOW (off)  
bool value = digitalRead(BUTTON_PIN);  // Read pin state  
```  

### **Timing**  
```cpp
delay(1000);  // Pause execution for 1000ms (1 second)  
```  

### **Interrupts**  
```cpp
attachInterrupt(digitalPinToInterrupt(PIN), ISR_function, RISING);  
```  

---

## **Usable Pins on the MCU**  
Check out this handy **[NodeMCU 1.0 pin reference](https://randomnerdtutorials.com/esp8266-pinout-reference-gpios/#table).**