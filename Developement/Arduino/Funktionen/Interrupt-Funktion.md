### Interrupt Funktion

^3971e4

Eine Interrupt-Funktion (auch Interrupt Service Routine oder ISR genannt) ist eine spezielle Funktion in deinem Arduino-Code, die automatisch aufgerufen wird, wenn ein bestimmtes Ereignis auftritt, das als Interrupt bezeichnet wird.

##### Wozu dienen Interrupts?

Interrupts sind nützlich, um auf Ereignisse zu reagieren, die asynchron zum Hauptprogrammablauf auftreten können.

**Beispiele:**

*   Ein Taster wird gedrückt.
*   Ein Sensorwert ändert sich.
*   Daten werden über die serielle Schnittstelle empfangen.
*   Ein Timer läuft ab.

##### Wie funktionieren Interrupts?

1.  **Interrupt-Pin konfigurieren:** Du musst einen bestimmten Pin deines Arduino als Eingang für den Interrupt konfigurieren.
2.  **Interrupt aktivieren:** Mit der Funktion `attachInterrupt()` legst du fest, welcher Pin den Interrupt auslösen soll, welche Funktion bei Auftreten des Interrupts aufgerufen werden soll und unter welcher Bedingung der Interrupt ausgelöst werden soll (z.B. wenn der Pegel am Pin steigt, fällt oder sich ändert).
3.  **Interrupt-Funktion schreiben:** Du schreibst eine spezielle Funktion, die ausgeführt wird, wenn der Interrupt ausgelöst wird.
4.  **Interrupt-Ereignis:** Wenn das konfigurierte Ereignis am Interrupt-Pin eintritt, wird die Ausführung des Hauptprogramms unterbrochen und die Interrupt-Funktion wird ausgeführt.
5.  **Rückkehr zum Hauptprogramm:** Nachdem die Interrupt-Funktion abgearbeitet ist, kehrt die Ausführung zum Hauptprogramm zurück.

##### Wichtige Punkte

*   **Schnelligkeit:** Interrupt-Funktionen sollten so kurz und effizient wie möglich sein, da sie die Ausführung des Hauptprogramms unterbrechen.
*   **Volatile Variablen:** Wenn du in einer Interrupt-Funktion auf Variablen zugreifst, die auch im Hauptprogramm verwendet werden, solltest du diese Variablen als `volatile` deklarieren, um sicherzustellen, dass der Compiler ihre Werte korrekt behandelt.
*   **Vermeidung von `delay()`:** In Interrupt-Funktionen solltest du die Funktion `delay()` vermeiden, da dies die Reaktion auf andere Interrupts verzögern kann.
*   **`Serial.print()` mit Vorsicht:** Die Verwendung von `Serial.print()` in Interrupt-Funktionen kann zu Problemen führen, da die serielle Kommunikation selbst Interrupts verwenden kann.

##### Beispiel

```c++
volatile int buttonState = LOW; // Volatile Variable für den Tasterzustand

void setup() {
  pinMode(2, INPUT_PULLUP); // Taster an Pin 2 mit Pull-Up-Widerstand
  attachInterrupt(digitalPinToInterrupt(2), changeButtonState, FALLING); // Interrupt bei fallender Flanke
  Serial.begin(9600);
}

void loop() {
  Serial.print("Tasterzustand: ");
  Serial.println(buttonState);
  delay(100);
}

void changeButtonState() {
  buttonState = !buttonState; // Tasterzustand ändern
}