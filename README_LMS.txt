RA EDUCATIVA — DEMO MULTI-MARCADOR (A-Frame + AR.js)
Fecha de creación: 2025-10-15

CONTENIDO
- index.html → demo lista para usar en línea (CDN). Dos marcadores: "hiro" y "kanji".
- assets/ → ubicá aquí tus modelos 3D (.glb/.gltf), imágenes y audios.

CÓMO USAR EN UN AULA VIRTUAL (EDUCATIVA/Moodle)
1) Subí esta carpeta a un hosting (Drive Web público, GitHub Pages, tu servidor) o comprimila y usá un "Paquete SCORM/Archivo" si tu LMS lo soporta como recurso descargable.
2) Insertá en el aula un Recurso "Página" o "Etiqueta" con un iframe, por ejemplo:
   <iframe src="URL_PUBLICA/index.html" width="100%" height="640" allow="camera *; microphone *" style="border:0"></iframe>

   Importante: algunos LMS abren en una pestaña nueva por seguridad. Permití la cámara en el navegador.

MARCADORES
- Usamos presets de AR.js: "hiro" y "kanji". Buscá e imprimí "hiro marker pdf" y "kanji marker pdf".
- Para marcadores propios (pattern.patt), generá el patrón con el generador de AR.js y reemplazá <a-marker preset="..."> por <a-marker type="pattern" url="assets/MI_PATRON.patt">.

PERSONALIZAR CON MODELOS 3D
- Reemplazá las primitivas por modelos GLB/GLTF dentro de cada marcador. Ejemplo:
  <a-gltf-model src="assets/yaguarete.glb" position="0 0 0" scale="0.5 0.5 0.5"></a-gltf-model>

SIN INTERNET (OFFLINE)
- Descargá estas librerías y referencialas en local:
  * aframe.min.js (v1.4.1)
  * aframe-ar-nft.js de AR.js (v3.3.2)
- Guardalas en /libs y cambia en index.html los <script src="..."> por rutas locales (ej.: ./libs/aframe.min.js).
- Si tu LMS bloquea la cámara embebida, abrí el recurso en ventana nueva.

ACCESIBILIDAD Y DUA
- Incluí instrucciones textuales, audio explicativo y un botón de captura (incluido).
- Agregá una alternativa 2D (imágenes, video corto del uso de RA) para estudiantes sin cámara o conectividad.
- Evaluación sugerida: mini-rúbrica de 3 criterios → (a) Orientación espacial (localiza y mantiene el marcador), (b) Comprensión del contenido (identifica el animal), (c) Comunicación (describe lo observado).

SEGURIDAD Y PRIVACIDAD
- No almacena video ni audio. La captura se hace en el dispositivo del usuario (PNG descargable).

SOPORTE RÁPIDO
- Si no aparece la cámara: revisar permisos del navegador, probar en Chrome/Edge/Firefox, cerrar otras apps que usen la cámara.
- Iluminación uniforme y marcadores impresos con buen contraste mejoran el tracking.
