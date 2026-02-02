La **capa de comunicaciones** en los sistemas IoT es responsable de transmitir de forma segura los datos desde los dispositivos inteligentes hacia los sistemas de procesamiento, usualmente a través de una o dos tecnologías: una para conectar los dispositivos con un _gateway_ y otra para conectar el _gateway_ con la nube.

Las comunicaciones IoT deben ser **de bajo costo y bajo consumo energético**, permitir **larga duración de batería**, **alto número de conexiones**, **diferentes tasas de transmisión**, **largo alcance** y una **arquitectura de red simple**.

### 📡 Tecnologías de comunicación

Las tecnologías IoT pueden clasificarse según su **área de cobertura**, incluyendo:

- Redes de proximidad (ej. NFC)
    
- WPAN, WHAN, WFAN
    
- WLAN, WNAN, WWAN
    
- LPWAN (ej. SIGFOX, LoRa)
    

Existen tecnologías consolidadas como **Bluetooth** y **WiFi**, y otras emergentes impulsadas por el crecimiento del IoT, como **WiFi HaLow**, **SIGFOX** y **LoRa**.

### ⚙️ Criterios de selección

Para elegir una tecnología de comunicación IoT se deben considerar:

- Rango de cobertura
    
- Tasa máxima de transferencia
    
- Consumo energético
    
- Costo de transmisión
    
- Zona de despliegue (urbana o rural)
    
- Uso del espectro (licenciado o no licenciado)
    
- Tipo de servicio (público o privado)
    
- Necesidad de infraestructura propia o de un operador
    

### 🧪 Caso MySUDS

En el sistema de drenaje urbano **MySUDS**, se eligió **SIGFOX** por su bajo tamaño de mensajes, alta frecuencia de transmisión, cobertura urbana de hasta 5 km y porque no requiere infraestructura propia, ya que cuenta con operador en Colombia.

### ✅ Conclusión

La selección de la tecnología de comunicaciones en IoT debe alinearse con los **requerimientos de diseño del sistema**, ya que impacta directamente atributos de calidad como el **desempeño** y la **seguridad de la información**.