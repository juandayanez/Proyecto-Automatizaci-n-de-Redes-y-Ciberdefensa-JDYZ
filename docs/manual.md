# Manual de Usuario - Network Builder Pro

## Instalación y Ejecución
La herramienta está desarrollada nativamente en HTML5, CSS3 y JavaScript (Vanilla), por lo que **no requiere instalación**.
1. Descargue el archivo `topologia.html`.
2. Haga doble clic sobre el archivo para abrirlo en su navegador web predeterminado.

## Uso Paso a Paso
**Paso 1: Configuración Inicial**
- Al abrir la aplicación, ingrese los datos de su proyecto: Nombre de la empresa, ASN, y las redes base IPv4 e IPv6.
- Defina el tamaño de la red indicando la cantidad de pisos (VLANs) y los usuarios por piso.
- Haga clic en el botón "Construir Arquitectura de Red".

**Paso 2: Visualización de Topología**
- Navegue a la pestaña **Topología Lógica**. Podrá interactuar con el grafo de red, mover los nodos (Router, Switches, PCs) y analizar las conexiones físicas simuladas.

**Paso 3: IP Planning**
- Vaya a la pestaña **IP Planning**. Aquí encontrará la tabla de enrutamiento y direccionamiento.
- Utilice el menú desplegable superior para filtrar la vista por pisos específicos o ver solo el Router Core.

**Paso 4: Generación de Scripts y Ciberdefensa**
- Navegue a **Scripts CLI**.
- Seleccione en el menú desplegable el fabricante del equipo que desea configurar (Cisco, Huawei, Fortinet o MikroTik).
- Haga clic en "Generar CLI". El código aparecerá en la consola inferior, listo para ser copiado y pegado en la terminal del dispositivo real.
