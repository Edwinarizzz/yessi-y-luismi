# Baby Prediction Bingo (Yessi)

Página estática, sin base de datos, sin dominio y sin build. Los invitados llenan sus predicciones y las
envían por WhatsApp al número configurado.

## Archivos
- `index.html` — el juego que comparten los invitados.
- `admin.html` — para la organizadora: pega los mensajes de WhatsApp, pone los resultados reales y calcula
  ganadores (todo en el navegador, no sube nada). Es público si el repo lo es, pero solo sirve si se le pegan datos.
- `foto.jpg` (opcional) — foto para la pantalla de inicio; activar con `CONFIG.foto = "foto.jpg"`.

## Configuración
Todo en el bloque `CONFIG` al inicio del `<script>` de `index.html`: teléfono, título, mensaje, fecha probable
(cuenta regresiva), fecha límite, foto, pregunta de sexo y música.

## Funciones
- Pantalla «Press Start», música chiptune (botón 🔊/🔇), cuenta regresiva, foto opcional.
- 11 tarjetas (incluye sexo y nombre) + mensaje para el bebé, barra de progreso, borrador autoguardado.
- Envío por WhatsApp al número de la organizadora, o copiar el texto.
- Fecha límite para participar.
- QR del enlace (imagen de api.qrserver.com; solo se muestra cuando la página está publicada en http/https).

## Estado
- Scripts revisados por sintaxis con `node --check`; **sin probar en navegador** desde este entorno.
- Pendiente: poner el número real en `CONFIG.telefono` y ajustar `fechaProbable`.
- Si se cambian textos de opciones en `index.html`, deben cambiarse igual en `admin.html` (array `Q`), porque
  la puntuación compara texto exacto.
