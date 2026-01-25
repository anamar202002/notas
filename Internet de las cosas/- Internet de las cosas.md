# Semana 1
entender que hd y sw tiene impacto
Objetivos:
- diseñar arqui de sw y hd y comunicaciones en un sistema de IoT
- herramientas y técnicas
- Adquisición de un dispositivo de IoT de bajo costo
	- temperatura y humedad relativa
## Origenes, visión y definiciones de un sistema IoT
- se uso en 1999
- en 1982 se creo una máquina de cocacola,  donde se puso microinterruptores diseñado para mostrar el estado de las cocacola
- tostadora conectado via IP para prender o apagar
- Qué es IoT?
	- infra global de la sociedad de la info
	- prestación de servicios avanzados
	- interconexión objetos (fisicos y virtuales) mediante la interoperatividad de TI
	- Unión entre muchas cosas y el internet
``` mermaid
graph TD
    IoT((IoT))

    Persona[Cualquier persona]
    Cosa[Cualquier cosa]
    Momento[Cualquier momento]
    Lugar[Cualquier lugar]
    Red[Desde cualquier red]
    Servicio[Cualquier servicio]
    Contexto[Cualquier contexto]

    IoT --- Persona
    IoT --- Cosa
    IoT --- Momento
    IoT --- Lugar
    IoT --- Red
    IoT --- Servicio
    IoT --- Contexto

    style IoT fill:#1a237e,stroke:#0d47a1,color:#ffffff

```
``` mermaid
---
title: Visión holística del IoT
---
graph TD
    IoT((IoT))

    Hardware((Dimensión de<br/>Hardware))
    Software((Dimensión de<br/>Software))
    Comunicacion((Dimensión de<br/>Comunicación))

    Hardware --- IoT
    Software --- IoT
    Comunicacion --- IoT

    Hardware --- Software
    Hardware --- Comunicacion
    Software --- Comunicacion

    style IoT fill:#9e9e9e,stroke:#616161,color:#000000
    style Hardware fill:#e0e0e0,stroke:#9e9e9e,color:#000000
    style Software fill:#eeeeee,stroke:#bdbdbd,color:#000000
    style Comunicacion fill:#d6d6d6,stroke:#9e9e9e,color:#000000

```

- Aplicación del IoT
	- hogares
	- oficinas
	- fabricas (rutinas de trabajo (auto))
	- Mineria, gas, construcción
		- salud
	- puntos de venta
	- ciudades
		- control adaptativo del trafico
	- Vehículos
		- mantenimiento basado en la situación
	- Cuerpo humano
		- controlar la salud
- Modelo de referencia de IoT  & [[Arquitectura de Referencia IoT]]

## The Internet of Things (IoT) Overview Resumen

[[The Internet of Things (IoT) Overview Resumen]]


## Los dominios de aplicación de los sistemas IoT
- Vehículos conectados, buses, trenes
- vehículos eléctricos o sin conductor
- salud
	- hospitales, clínicas
	- investigación

## Arquitecturas de los sistemas IoT
Los sistemas de **Internet de las Cosas (IoT)** son complejos debido a la gran cantidad de componentes involucrados: dispositivos, protocolos, redes y aplicaciones.  
Para facilitar su análisis y diseño, se utilizan **modelos por capas**, similares al modelo **ISO/OSI** de Internet.

---

## 📚 Modelo por capas: ventajas y desventajas

### ✅ Ventajas

- Facilita el **análisis de sistemas complejos**.
    
- Permite **identificar relaciones** entre componentes.
    
- Proporciona **modularidad**, lo que simplifica cambios o mejoras en una capa sin afectar a las demás.
    

### ⚠️ Desventajas

- **Duplicación de funcionalidades** entre capas (ej. recuperación de errores).
    
- Dependencias entre capas que **rompen la separación** (ej. uso de marcas temporales de otra capa).
    

---

## 🏗️ Arquitecturas IoT propuestas

### 🔹 Arquitectura de tres capas

1. **Capa de percepción**
    
    - Recolección de datos mediante sensores y dispositivos inteligentes.
        
    - Envío de datos a la capa de red.
        
2. **Capa de red (o transmisión)**
    
    - Transporte de datos usando redes integradas, Internet u otras tecnologías de comunicación.
        
3. **Capa de aplicación**
    
    - Provisión de servicios al usuario.
        
    - Incluye almacenamiento de datos, Big Data, minería de datos y análisis semántico.
        

---

### 🔹 Arquitectura de seis capas

Propuesta para integrar múltiples sistemas IoT y analizar su **valor empresarial**.

1. **Capa de enfoque**
    
    - Identificación de objetos inteligentes y del contexto del sistema IoT.
        
2. **Capa de conocimiento**
    
    - Sensores, actuadores y módulos de monitoreo.
        
    - Recolección de datos de los objetos identificados.
        
3. **Capa de transmisión**
    
    - Envío de datos desde la capa de conocimiento a la aplicación.
        
4. **Capa de aplicación**
    
    - Categorización de la información según nodos de aplicación.
        
5. **Capa de infraestructura**
    
    - Tecnologías orientadas a servicios: nube, Big Data, minería de datos.
        
6. **Capa de negocios de competencia**
    
    - Análisis de modelos de negocio de los sistemas IoT.
        

---

## 🌍 Modelo de referencia ITU (Y.4000 / Y.2060)

La **Unión Internacional de Telecomunicaciones (ITU)** propone un modelo de referencia utilizado como base en este curso.

### 🧱 Capas del modelo

1. **Capa de dispositivo**
    
2. **Capa de red**
    
3. **Capa de apoyo / servicios / datos**
    
4. **Capa de aplicación**
    

### 🔀 Capacidades transversales

- **Gestión**
    
- **Seguridad**
    

---

## 🔌 Capa de dispositivo

Responsable de:

- Recolección y procesamiento inicial de datos.
    
- Digitalización y transferencia de datos a la capa de red.
    

### Capacidades del dispositivo

- Envío y recepción **directa** de información.
    
- Envío y recepción **indirecta** mediante pasarelas.
    
- Creación de redes **ad hoc**.
    
- Gestión de energía (modos activo/reposo).
    

### Capacidades de pasarela

- Traducción entre tecnologías de comunicación.
    
- Necesarias cuando:
    
    - Se usan **protocolos distintos** en la capa de dispositivo.
        
    - Se comunican la capa de dispositivo y la de red con protocolos diferentes.
        

---

## 🌐 Capa de red

Responsable de la **transmisión segura de datos**.

### Capacidades

- **Capacidad de red**
    
    - Control de acceso.
        
    - Gestión de recursos.
        
    - Movilidad, autenticación, autorización y contabilidad.
        
- **Capacidad de transporte**
    
    - Conectividad para datos de aplicaciones IoT.
        
    - Transporte de información de control y gestión.
        

---

## 🗄️ Capa de apoyo, servicios y datos

Incluye dos tipos de capacidades:

### Capacidades genéricas

- Recolección y limpieza de datos.
    
- Almacenamiento.
    
- Procesamiento de datos.
    

### Capacidades específicas

- Funcionalidades particulares de la aplicación.
    
- Ejemplo: semántica de datos.
    

---

## 📱 Capa de aplicación

- Implementa las funcionalidades del sistema IoT.
    
- Ejemplos:
    
    - Ciudades inteligentes.
        
    - Seguridad pública.
        
    - Gestión energética.
        
    - Salud.
        
    - Medio ambiente.
        

---

## ⚙️ Gestión IoT (capacidad transversal)

Incluye funciones similares a redes tradicionales:

- Fallos
    
- Configuración
    
- Contabilidad
    
- Rendimiento
    
- Seguridad
    

### Capacidades de gestión genéricas

- Activación/desactivación remota de dispositivos.
    
- Diagnóstico.
    
- Actualización de firmware y software.
    
- Gestión del estado del dispositivo.
    
- Gestión de topología de red.
    
- Gestión de tráfico y congestión.
    

### Capacidades de gestión específicas

- Dependientes de la aplicación.
    
- Ejemplo: control de transmisión en redes eléctricas.
    

---

## 🔐 Seguridad IoT (capacidad transversal)

### Capacidades de seguridad genéricas

**Capa de aplicación**

- Autenticación y autorización.
    
- Confidencialidad e integridad de datos.
    
- Protección de la privacidad.
    
- Auditorías y antivirus.
    

**Capa de red**

- Autenticación y autorización.
    
- Confidencialidad e integridad de señalización y datos.
    

**Capa de dispositivos**

- Autenticación.
    
- Autorización.
    
- Integridad del dispositivo.
    
- Control de acceso.
    
- Confidencialidad de datos.
    

### Capacidades de seguridad específicas

- Dependientes del servicio.
    
- Ejemplo: seguridad en pagos móviles.
    

---

## 🏙️ Ejemplo: IoT para ciudad inteligente

### Capa de censado

- Sensores, transductores y actuadores.
    
- Cámaras, lectores RFID, escáneres QR.
    
- Integración con SCADA y redes de sensores.
    

### Capa de red

- ADSL.
    
- WiFi.
    
- Redes móviles (2G, 3G, 4G).
    
- Redes eléctricas (PLC).
    

### Capa de soporte

- Bases de datos industriales.
    
- Almacenamiento geoespacial.
    
- Datos económicos o poblacionales.
    

### Capa de aplicación

- Gobierno electrónico.
    
- Seguridad pública.
    
- Salud.
    
- Protección ambiental.
    

---

## 🧠 Conclusión

El modelo de referencia IoT permite **modelar cualquier sistema IoT**, independientemente de su complejidad.  
A lo largo del curso, este modelo servirá como base para comprender los aspectos de **hardware, comunicaciones y software** en sistemas IoT.