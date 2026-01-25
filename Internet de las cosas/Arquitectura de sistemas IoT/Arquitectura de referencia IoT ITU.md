# Arquitectura de referencia IoT ITU

La Unión Internacional de Telecomunicaciones (ITU) es el organismo especializado de las Naciones Unidas en telecomunicaciones y tecnologías de información y comunicación.

A través del sector ITU-T, se promueve la normalización de las telecomunicaciones a nivel mundial.

Por esta razón, se adopta como referencia el modelo definido en la recomendación Y.4000 / Y.2060.

## Diagrama de las capas

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


## Capas del modelo
1. [[Capa de dispositivo IoT]]
2. [[Capa de red]]
3. [[Capa de apoyo a aplicaciones y servicios]]
4. [[Capa de aplicación]]

## Capacidades transversales
- [[Gestión IoT]]
- [[Seguridad IoT]]

Este modelo permite el modelado de cualquier sistema IoT, independientemente de su nivel de complejidad.

# Interoperabilidad como reto del IoT

La coexistencia de múltiples arquitecturas IoT, terminologías y tecnologías limita la interoperabilidad entre sistemas.

Este problema motiva:
- Arquitecturas de referencia
- Normalización (ITU)

## Notas conceptuales relacionadas
- [[IoT como infraestructura global]]
- [[Any Thing communication]]
- [[Thing y dispositivo no son lo mismo]]
