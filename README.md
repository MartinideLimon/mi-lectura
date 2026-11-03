# Mi Lectura — PWA para iPhone

## Archivos
- `index.html`: aplicación de lectura.
- `manifest.webmanifest`: nombre, iconos y modo de aplicación.
- `sw.js`: caché para abrir la app sin conexión tras la primera carga.
- `icons/`: iconos de instalación y de pantalla de inicio.

## Publicarla para instalarla en iPhone
La instalación PWA necesita una dirección HTTPS. Abrir `index.html` directamente desde Archivos no permite registrar el service worker ni instalarla como PWA.

1. Sube el contenido de esta carpeta (no la carpeta ZIP) a un hosting HTTPS estático, por ejemplo GitHub Pages, Netlify o Cloudflare Pages.
2. Asegúrate de que `index.html`, `manifest.webmanifest`, `sw.js` e `icons/` estén en la misma raíz de publicación.
3. En el iPhone, abre la URL publicada en **Safari**.
4. Pulsa **Compartir** → **Añadir a pantalla de inicio**.
5. Si aparece la opción **Abrir como app web**, actívala y pulsa **Añadir**.
6. Abre Mi Lectura desde el nuevo icono. Después de cargarla una vez con conexión, los archivos principales se guardan en caché para uso sin conexión.

## Almacenamiento y privacidad
Los libros y sesiones se guardan con `localStorage` en el navegador de este dispositivo. No se envían a un servidor. El almacenamiento local no es una copia de seguridad garantizada: usa Historial → Exportar copia de seguridad periódicamente y conserva el archivo fuera del móvil.

## Notas
- Los datos se quedan en el navegador/origen donde uses la app; no se sincronizan entre dispositivos.
- Para actualizar la app tras cambiar archivos, sube la nueva versión y aumenta `CACHE_NAME` en `sw.js` (por ejemplo, `mi-lectura-pwa-v2`).
- El icono es una ilustración sencilla creada para esta primera versión.
