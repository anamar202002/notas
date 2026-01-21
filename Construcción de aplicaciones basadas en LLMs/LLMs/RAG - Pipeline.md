# Pipeline RAG – Visión General


Un sistema RAG no es un componente aislado, sino un pipeline compuesto por múltiples etapas interdependientes. Cada una cumple una función específica y su correcta orquestación determina la calidad, confiabilidad, latencia y costo del sistema completo.

El pipeline puede dividirse conceptualmente en dos flujos principales:
1. **Flujo offline (preparación del conocimiento)**: ingesta, limpieza, chunking y generación de embeddings.
2. **Flujo online (tiempo de consulta)**: procesamiento de la pregunta, recuperación de contexto, generación y evaluación.


```mermaid
flowchart TD
    A[Fuentes de Datos] --> B[Ingesta y Limpieza]
    B --> C[Chunking]
    C --> D[Embeddings]
    D --> E[Base de Datos Vectorial]

    F[Consulta del Usuario] --> G[Embedding de Consulta]
    G --> H[Recuperación de Contexto]
    H --> I[Reranking / Filtrado]
    I --> J[LLM Generador]
    J --> K[Respuesta Final]
    
```
Cada bloque del pipeline introduce decisiones de diseño críticas. Por ejemplo, una mala estrategia de chunking puede degradar la recuperación incluso si el modelo de embedding es de alta calidad. De igual forma, una recuperación deficiente no puede ser compensada por un modelo generativo más potente.

```mermaid
flowchart TD
    %% =========================
    %% FASE 1: INGESTIÓN (OFFLINE)
    %% =========================
    subgraph F1["FASE 1 · INGESTIÓN DE CONOCIMIENTO (Proceso Offline)"]
        A1["1️⃣ Documentos<br/><small>PDFs · Bases de datos · Markdown · etc.</small>"]
        A2["2️⃣ Fragmentación<br/><small>División en chunks con solapamiento</small>"]
        A3["3️⃣ Embeddings<br/><small>Vectorización del texto<br/>(Modelos de embedding)</small>"]
        A4["4️⃣ Vector DB<br/><small>Almacenamiento de vectores indexados</small>"]

        A1 --> A2 --> A3 --> A4
    end

    %% =========================
    %% TRANSICIÓN
    %% =========================
    A4 --> B1

    %% =========================
    %% FASE 2: INFERENCIA (ONLINE)
    %% =========================
    subgraph F2["FASE 2 · INFERENCIA Y RESPUESTA (Proceso Online / Tiempo Real)"]
        B1["5️⃣ Consulta del usuario<br/><small>¿Cómo funciona X en mi empresa?</small>"]
        B2["6️⃣ Búsqueda semántica<br/><small>Recuperación de fragmentos relevantes</small>"]
        B3["7️⃣ Aumentación<br/><small>Consulta + contexto recuperado</small>"]
        B4["8️⃣ Modelo LLM<br/><small>Generación basada en contexto inyectado</small>"]
        B5["9️⃣ Respuesta final<br/><small>Respuesta precisa, veraz y citada</small>"]

        B1 --> B2 --> B3 --> B4 --> B5
    end

```


Por esta razón, RAG debe entenderse como un **sistema**, no como una simple técnica.
## Desglose del pipeline

- Datos → [[RAG - Ingesta de Datos]]
- Representación semántica → [[RAG - Embeddings y Vector DB]]
- Recuperación → [[RAG - Recuperación]]
- Generación → [[RAG - Generación]]
- Validación → [[RAG - Evaluación]]