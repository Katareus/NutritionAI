# AGENTS.md
Aplicación en .net para generar una lista de la compra para whatsapp. Proyecto didáctico: el código debe poder entenderlo alguien que empieza a programar.
## Stack y estructura
- Framework: .NET10
- Librerías:
- NPM:
- Bundler:
- Build:
- Debe compilarse antes de poder ejecutar un archivo .exe
## Convenciones
- Textos de la interfaz en español.
- Código simple, nombres descriptivos y comentarios solo donde aporten.
- Diseño limpio; cualquier lista de la compra nueva debe verse bien en la aplicación whatsapp del móvil android.
## Datos
- localStorage, clave `nutrition-mapper-sesiones`: array de `{ date: "AAAA-MM-DD", topic, minutes }`.
- Si cambias la forma de los datos, mantén compatibilidad con lo ya guardado o el usuario perderá sus sesiones.
## Proceso de mapeo (fácil equivocarse)
- Leerás los pdf de la carpeta src/requests
- Extraeras los alimentos y sus cantidades
- Normalizarás los nombres de los alimentos, por ejemplo 'Tomate', 'Tomates'.
- Agruparas los alimentos y sumarás las cantidades.
- Categorizarás los alimentos según la siguiente lista: { "Verduleria", "Fruteria", "Panaderia", "Despensa", "Lacteos", "Charcuteria", "Carniceria", "Pescaderia", "Congelados", "Especias"}
- Escribirás la lista de alimentos normalizados, agrupados, sumados y categorizados. Tienes un ejemplo de resultado en src/responses/ShoppingList.txt
## Forma de trabajar
- Haz solo lo que se pide: no añadas funcionalidades por tu cuenta.
- Cambios pequeños y enfocados; no reescribas lo que ya funciona.
- Al terminar, resume qué has cambiado y cualquier decisión que deba revisar.
## Límites
- ✅ Siempre: mantener los textos en español.
- ✅ Siempre: actualizar `MEMORY.md` al terminar cada tarea.
- ⚠️ Pregunta antes: crear archivos nuevos, cambiar el formato de los datos guardados.
- 🚫 Nunca: añadir dependencias, frameworks o un paso de build sin preguntar.
## Verificación
- No hay tests automáticos. Después de cada cambio, verifica con el MCP de Chrome DevTools: abre `index.html`, prueba la funcionalidad, revisa la consola y comprueba la vista móvil. 
- Para empezar de cero: DevTools → Application → Local Storage → borrar la clave `nutrition-mapper-sesiones`.
## Memoria
- Al empezar, lee `MEMORY.md` para conocer el estado del proyecto y las decisiones tomadas.
- Al terminar una tarea, actualízalo: estado actual, decisiones importantes (con su porqué) y errores a evitar.
- Mantenlo breve (máximo ~50 líneas): resume o elimina lo que ya no aporte.
- Si algo se convierte en una regla permanente, propón moverlo a `AGENTS.md` en lugar de dejarlo en la memoria.
- No guardes nunca datos sensibles (claves, tokens, datos personales).
## Comandos
## Reglas
- Lee `docs/constitution.md` y la spec activa (`specs/NNN-*/`) antes de tocar código.