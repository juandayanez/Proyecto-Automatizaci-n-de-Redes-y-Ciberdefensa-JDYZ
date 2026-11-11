# Herramienta de Redes WAN - Juan David Yañez Zabala (trabajo individual)
Materia: Interconexión de Redes WAN
Repositorio (público): [Pega aquí la URL de tu repositorio]

## Qué hace esta herramienta
Aplicación web interactiva que automatiza el diseño lógico de redes empresariales, calcula subredes (IPv4/IPv6 EUI-64), renderiza la topología gráfica y genera scripts de configuración seguros (Zero Trust) para múltiples fabricantes.

## Funciones
- Subnetting / IP Planning (IPv4/IPv6, público/privado)
- Carga de la topología (dispositivos, enlaces, ISP)
- Generación de configuraciones: Cisco, Huawei, Fortinet, MikroTik
- Ciberdefensa contra IA (aplica docs/politicas-ia.md)

## Cómo ejecutarla
1. Descargar o clonar este repositorio en tu equipo local.
2. Abrir el archivo `topologia.html` en cualquier navegador web moderno (Google Chrome, Edge, Firefox). No requiere servidores locales ni bases de datos.

## Pruebas y % de confianza (Corte 3)
- Pruebas superadas: 10 de 10 = 100% (ver docs/pruebas.md)

## Documentos
- docs/informe-corte2.pdf · docs/informe-corte3.pdf
- docs/manual.md · docs/seguridad.md · docs/politicas-ia.md · docs/pruebas.md

## Capturas (evidencias)
docs/capturas/ (01-subnetting.png ... 10-app-final.png)

## Autoevaluación (marca Sí/No)
| Criterio | ¿Cumplido? | Evidencia |
|-------------------------------------|------------|-------------------------|
| Subnetting funciona                 | Sí         | 01-subnetting.png       |
| Carga de topología                  | Sí         | 02-topologia.png        |
| Config Cisco y Huawei               | Sí         | 03 / 04                 |
| Config Fortinet y MikroTik (C3)     | Sí         | 06 / 07                 |
| Ciberdefensa (politicas-ia.md)      | Sí         | 08-ciberdefensa.png     |
| Pruebas con % de confianza (C3)     | Sí         | docs/pruebas.md         |
