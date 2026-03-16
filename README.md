# telecom-analysis
# Proyecto 6 — Análisis de una empresa de telecomunicaciones

## Objetivo del proyecto
El objetivo de este proyecto es analizar el comportamiento de uso de los clientes de **ConnectaTel**, una empresa de telecomunicaciones con operaciones en México y Colombia.

A través del análisis de datos se busca identificar **patrones de uso, segmentos de clientes y oportunidades comerciales** que permitan mejorar la oferta de planes y apoyar la toma de decisiones del negocio.

---

# Datasets utilizados

El análisis se realizó utilizando tres datasets principales.

## 1. users_latam.csv
Contiene información demográfica y de registro de los usuarios.

Columnas principales:

- `user_id` — identificador del usuario
- `age` — edad del usuario
- `city` — ciudad
- `plan` — tipo de plan contratado
- `reg_date` — fecha de registro del usuario

---

## 2. usage.csv
Contiene los registros de uso de los servicios de telecomunicaciones.

Columnas principales:

- `id` — identificador del registro
- `user_id` — identificador del usuario
- `type` — tipo de uso (call o text)
- `duration` — duración de llamadas
- `length` — longitud del mensaje
- `date` — fecha del registro de uso

---

## 3. plans.csv
Contiene información general sobre los planes ofrecidos por la empresa.

---

# Etapas del análisis

El proyecto se desarrolló siguiendo un flujo típico de análisis de datos.

## 1. Exploración inicial de los datos
- Carga de datasets
- Revisión de estructura
- Identificación de tipos de datos

## 2. Limpieza de datos
- Corrección de **sentinels** (`-999`, `?`)
- Corrección de **fechas fuera de rango**
- Identificación de valores faltantes
- Evaluación de **Missing At Random (MAR)**

## 3. Preparación de datos
- Agregación de métricas de uso por usuario
- Creación del dataset **user_profile**
- Cálculo de:
  - cantidad de mensajes
  - cantidad de llamadas
  - minutos totales de llamadas

## 4. Análisis exploratorio
- Estadísticas descriptivas
- Visualización de distribuciones
- Identificación de **outliers**
- Segmentación de usuarios

## 5. Segmentación de clientes

Se crearon dos tipos de segmentación:

### Segmentación por uso
- Bajo uso
- Uso medio
- Alto uso

### Segmentación por edad
- Joven
- Adulto
- Adulto Mayor

## 6. Visualización
Se generaron gráficos para analizar:

- distribución de edad
- uso de llamadas y mensajes
- distribución de segmentos de clientes

## 7. Análisis ejecutivo
Se tradujeron los hallazgos del análisis en **recomendaciones accionables para el negocio**.

---

# Cómo ejecutar el proyecto

## Opción 1 — Google Colab

1. Abrir el notebook en **Google Colab**
2. Subir los datasets al entorno
3. Ejecutar las celdas en orden desde la parte superior

## Opción 2 — Jupyter Notebook

1. Clonar el repositorio
2. Instalar las librerías necesarias

```bash
pip install pandas seaborn matplotlib numpy

