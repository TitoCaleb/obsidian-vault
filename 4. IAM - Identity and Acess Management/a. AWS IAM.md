AWS IAM es el servicio que nos permite **definir usuarios, grupos, roles y políticas**, y controlar el tipo de acceso que cada entidad tendrá dentro de AWS.

✅ **Características principales**  
- **Gratis**: No hay costo adicional por crear usuarios, políticas o roles. (Solo pagas por los servicios que usan esos usuarios).  
- **Global**: IAM no es regional, se administra a nivel global en la cuenta.  
- **Seguridad**: Maneja **autenticación** (quién eres) y **autorización** (a qué puedes acceder).  
- **Granularidad**: Permite definir permisos detallados a nivel de recurso y acción.  

---

## 🧩 Componentes principales de IAM

### 👤 IAM User
- Entidad que representa una **persona o aplicación** que necesita autenticarse en AWS.  
- Usa **credenciales permanentes**:  
  - Usuario/contraseña (para consola)  
  - Access Key/Secret Key (para CLI o SDK)  
- **Ejemplo**: un desarrollador que accede a la consola, o una app que consume la API de AWS.  

---

### 👥 IAM Group
- Una **colección de usuarios IAM** que comparten los mismos permisos a través de políticas asociadas al grupo.  
- Simplifica la administración: se aplican políticas al grupo y todos los usuarios heredan esos permisos.  
- **Ejemplo**: Grupo `DevOps` con acceso de solo lectura a logs en CloudWatch.  

---

### 📜 Policy
- Documento en **JSON** que define permisos:  
  - **Acciones** (ej. `s3:PutObject`)  
  - **Recursos** (ej. `arn:aws:s3:::mi-bucket/*`)  
  - **Condiciones** (ej. solo desde una IP específica)  
- Una política no hace nada por sí sola: debe asociarse a un **User, Group o Role**.  
- **Ejemplo**: Permitir a un usuario subir archivos a un bucket S3.  

---

### 🎭 IAM Role
- Identidad con un set de permisos que **no pertenece a un usuario específico**.  
- Se **asume temporalmente** por:  
  - Servicios de AWS (ej. EC2, Lambda).  
  - Otros usuarios o cuentas (cross-account).  
- Usa credenciales **temporales** gestionadas por AWS STS (no permanentes).  
- **Ejemplo**: Un EC2 que asume un role para acceder a un bucket S3 sin necesidad de claves en el código.  

---

## 📝 Resumen comparativo

| Concepto   | Qué es                                            | Ejemplo                                     |
| ---------- | ------------------------------------------------- | ------------------------------------------- |
| **User**   | Identidad individual con credenciales permanentes | `alice@example.com` accediendo a la consola |
| **Group**  | Conjunto de usuarios con permisos comunes         | Grupo `Developers` con acceso a EC2         |
| **Policy** | Documento JSON con permisos (allow/deny)          | `"s3:PutObject"` sobre `mi-bucket`          |
| **Role**   | Identidad asumible con permisos temporales        | EC2 que accede a S3 mediante un Role        |