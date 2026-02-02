## 🌐 Capa de dispositivos en sistemas IoT

La **capa de dispositivos** es responsable de:

- Recolectar datos del entorno físico mediante **sensores**.
    
- Transmitir dichos datos a capas superiores usando **interfaces de servicio**.
    
- Ejecutar acciones sobre el entorno mediante **actuadores**.
    

Está compuesta por **dispositivos inteligentes** y **pasarelas de comunicación**.

---

## 🤖 Dispositivos inteligentes

Un dispositivo inteligente combina un **objeto físico** con un **componente electrónico**, que puede incluir:
``` mermaid
flowchart TB
    DI[Dispositivo Inteligente]

    DE[Dispositivo Electrónico]
    DF[Dispositivo Físico]

    ET[Etiqueta]
    S[Sensor]
    A[Actuador]

    DI --> DE
    DI --> DF

    ET -->|Lee| S
    S --> DE
    DE --> A

    A -->|Actúa en| DF
    S -->|Monitorea| DF
    ET -->|Identifica| DF

```

### 🏷️ Etiquetas

- Proveen identificación digital.
    
- Ejemplos: códigos de barras, QR, Aztec, RFID.
    

> [!summary] Nota importante
> Un sensor detecta los cambios ambientales y los convierte en una señal eléctrica.
> Un actuador convierte una señal eléctrica en una salida física en una acción
###  [[📡 Sensores]]

- Capturan estímulos físicos y los convierten en señales eléctricas.
    
- Estímulos comunes: temperatura, presión, humedad, movimiento, luz, sonido, presencia química.
    
- La señal puede expresarse como voltaje, corriente o datos digitales.
    
- Pueden ser:
    
    - **Simples**: lectura y envío de datos.
        
    - **Avanzados**: integran algoritmos inteligentes para análisis del entorno.
        

### [[⚙️ Actuadores]]

- Ejecutan acciones físicas a partir de señales eléctricas.
    
- Convierten energía eléctrica en energía mecánica u otra forma.
    
- Ejemplo: motores eléctricos.
    
- Requieren energía y señal de control.
    

🔋 Los dispositivos pueden operar en **modo activo o reposo** para optimizar el consumo energético.

---

## [[🌉 Pasarela de comunicación (Gateway IoT)]]

La pasarela conecta los dispositivos inteligentes con la red y la nube IoT. Sus funciones incluyen:

- Traducción de protocolos (ej. Bluetooth LE, ZigBee ↔ IP).
    
- Agregación y transmisión de datos.
    
- Preprocesamiento, filtrado y almacenamiento.
    
- Seguridad y análisis de datos.
    

📍 Este procesamiento local previo a la nube se conoce como **computación en el borde (Edge Computing)**.

---

## [[💻 Sistemas Operativos IoT]]

Un **Sistema Operativo IoT** permite:

- Comunicación con la nube y otros dispositivos.
    
- Ejecución de software.
    
- Procesamiento y almacenamiento de datos con recursos limitados.
    

### Tipos:

- **Código abierto**: TinyOS, RIOT, FreeRTOS, Raspbian.
    
- **Código cerrado**: Android Things, Windows 10 IoT, Particle, TI-RTOS.
    

🔁 Los **RTOS** (sistemas operativos en tiempo real) facilitan el desarrollo al gestionar tareas de bajo nivel.

---

## 🌧️ Caso de estudio: MySUDS

Sistema de drenaje urbano inteligente con:

- **Tres puntos de medición**:
    
    - Detección de lluvia.
        
    - Cámara de entrada.
        
    - Cámara de salida.
        
- Sensores para:
    
    - Nivel de agua.
        
    - Conductividad eléctrica.
        
- **Pluviómetros** para activar/desactivar el sistema según eventos de lluvia.
    
- Objetivo: **optimizar consumo energético y prolongar la vida útil**.
    

### Implementación técnica:

- Nodos basados en **NodeMCU** (bajo costo y consumo).
    
- Programación vía **Arduino**.
    
- Comunicación por red **SigFox**.
    
- Uso del sistema operativo **XTOS** (sin explotar todas sus capacidades por simplicidad).
    

---

## ✅ Consideraciones finales

- La selección de hardware y software debe basarse en **requisitos funcionales y de calidad**.
    
- Es clave garantizar:
    
    - **Disponibilidad**.
        
    - **Integridad de los datos**.
        
- La capa de dispositivos es fundamental para la recolección primaria de información en un sistema IoT.