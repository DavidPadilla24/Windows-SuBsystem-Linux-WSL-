## Instalación

**Paso 1: Habilitar WSL**

1. Abre PowerShell como administrador y ejecuta el siguiente comando:
   
   ``` dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart ```


2. Habilita la característica de Máquina Virtual:

  ``` dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart ```


3. Reinicia tu computadora para aplicar los cambios.


**Paso 2: Actualizar el kernel de WSL 2**

Actualización de la versión de WSL 1 a WSL 2
Las nuevas instalaciones de Linux, instaladas con el comando wsl --install, se establecerán en WSL 2 de forma predeterminada.

El comando wsl --set-version se puede usar para cambiar de WSL 2 a WSL 1 o para actualizar distribuciones de Linux instaladas previamente de WSL 1 a WSL 2.

Para ver si la distribución de Linux está establecida en WSL 1 o WSL 2, use el comando wsl -l -v.

Para cambiar de versión, use el comando: wsl --set-version <distro name> 2. Sustituya <distro name> por el nombre de la distribución de Linux que quiera actualizar. Por ejemplo, wsl --set-version Ubuntu-20.04 2 establecerá la distribución de Ubuntu 20.04 para usar WSL 2.

Si instaló WSL manualmente antes de que estuviera disponible el comando wsl --install, es posible que también tenga que habilitar el componente opcional de máquina virtual usado por WSL 2 e instalar el paquete de kernel si aún no lo ha hecho.

Para obtener más información, consulte la Referencia de comandos para WSL para obtener una lista de comandos WSL, Comparación de WSL 1 con WSL 2 para obtener instrucciones sobre cuál usar en su escenario de trabajo, o Procedimientos recomendados para configurar un entorno de desarrollo de WSL para obtener instrucciones generales sobre cómo configurar un buen flujo de trabajo de desarrollo con WSL.

Comprobación de la versión de WSL que se está ejecutando
Para enumerar las distribuciones de Linux instaladas y comprobar en qué versión de WSL está establecida cada una, puede escribir el comando wsl -l -v en PowerShell o en el Símbolo del sistema de Windows.

Para establecer la versión predeterminada en WSL 1 o WSL 2 cuando se instala una nueva distribución de Linux, use el comando wsl --set-default-version <Número de Versión>, reemplazando <Número de Versión> por 1 o 2.

Para establecer la distribución predeterminada de Linux que se usa con el comando wsl, escriba wsl -s <Nombre de la Distribución> o wsl --set-default <Nombre de la Distribución>, reemplazando <Nombre de la Distribución> por el nombre de la distribución de Linux que le gustaría usar. Por ejemplo, en PowerShell/CMD, escriba wsl -s Debian para establecer la distribución predeterminada en Debian. Ahora, al ejecutar wsl npm init desde PowerShell, se ejecutará el comando npm init en Debian.

Para ejecutar una distribución de WSL específica desde PowerShell o el Símbolo del sistema de Windows sin cambiar la distribución predeterminada, use el comando wsl -d <Nombre de la Distribución>, reemplazando <Nombre de la Distribución> por el nombre de la distribución que desea usar.

**Paso 3:Establecer WSL 2 como predeterminado**

1. En PowerShell, ejecuta: ``` wsl --set-default-version 2 ```

