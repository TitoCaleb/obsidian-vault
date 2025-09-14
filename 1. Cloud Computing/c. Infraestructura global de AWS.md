- AWS Regions
- AWS Availability Zones 
- AWS Data centers 
- Aws Edge Locations / Points of presence

¿Como elegir una región de AWS?
- Cumplimiento de los requisitos legales y de gobernanza de datos; los datos nunca salen de una región sin tu permiso explicito
- Proximidad a los clientes: latencia reducida
- Servicios disponibles en una región
- Precios

# Zonas de disponibilidad

Cada región tiene muchas zonas de disponibilidad ( normalmente 3)
- Cada zona de disponibilidad (AZ) es uno o varios centros de datos discretos con alimentación, red y conectividad redundantes
- Están separadas unas de otras, de modo que están aisladas de las catástrofes
- Están conectadas con redes de alto ancho de banda y latencia ultrajaba

# Puntos de presencia de AWS

Amazon tiene +450 puntos de presencia ( +10 cachés regionales ) en +90 ciudades de +40 paises
El contenido se entrega al usuario con menor latencia

## Tour por la consola de AWS
- AWS cuenta con servicios globales:
	- Identity and Access Managmente (IAM)
	- Route 53 (servicio DNS)
	- CloudFront (red de entrega de contenido)
	- WAF (firewall de aplicaciones WEB)
- La mayoria e los servicios de AWS sson de ámbito regional
	- Amazon EC2 (IaaS)
	- Elastic Beanstalk (PaaS)
	- Lambda (FaaS) Function as a Service
	- Rekognition (SaaS)