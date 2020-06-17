## Todo en aleatorio

En realidad, puedes usar números aleatorios para hacer que todo el programa se ejecute una y otra vez, ¡cambiando el patrón cada vez! Se verá un poco como los protectores de pantalla en la década de 1990... que probablemente no recordarás, ¡pero pregúntale a uno de tus padres!

Necesitas algunos cambios para que esto suceda. El primero es que necesitas establecer las variables `aumento`{:class="block3variables"} y `grados`{:class="block3variables"} aleatoriamente en lugar de pedirlas al usuario. Así que necesitas cambiar algunos de tus bloques de código.

\--- task \---

Elimina las preguntas de tu código y actualízalo para usar números aleatorios en su lugar.

```blocks3
    when green flag clicked
    set [steps v] to [0]
-    ask [How many steps should I grow by?] and wait
+    set [increase v] to (pick random (1) to (10))
-    ask [How many degrees should I turn?] and wait
+    set [degrees v] to (pick random (1) to (180))
    pen up
```

\--- /task \---

Si ejecutas tu programa ahora, verás que dibuja un patrón aleatorio, pero sólo una vez. ¿Por qué crees que es así?

Es porque el bucle solo se ejecuta hasta que llega al borde del escenario.

\--- task \---

Necesitas otro bucle que se ejecute para siempre (un bloque `por siempre` entonces {:class="block3control"}) fuera del ciclo actual para que continúe una y otra vez. Solo arrastra uno de la sección **Control** y añade todo el código dentro de él.

```blocks3
    when green flag clicked
+    forever 
        set [steps v] to [0]
        set [increase v] to (pick random (1) to (10))
        set [degrees v] to (pick random (1) to (180))
        pen up
        hide
        clear
        go to x: (0) y: (0)
        set pen color to [#4a6cd4]
        pen down
        repeat until <touching [edge v] ?> 
            move (steps) steps
            turn cw (degrees) degrees
            change [steps v] by (increase)
        end
    end
```

\--- /task \---

¡Ahora realmente tienes algo increíble para admirar!

Sin embargo, puedes notar que, de vez en cuando, la computadora dibuja algo que se ve bastante... mal. Esto es debido a que algunos números para algunas de esas variables son sólo malas opciones, y algunas **combinaciones de esos números** también son malas opciones.

En la siguiente tarjeta, ¡ayudarás a la computadora a elegir sólo buenas combinaciones!