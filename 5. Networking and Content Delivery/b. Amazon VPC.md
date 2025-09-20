## ¿Qué es?

- Servicio que permite crear una **sección aislada de la nube de AWS** (red privada virtual).
- Control total sobre:
    - Rango de direcciones IP.
    - Creación de **subnets** (públicas y privadas).
    - Configuración de **route tables** y **gateways**.
- Permite usar **IPv4** y **IPv6**.
- Seguridad en capas con **Security Groups** y **Network ACLs**.
---
## VPCs y Subnets
- **VPCs**
    - Aisladas lógicamente de otras VPCs.
    - Dedicadas a tu cuenta.
    - Pertenecen a **una región** y pueden abarcar **múltiples AZs**.
- **Subnets**
    - Rango de IPs dentro de una VPC.
    - Pertenecen a **una sola AZ**.
    - Pueden ser **públicas** (acceso a Internet) o **privadas** (sin acceso directo).
---
## Direccionamiento IP

- VPC asignada a un **CIDR IPv4** al crearse.
- No se puede cambiar después.
- Tamaños:
    - Máximo: `/16` → 65,536 IPs.
    - Mínimo: `/28` → 16 IPs.        
- Subnets → deben ser **subconjuntos no superpuestos** del CIDR de la VPC.
- AWS **reserva 5 IPs por subnet**:
    - `.0` → Dirección de red.
    - `.1` → Router local.
    - `.2` → DNS.
    - `.3` → Reservado futuro.
    - `.255` → Broadcast.
---
## Tipos de IP
- **Privadas** → asignadas por defecto en la VPC.
- **Públicas**:
    - **Auto-assign** (según config de la subnet).
    - **Elastic IP (EIP)**:
        - IP pública estática.
        - Puede reasignarse a otra instancia o interfaz.
        - Tiene costo si no se usa.
---
## Elastic Network Interface (ENI)
- Interfaz de red virtual.
- Puede **adjuntarse/desasociarse** de instancias.
- Mantiene sus atributos al moverse → redirige tráfico.
- Cada instancia tiene **una ENI primaria** que no se puede quitar.
- Se pueden agregar ENIs extra según el tipo de instancia.
---
## Route Tables y Routes
- Contienen **reglas de enrutamiento** (destino → target).
- Cada subnet debe tener **una sola route table** (pero una route table puede usarse en varias subnets).
- Todas las route tables incluyen una ruta **local** (tráfico dentro de la VPC).
- Existe una **Main Route Table** (por defecto).

# 📑 Cuadro Resumen

| Componente         | Función                                                                |
| ------------------ | ---------------------------------------------------------------------- |
| **VPC**            | Red privada virtual en AWS, aislada y dedicada a tu cuenta.            |
| **Subnet**         | División de la VPC en rangos de IP; públicas o privadas; 1 AZ.         |
| **CIDR**           | Define el rango de IPs; /16 a /28; no se puede cambiar.                |
| **IPs reservadas** | 5 IPs por subnet no utilizables (red, router, DNS, futuro, broadcast). |
| **Elastic IP**     | IP pública estática, reasignable, puede tener costo.                   |
| **ENI**            | Interfaz de red virtual; puede moverse entre instancias.               |
| **Route Table**    | Conjunto de reglas de enrutamiento; cada subnet requiere una.          |
```mermaid

flowchart TD
    A[VPC] --> B[Subnets]
    B --> B1["Public Subnet - acceso a Internet"]
    B --> B2["Private Subnet - sin acceso directo"]
    A --> C["CIDR Block - rango IP"]
    C --> C1["/16 (65,536 IPs)"]
    C --> C2["/28 (16 IPs)"]
    B --> D["Reserved IPs (5 por subnet)"]
    A --> E["Elastic Network Interface - ENI"]
    A --> F["Route Tables"]
    F --> F1["Local route (default)"]
    F --> F2["Custom routes → IGW o NAT"]
    A --> G["Tipos de IP"]
    G --> G1["Privadas - por defecto"]
    G --> G2["Públicas - Auto-assign o Elastic IP"]


