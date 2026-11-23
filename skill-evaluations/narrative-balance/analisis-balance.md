# Prueba de perfil: analista de balance

**Referencia:** «Un trazado compartido», `game-rules.js` y estado inicial de `index.html`.  
**Método:** cálculo de 20 decisiones con los efectos implementados, sin cambiar archivos ni ejecutar el flujo del juego. Se consideran las ganancias/pérdidas de cada opción, límite de atributos 0–100, revisiones, semanas y confianza. No se incluyen bonificaciones de atributos por subtramas; las subtramas solo se consideran en confianza para la estrategia mixta indicada.

## Costos implementados por decisión

| Opción | Liderazgo | Socioambiental | Legal | Demora | Revisiones |
| --- | ---: | ---: | ---: | ---: | --- |
| Pausar y verificar (0) | −1 | +2 | +4 | +1 semana | Cierra una pendiente si existe |
| Avanzar con seguimiento (1) | +3 | +4 | −1 | 0 | Abre una pendiente |

Sin subtrama antes de una decisión, la confianza baja 3 puntos. Registrar una subtrama la aumenta 4 y hace que esa decisión no aplique la pérdida de 3.

## Escenarios de 20 decisiones

Inicio: Liderazgo 42, Socioambiental 42, Legal 42, Confianza 65, 0 revisiones, 0 semanas.

| Estrategia | Liderazgo final | Socioambiental final | Legal final | Confianza final | Revisiones | Demora | Lectura |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | --- |
| Siempre pausar, sin subtramas | 22 | 82 | 100 | 5 | 0 | 20 semanas | Liderazgo y confianza quedan bajo el umbral. |
| Siempre avanzar, sin subtramas | 100 | 100 | 22 | 5 | 20 | 0 semanas | Rigor legal y confianza quedan bajo el umbral; se acumulan seguimientos. |
| Alternar avanzar/pausar; 10 subtramas antes de avanzar | 62 | 100 | 72 | 75 | 0 | 10 semanas | Supera los umbrales numéricos; todavía exige 20 evidencias, 20 decisiones y 5 puzles. |

El umbral de cierre es 35 para cada atributo, 45 para Confianza y 20 decisiones/evidencias más 5 puzles. La tabla no presume completados los requisitos de evidencia o puzles.

## Conclusión

Las dos opciones tienen costos claros y ninguna estrategia extrema basta para cumplir los umbrales de atributos. La estrategia mixta equilibra los tres atributos y permite cerrar los seguimientos si se alternan las decisiones; escuchar en subtramas es clave para la confianza. La pausa repetida acumula 20 semanas, así que el costo temporal es alto aunque el rigor suba. No se observa una opción dominante en los efectos numéricos examinados.

**Límite:** esta es una simulación aritmética aislada de los efectos de las decisiones, no un recorrido integral. No modela puzles, evidencias, eventos ambientales, ganancias de atributos de las subtramas ni todos los estados narrativos. Revisar esos factores en una prueba integral.
