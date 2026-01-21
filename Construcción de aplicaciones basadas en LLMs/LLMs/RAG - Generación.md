# Generación de Respuestas

En la etapa de generación, el LLM recibe tres insumos principales:
- Instrucciones del sistema.
- La pregunta del usuario.
- El contexto recuperado.

El modelo no debe tratarse como una fuente de conocimiento autónoma, sino como un componente encargado de **razonar, sintetizar y redactar** a partir de la información proporcionada.

Buenas prácticas enfatizadas en la lectura incluyen:
- Separar claramente las instrucciones del contexto recuperado.
- Limitar la longitud de la respuesta para controlar costos.
- Forzar al modelo a basar sus afirmaciones únicamente en el contexto.

Esta etapa es especialmente sensible a problemas de seguridad y confiabilidad, ya que una mala delimitación del contexto puede inducir comportamientos no deseados.

Relacionado con:
- [[RAG - Seguridad y Producción]]
- [[RAG - Observabilidad y Costos]]
