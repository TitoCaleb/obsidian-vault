## ¿Qué es un volumen EBS?

- Un volumen EBS (Elastic Block Store) es una unidad de red que puede adjuntar a las instancias mientras se ejecutan
- Permite que las instancias persistan los datos, incluso después de su finalización
- Sólo pueden montarse en una instancia a la vez (a nivel de CCP)
- Están vinculados a una zona de disponibilidad especifica

- Analogía: Piensa en ellos como una "memoria USB de red"
- Nivel gratuito: 30 GB  de almacenamiento EBS gratuito de tipo Propósito General (SSD) o Magnético al mes

## Volumen EBS

- Es una unidad de red (es decir, no es una unidad física)
	- Utiliza la red para comunicar la instancia, lo que significa que puede haber un poco de latencia
	- Se puede separar de una instancia EC2 y conectarla a otra rápidamente 
- Está bloqueado en una Zona de Disponibilidad (AZ)
	- Un volumen EBS en (us-east-1 a) no puede adjuntarse a (us-east-1 b)
	- Para trasladar un volumen, primero hay que hacer un snapshot del mismo
- Tener una capacidad provisionada (tamaño en GBs, e IOPS)
	- Se facturará toda la capacidad aprovisionada
	- Puede aumentar la capacidad de la unidad con el tiempo
	  
	  

> [!NOTE]
> Atributo borrar al terminar
> - Controla el comportamiento de EBS cuando una instancia EC2 termina
> 	- Por defecto, se elimina el volumen EBS root (atributo habilitado)
> 	- Por defecto, cualquier otro volumen adjunto no se elimina (atributo deshabilitado)
> - Esto puede ser controlado por la consola de AWS / AWS CLI
> - Caso de uso: preservar el volumen root cuando se termina la instancia


