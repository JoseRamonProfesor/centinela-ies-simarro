# Casos de uso reutilizables

**El catálogo de proyectos que puedes plantear con tus alumnos** — el mismo que usamos en el curso 2025-2026, con su enunciado y anexos completos.

Cada caso de uso funciona con **el generador de datos sintéticos** (sin invertir en sensores → ver [`/generador`](../generador)) **o** con un **dataset público** descargable. Elige los que encajen con tu grupo y tu temario.

---

## Cómo usar este catálogo

1. Mira la tabla y **escoge los casos de uso** que quieras trabajar.
2. Reparte cada caso a un equipo (2-3 alumnos). Son **independientes pero interconectables**: todos leen y escriben sobre el mismo InfluxDB con el schema canónico, así que el dashboard o el chatbot de un equipo puede usar los modelos de otro.
3. Apóyate en el **enunciado** y los **anexos** de esta carpeta para los detalles, los recursos y la evaluación.

> **Sin historia de datos propia, no hay problema:** todos los casos están pensados para entrenarse con datos sintéticos o públicos y transferirse después a datos reales con un cambio mínimo de configuración.

---

## El catálogo de un vistazo

### 🛰️ Datos y monitorización
| Caso | Qué hacen tus alumnos | Técnicas | Datos | Variables CENTINELA |
|---|---|---|---|---|
| **A — Pipeline de ingesta IoT** | Construir el camino del dato de extremo a extremo (sensor→pantalla); pieza fundacional que replica el flujo real | MQTT, Telegraf, InfluxDB, Grafana, lakeFS | Generador / cualquier dataset | todas |
| **D — Calidad del aire, confort y ocupación** | Detectar ocupación a partir de variables ambientales y analizar el confort del aula | Clasificación (Random Forest) | Generador / In-Gauge·En-Gage, UCI Occupancy | `co2`, `temperature-indoor`, `relative-humidity`, `avg-sound-level`, `luminosity`, `occupancy` |

### 📈 Predicción y modelado
| Caso | Qué hacen tus alumnos | Técnicas | Datos | Variables CENTINELA |
|---|---|---|---|---|
| **B — Predicción de consumo (24 h)** | Predecir el consumo eléctrico del día siguiente y comparar modelos contra un baseline | SARIMA, XGBoost, LSTM | Generador / BDG2, UCI Appliances | `power_01`, temperatura exterior, `occupancy` |
| **C — Anomalías en climatización (HVAC)** | Distinguir funcionamiento normal de averías en climatización | Isolation Forest, Autoencoders | Generador / LBNL FDD | válvulas, ventiladores, temperaturas suministro/retorno |
| **E — Meteorología y generación solar** | Procesar datos meteorológicos y predecir la generación fotovoltaica | Series temporales, modelos FV | ERA5 (ECMWF) | temp. exterior, radiación solar, viento, presión |

### 🤖 IA generativa y agentes
| Caso | Qué hacen tus alumnos | Técnicas | Datos | Variables CENTINELA |
|---|---|---|---|---|
| **H — Asistente conversacional (RAG)** | Un chatbot al que se le pregunta en lenguaje natural sobre el edificio y la meteorología; integra los modelos de B, C, D y E | RAG, ElasticSearch, LLM local (Ollama), agentes y enrutamiento | ERA5 + `captia_metadata` + InfluxDB | lectura de `telemetry` / metadatos |

### ⚙️ Big Data, MLOps y calidad
| Caso | Qué hacen tus alumnos | Técnicas | Datos | Variables CENTINELA |
|---|---|---|---|---|
| **I — Big Data: Spark vs Pandas** | Demostrar empíricamente cuándo y por qué hace falta Big Data | Apache Spark, Hadoop/HDFS | BDG2 (53 M+ registros) | — |
| **F — MLOps y ciclo de vida** | Montar la infraestructura que hace reproducible y trazable todo el trabajo | JupyterHub, MLflow, lakeFS | — (infraestructura) | — |
| **G — Calidad de datos con agentes** | Auditar la calidad de datos y modelos (incluida la evaluación del chatbot) con agentes especialistas | Great Expectations, agentes de IA | Todos los datasets | issues de calidad reales |

### ➕ Casos extra (opcionales / avanzados)
| Caso | Qué hacen tus alumnos | Técnicas | Datos |
|---|---|---|---|
| **J — Tráfico y visión artificial** | Contar vehículos en cámaras y construir una serie de intensidad de tráfico | YOLOv, visión por computador | Cámaras DGT + AEMET |
| **K — Edge Computing** *(opcional)* | Inferencia en el borde, simulando el edge gateway | NVIDIA Jetson Orin Nano | — |

---

## Por dónde empezar (recomendaciones)

- **Si empiezas o quieres una victoria rápida:** **D** (ocupación/confort, muy alineado con el aula y con datasets pequeños y limpios) y **A** (el pipeline, que da base al resto).
- **Para lucirse en la defensa:** **H** (el chatbot, muy visual) apoyándose en **B** y **C**.
- **Para justificar el Big Data:** **I** (el benchmark Spark vs pandas).
- Cada caso tiene un **escenario base (MVP)** y un **escenario avanzado (mejora de nota)** en el Anexo I.

---

## Ficheros de esta carpeta

| Fichero | Qué es |
|---|---|
| `Enunciado` (principal) | El proyecto integrador completo: objetivos, organización y planificación |
| `Anexo_I_Casos_de_Uso` | Descripción detallada de cada caso: objetivo, escenario base y avanzado |
| `Anexo_II_Recursos` | Recursos, datasets, infraestructura y stack tecnológico |
| `Anexo_III_Entregables` | Qué se entrega (vídeo, documentación, código) y cómo |
| `Anexo_IV_Evaluacion_Rubrica` | Rúbrica de evaluación por competencias |

**Para montarlo en tu centro**, combina este catálogo con el [generador de datos sintéticos](../generador), las [guías del alumnado](../guias) y la [arquitectura de referencia](../arquitectura).
