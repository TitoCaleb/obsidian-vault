AWS Organizations es un servicio que permite **administrar múltiples cuentas de AWS de manera centralizada**.  
Ofrece control, seguridad y optimización de costos, manteniendo independencia entre cuentas, pero con visibilidad y políticas unificadas desde una cuenta principal (**Management Account**).  

---

## ✅ Beneficios principales
- **Gestión centralizada**: una sola consola para manejar varias cuentas.  
- **Aislamiento de entornos**: producción, desarrollo, pruebas o startups separadas entre sí.  
- **Facturación consolidada**: un solo recibo global con desglose por cuenta y descuentos por volumen.  
- **Seguridad y compliance**: aplicar *Service Control Policies (SCP)* que restringen servicios o regiones.  
- **Escalabilidad**: crear o invitar nuevas cuentas fácilmente sin perder control global.  

---

## 📂 Ejemplo práctico
Imagina un **holding de empresas** que invierte en varias **startups**:

- La **Management Account** actúa como la empresa madre.  
- Cada **startup** tiene su **propia cuenta AWS (miembro)**, aislada en recursos y facturación.  
- Gracias a **Organizations**:  
  - El holding puede ver y consolidar los costos de todas las startups.  
  - Puede aplicar reglas globales (ej. “ninguna cuenta puede crear recursos fuera de us-east-1”).  
  - Cada startup mantiene autonomía en su propia cuenta, pero bajo control financiero y de seguridad centralizado.  

---
# 💳 Facturación en AWS Organizations

## 📌 Cómo se maneja la facturación en AWS Organizations

### 🏛️ Management Account (administrador de la organización)
- Es la **única cuenta que paga directamente a AWS**.  
- AWS envía **una sola factura consolidada** a la tarjeta o medio de pago de la cuenta principal.  
- Tiene **visibilidad de todos los gastos** de cada cuenta miembro (puede ver reportes detallados).  

### 👥 Cuentas miembro
- **No pagan directamente a AWS** (aunque cuando las creas sí te pide tarjeta).  
- Esa tarjeta queda registrada en la cuenta miembro, pero **no se utiliza mientras la cuenta esté dentro de la organización con facturación consolidada**.  
- El costo de sus recursos se **acumula en la factura de la Management Account**.  

### 📊 Distribución de costos
- Aunque el pago se hace desde la cuenta principal, puedes usar:  
  - **Cost Explorer**  
  - **Cost and Usage Reports (CUR)**  
  - **AWS Billing Conductor**  

  para **asignar costos por cuenta o incluso por proyecto**.  

- Esto permite que cada startup/área sepa **cuánto consumió**, aunque **no pague directamente a AWS**.  
