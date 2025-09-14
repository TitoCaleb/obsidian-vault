- Bajo demanda : carga de trabajo corta, precio predecible, pago por segundos
- Reservadas (1 y 3 años)
	- Instancias reservadas - cargas de trabajo largas
	- Instancias reservadas convertibles: cargas de trabajo largas con instancias flexibles
- Planes de ahorro (1 y 3 años): compromiso con una cantidad de uso, carga de trabajo largas
- Instancias spot - cargas de trabajo cortas, baratas, pueden perder instancias (menos fiables)
- Host dedicados: reserve un servidor físico completo, controle la ubicación de las instancias
- Instancias dedicadas: ningún otro cliente compartiría tu hardware
- Reservadas de capacidad: reserva de capacidad en una AZ especifica para cualquier duración


### Bajo demanda (On demand)

- Paga por lo que usas:
	- Linux o windows: facturación por segundo, despues del primer minuto
	- Todos los demas sistemas operativos: facturacion por hora
- Tiene el coste más elevado, pero no hay que pagar por adelantado
- Sin compromiso a largo plazo
- Recomendado para cargas de trabajo a corto plazo y sin interrupciones, cuando no se puede predecir el comportamiento de la aplicación

### Instancias reservadas de EC2

- Hasta un <span style="color:#0070c0">72%</span> de descuento en comparación con el servicio bajo demanda
- Reserva de atributos de instancia específicos (tipo de instancia, región, ocupación, sistema operativo)
- Periodo de reserva - 1año (+descuento) o 3 años (+++descuento)
- Opciones de pago - Sin pago inicial (+), Pago inicial parcial (++), pago inicial total (+++)
- Alcance de la instancia reservada - Por región o por zona (capacidad de reserva en una AZ)
- Recomendado para aplicaciones de uso constante (piensa en una base de datos)
- Puedes comprar y vender en el Marketplace de instancias reservadas


##### Instancia reservada convertible
- Puedes cambiar el tipo de instancia EC2, la familia de instancias, el SO, etc
- Hasta un <span style="color:#0070c0">6<span style="color:#0070c0">6%</span></span> de descuento 

### Planes de ahorro EC2

- Obtén un descuento basado en el uso a largo plazo (hasta el <span style="color:#0070c0">72%</span>)
- Comprométete a un determinado tipo de uso (10 $/hora durante 1 o 3 años)
- El uso más allá de los planes de ahorro de EC2 se factura el precio bajo demanda
- Bloqueado a una familia de instancias especificas y a una región de AWS (por ejemplo, M5 en us-east-1)
- Flexible a través de:
	- Tamaño de instancia (por ejemplo, m5.xlarge, m5.2xlarge)
	- Sistema Operativo (por ejemplo, Linux, windows)
	- Tenencia (Anfitrion, Dedicado, Por defecto)

### Instancias Spot

- Puedes obtener un descuento de hasta 90% en comparación con la demanda.
- Instancias que puedes "perder" en cualquier momento si su precio máximo es inferior al precio spot actual
- Las instancias más rentables en AWS
- Útil para las cargas de trabajo que son resistentes a los fallos
	- Trabajos por lotes
	- Análisis de datos
	- Procesamiento de imágenes
	- Cualquier carga de trabajo distribuida
	- Cargas de trabajo con una hora de inicio y finalización flexible
- No es adecuado para trabajos críticos o bases de datos

### Hosts dedicados de EC2 

- Un servidor físico con capacidad de instancia EC2 totalmente dedicado a su uso 
- Permite abordar los requisitos de normativas y utilizar licencias de software vinculadas al servidor existentes (licencias de software por socket, por núcleo, por VM )
- Opciones de compra
	- Bajo demanda - pago por segundo por el host dedicado activo
	- Reservado - 1 0 3 años (sin pago inicial, pago inicial parcial, pago inicial total)
- Es la opción más cara
- Útil para el software que tiene un modelo de licencia complicado (BYOL - Bring your own license)
- O para empresas que tienen fuertes necesidades de regulación o cumplimiento

### Instancias dedicadas de EC2

- Las instancias se ejecutan en un hardware dedicado para ti
- Puedes compartir el hardware con otras instancias de la misma cuenta
- No hay control sobre la ubicación de las instancias (se puede mover el hardware después de la parada/arranque) 

## HOST DEDICADOS VS INSTANCIAS DEDICADAS 
![[Pasted image 20240419013727.png]]


### Reservas de capacidad de EC2

- Reserva la capacidad de las instancias bajo demanda en una AZ (Available Zone) especifica para cualquier duración
- Siempre tendras acceso a la capacidad de EC2 cuando la necesites
- Sin compromiso de tiempo (crear / cancelar en cualquier momento), sin descuentos en facturación
- Combina con las instancias regionales reservadas y los planes de ahorro para beneficiarte de descuentos en la facturación
- Se te cobra la tarifa bajo demanda tanto si ejecuta instancias como si no
- Adecuado para cargas de trabajo ininterrumpidas a corto plazo que necesitan estar en una AZ especifica


## ¿Qué opción de compra me conviene?

Imaginemos que quiero ir a un resort y cuentas con diferentes tipos de pago y oferta

![[Pasted image 20240421233008.png]]
