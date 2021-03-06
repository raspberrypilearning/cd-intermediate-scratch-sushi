## Líneas más atractivas

¡Hora de añadir color! En este momento, tu línea es de un color, pero el **Lápiz** tiene bloques que pueden cambiar su color. ¡Y con el bloque de **Operadores** correcto, incluso puedes cambiar el color al azar!

El bloque para cambiar el color del **Lápiz** es `cambiar color de lápiz por`{:class="block3extensions"}:

```blocks3
    change pen color by (10)
```

--- task ---

Toma uno de esos bloques y ponlo en tu bucle `repetir hasta que`{:class="block3control"}, así:

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (10)
        move (pasos) steps
        turn cw (grados ::variables) degrees
        change [pasos v] by (aumento ::variables)
    end
```

--- /task ---

Eso es genial, pero un poco predecible. Puedes hacerlo un poco más divertido si le agregas un número aleatorio, para que el color cambie al azar.

--- task ---

Pon el bloque número aleatorio del grupo **Operadores** en el bloque `cambiar color de lápiz por`{:class="block3extensions"} y escoge algunos valores para ponerle. Yo lo Intentaría con `1` y `100` para empezar.

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (pick random (1) to (100))
        move (pasos) steps
        turn cw (grados ::variables) degrees
        change [pasos v] by (aumento ::variables)
    end
```

--- /task ---

--- task ---

¡Intenta ejecutarlo de nuevo, y mira el arco iris aleatorio!

--- /task ---