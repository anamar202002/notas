Evaluar un sistema RAG requiere abandonar métricas tradicionales deterministas. La lectura subraya que la calidad es el resultado de la interacción entre recuperación y generación.

Las métricas especializadas permiten descomponer el problema:
- **Faithfulness** evalúa si la respuesta es fiel al contexto.
- **Answer relevance** mide si responde a la pregunta.
- **Context precision y recall** analizan la calidad de la recuperación.
- **Groundedness** verifica la trazabilidad de cada afirmación.

Frameworks como RAGAS y TruLens automatizan estas evaluaciones, utilizando LLMs como jueces. Aun así, la evaluación humana sigue siendo esencial para casos críticos y calibración.

La evaluación no solo mide calidad, sino que guía la mejora continua del sistema.
