Es muy importante conocer cual es la resposabilidad que tiene el cliente y cual es la responsabilidad del propio AWS

# Cliente

1. Controlar los datos de sus propios clientes (Datos confidenciales)}
	- Va muy de la mano con cognito, y tambien los datos que se puedan almacenar en DB y S3
2. Administración de acceso, identidades, aplicaciones y plataforma
	- Va de la mano con IAM y los permisos que se le puedan dar a un usuario de la organización para poder hacer uso de los servicios de AWS
3. Configuración de Firewall, redes y sistema operativo
	- Muy de la mano de EC2 u otros servicios de computo donde uno es el que permite el acceso a ese servicio, la creación de un firewall, tambien de servicios con WAF para ciertos servicios que tenemos y la inyección de datos que podemos recibir
4. Cifrado del lado del cliente (uso de tokens), cifrado del lado del servidor (sistemas de datos y archivos) y protección del trafico de red (cifrado, integridad y identidad), en pocas palabras se habla de uso computacional que se da para uso en el internet el usuario debe ser el que gestione quienes tiene la posibilidad de acceder a el y dar el mantenimiento y las credenciales de uso.

## AWS

1. Software, se encarga de la computación, almacenamiento, data bases y redes
2. Hardware. se encarga de la infraestructura global, regiones, zonas de disponibilidad, ubicaciones de borde