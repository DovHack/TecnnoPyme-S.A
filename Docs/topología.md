# Topología de Red – TecnoPYME S.A.

## 1. Visión general
La infraestructura de red de **TecnoPYME S.A.** se encuentra distribuida en **tres plantas**, organizadas por departamentos. El diseño sigue una arquitectura jerárquica simple, adecuada para una PYME, con un **switch central (core/distribución)** y switches de acceso por piso.

El enrutamiento entre VLANs se realiza mediante **Router-on-a-Stick**, centralizando la lógica de red y facilitando la administración.

---

## 2. Distribución por pisos

### Piso 1 – Administración y Acceso principal
**Departamentos:**
- ADMIN
- GUEST

**Dispositivos:**
- Router principal
- Switch 2960 (Switch Piso 1)
- Access Point (AP-PT)
- Laptop Gerente (ADMIN)
- PC Asistente Administrativo (ADMIN)

**Descripción:**
El piso 1 aloja el **núcleo de la red**, donde se encuentra el router principal y el switch central. Desde este punto se distribuye la conectividad hacia los demás pisos. El acceso inalámbrico permite conectividad para usuarios invitados y personal administrativo.

---

### Piso 2 – Tecnología y Gestión
**Departamentos:**
- IT
- MGMT

**Dispositivos:**
- Switch 2960 (Switch Piso 2)
- Access Point (AP-PT)
- 2 PCs Técnico IT
- Laptop Supervisor IT
- Servidor (Server0)
- 2 PCs Técnico MGMT
- Laptop Supervisor MGMT

**Descripción:**
Este piso concentra los recursos tecnológicos y de gestión de la red. El servidor se encuentra en la VLAN de IT y provee servicios internos. La VLAN MGMT está destinada a tareas administrativas y de gestión de infraestructura.

---

### Piso 3 – Producción / Ventas
**Departamento:**
- SALES

**Dispositivos:**
- Switch 2960 (Switch Piso 3)
- 1 PC Supervisor de Planta
- 8 PCs Operadores
- 1 Impresora de red

**Descripción:**
El piso 3 corresponde al área de producción/ventas, con una alta densidad de dispositivos finales. Todo el tráfico de este piso se encuentra segmentado en la VLAN SALES para aislarlo del resto de la red corporativa.

---

## 3. Rol de los switches

### Switch Piso 1 – Core / Distribución
- Punto central de la red
- Conecta directamente al router principal
- Mantiene enlaces trunk hacia:
  - Switch Piso 2
  - Switch Piso 3
- Transporta todas las VLANs del entorno

**Rol:** Core y distribución

---

### Switch Piso 2 – Acceso
- Proporciona conectividad a dispositivos de IT y MGMT
- Maneja VLANs IT y MGMT
- Enlace trunk hacia el switch del piso 1

**Rol:** Acceso

---

### Switch Piso 3 – Acceso
- Proporciona conectividad a dispositivos del departamento SALES
- Maneja exclusivamente la VLAN SALES
- Enlace trunk hacia el switch del piso 1

**Rol:** Acceso

---

## 4. Consideraciones de diseño
- Se evita el uso de VLAN 1 para tráfico de usuarios
- La segmentación por pisos facilita el troubleshooting y la escalabilidad
- El diseño permite agregar nuevos departamentos o dispositivos sin cambios estructurales mayores
- La topología es coherente con entornos reales de pequeñas y medianas empresas

---

## 5. Observaciones
La topología definida sirve como base para las siguientes fases del proyecto: cableado, configuración de VLANs, enrutamiento inter-VLAN, pruebas y aplicación de medidas básicas de seguridad.
