Para acceder a AWS, tienes tres opciones:
- Consola de administración de AWS (protegida por contraseña + MFA)
	- Interfaz de línea de comandos de AWS (CLI): protegida por claves de acceso
	- AWS Software Developer Kit (SDK) - para el código: protegido por claves de acceso
	- Las claves de acceso se generan a través de la Consola de AWS
- Los usuarios gestionan sus propias claves de acceso
- Las claves de acceso son secretas, como una contraseña. No se comparten


# ¿Qué es la CLI de AWS?

Una herramienta que permite interactuar con los servicios de AWS mediante comandos de tu SHELL de línea de comandos

- Acceso directo a las API publicas de los servicios de AWS
- Puedes desarrollar scripts para gestionar tus recursos
- Alternativa al uso de la consola de administración de AWS

# ¿Qué es el SDK de AWS?

- Kit de desarrollo de software de AWS (AWS SDK)
- APIs especificas para cada lenguaje (conjunto de bibliotecas)
- Permite acceder y administrar los servicios de AWS mediante programación
- Integrado en la aplicación
- Admite:
	- SDKs (JS, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++)
	- SDKs para moviles (Android, IOS, etc)
	- SDKs para dispositivos IoT (Embedded C, Arduino, ...)