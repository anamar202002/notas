# Embeddings y Bases Vectoriales

Los embeddings son **representaciones vectoriales densas que capturan el significado semántico del texto**. Constituyen el puente entre el lenguaje natural y los algoritmos de búsqueda numérica.

La elección del modelo de embedding es una decisión estratégica. Existen modelos comerciales y de código abierto, cada uno con compromisos distintos entre calidad semántica, dimensionalidad, latencia y costo. Un embedding de mayor calidad no siempre produce mejores resultados si el resto del pipeline no está bien diseñado.

Los embeddings se almacenan en bases de datos vectoriales, que implementan algoritmos de búsqueda aproximada para operar eficientemente sobre grandes volúmenes de datos. Estas bases permiten realizar consultas de similitud semántica en tiempo aceptable incluso con millones de documentos.

Decisiones clave:
- Modelo de embedding y su versionamiento.
- Dimensionalidad del vector.
- Estrategia de actualización incremental.
- Persistencia de metadatos para trazabilidad.

Cambiar el modelo de embedding implica, en la mayoría de los casos, **reprocesar todo el corpus**, lo que convierte esta decisión en un factor crítico de diseño desde etapas tempranas.

Relacionado con:
- [[RAG - Recuperación]]
- [[RAG - Observabilidad y Costos]]
