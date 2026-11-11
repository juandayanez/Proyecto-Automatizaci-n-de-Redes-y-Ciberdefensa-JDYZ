# Políticas de Ciberdefensa contra Inteligencia Artificial (Anti-IA)

El auge de agentes autónomos y bots basados en IA requiere adaptar la infraestructura para prevenir escaneos de vulnerabilidades automatizados y movimientos laterales no autorizados. La herramienta implementa las siguientes políticas:

1. **Enfoque Zero Trust Network Access (ZTNA) en ACLs:**
   - **Default Deny (Denegación por Defecto):** Todas las listas de control de acceso (ACLs) terminan con una regla explícita de `deny ip any any log`. Cualquier paquete no autorizado explícitamente es descartado y registrado, frustrando el descubrimiento de red por parte de IAs maliciosas.
   - **Segmentación de Administración:** El acceso a los puertos de gestión (SSH) está restringido única y exclusivamente a la subred de administración (`192.168.10.0/24`). Ningún agente desde otra VLAN puede alcanzar la línea VTY de los equipos Core.

2. **Manejo Seguro de Secretos:**
   - La aplicación no guarda credenciales maestras predecibles en su código fuente (frontend). Las contraseñas generadas combinan el identificador del proyecto, el ASN y caracteres especiales, evitando patrones que un modelo de lenguaje (LLM) pueda predecir fácilmente.

3. **Validación de Entradas (Front-end):**
   - El formulario de generación restringe y valida los tipos de datos (números, rangos, y máscaras válidas) impidiendo inyecciones de código malicioso o configuraciones desbordadas (ej. generación masiva de bucles o VLANs inexistentes).
