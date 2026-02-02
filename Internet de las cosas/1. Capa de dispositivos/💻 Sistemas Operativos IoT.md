Los **sistemas operativos (SO) en IoT** son una capa fundamental que soporta la ejecución de aplicaciones, la gestión del hardware y la conectividad. Aunque derivan de los sistemas operativos embebidos, IoT introduce **restricciones adicionales** de recursos, energía y conectividad.

---

## 🔀 Tipos de sistemas operativos IoT

Según el tipo de dispositivo, los SO IoT se clasifican en:

### 1. Sistemas operativos para dispositivos finales

- Ejecutan en nodos IoT (sensores/actuadores).
    
- Recursos muy limitados:
    
    - Memoria
        
    - Procesamiento
        
    - Energía
        
- Alta eficiencia y bajo consumo.
    

### 2. Sistemas operativos para pasarelas (gateways)

- Ejecutan en dispositivos con mayor capacidad.
    
- Soportan:
    
    - Preprocesamiento de datos
        
    - Seguridad avanzada
        
    - Conectividad heterogénea
        
    - Computación en el borde
        

---

## ⚠️ Importancia de la elección del SO

- El sistema operativo es la **base del sistema IoT**.
    
- Cambiarlo implica:
    
    - Refactorización de aplicaciones.
        
    - Reescritura de controladores.
        
- En muchos casos:
    
    - El fabricante recomienda el SO.
        
    - En hardware personalizado, la elección es más compleja.
        

---

## 🧩 Criterios de selección de un sistema operativo IoT

### 🔹 Características técnicas clave

- **Huella (footprint)**: bajo uso de memoria y CPU.
    
- **Escalabilidad**: uso del mismo SO en nodos y pasarelas.
    
- **Portabilidad**: independencia del hardware.
    
- **Modularidad**: kernel mínimo + módulos opcionales.
    
- **Conectividad**:
    
    - Ethernet
        
    - Wi-Fi
        
    - Bluetooth
        
    - IEEE 802.15.4
        
- **Seguridad**:
    
    - Arranque seguro
        
    - SSL/TLS
        
    - Cifrado por hardware
        
- **Fiabilidad**:
    
    - Operación prolongada en entornos remotos
        
    - Certificaciones industriales
        
- **Lenguajes soportados**:
    
    - Principalmente C y C++
        
    - En algunos casos Python u otros
        

---

## ❓ Preguntas clave para elegir un SO IoT

- ¿Es comercial o de código abierto?
    
- ¿Requiere contrato de soporte?
    
- ¿Necesita **tiempo real (RTOS)**?
    
- ¿Qué arquitectura soporta?
    
    - ARM
        
    - x86
        
- ¿Soporta:
    
    - Memoria virtual?
        
    - Caché multinivel?
        
    - Punto flotante?
        
- ¿Cómo se gestionan paquetes y extensiones?
    
- ¿Cómo arranca el sistema?
    
    - Flash
        
    - Red
        
- ¿Incluye servicios de seguridad integrados?
    
- ¿Permite reducir RAM y almacenamiento?
    
- ¿El tiempo de arranque es crítico?
    
- ¿Qué sistemas de archivos soporta?
    
- ¿Soporta los drivers del hardware?
    
- ¿Requiere interfaz gráfica (GUI)?
    

---

## 🌍 Sistemas operativos IoT existentes

### 🧑‍💻 Código abierto

- **TinyOS** – académico, uno de los más antiguos.
    
- **Contiki** – académico, ampliamente usado.
    
- **RIOT** – comunidad activa y moderna.
    
- **FreeRTOS** – uno de los más populares.
    
- **LiteOS** – desarrollado por Huawei.
    
- **ARM Mbed OS** – optimizado para ARM.
    
- **Zephyr OS** – kernel compilado estáticamente.
    
- **Ubuntu Core** – basado en paquetes tipo _snapshots_.
    
- **Yocto** – plataforma para crear Linux personalizados.
    

### 🏢 Comerciales

- **Windows 10 IoT**
    
- **Particle**
    
- **Android Things**
    

👉 Preferidos en sectores donde **seguridad y confiabilidad** son críticas:

- Aeroespacial
    
- Automotriz
    
- Industrial
    
- Salud
    

---

## ⏱️ Sistemas operativos en tiempo real (RTOS)

- Identificables por “RTOS” en su nombre.
    
- Garantizan procesamiento dentro de límites de tiempo.
    
- Ideales cuando:
    
    - Hay múltiples hilos.
        
    - Se deben cumplir plazos estrictos.
        
    - Se comparten recursos.
        

---

## 🐧 Linux en IoT

- Filosofía IoT:
    
    - **Imagen mínima**
        
    - Solo paquetes necesarios
        
- Ventaja:
    
    - Flexibilidad
        
    - Modularidad
        
- Evita:
    
    - Consumo innecesario de RAM y almacenamiento
        

---

## 🛠️ Buildroot

- Herramienta para crear Linux embebido.
    
- Permite:
    
    - Compilación cruzada.
        
    - Construcción del kernel.
        
    - Creación del sistema de archivos raíz.
        
    - Generación del bootloader.
        
- Soporta múltiples plataformas:
    
    - Raspberry Pi
        
    - Cubieboard
        
    - BeagleBone
        
- Ideal para dispositivos con **recursos muy limitados**.
    

---

## 🌐 Computación en el borde y EVE-OS

El crecimiento de IoT impulsa la **computación en el borde** por:

- Latencia
    
- Seguridad
    
- Privacidad
    
- Ahorro de ancho de banda
    

### 🔹 EVE-OS

- Sistema operativo abierto basado en Linux.
    
- Objetivo:
    
    - Hacer para el borde lo que Android hizo para móviles.
        
- Características:
    
    - Soporte Docker
        
    - Kubernetes
        
    - Máquinas virtuales
        
- Base flexible para hardware y aplicaciones heterogéneas.
    

---

## ✅ Reflexión final

- Un dispositivo IoT **no siempre necesita un SO**.
    
- Pero:
    
    - La complejidad creciente lo hace cada vez más necesario.
        
    - Especialmente los **RTOS**.
        
- La elección depende del **contexto**:
    
    - Estándares industriales.
        
    - Consumo energético.
        
    - Arquitectura del hardware.
        
    - Fuente de alimentación (batería vs red eléctrica).