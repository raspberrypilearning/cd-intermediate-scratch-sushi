## Pidiendo valores de entrada

Ok, esto se está poniendo interesante, pero es un poco aburrido tener que editar el código cada vez que quieres dibujar un patrón diferente. ¿No sería bueno hacer que el programa te pida los valores que tiene que usar? ¡Puedes hacerlo!

--- task ---

Primero, ve a la sección **Variables** y crea unas variables llamadas `grados`{:class="block3variables"} y `aumento`{:class="block3variables"}.

--- /task ---

--- task ---

Ahora añade las nuevas variables a tu código así:

```blocks3
    repeat until <touching [edge v] ?> 
        move (pasos) steps
        turn cw (grados ::variables) degrees
        change [pasos v] by (aumento ::variables)
    end
```

--- /task ---

Ahora necesitas pedir los valores para estas dos variables y almacenarlas. Para hacer esto usa un bloque **Sensores** llamado `Preguntar y esperar`{:class="block3sensing"}, en el que puedes escribir una pregunta.

--- task ---

Agrega el bloque `Preguntar y esperar`{:class="block3sensing"} al panel de objeto y cambiar la pregunta a `¿Cuántos pasos debo aumentar?`{:class="block3sensing"}

Luego añádelo a tu programa, justo después de dar a `pasos`{:class="block3variables"} el valor `0`, de esta manera:

```blocks3
    when green flag clicked
    set [pasos v] to [0]
+    ask [¿Cuántos pasos debo aumentar?] and wait
    pen up
```

--- /task ---

Ahora que conseguiste que tu programa haga una pregunta, ¡necesitas que recuerde la respuesta! Resulta que Scratch tiene una variable especial llamada `respuesta`{:class="block3sensing"}, donde almacena la respuesta más reciente que ha recibido. Puede encontrar esta variable entre los bloques **Sensores**.

--- task ---

Usa el bloque `dar a el valor`{:class="block3variables"} desde el grupo **Variables**, dale el valor de `respuesta`{:class="block3sensing"} y guárdalo en la variable `aumento`{:class="block3variables"} de esta forma:

```blocks3
    ask [¿Cuántos pasos debo aumentar?] and wait
+    set [aumento v] to (answer)
```

--- /task ---

--- task ---

Ahora, haz lo mismo con `grados`{:class="block3variables"}, preguntando `¿Cuántos grados debo girar?`{:class="block3sensing"} y almacena el valor de `respuesta`{:class="block3sensing"} en `grados`{:class="block3variables"}:

```blocks3
    set [aumento v] to (answer)
+    ask [¿Cuántos grados debo girar?] and wait
+    set [grados v] to (answer)
```

--- /task ---

--- task ---

Comprueba que tu programa se vea como el que aparece abajo, y ejecútalo unas cuantas veces con diferentes números. Escribe las respuestas que crean las mejores imágenes. ¡Las necesitarás más tarde!

```blocks3
    when green flag clicked
    set [pasos v] to [0]
    ask [¿Cuántos pasos debo aumentar?] and wait
    set [aumento v] to (answer)
    ask [¿Cuántos grados debo girar?] and wait
    set [grados v] to (answer)
    pen up
    hide
    clear
    go to x: (0) y: (0)
    set pen color to [#4a6cd4]
    pen down
    repeat until <touching [edge v] ?> 
        move (pasos) steps
        turn cw (grados) degrees
        change [pasos v] by (increase)
    end
```

--- /task ---