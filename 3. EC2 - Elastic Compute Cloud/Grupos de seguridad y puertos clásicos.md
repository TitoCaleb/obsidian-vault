Los grupos de seguridad son la base de la seguridad de la red en AWS
Controlan cómo se permite el tráfico dentro o fuera de nuestras instancia EC2

![[Pasted image 20240408230624.png]]

- Los grupos de seguridad solo contienen reglas de <span style="color:#00b050">permiso</span> 
- Las reglas de los grupos de seguridad pueden hacer referencia por IP o por grupo de seguridad

# Inmersión más profunda
Los grupos de seguridad actúan como un firewall en las instancia de EC2
Regulan:
- El acceso a los puertos
- Rangos de IP autorizados - IPv4 e IPv6
- Control de la red de entrada (de otros a la instancia)
- Control de la red saliente (desde la instancia hacia otra)

# Diagrama
![[Pasted image 20240408231246.png]]

# Good to know
- Puede adjuntarse a múltiples instancias
- Bloqueado a una combinación de región / VPC
- Vive "fuera" del EC2 - si el tráfico esta bloqueado, la instancia EC2 no lo verá
- Es bueno mantener un grupo de seguridad separado para el acceso SSH
- Si tu aplicación no es accesible (tiempo de espera), entonces es un problema de grupo de seguridad
- Si tu aplicación da un error de "conexión rechazada", entonces es un error de la aplicación o no se ha lanzado
- Todo el tráfico de entrada está <span style="color:#c00000">bloqueado</span> por defecto
- Todo el tráfico de salida esta <span style="color:#00b050">autorizado</span> por defecto

![[Pasted image 20240408231721.png]]

# Puertos clásicos que hay que conocer

- 22 = SSH (Secure Shell) - iniciar sesión en una instancia de Linux
- 21 = FTP (File Transfer Protocol) - subir archivos a un archivo compartido
- 22 = SFTP (Secure File Transfer Protocol) - subir archivo usando SSH
- 80 = HTTP - acceso a sitios web no seguros
- 443 = HTTPS - acceso a sitios web seguros
- 3389 = RDP (Remote Desktop Protocol) - iniciar sesión en una instancia de Windows
