CHANGELOG 1.9 --> 1.9.1:
- Ajustes finales en las variables de usuario.
- Optimización, eliminadas variables no necesarias.

CHANGELOG 1.8 --> 1.9:
- Nueva variable de usuario para controlar la cadencia en los auto_progresivos.
- Refactorización y modificación de métodos para trabajar en escala analógica con los valores del acelerador por dabadg (https://github.com/dabadg).
- Añadida variable para elegir entre modos de crucero en la asistencia a 6 km/h y mejorada la respuesta en este modo.
- Optimizaciones, correcciones y limpieza de código.
- Nuevo método para establecer crucero sólo cuando se pedalea por dabadg (https://github.com/dabadg).

CHANGELOG 1.7.1 --> 1.8:
- Recuperado nivel inicial en el progresivo.
- 2 variables nuevas llamadas cadencia1 y cadencia2 para configurar por el usuario, dependiendo de si arrancamos la bici normal o con el freno pulsado (activa la asistencia a 6 km/h desde parado).
- Re estructuración del loop:
  - Lee Acelerador, Manda acelerador y contador de pulsos se ejecutan sin retardo.
  - Las comprobaciones de cadencia se hacen cada 250 ms.
  - Establece crucero cada 125 ms.
- Añadido buzzer para emitir avisos y refactorización de funciones por dabadg (https://github.com/dabadg).
- Correcciones menores.
- Añadido en comentarios nuevas secciones:
  - Autoprogresivos.
  - Developers.
  - Agradecimientos.

CHANGELOG 1.7 --> 1.7.1:
- Corregida duración de 30 sg del bucle de la asistencia a 6km/h.

CHANGELOG 1.6 --> 1.7:
- Modificada asistencia a 6 km/h desde parado.
  - Se sale de la asistencia a 6kmh soltando acelerador o pedaleando.
    - Soltando acelerador (pedales parados) "no borra" crucero, si lo hubiera.
    - Pedalenado (sin soltar acelerador), prevalece el acelerador. 

CHANGELOG 1.5 --> 1.6:
- Mejorada respuesta en fijación del crucero.

CHANGELOG 1.4 --> 1.5:
- Corta crucero al dejar de usar la asistencia a 6 km/h.

CHANGELOG 1.3 --> 1.4:
- Lectura del acelerador sin afectación del tiempo de cadencia.
- Establece crucero controlado por millis().

CHANGELOG 1.2 --> 1.3:
- Eliminado nivel inicial del progresivo.
- Actualizados comentarios.

CHANGELOG 1.1 --> 1.2:
- Activado de nuevo desacelera_al_parar_pedal por defecto y corregido su comportamiento.
- Pequeña modificación en cálculo del autoprogresivo.

CHANGELOG 1.0 --> 1.1:
- Añadida posibilidad de activar ayuda de 6km/h desde parado mientras se usa el acelerador, accionando el freno al arrancar.
- Corregido temporizador del retardo_paro_motor.
- Por defecto retardo_paro_motor = 0.50.
- Desactivado temporalmente desacelera_al_parar_pedal.
