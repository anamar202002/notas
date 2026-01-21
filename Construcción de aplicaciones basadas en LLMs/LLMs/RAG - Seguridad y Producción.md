Llevar RAG a producción implica enfrentar retos de escalabilidad, seguridad y cumplimiento normativo.

En términos de seguridad, la lectura destaca riesgos específicos:
- Inyección de prompts a través de documentos indexados.
- Exposición de datos sensibles.
- Falta de control de acceso contextual.

Las mitigaciones incluyen:
- Sanitización estricta en la ingesta.
- Separación lógica entre instrucciones y contexto.
- Controles de acceso por usuario.
- Auditoría y trazabilidad completas.

Desde el punto de vista operativo, problemas como el versionamiento de [[RAG - Embeddings y Vector DB|embeddings]], la actualización incremental de índices y el derecho al olvido deben resolverse desde el diseño inicial.

Un sistema RAG en producción es tanto un desafío técnico como organizacional.


### Escalabilidad

Retos principales:

- Crecimiento masivo de documentos.
    
- Incremento de usuarios.
    
- Requisitos estrictos de latencia.
    
- Reindexación incremental.
    
- Versionamiento de embeddings.
    

### Seguridad

Riesgos clave:

- **Inyección de prompts vía documentos**.
    
- Exposición de datos confidenciales.
    
- Acceso no autorizado a información indexada.
    

Mitigaciones:

- Sanitización en la ingesta.
    
- Separación estricta entre instrucciones del sistema y contexto.
    
- Controles de acceso por usuario.
    
- Auditoría, trazabilidad y derecho al olvido.