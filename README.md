# 📊 RappiPlus: De Datos a Decisiones de Negocio
Este repositorio contiene el ecosistema analítico desarrollado para RappiPlus, el servicio de suscripción premium de Rappi. El objetivo principal es determinar mediante evidencia empírica si el modelo de suscripción cumple con su promesa de valor: aumentar la frecuencia de compra, la retención y la rentabilidad por usuario.

El proyecto integra limpieza de datos con Python, consultas complejas en SQL para el comportamiento de usuarios y validación estadística de experimentos A/B.

**📂 Estructura del Proyecto**

Analisis_RappiPlus_Full.ipynb: Notebook principal con las 6 etapas del análisis (Calidad, Rentabilidad, Funnel, Cohortes, A/B Testing y Visualización).

Datasets/: Carpeta con los archivos crudos y procesados (orders, catalog, marketing_spend).

SQL_Queries/: Consultas estructuradas para el análisis de comportamiento en base de datos.

**🧠 Objetivo del Análisis**

Transformar el ruido de los pedidos y eventos en una hoja de ruta estratégica para el equipo de producto:

Confiabilidad: ¿Los datos de transacciones y costos son consistentes?

Rentabilidad: ¿El margen generado supera el gasto de adquisición y costos de catálogo?

Fricción: ¿En qué etapa del funnel (first visit -> checkout) estamos perdiendo más usuarios?

Retención: ¿Los suscriptores regresan o el churn es mayor al crecimiento?

**🛠️ Tecnologías Utilizadas**

Python (Pandas, SciPy, Seaborn): Limpieza de datos y evaluación de impacto de experimentos A/B.

SQL (PostgreSQL/SQLite): Construcción de embudos (funnels) y matrices de cohortes a partir de tablas de eventos y actividad.

Estadística Inferencial: Pruebas de hipótesis para validar cambios en la UI del checkout.

**📈 Metodología y Hallazgos Esperados (Insights)**

Calidad de Datos y Rentabilidad (Python)

Proceso: Consolidación de orders con catalog para calcular el costo real de ventas.

KPIs Clave: Revenue total, Profit por categoría y ROI de campañas de marketing por país.

Análisis de Fricción (Funnel con SQL)

Proceso: Análisis del flujo de sesiones desde el evento first_visit hasta la confirmación de pago.

Insight Objetivo: Identificar el "Mayor Drop-off" (punto de abandono crítico) para optimizar la interfaz de usuario.

**Retención por Cohortes (SQL)**

Proceso: Agrupación de usuarios por fecha_registro y seguimiento de su actividad (user_activity) en ventanas de tiempo (N-días).

Insight Objetivo: Determinar si los usuarios de planes free vs. plus mantienen niveles de actividad diferenciados en el tiempo.

**Evaluación de Impacto A/B (Python)**

Proceso: Comparación de tasas de conversión entre variantes de control y tratamiento en el checkout.

Evidencia: Cálculo de significancia estadística para decidir si el cambio en la UI debe implementarse globalmente.

**🚀 Conclusiones de Negocio**

[!IMPORTANTE¡]
Entregable Estratégico: El análisis culmina en un Dashboard Ejecutivo que comunica no solo "qué pasó", sino "por qué pasó" y qué acciones inmediatas (cambios en catálogo, inversión en canales específicos o ajustes de UX) deben ejecutarse para salvar la rentabilidad del servicio Plus.
