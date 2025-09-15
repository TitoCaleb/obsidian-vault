Puedes utilizar diferentes tipos de instancias EC2 optimizadas para diferentes casos de uso (https://aws.amazon.com/ec2/instance-types/)

AWS tiene la siguiente convención de nombres: -> <span style="color:#0070c0">m</span><span style="color:#ffc000">5</span>.<span style="color:#00b050">2xlarge</span> 

- <span style="color:#0070c0">m</span> : clase de instancia
- <span style="color:#ffc000">5</span> : generación (AWS los mejora con el tiempo)
- <span style="color:#00b050">2xlarge</span> : tamaño dentro de la clase de instancia

## Instancia de propósito general

Excelente para una diversidad de cargas de trabajo, como servidores web o repositorios de código
Equilibrio entre
- Computación 
- Memoria
- Red

Se utilizara la instancia t2.micro que es una instancia EC2 de propósito general 
![[Pasted image 20240408223526.png]]
## Instancia de computación optimizada

Ideal para tareas de cálculo intensivo que requieren procesadores de alto rendimiento
- Cargas de trabajo de procesamiento por lotes
- Transcodificación de medios
- Servidores web de alto rendimiento
- Computación de alto rendimiento (HPC)
- Modelado científico y aprendizaje automático
- Servidores dedicados a juegos
![[Pasted image 20240408223648.png]]

## Instancia de memoria optimizada

Rápido rendimiento para cargas de trabajo que procesan grandes conjuntos de datos en memoria
- Alto rendimiento, bases de datos relacionales/no relacionales
- Almacenes de caché distribuidos a escala web
- Bases de datos en memoria optimizadas para BI (Business intelligence)
- Aplicaciones que realizan el procesamiento en tiempo real de grandes datos no estructurados

![[Pasted image 20240408224014.png]]

## Instancia de almacenamiento optimizado

Ideal para tareas de almacenamiento intensivo, que requieran un acceso alto y secuencial de lectura y escritura a grandes conjuntos de datos en el almacenamiento local
- Sistemas de procesamiento de transacciones en línea (OLTP) de alta frecuencia
- Bases de datos relacionales y NoSQL
- Caché para bases de datos en memoria (por ejemplo Redis)
- Aplicaciones de almacenamiento de datos
- Sistemas de archivos distribuidos

![[Pasted image 20240408224236.png]]



