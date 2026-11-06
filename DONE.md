# Café Luna — listo

Landing estática responsive de una sola página. Sin build, sin repositorio git ni publicación.

## Archivos
- `index.html`: todas las secciones, metadatos y contacto demo.
- `styles.css`: diseño responsive, textura de papel, vapor, hover, foco y reduced-motion.
- `main.js`: revelado progresivo con IntersectionObserver, contenido visible sin JS.
- `robots.txt`: permite crawling para que los robots lean noindex.
- `_headers`: X-Robots-Tag: noindex,nofollow (para hosts compatibles).
- `assets/favicon.svg`: luna en fondo espresso.
- `spec.md`: dirección visual y referencias.
- `assets/images/hero-latte.png`
- `assets/images/medialunas.png`
- `assets/images/barra.png`
- `assets/images/rincon.png`
- `qa/desktop.png`, `qa/mobile.png`: capturas a 1280 y 390 px.
- `DONE.md`: esta documentación.

## Tipografías
Instrument Serif (normal e italic) + DM Sans (400, 500, 600, 700), desde Google Fonts. Fallbacks Georgia y Arial. Se necesita internet para las fuentes; fotos y estilos son locales.

## Fotos originales
Generadas con el tool integrado imagegen y copiadas desde `/home/box/.codex/generated_images/` a `assets/images/`.

Prompts finales, todos con fotografía editorial realista, luz cálida, sin texto ni logos:
1. Hero, 16:9: taza y plato de cerámica crema con latte y arte de luna creciente, mesa de nogal junto a ventana al anochecer, taza al centro-derecha y espacio oscuro a izquierda, bokeh de calle de Buenos Aires, textura natural y grano sutil.
2. Medialunas, 4:3: tres medialunas argentinas doradas y brillantes en plato cerámico crema sobre nogal, luz cálida de tarde, primer plano apetitoso y natural.
3. Barra, 4:3: pequeño café de barrio de Villa Crespo al anochecer, barra de madera, máquina de espresso de acero, tazas, lámparas cálidas, estantes oscuros y paredes crema, sin personas.
4. Rincón, 4:3: mesa y sillas de madera, banco con almohadones caramelo, libros, ventana con luz cálida de tarde, paredes crema, pequeño café de Villa Crespo, sin personas.

Las imágenes son ilustrativas; no representan un local real. El WhatsApp y los horarios están identificados como ficticios.

## Abrir localmente
Abrí `index.html` directamente en el navegador. También podés ejecutar desde este directorio:

```sh
python3 -m http.server 8000
```

Luego visitá http://localhost:8000. `_headers` requiere un hosting que interprete ese formato; el servidor Python no lo aplica. La meta robots funciona en el HTML.

## Verificación
- Render en Chrome headless y revisión visual de capturas de escritorio 1280×960 y móvil 390×844.
- Sintaxis JS verificada con `node --check main.js`.
- Verificadas las referencias locales, los textos alternativos y los destinos de anclas.
- Sin Disallow: /; meta y header noindex,nofollow presentes.
- Focus visible, enlace para saltar al contenido y soporte prefers-reduced-motion.
