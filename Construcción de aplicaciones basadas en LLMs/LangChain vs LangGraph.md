## Comparación de modelos y consideraciones prácticas

En esta sección se comparan los modelos de lenguaje propietarios consumidos mediante API con los modelos ejecutados de forma local, a partir de la experiencia obtenida al adaptar los ejemplos en `LangChain` y `LangGraph`. El objetivo no es determinar cuál enfoque es mejor en términos absolutos, sino identificar en qué escenarios resulta más conveniente cada uno.

## Costos de uso

Desde el punto de vista de costos, los modelos ejecutados localmente eliminan el pago por uso asociado a las APIs propietarias. Una vez descargado el modelo, su ejecución no genera costos adicionales por número de solicitudes o tokens procesados. En contraste, los modelos consumidos mediante API facilitan el acceso a modelos de mayor capacidad y mejor desempeño general, pero implican costos recurrentes que dependen directamente del volumen de uso de la aplicación.

## Latencia y uso de recursos

En términos de latencia, los modelos locales pueden ofrecer tiempos de respuesta adecuados para tareas simples, especialmente cuando se ejecutan en el mismo entorno donde corre la aplicación. No obstante, su desempeño está fuertemente condicionado por el hardware disponible, como CPU, GPU y memoria. Los modelos consumidos vía API, por su parte, suelen ejecutarse en infraestructura optimizada, lo que permite obtener respuestas rápidas y consistentes incluso para modelos de gran tamaño, a costa de una dependencia permanente de la conectividad de red.

## Control y flexibilidad

El control y la flexibilidad son aspectos donde los modelos locales presentan una ventaja clara. Ejecutar el modelo en el propio entorno permite decidir exactamente qué versión utilizar, cuándo actualizarla y cómo integrarla con el sistema. Gracias a la abstracción que ofrecen `LangChain` y `LangGraph`, el cambio entre distintos modelos locales o remotos puede realizarse de forma transparente, sin necesidad de modificar la lógica central de la aplicación.

## Privacidad y manejo de datos

La privacidad y el manejo de datos son factores clave al elegir un modelo local. En este enfoque, las entradas y salidas permanecen dentro del entorno de ejecución, lo cual resulta especialmente relevante en escenarios donde se manejan datos sensibles o regulados. En el caso de los modelos consumidos mediante API, aunque los proveedores suelen ofrecer garantías de seguridad, los datos deben ser enviados a servicios externos, lo que puede no ser adecuado en todos los contextos.

## Limitaciones de los modelos locales

A pesar de sus ventajas, los modelos locales presentan limitaciones importantes que deben considerarse. En general, estos modelos suelen tener menor capacidad que los modelos propietarios más avanzados y no siempre cuentan con información actualizada. Un ejemplo claro de esto es el modelo `gemma3:1b` el cual, a pesar de también ser desarrollado por Google, no puede responder correctamente a preguntas relacionadas con herramientas o frameworks recientes, como `LangChain`, debido a que su conocimiento está limitado al momento en que fue entrenado y a la cantidad de parámetros presentes en el modelo.

Esta limitación resulta especialmente relevante en tareas que dependen de información actualizada, documentación reciente o cambios frecuentes en el ecosistema de herramientas. En estos casos, los modelos consumidos mediante API suelen ofrecer mejores resultados, ya que generalmente incorporan entrenamientos más recientes y capacidades más avanzadas.

## Escenarios de uso recomendados

En la práctica, los modelos locales resultan especialmente útiles para prototipos, aplicaciones educativas, pruebas de concepto o escenarios donde el control, la privacidad y la reducción de costos son prioritarios. Por otro lado, los modelos consumidos mediante API suelen ser más adecuados para aplicaciones en producción que requieren mayor calidad de respuesta, conocimiento actualizado y escalabilidad inmediata.

Con esta comparación se refuerza la idea central del tutorial, gracias a `LangChain` y `LangGraph`, es posible cambiar entre modelos locales y modelos remotos de forma transparente, permitiendo elegir el enfoque más adecuado según las necesidades específicas de cada aplicación.