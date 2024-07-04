# Instrucciones para tutor

* [Inicio](./index.html)
* [Instalar VirtualBox](#instalar-virtualbox)
* [Importar Máquina Virtual (VM)](importar-máquina-virtual-vm)
* [Configurar el Teclado](#configurar-el-teclado)
* [Cargar y Activar LabView](#cargar-y-activar-labview)
* [Instalar Materiales del Curso](#instalar-materiales-del-curso)
* [Instalar Drivers](#instalar-drivers)
* [Hacer que el Emulador corra en Linux](#hacer-que-el-emulador-corra-en-linux)
* [Configurar Firmware del RPi Pico](#configurar-firmware-del-rpi-pico)
* [Conectar y Probar el RPi Pico](#conectar-y-probar-el-rpi-pico)
* [Hardware](#hardware)
* [Software de Soporte](#software-de-soporte)

## Instalar VirtualBox

Visite el sitio:

[Virtual Box Downloads](https://www.virtualbox.org/wiki/Downloads)

* Descargue la última versión e instálela.

![image](./assets/VirtualBox.png)

## Importar Máquina Virtual (VM)

Visite el sitio de GCentral para descargar una imagen de máquina virtual que contiene LabVIEW previamente instalado.
Ve a "Initiatives" y presiona el enlace "Community Training Initiative". Una vez ahí, presiona el enlace "Download the CTI VMN" para bajar la imagen de la máquina virtual.

[GCentral](https://www.gcentral.org)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/7232195/31aa4276-be32-4ff8-82da-e9752427e0d2)



Una vez descargado, vaya a Virtual Box, al menú **File >> Import Appliance into Virtualbox**, o bien presione **Ctrl+I**.

![image](./assets/VirtualBoxImportAppliance.png)

Encuentre el archivo .OVA previamente descargado y presiona el botón Next.

![image](./assets/VirtualBoxOVA.png)

De ser necesario revise los Settings de la máquina virtual. Se pueden hacer cambios con doble click en lo que se quiera modificar. Por ejemplo, es posible que el número de CPUs sea diferente.

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

## Configurar el Teclado

Para cambiar el teclado a otro idioma, abra el menu de Inicio y seleccione Settings >> Keyboard.

![image](./assets/KeyboardSetup.png)

Selecciona el teclado que le sea de mayor utilidad.

![image](./assets/KeyboardSelection.png)

## Cargar y Activar LabVIEW

Para poder activar la licencia de LabView Community Edition, se requiere una cuenta de NI activa. Si no la tiene, cree una en:

[Página Web de NI](https://www.ni.com/es.html)

![image](./assets/NIAccount1.png)

![image](./assets/NIAccount.png)

Al abrir LabVIEW, deberá dar click en el botón 'Activate LabVIEW Community Edition'.

![image](./assets/ActivateLabVIEW.png)

Esto cargará el sitio de activación utilizando Firefox.

![cargarlabview1](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/6736731b-9a83-4994-864f-93a8d5d57fd5)

Ingrese los detalles de su cuenta de usuario y la licencia de LabView se activará.

Si quiere remover una licencia, el archivo .lc se puede encontra en **/root/natinst/.config/LabView-2022/**.

![cargarlabview2](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/b5e63fa2-f7a7-4595-8769-89753523518a)

LabVIEW ahora se cargará normalmente. 

## Instalar Materiales del Curso

![materiales1](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/c43c2bb1-4db3-43ac-9227-a373ddbbfdfa)

Hemos modificado la ventana de introducción, este enlace le llevará al repositorio de Github de CTI (Community Training Initiative).

![materiales2](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/c8c0c8f8-4b1e-4fde-940b-ab1dbf77d80b)

Seleccione el curso que desea dar.

![materiales3](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/818632c1-1ee0-46c1-9fd8-11f3638e112b)

Descárguelo como un archivo .zip.

![materiales4](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/f95e034a-fe80-4985-9d82-32e610ec786e)

Haga clic en el símbolo del archivo.

![materiales5](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/5e2c6f10-8624-4195-8089-80c953fb947d)

Extraiga el archivo en /root/Desktop.

![materiales6](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/8104e85e-fde0-429c-a5e0-b954420a4111)

Debería de tener un escritorio similar a este:

![materiales7](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/2b3a148a-1ecc-4294-8eb7-36fc246cdbf5)

## Instalar Drivers

Abra **../4) LabView Instrument Drivers** en una ventana.

Usando el ícono del Sistema de archivos en el escritorio, navegue hasta **/usr/local/natinst/LabVIEW-2022-64/instr.lib**.

Arrastre el directorio HandsOnPi2040 a **../instr.lib**.

![drivers1](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/3c332951-463f-4f94-998c-b696ae12383b)

Abra LabVIEW y cree un nuevo VI. Verifique que los controladores estén en instr.lib como es de esperarse.

![drivers2](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/227b0d93-26f5-49c0-bece-909e368dd3ba)

## Hacer que el Emulador corra en Linux

El archivo CTIPicoVISAEmulator.exe debe configurarse para que sea ejecutable.

![emulador](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/2ef86806-dd98-4bed-a29c-9d2225df72c6)

## Configurar Firmware del RPi Pico

Cada Raspberry Pi Pico necesitará tener instalado el firmware del curso.

Mantenga presionado el botón BOOTSEL en el RPi Pico y conecte el cable USB a la computadora. El RPi Pico actuará como una unidad flash.

![firmware1](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/68427376-917b-47a2-92b8-25b419521375)

En la máquina virtual Linux, seleccione Devices >> USB >> Raspberry Pi RP2 Boot [0100] (o similar).

![firmware2](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/2019ff3e-9f2d-4058-9577-5022c4eb56f1)

Esto montará el disco duro en el escritorio.

![firmware3](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/8f175a08-195b-42e5-857a-6f356b3e359f)

Luego arrastre y suelte el archivo de firmware del curso en el RPi Pico. Esto instalará el firmware, y el LED del RPi Pico parpadeará una luz verde 6 veces.

![firmware4](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/de761032-adee-4c97-b92a-b2d3f7d92566)

## Conectar y Probar el RPi Pico

En la máquina virtual Linux, seleccione Devices >> USB >> Raspberry Pi Pico [0100] (o similar).

![connectandtest](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/8de21e74-d91a-49fd-9eb4-55784eb4c5fc)

Conecte el RPi Pico.

## Hardware

Raspberry Pi Pico o Pico W.

Proveedores de EE. UU. y el Reino Unido: probablemente estandaricemos Pico-W

https://www.pishop.us/product/pico-breadboard-kit/

https://thepihut.com/products/analog-test-board

https://www.waveshare.com/analog-test-board.htm

https://thepihut.com/products/breadboard-kit-for-raspberry-pi-pico


## Software de Soporte

Parte de la idea detrás de este proyecto es que no haya costos respecto al software.

La VM viene precargada con LibreOffice: es el medio preferido para leer los manuales.

La VM también tiene un programa llamado Pinta, un programa de gráficos en capas similar a Paint.net. Los diagramas de cableado están hechos con este programa.
