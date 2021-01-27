---
layout: page_entregas
title: Preguntas frecuentes
subtitle: con respecto al DAW, plugins y producción musical en general
menubar_toc: true
toc_title: INDICE
---

## **Latencia**

Si esta teniendo problemas de latencia _(la diferencia de tiempo entre oprimir una tecla del piano y el momento en
el cual sale el sonido)_. Si esta utilizando windows y no tiene una interface de audio lo más probable es que este
utilizando los drivers de audio de windows, los cuales no son muy buenos para aplicaciones de sonido.

En caso de estar utilizando OSX lo mas probables es que el problema este en la configuración de su DAW.

Sabiendo esto vamos a dar soluciones a ambos problemas:

- ### Windows con interface

  Si esta utilizando una interface de audio primero debe asegurarse de de estar utilizando la versión más reciente  
  de los drivers de la interface.

  Una vez instalados los drivers abrir el panel de configuración de los drivers y seleccionar un tamaño de buffer
  **(Buffer Size)** igual o menor a **512** samples, mientras más pequeño sea este número menor sera la latencia
  pero mayor sera la carga en la CPU del computador, mi recomendación es manejar un buffer size entre **128** y
  **256** samples siempre y cuando el computador lo permita _(no suenan distorsiones, clicks o pops al reproducir audio)_

  Tambien puede acceder al panel de configuración de los drivers desde el DAW. Para acceder a este menu abra su DAW,
  entre a las preferencias `ctrl + ,` para ableton live o ir a `opciones > preferencias` y ubicar la pestaña de audio
  En la sección de "Driver" seleccionar "ASIO" y en la sección "Dispositivo de Audio (Audio Device)" seleccionar su
  interface, una vez seleccionado el driver y el dispositivo de audio hacer click en el botón de "Hardware Setup" y
  seleccionar un Buffer Size **128** samples o menor.
  <br />
  <br />

- ### Windows sin interface

  En el caso de no tener una interface de audio descargar versión más reciente de [ASIO4ALL](https://www.asio4all.org/),
  instalarlo y reiniciar el equipo.

  Una vez realizado este proceso abrir su DAW de preferencia _(En este caso voy a demostrar en Ableton Live pero el proceso
  es el mismo en otros DAWS)_, abrir las preferencias `ctrl + ,` o ir a `opciones > preferencias` y ubicar la pestaña de audio
  En la sección de "Driver" seleccionar "ASIO" y en la sección "Dispositivo de Audio (Audio Device)" seleccionar "ASIO4ALL",
  una vez seleccionado el driver y el dispositivo de audio hacer click en el boton de hardware setup y bajar el slider a **128**
  samples.

  En este punto la latencia debe de estar a un nivel aceptable para poder producir música de manera cómoda y agradable.

{% include notification.html
  message= "El driver de **ASIO4ALL** se apodera del sonido del equipo por lo cual es **NORMAL** que **NO** funcione el audio en ninguna
  otra aplicación excepto el DAW en el cual se esta trabajando, tambien es normal que los videos de youtube no se reproduzcan más
  y muestren un error. Todo volvera a la normalidad una vez cierre el DAW o cambie el Driver de Audio"
  status = "is-warning"
%}

- ### OSX

  El procedimiento es muy parecido al que se sigue en windows pero gracias al "Core Audio" es un poco mas sencillo de controlar la latencia
  del sistema.

  Para reducir la latencia en OSX se hace directamente desde el DAW, entrando en las preferencias de audio, para Ableton Live el atajo es
  `cmd + ,`, ir a la pestaña de audio y seleccionar como "Driver" **Core Audio** y en "Dispositivo de Audio" La salida de audio que quiera
  utilizar, sea de una interface o la integrada luego en en la pestaña de **"Buffer Size"** seleccionar un tamaño de Buffer igual o menor
  a 512 samples.

  Con estos pasos los problemas de la latencia deberian quedar solucionados.

---

## **No tengo un controlador midi. ¿Qué puedo hacer?**

<br />

### Teclado del computador

En caso de necesitar una mejor herramienta para crear melodías y armonías una opcion que todos tenemos disponible es utilizar el teclado
del computador controlador midi y afortunadamente tanto Reaper como Ableton Live nos permiten hacer esto.

- ### Ableton Live

  En Ableton Live existen varias maneras para activar o descativar el declado virtual:

  1. Oprimir la tecla `M` para activar o desactivar el teclado virtual.
  2. Ir a `opciones > teclado MIDI del Computador` para activar o desactivar el teclado virtual.
  3. Hacer click en el símbolo de teclado en la esquina superior derecha junto al botón de `key`
     ![Ableton-key-button](/img/faq/ableton-virtualkeyboard-button.jpg)

  Con cualquiera de estas opciones ya tenemos disponible un teclado de una octava al cual se le puede variar la altura con las
  teclas `X` y `Z` respectivamente
  ![Ableton-keymap](/img/faq/key-map.png)

  <sub><sup>Imagen tomada de [soundfly.com](https://flypaper.soundfly.com/produce/make-your-first-beat-in-ableton-live-making-sound-recording-midi/)</sup></sub>

  <br /><br />

- ### Reaper

  Al igual que Ableton Live, Reaper ofrece un **_"piano"_** virtual con el teclado del computador, pero en el caso de Reaper
  este **_"piano"_** ofrece una mayor cantidad de notas 2 octavas y 4 notas haciendo uso de una mayor cantidad de teclas y
  utilizando una distribución diferente a la de Ableton Live.

  Para activar el teclado virtual existen dos opciones:

  1. Ir a `View > Virtual Midi Keybooard`
  2. Oprimir la combinación`Alt+B`

  ![Reaper-keymap](/img/faq/reaper_keymap.jpg)<br />
  <sub><sup>Imagen tomada de [Cockos Forum](https://forum.cockos.com/showthread.php?t=222635)</sup></sub>

{% include notification.html
  message = "Para que el ***'piano'*** en Reaper funcione correctamente hay que **enfocar/seleccionar** la ventana flotante
  de este al momento de ir a tocar, ya que si no se hace esto el teclado virtual **NO** funcionara "
  status = "is-warning"
%}

<!-- ### Smartphone como controlador midi

Otra buena opcion y que nos permite tener diferrentes superficies de control en un solo dispositivo es utilizar un smartphone o una tablet
como controlador midi.

En el mercado existen muchas opciones de aplicaciones para conseguir este objetivo tanto para Android como para IOS, pero aqui solo vamos a
mencionar las opciones gratuitas y como utilizarlos con Windows O OSX -->
