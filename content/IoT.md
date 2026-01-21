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
- Modelo de referencia de IoT Arquitectura de Referencia IoT

<h3 style="text-align:center; margin-bottom:20px;">
  Arquitectura de Referencia IoT
</h3>

<table style="
  width:100%;
  border-collapse:separate;
  border-spacing:14px;
  text-align:center;
  font-family:Arial, sans-serif;
">

  <!-- Encabezados -->
  <tr>
    <th style="background:#7e57c2; color:white; padding:16px; border-radius:8px;">
      🛠️ Capa de Gestión
    </th>
    <th style="background:#0288d1; color:white; padding:16px; border-radius:8px;">
      🌐 Arquitectura IoT
    </th>
    <th style="background:#ad1457; color:white; padding:16px; border-radius:8px;">
      🔐 Capa de Seguridad
    </th>
  </tr>

  <!-- Fila 1 -->
  <tr>
    <td rowspan="4" style="
      background:#ede7f6;
      color:#311b92;
      padding:20px;
      border-radius:10px;
      font-weight:600;
      line-height:1.6;
    ">
      Capacidades de Gestión<br>
      <small>(Genéricas / Específicas)</small>
    </td>

    <td style="
      background:#e1f5fe;
      color:#01579b;
      padding:22px;
      border-radius:12px;
      font-weight:700;
      line-height:1.6;
    ">
      4️⃣ Capa de Aplicación<br>
      <small>Aplicaciones IoT</small>
    </td>

    <td rowspan="4" style="
      background:#fce4ec;
      color:#880e4f;
      padding:20px;
      border-radius:10px;
      font-weight:600;
      line-height:1.6;
    ">
      Capacidades de Seguridad<br>
      <small>(Genéricas / Específicas)</small>
    </td>
  </tr>

  <!-- Fila 2 -->
  <tr>
    <td style="
      background:#e3f2fd;
      color:#0d47a1;
      padding:22px;
      border-radius:12px;
      font-weight:700;
      line-height:1.6;
    ">
      3️⃣ Capa de Apoyo a Aplicación y Servicios<br>
      <small>
        Capacidades de soporte genéricas<br>
        Capacidades de soporte específicas
      </small>
    </td>
  </tr>

  <!-- Fila 3 -->
  <tr>
    <td style="
      background:#e8eaf6;
      color:#1a237e;
      padding:22px;
      border-radius:12px;
      font-weight:700;
      line-height:1.6;
    ">
      2️⃣ Capa de Red<br>
      <small>
        Capacidades de Red<br>
        Capacidades de Transporte
      </small>
    </td>
  </tr>

  <!-- Fila 4 -->
  <tr>
    <td style="
      background:#ede7f6;
      color:#4527a0;
      padding:22px;
      border-radius:12px;
      font-weight:700;
      line-height:1.6;
    ">
      1️⃣ Capa de Dispositivo<br>
      <small>
        Capacidades de Dispositivo<br>
        Capacidades de Gateway
      </small>
    </td>
  </tr>

</table>

MySUDS
- sistema de drenaje urbano automatizado e inteligente

## The Internet of Things (IoT): Overview — Resumen

El **Internet de las Cosas (IoT)** se refiere a la conexión de **objetos físicos cotidianos** a Internet, permitiéndoles **enviar, recibir y procesar información**. A diferencia de los computadores tradicionales (PC, tabletas o smartphones), estos dispositivos están **diseñados para un propósito específico** y se integran de forma natural en la vida diaria.

### 🔹 ¿Por qué “Internet of Things”?

- **Internet**: actúa como el canal central para la comunicación, el procesamiento de datos y la coordinación.
    
- **Things (Cosas)**: no son computadores genéricos, sino objetos como relojes, zapatos, paraguas, frascos de medicina o sensores urbanos.
    

Cada “Thing” combina:

- **Sensores** → capturan información del mundo físico.
    
- **Conectividad** → envían esos datos a Internet.
    
- **Procesamiento** → local o remoto.
    
- **Actuadores** → producen acciones o respuestas en el mundo real.
    

---

### 🔹 IoT vs. Ubiquitous Computing

Antes del término IoT se hablaba de **ubiquitous computing (ubicomp)**, que describe la idea de computación integrada en el entorno.  
La diferencia clave es que:

- **Ubicomp** no requería necesariamente conexión a Internet.
    
- **IoT** se apoya fuertemente en Internet como infraestructura central.
    

Hoy, casi todas las soluciones interesantes de computación integrada incluyen conectividad, lo que hace que IoT sea la evolución natural del concepto.

---

### 🔹 ¿Por qué no usar solo smartphones?

Aunque los smartphones pueden realizar muchas de estas funciones, los objetos IoT:

- Reducen la **fricción en la interacción** (información ambiental, no invasiva).
    
- Se integran en las **rutinas cotidianas** sin exigir atención constante.
    
- Están **optimizados para su contexto** (resistentes al agua, fáciles de leer en movimiento, siempre visibles).
    

Ejemplo:  
Un paraguas con una luz que indica lluvia comunica la información de forma **ambiental**, sin requerir abrir una app ni cambiar el comportamiento del usuario.

---

### 🔹 Idea central del IoT

En lugar de pocos dispositivos muy potentes, el IoT propone:

> **Muchos objetos simples, conectados, distribuidos en el entorno**, cada uno diseñado para una función concreta.

Estos objetos trasladan la “inteligencia” desde la pantalla del computador hacia el entorno físico, haciendo que la tecnología sea **más invisible, contextual y natural**.

---

### 🔹 Principio clave

La forma del objeto **sigue a su función**.  
El hecho de estar conectado a Internet no cambia necesariamente su apariencia, sino que **amplía sus capacidades**.

### 🔹 Tecnología como movimiento

Históricamente, gran parte de la tecnología ha estado orientada a:

- **Mover recursos en el espacio** (transporte, comercio).
    
- **Mover recursos en el tiempo** (almacenamiento).
    
- **Mover información** (lenguaje, escritura, telecomunicaciones, medios digitales).
    

Con el paso del tiempo, el énfasis tecnológico se ha desplazado progresivamente hacia la **información**: cómo se transmite, procesa, combina y reutiliza.

---

### 🔹 De computadores centrales a objetos inteligentes

Los computadores comenzaron como máquinas **costosas y especializadas**, accesibles solo para universidades, grandes corporaciones y el sector militar.  
Más tarde, la visión evolucionó hacia:

- “Un computador en cada hogar”
    
- “Un computador en cada escritorio”
    
- Finalmente, **computación integrada en todas partes**
    

La reducción de costos, la miniaturización y la optimización han permitido que **capacidades computacionales generales** se integren en objetos cotidianos: televisores, lavadoras, automóviles, relojes y electrodomésticos.

---

### 🔹 Computación no es suficiente: conectividad + mundo físico

El IoT no surge solo porque ahora sea barato añadir computación a los objetos, sino porque esta computación:

- Está conectada a **sensores** (entrada desde el mundo físico).
    
- Controla **actuadores** (salida hacia el mundo físico).
    
- Se **conecta a Internet**, permitiendo el intercambio de datos a gran escala.
    

La conexión a Internet transforma radicalmente los objetos, ya que permite:

- Análisis avanzado
    
- Agregación de datos
    
- Interacción con servicios externos
    
- Creación de nuevos usos no previstos originalmente
    

---

### 🔹 Ejemplo: el automóvil conectado

Un coche moderno ya contiene múltiples computadores que procesan información local (frenos, motor, presión, estabilidad).  
Sin embargo, cuando se conecta a Internet:

- Puede compartir datos con servicios externos.
    
- Puede adaptarse en tiempo real (tráfico, rutas, seguros).
    
- Puede beneficiarse de datos colectivos (“inteligencia social”).
    

Esto marca una **diferencia cualitativa**, no solo cuantitativa.

---

### 🔹 ¿Por qué el IoT es posible ahora?

El surgimiento del IoT se debe a la convergencia de varios factores:

- 📉 **Reducción drástica del costo del cómputo**  
    Microchips que antes costaban miles hoy cuestan centavos (Moore’s Law).
    
- 🧩 **Uso de CPUs de propósito general**  
    Más barato que diseñar hardware especializado.
    
- 🌐 **Conectividad ubicua y económica**  
    Banda ancha, WiFi, redes móviles.
    
- ☁️ **Madurez de plataformas digitales**  
    APIs, servicios web, cloud computing.
    
- 🛠️ **Herramientas accesibles de desarrollo y prototipado**  
    Microcontroladores, frameworks web, servicios en la nube.
    

Estos factores han alcanzado un **punto óptimo de costo–beneficio**, donde añadir conectividad a un objeto es comparable a elegir un mejor material o acabado.

---

### 🔹 Idea clave

El Internet de las Cosas no es solo una evolución tecnológica incremental, sino el resultado de:

>[!important] El IoT es:
> **Computación barata + conectividad permanente + integración con el mundo físico**

Esto permite que la “inteligencia” deje de estar concentrada en unos pocos dispositivos y se distribuya por el entorno.

### Necesidades humanas reflejadas en objetos “encantados”

Los relatos tradicionales han imaginado objetos que cumplen funciones que hoy asociamos con la tecnología:

- **Protección**  
    Espadas y armaduras mágicas ↔ tecnologías militares, seguridad y defensa.
    
- **Salud**  
    Pociones y curaciones mágicas ↔ medicina, farmacología y dispositivos de monitoreo.
    
- **Omnisciencia**  
    Espejos que revelan la verdad ↔ acceso inmediato a información (Internet, smartphones).
    
- **Conexión humana**  
    Objetos que indican el estado de seres queridos ↔ correo, telefonía, redes sociales.
    
- **Movilidad sin esfuerzo**  
    Alfombras voladoras y botas mágicas ↔ automóviles, trenes, aviones.
    
- **Expresión creativa**  
    Instrumentos y herramientas encantadas ↔ arte, música y medios digitales.
    

---

### 🔹 Tecnología como magia cotidiana

Siguiendo la idea de que **una tecnología suficientemente avanzada parece magia**, el IoT hace que objetos comunes:

- Actúen de forma autónoma
    
- Respondan al contexto
    
- Anticipen necesidades humanas
    

Esto genera interacciones **sutiles y casi invisibles**, similares a los efectos mágicos de los cuentos.

---

### 🔹 Personalidad e inteligencia de los objetos

Un rasgo clave de los objetos encantados es que:

- Tienen **nombre**    
- Poseen **personalidad**    
- Sugieren una **inteligencia mayor** que la estrictamente necesaria    

De manera similar, los dispositivos IoT:

- Tienen capacidades de procesamiento y comunicación muy superiores a su función básica    
- Pueden percibirse como “inteligentes”    
- Operan más allá de lo que se espera de objetos simples como lámparas, paraguas o utensilios domésticos
    

---

### 🔹 Idea clave

El Internet de las Cosas puede entenderse como la **materialización tecnológica moderna de los objetos encantados**:

> Objetos cotidianos que combinan función, inteligencia y conectividad, integrándose de forma casi mágica en la vida diaria.


## Who Is Making the Internet of Things?
### 🔹 Un campo interdisciplinario

Las fronteras entre disciplinas son difusas:

- Artistas colaboran con diseñadores y artesanos.
    
- Diseñadores e ingenieros trabajan juntos en productos industriales.
    
- Hackers y aficionados combinan habilidades técnicas y creativas para prototipar ideas.
    

La ausencia explícita del rol “constructor del IoT” no es un descuido, sino una afirmación implícita: **el IoT atraviesa todas estas disciplinas**.

### Roles en la creación de un “Thing”

Un proyecto de Internet de las Cosas suele implicar distintos aportes a lo largo de su ciclo de vida:

- **Hackers o prototipadores**: exploran ideas y construyen los primeros prototipos funcionales.
- **Desarrolladores de software**: crean los componentes en línea y los servicios que procesan y conectan los datos.    
- **Diseñadores y artesanos**: transforman prototipos rudimentarios en objetos atractivos, usables y coherentes con su contexto.    
- **Ingenieros**: resuelven retos técnicos complejos, especialmente al escalar de prototipo a producción.

Rara vez una sola persona domina todas estas áreas con la profundidad necesaria; sin embargo, **es posible avanzar con conocimientos básicos de varias disciplinas y apoyo externo cuando sea necesario**.

---

### 🔹 El IoT como “Internet of Beautiful Things”

El IoT no debería limitarse a funcionar correctamente, sino aspirar a ser el **“Internet de las cosas bellas”**: objetos bien diseñados, elegantes y agradables de usar. En este sentido, cada objeto conectado puede considerarse también una **obra creativa**, además de un producto técnico.

---

### 🔹 Un campo accesible para todos

Aunque la creación de un objeto IoT puede parecer compleja, la diversidad de habilidades necesarias tiene un efecto positivo: **el campo está sorprendentemente abierto**. Cualquier persona con interés creativo —desde una sola disciplina— puede comenzar a experimentar y construir, aprendiendo progresivamente o colaborando con otros.

---

### 🔹 Idea clave

> El Internet de las Cosas es un terreno interdisciplinario donde convergen objeto físico, computación integrada y servicios en Internet, y donde **no existe un único perfil “correcto” para participar**.
