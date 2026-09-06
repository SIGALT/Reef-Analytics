Reef Analytics — V7

Cambios principales
- Corrección del nombre: Reef Analytics.
- Generador geométrico 3D nativo, sin librerías externas.
- Vista 3D interactiva mediante arrastre en escritorio y móvil.
- Df3D aproximado mediante box-counting de puntos muestreados sobre la superficie sintética.
- Surface area calculada como suma de áreas laterales de troncos de cono que representan las ramas.
- Colony volume calculado como suma de volúmenes de troncos de cono.
- Projected area estimada sobre el plano XY.
- Height calculada como extensión vertical del modelo.
- Shelter volume = projected area × height − colony volume.
- Escala configurable en cm por unidad del modelo.
- Comparación T0 vs T1.
- Exportación CSV, PNG y nube de puntos PLY.

Notas científicas
- Las métricas pertenecen al modelo geométrico sintético.
- Df3D no debe interpretarse como equivalente a Df3D de una malla fotogramétrica real.
- Shelter volume sigue la formulación funcional: área proyectada × altura − volumen de colonia.
- Surface area y colony volume son aproximaciones analíticas de la geometría tubular sintética.
- El parámetro de estrés sigue siendo un escenario conceptual, no una predicción calibrada con DHW, temperatura o mortalidad real.

Netlify
1. Descomprime este ZIP.
2. Sube el contenido como nuevo deploy.
3. Cierra y vuelve a abrir la URL para cargar la caché reef-analytics-v7.
