# Recuperación de Información (Retrieval)

La recuperación es el corazón operativo del sistema RAG. Su objetivo es seleccionar, a partir de una consulta del usuario, los fragmentos de información más relevantes para ser utilizados como contexto del LLM.

La búsqueda semántica basada en embeddings permite recuperar documentos por significado, superando las limitaciones de la búsqueda léxica tradicional. Sin embargo, la lectura destaca que las mejores implementaciones suelen combinar ambos enfoques en sistemas híbridos.



> [!Nota]
> Una recuperación deficiente conduce directamente a respuestas incorrectas o incompletas, independientemente de la capacidad del modelo generativo.


## Técnicas
- Búsqueda semántica (embeddings)
- Búsqueda léxica
- Enfoques híbridos

## Optimizaciones
- Reranking con cross-encoders
- MMR (diversidad)
- HyDE (expansión de consulta)

## Métricas asociadas
- Context precision
- Context recall

Relacionado con:
- [[RAG - Evaluación]]
