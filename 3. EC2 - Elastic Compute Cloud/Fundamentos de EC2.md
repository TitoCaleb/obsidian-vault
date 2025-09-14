EC2 es una de las ofertas más populares de AWS
EC2 = Elastic Compute Cloud = Infraestructura como servicio (IaaS)
Consiste en la capacidad de : 
- Alquilar maquinas virtuales (EC2)
- Almacenar datos en unidades virtuales (EBS)
- Distribuir la carga entre las maquinas (ELB)
- Escalar los servicios mediante un Auto Scaling Group (ASG) o también conocido en español como Grupo de Autoescalado
  
Conocer EC2 es fundamental para entender el funcionamiento del Cloud

## Opciones de tamaño y configuracion de EC2

- Sistema Operativo (OS) : Linux, Windows o Mac OS
- Cuanta potencia de cálculo y nucleos (CPU)
- Cuanta memoria de acceso aleatorio (RAM)
- Cuanto espacio de almacenamiento:
	- Conectado a la red (EBS y EFS)
	- Hardware (EC2 Instance store)
- Tarjeta de red: velocidad de la tarjeta, direccion IP pública
- Reglas de firewall: **grupo de seguridad**
- Script de arranque (configurar en el primer lanzamiento): Datos de usuario de EC2

## Datos del usuario de EC2

- Es posible arrancar nuestras instancias utilizando ***un script de datos de usuarios*** de EC2
- ***Bootstrapping*** significa lanzar comandos cuando una maquina se inicia
- Ese script solo ***se ejecuta una vez*** en el ***primer arranque de la instancia***
- Los datos de usuario EC2 se utilizan para automatizar tareas de arranque como:
	- Instalar actualizaciones
	- Instalación de software
	- Descarga de archivos comunes de Internet
	- Cualquier cosa que se te ocurra 
- El script de datos de usuario de EC2 se ejecuta ***con el usuario root***
