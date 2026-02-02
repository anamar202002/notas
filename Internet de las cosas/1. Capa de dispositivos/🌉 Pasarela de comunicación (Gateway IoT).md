
> [!summary] ¿Qué es?
> **Enlace de comunicación** entre los **dispositivos de borde** (sensores y actuadores) y la **nube IoT** y por extensión, con las aplicaciones del sistema.
> Pueden ser físicos o un software

## 🔧 Funciones principales de una pasarela IoT

Una pasarela IoT puede encargarse de:

- **Recolección de datos** desde sensores y actuadores.
    
- **Preprocesamiento de datos**:
    
    - Agregación.
        
    - Compresión.
        
    - Filtrado.
        
- **Traducción de protocolos** para soportar interoperabilidad.
    
- **Seguridad**:
    
    - Cifrado de datos.
        
    - Protección contra accesos no autorizados.
        
- **Gestión de dispositivos IoT** conectados.
    
- **Enrutamiento de paquetes** hacia la nube.
    
- **Soporte de calidad de servicio (QoS)**.
    
- **Computación en el borde (Edge Computing)**.
    

---

## 🧩 Tipos de pasarelas IoT (a nivel abstracto)

### 1. Pasarela central

- No integra sensores.
    
- El software de la pasarela:
    
    - Recibe datos de sensores externos.
        
    - Preprocesa y transmite a la nube.
        
- Arquitectura más simple.
    

### 2. Pasarela integrada

- Integra pasarela + sensores en un mismo dispositivo.
    
- Cada dispositivo final incorpora la funcionalidad de gateway.
    
- Útil para dispositivos autónomos y despliegues masivos.
    
- Requiere desarrollo de hardware personalizado.

|Característica|Pasarela Central|Pasarela Integrada|
|---|---|---|
|Ubicación de la pasarela|Dispositivo independiente|Integrada en cada dispositivo final|
|Sensores incorporados|❌ No|✅ Sí|
|Arquitectura|Sensores → Gateway → Nube|Dispositivo (sensor + gateway) → Nube|
|Complejidad del dispositivo final|Baja|Alta|
|Desarrollo de hardware|Uso de componentes existentes|Hardware personalizado|
|Escalabilidad|Media–Alta|Alta (en despliegues masivos)|
|Integración de sensores externos|✅ Fácil|❌ Limitada|
|Costo inicial|Menor|Mayor|
|Tiempo de implementación|Menor|Mayor|
|Casos de uso típicos|Automatización industrial, agricultura, domótica|Dispositivos autónomos, wearables, sensores inteligentes|
|Dependencia de conectividad local|Alta|Baja|
|Ejemplo típico|Gateway IoT centralizado|Nodo IoT todo-en-uno|
    

---

## 🔄 Evolución de las pasarelas IoT

Las pasarelas modernas pueden:

- Recibir, almacenar en buffer y reprocesar datos.
    
- Convertir protocolos heterogéneos.
    
- Soportar múltiples interfaces de comunicación:
    
    - Zigbee
        
    - Bluetooth
        
    - LTE
        
    - Wi-Fi
        
- Gestionar seguridad avanzada.
    
- Administrar los dispositivos conectados.
    

---

## 🏗️ Arquitectura genérica de una pasarela IoT

``` mermaid
flowchart TB
    subgraph Dispositivos_Borde["Dispositivos de Borde"]
        S[Sensor]
        A[Actuador]
    end

    subgraph Gateway["Pasarela IoT"]
        HW[Capa de Hardware]
        OS[Sistema Operativo]
        HAL[Abstracción de Hardware]
        CON[Conectividad]
        DATA[Gestión de Datos]
        SEC[Seguridad]
        SRV[Abstracción de Servicios]
    end

    CLOUD[Nube IoT / Aplicaciones]

    S --> Gateway
    A --> Gateway
    Gateway --> CLOUD

    HW --> OS
    OS --> HAL
    HAL --> CON
    CON --> DATA
    DATA --> SEC
    SEC --> SRV

```

### 1. Capa de hardware

Incluye:

- Sensores (opcional).
    
- Procesador.
    
- Módulos de comunicación.
    
- Memoria y capacidad de cómputo.
    

📌 La elección del hardware depende de:

- Complejidad de las aplicaciones IoT.
    
- Sistema operativo subyacente.
    

---

### 2. [[💻 Sistemas Operativos IoT]] de la pasarela

- Diseñado según los requisitos de la aplicación.
    
- Puede ser:
    
    - **RTOS** (tiempo real).
        
    - **Linux**.
        
    - **Android** (para aplicaciones con interfaz gráfica).
        

---

### 3. Capa de abstracción de hardware

- Permite independencia entre software y hardware.
    
- Reduce costos de rediseño.
    
- Facilita la portabilidad de aplicaciones IoT.
    

---

### 4. Módulos de conectividad

- Redes de baja potencia:
    
    - RFID
        
    - Zigbee
        
    - Bluetooth
        
- Redes hacia la nube:
    
    - Wi-Fi
        
    - Redes celulares
        
    - Conectividad cableada o inalámbrica.


| Tecnología    | Alcance aprox. | Tasa de datos | Consumo energético | Costo    | Espectro     |
| ------------- | -------------- | ------------- | ------------------ | -------- | ------------ |
| **RFID**      | ~1 m           | Muy baja      | Muy bajo           | Bajo     | Sin licencia |
| **Bluetooth** | ~10 m          | Media         | Bajo               | Bajo     | Sin licencia |
| **Zigbee**    | ~100 m         | Baja          | Bajo               | Bajo     | Sin licencia |
| **Wi-Fi**     | ~100 m         | Alta          | Alto               | Medio    | Sin licencia |
| **LTE-M**     | ~1 km          | Media         | Media              | Alto     | Licenciado   |
| **NB-IoT**    | ~5 km          | Baja          | Muy bajo           | Bajo     | Licenciado   |
| **LoRaWAN**   | ~15 km         | Muy baja      | Muy bajo           | Muy bajo | Sin licencia |

> [!info]
> A mayor alcance de comunicación, menor es la tasa de datos y menor el consumo energético, especialmente en tecnologías LPWAN como NB-IoT y LoRaWAN.


``` mermaid
flowchart LR
    RFID["RFID\n1 m"]
    BT["Bluetooth\n10 m"]
    ZB["Zigbee\n100 m"]
    WIFI["Wi-Fi\n100 m"]
    LTEM["LTE-M\n1 km"]
    NBIOT["NB-IoT\n5 km"]
    LORA["LoRaWAN\n15 km"]

    RFID --> BT --> ZB --> WIFI --> LTEM --> NBIOT --> LORA

```

---

### 5. Capa de reenvío de datos y conversión de protocolos

Incluye:

- **Selección de red**: identifica la red disponible.
    
- **Selección de interfaz**: elige la interfaz adecuada.
    
- **Adaptación**: ajusta tamaños de paquetes y protocolos.
    

---

### 6. Capa de abstracción de servicios

- Proporciona interfaces estándar.
    
- Facilita el acceso de las aplicaciones a las tecnologías de red.
    

---

### 7. Gestión de dispositivos

- Seguimiento de sensores conectados.
    
- Configuración básica de dispositivos.
    
- Acceso y control de datos desde la pasarela.
    

---

### 8. Gestión de datos

- Transmisión de datos a la nube.
    
- Filtrado y almacenamiento temporal.
    
- Soporte ante fallos de conectividad con la nube.
    

---

### 9. Capa de seguridad

- Autenticación criptográfica.
    
- Cifrado de todas las transmisiones.
    
- Protección de:
    
    - Dispositivos.
        
    - Datos.
        
    - Redes.
        

---

## 🧠 Selección de una pasarela IoT

La selección depende de:

- La **arquitectura IoT**:
    
    - Pasarela integrada.
        
    - Pasarela central.
        
- El **contexto de la aplicación**:
    
    - Salud.
        
    - Seguridad.
        
    - Agricultura.
        
    - Automatización industrial.
        
    - Vehículos autónomos.
        

### Factores clave de selección:

- Consumo energético.
    
- Capacidad de almacenamiento local.
    
- Soporte a múltiples lenguajes:
    
    - C, C++, Python, entre otros.
        
- Seguridad integrada.
    
- Soporte OTA (actualización remota de firmware).
    
- Compatibilidad con protocolos:
    
    - TCP/IP, HTTP, UDP, IPv4, IPv6.
        
    - MQTT, CoAP, 6LoWPAN.
        
- Soporte de **computación en el borde**.
    

---

## 🎯 Beneficios del uso de gateways IoT

- Mejora de tiempos de respuesta.
    
- Mayor seguridad del sistema.
    
- Optimización del consumo energético.
    
- Reducción de costos de infraestructura.
    
- Mayor escalabilidad y flexibilidad del sistema IoT.