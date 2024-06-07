# Instrucciones para tutor

* [Inicio](./index.html)
* [Instalar VirtualBox]
* [Importar Máquina Virtual (VM)]
* [Configurar el Teclado]
* [Cargar y Activar LabView]
* [Instalar Materiales del Curso]
* [Instalar Drivers]
* [Hacer que Emulador.exe corra en Linux]
* [Configurar Firmware del RPi Pico]
* [Conectar y Probar el RPi Pico]
* [Hardware]
* [Software de Soporte]

## Instalar VirtualBox

Visite el sitio:

[Virtual Box Downloads](https://www.virtualbox.org/wiki/Downloads)

* Descargue la última versión e instálela.

![image](./assets/VirtualBox.png)

## Importar Máquina Virtual (VM)

Visite el sitio de GCentral para descargar una imagen de máquina virtual que contiene LabVIEW previamente instalado:

[GCentral - Community Training Initiative](https://www.gcentral.org/g-community-resources/community-training-image)

![image](./assets/GCentralmage.png)

Una vez descargado, vaya a Virtual Box, al menú **File >> Import Appliance into Virtualbox**, o bien presione **Ctrl+I**.

![image](./assets/VirtualBoxImportAppliance.png)

Encuentre el archivo .OVA previamente descargado y presiona el botón Next.

![image](./assets/VirtualBoxOVA.png)

De ser necesario revise los Settings de la máquina virtual.

![image](./assets/ApplianceSettings.png)

Presione el boton de 'Finish' y la imagen .OVA se importará y aparecerá como una nueva máquina virtual.

![image](./assets/OVAImport.png)

Al finalizar, podrá ejecutar la máquina virtual haciendo click en el botón 'Start'.

![image](./assets/OpenVM.png)

La máquina virtual deberá arrancar, pero se requiere iniciar como usuario 'root' para poder activar LabVIEW Community, para iniciar como 'root' hay que salir del usuario actual

![image](./assets/VMLogout.png)

![image](./assets/VMLogoutDialog.png)

Haga click en el usuario actual 'LabVIEW Training' y seleccione 'Other'.

![image](./assets/LabVIEWTrainingUser.png)

![image](./assets/RootUser.png)

Usuario: **root** 

Password: **labviewtraining**

Deberá ver lo siguiente:

![image](./assets/VMDesktop.png)

## Configurar del Teclado

Para cambiar el teclado a otro idioma, abra el menu de Inicio y seleccione Settings >> Keyboard.

![image](./assets/KeyboardSetup.png)

Selecciona el teclado que le sea de mayor utilidad.

![image](./assets/KeyboardSelection.png)

# Cargar y Activar LabVIEW

Para poder activar la licencia de LabView Community Edition, se requiere una cuenta de NI activa. Si no la tiene, cree una en:

[Página Web de NI](https://www.ni.com/es.html)

![image](./assets/NIAccount1.png)

![image](./assets/NIAccount.png)

Al abrir LabVIEW, deberá dar click en el botón 'Activate LabVIEW Community Edition'.

![image](./assets/ActivateLabVIEW.png)

Esto cargará el sitio de activación utilizando Firefox.
