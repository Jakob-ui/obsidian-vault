### millis() Funktion

*   **Zweck:** Gibt die Anzahl der Millisekunden seit Programmstart zurück.
*   **Vorteil:** Ermöglicht nicht-blockierende Zeitmessung (im Gegensatz zu `delay()`).
*   **Rückgabewert:** [`unsigned long`](Datatypes.md#^4e6c8b) (Millisekunden).

##### Timer mit millis() erstellen

1.  **Variablen:**
    ```c++
    unsigned long previousMillis = 0;
    const long interval = 1000; // Intervall in ms
    ```

2.  **loop() Funktion:**
    ```c++
    void loop() {
      unsigned long currentMillis = millis();

      if (currentMillis - previousMillis >= interval) {
        previousMillis = currentMillis;

        // Code hier ausführen
      }
    }
    ```

##### Erklärung

*   `previousMillis`: Speichert letzte Ereigniszeit.
*   `interval`: Gewünschtes Zeitintervall.
*   `loop()`: Überprüft regelmäßig, ob das Intervall abgelaufen ist.