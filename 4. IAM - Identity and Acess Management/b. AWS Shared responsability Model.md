
| **Responsable** | **Áreas de Responsabilidad** | **Ejemplos prácticos** |
|-----------------|-------------------------------|-------------------------|
| **AWS** (Seguridad **de** la nube) | - Infraestructura global (Regiones, AZs, Edge Locations)<br>- Hardware físico (servidores, racks, discos)<br>- Red física<br>- Virtualización<br>- Software base (EC2 hypervisor, S3 storage system, etc.) | - Mantener centros de datos seguros (guardias, CCTV, electricidad redundante).<br>- Actualizar hipervisores de EC2.<br>- Garantizar que los discos dañados de S3 sean eliminados de forma segura.<br>- Mantener la disponibilidad de servicios (ej. caída de AZ). |
| **Cliente** (Seguridad **en** la nube) | - Datos del cliente<br>- Configuración de red (Security Groups, NACLs, Firewalls)<br>- Sistemas operativos y parches en EC2<br>- Gestión de identidades (IAM, MFA, roles)<br>- Cifrado del lado cliente y políticas de acceso<br>- Aplicaciones propias | - Definir quién accede a una bucket S3.<br>- Configurar reglas de firewall en EC2.<br>- Habilitar cifrado en una base de datos RDS.<br>- Rotar contraseñas o llaves de acceso.<br>- Instalar parches en un Windows Server en EC2.<br>- Proteger datos sensibles en DynamoDB con encriptación KMS. |


---

# 🃏 Flashcards: Preguntas y Respuestas

## ¿Quién es responsable de configurar reglas de firewall en una instancia EC2?
**Respuesta:** El cliente.

---

## ¿Quién administra la seguridad física de los servidores en los data centers de AWS?
**Respuesta:** AWS.

---

## ¿Quién debe aplicar parches al sistema operativo de una máquina virtual en EC2?
**Respuesta:** El cliente.

---

## ¿Quién asegura que las zonas de disponibilidad tengan energía y red redundante?
**Respuesta:** AWS.

---

## ¿Quién define las políticas de acceso a los usuarios de IAM?
**Respuesta:** El cliente.

---

## Si ocurre una fuga de datos por mal uso de credenciales IAM, ¿quién es responsable?
**Respuesta:** El cliente.

---

## Si hay una falla eléctrica en un centro de datos, ¿quién es responsable de mantener el servicio?
**Respuesta:** AWS.

---

## ¿Quién es responsable de cifrar datos sensibles antes de subirlos a S3 (lado cliente)?
**Respuesta:** El cliente.

---

## ¿Quién se encarga de reemplazar discos defectuosos en un servidor físico?
**Respuesta:** AWS.

