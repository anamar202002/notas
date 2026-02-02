## Ventajas del modelo por capas
- Permite identificar y reconocer las relaciones entre los componentes del sistema.
- Proporciona una simplificación conceptual del sistema.
- Introduce modularidad, facilitando la modificación de la implementación de una capa sin afectar a las demás.

## Limitaciones del modelo por capas
- Una capa puede duplicar funcionalidades de otra capa inferior, como la recuperación de errores.
- Una capa puede requerir información que solo existe en otra capa, por ejemplo, marcas temporales, violando el principio de separación de capas.

## Relacionado
- [[IoT Modelo por Capas]]
