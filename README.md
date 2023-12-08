# SOC-lab: 

# Configuración del Entorno Virtual

## Preparar el Entorno

- Descargar e implementar una máquina virtual de Windows gratuita de Microsoft.


## Instalar Ubuntu en una Nueva VM

- Descargar el instalador ISO de Ubuntu Server 22.04.1.
- Crear una nueva VM en Workstation con las siguientes especificaciones:

## Configurar la Red en Ubuntu

- Establecer una dirección IP estática para la VM 
- Establecer un nombre de usuario/contraseña.
- Instalar el servidor OpenSSH durante la instalación.

# Configuración de la VM de Windows

## Desactivar Windows Defender

- Iniciar la VM de Windows.
- Deshabilitar permanentemente Microsoft Defender
- Descargar y configurar Sysmon, una herramienta para recopilar telemetría detallada del sistema.
- Instalar y configurar LimaCharlie EDR para recopilar registros de eventos Sysmon junto con su propia telemetría.

# Configuración del Sistema de Ataque (Ubuntu VM)

## Preparar el Sistema de Ataque desde la VM de Linux

- Acceder a la VM de Ubuntu a través de SSH.
- Descargar e instalar Sliver, un marco de Comando y Control (C2) de BishopFox.
