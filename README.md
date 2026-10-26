# Yessi & Luismi · Predicciones del bebé

Página estática, sin base de datos, sin dominio propio y sin build. Los invitados llenan sus predicciones y las
envían por WhatsApp al número configurado. Publicada con GitHub Pages: https://edwinarizzz.github.io/yessi-y-luismi/

## Archivos
- `index.html` — el formulario que comparten los invitados (diseño sobrio: marfil, verde salvia y dorado).
- `admin.html` — para la organizadora: pega los mensajes de WhatsApp, pone los resultados reales y calcula
  ganadores (todo en el navegador, no sube nada).
- `foto.jpg` (opcional) — activar con `CONFIG.foto = "foto.jpg"`.

## Configuración
Bloque `CONFIG` al inicio del `<script>` de `index.html`: teléfono, mensaje, fecha probable (cuenta regresiva),
fecha límite, foto y pregunta de sexo.

## Funciones
- 11 preguntas + mensaje opcional; «momento del día» es una selección (madrugada / mañana / tarde / noche).
- Cuenta regresiva, foto opcional, barra de progreso discreta, borrador autoguardado.
- Envío por WhatsApp o copiar el texto; QR del enlace (api.qrserver.com, solo cuando está publicada).

## Estado
- Rediseño elegante (se quitó el tema de videojuego, la música y la pantalla de inicio).
- Scripts revisados por sintaxis con `node --check`; **sin probar en navegador** desde este entorno.
- Si se cambian textos de opciones o etiquetas del mensaje en `index.html`, cambiarlos igual en `admin.html`
  (array `Q`), porque la puntuación compara texto exacto.
