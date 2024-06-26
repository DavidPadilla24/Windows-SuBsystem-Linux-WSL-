## Instalación de Linux en Windows con WSL
Los desarrolladores pueden acceder a la potencia de Windows y Linux al mismo tiempo en una máquina Windows. Subsistema de Windows para Linux (WSL) permite a los desarrolladores instalar una distribución de Linux (como Ubuntu, OpenSUSE, Kali, Debian, Arch Linux, etc.) y usar aplicaciones, utilidades y herramientas de línea de comandos de Bash directamente en Windows, sin modificar, sin la sobrecarga de una máquina virtual tradicional o una configuración de arranque dual.

## Prerrequisitos

Para ejecutar los siguientes comandos, debe ejecutar Windows 10 versión 2004 y posteriores (compilación 19041 y posteriores) o Windows 11. Si está en versiones anteriores, consulte la [página de instalación manual](https://learn.microsoft.com/es-es/windows/wsl/install-manual).


## Comando de instalación de WSL

Ahora puede instalar todo lo que necesita para ejecutar WSL con un solo comando. Abra PowerShell o el símbolo del sistema de Windows como administrador; para ello, haga clic con el botón derecho y seleccione "Ejecutar como administrador", escriba el comando `wsl --install` y reinicie la máquina.

### PowerShell

```powershell
wsl --install

Este comando habilitará las características necesarias para ejecutar WSL e instalará la distribución Ubuntu de Linux. (Esta distribución predeterminada se puede cambiar).

La primera vez que inicie una distribución de Linux recién instalada, se abrirá una ventana de la consola y se le pedirá que espere a que los archivos se descompriman y se almacenen en el equipo. Todos los inicios posteriores deberían tardar menos de un segundo en completarse.
````poweshell
wsl --list --online para ver una lista de distribuciones disponibles y ejecute 
wsl --install -d <DistroName> para instalar una distribución.
```

Si desea instalar distribuciones adicionales desde dentro de una línea de comandos de Linux/Bash (en lugar de hacerlo desde PowerShell o el símbolo del sistema), debe usar `.exe` en el comando `wsl.exe --install -d <Nombre de la Distribución>` o para enumerar las distribuciones disponibles: `wsl.exe -l -o`.

## Cambio de la distribución predeterminada de Linux instalada

De forma predeterminada, la distribución de Linux instalada será Ubuntu. Se puede cambiar mediante la marca `-d`.

Para cambiar la distribución instalada, escriba: `wsl --install -d <Nombre de la Distribución>`. Reemplace `<Nombre de la Distribución>` por el nombre de la distribución que desea instalar.

Para ver una lista de las distribuciones de Linux disponibles para descargar a través de la tienda en línea, escriba `wsl --list --online` o `wsl -l -o`.

Para instalar distribuciones de Linux adicionales después de la instalación inicial, también puede usar el comando `wsl --install -d <Nombre de la Distribución>`.

