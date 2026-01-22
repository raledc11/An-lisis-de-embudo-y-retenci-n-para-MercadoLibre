# 📊 Análisis de Embudo y Retención de Usuarios – MercadoLibre

## 🧠 Contexto

Este proyecto analiza el **comportamiento de usuarios en MercadoLibre** a través de dos enfoques clave de analítica de producto:

- **Embudo de conversión (Funnel Analysis)**
- **Análisis de retención por cohortes**

El objetivo es entender **dónde se pierden los usuarios** y **qué tan bien la plataforma retiene a sus nuevos usuarios en el tiempo**, información clave para equipos de Producto, Growth y Negocio.

---

## 🎯 Objetivos

- Medir la conversión de usuarios a lo largo del embudo de compra.
- Comparar conversiones por país.
- Analizar la retención de usuarios por cohortes de registro.
- Generar métricas accionables para toma de decisiones.

---

## 🗂️ Dataset

El análisis se basa en dos tablas principales:

### 📌 `mercadolibre_funnel`
Contiene eventos de usuario:
- `user_id`
- `event_name`
- `event_date`
- `country`

Eventos analizados:
- first_visit  
- select_item / select_promotion  
- add_to_cart  
- begin_checkout  
- add_shipping_info  
- add_payment_info  
- purchase  

### 📌 `mercadolibre_retention`
Contiene información de actividad post-registro:
- `user_id`
- `signup_date`
- `activity_date`
- `day_after_signup`
- `active`

Periodo analizado:
📅 **01-01-2025 a 31-08-2025**

---

## 🛠️ Herramientas Utilizadas

- **SQL**
  - CTEs
  - LEFT JOINs
  - COUNT DISTINCT
  - Cohort Analysis
- **Pensamiento analítico orientado a producto**
- **Métricas de conversión y retención**

---

## 🔍 Metodología

### 1️⃣ Análisis de Embudo
- Se identificaron los eventos del funnel.
- Se construyeron CTEs por cada etapa.
- Se calcularon conversiones tomando como base `first_visit`.
- Se segmentó el análisis por país.

### 2️⃣ Análisis de Retención
- Se crearon cohortes mensuales por fecha de registro.
- Se midió retención acumulada:
  - Día 7
  - Día 14
  - Día 21
  - Día 28
- Se calcularon porcentajes de usuarios activos por cohorte.

---

## 📈 Métricas Clave

### 🔹 Funnel
- Conversión a selección de producto
- Conversión a carrito
- Conversión a checkout
- Conversión a compra final

### 🔹 Retención
- Retención D7
- Retención D14
- Retención D21
- Retención D28

---

## 💡 Insights Clave

- La mayor caída del embudo ocurre antes de llegar al checkout.
- Existen diferencias relevantes de conversión entre países.
- Las cohortes más recientes muestran mejor retención temprana (D7).
- La retención disminuye progresivamente después del día 14, indicando oportunidad de mejoras en engagement post-registro.

---

## 🧾 Conclusiones

El análisis permite identificar **puntos críticos del embudo** y **oportunidades de mejora en retención**, aportando información clave para optimizar la experiencia de usuario y aumentar la conversión en MercadoLibre.

---

## 🚀 Próximos Pasos

- Analizar el embudo por tipo de dispositivo.
- Integrar variables de marketing o promociones.
- Automatizar el análisis con dashboards.
- Construir modelos predictivos de churn.

---

📌 *Proyecto desarrollado por Alejandra Carballo – Data Analyst*
