* `pinmode(<Pin>, <Output/Input>);`
* [`attachInterrupt(digitalPinToInterrupt(<Pin>), <interupt function>, <Ausführzeitpunkt>);`](Interrupt-Funktion.md#^3971e4)
* `Serial.print(<Wert>);`
* `digitalWrite(<Pin>, <State/Wert>);`
* [`analogWrite(<Pin>, <State/Wert>);`](Board-Things.md#^5b2568) benötigt einen PWM Pin (Gibt PWM-Wert an PWM-Pin aus.)
* `digitalRead(<Pin>)`
* [`analogRead(<Pin>)`](Board-Things.md#^dc7251)benötigt einen PWM Pin (Liest analogen Sensorwert aus.) 

##### Beispiel Setup:
```c++
## Arduino Projekt Template

Dieses Template dient als Grundlage für neue Arduino-Projekte und enthält grundlegende Funktionen und Strukturen.

### Grundstruktur

// Definitions and Constants
#define LED_PIN 13 // Example: Define LED pin
const int SENSOR_PIN = 10; // Example: Define sensor pin

// Global Variables
int sensorValue;

// Setup Function (runs once at the beginning)
void setup() {
  // Pin Modes
  pinMode(LED_PIN, OUTPUT);
  pinMode(SENSOR_PIN, INPUT);

  // Serial Communication (for debugging)
  Serial.begin(9600); // Set baud rate
}

// Loop Function (runs continuously)
void loop() {
  // Read Sensor Value
  sensorValue = analogRead(SENSOR_PIN);

  // Control LED based on Sensor Value
  if (sensorValue > 500) {
    digitalWrite(LED_PIN, HIGH);
  } else {
    digitalWrite(LED_PIN, LOW);
  }

  // Print Sensor Value to Serial Monitor
  Serial.print("Sensor Value: ");
  Serial.println(sensorValue);

  // Delay for stability (optional)
  delay(100);
}

// Interrupt Function (example)
void myInterruptFunction() {
  // Code to be executed when interrupt occurs
}
```