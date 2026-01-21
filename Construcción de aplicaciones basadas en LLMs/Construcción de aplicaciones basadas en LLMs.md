Large Language Model
# Semana 1
- [[Índice casos de uso, costos y arquitectura]]
## Arquitectura de aplicaciones basadas en LLMs
Antes teníamos un front que se conectaba al back mediante una API, ahora con los LLM es más complejo el tema.
Ahora hay un preprocesamiento que llama al orquestador LLM:
- ¿se debe buscar en otro lado? (bases de k)
- herramientas externas
- solo LLM
ahora hay dos componentes nuevos:
- Memoria: guarda la info para mantener contexto, personalizar respuestas
- Observabilidad: costos y latencia de los modelos
La latencia y escalabilidad se pueden ver más afectadas a raíz de los LLMs

Seguridad y privacidad:
- normativas específicas, manejo seguro de la memoria
- Gestión de errores y moderación
	- pos-procesamiento
```mermaid
flowchart TD
    %% =========================
    %% USUARIO
    %% =========================
    U[Usuario]

    %% =========================
    %% FRONT-END
    %% =========================
    subgraph FE["Front-End"]
        UI["Interfaz de Usuario (UI)"]
    end

    U --> UI

    %% =========================
    %% BACK-END
    %% =========================
    subgraph BE["Back-End"]
        PRE["Pre-procesamiento<br/><small>Limpieza, formato de prompt</small>"]

        POST["Post-procesamiento<br/><small>Validación, formato, moderación</small>"]

        OBS["Observabilidad<br/><small>Logs, métricas y trazas</small>"]

        MEM["Memoria<br/><small>Base de datos para guardar contexto</small>"]

        %% =========================
        %% ORQUESTADOR LLM
        %% =========================
        subgraph ORQ["Orquestador LLM"]
            RAG["(1) Búsqueda RAG<br/><small>Base de datos vectorial</small>"]
            TOOLS["(2) Herramientas<br/><small>APIs, funciones, etc.</small>"]
            LLM["(3) Llamado al LLM<br/><small>Generación de texto</small>"]
        end
    end

    %% =========================
    %% FLUJO PRINCIPAL
    %% =========================
    UI -->|Llamada a API| PRE

    PRE --> RAG
    PRE --> TOOLS
    PRE --> LLM

    MEM --> RAG

    RAG --> LLM
    TOOLS --> LLM

    LLM --> POST
    POST --> UI

    %% =========================
    %% OBSERVABILIDAD
    %% =========================
    RAG --> OBS
    TOOLS --> OBS
    LLM --> OBS
    POST --> OBS

```