#README

    bluedetecth es una pequeña utilidad que se encarga de bloquear la pantalla
    cuando el usuario se aleja del PC en el que se está ejecutando.
    Copyright (C) <2011> <Miguel Ponce Torres>

    Este programa es software libre: usted puede redistribuirlo y / o modificar
    bajo los términos de la GNU General Public License publicada por
    la Free Software Foundation, bien de la versión 3 de la Licencia, o
    (A su elección) cualquier versión posterior.

    Este programa se distribuye con la esperanza de que sea útil,
    pero SIN NINGUNA GARANTÍA, incluso sin la garantía implícita de
    COMERCIALIZACIÓN o IDONEIDAD PARA UN PROPÓSITO PARTICULAR. Consulte la
    Licencia Pública General GNU para más detalles.

    Debería haber recibido una copia de la Licencia Pública General GNU
    junto con este programa. Si no, vea <http://www.gnu.org/licenses/>.

    Si quiere contactar con <Miguel Ponce Torres> puede hacerlo en: miguelponcetorres@gmail.com

    Este script usa la idea original de Javier Perez
    <http://javierperez.eu/bloqueo-y-desbloqueo-de-pantalla-por-detector-de-presencia-en-ubuntu-con-bluetooth-aimtooth/>
    pero se han añadido muchos más extras y más facilidad de uso que en el script original no tenía.

    Este script está preparado para andar en Gnome, para que funcione en KDE u otros
    escritorios hay que cambiar la orden zinety por la adecuada para KDE u otros.



INSTALACIÓN:

Copia esta carpeta y todo el contenido en tu carpeta personal, luego ejecúta el script llamado "bluedetecth", este le guiará tras la primera ejecución.



FUNCIONAMIENTO:

Ejecute "bluedetecth" para arrancarlo, y si quieres pararlo vuelve a ejecutarlo y él mismo se encargará de parar el script tras tu confirmación.

Asegúrate de tener el bluetooth encendido, "bluedetecth" te avisará tambien.
Se hará un barrido y te mostrará los dispositivos encontrados.

Tras elegir uno de los dispositivos de la lista, "bluedetecth" comprobará si en su base de datos existen referencias del aparato, si no es así, le pedirá permiso para añadirlo a su base de datos.

El punto anterior es importante ya que cada dispositivo puede ser muy diferente y el nivel de potencia puede oscilar mucho.
Si se aborta esta operación bluedetecth usará valores estandar muy por debajo de lo normal y bastante seguros.

Una vez todo concluido, bluedetecth comprobará la calidad de la señal del terminal elegido y si baja de los límites de seguridad la pantalla se bloquea.


NOTA:

"bluedetecth" usa herramientas que suelen pertencer a root, por tanto, habrá momentos en los que el programa le pida dicha contraseña.


DESBLOQUEO DE EMERGENCIA

Si por cualquier motivo el terminal al que se está enlazado no es accesible (porque se le desactive el bluetooth, se apage por batería baja, etc) "bluedetecth"
mantendrá su pantalla bloqueada hasta que se vuelva a localizar el terminal.
Para solucionar este problema en caso de que el terminal no pueda volver a estar disponible, usted puede apretar Ctrl+ALT+F1 se abrirá una consola "tty1" en ella
podrá identificarse, luego pondrá su contraseña y por ultimo podrá meter el siguiente comando para matar el proseso de "bluedetecth".

$ killall bluedetecth
$ exit

Presione Ctrl+ALT+F7 para ir a la interfaz gráfica, y una vez ahí podrá meter la contraseña y desbloquear su cuenta.


< miguelponcetorres@gmail.com | http://pc-citos.blogspot.com >
