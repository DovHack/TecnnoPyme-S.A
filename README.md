<<Proyecto de Red Empresarial – TecnoPYME S.A.
<Descripción general

Este proyecto documenta el diseño, configuración y validación de una red empresarial simulada para TecnoPYME S.A., implementada en Cisco Packet Tracer.
El objetivo principal fue construir una red segmentada por VLANs, con enlaces backbone entre switches, enrutamiento inter-VLAN mediante Router-on-a-Stick, asignación manual de IPs y verificación completa de conectividad.

El enfoque del proyecto es práctico, estructurado y documentado, siguiendo buenas prácticas de redes empresariales.

<Objetivos del proyecto

Diseñar una topología jerárquica por pisos.

Implementar segmentación lógica mediante VLANs.

Configurar enlaces backbone (trunk 802.1Q).

Implementar Inter-VLAN Routing (Router-on-a-Stick).

Asignar direcciones IP y Gateway a todos los endpoints.

Validar conectividad intra-VLAN e inter-VLAN.

Documentar cada etapa con evidencias técnicas.

<Topología general

1 Router Cisco (Inter-VLAN Routing)

3 Switches Cisco (uno por piso)

Endpoints distribuidos por VLAN según rol

Enlaces backbone en puertos Gigabit entre switches y router

<VLANs implementadas>
VLAN ID	Nombre	Propósito
10	ADMIN	Administración
20	GUEST	Visitantes
30	TI	Tecnología
40	MGMT	Gestión de red
50	SALES	Ventas

<Direccionamiento IP>
VLAN	Red	Gateway
VLAN 10	192.168.10.0/24	192.168.10.1
VLAN 20	192.168.20.0/24	192.168.20.1
VLAN 30	192.168.30.0/24	192.168.30.1
VLAN 40	192.168.40.0/24	192.168.40.1
VLAN 50	192.168.50.0/24	192.168.50.1

El gateway de cada VLAN corresponde a una subinterfaz del router.

<Etapas del proyecto

Asignación de nombres a equipos y cableado

Implementación de puertos Gigabit

Configuración de enlaces Backbone

Definición y configuración de VLANs

Verificación de VLANs

Validación con show vlan brief

Asignación de puertos por VLAN (Switch piso 2)

Configuración Inter-VLAN Routing – Parte 1

Configuración Inter-VLAN Routing – Parte 2

Asignación de IPs y Gateway a endpoints

Evidencia conectividad Endpoint → Gateway

Evidencia conectividad Inter-VLAN

Evidencia conectividad Intra-VLAN (MGMT)

Cada etapa está documentada con comandos, salidas y capturas como evidencia.

>><Inter-VLAN Routing (Router-on-a-Stick)

Se implementó enrutamiento inter-VLAN utilizando subinterfaces sobre GigabitEthernet0/0, con encapsulación 802.1Q.

Ejemplo:

Gig0/0.10 → VLAN 10 – 192.168.10.1

Gig0/0.20 → VLAN 20 – 192.168.20.1

Gig0/0.30 → VLAN 30 – 192.168.30.1

Gig0/0.40 → VLAN 40 – 192.168.40.1

Gig0/0.50 → VLAN 50 – 192.168.50.1

>><Verificación y pruebas

Se validó:

Conectividad intra-VLAN

Conectividad inter-VLAN

Comunicación endpoint → gateway

Estado correcto de trunks

VLANs activas y propagadas por backbone

>><Comandos clave utilizados:

show vlan brief

show interfaces trunk

show ip interface brief

ping

>><Herramientas utilizadas

Cisco Packet Tracer

Cisco IOS

Git & GitHub (versionado)

Documentación en Markdown

>><Estado del proyecto

 Diseño completo
 VLANs configuradas
 Trunks operativos
 Inter-VLAN Routing funcional
 IPs y Gateways asignados
 Conectividad validada

>><Autor

Maikol Fernández Molina
Estudiante de Ingeniería en Ciberseguridad
Proyecto académico – Redes empresariales

