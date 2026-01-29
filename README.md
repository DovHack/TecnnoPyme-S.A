# 📡 Infraestructura de Red Corporativa Segmentada por VLANs – Packet Tracer

## 📌 Descripción del proyecto
Este proyecto consiste en el diseño, configuración y puesta en marcha de una **infraestructura de red corporativa** simulada en **Cisco Packet Tracer**, enfocada en la **segmentación lógica mediante VLANs**, interconexión segura y buenas prácticas básicas de networking.

El escenario representa una **PYME** con múltiples departamentos que requiere aislamiento de tráfico, mejor administración de red y una base escalable para crecimiento futuro.


## Objetivos
- Diseñar una red LAN corporativa con **mínimo 20 dispositivos**
- Implementar **segmentación por VLANs**
- Configurar **trunking 802.1Q**
- Implementar **Inter-VLAN Routing (Router-on-a-Stick)**
- Aplicar **buenas prácticas básicas de seguridad**- Verificar conectividad y aislamiento entre segmentos


##  Topología general
- 1 Router Cisco (ISR)
- 2 Switches Cisco 2960
- 20 End Devices (PCs / Laptops)
- (Opcional) 1 Servidor

Total aproximado: **23–24 dispositivos**

La topología utiliza:
- Enlaces **trunk** entre switches
- Enlace **trunk** entre router y switch principal
- Puertos **access** para dispositivos finales


##  Segmentación por VLANs

| VLAN ID | Nombre | Departamento        | Red IP              |
|-------|--------|---------------------|---------------------|
| 10    | ADMIN  | Administración      | 192.168.10.0/24     |
| 20    | SALES  | Ventas              | 192.168.20.0/24     |
| 30    | IT     | Tecnología          | 192.168.30.0/24     |
| 40    | GUEST  | Invitados           | 192.168.40.0/24     |
| 99    | MGMT   | Gestión de red      | 192.168.99.0/24     |

Cada VLAN cuenta con al menos **4 dispositivos finales**, excepto MGMT.


## Configuraciones implementadas

### Switching
- Creación y nombrado de VLANs
- Asignación de puertos en modo `access`
- Configuración de enlaces `trunk`
- Desactivación de puertos no utilizados
- Uso de VLAN dedicada para gestión

### Routing
- Router-on-a-Stick
- Subinterfaces por VLAN
- Gateway por defecto para cada red

- Enrutamiento entre VLANs

### Seguridad básica
- No uso de VLAN 1 para usuarios
- Puertos no usados asignados a VLAN “BLACKHOLE”
- DTP deshabilitado en enlaces trunk
- (Opcional) Port Security en puertos de acceso
- (Opcional) ACL para restringir tráfico de GUEST



## Pruebas y validación

Se realizaron las siguientes verificaciones:

- Conectividad entre dispositivos de la **misma VLAN**
- Conectividad entre dispositivos de **diferentes VLANs**
- Comprobación de trunking:
  ```bash
  show interfaces trunk
Verificación de VLANs:

show vlan brief
Verificación de routing:

show ip route
📂 Estructura del repositorio
├── packet-tracer/
│   └── infraestructura_vlan_corporativa.pkt
├── docs/
│   ├── topologia.png
│   └── direccionamiento_ip.md
├── evidencias/
│   └── pruebas_conectividad.md
└── README.md

Aprendizajes clave
Este proyecto refuerza conceptos fundamentales como:

Segmentación lógica

Enrutamiento interno

Buenas prácticas Cisco

Documentación técnica


# Infraestructura de Red Corporativa Segmentada por VLANs – Packet Tracer

## Descripción del proyecto
Este proyecto consiste en el diseño, configuración y puesta en marcha de una **infraestructura de red corporativa** simulada en **Cisco Packet Tracer**, enfocada en la **segmentación lógica mediante VLANs**, interconexión segura y buenas prácticas básicas de networking.

El escenario representa una **PYME** con múltiples departamentos que requiere aislamiento de tráfico, mejor administración de red y una base escalable para crecimiento futuro.



## Objetivos
- Diseñar una red LAN corporativa con **mínimo 20 dispositivos**
- Implementar **segmentación por VLANs**
- Configurar **trunking 802.1Q**
- Implementar **Inter-VLAN Routing (Router-on-a-Stick)**
- Aplicar **buenas prácticas básicas de seguridad**
- Verificar conectividad y aislamiento entre segmentos


##  Topología general
- 1 Router Cisco (ISR)
- 2 Switches Cisco 2960
- 20 End Devices (PCs / Laptops)
- (Opcional) 1 Servidor

Total aproximado: **23–24 dispositivos**

La topología utiliza:
- Enlaces **trunk** entre switches
- Enlace **trunk** entre router y switch principal
- Puertos **access** para dispositivos finales



##  Segmentación por VLANs

| VLAN ID | Nombre | Departamento        | Red IP              |
|-------|--------|---------------------|---------------------|
| 10    | ADMIN  | Administración      | 192.168.10.0/24     |
| 20    | SALES  | Ventas              | 192.168.20.0/24     |
| 30    | IT     | Tecnología          | 192.168.30.0/24     |
| 40    | GUEST  | Invitados           | 192.168.40.0/24     |
| 99    | MGMT   | Gestión de red      | 192.168.99.0/24     |

Cada VLAN cuenta con al menos **4 dispositivos finales**, excepto MGMT.

---

## Configuraciones implementadas

### Switching
- Creación y nombrado de VLANs
- Asignación de puertos en modo `access`
- Configuración de enlaces `trunk`
- Desactivación de puertos no utilizados
- Uso de VLAN dedicada para gestión

### Routing
- Router-on-a-Stick
- Subinterfaces por VLAN
- Gateway por defecto para cada red
- Enrutamiento entre VLANs

### Seguridad básica
- No uso de VLAN 1 para usuarios
- Puertos no usados asignados a VLAN “BLACKHOLE”
- DTP deshabilitado en enlaces trunk
- (Opcional) Port Security en puertos de acceso
- (Opcional) ACL para restringir tráfico de GUEST



Autor:
Maikol Fernández
Estudiante de Ingeniería en Ciberseguridad
Proyecto académico y práctico de networking

