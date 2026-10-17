# Mi Lectura — Dark Academia (PWA para iPhone)

Aplicación web instalable con biblioteca, registro de progreso, calendario mensual, estadísticas e historial. Diseño combinado: menús verde bosque, páginas color pergamino y detalles dorados.

## Publicar con GitHub Pages desde iPhone
1. En GitHub crea un repositorio llamado `mi-lectura`. Para Pages gratuito y la configuración más sencilla, selecciona **Public**. El código será público: no subas nunca copias de seguridad ni datos personales.
2. En el repositorio pulsa **Add file → Upload files** y sube TODO el contenido de esta carpeta: `index.html`, `manifest.webmanifest`, `sw.js`, `icons/` y `README.md`.
3. Ve a **Settings → Pages**. En **Build and deployment**, elige **Deploy from a branch**, branch `main`, carpeta `/ (root)` y pulsa **Save**.
4. Espera a que termine la publicación y abre la URL que GitHub Pages te muestre.
5. En Safari del iPhone: Compartir → Añadir a pantalla de inicio.
6. Abre la app una vez con internet para guardar sus archivos y después prueba el modo avión.

## Privacidad y copias
Los datos se guardan en el almacenamiento local del navegador del dispositivo. No se envían a GitHub ni a un servidor. Exporta periódicamente una copia desde **Historial → Datos y privacidad** y guárdala en Archivos/iCloud Drive. Si borras los datos de Safari o la aplicación web, podrías perderlos. La copia JSON contiene tus datos personales; no la subas al repositorio público.

## Notas
- El alojamiento HTTPS debe seguir disponible para la primera carga y las actualizaciones. Tras la primera carga, el service worker permite abrir la app sin conexión cuando el navegador conserva la caché.
- Esta es una PWA, no una app nativa de App Store. Algunas integraciones de iOS pueden diferir.
