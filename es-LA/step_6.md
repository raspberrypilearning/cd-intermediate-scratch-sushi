## Todo en aleatorio

En realidad, puedes usar números aleatorios para hacer que todo el programa se ejecute una y otra vez, ¡cambiando el patrón cada vez! Se verá un poco como los protectores de pantalla en la década de 1990... que probablemente no recordarás, ¡pero pregúntale a uno de tus padres!

Necesitas algunos cambios para que esto suceda. El primero es que necesitas establecer las variables `aumento`{:class="block3variables"} y `grados`{:class="block3variables"} aleatoriamente en lugar de pedirlas al usuario. Así que necesitas cambiar algunos de tus bloques de código.

--- task ---

Elimina las preguntas de tu código y actualízalo para usar números aleatorios en su lugar.

```blocks3
    when green flag clicked
    set [pasos v] to [0]
-    ask [¿Cuántos pasos debo aumentar?] and wait
+    set [aumento v] to (pick random (1) to (10))
-    ask [¿Cuántos grados debo girar?] and wait
+    set [grados v] to (pick random (1) to (180))
    pen up
```

--- /task ---

Si ejecutas tu programa ahora, verás que dibuja un patrón aleatorio, pero sólo una vez. ¿Por qué crees que es así?

Es porque el bucle solo se ejecuta hasta que llega al borde del escenario.

--- task ---

Necesitas otro bucle que se ejecute para siempre (un bloque `por siempre`{:class="block3control"} entonces) fuera del ciclo actual para que continúe una y otra vez. Solo arrastra uno de la sección **Control** y añade todo el código dentro de él.

```blocks3
    when green flag clicked
+    forever 
        set [pasos v] to [0]
        set [aumento v] to (pick random (1) to (10))
        set [grados v] to (pick random (1) to (180))
        pen up
        hide
        clear
        go to x: (0) y: (0)
        set pen color to [#4a6cd4]
        pen down
        repeat until <touching [edge v] ?> 
            move (pasos) steps
            turn cw (grados) degrees
            change [pasos v] by (aumento)
        end
    end
```

--- /task ---

¡Ahora realmente tienes algo increíble para admirar!

Sin embargo, puedes notar que, de vez en cuando, la computadora dibuja algo que se ve bastante... mal. Esto es debido a que algunos números para algunas de esas variables son sólo malas opciones, y algunas **combinaciones de esos números** también son malas opciones.

En la siguiente tarjeta, ¡ayudarás a la computadora a elegir sólo buenas combinaciones!