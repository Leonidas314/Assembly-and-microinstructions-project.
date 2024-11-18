
Lo primero que hacemos es crear los dos registros necesarios para almacenar temporalmente las direcciones de memoria del arreglo pasado y de la direccion donde va a ser copiado el arreglo.

Decidimos que los registros fuente (si) y destino (di) tendran un espacio de 16 bits dado que asi tendran la posibilidad de usarse como proposito general.

Al tener un registro de 16 (si y di) podemos pasar la direccion del mar directamente y saltarnos el paso al registr mdr.

Debemos crear una microinstruccion que limpie lso registros si y di ya que al ser usados en algun proposito general qudaran con 16 bist cargados y luego al usarse como direcciones solo se necesitan 12, lo que puede genera algun problema.

Al crear la microinstruccion el "StartBitDest" es 4 cuando el source register es mar, ya que mar es de 12 bits y decidimos ocupar los ultimos doce bits los registros si y di desde el 4 en adelante por CONVENSION. 