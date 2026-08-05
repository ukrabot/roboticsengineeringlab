# Auditoría previa a AdSense

## Cambios aplicados en esta revisión

- Se corrigió el contador de la portada: el repositorio contiene 53 artículos HTML, no 49.
- Se incorporaron al `sitemap.xml` los cuatro artículos que faltaban: paletizado, batería, comparación de controladores y tipos de brazos robóticos.
- Se corrigió la fecha de actualización visible de la portada para que no aparezca como actualizada en 2024 mientras el repositorio contiene artículos de 2026.
- Se eliminó la falsa confirmación de suscripción del formulario de newsletter. El formulario mostraba “Subscribed” sin enviar ni guardar ningún correo. Ahora dirige al formulario de contacto.

## Hallazgos que aún requieren intervención editorial

1. La cantidad de páginas no sustituye a la experiencia original. Los artículos deben incorporar fotos propias, pruebas, mediciones, código, CAD, esquemas o una metodología verificable cuando se afirme experiencia práctica.
2. Las reseñas de equipos que no fueron probados deben titularse como análisis documental o comparación de especificaciones, no como reseñas prácticas.
3. Deben revisarse las afirmaciones de precios, certificaciones, rendimiento y disponibilidad contra fuentes primarias y con fecha de consulta.
4. Deben sustituirse imágenes genéricas repetidas por material específico del proyecto, con pies de foto y licencia documentada.
5. Revisar autoría, biografías, experiencia y fotografías para que sean reales y verificables.
6. Comprobar el sitio publicado, no solo el repositorio: respuestas 200, imágenes, canonical, sitemap, robots, móvil y ausencia de 404.
7. Mantener accesibles y actualizadas las páginas About, Contact, Privacy y Terms. La política de privacidad debe reflejar los servicios realmente activos; no declarar analytics, newsletter o anuncios que no estén configurados.

## Revisión técnica realizada

- 53 artículos HTML en `/articles/`.
- Enlaces locales comprobados contra los archivos del repositorio: no se detectaron rutas locales inexistentes en esta copia.
- Se detectó que el sitemap tenía 49 artículos y omitía cuatro; ya fue corregido.
- No se debe solicitar una nueva revisión de AdSense hasta completar la revisión editorial y probar el sitio desplegado.

## Ajustes editoriales aplicados después de la auditoría

- La portada ya no simula una suscripción a un boletín que no tiene servicio de envío configurado.
- Se cambiaron varias etiquetas de “Review” a “Technical Analysis / Engineering Analysis” cuando el propio contenido indica que se basa en especificaciones públicas y no en una prueba del producto.
