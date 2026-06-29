# CENTINELA+ · Kit replicable para el aula

> **¿Quieres hacer los proyectos de IA y Big Data de CENTINELA con tus alumnos, pero no tienes el presupuesto de sensórica? No te hace falta.**
> Replica la experiencia completa **sin inversión en sensores ni hardware**, usando un **generador de datos sintéticos** y los enunciados reales del curso 2025-2026.

**IES Dr. Lluís Simarro** — Centro de Excelencia en IA y Big Data · Xàtiva (Valencia)
Curso de Especialización en Inteligencia Artificial y Big Data

---

## ¿Por qué este kit?

CENTINELA+ convierte el edificio del instituto en un **edificio inteligente** y, a la vez, en el **laboratorio real** donde aprende el alumnado. La barrera para que otro centro lo replique siempre ha sido la misma: **la inversión en sensórica e infraestructura**.

Este kit elimina esa barrera. El **generador de datos sintéticos** reproduce el mismo flujo de datos que el sistema real —**MQTT → Telegraf → InfluxDB → Grafana**— **sin comprar un solo sensor**. Tus alumnos trabajan exactamente como si los datos vinieran del edificio, y el código que escriben sirve el día que tengas datos reales.

En resumen: **mismos proyectos, mismas competencias, cero inversión en hardware.**

---

## Empieza en 3 pasos

1. **Despliega el generador de datos sintéticos** (software libre, sin hardware) → ver [`/generador`](./generador).
2. **Escoge los casos de uso que quieres trabajar con tus alumnos** entre los del enunciado y sus anexos → ver [`/casos-de-uso-reutilizables`](./casos-de-uso-reutilizables).
3. **Tus alumnos trabajan como si fueran datos reales** del edificio: ingesta, modelos, dashboards, chatbots… con el stack open source.

---

## Qué NO necesitas

- ❌ Sensores ni instalación eléctrica.
- ❌ La plataforma CAPTIA ni ningún servicio de pago.
- ❌ Presupuesto desorbitado en hardware.

**Solo necesitas software libre** (Docker y el stack open source) corriendo en un equipo o servidor del centro.

---

## Las dos vías de datos

**Vía principal — Generador de datos sintéticos** *(recomendada, sin inversión)*
Reproduce el comportamiento del edificio y el flujo completo del dato. Se despliega en minutos. Es lo que hace este kit autosuficiente. → [`/generador`](./generador)

**Vía alternativa — Datasets públicos** *(también gratis)*
Conjuntos de datos reales de otros edificios y aulas descargables de Internet (consumo, CO₂, meteorología, anomalías HVAC). Útiles para enriquecer o contrastar. Documentados en el [Anexo II](./casos-de-uso-reutilizables).

Cualquiera de las dos permite empezar hoy; lo construido vale luego con datos reales.

---

## Contenido del repositorio

| Carpeta | Qué contiene |
|---|---|
| [`/generador`](./generador) | Cómo desplegar y usar en clase el generador de datos sintéticos (enlace al repo de CAPTIA) |
| [`/casos-de-uso-reutilizables`](./casos-de-uso-reutilizables) | Enunciado del proyecto final y **Anexos I–IV**: casos de uso, recursos, entregables y rúbrica de evaluación |
| [`/guias`](./guias) | Guía de integración para el alumnado y cómo usar el generador en el aula |
| [`/arquitectura`](./arquitectura) | Arquitectura de referencia (Medallion) y schema de datos |
| [`/presentacion`](./presentacion) | Presentación del proyecto (PDF y PPTX editable) |

**Vídeos de los proyectos del alumnado (YouTube):**
https://www.youtube.com/playlist?list=PLBpxYI9K1yOJ6ReU5TXAq5S0gi65KkYMo

---

## Cómo reutilizarlo en tu centro

1. Mira la **presentación** para una visión general.
2. Despliega el **generador** y elige **casos de uso** del enunciado y los anexos.
3. Apóyate en las **guías** y en la **arquitectura de referencia** para organizar el trabajo del alumnado.
4. Todo el stack es **open source**: sin coste de licencia.

¿Quieres replicarlo o colaborar en proyectos de innovación? Escríbeme (contacto abajo).

---

## Sobre el curso

El **Curso de Especialización en Inteligencia Artificial y Big Data** del IES Dr. Lluís Simarro forma perfiles muy demandados —Ingeniería de Datos, Machine Learning, MLOps e IA generativa— sobre proyectos con impacto real. CENTINELA+ es su proyecto integrador.

## Autor y contacto

**José Ramón Cebolla** — Tutor del Curso de Especialización en IA y Big Data, IES Dr. Lluís Simarro.
Email: `<jr.cebollacebolla@edu.gva.es>`

## Licencia

La documentación de este repositorio se publica bajo **Creative Commons Atribución 4.0 (CC BY 4.0)**: reutilízala y adáptala citando la fuente.

> **Nota:** el **generador de datos sintéticos** es un repositorio externo de **CAPTIA Technology** con su propia licencia. Revisa sus condiciones en su repositorio.

<!--
  Topics sugeridos para el repo (Settings → Topics), mejoran la difusión:
  education · formacion-profesional · artificial-intelligence · big-data ·
  iot · synthetic-data · mlops · teaching-materials
  Descripción "About" sugerida:
  Kit replicable: monta los proyectos de IA y Big Data de CENTINELA en tu aula,
  sin sensores ni inversión en hardware, usando un generador de datos sintéticos.
-->
