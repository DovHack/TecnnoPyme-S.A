#   Infraestructura de Red Corporativa Segmentada por VLANs – Packet Tracer

##           Descripción del proyecto
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
Estudiante de Ingeniería en Ciberseguridad / Técnico redes
Proyecto académico y práctico de networking

