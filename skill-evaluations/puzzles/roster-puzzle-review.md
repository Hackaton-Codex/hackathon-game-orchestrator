# Revisión del puzle de asignación de turnos

**Perfil probado:** `puzzle-design-reviewer`  
**Puzle:** «Relevo con habilitaciones», capítulo 2, en `index.html`  
**Alcance:** revisión estática de reglas, pistas y validador. No se hizo una sesión de navegador ni se modificó el juego.

## Referencias

- `index.html`, objeto `facilityPuzzles.roster`, la vista `showPuzzle` y `answerPuzzle`.
- `PLAN.md`, secciones de disponibilidad de pistas y puzles y pruebas integrales.
- Las inspecciones opcionales del interior: Archivador de solicitudes y Mesa de relevo.

## Objetivo y solución

Asignar una vez a cada persona a Bomba, Muestras y Despacho.

Las pistas disponibles establecen que Paz cubre Bomba; Nicolás no puede tomar muestras y es la única persona que puede cubrir Despacho; Mara no cubre Despacho. La única solución es **Paz → Bomba, Mara → Muestras, Nicolás → Despacho**. Enumeré las seis permutaciones posibles: el validador acepta solo esta.

## Hallazgo principal — feedback incorrecto para varios errores

El formulario permite seleccionar cualquiera de las seis permutaciones, pero una respuesta incorrecta siempre llama `answerPuzzle` con el índice de feedback `1`. Ese texto solo describe una de las opciones incorrectas predefinidas. Por ejemplo:

- **Entrada:** Mara → Bomba, Nicolás → Despacho, Paz → Muestras.
- **Resultado correcto:** rechazarla porque Paz no quedó en Bomba.
- **Feedback actual:** “Nicolás no puede tomar muestras y Mara no cubre despacho”, lo que no corresponde a la entrada realizada.

Esto puede confundir a quien resuelve el puzle y hace que parte del feedback definido en `facilityPuzzles.roster.feedback` no se use. **Prioridad sugerida: media.** Una corrección posible es validar y explicar la primera restricción incumplida; otra es limitar la interfaz a las tres opciones escritas y asociar cada una a su explicación correspondiente.

## Otros puntos

- **Pistas suficientes, pero externas al módulo:** la breve introducción dice que existen tarjetas de habilitación; el formulario solo muestra menús de nombres. La información lógica aparece en dos inspecciones opcionales y la pista del puzle revela la solución completa. Considerar mostrar las habilitaciones dentro del módulo o enlazar claramente las inspecciones antes de jugar.
- **Falta un panel visual de referencia:** el reto trata de asignar personas a puestos, pero se presenta principalmente con menús. Para hacerlo más comprensible y entretenido, mostrar tarjetas de personas con sus habilitaciones junto a estaciones visuales de trabajo, y permitir colocar cada tarjeta en un puesto. La interfaz debe dejar visibles las restricciones que el jugador ya encontró.
- **Pista directa:** “Paz en bomba, Nicolás en despacho, Mara restante” resuelve todo de inmediato. Es accesible y sin penalización; para conservar algo de deducción, se pueden ofrecer niveles de pista, dejando la solución explícita como último nivel.
- **Reintento:** al fallar se ofrecen intentar de nuevo, ver pista o volver a explorar. El código reserva la entrega de evidencia y los cambios de atributos para una respuesta correcta; esta revisión no confirma el flujo en navegador.

## Resultado del perfil

La revisión verificó que la solución prevista es única y encontró una discrepancia reproducible entre el validador y el feedback. También distinguió que la pista opcional completa la información que no está visible en el formulario. La validación de la skill pasó con `quick_validate.py`; la interfaz todavía requiere una prueba interactiva si se decide corregirla.
