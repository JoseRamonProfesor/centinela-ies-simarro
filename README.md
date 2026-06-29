# CENTINELA+ · IES Dr. Lluís Simarro

> Edificio inteligente y laboratorio vivo de IA y Big Data en un instituto de Formación Profesional.
> Documentación abierta del proyecto y materiales reutilizables para otros centros educativos.

**IES Dr. Lluís Simarro** — Centro de Excelencia en IA y Big Data · Xàtiva (Valencia)
Curso de Especialización en Inteligencia Artificial y Big Data 2025-2026

---

## Qué es CENTINELA+

CENTINELA+ (*Centro Educativo NeTwork INteligente para el Entrenamiento, la investigación y el Aprendizaje*) convierte el propio edificio del instituto en un **edificio inteligente** que se monitoriza y optimiza mediante sensores e inteligencia artificial, y que **a la vez es el laboratorio real donde aprende el alumnado** del Curso de Especialización en IA y Big Data.

El proyecto persigue dos objetivos del mismo peso:

- **Sostenibilidad:** medir y reducir el consumo energético de las aulas (objetivo de proyecto: al menos un 15%).
- **Formación:** que el alumnado desarrolle competencias profesionales reales como Ingeniero/a de Datos, de Machine Learning y de DevOps, trabajando sobre infraestructura real.

El sistema sigue una cadena estándar de datos: **sensores → MQTT → Telegraf → InfluxDB → captia.ai / Grafana**, diseñada para ser **replicable en cualquier centro**.

---

## Objetivo de este repositorio

Este repositorio es la **documentación abierta** de CENTINELA+ y un **kit de reutilización** para que otros institutos puedan replicar tanto la experiencia formativa como la arquitectura técnica. Aquí encontrarás la presentación, el enunciado completo del proyecto final con sus anexos, las guías para el alumnado y la arquitectura de referencia.

---

## Contenido

| Carpeta / fichero | Descripción |
|---|---|
| `presentacion/` | Presentación para centros visitantes|
| `enunciado/` | Enunciado del proyecto final y sus anexos |
| `enunciado/Anexo_I_Casos_de_Uso` | Casos de uso del proyecto |
| `enunciado/Anexo_II_Recursos` | Recursos, datasets e infraestructura |
| `enunciado/Anexo_III_Entregables` | Entregables y criterios de entrega |
| `enunciado/Anexo_IV_Evaluacion_Rubrica` | Rúbrica de evaluación |
| `guias/` | Guía de integración para el alumnado y guía de arquitectura de datos |
| `arquitectura/` | Arquitectura de referencia (Medallion) y schema de datos |

**Enlaces relacionados**

- Vídeos de los proyectos del alumnado (YouTube): `[https://www.youtube.com/playlist?list=PLBpxYI9K1yOJ6ReU5TXAq5S0gi65KkYMo]
- Generador de datos sintéticos (GitHub): [https://github.com/<usuario>/captia-synthetic-data-bms](https://github.com/captia-technology/captia-synthetic-data-bms)
- Plataforma de despliegue: CAPTIA-connect / captia.ai

---

## Cómo reutilizarlo en tu centro

1. Revisa la **presentación** para una visión general del proyecto.
2. Lee el **enunciado y los anexos**: definen casos de uso, recursos, entregables y evaluación, listos para adaptar.
3. Consulta la **guía de arquitectura**: el proyecto trabaja con **datasets públicos** o con el **generador de datos sintéticos**, de modo que el alumnado puede empezar sin esperar a tener datos históricos propios.
4. El stack es **100% open source** (Mosquitto, Telegraf, InfluxDB, Grafana, JupyterHub, MLflow, ElasticSearch, Ollama): sin coste de licencia.

¿Quieres replicarlo o colaborar en proyectos de innovación? Contacto al final.

---

## Sobre el curso

El **Curso de Especialización en Inteligencia Artificial y Big Data** del IES Dr. Lluís Simarro forma perfiles muy demandados combinando ingeniería de datos, machine learning, MLOps e IA generativa sobre proyectos con impacto real. CENTINELA+ es su proyecto integrador.

## Autor y contacto

**José Ramón Cebolla** — Profesor del Curso de Especialización en IA y Big Data, IES Dr. Lluís Simarro.


## Licencia

Documentación publicada bajo **Creative Commons Atribución 4.0 (CC BY 4.0)**: puedes reutilizarla y adaptarla citando la fuente.
