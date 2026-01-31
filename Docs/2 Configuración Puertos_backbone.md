# Documentación de Puertos Backbone – TecnoPYME S.A

>Puertos backbone: Los puertos backbone son interfaces dedicadas a la interconexión entre dispositivos de red principales (router y switches), por donde circula el tráfico agregado de múltiples VLANs.
Se utilizan para enlaces troncales, priorizando capacidad, estabilidad y organización de la infraestructura. 


## Objetivo
Este documento describe la interconexión física y lógica de los puertos de red entre el router y los switches de la infraestructura de TecnoPYME S.A., con el fin de facilitar mantenimiento, escalabilidad y troubleshooting.

---

## Criterios de diseño
- Los enlaces **router–switch** y **switch–switch** utilizan **puertos GigabitEthernet** por ser enlaces de backbone.
- Los puertos **FastEthernet 0/1 a 0/5** de cada switch se mantienen **reservados para expansión futura** o dispositivos de red.
- Los enlaces entre switches operan en **modo trunk**.
- Se utiliza un esquema de nombrado consistente para todos los dispositivos y puertos.

---

## Interconexión de dispositivos

### Router a Switch Piso 1
- **R1 G0/0** → **SW-P1 G0/1**  
  - Rol: Uplink principal / Gateway LAN  
  - Tipo de enlace: Trunk  

---

### Switch Piso 1 a Switch Piso 2
- **SW-P1 G0/2** → **SW-P2 G0/1**  
  - Rol: Backbone inter-switch  
  - Tipo de enlace: Trunk  

---

### Switch Piso 2 a Switch Piso 3
- **SW-P2 G0/2** → **SW-P3 G0/1**  
  - Rol: Backbone inter-switch  
  - Tipo de enlace: Trunk  

---

## Puertos reservados
En cada switch:
- **FastEthernet 0/1 – 0/5**  
  - Estado: Reservados  
  - Uso previsto: Expansión futura / Dispositivos de red / Troubleshooting  
  - Nota: No utilizar para estaciones de trabajo sin revisión del diseño.

---

## Observaciones
- Cualquier cambio en la asignación de puertos debe reflejarse en este documento.
- Este archivo forma parte de la documentación base del proyecto de red.

