### Define und const
* `#define` Dies ersetzt alle Variablen im Code mit dem deklarierten Wert bevor der Code kompiliert wird (spart dadurch RAM). Wird vor allem für pins genutzt.
* `const` Hier wird eine Variable festgelegt die im Code selbst nicht mehr verändert werden kann.
##### Wann define und wann const
Manche Compiler sind schlau genug um zu wissen das const im Code nicht verändert werden können und somit genau wie define, im Code einfach ausgetauscht werden. Das kann dazu führen das define redundant wird. Desweiteren kann der Compiler mit const eventuelle Fehler im Code leichter finden. Folglich ist es Best practice const zu benutzen wenn man den richtigen Compiler hat.

### Andere Variablen
* `int` Normale integer Deklaration
* `bool` Normale boolean Deklaration
*  `float` Normale float Deklaration
*  `unsigned long`Lange int, meistens benutzt für `millis()`