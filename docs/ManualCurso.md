[Inicio](./index.html)

* [Configurando el sistema](#configurando-el-sistema)
* [Lección 1 – LabVIEW “Hello World” LED On/Off](#lección-1--labview-hello-world-led-onoff)
* [Lección 2 – Ciclos For (For Loops)](#lección-2---ciclos-for-for-loops)
* [Lección 3 – Ciclos While (While Loop)](#lección-3---ciclos-while---while-loops)
* [Lección 4 – Estructura de Eventos (Event Structure)](#lección-4---estructura-de-eventos---event-structure)
* [Lección 5 – Numeros, Graficas y Charts](#lección-5---numeros-gráficas-y-charts)
* [Conceptos Generales](#conceptos-generales)
* [Tipos de Datos](#tipos-de-datos)
* [Ciclos While - While Loops](#ciclos-while)
* [Ciclos For - For Loops](#ciclos-for)
* [Estructuras de Eventos - Event Structures](#estructuras-de-eventos)

## Configurando el sistema
[Instrucciones para tutor](./InstruccionesTutor.html)

Para usar el emulador, clona el repositorio y cargalo navegando a /root/Desktop/GettingStartedLabVIEW1-Spanish-main/3) LabVIEW Instrument Emulator/builds/HandsOn/CTIPicoVISAEmulator/

Da click derecho y selecciona ‘Open Terminal Here’

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/9edd704c-c81b-4c34-a92f-416af763ec48)

Escribe lo siguiente: 

>./CTIPicoVISAEmulator.exe

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/f644fde9-b481-48f4-b450-e48bac99970a)

El emulador te pedirá elegir una subred.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/159f16c4-16f9-4530-b841-644f0cbbf5ad)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/3b293499-a5ea-4dd9-b082-2c3e08ba427c)

Después simplemente esperará por una conexión. “Connecting” será mostrado en la barra de estado.

# Lección 1 – LabVIEW “Hello World” LED On/Off

**Opcional**: Configurando el Hardware 

Si tienes el hardware para este curso, necesitaras configurarlo y conectarlo como lo muestra la siguiente imagen. Si no, avanza a Instrucciones.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/19efa352-e5e0-420e-9437-6cefb5fb1a49)

## Instrucciones

El equivalente en LabVIEW de un programa “Hello World” es hacer que una pieza de hardware haga algo básico, usualmente es hacer un led parpadear (ON-Off).
Arranca LabVIEW y selecciona New VI.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/4c3341c5-da7e-45ad-b18c-0185f6f0bbcf)

Acomoda las ventanas de la siguiente manera:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/7350d66a-f07d-4169-ac20-ded705dd28cd)

En LabVIEW un VI (Virtual Instrument) es el equivalente a una función o un módulo en otros lenguajes de programación. Un programa en LabVIEW esta hecho por uno o mas VIs.

En el diagrama de bloques (Block Diagram) da click derecho y navega a HandsOnPi2040 Driver Palette.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/bd6141e9-356a-44bc-8179-4b56c5abcde3)
      
Arrastra el VI Initialize.vi, WriteDO.vi y Close.vi en el diagrama de bloques como se muestra a continuacion.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/142dd1d1-fb9d-4c31-b3b4-c04780d127ff)

*Observa que la flecha para ejecutar esta rota (esta flecha esta en la esquina superior izquierda), si la presionas, la ventana de errores aparecera y vendran todas las razones por las cuales no se puede ejecutar el codigo.*

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/4e371803-0d24-445c-958a-ec8414309aab)

LabVIEW no le permitirá ejecutar el código fuente hasta que se solucionen estos errores. Cierre la Lista de errores y seleccione todos los Vis. (Haga clic con el botón izquierdo y arrastre el mouse).

Presione Ctrl+espacio para abrir 'Quick Drop' y presione 'Ctrl+W' para conectar los VIs. Quick drop es una herramienta de productividad extremadamente útil que viene con LabVIEW. Le permite automatizar tareas repetitivas con algunas combinaciones de teclas

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/b09151fb-88f6-4823-922d-639e41c5ae2a)

Si presiona la flecha Ejecutar, notará que solo hay 2 problemas enumerados, ¡buen trabajo!

Presione Ctrl-H para abrir la ventana de ayuda contextual. Pase el cursor sobre Initialize.vi.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/2b384f7c-d2fa-4ee6-9652-e3cd71acd2af)

Observe que algunas entradas estan en negrita como 'Visa Resource Name'. Esto significa que esta entrada es obligatoria.

Haga clic derecho en 'VISA Resource Name' del VI Initialize.vi y seleccione crear constante.

Si presiona la flecha Ejecutar ahora, notará que solo queda 1 error a resolver

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/c9299b51-d207-4239-95fd-ef3d75db44e4)

Este VI necesita su cableado de salida y valor DO (verdadero). Así que creemos constantes para ellos. Utilice la flecha de la derecha para seleccionar una salida

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/1000353a-eb6f-4a4b-af81-35b8e72f4637)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/e716a2d7-111b-4a47-aadd-653b44fc29bf)

Es bueno que se muestre la etiqueta constante para los booleanos.

Haga clic derecho en la constante booleana "True". Aparecerá una ventana desplegable, coloque el cursor sobre "Visible Items" y seleccione "Label".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/54096500-f600-452a-b244-107407c492ae)

Las constantes son terminales en el diagrama de bloques que suministran valores de datos fijos al diagrama. Discutiremos los tipos de datos, etc. más adelante en la sesión.

Finalmente conectemos un par de salidas.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/cf6d9b82-d9f4-432e-b8c4-a58dc475ac3e)

Haga clic derecho en IDN para Inicializar.vi y seleccione "Create Indicator". Luego necesitamos eliminar un error, así que haga clic derecho en la parte inferior de Close.vi y seleccione "Create Indicator".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/52586b53-ab80-4d8b-a49f-35b1f0e1a3da)

Observe cómo aparecen los indicadores en el panel frontal. Discutiremos los diagramas de bloques y los paneles frontales en un momento.

¡Ahora tenemos un programa listo para ejecutar!

Sin embargo, notarás que tendremos un error.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/7908dc72-b056-470f-b530-332540ef524c)

Podemos consultar el mensaje de error para intentar obtener una pista de por qué todo salió tan mal. A veces incluso puede resultar útil.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/062e5d5b-1a24-4af7-b5aa-cdafeef3ff3d)

En este caso el problema es

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/74f37f12-a5fd-49bd-ab48-0a0f6dd83108)

_Los VIs no saben con que hardware están vinculandose. Para solucionar este problema, los usuarios de hardware deben configurar la referencia VISA correcta en el cuadro desplegable 'VISA'. Para los usuarios del emulador, haga clic en el botón 'Copiar', como se ve en la imagen a continuación y pegue la referencia, si tiene una actualización de hardware. y seleccione la referencia ASRL._

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/ff03d635-6c29-474a-83ce-bdf153fab323)

Ahora, presione 'Run' nuevamente

El indicador de error mostrara que no hay error, el indicador de identidad habra cambiado y ahora despliega valores.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/5c2570bb-2497-4d50-9b4f-670e6ed637f1)

Pero, algo mas importante es que el LED del hardware se ha encendido!

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/465b4cdf-0aa2-4014-92a6-4eab1eb42a3c)


# Lección 2 - Ciclos For (For Loops)
Opcional: Configuración de Hardware

Conecte el hardware como la imagen siguiente:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/55b91ce8-3c9b-4bb9-8082-a911e74e7275)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/ab4506dc-f5f3-4008-a3b9-03123cd26ebf)

## Instrucciones

Un ciclo For ejecuta un sub-diagrama un numero determinado de veces. En este caso, aprenderás a construir un programa que hace parpadear un LED 10 veces antes de detenerse

Agrande su espacio de trabajo para dejar espacio para agregar objetos. Utilice Ctrl y luego arrastre para expandir

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/484becac-5d71-445e-90b0-37525819cead)


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/c7ebdddb-80e6-43cc-a645-2c6b2acd05d9)

Alternativamente, seleccione los objetos que necesita mover con la herramienta de selección y arrástrelos a donde desee con el mouse o usando las flechas.

__Nota: presione Mayús y una tecla de flecha para mover los elementos seleccionados más rápido.__

Ahora inserte un ciclo For, para hacerlo, haga clic derecho en cualquier lugar del diagrama de bloques para abrir la paleta de funciones. Seleccione 'Estructuras' y luego 'For Loop'.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/fcb44595-01e3-49f8-ac4f-7bbb2802f783)

Sólo necesitará colocar el bucle For alrededor del WriteDO SubVI (y las constantes adjuntas a él).

Una vez que se haya colocado el ciclo For, verá una 'N' en la esquina superior izquierda, este es el numero de iteraciones que realizará el ciclo For.

Haga clic derecho en la N y seleccione "Crear una constante". Para esta tarea necesitará que el número de bucles sea 20 (10 veces activado y 10 veces desactivado).

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/414e694a-ae63-41e2-a36a-63e4354bbe9b)

Para que el programa "parpadee" correctamente, necesitará saber qué se ha ejecutado en la iteración anterior, por lo que necesitará un registro de desplazamiento (shift Register).

Haga clic derecho en el borde del ciclo For y seleccione "add shift register". Conecte la constante verdadera a los registros de desplazamiento y al terminal del cable DO (valor).

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/e7da0c07-5417-48a3-b640-e2e671d020ad)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/28a02b6e-76f8-47d5-ac87-b2f6834763ae)

Si ejecutara el programa en este punto, el LED se iluminaría, pero no "parpadearía".

Para un LED parpadeante necesitarás invertir el valor booleano después de cada iteración. Para hacer esto, haga clic derecho en cualquier lugar para abrir la paleta de funciones. Pase el cursor sobre "Booleano" y luego seleccione el booleano "Not". Conecte esto al registro de desplazamiento.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/790e2351-196b-4504-8a31-4beed7c9c29b)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/fddc4fb2-9e21-4835-b9d7-37538c2a42da)

¡El programa ahora funcionará! Sin embargo, se ejecutará muy rápido y no podrá ver el LED parpadeando. Entonces necesitas reducir la velocidad del ciclo.

Haga clic derecho dentro del ciclo For y coloque el cursor sobre "Time". Allí verá muchas opciones de tiempo diferentes. Para ello utilizarás la función 'Wait'. Seleccionala y coloca dentro del Loop.

Creea una constante haciendo clic derecho en el lado izquierdo de la función "Wait". La función "Wait" se ejecuta en milisegundos, por lo tanto, para ralentizar el ciclo 5 segundos, escriba 500.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/b4139bcd-b996-4248-a196-99a3b79d2572)

Ahora ejecuta el programa. Ha utilizado con éxito un ciclo For para hacer parpadear la salida digital.

# Lección 3 - Ciclos While - While Loops

Opcional: Configuración del Hardware
Conecta el hardware de la siguiente manera:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/d5d6d0d4-3271-40d3-b116-08c1402f5202)


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/de741e88-970b-4f3c-8d0d-307193177107)



## Instrucciones

El ciclo While ejecuta el subdiagrama hasta que ocurre una condición específica. Siempre se ejecutará al menos una vez.

En este caso, deseamos que el LED parpadee continuamente hasta que se presione el botón "Stop". Puede crear esto utilizando el programa creado previamente con el For Loop.

En primer lugar, haga clic derecho en el borde del ciclo For y seleccione "Replace with While Loop".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/e46e9a0c-a3d8-4d65-8921-88aa0e509a8c)

Ahora que el ciclo For ha sido reemplazado, el Loop Count (N) no está conectado. Esto no es necesario para un ciclo While y se puede eliminar.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/2d510608-2133-4bdd-b4fb-84f7318bafa7)

Para agregar un booleano 'Stop', cambie a la ventana del panel frontal y haga clic derecho donde desea colocar el botón. Aparecerá la paleta Controles, seleccione "Boolean" y elija un botón. El ejemplo utiliza un "botón pulsador", pero cualquiera funcionará.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/4a82db62-590e-4cb7-b686-78641c159c9a)

De vuelta en el diagrama de bloques, mueva el nuevo control booleano al ciclo While y conéctelo al terminal condicional en la esquina inferior derecha. Si se presiona el botón en el panel frontal cuando el programa se está ejecutando, el bucle finalizará y el LED "parpadeante" se detendrá.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/b342eea4-0fb3-4e38-b6b3-0285ed0a56c4)

## Ejercicio - Uso de entradas digitales (DI) para detener el ciclo While
__Pista: Diagrama de cableado para entrada digital__

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/5b8ede3a-05b2-4cb2-ac67-4036c2f412d3)

__Pista: VI para entrada digital (DI)__

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/54f52bc0-7a5e-4f27-b68c-5fb68d4cdade)

# Lección 4 - Estructura de Eventos - Event Structure

Opcional: Configuración de Hardware
Conecte el hardware de la siguiente manera:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/3dd90791-c8ab-4f77-8387-0f2b7a896ca3)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/bfba31c3-231d-44f0-852b-3f20378f4bf3)

## Instrucciones

Una estructura de eventos espera hasta que ocurra un determinado evento y luego ejecuta el caso apropiado para manejar ese evento. En este ejemplo, queremos presionar un botón y la luz correspondiente para encenderla.

Primero, eliminemos el ciclo while y su contenido. Haga clic en el bucle While y presione la tecla Eliminar. Haga lo mismo con la constante "Verdadero". Luego retire los cables rotos con Ctrl+B

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/9b7012b5-e34c-4e5f-b87e-6476fc6177fc)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/db1f0425-07d1-4ba5-97cd-6980df33df38)

Haga clic derecho para abrir la paleta de funciones, coloque el cursor sobre "Estructuras" y luego seleccione "Estructura de eventos". Coloque la estructura de eventos en el diagrama de bloques

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/622c01a2-39d0-48ce-91f0-fa433fee8706)

Conecte el VI Inicializar y el VI Cerrar a través de la Estructura del Evento

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/5f2b924e-e26b-452e-824d-c8fa1420b310)


Agregue un nuevo caso de evento haciendo clic derecho en la etiqueta del selector y seleccione "Agregar caso de evento".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/eabaf06e-5cef-4096-bd08-cc7a2040c960)

Agregue WriteDO.vi abriendo la paleta de funciones, coloque el cursor sobre "Instrument I/O", "Instr Drivers", "HandsOnPi2040" y seleccione "WriteDO.vi".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/ffc7cfce-a9b2-415b-9a74-0ce61016a1a6)

Arrastre el sub VI dentro de la estructura del evento y conéctelo. Haga clic derecho en el terminal Salida y cree una Constante.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/83968bae-93f4-404d-87b1-f2b8b2fd1b79)

Cambie la salida de "NO DO - Error" a "DO1" haciendo clic en la flecha desplegable en la constante de salida.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/46e9732c-15a8-47b2-b1e7-172c74becddb)

A continuación necesitamos agregar un botón para la Salida Digital. Vaya al Panel frontal y haga clic derecho en cualquier lugar para abrir la Paleta de controles. Pase el cursor sobre "Boolean" y seleccione "Push button"


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/6f69a3fb-3296-474f-b7a6-3ab3a3e7bf20)

Conecte el nuevo control booleano al terminal 'DO Value'


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/3d3a1c4a-8979-4b19-a65d-90c390ca4e29)


Haga clic derecho en el selector de etiquetas, ya que necesitamos "Edit Events Handled by This Case"


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/f4f668c1-ad34-45ca-be7a-d92124c4b1ba)

Esto abrirá la ventana "Editar eventos". Seleccione "Boolean".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/77a94469-75c5-4d39-b9bb-dcdc7aa75e91)

Este caso de evento ya está completo. Necesitaremos 3 Casos de Eventos más, cada uno correspondiente a un LED. La forma más sencilla de hacerlo es hacer clic derecho en el selector de etiquetas y seleccionar "Duplicate Event Case".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/9058f9cc-ad66-4707-a9c7-7d1d55892312)

Seleccione 'Boolean 2' en la ventana Editar eventos.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/a6e7bdbb-ad83-40ad-b8b5-3adae35cf8f7)

Es importante cambiar la constante DO cuando el caso se ha duplicado. (DO1 para booleano, DO2 para booleano 2, etc.) Duplique este caso 2 veces más para DO3 y DO4.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/33ec6534-b6e1-4cf1-a0f9-b14acec732cb)

En este punto, su panel frontal puede verse un poco desordenado; tómese un tiempo para limpiarlo. Esto hará que sea más fácil de usar cuando haya terminado de crear el programa.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/984b7c28-6b73-4b47-a326-5f7b30bed4c2)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/03847edd-1889-430e-afbd-e0cdfda0db37)

__Podrá ejecutar el programa ahora; sin embargo, se detendrá después de seleccionar un valor booleano. Podemos hacer esto más eficiente.__

De vuelta en el diagrama de bloques necesitaremos agregar un ciclo While. Haga clic derecho para abrir la paleta de funciones, coloque el cursor sobre "Structures" y seleccione "While Loop"


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/d3604cb7-e7ce-4c32-abdd-4993d1bf80b1)

Coloque el ciclo While alrededor de la estructura del evento.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/559b21af-6ef2-4398-9058-435afdab1dca)

Vaya al Panel frontal, para que podamos agregar un botón "Stop" que conectaremos a la condición del ciclo. Haga clic derecho para abrir la paleta de controles, coloque el cursor sobre "Boolean" y luego seleccione "Stop Button".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/63692026-a3d4-4e5f-8fbe-e911a3f4c46e)

También necesitaremos crear un nuevo Caso de evento para este botón de Stop. Haga clic derecho en la etiqueta del selector y seleccione "Add Event Case".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/70c38ba9-6c0a-4dcb-b640-d057b698e3dc)

Coloque el control 'Detener' dentro del nuevo caso.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/574509f2-1b65-4303-af13-b9004b119784)

Haga clic derecho en la etiqueta del selector y seleccione "Edit Events Handled by This Case"


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/b850954f-9a5d-4865-ae39-305abdebcbbd)

Cuando aparezca la ventana "Edit Events", elija la opción "Stop" en la tabla "Event Sources".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/960609b9-c1bf-4461-8a4a-72715f34399d)

Nuestro último paso es conectar una constante "Verdadera" a la condición de ciclo. Haga clic derecho para abrir la paleta de funciones, coloque el cursor sobre "Boolean" y seleccione "True Constant". Coloque la Constante dentro de la Estructura del Evento


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/dc46242b-379b-40d7-9e69-860070f1752a)

Conecte la constante a la condición de ciclo, como se muestra en la imagen a continuación


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/3fdd8ba7-f668-414c-a42d-b2a7b8b8797f)


El programa ahora se ejecutará exitosamente. Podrás encender y apagar los LED tantas veces como quieras. Puede utilizar el botón Stop para detener la ejecución del programa.

# Lección 5 - Numeros, Gráficas y Charts

Opcional: Configuración del Hardware
Conecta el hardware de la siguiente manera:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/97fc78a9-7876-422d-b74a-c75400bb1ffb)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/4d478f5a-b4c3-4f98-84bd-672c19c3b992)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/e2a09693-e729-4f72-b7af-9d67f6fa4efd)

## Instrucciones

### Entrada Analogica (Analog Input)

Hasta ahora has realizado programas usando entradas y salidas Digitales, es momento de revisar las entradas y salidas Analogicas. En esta leccion nos enfocaremos en las entradas Analogicas

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/f3772781-e5db-459d-a3c1-fc9bf1694eba)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/4bb4c9f0-a99d-4d62-ad71-b2231c1796c4)

* De igual manera que las lecciones anteriores, hay que comenzar con los VIs Initialize.vi y Close.vi en un nuevo diagrama de bloques (Block Diagram)

* De click derecho para sacar la palete de funciones (Functions Palette). Revisa la siguiente imagen para ubicar el VI ReadAI.vi y arrastrarlo al diagrama de bloques

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/e9606dd8-840e-4f37-aea6-ce94b8eeed83)

* Hay que conectar una constante dando click derecho en el VI ReadAI.vi y seleccionar 'Create Constant'

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/0a50edff-593b-4fb6-aec7-7740e40c36f4)

* Crea un indicador para el valor analogico en el lado derecho del VI

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/9f993dd9-e3f4-402b-94bf-2344cdac3703)

* Escribe el programa como la siguiente imagen

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/08b24200-3beb-475f-8bd2-2212003820e8)

_El programa se ejecutara exitosamente, pero, se ejecutara una sola vez, obteniendo solo una lectura del canal analogico seleccionado_

* Para resolver este problema, podemos agregar un ciclo While. Da click derecho para traer la paleta de funciones, luego navega a 'Structures' y selecciona 'While Loop'. Colocalo alrededor de el VI ReadAI.vi y deja espacio para otras funciones

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/60952926-50fc-49d2-8053-e6e6154ae2d2)

* Un ciclo While no funcionara sin una condicion de paro. En muchos casos se utiliza un simple boton boleano, da click derecho en la condicion de paro del While loop y selecciona 'Create Control', esto creara un boton en el panel frontal

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/e0016811-c6ed-4a52-9506-641d6eff7be3)


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/c6d726ba-6fed-4946-a9eb-ba4b943fa0ed)

* Puedes ejecutar el programa ahora y al girar las perillas analogicas el valor se mostrara en el panel frontal

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/e9b586b6-9b3f-4b26-a7fb-a0f1f894cdc9)

_Si estas utilizando el hardware fisico, notaras que el valor analogico leido estara brincando de un valor a otro, esto es hasta cierto punto normal y esta relacionado al ruido electromagnetico en el equipo._

* Para tener un mejor aspecto, se puede reemplazar el indicador numerico por un Waveform Chart, el cual desplegara los datos de manera continua, da click derecho en el indicador 'Value', y navega hasta la opcion de reemplazar, aparecera la paleta de controles y ahi podras elegir un waveform Chart

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/492827a5-558b-4301-a19c-5581588ef463)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/ad605cde-82e2-493c-a794-9fafdda85b73)



# Conceptos Generales

# Tipos de Datos

# Ciclos While


# Ciclos For

# Estructuras de Eventos





























