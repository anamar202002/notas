La ingesta es la base de cualquier sistema RAG. Su función es transformar información heterogénea y no estructurada en contenido listo para ser indexado y recuperado de forma eficiente.

Las fuentes de datos pueden incluir documentación técnica, manuales internos, políticas corporativas, tickets de soporte, correos electrónicos, bases de conocimiento o registros históricos. Cada tipo de fuente introduce desafíos distintos en términos de extracción y limpieza.

### Etapas
1. **Extracción de texto**, adaptada al formato (PDF, HTML, DOCX, etc.).
2. **Limpieza y normalización**, eliminando encabezados repetidos, ruido, caracteres inválidos y contenido irrelevante.
3. **Estandarización**, asegurando coherencia en fechas, unidades, nombres y estructuras.
4. **Control de versiones**, para permitir actualizaciones incrementales del corpus.

### Fuentes comunes
- PDFs
- HTML / Confluence
- Word / Excel
- Bases de datos
- APIs internas

Un aspecto crítico señalado en la lectura es la **sanitización de contenido**. En sistemas RAG, los documentos no son datos pasivos: se convierten en contexto que influye directamente en el comportamiento del LLM. Esto abre la puerta a ataques como la inyección de prompts a través de documentos, lo que obliga a tratar la ingesta como una superficie de ataque.

Relacionado con:
- [[RAG - Seguridad y Producción]]