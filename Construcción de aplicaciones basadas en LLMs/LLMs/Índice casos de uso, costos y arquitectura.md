# RAG – Generación Aumentada por Recuperación

La Generación Aumentada por Recuperación (Retrieval-Augmented Generation, RAG) es un patrón arquitectónico que combina modelos de lenguaje de gran escala (LLMs) con mecanismos de recuperación de información desde fuentes externas confiables.

> [!Idea principal]
> **RAG** permite que el modelo recupere información de fuentes externa

El objetivo fundamental de RAG es **superar las limitaciones inherentes de los LLMs**, particularmente:
- Su conocimiento estático, limitado al momento de entrenamiento.
- La tendencia a generar alucinaciones cuando carecen de información suficiente o verificable.

> [!hint]  Importante
> RAG introduce una capa explícita de recuperación que aporta contexto relevante y verificable antes de la generación de la respuesta. De esta forma, el LLM actúa como un motor de razonamiento y síntesis, no como una fuente primaria de verdad.

Desde una perspectiva de ingeniería de software, RAG representa un cambio de paradigma: el valor ya no está en el modelo, sino en la **arquitectura**, la **orquestación del pipeline** y la **integración con datos propios del dominio**.

## Notas relacionadas
- [[RAG - Pipeline]]
- [[RAG - Ingesta de Datos]]
- [[RAG - Embeddings y Vector DB]]
- [[RAG - Recuperación]]
- [[RAG - Generación]]
- [[RAG - Evaluación]]
- [[RAG - Observabilidad y Costos]]
- [[RAG - Seguridad y Producción]]
- [[RAG - Frameworks para desarrollo con LLMs]]
