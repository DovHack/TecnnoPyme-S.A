# Puertos de Acceso – TecnoPYME S.A.

>> Este documento describe la asignación de puertos de acceso en los switches de la red TecnoPYME S.A., donde se conectan los dispositivos finales (PCs, laptops, impresoras, servidores y puntos de acceso).
>>Los puertos de acceso pertenecen a una única VLAN y permiten la segmentación lógica de la red por departamentos.

### Piso 1 – Administración y Guest
 - Switch: Switch Piso 1 (Cisco 2960)

 - Fa0/6 → Laptop Gerente (VLAN ADMIN)

 - Fa0/7 → PC Asistente Administrativo (VLAN ADMIN)

 - Fa0/8 → Access Point Piso 1 (VLAN GUEST)

 **Notas:**

Puertos Fa0/1–Fa0/5 reservados para crecimiento futuro.

El AP provee conectividad inalámbrica únicamente para la VLAN GUEST.


### Piso 2 – TI y MGMT
 - Switch: Switch Piso 2 (Cisco 2960)

> Departamento TI

 - Fa0/6 → PC Técnico TI 1 (VLAN TI)

 - Fa0/7 → PC Técnico TI 2 (VLAN TI)

 - Fa0/8 → Laptop Supervisor TI (VLAN TI)

 - Fa0/9 → Server0 (VLAN TI)


>Departamento MGMT

- Fa0/10 → PC Técnico MGMT 1 (VLAN MGMT)

- Fa0/11 → PC Técnico MGMT 2 (VLAN MGMT)

- Fa0/12 → Laptop Supervisor MGMT (VLAN MGMT)

- Fa0/13 → Access Point Piso 2 (VLAN MGMT o VLAN dedicada si se amplía)

**Notas:**

Separación lógica estricta entre TI y MGMT mediante VLANs.

Servidor ubicado en TI por control y mantenimiento.


### Piso 3 – Producción (SALES)
- Switch: Switch Piso 3 (Cisco 2960)

- Fa0/6 → PC Supervisor de Planta (VLAN SALES)

- Fa0/7 → PC Operador 1 (VLAN SALES)

- Fa0/8 → PC Operador 2 (VLAN SALES)

- Fa0/9 → PC Operador 3 (VLAN SALES)

- Fa0/10 → PC Operador 4 (VLAN SALES)

- Fa0/11 → PC Operador 5 (VLAN SALES)

- Fa0/12 → PC Operador 6 (VLAN SALES)

- Fa0/13 → PC Operador 7 (VLAN SALES)

- Fa0/14 → PC Operador 8 (VLAN SALES)

Fa0/15 → Impresora de Producción (VLAN SALES)

**Notas: Alta densidad de dispositivos concentrados en una sola VLAN. Ideal para aplicar políticas futuras de QoS o ACLs.**

