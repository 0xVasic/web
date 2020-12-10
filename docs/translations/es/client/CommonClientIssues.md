---
title: Common Issues
---

## Contents

## Client

### Tengo constantemente el error "San Andreas cannot be found"

�San Andreas Multiplayer **NO ES** un programa independiente! Solo a�ade funciones multijugador al GTA: San Andreas (y, por lo tanto, necesitas GTA:SA instalado en tu computadora). Tiene que ser, adem�s, la versi�n **EU/US v1.0**, ya que otras versiones como 2.0, versiones de Steam o versiones de Direct2Drive no funcionar�n. [Cliquea aqu� para descargar un parche para downgradear tu GTA:SA a la version 1.0](http://grandtheftauto.filefront.com/file/GTA_SA_Downgrader_Patch;74661)

### No veo ning�n servidor en el buscador de servidores de SA:MP.

Primero que nada, aseg�rate de seguir los procedimientos previstos en la [Gu�a de inicio r�pido](https://wiki.sa-mp.com/wiki/Getting_Started). Si el problema persiste a�n si verificaste lo anterior, debes permitir el acceso de SA:MP a trav�s de tu cortafuegos. Desafortunadamente, debido a la gran cantidad de software cortafuego que existe, no podemos dar soporte con esto, pero sugerimos el revisar en el sitio del programa (o realizar una busqueda ante nuestro todo poderoso Google). Aseg�rate adem�s de tener la �ltima versi�n de SA:MP.

### El modo un jugador inicia en vez de SA:MP

:::warning

No se supone que debas ver las opciones del modo un jugador (Iniciar Partida, Cargar Partida, etc�tera) - SA:MP deber�a iniciarse por si solo y no presentar estas opciones. Si ves la opci�n de "Inciar Partida", se inici� el modo de un jugador en ves de SA:MP.

:::

El modo un jugador puede iniciarse por 2 razones: Tienes SA:MP instalado en la carpeta incorrecta o no tienes una versi�n compatible de GTA:SA. Si tienes la versi�n incorrecta puedes reallizar un downgrade a tu juego utilizando el downgrader de GTA:SA. Cliquea [aqu�](http://grandtheftauto.filefront.com/file/GTA_SA_Downgrader_Patch;74661) para descargarlo.

Existen ciertos casos en el que el men� del modo un jugador ser� mostrado, pero SA:MP habr� correctamente inciado. Para arreglar esto simplemente tienes que seleccionar un elemento en el men�, seguido de tocarla tecla Escape para salir de este. De esta forma, SA:MP proceder� a cargar.

### Obtengo el error "Unacceptable Nickname" cuando conecto a un servidor.


Aseg�rate de que no estas usando ningun car�cter no permitido (solo puedes utilizar n�meros del 0-9, letras de la A a la Z, \[\], (), \$, @, ., \_ y =), adem�s de asegurarte que tu nombre no supera los 20 car�cteres. Esto tambi�n podr�a ser causado cuando un jugador est� conectado en el servidor con el mismo nombre que t� (que puede pasar si reconectas a un servidor de manera r�pida antes de que el servidor registre tu desconexi�n). Un servidor de SA:MP corriendo en Windows durante mas de 50 d�as seguidos puede tambi�n ocasionar este bug.

### La pantalla se queda en "Connecting to  IP:Port..."

Esto puede ser causado porque el servidor no esta encendido. Si tienes este error con mas de 1 servidor y estas seguro que estos servidores no est�n apagados, deshabilita tu cortafuegos y comprueba si el error persiste. Caso contrario, reconfigura tu cortafuegos para aceptar el tr�fico entrante-saliente de SA:MP. Puede ser tambi�n que estes ejecutando una versi�n obsoleta de SA:MP - Puedes encontrar la versi�n m�s reciente [Aqu�](http://sa-mp.com/download.php).

### Tengo un GTA:SA modificado y SA:MP no inicia

Si SA:MP no inicia, intenta remover las modificaciones instaladas.

### Cuando ejecuto GTA con SA:MP no sucede nada (no inicia)

Borra gta_sa.set de tu carpeta "GTA San Andreas User Files", adem�s de asegurarte de que no tienes ningun cheat o modificaciones.

### El juego crashea (se cierra) cuando un veh�culo explota

Si tienes 2 monitores, hay 3 maneras de resolverlo:

1. Deshabilita tu segundo monitor cuando juegues SA:MP. (Quiz�s no sea lo mejor, pero es lo m�s rapido si no te importa el no poder utilizar el otro monitor).
2. Configura "Efectos Visuales" a Bajo (Escape > Opciones > Configuraci�n de pantalla > Avanzados).
3. Renombra tu carpeta de GTA:SA (ejemplo "GTA San Andreas2") (Esto puede funcionar a veces, de todas maneras a veces puede dejar de funcionar nuevamente as� que tienes que renombrarla de otra forma).

### Mi rat�n no funciona luego de slair del men� de pausa

Si tu rat�n no funciona en el juego y funciona de manera incompleta en el men� de pausa, deber�as desactivar la funci�n multin�cleo ("multicore") de tu[sa-mp.cfg](/web/20190421141207/https://wiki.sa-mp.com/wiki/Sa-mp.cfg "Sa-mp.cfg") (Colocala en 0). Pulsar repetidamente la tecla Escape o mantenerla apretada hasta que el rat�n responda de nuevo puede funcionar, pero no es una soluci�n definitiva.

### El archivo dinput8.dll no existe

Este problema puede aparecer cuando DirectX no esta instalado correctamente. Intenta reinstalarlo (no olvides de reiniciar tu PC). Si el problema persiste, solo ve a C:\\Windows\\System32 y copia el archivo dinput.dll a tu carpeta de GTA.

### No puedo ver los nombres de los dem�s jugadores

Por favor comprender que algunos servidores tienen sus nametags desactivados de forma global. De todas formas, este problema puede ocurrir en computadores con procesadores que incluyen gr�ficos integrados Intel HD (Que no estar�an exactamente hechos para gaming, a�n as�). Desafortunadamente, la causa exacta es desconocida y no parece haber ninguna forma de arreglarlo hasta ahora. Una soluci�n ser�a el instalar un procesador gr�fico dedicado (tarjeta de video) en tu computadora, siempre y cuando sea posible y tu presupuesto monetario te lo permita.
