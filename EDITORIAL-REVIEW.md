# Revisión editorial profunda — estado de trabajo

Se revisaron los 53 artículos del repositorio. El detalle por archivo está en `EDITORIAL-PLAN.csv`.

## Criterios usados

- presencia de fuentes externas;
- claridad de autoría;
- cantidad y especificidad de imágenes;
- extensión útil, no solo cantidad de palabras;
- promesas del título frente a la metodología realmente descrita;
- posibilidad de reproducir el procedimiento.

## Cambios realizados

- La página About ahora distingue entre prototipos documentados, cálculos y síntesis de fuentes públicas; no presenta todos los artículos como pruebas prácticas.
- Se moderó la promesa de verificación universal de datos.
- Se generó una matriz editorial para trabajar artículo por artículo sin inventar pruebas, fotografías ni mediciones.

## Próxima intervención recomendada

Empezar por los artículos marcados como prioridad alta: añadir fuentes primarias concretas, ejemplos reproducibles, diagramas propios y una nota de alcance honesta. No publicar como “probado” ningún resultado que no tenga evidencia del autor.

## Ilustraciones originales añadidas

Se añadieron cuatro diagramas editoriales conceptuales, cada uno con pie de imagen que indica que no sustituye la validación técnica:

- `articles/diagram-arduino-servo-power.png`
- `articles/diagram-robot-transmissions.png`
- `articles/diagram-cable-routing.png`
- `articles/diagram-robot-arm-materials.png`

Se integraron respectivamente en los artículos de cableado Arduino, transmisiones, gestión de cables y estructura de aluminio. Estas ilustraciones mejoran la explicación visual, pero no se presentan como fotografías de pruebas ni como mediciones reales.

Se añadieron tres ilustraciones conceptuales adicionales en impresión 3D, cinemática 6-DOF y fibra de carbono. También se sustituyó la expresión promocional repetida “premium guide” por “reference guide”.

## Fuentes añadidas en esta fase

Se añadieron bloques de fuentes primarias y documentación técnica en 12 artículos que tenían pocas o ninguna referencia externa: Arduino, ESP32, impresión 3D, transmisiones, cinemática, payload, ruido, refrigeración y vacío. Cada bloque incluye enlaces directos, aviso de verificación por configuración y fecha de revisión. Esto es un primer lote; los datos específicos de cada tabla aún deben tener su enlace inmediato cuando corresponda.

## Referencias de tablas

Se añadieron captions con enlaces de referencia a las 90 tablas detectadas. Cuando el artículo ya tenía una fuente externa, se usa como referencia primaria; cuando no la tenía, el caption está marcado explícitamente como “Suggested primary reference”. En todos los casos se indica que el lector debe verificar cada fila contra la revisión vigente y la configuración exacta. No se presentan estas referencias genéricas como prueba de cada cifra; la verificación fila por fila sigue siendo necesaria para datos de fabricante, precios y normas.
