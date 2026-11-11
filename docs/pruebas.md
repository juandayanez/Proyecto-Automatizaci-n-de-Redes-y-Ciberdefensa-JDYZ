# Plan de Pruebas y Validación (Corte 3)

Se ejecutaron 10 pruebas unitarias y de integración sobre la herramienta para validar su funcionamiento correcto.

| ID | Descripción de la Prueba | Resultado Esperado | Estado |
|----|--------------------------|--------------------|--------|
| 01 | Carga de formulario inicial y validación de datos nulos. | La app no genera la red si faltan datos críticos. | ✅ Superado |
| 02 | Cálculo de subredes IPv4 por piso (CIDR /24). | Asignación secuencial correcta (VLAN 10 = .10, VLAN 20 = .20). | ✅ Superado |
| 03 | Cálculo algorítmico EUI-64 para IPv6. | Inversión correcta del séptimo bit en la dirección MAC generada. | ✅ Superado |
| 04 | Renderizado de topología lógica (`vis-network`). | Grafo jerárquico visible con Core, Switches y PCs interactivos. | ✅ Superado |
| 05 | Filtrado dinámico en IP Planning. | La tabla muestra únicamente los equipos del piso seleccionado. | ✅ Superado |
| 06 | Generación de Script Cisco (Router Core). | Salida CLI con OSPF, SSH, RSA y ACLs aplicadas. | ✅ Superado |
| 07 | Generación de Script Huawei (Switches Acceso). | Salida CLI con VLANs, Port Security, RSTP y AAA local. | ✅ Superado |
| 08 | Generación de Script Fortinet (Firewall). | Reglas de bloqueo explícito aplicadas a Telnet y tráfico bot. | ✅ Superado |
| 09 | Generación de Script MikroTik (Borde). | Reglas en firewall filter limitando el escaneo de puertos. | ✅ Superado |
| 10 | Cálculo del presupuesto comercial en COP. | Multiplicación exacta de las cantidades por el valor base del equipo. | ✅ Superado |

### **Resultado de Confianza**
- **Pruebas superadas:** 10 de 10
- **Porcentaje de confianza de la herramienta:** **100%**
