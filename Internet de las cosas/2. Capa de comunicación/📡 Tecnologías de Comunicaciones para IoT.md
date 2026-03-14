 ### 🔹 Proximidad

**RFID (Radio Frequency Identification)**  
Tecnología para identificación de objetos mediante etiquetas que transmiten un identificador único por radiofrecuencia. No requiere línea de vista directa. Un sistema RFID se compone de etiqueta, lector y aplicación de procesamiento.

**NFC (Near Field Communication)**  
Comunicación inalámbrica de corto alcance y alta frecuencia. Soporta comunicación unidireccional y bidireccional. Usada en pagos sin contacto, control de acceso, identificación, automatización de smartphones y aplicaciones deportivas. Ofrece mayor seguridad y privacidad que RFID.

---

### 🔹 Área personal (WPAN)

**Bluetooth Classic**  
Opera en la banda ISM de 2.4 GHz. Usado principalmente para transmisión de audio y datos (auriculares, altavoces, sistemas de entretenimiento). Mayor consumo energético.

**Bluetooth Low Energy (BLE)**  
Diseñado para bajo consumo. Soporta topologías punto a punto, difusión y malla. Ampliamente usado en IoT, localización en interiores y servicios de posicionamiento.

- v4.2: hasta 50 m (exterior), 31 bytes por mensaje
    
- v5: hasta 200 m (exterior), 255 bytes por mensaje
    

---

### 🔹 IEEE 802.15.4 y derivados

**IEEE 802.15.4**  
Estándar base para redes inalámbricas de baja velocidad, bajo costo y bajo consumo energético. Opera en 868 MHz, 915 MHz y 2.4 GHz. Base de múltiples protocolos IoT.

**Zigbee**  
Basado en IEEE 802.15.4. Utilizado en automatización del hogar y dispositivos médicos. Opera en banda ISM 2.4 GHz. Cuenta con certificación para interoperabilidad.

**WirelessHART**  
Orientado a automatización industrial y control de procesos. Alta confiabilidad (≈99.9%), robusto frente a interferencias y compatible con dispositivos HART existentes.

---

### 🔹 Área local (WLAN)

**WiFi (IEEE 802.11)**  
Tecnología inalámbrica ampliamente utilizada. Opera en bandas de 2.4, 5, 6 y 60 GHz.

- WiFi 6: hasta ~10 Gbps y ~120 m de cobertura
    
- WiFi 7 (en desarrollo): hasta ~46 Gbps
    

**WiFi HaLow (IEEE 802.11ah)**  
Diseñado para IoT. Opera en banda ISM de 900 MHz. Ofrece bajo consumo, mayor alcance y mejor penetración de obstáculos. Aplicable a hogar inteligente, ciudad inteligente, industria, agricultura, salud y automatización.

---

### 🔹 Área amplia (WWAN / LPWAN)

**Sigfox**  
Red LPWAN de bajo consumo y largo alcance para transmisión de mensajes pequeños. No licenciada. La complejidad se gestiona en la nube. No requiere infraestructura propia del usuario. Adecuada para comunicaciones simples y resilientes.

**LoRaWAN**  
Protocolo LPWAN que define la arquitectura de red; LoRa corresponde a la capa física. Permite comunicación bidireccional, movilidad y seguridad extremo a extremo. Los nodos pueden ser escuchados por múltiples pasarelas sin necesidad de handover.

**NB-IoT (Narrowband IoT)**  
Tecnología LPWAN basada en LTE (3GPP Release 13). Opera en espectro licenciado. Bajo consumo, buena penetración en interiores. No soporta movilidad (sin handover). Ideal para dispositivos estacionarios.

**LTE-M**  
Tecnología LPWAN basada en LTE. Mayor velocidad y menor latencia que NB-IoT. Soporta movilidad y handover. Adecuada para dispositivos móviles, wearables, seguimiento de activos y aplicaciones con voz.

---

| Tecnología        | Área de cobertura | Banda / Espectro     | Consumo energético | Tasa de datos        | Movilidad | Casos de uso típicos |
|------------------|------------------|----------------------|--------------------|----------------------|-----------|---------------------|
| RFID             | Proximidad       | No licenciada        | Muy bajo           | Muy baja             | No        | Identificación de objetos |
| NFC              | Proximidad       | No licenciada        | Bajo               | Baja                 | No        | Pagos, acceso, identidad |
| Bluetooth Classic| WPAN             | 2.4 GHz (ISM)        | Medio              | Media                | Limitada  | Audio, periféricos |
| BLE              | WPAN             | 2.4 GHz (ISM)        | Muy bajo           | Baja                 | Limitada  | IoT, beacons, sensores |
| IEEE 802.15.4    | WPAN             | 868/915/2.4 GHz      | Muy bajo           | Baja                 | Limitada  | Base de Zigbee, IoT |
| Zigbee           | WPAN             | 2.4 GHz (ISM)        | Muy bajo           | Baja                 | Limitada  | Hogar inteligente |
| WirelessHART     | WPAN / Fábrica   | 2.4 GHz              | Bajo               | Baja                 | Limitada  | Automatización industrial |
| WiFi             | WLAN             | 2.4/5/6/60 GHz       | Alto               | Muy alta             | Sí        | Internet, video |
| WiFi HaLow       | WLAN             | 900 MHz (ISM)        | Bajo               | Media                | Sí        | IoT de largo alcance |
| Sigfox           | LPWAN / WWAN     | No licenciada        | Muy bajo           | Muy baja             | Limitada  | Sensores simples |
| LoRaWAN          | LPWAN / WWAN     | No licenciada        | Muy bajo           | Baja                 | Sí        | Seguimiento, sensores |
| NB-IoT           | LPWAN / WWAN     | Licenciada (LTE)     | Muy bajo           | Muy baja             | No        | Sensores fijos |
| LTE-M            | LPWAN / WWAN     | Licenciada (LTE)     | Bajo               | Media (~1 Mbps)      | Sí        | Activos móviles, wearables |
