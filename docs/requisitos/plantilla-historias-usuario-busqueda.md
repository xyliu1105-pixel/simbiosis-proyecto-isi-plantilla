# Historias de usuario de búsqueda

| Campo | Valor |
| --- | --- |
| Proyecto | Proyecto Simbiosis |
| Fecha | [27/10/2026] |
| Versión | [1.0] |
| Estado | Borrador |

## Fuentes comunes

- [Acta de UC-21 Buscar recetas](../captura/acta-acuerdos-uc-21-buscar-recetas.md), v1.1, Vigente.
- [Catálogo de requisitos](catalogo-requisitos.md), UR-08 y FR pertinentes.
- [Modelo de casos de uso](../modelos/modelo-casos-de-uso.md), UC-21.

## Épica de búsqueda

Como persona usuaria registrada, quiero buscar recetas por término de texto, por ingredientes incluidos o por ingredientes excluidos, para encontrar preparaciones culinarias ajustadas a mis gustos y restricciones alimentarias.

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta.

## Justificación de la división

Dividimos la épica en tres historias independientes porque cada una cubre una capacidad de búsqueda funcional específica que aporta un valor diferenciado por sí misma. Esto permite que una persona busque solo por texto, busque aprovechando sus ingredientes disponibles o filtre alimentos que desea evitar, ofreciendo un resultado útil en cualquiera de los tres casos sin obligar a implementar el conjunto completo desde el inicio. 

## US-01

**Título:** Búsqueda por palabra o frase libre

Como persona usuaria registrada, quiero buscar recetas mediante una palabra o frase, para localizar preparaciones que contengan dicho texto en su título o descripción.

**Fuentes:** UR-08; UC-21; FR-085; acta, apartado 2.

### Criterios de aceptación

- **CA-01.** Dado que existen las recetas publicadas "Ensalada de pasta" y "Pasta al pesto", cuando la persona usuaria busca la frase "pasta al pesto", entonces el sistema muestra únicamente "Pasta al pesto" en los resultados.
- **CA-02.** Dado que existen las recetas publicadas "Tarta de Manzana" y "Sopa de verdura", cuando la persona usuaria busca el texto "manzana", entonces el sistema devuelve "Tarta de Manzana" ignorando las mayúsculas y las tildes.
- **CA-03.** Dado que no existe ninguna receta publicada con el término "quinoa", cuando la persona usuaria busca "quinoa", entonces el sistema indica que no hay resultados para esa búsqueda y propone una corrección u opción alternativa.

## US-02

**Título:** Búsqueda por ingredientes incluidos

Como persona usuaria registrada, quiero buscar recetas seleccionando ingredientes que deseo añadir, para encontrar platos que aprovechen los alimentos de los que dispongo.

**Fuentes:** UR-08; UC-21; FR-086; acta, apartado 2.

### Criterios de aceptación

- **CA-01.** Dado que la receta "Arroz al horno" contiene "arroz" y "tomate", y la receta "Ensalada" solo contiene "tomate", cuando la persona usuaria selecciona incluir "arroz" y "tomate", entonces el sistema muestra en los resultados únicamente "Arroz al horno" por cumplir la inclusión de todos los ingredientes seleccionados.
- **CA-02.** Dado que existen recetas con el ingrediente "lentejas", cuando la persona usuaria selecciona únicamente el ingrediente "lentejas" y ejecuta la búsqueda, entonces el sistema muestra el listado de recetas que contienen dicho ingrediente ordenadas por fecha de publicación.
- **CA-03.** Dado que no existen recetas validadas que contengan conjuntamente "aguacate" y "garbanzos", cuando la persona busca ambos ingredientes incluidos, entonces el sistema indica que no hay resultados y sugiere alternativas conservando los criterios seleccionados.

## US-03

**Título:** Búsqueda por exclusión de ingredientes y búsqueda combinada

Como [rol], quiero [capacidad], para [beneficio].

**Fuentes:** UR-08; UC-21; [FR principal]; acta, [apartado pertinente].

### Criterios de aceptación

- **CA-01.** Dado [situación], cuando [acción], entonces [resultado observable].
- **CA-02.** Dado [situación], cuando [acción], entonces [resultado observable].
- **CA-03.** Dado [situación], cuando [acción], entonces [resultado observable].

## Revisión INVEST

La revisión abarca US-01, US-02 y US-03. «Aplicado» indica si se ha realizado la comprobación. «Cumple» indica si todas las historias cumplen el criterio. Si alguna no lo cumple, indicar «No» e identificar la historia y el motivo en la justificación. Si no se ha realizado la comprobación o faltan datos, indicar «Pendiente» en «Cumple».

| Criterio | Pregunta de revisión | Aplicado | Cumple | Justificación |
| --- | --- | --- | --- | --- |
| Independiente | ¿Puede implementarse cada historia y ofrecer un resultado útil sin implementar antes las otras historias del conjunto? Puede compartir infraestructura con ellas. | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Negociable | ¿Cada historia explica qué necesita la persona y deja margen para discutir los detalles de la solución, respetando los acuerdos confirmados? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Valiosa | ¿La parte «para…» de cada historia explica el beneficio que obtiene la persona al usar esa capacidad? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Estimable | ¿Están claros el alcance y los datos necesarios para estimar el trabajo de cada historia? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Pequeña | ¿Se centra cada historia en una única capacidad de alcance manejable? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Comprobable | ¿Los criterios de aceptación de cada historia describen acciones y resultados observables que permiten distinguir un comportamiento correcto de uno incorrecto? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |

## Dudas pendientes

[Cuestiones pendientes de aclaración. Si no quedan cuestiones, indicar «Ninguna».]
