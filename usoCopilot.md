# Manual de uso: Microsoft Teams con Copilot

**Versión:** 1.0  
**Autor:** Alejandro / Equipo TI  
**Objetivo:** Manual práctico y sencillo para que usuarios no tan habilidosos aprendan a usar Copilot en Teams en su trabajo diario. Incluye ejemplos paso a paso y capturas simuladas para facilitar la comprensión.

---

## Índice
1. Introducción rápida
2. ¿Qué es Copilot en Teams?
3. Cómo acceder a Copilot (escritorio y móvil)
4. Usos principales y ejemplos paso a paso
   - 4.1 En reuniones (resumen, actas, tareas)
   - 4.2 En chats y canales (responder, resumir, buscar)
   - 4.3 En archivos (resumen de documentos, extracción de datos)
5. Ejemplos prácticos (plantillas y prompts listos para copiar)
6. Capturas simuladas (UI simplificada)
7. Buenas prácticas y recomendaciones
8. Problemas comunes y soluciones rápidas
9. Plantillas de prompts para copiar y usar
10. Checklist de adopción para administradores
11. Anexos y contactos de soporte

---

## 1. Introducción rápida
Este manual está pensado para que cualquier persona, sin grandes conocimientos técnicos, pueda usar Copilot dentro de Microsoft Teams para ahorrar tiempo: generar resúmenes, redactar correos o actas, extraer tareas, y comprender documentos complejos.

**Cómo usar este manual:**
- Sigue los pasos numerados en cada ejemplo.  
- Copia los *prompts* (las instrucciones que damos a Copilot) y pégalos directamente en la caja de texto de Copilot.  
- Revisa siempre la respuesta de Copilot antes de enviarla o compartirla.

---

## 2. ¿Qué es Copilot en Teams?
Copilot es una herramienta de IA integrada en Teams que te ayuda a resumir, redactar, presentar y buscar información dentro de tus reuniones, chats y archivos. Piensa en Copilot como un asistente que entiende texto y audios (en reuniones) para darte respuestas rápidas.

---

## 3. Cómo acceder a Copilot

### 3.1 Desde la app de escritorio (Windows/macOS)
1. Abre Microsoft Teams e inicia sesión con tu cuenta laboral.  
2. Observa la **barra lateral** o la **barra superior**: deberías ver un icono o entrada llamada **Copilot** (a veces aparece como un icono de robot 🤖 o como "Copilot").  
3. Haz clic en **Copilot** para abrir el panel lateral o la ventana de conversación con Copilot.  
4. Alternativamente, dentro de un **chat** o **canal**, haz clic en el botón que dice “Copilot” o en la opción de tres puntos si está dentro del menú de extensiones.

_Si no ves Copilot:_ actualiza Teams, reinicia la app y si sigue sin aparecer consulta a tu administrador de TI (puede requerir licencia o configuración en el tenant).

### 3.2 Desde la app móvil (iOS/Android)
1. Abre Teams en tu móvil.  
2. En el menú inferior o en los tres puntos, busca la opción **Copilot**.  
3. Toca para abrir y escribe tu pregunta o pega un prompt.

---

## 4. Usos principales y ejemplos paso a paso
Aquí vienen ejemplos listos para copiar, con pasos concretos y capturas simuladas.

### 4.1 En Reuniones — Ejemplo: Generar acta y tareas
**Objetivo:** Al terminar una reunión, obtener un resumen y una lista de tareas asignadas.

**Pasos:**
1. Durante o al finalizar la reunión, abre el panel de Copilot (en la misma ventana de Teams).  
2. Copia y pega este prompt en Copilot:

```
Resumen de la reunión: genera un resumen breve en 5-6 frases con los puntos clave, lista de decisiones tomadas y una tabla con las tareas asignadas (tarea | responsable | fecha límite).
```

3. Revisa la respuesta y copia la tabla al chat o a un documento compartido.

**Ejemplo de salida esperada (lo que Copilot puede devolver):**
- Resumen en párrafos cortos.  
- Lista de decisiones.  
- Tabla con tareas y responsables.

**Captura simulada — panel de reunión con Copilot:**
```
+------------------------------------------------------------+
| REUNIÓN: Seguimiento Proyecto XYZ                           |
| ---------------------------------------------------------- |
| [VIDEO] [USUARIOS]             [Copilot 🤖 - Panel]         |
|                                                            |
| Copilot: "Pega tu prompt aquí"  [Enviar]                   |
|                                                            |
| Resumen (generado):                                         |
| - Punto 1...                                                |
| - Decisión: Aprobar presupuesto                              |
|                                                            |
| Tareas:                                                     |
| | Tarea                    | Responsable | Fecha límite |   |
| | Preparar informe         | María       | 2025-09-15   |   |
+------------------------------------------------------------+
```

---

### 4.2 En Chats y Canales — Ejemplo: Responder un mensaje difícil
**Objetivo:** Preparar una respuesta profesional y breve a un mensaje complicado.

**Pasos:**
1. Copia el mensaje al que quieres responder (selecciónalo y copia).  
2. Abre Copilot en el chat y pega este prompt:

```
Contexto: [pega acá el mensaje original].  
Tono: profesional y breve.  
Objetivo: pedir más información sobre el punto 2 y proponer una reunión de 15 minutos.  
Escribe la respuesta en español, 2-3 frases.
```

3. Revisa y envía la respuesta sugerida por Copilot.

**Captura simulada — Chat con Copilot:**
```
+-----------------------------------------------+
| Chat: Equipo Marketing                         |
| --------------------------------------------- |
| Juan: "No estoy de acuerdo con el informe..." |
| Copilot panel:                                 |
| Copilot: "¿Quieres que redacte una respuesta?" |
| Sugerencia: "Gracias por el comentario, Juan. ¿Podrías aclarar ..." |
+-----------------------------------------------+
```

---

### 4.3 En Archivos — Ejemplo: Resumir un Excel o Word compartido
**Objetivo:** Obtener los puntos clave de un documento largo.

**Pasos:**
1. Asegúrate de que el archivo esté cargado en el canal o chat.  
2. Abre Copilot y pega este prompt (o usa la opción de analizar archivo si está disponible):

```
Resume el documento adjunto en 6-8 frases. Enumera las 3 métricas/valores más importantes y su valor.
```

3. Copilot devolverá un resumen y puede extraer valores clave.

**Captura simulada — Copilot analizando un archivo:**
```
+--------------------------------------------+
| Canal: Reportes Mensuales                   |
| Archivo: resumen_financiero_sep2025.xlsx    |
| Copilot: "Resumen rápido:"                  |
| - Ingresos totales: $120,000                |
| - Gastos operativos: $65,000                |
+--------------------------------------------+
```

---

## 5. Ejemplos prácticos (plantillas y prompts listos)
A continuación tienes prompts listos para copiar. Pégalos tal cual en Copilot y ajusta nombres/fechas.

### 5.1 Acta de reunión corta
```
Genera un acta de la reunión con título "Reunión Seguimiento Proyecto X". Incluye: resumen en 5 frases, decisiones, y tabla de tareas (tarea | responsable | fecha límite). Formato: Markdown.
```

### 5.2 Respuesta a cliente insatisfecho
```
Contexto: el cliente escribió: "No recibí el equipo en la fecha acordada". Redacta una respuesta en tono empático, ofrece solución y propone llamada de 10 minutos. Longitud: 3-4 frases.
```

### 5.3 Resumen ejecutivo de un documento
```
Resume el documento adjunto en 6 puntos clave y luego escribe 3 recomendaciones prácticas y concretas en español sencillo.
```

### 5.4 Extraer tareas de un chat largo
```
Analiza el chat y lista todas las tareas implícitas y explícitas en formato: tarea | responsable (si se menciona) | prioridad sugerida.
```

---

## 6. Capturas simuladas (UI simplificada)
Aquí hay varias capturas simuladas para aprender a identificar dónde aparece Copilot. Son ilustraciones de ejemplo y están simplificadas para entender la idea visual.

**Captura A — Barra superior con Copilot**
```
+--------------------------------------------------+
| [Equipos] [Calendario] [Llamadas] [Archivos] [Copilot🤖] |
+--------------------------------------------------+
```

**Captura B — Panel lateral de Copilot en reunión**
```
+----------------------+   +-----------------------+
| VIDEO REUNIÓN         |   | COPILOT (panel)       |
| [Participantes...]    |   | --------------------- |
|                       |   | Escribe tu pregunta...|
|                       |   | [Ej. Resume la reunión]|
+----------------------+   +-----------------------+
```

**Captura C — Sugerencia de respuesta en chat**
```
+------------------------------------------+
| Chat: Soporte Técnico                     |
| Usuario: "El equipo no enciende"         |
| [Copilot sugiere: "¿Probaste desconectar..."]|
+------------------------------------------+
```

> Estas capturas son simuladas; sirven para reconocer la interfaz. Si quieres capturas reales, puedo generarlas basadas en tu Teams (necesitaría que subas pantallazos reales o permiso para generarlas).

---

## 7. Buenas prácticas y recomendaciones
- **Ser específico:** cuanto más claro sea el prompt, mejor la respuesta.  
- **Pedir formato:** si necesitas un e-mail, pide "Escribe como correo"; si necesitas una tabla, pide "Devuélvelo en tabla Markdown".  
- **Verificar siempre:** Copilot puede equivocarse; revisa hechos, fechas, cifras.  
- **Privacidad:** no pidas a Copilot que comparta información confidencial fuera del entorno controlado.  
- **Idioma:** Copilot entiende múltiples idiomas; si necesitas español sencillo, pídelo.

---

## 8. Problemas comunes y soluciones rápidas
- **No aparece Copilot:** actualiza Teams, revisa permisos/licencias, reinicia la app o prueba Teams web. Contacta al administrador si persiste.  
- **Respuestas incorrectas:** pide más detalle a Copilot: "Corrige esto: ..." o "Verifica la fecha y corrige".  
- **Privacidad/dudas legales:** antes de usar Copilot con datos sensibles, consulta la política de datos de la empresa.

---

## 9. Plantillas de prompts (cheat sheet)
Pequeña hoja de trabajo para pegar directamente en Copilot.

| Tarea | Prompt ejemplo |
|---|---|
| Resumen reunión | `Resume la reunión en 5 frases y lista las 5 tareas principales.` |
| Redactar correo | `Escribe un correo para X en tono formal breve, asunto: "Seguimiento".` |
| Extraer tareas | `Lista todas las tareas del chat en formato tabla: tarea | responsable | fecha sugerida.` |
| Simplificar texto | `Explica este párrafo en lenguaje sencillo (nivel escolar).` |
| Traducir | `Traduce este texto a inglés británico, mantén el tono formal.` |

---

## 10. Checklist de adopción (para equipos)
- ✅ Formar una sesión de 30 minutos para mostrar Copilot a los equipos.  
- ✅ Compartir esta guía y la hoja de prompts.  
- ✅ Definir política de uso (qué datos están permitidos).  
- ✅ Crear canal de soporte interno para dudas.  
- ✅ Solicitar feedback tras 2 semanas de uso.

---

## 11. Anexos y contactos
- **Soporte TI:** escribe a soporte@tuempresa.com para dudas de acceso o permisos.  
- **Sugerencias de mejora del manual:** responde en este documento con comentarios.

---

## Versión imprimible / acciones siguientes
Si quieres, puedo:  
- **Generar un PDF listo para compartir** (con las mismas capturas simuladas).  
- **Crear capturas reales** a partir de pantallazos tuyos y reemplazar las simuladas.  
- **Reducir el manual a una hoja de "cheat sheet" en una página.**

Dime cuál opción prefieres y la genero ahora.

---

*Fin del manual — versión 1.0*

