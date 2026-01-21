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
