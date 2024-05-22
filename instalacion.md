## Instalación

**Paso 1: Habilitar WSL**

1. Abre PowerShell como administrador y ejecuta el siguiente comando:
   ```powershell
   dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart


2. Habilita la característica de Máquina Virtual:

  dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart


3. Reinicia tu computadora para aplicar los cambios.


**Paso 2: Actualizar el kernel de WSL 2**

1. Descarga el último paquete de actualización del kernel de Linux para WSL 2.

2. Instálalo siguiendo las instrucciones del asistente.

**Paso 3:Establecer WSL 2 como predeterminado**

1. En PowerShell, ejecuta: wsl --set-default-version 2

