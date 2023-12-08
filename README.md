# SOC-lab: 

## Configuración del Entorno Virtual

### Preparar el Entorno

- Descargar e implementar una máquina virtual de Windows gratuita de Microsoft.


### Instalar Ubuntu en una Nueva VM

- Descargar el instalador ISO de Ubuntu Server 22.04.1.
- Crear una nueva VM en Workstation con las siguientes especificaciones:

### Configurar la Red en Ubuntu

- Establecer una dirección IP estática para la VM 
- Establecer un nombre de usuario/contraseña.
- Instalar el servidor OpenSSH durante la instalación.

### Configuración de la VM de Windows

- Deshabilitar permanentemente Microsoft Windows Defender
- Descargar y configurar Sysmon, una herramienta para recopilar telemetría detallada del sistema.
- Instalar y configurar LimaCharlie EDR para recopilar registros de eventos Sysmon junto con su propia telemetría.

### Configuración del Sistema de Ataque (Ubuntu VM)

- Acceder a la VM de Ubuntu a través de SSH.
- Descargar e instalar Sliver, un marco de Comando y Control (C2) de BishopFox.

## Generar nuestro C2 Payload

- Iniciar servidor Sliver en la VM de Linux.
- Generar payload C2 usando la IP estática.
- Transferir el payload a la VM de Windows.

### Iniciar Sesión de Comando y Control (C2)

- Habilitar servidor HTTP en Sliver.
- Ejecutar payload descargado en Windows.
- Verificar conexión en el servidor Sliver.
- Interactuar con la sesión C2 en Windows.

### Observar Telemetría de EDR en LimaCharlie

- Explorar eventos y procesos.
- Revisar archivos, conexiones de red.
- Analizar eventos de EDR, filtrar por IOCs.

## Actividades del atacante

### Acceso al C2 de Sliver y ejecución de comandos

- Reanudar sesión C2 en la VM de Linux.
- Acceder a la sesión C2 en la víctima.
- Verificar privilegios en el host víctima.
- Extraer lsass.exe de la memoria.

### Detección de Actividad Adversarial

- Utilizar LimaCharlie para detectar la actividad.
- Filtrar eventos de acceso a procesos sensibles.
- Crear regla de detección.
- Establecer respuesta para esta regla.

### Verificación de la Detección

- Regresar a la sesión C2 y reproducir actividad.
- Verificar detección en LimaCharlie.
- Explorar el evento detectado en la línea de tiempo.

