# Medidas de Seguridad Aplicadas (Hardening)

La herramienta genera automáticamente scripts de configuración que aplican los siguientes estándares de seguridad corporativa:

1. **Gestión de Accesos (AAA y Usuarios Locales):**
   - Se configuran usuarios administrativos locales con el máximo nivel de privilegios (`privilege 15`).
   - Las contraseñas se generan utilizando algoritmos de cifrado fuertes y no reversibles (`secret` en Cisco, `irreversible-cipher` en Huawei).

2. **Criptografía y Protocolos de Administración:**
   - Se generan llaves criptográficas RSA de 2048 bits obligatorias.
   - Se habilita exclusivamente el acceso remoto mediante **SSH** v2.
   - El protocolo Telnet (puerto 23) queda explícitamente bloqueado y deshabilitado por ser vulnerable a intercepción en texto plano.

3. **Seguridad de Capa 2 (Switching):**
   - **Port Security:** Los puertos de acceso limitan el aprendizaje a un máximo de 2 direcciones MAC por interfaz de manera persistente (`sticky`), mitigando ataques de *MAC Flooding* y suplantación.
   - **Spanning-Tree (RSTP):** Activación de protección de BPDUs (`bpdu-protection`) y puertos de borde (`edged-port`) para evitar la manipulación de la topología lógica por dispositivos no autorizados.

4. **Avisos Legales (Banners):**
   - Implementación de Banners MOTD (Message of the Day) disuasorios, declarando la propiedad de la infraestructura y advirtiendo sobre el acceso no autorizado.
