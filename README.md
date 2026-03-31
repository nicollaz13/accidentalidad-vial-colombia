# 🚦 Análisis de Accidentalidad Vial en Colombia
### Vehículos Involucrados en Accidentes de Tránsito — Ley 2251-2022

---

## 📋 Descripción del Proyecto

Análisis exploratorio de datos (EDA) sobre accidentalidad vial en Colombia, usando el dataset oficial del **Registro Único Nacional de Tránsito (RUNT)**, publicado en [datos.gov.co](https://datos.gov.co).

El objetivo es identificar patrones, tendencias y factores de riesgo en los accidentes de tránsito registrados a nivel nacional entre 2022 y 2026.

---

## 📊 Dataset

| Característica | Detalle |
|---|---|
| **Fuente** | RUNT — Registro Único Nacional de Tránsito |
| **Portal** | [datos.gov.co](https://datos.gov.co) |
| **Ley** | Ley 2251 de 2022 |
| **Última actualización** | 3 de febrero de 2026 |
| **Total de registros** | 406,540 accidentes |
| **Cobertura** | Nacional — todos los departamentos de Colombia |

### Variables analizadas

| Columna | Descripción |
|---|---|
| `MARCA_VEHICULO` | Marca del vehículo involucrado |
| `MODELO_VEHICULO` | Año de fabricación |
| `TIPO_VEHICULO` | Categoría del vehículo (moto, automóvil, bus, etc.) |
| `EDAD_VEHICULO` | Antigüedad del vehículo en años |
| `FECHA_ACCIDENTE` | Mes y año del accidente |
| `GRAVEDAD_ACCIDENTE` | CON HERIDOS / CON MUERTOS |
| `DEPARTAMENTO_ACCIDENTE` | Departamento donde ocurrió |
| `MUNICIPIO_ACCIDENTE` | Municipio donde ocurrió |
| `AUTORIDAD_DE_TRANSITO` | Entidad que reportó el accidente |

---

## 🔍 Hallazgos Principales

### 1. 🏍️ Tipo de vehículo con más accidentes
La **motocicleta representa el 56% de todos los accidentes** registrados en Colombia.

| Tipo de Vehículo | Accidentes |
|---|---|
| MOTOCICLETA | 229,212 |
| AUTOMOVIL | 92,166 |
| CAMIONETA | 34,270 |
| BUS | 16,127 |

> **Conclusión:** Más de la mitad de los accidentes viales en Colombia involucran motocicletas, lo que señala una necesidad urgente de políticas de seguridad vial enfocadas en este segmento.

---

### 2. 🗺️ Departamentos con más accidentes
Los tres departamentos con mayor accidentalidad son **Antioquia, Bogotá D.C. y Valle del Cauca**, concentrando la mayor parte de los registros nacionales.

> **Conclusión:** La accidentalidad está fuertemente concentrada en los departamentos de mayor densidad poblacional y actividad económica.

---

### 3. 🚗 Edad del vehículo vs. Gravedad del accidente

| Gravedad | Edad promedio del vehículo |
|---|---|
| CON HERIDOS | 10.4 años |
| CON MUERTOS | 11.75 años |

> **Conclusión:** Los vehículos involucrados en accidentes mortales son en promedio 1.35 años más antiguos. Esto sugiere que una revisión técnico-mecánica más estricta para vehículos mayores de 10 años podría contribuir a reducir la fatalidad en vías.

---

### 4. 📅 Tendencia temporal y anomalía detectada

- Los meses de **marzo, mayo y septiembre** registran históricamente los picos más altos de accidentalidad.
- Se detectó una **anomalía en julio de 2024**: 28,794 registros frente a un promedio mensual de ~8,500. Este outlier requiere validación con la fuente antes de incluirse en conclusiones definitivas.
- Los datos de 2025 y 2026 están **incompletos** — el dataset aún se encuentra en proceso de actualización por parte del RUNT.

> **Conclusión:** La detección de anomalías en los datos es parte esencial del análisis de calidad — un dato atípico no siempre representa la realidad y debe ser señalado antes de tomar decisiones.

---

### 5. 🏷️ Marcas con más accidentes mortales

| Marca | CON MUERTOS | CON HERIDOS |
|---|---|---|
| BAJAJ | 2,911 | 50,125 |
| CHEVROLET | 2,445 | 43,898 |
| YAMAHA | 2,115 | 48,976 |
| SUZUKI | 1,375 | 21,392 |
| AKT | 1,414 | 30,391 |

> **Conclusión:** 4 de las 5 marcas con más muertes son fabricantes de motocicletas (BAJAJ, YAMAHA, SUZUKI, AKT). Esto refuerza el hallazgo #1 y apunta a la necesidad de intervención específica en el segmento de motos.

---

## 🛠️ Herramientas Utilizadas

| Herramienta | Uso |
|---|---|
| **Google Sheets** | Análisis exploratorio, tablas dinámicas y visualizaciones |
| **datos.gov.co** | Fuente oficial del dataset |
| **SQL** *(próximamente)* | Replicar consultas sobre base de datos relacional |
| **Python / Pandas** *(próximamente)* | Automatización del análisis y visualizaciones avanzadas |

---

## 📁 Estructura del Proyecto

```
📦 accidentalidad-vial-colombia
 ┣ 📂 data
 ┃ ┗ 📄 VEHICULOS_INVOLUCRADOS_LEY2251_2022.csv
 ┣ 📂 analisis
 ┃ ┗ 📄 EDA_Accidentalidad_Colombia.xlsx
 ┣ 📂 graficas
 ┃ ┣ 📄 tipo_vehiculo.png
 ┃ ┣ 📄 departamentos.png
 ┃ ┣ 📄 marcas_gravedad.png
 ┃ ┗ 📄 tendencia_temporal.png
 ┗ 📄 README.md
```

---

## 🚀 Próximos Pasos

- [ ] Replicar el análisis en **SQL** usando SQLiteOnline
- [ ] Automatizar la limpieza de datos con **Python / Pandas**
- [ ] Crear un **dashboard interactivo** con Google Looker Studio
- [ ] Ampliar el análisis con datos de **municipios específicos**

---

## 👤 Autor

Proyecto desarrollado como parte de mi transición profesional hacia el rol de **Analista de Datos**, usando fuentes de datos oficiales del gobierno colombiano.

📍 Colombia  
🔗 LinkedIn: *(agrega tu enlace aquí)*  
📧 *(agrega tu correo aquí)*

---

## 📌 Fuente de los datos

> Registro Único Nacional de Tránsito (RUNT) — Publicado en cumplimiento del Artículo 11 de la Ley 2251 de 2022.  
> Disponible en: [https://datos.gov.co](https://datos.gov.co)
