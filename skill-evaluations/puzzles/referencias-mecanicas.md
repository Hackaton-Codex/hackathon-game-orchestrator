# Referencias de diseño de puzles

**Propósito:** reunir patrones de juegos conocidos como nociones generales para futuras pruebas. Maite es un caso de estudio que ayuda a ver oportunidades; no se asume que su género, arte, tono o interfaz se usarán en la hackathon. Las propuestas son inspiraciones, no decisiones de implementación ni copia de contenido.

## Referencias

### Blue Prince — pistas repartidas entre espacios

La página oficial describe una mansión cuyas salas cambian, donde elegir cada habitación afecta la ruta; los objetos pueden ayudar a explorar más y la investigación narrativa se despliega bajo el objetivo visible.

- Fuente: [Blue Prince en Steam](https://store.steampowered.com/app/1569580/Blue_Prince/).
- **Adaptación posible:** conectar dos o tres pistas de distintas instalaciones en un tablero del diario. Una pista puede cambiar cómo se interpreta otra; el jugador conserva notas entre visitas.
- **Ajuste al proyecto:** tomar el descubrimiento cruzado, no el reinicio diario o el mapa aleatorio, que añadirían complejidad y cambiarían el flujo actual.

### Professor Layton — retos breves, variados y con pistas escalonadas

Nintendo describe una aventura de misterio que intercala muchos puzles pequeños de lógica, lenguaje, espacio y matemática; el jugador explora lugares y conversa para encontrarlos. Los manuales oficiales describen pistas comprables, volver más tarde, deshacer y reiniciar ciertos retos.

- Fuentes: [guía de Nintendo de la serie](https://www.nintendo.com/en-gb/News/2011/The-Beginners-Guide-to-the-Professor-Layton-Games-253601.html) y [manual oficial de Miracle Mask](https://csassets.nintendo.com/noaext/image/private/t_KA_PDF/3DS_Professor_Layton_Miracle_Mask_single_sheet_fr?_a=DATC1RAAZAA0).
- **Adaptación posible:** conservar los puzles opcionales como descubrimientos del entorno; dar una pista en tres etapas: observación, deducción y solución casi explícita. Mantener el uso de pistas y reintentos sin penalización si se quiere priorizar accesibilidad.
- **Ajuste al proyecto:** evitar una moneda de pistas si no hay una economía que la justifique. Las pistas ya pueden ser objetos y conversaciones opcionales.

### The Witness — enseñar una regla y combinarla gradualmente

Su descripción oficial presenta una isla explorable con muchas ubicaciones y puzles, cada uno con una idea nueva.

- Fuente: [The Witness en Steam](https://store.steampowered.com/app/210970/The_Witness/).
- **Adaptación posible:** introducir una sola regla visual por sector, dar un ejemplo seguro y después combinarla con una segunda regla. Puede inspirar el trazado de una ruta segura o la lectura de un esquema sin una explicación larga.
- **Ajuste al proyecto:** no esconder información esencial en un código visual sin enseñar antes cómo leerlo.

### Return of the Obra Dinn — observación y deducción de escenas

La página oficial lo define como una aventura de misterio en primera persona basada en exploración y deducción lógica.

- Fuente: [Return of the Obra Dinn en Steam](https://store.steampowered.com/app/653530/Return_of_the_Obra_Dinn/).
- **Adaptación posible:** reconstruir una secuencia de hechos a partir de varios registros: quién estuvo de turno, cuándo cambió la ruta y qué medición lo respalda.
- **Ajuste al proyecto:** presentar conclusiones como “confirmada”, “pendiente” o “contradictoria”; no convertir una inferencia del puzle en una acusación o conclusión legal definitiva.

### The Case of the Golden Idol — completar una deducción estructurada

La página oficial pide observar las escenas y reconstruirlas mediante deducciones sobre participantes, motivos y herramientas.

- Fuente: [The Case of the Golden Idol en Steam](https://store.steampowered.com/app/1677770/The_Case_of_the_Golden_Idol/).
- **Adaptación posible:** un tablero de informe donde el jugador conecte personas, hora, ubicación y evidencia para completar una conclusión revisable.
- **Ajuste al proyecto:** validar cada relación con una pista localizable y permitir volver a revisar la evidencia; evitar depender de una sola pista diminuta.

## Nociones de diseño transferibles

1. **Representación a la medida de la acción.** Si la persona ordena, asigna, conecta o cambia estados, mostrar esos elementos en un formato que pueda leer y manipular: tarjetas, tabla, diagrama, mapa o panel. Para acertijos verbales, otra forma puede ser más clara. No imponer una estética ni una interfaz universal.
2. **Pistas y feedback informativos.** Escalonar la ayuda desde una observación hasta una deducción y, al final, una solución. Explicar el error según lo que la persona ingresó, no con un mensaje genérico.
3. **Deducción con evidencia rastreable.** Hacer que cada conclusión pueda vincularse a una o más pistas; separar lo observado, lo inferido y lo que sigue abierto.
4. **Progresión de reglas.** Enseñar una regla con un ejemplo seguro, después pedir que se aplique y finalmente combinarla con otra.

## Ejemplos del caso de estudio Maite

- El puzle de bloqueo podría mostrar una consola esquemática con estados visibles para que el orden tenga consecuencias en pantalla; es solo un ejemplo de representación para un reto de secuencia.
- El puzle de turnos podría usar tarjetas de personas y puestos con habilitaciones a la vista; es solo un ejemplo de representación para un reto de asignación.
- La idea de conectar varias fuentes en un tablero puede llevarse a una aventura de investigación, pero no es necesaria en todos los géneros.

## Contexto del proyecto

Maite ya contiene cinco modos: secuencia, asignación, calibración numérica, selección de circuito y orden de muestreo. Para ese caso específico, conviene mejorar primero la representación y el feedback de dos puzles. Esa observación sirve para probar el skill; no limita el tipo de juego ni las mecánicas de la hackathon.
