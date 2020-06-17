## Utilizar la herramienta Lápiz

El proyecto que vas a realizar se basa en la herramienta **Lápiz**, que dibuja una línea detrás del centro de un objeto a medida que se mueve. ¡Aprenderás a usarla ahora!

\--- task \---

Crea una carpeta nueva en Scratch, selecciona el objeto Gato Scratch y arrastra algunos bloques que posiblemente ya hayas visto, hasta que se vea así:

```blocks3
    when green flag clicked
    go to x: (0) y: (0)
    move (50) steps
    turn cw (15) degrees
```

\--- /task \---

Ahora, ¡es hora de probar el lápiz!

Para utilizar los bloques Lápiz en Scratch, necesitas agregar la **extensión de Lápiz**.

\--- task \---

Haz clic en el botón **Añadir extensión** en la esquina inferior izquierda.

![añadir botón de extensión resaltado](images/add-extension-annotated.png)

Clic en la extensión **Lápiz** para agregarla.

![extensión de lápiz resaltada](images/click-pen-annotated.png)

La sección Lápiz ahora aparece en la parte inferior del menú de bloques.

![bloques de extensión Lápiz](images/pen-extension-blocks.png)

En la sección **Lápiz**, selecciona el bloque `bajar lápiz`{:class = "block3extensions"} y agrégalo al inicio del programa, de esta manera:

```blocks3
    when green flag clicked
+    pen down
    go to x: (0) y: (0)
```

\--- /task \---

\--- task \---

Ahora haz clic en la bandera verde unas cuantas veces y observa lo que sucede.

\--- /task \---

Si puedes ver las líneas detrás del objeto gato, entonces el lápiz está funcionando y puedes comenzar a dibujar patrones realmente geniales.

Primero, debes deshacerte del objeto. ¡Se está interponiendo en el camino del dibujo!

\--- task \---

Agrega un bloque `esconder`{:class = "block3looks"} en **Apariencia** al inicio del programa y desaparecerá.

```blocks3
    when green flag clicked
+    hide
    pen down
```

\--- /task \---

Ahora, puedes cambiar el color del lápiz con otro bloque de la sección **Lápiz**, pero ese bloque es un poco diferente a los otros que has visto. Es el bloque `fijar color de lápiz a`{:class = "block3extensions"} y se ve así:

```blocks3
    set pen color to [#4a6cd4]
```

\--- task \---

Arrastra un bloque `fijar color de lápiz a `{:class="block3extensions"} a tu panel de objetos, e insertalo por encima del bloque `bajar lápiz`{:class="block3extensions"}.

```blocks3
    when green flag clicked
    hide
+    set pen color to [#4a6cd4]
    pen down
```

Ahora, haz clic en el cuadro de color (en el código de arriba es el azul) y elije un color.

\--- /task \---

Si has estado haciendo clic en la bandera verde para probar tu código, te habrás dado cuenta que los dibujos que hace el lápiz no desaparecen.

\--- task \---

Agrega un bloque `borrar todo`{:class="block3extensions"} de la sección **lápiz** al principio de tu código para solucionar eso:

```blocks3
    when green flag clicked
+    clear
    hide
```

\--- /task \---