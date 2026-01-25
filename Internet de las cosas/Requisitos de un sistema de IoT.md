# 📋 Levantamiento y especificación de requisitos en sistemas IoT

## Tema

**Cómo levantar y especificar requisitos funcionales y de calidad en sistemas IoT usando historias de arquitectura**

---

## 🧠 Importancia del levantamiento de requisitos

El levantamiento y la especificación de requisitos es el **punto de partida de cualquier producto de software**.

En sistemas tradicionales (web, transaccionales) ya existen retos como:

- Inconsistencias
    
- Ambigüedad
    
- Omisiones
    

En **IoT**, además de estos retos, aparece uno adicional y crítico:

- La necesidad de **capturar y describir hardware, software y comunicaciones** de forma integrada.
    

Por ello, es clave reforzar las **prácticas de análisis** en esta etapa.

---

## 🧩 Prácticas para levantar requisitos

No existe una guía definitiva para IoT. En la práctica se usan:

- Técnicas tradicionales (casos de uso)
    
- Técnicas ágiles (historias de usuario)
    

En este curso se propone el uso de **historias de arquitectura**, adaptadas al dominio IoT.

---

## ⚙️ Tipos de requisitos en IoT

### Requisitos funcionales

No exhaustivos, pero comúnmente incluyen:

- Envío de datos
    
- Registro de dispositivos
    
- Control de actuadores
    
- Análisis de datos
    
- Generación de reportes
    

---

### Requisitos de calidad (no funcionales)

#### Guías generales

- **Estándares ISO** (ej. ISO 9126, ISO 25010):  
    Atributos de calidad generales del software.
    

#### Guías específicas para IoT

- **Ontología SSN (W3C)**  
    Atributos de calidad de la capa física (sensores y dispositivos).
    
- **Recomendaciones ITU-T**  
    Elementos de infraestructura, información y comunicaciones en IoT.
    

---

## 🌐 Atributos de calidad relevantes en IoT (según ITU)

### Atributos compartidos con sistemas tradicionales

- **Interoperabilidad**  
    Compatibilidad entre dispositivos físicos y servicios de software, manejando heterogeneidad de hardware, SO y protocolos.
    
- **Escalabilidad**  
    Capacidad de gestionar un crecimiento en el número de dispositivos conectados.
    
- **Seguridad**
    - Confidencialidad
    - Autenticidad
    - Integridad de la información

		
---

### Atributos propios del dominio IoT

Estos surgen porque **hardware y comunicaciones** son tan importantes como el software:

- **Robustez**  
    Capacidad de resistir condiciones adversas (humedad, temperatura).
    
- **Eficiencia energética**  
    Capacidad de extender el tiempo de operación con bajo consumo.
    
- **Estética**  
    Integración armónica del dispositivo en el entorno, sin ser intrusivo.
    
- **Autonomía**  
    Capacidad de actuar sin intervención humana (auto-configuración, reacción a eventos).
    
- **Direccionalidad**  
    Capacidad de establecer conectividad usando el identificador del dispositivo.
    
- **Movilidad**  
    Capacidad de soportar dispositivos en diferentes ubicaciones manteniendo el servicio.
    

---

## 📖 Historias de arquitectura en IoT

Una **historia de arquitectura** combina:

- Una **funcionalidad valiosa**
    
- Un **escenario para evaluar un atributo de calidad**
    

Es decir, integra requisitos **funcionales y de calidad** en un solo formato.

---

## 🧱 Partes de una historia de arquitectura

### 1. Estímulo

Acción que provoca una respuesta del sistema.

- En IoT, suele provenir de **dispositivos** al detectar eventos del entorno.
    

### 2. Ambiente

Condición bajo la cual ocurre la historia:

- Normal
    
- Sobrecargado
    
- Degradado
    

En IoT puede incluir:

- Volumen de datos
    
- Tecnología de conectividad
    
- Condiciones ambientales (lluvia, humo, etc.)
    

### 3. Rol

Interesado para quien la historia es valiosa.

- Usuarios
    
- Administradores
    
- Diseñadores
    
- Entidades externas
    

### 4. Respuesta

Acción del sistema que genera valor.

- En sistemas tradicionales: CRUD, análisis de datos
    
- En IoT:
    
    - Control de actuadores
        
    - Ajuste de dispositivos
        
    - Interacción con el mundo físico
        

### 5. Medida de respuesta

Valor esperado del atributo de calidad.

- Puede ser:
    
    - **Cuantitativa** (latencia, disponibilidad)
        
    - **Cualitativa** (estética, integración visual)
        

---

## 🧾 Formato recomendado de historia de arquitectura

- **Prioridad**: Alta / Media / Baja
    
- **Cuando** → Estímulo
    
- **Dado que** → Ambiente
    
- **Yo como** → Rol
    
- **Quiero** → Respuesta
    
- **Debe suceder** → Medida de respuesta
    

---

## 🏙️ Ejemplos de historias de arquitectura en MySUDS

### Escalabilidad

- **Estímulo**: envío concurrente de datos desde dispositivos
    
- **Ambiente**: sobrecargado (1.000 dispositivos, 60 minutos)
    
- **Conectividad**: Sigfox
    
- **Respuesta**: almacenar datos correctamente
    
- **Métrica**: latencia < 300 ms
    

---

### Robustez

- **Estímulo**: instalación de dispositivos
    
- **Ambiente**: normal
    
- **Respuesta**: funcionamiento correcto para iniciar monitoreo
    
- **Métrica**: operación a la intemperie y con alta humedad
    

---

### Estética

- Similar a robustez
    
- **Métrica**: integración visual armónica con el parque
    

---

### Eficiencia energética

- **Estímulo**: inicio de lluvia con batería al 10 %
    
- **Respuesta**: activación de paneles solares
    
- **Métrica**: energía alternativa durante todo el evento (≈ 1 hora)
    

---

### Autonomía

- **Estímulo**: detección de inicio de lluvia
    
- **Condición**: promedio > 30 mm en 30 minutos
    
- **Respuesta**: apertura automática de compuertas
    
- **Métrica**: acción ejecutada en ≤ 5 minutos
    

---

## 🧠 Ideas clave finales

- No existe una guía única para requisitos IoT.
    
- Es recomendable apoyarse en:
    
    - Estándares ISO
        
    - Recomendaciones ITU
        
    - Ontología SSN (W3C)
        
- Las **historias de arquitectura** permiten:
    
    - Integrar funcionalidad y calidad
        
    - Incorporar información específica de IoT:
        
        - Conectividad
            
        - Condiciones ambientales
            
        - Capa física