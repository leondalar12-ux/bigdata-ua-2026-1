# GUÍA — BIG DATA (DD283)
## Universidad Autónoma del Perú | Ingeniería de Sistemas | Ciclo VIII
## [MSc. Ruben Quispe](https://www.linkedin.com/in/ruben-quispe-l/)
---

## 1. FILOSOFÍA DE ENSEÑANZA

Este curso está diseñado para **working adults** — profesionales que ya trabajan en empresas. Esto significa:

- Conectar SIEMPRE cada concepto con casos reales del mundo laboral peruano y latinoamericano
- Usar datos de contextos conocidos: retail, banca, telecomunicaciones, salud, gobierno
- Respetar su tiempo: labs concisos, bien explicados, con resultado visible en la sesión
- Exigencia alta + soporte alto: quien estudia aprueba, quien no estudia reprueba
- Metodología: **Aprendizaje Basado en Proyectos (ABP)**

### Reglas de oro:
1. **Nunca dar respuesta sin antes preguntar** — usa el método socrático
2. **Cada semana debe tener un entregable visible** — el estudiante debe "ver" Big Data funcionando
3. **Conectar teoria → herramienta → caso real** en cada sesión
4. **Retroalimentación inmediata** — revisar avances de proyectos en clase
5. **Tolerancia cero al plagio** — los proyectos deben tener datos reales únicos

---

## 2. RESUMEN DEL CURSO

| Item | Detalle |
|------|---------|
| Código | DD283 |
| Duración | 8 semanas |
| Horas/semana | 3h Teoría + 3h Práctica |
| Modalidad | Semipresencial |
| Evaluación | EC(10%) + EP(40%) + EF(50%) |
| Nota mínima | 10.5/20 |
| Fórmula | (EC×0.10) + (EP×0.40) + (EF×0.50) |

### Sistema de evaluación explicado:
- **EC (10%)**: Examen individual de conceptos — semana 4
- **EP (40%)**: Sustentación grupal avance de proyecto — semana 4
- **EF (50%)**: Sustentación final del proyecto completo — semana 8

### Para aprobar el estudiante necesita:
Si EC=20, EP=20 → EF mínimo = 5.5 (imposible fallar solo el final)
Si EC=0, EP=0 → EF mínimo = 21 (matemáticamente imposible)
**Conclusión: quien no trabaja el proyecto NO puede aprobar.**

---

## 3. TECNOLOGÍAS DEL CURSO

### Stack tecnológico principal (ordenado por semana de uso):

| Tecnología | Semana | Propósito | Costo |
|-----------|--------|-----------|-------|
| Google Colab | 1-8 | Entorno Python sin instalación | Gratis |
| Docker Desktop | 2-4 | Simular clusters localmente | Gratis |
| Apache Hadoop (Docker) | 2-3 | HDFS, MapReduce, YARN | Gratis |
| Apache Hive (Docker) | 3 | SQL sobre Hadoop | Gratis |
| MongoDB Atlas | 3 | Base de datos NoSQL en nube | Gratis tier |
| CockroachDB Cloud | 4 | Base de datos NewSQL | Gratis tier |
| Databricks Community | 5 | Apache Spark en nube | Gratis |
| PySpark (Colab) | 5 | Procesamiento distribuido | Gratis |
| Scikit-learn + PySpark MLlib | 6 | Machine Learning | Gratis |
| BeautifulSoup + Scrapy | 7 | Web Scraping | Gratis |
| Pandas + Great Expectations | 7 | Limpieza de datos | Gratis |
| Power BI Desktop | 8 | Visualización | Gratis |
| Azure Free Tier / GCP Free | 1-8 | Cloud demos | Gratis 300$ créditos |

### Por qué este stack:
- **Google Colab**: students con laptops limitadas pueden trabajar sin instalar nada
- **Docker**: simula un cluster real en cualquier laptop con 8GB RAM
- **Databricks Community**: Spark real, gratis, sin configuración
- **MongoDB Atlas**: NoSQL en nube, interfaz web amigable
- **Todo gratis**: critical para estudiantes trabajadores

---

## 4. SOFTWARE A INSTALAR (Guía por semana)

### Instalación mínima requerida (semana 1):
```
1. Python 3.11+ con Anaconda Distribution
   Descarga: https://www.anaconda.com/download
   
2. Visual Studio Code
   Descarga: https://code.visualstudio.com/
   Extensiones: Python, Jupyter, Docker
   
3. Git
   Descarga: https://git-scm.com/downloads
   
4. Docker Desktop
   Descarga: https://www.docker.com/products/docker-desktop/
   Requiere: 8GB RAM mínimo, 50GB espacio libre
```

### Cuentas online a crear (semana 1):
```
1. Google Account → Google Colab (colab.research.google.com)
2. GitHub Account → github.com
3. MongoDB Atlas → cloud.mongodb.com (gratis)
4. Databricks Community → community.cloud.databricks.com (gratis)
5. CockroachDB Cloud → cockroachlabs.cloud (gratis)
```

### Instalación semana 2 (Hadoop con Docker):
```bash
# docker-compose.yml proporcionado por el docente
docker pull apache/hadoop:3
docker-compose up -d
```

### Instalación semana 5 (PySpark local opcional):
```bash
pip install pyspark findspark
# O usar Databricks Community (recomendado)
```

---

## 5. ESTRUCTURA DE CADA SESIÓN (3 horas teoría)

```
00:00 - 00:15  Warm-up: Caso real del mundo (noticia Big Data reciente)
00:15 - 01:00  Teoría con slides + preguntas socráticas (45 min)
01:00 - 01:10  Break (10 min)
01:10 - 02:00  Demo en vivo del docente con herramienta (50 min)
02:00 - 02:30  Trabajo colaborativo en clase (30 min)
02:30 - 02:50  Revisión avance de proyectos (20 min)
02:50 - 03:00  Cierre: qué aprendimos, qué sigue, tarea
```

---

## 6. MAPA SEMANA A SEMANA

| Semana | Temas | Herramientas | Entregable |
|--------|-------|-------------|-----------|
| 1 | Intro Big Data, Arquitectura, Clusters | Colab, Draw.io | Diagrama arquitectura |
| 2 | Cloud, Hadoop, HDFS, MapReduce, HBase | Docker + Hadoop | Word Count en Hadoop |
| 3 | Hadoop avanzado (Hive,Pig), NoSQL | Docker, MongoDB Atlas | CRUD en MongoDB |
| 4 | NewSQL + Examen Parcial | CockroachDB | EP: Avance proyecto |
| 5 | MapReduce + Apache Spark | Databricks/Colab+PySpark | Pipeline Spark |
| 6 | Machine Learning en Big Data | PySpark MLlib, Scikit-learn | Modelo ML sobre datos masivos |
| 7 | Scraping + Limpieza de datos | Scrapy, Pandas | Dataset limpio scrapeado |
| 8 | Casos de éxito + Sustentación Final | Power BI | EF: Proyecto completo |

---

## 7. FORMACIÓN DE GRUPOS DE PROYECTO

- Grupos de **3-4 estudiantes** máximo
- Formar en semana 1
- Cada grupo elige UN proyecto de la lista de 10 proyectos innovadores
- Un integrante diferente presenta cada semana
- **Regla de oro**: todos los integrantes deben poder explicar todo el proyecto

### Criterios de evaluación del proyecto (EP y EF):
| Criterio | Peso |
|---------|------|
| Problema bien definido con datos reales | 20% |
| Arquitectura Big Data correcta | 20% |
| Implementación técnica funcional | 30% |
| Análisis e insights generados | 20% |
| Presentación y claridad | 10% |



## 8. REPOSITORIO GITHUB DEL CURSO

Estructura recomendada para el repositorio del docente:

```
bigdata-ua-2026-1/
├── README.md                    (Syllabus + instrucciones)
├── setup/
│   ├── environment.yml          (Conda environment)
│   ├── docker-compose.yml       (Hadoop stack)
│   └── requirements.txt
├── semana_01/
│   ├── slides/
│   ├── notebooks/
│   └── datasets/
├── semana_02/ ... semana_08/
├── proyectos/
│   └── template_proyecto/
└── datasets/
    └── (datasets reales para labs)
```

GitHub Classroom para recibir trabajos: https://classroom.github.com/

---

## 10. RECURSOS ESENCIALES DEL DOCENTE

### Libros fundamentales:
1. **"Big Data: técnicas, herramientas y aplicaciones"** — Maria Marques Perez (Alfaomega, 2019)
2. **"Big Data con Python"** — Rafael Caballero (Alfaomega, 2019)
3. **"Learning Spark, 2nd Ed."** — Jules Damji et al. (O'Reilly, 2020) — FREE: https://pages.databricks.com/rs/094-YMS-629/images/LearningSpark2.0.pdf
4. **"Hadoop: The Definitive Guide"** — Tom White (O'Reilly) — Referencia técnica
5. **"Designing Data-Intensive Applications"** — Martin Kleppmann (O'Reilly) — El libro más importante de arquitectura de datos

### Plataformas de práctica:
- **Kaggle**: datasets reales + notebooks + competencias (kaggle.com)
- **DataCamp**: cursos PySpark, Hadoop (datacamp.com)
- **Coursera IBM Big Data**: certificado gratuito con audit
- **Google Cloud Skills Boost**: labs gratuitos de BigQuery, Dataproc

### Comunidades:
- Apache Hadoop community: hadoop.apache.org/mailing_lists.html
- Apache Spark community: spark.apache.org/community.html
- Data Engineering Peru: buscar en LinkedIn grupos peruanos

---

## 11. PLAN DE CONTINGENCIA

### Si Docker no funciona en laptops de estudiantes:
→ Usar Google Colab para TODO (tiene Spark via PySpark)
→ Usar Databricks Community Edition
→ El docente tiene una VM en Azure/GCP compartida (ver Semana 2)

### Si internet es lento en clase:
→ Tener datasets descargados localmente en USB
→ Usar datos de Kaggle pre-descargados
→ Tener notebooks offline preparados

### Si el tiempo es insuficiente:
→ Priorizar: Spark > MongoDB > Hadoop puro (más relevante en 2026)
→ Los conceptos de Hadoop se pueden explicar teóricamente si el lab no funciona

---

*Versión 1.0 — Semestre 2026-1 | Docente: Universidad Autónoma del Perú*
