
## Conceptos de Red

- Una red es un conjunto de **máquinas clientes conectadas** para compartir recursos.
- Se puede dividir lógicamente en **subredes** (_subnets_).
- Requiere dispositivos de red (ej. router, switch) para permitir la comunicación.

## Direcciones IP

- Cada máquina tiene una **IP única** que la identifica.
- **IPv4**:
    - 32 bits → representados en 4 bloques de 0–255 (ej: `192.0.2.0`).
    - Máximo de ~4.3 mil millones de direcciones.
- **IPv6**:
    - 128 bits → 8 grupos de 4 caracteres hexadecimales separados por `:` (ej: `2600:1f18:22ba:8c00:ba86:a05e:a5ba:00FF`).
    - Mucho mayor capacidad de dispositivos que IPv4.
## CIDR (Classless Inter-Domain Routing)

- Forma de **expresar rangos de IP consecutivas**.
- Sintaxis: `Dirección_IP/prefijo`.
    - Ej: `192.0.2.0/24`
        - `/24` → los primeros 24 bits son fijos, los últimos 8 pueden variar → **256 IPs** (`192.0.2.0` → `192.0.2.255`).
    - Ej: `192.0.2.0/16` → **65,536 IPs**.
- Casos especiales:
    - `/32` → una sola IP (ej: firewall reglas para un host).
    - `0.0.0.0/0` → internet completo (todas las IPs).


```mermaid
mindmap
  root((VPC Basics))
    Redes
      ::Máquinas conectadas
      ::Subredes (Subnets)
      ::Routers / Switches
    Direcciones IP
      IPv4
        ::32 bits
        ::Ej: 192.0.2.0
      IPv6
        ::128 bits
        ::Ej: 2600:1f18:22ba...
    CIDR
      ::Formato: IP/prefijo
      ::/24 → 256 IPs
      ::/16 → 65,536 IPs
      ::/32 → 1 IP
      ::0.0.0.0/0 → Internet
    OSI Model
      ::7 Capas
      ::Hubs/Switches = Capa 2
      ::Routers = Capa 3
      ::Base de comunicación en VPC
      
````


## Modelo OSI (Open Systems Interconnection)

- Modelo conceptual de **7 capas** para entender cómo viaja la información en una red.
- Ejemplos:
    - **Capa 2 (Enlace de datos)**: hubs, switches.      
    - **Capa 3 (Red)**: routers.
- También se aplica para comprender la comunicación dentro de una **VPC en AWS**.

|Capa|Nombre|Función principal|Ejemplos|
|---|---|---|---|
|**7**|Aplicación|Interacción con el usuario|HTTP, FTP, DNS|
|**6**|Presentación|Traducción y encriptación de datos|SSL/TLS, JPEG, ASCII|
|**5**|Sesión|Establece y mantiene la sesión|NetBIOS, RPC|
|**4**|Transporte|Control de flujo y entrega confiable|TCP, UDP|
|**3**|Red|Dirección y enrutamiento|IP, ICMP, Routers|
|**2**|Enlace de datos|Comunicación entre nodos|Ethernet, Switches|
|**1**|Física|Transmisión de bits en el medio|Cables, Fibra, Hubs|