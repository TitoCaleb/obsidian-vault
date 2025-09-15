
## 📌 Regiones

- Una **Región de AWS** es un área geográfica que contiene múltiples **Zonas de Disponibilidad (AZs)**.  
- Cada región está **físicamente separada** de otras regiones, para cumplir con requisitos de **soberanía de datos**, **latencia** y **resiliencia**.  
- Se identifican con códigos como:  
  - `us-east-1` → N. Virginia  
  - `eu-west-1` → Irlanda  
- Los servicios que despliegues en una región **no se replican automáticamente en otra** (a menos que lo configures, como en S3 Cross-Region Replication).  
- Es importante elegir la región más cercana a tus usuarios o la que cumpla regulaciones.  

---

## 📌 Zonas de Disponibilidad (AZs)

- Cada región tiene **múltiples AZs** (mínimo 2, normalmente 3 o más).  
- Una **AZ** es una **partición aislada de la infraestructura de AWS**.  
- Cada AZ puede incluir **varios centros de datos** (data centers), con **energía, red y refrigeración independientes**.  
- AZs están **físicamente separadas por kilómetros** (hasta 100 km) para tolerar desastres naturales, pero lo suficientemente cerca para mantener **latencia baja**.  
- Están conectadas entre sí con **fibra dedicada, redundante y de alta velocidad**, lo que permite:  
  - **Baja latencia** entre AZs.  
  - **Replicación síncrona** (ej. en bases de datos o almacenamiento).  
- AWS recomienda diseñar aplicaciones replicadas en múltiples AZs para:  
  - Alta disponibilidad.  
  - Tolerancia a fallos.  
  - Escalabilidad.  

---

# 📌 Data Centers

- Los **data centers** son la **base física de la infraestructura de AWS**.  
- Aunque son donde realmente reside la información, los clientes **no eligen un data center específico**, sino que el nivel más granular disponible es la **Zona de Disponibilidad (AZ)**.  

---

##  Características principales

- **Diseño seguro y redundante**: preparados para anticipar y tolerar fallos sin afectar el servicio.  
- **Evaluación ambiental**: cada ubicación se selecciona cuidadosamente para mitigar riesgos (ej. terremotos, inundaciones, incendios).  
- **Alta disponibilidad**:  
  - Los componentes críticos están respaldados y distribuidos en múltiples **AZs**.  
  - En caso de falla, procesos automatizados redirigen el tráfico fuera del área afectada.  
- **Capacidad garantizada**: AWS monitorea constantemente el uso de servicios y despliega infraestructura adicional cuando es necesario.  
- **Acceso restringido**:  
  - La ubicación exacta de los data centers **no se divulga públicamente**.  
  - Todo acceso físico está controlado estrictamente.  
- **Equipamiento personalizado**:  
  - AWS utiliza hardware de red propio, diseñado específicamente para sus necesidades.  
  - Trabaja con **ODMs (Original Device Manufacturers)** que fabrican equipos bajo especificaciones de AWS y luego son rebrandeados.  

---

## Riesgo y resiliencia
- Aunque es raro, un **fallo en un data center** puede impactar instancias en ese mismo lugar.  
- Si se concentran todos los recursos en un solo data center y ocurre una falla, todos los recursos quedarían inactivos.  
- Por ello, AWS recomienda desplegar recursos en **múltiples AZs**, que a su vez están compuestas por **varios data centers**.  

# 📌 Puntos de Presencia (PoPs) en AWS

- Los **Puntos de Presencia (Points of Presence - PoPs)** son ubicaciones distribuidas globalmente en las principales ciudades del mundo.  
- Se utilizan para **acercar el contenido y los servicios de AWS a los usuarios finales**, reduciendo la latencia y mejorando la experiencia.  
- Están formados por:
  - **Edge Locations** (ubicaciones de borde).  
  - **Regional Edge Caches** (cachés regionales).  

---

## 📌 Servicios que usan los PoPs
- **Amazon CloudFront** (CDN para distribución de contenido).  
- **Amazon Route 53** (servicio DNS global).  
- **AWS Shield** (protección DDoS).  
- **AWS WAF** (Web Application Firewall).  

---

## 📌 Edge Locations

- Son los puntos principales de los PoPs.  
- Manejan solicitudes de los usuarios y entregan contenido en la ubicación más cercana al cliente.  
- Beneficio: **latencia mínima** al acercar la respuesta al usuario final.  

---

## 📌 Regional Edge Caches
- Funcionan como un nivel intermedio entre las **Edge Locations** y el **servidor de origen**.  
- Se utilizan cuando el contenido **no es accedido con frecuencia** para permanecer en una Edge Location.  
- Beneficio: reducen la necesidad de ir hasta el origen para recuperar el contenido, optimizando la entrega.  


