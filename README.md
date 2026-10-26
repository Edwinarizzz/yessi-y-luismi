# Yessi & Luismi · Baby Prediction Bingo

Página estática (GitHub Pages) pensada para celular. Sin servidor propio ni dominio: las predicciones se guardan
en una hoja de Google (Apps Script) y también se pueden enviar por WhatsApp.

Publicada en: https://edwinarizzz.github.io/yessi-y-luismi/

## Archivos
- `index.html` — el juego que comparten los invitados (estilo arcade neón; la tarjeta activa brilla en rosado).
- `admin.html` — panel de la organizadora: carga las respuestas de la hoja, pone los resultados reales y muestra
  el ranking. Pide una clave la primera vez.
- `apps-script.gs` — script de Google Sheets. **No está en el repo** (`.gitignore`) porque lleva la clave.
- `foto.jpg` (opcional) — activar con `CONFIG.foto = "foto.jpg"`.

## Configuración
Bloque `CONFIG` al inicio del `<script>` de `index.html`: teléfono, mensaje, fecha probable (cuenta regresiva),
fecha límite, foto, pregunta de sexo, música y URL de la hoja (`hoja`).

## Puntos (admin.html)
- 1 punto por acierto exacto en cada una de las 11 preguntas.
- Fecha (±1 día), peso (±0.1 kg) y longitud (±1 cm): quedar cerca da 0.5 punto. Los márgenes están en `tol` dentro de `Q`.
- El peso se lee como kilos; si alguien escribe libras quedará lejos.

## Estado
- Funciona: guardado en la hoja (probado con el endpoint real), lectura con clave, música que se pausa en segundo plano.
- Scripts revisados por sintaxis con `node --check`; el diseño se probó en celular por el usuario.
- Pendiente antes de compartir: borrar las filas de "PRUEBA" de la hoja de Google.
- Si se cambian textos de opciones o etiquetas del mensaje en `index.html`, cambiarlos igual en `admin.html` (`Q`).
- Si se cambia el script de Google: Implementar → Administrar implementaciones → Nueva versión.
