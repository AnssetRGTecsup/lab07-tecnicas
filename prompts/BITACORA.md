# Bitacora de tecnicas avanzadas
Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: Chat GPT - 5

## Ejercicio 2: Zero-shot, one-shot y few-shot
| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) |
|------|-----------------|-------------------------|------------------------------------|
| Zero-shot | 5 | Tabulación con valores Positivo, Negativo, Neutral | Sí |
| One-shot | 5 | Lista con valores Positivo, Negativo, Neutral| Sí |
| Few-shot | 5 | Asignar con valores Positivo, Negativo, Neutral| Sí|

## Ejercicio 3: Chain of Thought
| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
|--------|--------------------|---------------------------|------------------|
| Directo | 318.60 | No | Sí|
| Paso a paso | 318.60 (con secuencia de pasos)| Sí | Sí|

## Ejercicio 4: Role prompting
| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas |
|---------|-------------------------------|-----------------------|----------------------|
| A. Sin rol | Sencillo | Ambos | Publico general |
| B. Rol docente | Técnico didáctico| Ambos | Estudiantil|
| C. Rol senior | Técnico | Código | Profesional |

## Ejercicio 5: Descomposicion
Registrar en la bitácora una línea por paso indicando qué te entregó la IA y una línea comparando el
resultado con el pedido de una sola vez.

* Simlpe Prompt: La IA devuelve una respuesta general con una estructura básica de clases para luego ser evidecniado en un código de Java todo en una misma respuesta
* Descomposition prompt:
 * Lista 5 requisitos con sus detalles y objetivos
 * Diseña las clases con sus atributos
 * Escribe los códigos en java utilizndo las clases
 * Revisa y sugiere 3 mejoras concretas

## Ejercicio 6: Prompt estructurado y autocritica
```text
<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea
despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada,
resultado esperado.</formato>

Revisa tu tabla: faltan casos limite como campos vacios, correo sin @ o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```
