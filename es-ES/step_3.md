## Patrones de dibujo

Ahora tienes un programa que dibuja una línea, pero una solamente. ¡Eso es un poco aburrido! Podrias usar un bucle `por siempre`{:class="block3control"} para dibujar algo una y otra vez, ¡pero entonces obtendrás dibujos que saldrán del escenario!

Así que necesitas usar un tipo diferente de bucle llamado `repetir hasta que`{:class="block3control"}, que también encontrarás en la sección **Control**. Este tipo de bucle hará algo una y otra vez, **hasta que** una condición Verdadero/Falso se cumple.

--- task ---

Toma un bloque `repetir hasta que`{:class="block3control"} de la sección **Control** y pon los bloques `mover`{:class="block3motion"} y `girar`{:class="block3motion"} en su interior, así:

```blocks3
+    repeat until <> 
        move (50) steps
        turn cw (15) degrees
    end
```

--- /task ---

--- task ---

Ahora haz clic en la bandera verde unas cuantas veces y observa lo que sucede. Te darás cuenta de dos cosas: el lápiz siempre comienza dibujando una línea hacia el medio del escenario, y no se detiene en el borde.

--- /task ---

--- collapse ---
---
title: ¿Por qué el lápiz hace esto?
---

El lápiz siempre comienza a dibujar dirigiéndose hacia el medio, porque el primer bloque **Movimiento** que se ejecuta después del `bajar lápiz`{:class="block3extensions"} es `ir a x: 0 y: 0`{:class="block3motion"}. Entonces, el lápiz dibujará una línea a medida que se mueve hacia el centro del escenario.

El lápiz no se detiene en el borde del escenario, porque aún no le has dicho al bloque del bucle `repetir hasta que`{:class="block3control"} qué condición tiene que comprobar. Esto significa que la condición nunca se puede cumplir, por lo que el bucle se ejecutará una y otra vez. Esto implica que en este momento, el bucle está funcionando como un bucle `por siempre`{:class="block3control"}.

--- /collapse ---

--- task ---

Mueve el bloque `ir a x: 0 y: 0`{:class="block3motion"} antes del bloque `bajar lápiz`{:class="block3extensions"} y añade, desde la sección **Lápiz**, un bloque `subir lápiz`{:class="block3extensions"} justo al principio de tu código.

--- /task ---

Es hora de arreglar la repetición del bucle `repetir hasta que`{:class="block3control"} para que se detenga cuando quieras. Estás buscando averiguar si el objeto (invisible) está tocando el borde del escenario, por lo que necesitas un bloque **Sensores** — en este caso, el bloque `¿tocando?`{:class="block3sensing"} .

--- task ---

Añade un bloque `¿tocando?`{:class="block3sensing"} en tu bucle `repetir hasta que`{:class="block3control"} y selecciona `borde`{:class="block3sensing"} . Ahora, el bucle continuará **hasta que** el objeto (invisible) toque el borde del escenario.

```blocks3
    pen down
+    repeat until <touching [edge v] ?> 
        move (50) steps
        turn cw (15) degrees
    end
```

--- /task ---

--- task ---

Cambia el número de pasos en el bloque `mover`{:class="block3motion"} a `5`, y comprueba que tu programa coincida con éste antes de probarlo:

```blocks3
    when green flag clicked
    pen up
    hide
    clear
    go to x: (0) y: (0)
    set pen color to [#4a6cd4]
    pen down
    repeat until <touching [edge v] ?> 
        move (5) steps
        turn cw (15) degrees
    end
```

--- /task ---

Si ejecutas el código ahora, verás que el dibujo que hace el lápiz se queda en el escenario.

¡No solo eso, sino que tu programa se ha convertido en un programa para dibujar círculos! Lo que está sucediendo aquí es que esos giros de 15 grados eventualmente suman 360 grados, por lo que tu lápiz se gira un círculo completo. Vas a cambiar ligeramente la forma en que se mueve para que cada vez de un paso un poco más largo, por lo que se moverá en espiral. Para esto, vas a necesitar una **variable**.

Las variables son básicamente lugares etiquetados para almacenar números u otra información que te interese. Puedes crearlas en la sección de los bloques **Variables**.

--- task ---

Haz una variable llamada `pasos`{:class="block3variables"}, y luego añade el bloque `dar a pasos el valor 0`{:class="block3variables"} al comienzo de tu programa.

```blocks3
    when green flag clicked
+   set [pasos v] to [0]
    pen up
```

--- /task ---

--- task ---

Luego usa el valor de `pasos`{:class="block3variables"} en lugar de `5` en el bloque `mover`{:class="block3motion"} y añade `sumar a pasos 1`{:class="block3variables"} como parte de tu bucle:

```blocks3
    pen down
    repeat until <touching [edge v] ?> 
+       move (pasos) steps
        turn cw (76) degrees
+        change [pasos v] by (1)
    end
```

--- /task ---

¿Crees que importa en que parte del bucle pones el bloque `sumar a pasos 1`{:class="block3variables"}?

--- collapse ---
---
title: Poniendo el código en el orden correcto
---

Cuando estés decidiendo en qué orden poner los bloques, piensa qué hace cada uno y qué quieres que haga tu código.

En este caso, deseas que la pluma se mueva, luego gire, una y otra vez. Cada vez que lo hace, quieres que se mueva un paso más.

Así que tiene sentido poner el bloque `sumar a pasos 1`{:class="block3variables"} **después** del bloque `mover`{:class="block3motion"}. Sin embargo, después de moverse, realmente no importa si el lápiz gira primero y luego cambia el número de pasos, o si el número de pasos cambia primero y luego el lápiz gira.

--- /collapse ---

--- task ---

Ahora ejecuta el programa, y también intenta cambiar el número de grados (¡Prueba `76` y `120`)!

--- /task ---