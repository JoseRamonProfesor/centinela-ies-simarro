# Generador de datos sintéticos

**El componente que hace este kit posible sin invertir en hardware.**

En CENTINELA+, los datos los producen sensores reales instalados en las aulas. Para **replicar los proyectos sin esa inversión**, este generador **simula esos sensores**: fabrica datos sintéticos realistas y los publica **por el mismo camino** que el sistema real, de modo que para tus alumnos es indistinguible de trabajar con el edificio.

---

## Qué reproduce

El generador emite datos siguiendo el flujo y el formato reales de CENTINELA+:

```
[Generador sintético]  →  MQTT (Mosquitto)  →  Telegraf  →  InfluxDB  →  Grafana
```

- Mismo **flujo** de ingesta que en producción.
- Mismo **esquema de datos** canónico (measurement `captia_point`, tags y variables del edificio: `co2`, `temperature_01`, `relative-humidity`, `occupancy`, `power_01`…).

Resultado: el código que escriban tus alumnos para consumir estos datos **funcionará sin cambios** el día que tengas datos reales. Solo cambian las credenciales, no el código.

---

## Repositorio

El generador es un proyecto open source de **CAPTIA Technology**:

**https://github.com/captia-technology/captia-synthetic-data-bms**

> Es un repositorio externo con su propia licencia y documentación. Consulta su `README` para los requisitos exactos y la versión más reciente.

---

## Cómo usarlo en clase (visión general)

1. **Despliega** el generador siguiendo las instrucciones de su repositorio (típicamente con Docker, junto a Mosquitto, Telegraf, InfluxDB y Grafana).
2. **Arráncalo**: empezará a publicar lecturas sintéticas de varias aulas, en continuo, como lo haría un edificio real.
3. **Reparte los casos de uso** entre los equipos (ver [`/proyectos-reutilizables`](../proyectos-reutilizables)): cada grupo consume los mismos datos y construye su pipeline, modelo, dashboard o chatbot.
4. Cuando quieras, sustituye el generador por **datasets públicos** o por **datos reales**: el trabajo del alumnado sigue siendo válido.

---

## Qué necesitas (y qué no)

- ✅ **Necesitas:** software libre (Docker y el stack open source) en un equipo o servidor del centro.
- ❌ **No necesitas:** sensores, instalación eléctrica, la plataforma CAPTIA ni presupuesto de hardware.

---

Para entender cómo encaja con el resto del sistema, consulta [`/arquitectura`](../arquitectura) (arquitectura de referencia Medallion y schema de datos).
