La **seguridad en Internet de las Cosas (IoT)** debe abordarse de forma **integral y de extremo a extremo**, considerando dispositivos, datos, red y nube, debido a la diversidad de aplicaciones (hogar, edificios, industria) y a las **limitaciones propias de los dispositivos IoT**.

---

### 🧩 Componentes y visión end-to-end

En un sistema IoT es clave asegurar procesos como:

- Actualización de firmware
    
- Emparejamiento y vinculación con controladores
    
- Autenticación y control local/remoto
    
- Detección, notificación y análisis de datos (Edge, Fog y Cloud)
    

---

### ⚠️ Tipos de amenazas

- **Amenazas contra IoT**: hackeo de dispositivos (cámaras IP), ataques DDoS, botnets, inyección SQL.
    
- **Amenazas de IoT**: uso de dispositivos IoT para lanzar ataques (ej. XSS, acceso a datos privados).
    

---

### 🚧 Limitaciones de los dispositivos IoT

- **Hardware**: bajo poder computacional, energía y almacenamiento.
    
- **Software**: sistemas operativos limitados y dificultad para aplicar parches.
    
- **Comunicaciones**: múltiples protocolos y movilidad que dificultan usar seguridad tradicional.
    

---

## 🛡️ Niveles de seguridad en IoT

### 1️⃣ Seguridad de la información

- **Confidencialidad**: acceso solo a usuarios autorizados, protección de privacidad.
    
- **Integridad**: evitar manipulación de datos y dispositivos.
    
- **No repudio**: impedir la negación de autoría.
    
- **Actualización (freshness)**: asegurar que los datos sean actuales.
    

> Se requieren **mecanismos livianos** (bajo consumo energético), ya que soluciones tradicionales pueden ser inviables.

---

### 2️⃣ Seguridad de acceso

- **Identificación**: reconocimiento de dispositivos y usuarios.
    
- **Autenticación**: verificación de identidad y credibilidad.
    
- **Autorización**: acceso solo a recursos permitidos.
    
- **Control de acceso**: validación continua de permisos.
    

---

### 3️⃣ Seguridad funcional

- **Disponibilidad**: acceso continuo a datos y servicios, incluso ante fallos.
    
- **Manejo de excepciones y resiliencia**: tolerancia a fallos de hardware/software.
    
- **Autoorganización**: operación segura ante fallos o agotamiento energético.
    

---

## 🚀 Retos clave en seguridad IoT

- Criptografía eficiente para dispositivos con recursos limitados
    
- Interoperabilidad entre distintos dispositivos
    
- Escalabilidad de los mecanismos de seguridad
    
- Protección de la privacidad
    
- Resiliencia ante ataques físicos
    
- Control autónomo y seguridad en la nube
    

---

### 📌 Enfoque recomendado

Abordar la seguridad **por capas de la arquitectura IoT**, adaptando mecanismos según el tipo de aplicación y sus riesgos específicos.