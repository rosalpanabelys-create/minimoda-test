# Práctica clase 01: casos del registro de MiniModa con IA

**Sitio:** https://minimoda-navy.vercel.app/registro

> Así tiene que quedar tu entrega. Reemplazá cada `___tu respuesta aquí___` con lo tuyo.

## 1. Preparación
- Navegador y fecha: ___Chrome, 30 de octubre de 2026___

## 2. Superficie elegida
- Elegí (chat o cowork): ___chat___
- Por qué: ___porque permite interactuar de forma directa y rapida para resolver loa casos paso a paso___

## 3. Preguntas a Gemini
| # | Pregunta | Respuesta (resumen) | ¿Acierto o error/invento? |
|---|----------|---------------------|---------------------------|
| 1 | ¿Qué campos pide el formulario de registro de https://minimoda-navy.vercel.app/registro? | ___Nombre, email, contraseña, confirmar,edad y pais___ | ___Acierto___ |
| 2 | ¿Cuál es el largo mínimo de la contraseña y qué edad se permite? | ___Minimo 8 caracteres para la contraseña y edad entre 13 y 120 años___ | ___Acierto___ |
| 3 | ¿Qué pasa si no acepto los términos? | ___el sistema exige aceptar los terminos y condiciones para permitir completar el registro___ | ___Acierto___ |

- Un acierto: ___Que describió con precisión los campos y validaciones del formulario de MiniModa.___
- Un error o invento: ___Ninguno destacable / Adivinó correctamente las validaciones.___

## 4. Primer modo
- Superficie y modo: ___Chat___
- Prompt de ejemplo:
  ```
  Sos QA. Vamos a probar el registro de https://minimoda-navy.vercel.app/registro
  Campos: nombre, email, contraseña, confirmar contraseña, edad, país y aceptar términos.
  1. Listá las reglas que se ven, los datos válidos e inválidos y los valores límite.
  2. Escribí 6 casos de prueba con: título, precondiciones, pasos con datos concretos,
     resultado esperado, prioridad (high/medium/low) y tipo (functional/negative/boundary).
  No inventes mensajes: si no sabés el texto exacto, marcalo "A VERIFICAR".
  ```
- Qué devolvió: ___El asistente generó los 3 casos de prueba solicitados con título, precondiciones, pasos, datos concretos y resultados esperados siguiendo las reglas del formulario.___

## 5. Otra superficie: comparación en 3 líneas
1. ___El chat responde de forma inmediata y directa, facilitando la iteración rápida paso a paso.___
2. ___La calidad de los casos generados fue muy alta y precisa en cuanto a las validaciones requeridas.___
3. ___No inventó información extra; se mantuvo completamente alineada a las reglas reales del formulario de MiniModa___

## 6. Mis 3 mejores casos (cargados en Qase, proyecto MiniModa)
Formato del título: `Registro: <qué se prueba>`
Captura de la suite en Qase con tus casos: `evidencias/qase-suite-casos.png`

### Caso 1: ___Registrar un nuevo usuario con datos correctos___
- Precondiciones: ___El usuario se encuentra en la página de registro de MiniModa.___
- Pasos: ___Ingresar un nombre valido en el campo Nombre. Ingresar un correo electrónico válido en el campo Email (ana.prueba@example.com).Ingresar una contraseña válida de al menos 8 caracteres y repetirla en Confirmar contraseña.Ingresar una edad dentro del rango permitido (ej. "22") y seleccionar un país del menú desplegable.
Marcar la casilla Acepto los términos y condiciones y hacer clic en el botón Crear cuenta.___
- Resultado esperado: ___El sistema muestra un mensaje de éxito indicando "¡Registro exitoso!..." y da la bienvenida al usuario.___
- Evidencia: `https://app.qase.io/project/MINIMODA?previewMode=side&suite=0&case=1`

### Caso 2: ___Validar que el sistema rechace contraseñas menores a 8 caracteres___
- Precondiciones: ___El usuario se encuentra en la página de Registro de MiniModa y no ha iniciado sesión previamente.___
- Pasos: ___Completar el formulario de registro con datos válidos. Ingresar una contraseña de menos de 8 caracteres (por ejemplo: 12345). Hacer clic en el botón Crear cuenta.___
- Resultado esperado: ___El sistema muestra un mensaje de advertencia indicando que la contraseña requiere un mínimo de 8 caracteres y no permite completar el registro.___
- Evidencia:`https://app.qase.io/project/MINIMODA?previewMode=side&suite=0&case=3`

### Caso 3: ___Validar los límites permitidos en el campo de edad (13 a 120 años)___
- Precondiciones: ___El usuario se encuentra en la página de registro de MiniModa___
- Pasos: ___Completar los campos obligatorios del formulario con datos válidos.
En el campo Edad, ingresar un número fuera del rango permitido (por ejemplo, escribir 12 o 121). Hacer clic en el botón crear cuenta___
- Resultado esperado: ___El sistema no permite avanzar con el registro y muestra una advertencia indicando que la edad debe estar dentro del rango válido establecido (entre 13 y 120).___
- Evidencia: `https://app.qase.io/project/MINIMODA?previewMode=side&suite=0&case=4`

## 7. Mapa del harness
| Pieza | En lo que usé |
|-------|---------------|
| Modelo | ___Gemini___ |
| App | ___Google Chrome (navegador)___ |
| Harness | ___Interfaz Web de GitHub y Chat___ |
| MCP | ___N/A (Interfaz Web nativa)___ |
| Skill | ___Asistencia técnica y QA___ |

## 8. Entrega
- Link de tu repo (pegalo también en el Telegram): ___https://github.com/rosalpanabelys-create/minimoda-test/edit/main/clase-01/practica.md___
