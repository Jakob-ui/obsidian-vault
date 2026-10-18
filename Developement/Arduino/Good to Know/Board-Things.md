### PWM (Pulsweitenmodulation)

Ein digitales Signal wird verwendet, um die Leistung zu steuern, die an ein Gerät abgegeben wird. Dies geschieht durch sehr schnelles Ein- und Ausschalten des Signals. Stell dir einen Wasserhahn vor. Wenn du ihn voll aufdrehst, fließt viel Wasser (hohe Leistung). Wenn du ihn nur ein bisschen aufdrehst, fließt wenig Wasser (niedrige Leistung). PWM ist wie ein Wasserhahn, der sehr schnell auf und zu gedreht wird. Je länger der Hahn auf ist, desto mehr Wasser fließt (höhere Leistung).
##### Übersicht
*   **Zweck:** Steuerung von Helligkeit/Geschwindigkeit durch variable digitale Signale.
*   **Funktionsweise:** 
	* analogRead() -> Wandelt Spannung in digitalen Wert (0-1023) um. ^dc7251
	* analogWrite() -> Erzeugt PWM-Signal mit entsprechendem Tastverhältnis (0-255). ^5b2568
*   **Vorteile:** Einfache Steuerung ohne komplexe Schaltungen.
*   **Hinweis:** Nicht alle Pins sind PWM-fähig (~).
*   Anwendungsbeispiele:
	* **LED-Dimmer:** Durch Ändern des Tastverhältnisses kann die Helligkeit einer LED stufenlos eingestellt werden. 
	* **Motorsteuerung:** Mit PWM kann die Drehzahl eines Motors präzise gesteuert werden. 
	* **Audio:** PWM wird in einigen Audioverstärkern verwendet, um Audiosignale zu erzeugen.