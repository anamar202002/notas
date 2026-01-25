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
