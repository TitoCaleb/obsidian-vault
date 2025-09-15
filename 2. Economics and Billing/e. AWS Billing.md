# 💰 Herramientas de Costos y Facturación en AWS

## 📊 Billing Dashboard
Vista central para monitorear y administrar los costos de tu cuenta u organización.

- **Spend Summary** → Resumen del gasto actual y comparación con meses anteriores.  
- **Monthly to Date Spend by Service** → Gasto acumulado en el mes, dividido por servicio.  

---

## 🛠️ Herramientas principales

| Herramienta | Función principal | Nivel de detalle | Casos de uso |
|-------------|------------------|------------------|--------------|
| **AWS Budgets** | Crear **presupuestos** y recibir **alertas** si el gasto estimado o real los supera. | Medio | Control preventivo de costos, alertas a equipos antes de exceder el límite. |
| **Cost and Usage Report (CUR)** | Reporte **ultra detallado** de uso y costos, exportado a **S3**. | Muy alto (hasta nivel de recurso individual) | Análisis financiero avanzado, integración con Athena/Redshift o contabilidad interna. |
| **Cost Explorer** | Análisis **visual e interactivo** de costos con filtros (cuenta, servicio, región, tags). | Alto | Identificar tendencias, servicios más costosos, proyecciones de gasto futuro. |
| **Bills Page** | **Factura oficial** con desglose por servicio y región, incluye impuestos. | Bajo a medio | Descarga de facturas para contabilidad y reportes financieros. |

---

## 📌 Resumen rápido

- **Budgets** → Control de presupuestos con alertas.  
- **CUR** → Reportes técnicos/financieros más detallados (nivel granular).  
- **Cost Explorer** → Análisis gráfico y exploratorio de costos.  
- **Bills Page** → Facturas oficiales y desglose completo.  
